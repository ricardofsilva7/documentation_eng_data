# 📜 Relatório

**Nome do Estagiário: Ricardo Silva**  
**Data: 20/08/2024**

**Módulos/Etapas Feitas:**  
1. **Docker**
2. **MinIO**
3. **Zeppelin**

***

## 📚 Resumo do Desafio 
&nbsp;

### 💫 Primeiros Passos
- **Primeiro iniciamos o Docker via VSCode; importamos o arquivo csv do repositóito do desafio.**
- **Iniciamos o bucket no MinIO _(localhost:9001)_**
- **Posteriormente criamos um novo _note_ no Zeppelin _(localhost:80080)_ e importamos a base dados conforme o caminho do MinIO.**
- **Iniciamos as Query conforme solicitado no desafio**

<br>

### 1. **Importando o banco de dados**
~~~
%livy.pyspark
df = spark.read.option("header","true").csv("s3a://desafio-docker/purchases_2023.csv")
df.show()
~~~

<br>

### 2. **Selecionando por data (30 dias)**
~~~
%livy.pyspark
df.filter(df["purchase_datetime"].between("2023-04-01", "2023-04-31")).show()
~~~
<br>

### 3. **Selceionar colunas mais importantes**
~~~
%livy.pyspark
df.select("product_id", "amount", "price","discount_applied", "payment_method", "purchase_datetime","purchase_location", "client_id").show()
~~~

**Obs: Como não sabemos qual o objetivo da consulta, considerei que todos são importantes.**


<br>

### 4. **Tratamento de dados**
~~~
%livy.pyspark
from pyspark.sql.functions import round

df_around = df.withColumn("price", round(col("price"), 2))

df_around.show()
~~~

### 5. **Pipeline - Airflow**

<br>

**Primeiro deve alterar as variáveis**
~~~
%livy.pyspark
df_date = df_date.withColumn("amount", col("amount").cast("int"))
df_date = df_date.withColumn("discount_applied", col("discount_applied").cast("double"))
df_date = df_date.withColumn("purchase_datetime", col("purchase_datetime").cast("timestamp"))
df_date = df_date.withColumn("date_hour", col("date_hour").cast("timestamp"))
df_date.printSchema()
~~~
<br>

**Posteriormente, criamos a tabela para pode enviar ao Airflow**
~~~
%livy.pyspark
df_date = df_date.withColumn("amount", col("amount").cast("int"))
df_date = df_date.withColumn("discount_applied", col("discount_applied").cast("double"))
df_date = df_date.withColumn("purchase_datetime", col("purchase_datetime").cast("timestamp"))
df_date = df_date.withColumn("date_hour", col("date_hour").cast("timestamp"))
df_date.printSchema()
~~~

<br>

**Posteriormente precisamos configuração a conexão do Airflow da seguinte maneira:**
 
 ![airflow-config](/assets/airflow.png)

**Finalmente, criamos o script para gerar a conexão entres as ferramentas:**
~~~
from pyspark.sql.functions import month, year, col, round, current_timestamp, desc

df = spark.read.option("header", "true").csv("s3a://desafio-docker/purchases_2023.csv")
df = df.withColumn("price", round("price", 2))

mes = 4
df_mes = df.filter((month(col("purchase_datetime")) == mes))

df_multi = df_mes.withColumn("amount_price", col("price") * col("amount"))

df_date = df_multi.withColumn("date_hour", current_timestamp()).orderBy(desc("price"))

df_date = df_date.withColumn("amount", col("amount").cast("int"))
df_date = df_date.withColumn("discount_applied", col("discount_applied").cast("double"))
df_date = df_date.withColumn("purchase_datetime", col("purchase_datetime").cast("timestamp"))
df_date = df_date.withColumn("date_hour", col("date_hour").cast("timestamp"))

df_date.write.format("orc").option("orc.compression", "zlib").option("spark.sql.files.maxRecordsPerfile","-1").insertInto("default.purchase")
~~~
***