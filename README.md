# 📜 Relatório

**Nome do Estagiário: Ricardo Silva**  
**Data: 30/08/2024**

**Módulos/Etapas Feitas:**  
1. **Docker**
2. **MinIO**
3. **Zeppelin**

***

## 📚 Resumo da Tarefa
&nbsp;

### 💫 Primeiros Passos
- **Primeiro iniciamos o Docker via VSCode; importamos o arquivo csv do repositóito do desafio.**
- **Iniciamos o bucket no MinIO _(localhost:9001)_**
- **Posteriormente criamos um novo _note_ no Zeppelin _(localhost:80080)_ e importamos a base dados conforme o caminho do MinIO.**
- **Iniciamos as Query conforme solicitado no desafio**

**Obs: O arquivo em SQL se encontra na pasta assets deste repositório.**
***



### 1. **Criação das tabelas**
~~~
%hive

CREATE TABLE campaigns (
    lines BIGINT,
    id_campaign STRING,
    type_campaign STRING,
    days_valid STRING,
    data_campaign STRING,
    channel STRING,
    return_status STRING,
    return_date STRING,
    client_id STRING
) ROW FORMAT DELIMITED
FIELDS TERMINATED BY ','
STORED AS TEXTFILE
LOCATION 's3a://datasets/campaign_data/'
TBLPROPERTIES ("skip.header.line.count"="1")
~~~

~~~
%hive

CREATE TABLE purchases (
    purchase_id STRING,
    product_name STRING,
    product_id STRING,
    amount INT,
    price DECIMAL(10, 2),
    discount_applied DOUBLE,
    payment_method STRING,
    purchase_datetime TIMESTAMP,
    purchase_location STRING,
    client_id STRING
) ROW FORMAT DELIMITED
FIELDS TERMINATED BY ','
STORED AS TEXTFILE
LOCATION 's3a://datasets/purcashe_data/'
TBLPROPERTIES ("skip.header.line.count"="1")
~~~

<br>

### 2. **Carregar Datasets**
~~~
%hive

LOAD DATA INPATH 's3a://datasets/campaigns_2023_hist.csv' INTO TABLE campaigns
~~~
~~~
%hive

LOAD DATA INPATH 's3a://datasets/purchases_2023.csv' INTO TABLE purchases
~~~
<br>

### 3. **Selecionar tabelas**
~~~
%hive
SELECT * FROM campaigns
~~~
~~~
%hive
SELECT * FROM purchases
~~~

<br>

### 4. **Normalização de dados conforme solicitado**
~~~
%hive
SELECT
    client_id,
    ROUND(SUM(price * amount * discount_applied), 2) AS total_price,
    MAX(purchase_location) AS most_purchase_location,
    DATE_FORMAT(MIN(purchase_datetime), 'yyyy-MM-dd HH:mm') AS first_purchase,
    DATE_FORMAT(MAX(purchase_datetime), 'yyyy-MM-dd HH:mm') AS last_purchase
FROM purchases
~~~

<br>

### 5. **Query para _most campaign_**

~~~
%hive

SELECT 
    client_id, 
    SUM(CASE WHEN return_status != 'error' THEN 1 ELSE 0 END) AS most_campaign,
        SUM(CASE WHEN return_status = 'error' THEN 1 ELSE 0 END) AS quantity_error
FROM 
    campaigns
GROUP BY 
    client_id
~~~

<br>

### 6. **Query para _quantity error_**

~~~
%hive

SELECT
    id_campaign,
    COUNT(*) AS quantity_error
FROM
    campaigns
WHERE
    return_status = 'sms'
GROUP BY
    id_campaign
~~~

<br>

### 7. **Script completo**
~~~
%hive

SELECT
    p.client_id,
    ROUND(SUM(p.price * p.amount * p.discount_applied), 2) AS total_price,
    MAX(p.purchase_location) AS most_purchase_location,
    DATE_FORMAT(MIN(p.purchase_datetime), 'yyyy-MM-dd HH:mm') AS first_purchase,
    DATE_FORMAT(MAX(p.purchase_datetime), 'yyyy-MM-dd HH:mm') AS last_purchase,
    COALESCE(MAX(c.most_campaign), 0) AS most_campaign,
    COALESCE(MAX(c.quantity_error), 0) AS quantity_error
FROM 
    purchases p
LEFT JOIN (
    SELECT 
        client_id, 
        SUM(CASE WHEN return_status != 'error' THEN 1 ELSE 0 END) AS most_campaign,
        SUM(CASE WHEN return_status = 'error' THEN 1 ELSE 0 END) AS quantity_error
    FROM 
        campaigns
    GROUP BY 
        client_id
) c
ON p.client_id = c.client_id
GROUP BY 
    p.client_id
~~~
***
