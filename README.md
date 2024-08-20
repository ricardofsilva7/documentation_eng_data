# 📜 Relatório de Estudos

**Nome do Estagiário: Ricardo Silva**  
**Data: 07/08/2024**

**Módulos/Etapas Feitas:**  
1. [**Modelagem de Dados**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana2?tab=readme-ov-file#-modelagem-de-dados)
2. [**BigQuery**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana2?tab=readme-ov-file#-bigquery)
3. [**Bases Analíticas**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana2?tab=readme-ov-file#-bases-anal%C3%ADticas)
4. [**Transacional (OLTP)**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana2?tab=readme-ov-file#-transacional-oltp)
5. [**Mensageria**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana2?tab=readme-ov-file#-mensageria)

***

# 📚 Resumo dos Módulos 
&nbsp;

## ✨ Modelagem de Dados

### 💫 Conceito
**A *Modelagem de Dados* é utilizada para criar um modelo para os dados que serão utilizados em um sistema de informação. Ele define as estruturas lógicas e as relações entre os diferentes tipos de dados, se tornando uma base para a construção de Bancos de Dados, e sistemas de gerenciamento de informações. A modelagem de dados busca garantir que os dados sejam organizados de maneira eficiente e que possam ser acessados e manipulados de maneira eficiente**

***
### 🔖 Por que a Modelagem de Dados é importante 
**As organizações coletam volumes de dados em grande escala e de várias fontes diferentes. Entretanto, dados brutos não são o suficiente, voce precisa analisar dados para absorver insights acionáveis e que possam orientar na tomada de decisão. Qualquer análise precisa de dados exige: *coleta, armazenamento e processamento de dados eficientes*. Existem muitas tecnologias de banco de dados e ferramentas de processamento de dados, e diferentes conjuntos de dados exigem ferramentas distintas para uma análise eficiente. A modelagem de dados nos da a chance de entender os dados e fazer as escolhas tecnológicas certas para armazenar e gerenciar esses dados. A *Modelagem de Dados* traz os seguintes benefícios:**

- *Reduz erros no desenvolvimento de softwares de Banco de Dados*
- *Facilita a velocidade e eficiência da concepção e criação de Banco de Dados*
- *Cria consistência  na documentação de dados e na concepção do sistemas em toda a organização*
- *Facilita a comunicação entre engenheiros de dados e equipes de BI (Business Intelligence)*

***

### 📝 Como modelos de dados são usados na prática?
**Existem três estilos básicos de modelos de dados que iremos explanar a seguir**

1. **Modelos de dados conceituais:** Geralmente utilizado para explorar conceitos do domínio com os envolvidos no projeto. Em equipes ágeis, modelos conceituais de alto nível são normalmente criados como parte do esforço inicial do entendimento dos requisitos do sistema, pois eles são usados para explorar as estruturas e conceitos de negócios estáticos de alto nível

2. **Modelos lógicos de dados (MLD's): MLD's** são usados para explorar os conceitos do domínio e seus realcionados. Pode ser feito para o escopo de um simples projeto ou para uma empresas inteira. **MLD's**  descrevem os tipos de entidades lógicas, tipicamente referenciadas simplesmente como tipo de entidade, os atributos de dados que descrevem essas entidades e os relacionamentos entre entidades, **MLD's** são raramente usados em projetos ágeis apesar de normalmente estarem presentes em projetos tradicionais (onde eles poucas vezes adicionam muito valor na prática)

3. **Modelos físicos de dados (MFD's): MFD's** são usados para projetar o esquema interno de um banco de dados, descrevendo as tabelas de dados, as colunas de dados das tabelas e o relacionamento entre as tabelas. **MFD's** normlmente são bastante úteis em projetos ágeis e tradicionais.

&nbsp;

**A** *Figura 1* **apresenta um simples MLD e a** *Figura 2* **um simples MFD, ambos modelando o conceito de clientes e endereços, assim como o relacionamento entre eles. Ambos diagramas sugerem a notação de Barker. Note como o MFD mostra mais detalhes, incluindo uma tabela associativa necessária para implementar a associação, assim como as chaves necessárias para manter os relacionamentos**

- _Figura 1_

![Figura 1](/assets/image001.jpg)

- _Figura 2_

![Figura 2](/assets/image002.jpg)

***
>### 🔧 Ferramentas de Modelagem de Dados
>- `ER/Studio`
>- `IBM InfoSphere Data Architect`
>- `Microsoft Visio`
>- `Oracle SQL Developer Data Modelar`
>- `PowerDesign`
>- `MySQL Workbench`
***
### 💡 Aplicação de modelagem de dados
1. **Sistemas de Gerenciamento de Relacionamento com o Cliente (CRM):** *Estruturação de dados de clientes, interações e histórico de compras, muito utilizado por instituições financeiras para acompanhamento de clientes.*
2. **Sistemas de Planejamento de Recursos Empresariais (ERP):** *Organização de dados sobre finanças, logisticas, recursos humanos, geração de notas fiscais e emails focados.*

3. **Data Warehouse:** *Integração e estruturação de dados de várias fontes para análise e relatórios.*
***
### 🔒️ Conclusão
 **A modelagem de dados é uma etapa fundamental na criação de sistemas de Banco de Dados. Com esses processos é possível criar a estrutura do banco de dados da empresa ou do projeto para alcançar os objetivos do negócio com o armazenamento de dados. Por isso, o modelo  de dados deve ser bem projetado para não gerar duplicidade de informações, armazenar dados em excesso e causar conflito de dados nas análises.**
***
**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github](https://github.com/Game-JAVA/data_engineer/blob/main/wiki/subpages/modelagem_de_dados.md)
- [Voitto](https://voitto.com.br/blog/artigo/modelagem-de-dados)
- [DevMedia](https://www.devmedia.com.br/modelagem-de-dados-tutorial/20398)
***
&nbsp;

## ✨ BigQuery
### 💫 Conceito

**O BigQuery é um serviço de armazenamento de dados de baixo custo e totalmente gerenciado do Google para análises com escala em *Petabytes*. É uma ferramenta *NoOps*, ou seja, ela não requer uma infraestrutura responsável pelo gerenciamento nem um administrador de banco de dados. Com o BigQuery, você se concentra na análise de dados para ter acesso a insights relevantes usando um SQL familiar e aprendizado de máquina integrado.**
***
### 🔖 Principais Características

**Alta Performance e Escalabilidade**
* **Consulta Rápida**: Capaz de executar consultas SQL em conjuntos de dados de forma extremamente rápido.

* **Escabilidade Automática:** Gerencia automaticamente a escala de armazenamento e recursos computacionais conforme necessário.

**Armazenamento de Dados**
* **Colunar**:  Utiliza um formato de armazenamento colunar que otimiza o desempenho de consultas.

* **Separação de Armazenaento e Computação**: Permite que o armazenamento de daos e a computação sejam escalados independentemente.

**Facilidade de Uso**
* **SQL compatível**: Utiliza SQL padrão, facilitando a implementação por usuários com conhecimento já adquirido de SQL.

**Integração e Compatibilidade**
* **ETL/ELT**: Suporta pipelines de ETL/ELT para ingestão de dados.
* **API e Conectores**: Integração com API's e conectores para diversas outras ferramentas de BI.

**Análise e Machine Learning**
* **Análise em Tempo Real**: Capaz de realizar análises em tempo real com suporte a dados em streaming.
* **Machine Learning Integrado**: Integração com o BigQuery ML, permitindo a criação e execução de modelos de Machine Learning diretamente na base de dados.

**Segurança e Governança**
* **Controle de acesso granulares**: Gerenciamento detalhado de permissões e acesso a dados.
* **Compliance**: Conformidade com diversos padrões de segurança e privacidade como *GDPR*.

**Custo e Gestão**
* **Modelo de Preço Pago por Consulta**: Pagar-se pelo volume de dados processados mais consultas, com opções de preços flexíveis.
* **Gerenciamento de Recursos**: Monitoramento e otimização de custos através de relatórios detalhados.

****
### 🏷️ Casos de Uso

1. **Análise de Big Data:** *Análise de dados em grandes volumes, tanto para extrair insights e gerar bases para tomada de decisão.*
2. **Business Intelligence:** *Geração de relatórios e dashboards para visualização e análise de dados empresariais e desempenho.*
3. **Processamento de Dados Streaming:** *Análise de dados em streaming para monitoramento e respostas rápidas a eventos específicos ou não.*
4. **Data warehousing:** *Armazenamento e gerenciamento de dados históricos para análise longitudinal e geração de relatórios.*

***
### 🔒️ Conclusão
 **BigQuery é uma ferramenta extraordinárias, principalmente para empresas e para o mercado de trabalho, o suporte a grandes volumes de dados, o elevado desempenho, a análise em tempo real, facilidade na integração de API's, e o modelo de pagamento flexivel**
***
**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github](https://github.com/Game-JAVA/data_engineer/blob/main/wiki/subpages/bigquery.md)
- [Artigo](https://metricasboss.com.br/artigos/o-que-e-o-google-big-query-e-como-utilizar)
- [Predicta](hhttps://predicta.net/bigquery-entenda-como-funciona-o-armazenamento-de-dados-na-nuvem-do-google/)
***
&nbsp;

## ✨ Bases Analíticas
### 💫 Conceito
**Bases análitcas são sistemas e tecnologias projetados para facilitar a análise de grandes volumes de dados. São otimizados para consultas complexas e operações analíticas, permitindo que as organizações extraiam insights valiosos e seus dados. As bases analíticas são frequentemente usadas em conjunto com *data warehouses* e *data lakes* para suportar diversas necessidades de análise de dados.**

***
### 🔖 Principais Características
**1. Desempenho de consultas:** *São otimizados para executar consultas complexas e pesadas de maneira rápida e eficiente.*

**2. Escalabilidade:** *Podem lidar com grandes volumes de dados e aumentar a capacidade conforme necessário.*
 
**3. Integração de Dados:** *Suportam a integração de dados de multipasa fontes, sejam eles estruturados, semiestruturados ou não estruturados.*

**4. Modelagem de Dados:** *Usam técnicas avançadas de modelagem de dados para organizar e relacionar informações de maneira lógica e acessível.*

**5. Ferramentas de Análise:** *Incluem ferramentas para mineração de dados, Machine Learning, visualização de dados e análise estatística.*

***
### 🏷️ Exemplos de Tecnologias de Bases Analíticas 
**`OLAP (Online Analytical Processing)`**
- **Descrição:** *OLAP* refere-se a tecnologias que permitem a realização de consultas multidimensionais sobre grandes volumes de dados, facilitando análises completas e a exploração interativo dos dados.

- **Características:** Suporte as operações: *drill-down, roll-up, slice, dice e pivot*, geralmente utilizando um modelo de dados multidimensional.

- **Exemplos de execução:** BI, relatórios financeiros, análise de desempenho comercial/empresarial.

**`Apache Spark`**
- **Descrição:** *Apach Spark* é uma plataforma de processamento de dados de código aberto que oferece suporte a processamento em tempo real ou em batch.

- **Características:** Alta velocidade de processamento suporte a *API's* em várias linguagens (Java, Scala, Python, R) integração com Hadoop e bibliotecas para *Machine Learning, SQL e Data Warehouse*.

- **Exemplos de execução:** Análise  de Big Data, Machine Learning, processamento de dados em tempo real, e integração com Data Lakes e Data Warehouse. 

**`Amazon Redshit`**
- **Descrição:** É um serviço de data warehouse gerenciado pela *Amazon Web Services (AWS)*.

- **Características:**  Escalabilidade, integração com ferramentas de visualização de dados, relatórios financeiros.

- **Exemplos de execução:** Business Intelligence, integração com ferramentas de visualização de dados, relatórios financeiros. 

**`Microsoft Azure Synope Analytics`**
- **Descrição:** *Azure* é um serviço de análise ilimitada que combina data warehousing empresarial e análise de Big Data. 

- **Características:**  Integração com serviços Azure, suporte a análise em tempo real, consulta distribuída e escalabilidade.

- **Exemplos de execução:** Análise de Big Data, BI, relatórios empresariais, integração de dados de diversas fontes. 

***

### ✅ Benefícios das Bases Analíticas
- **Insights:** *Permitem a extração de insights valiosas dos dados, ajudando na tomada de decisões.*
- **Desempenho:** *Otimizadas para consultas simples e complexas, melhorando a eficiência das operações analíticas.*
- **Flexibilidade e Escalabilidade:** Podem lidar com diferentes tipos e volumes de dados, ajustando as necessidades da organização.
- **Integração de Dados:** Facilitam a integração de dados de diversas fontes, possibilitando uma *visão holística* das informações
- **Ferramentas Avançadas:** Incluem ferramentas para análises avançadas, visualização de dados, e Machine Learning, ampliando as possibilidades analíticas das organizações.
***
&nbsp;

## ✨ Transacional (OLTP)
### 💫 Conceito
**O *OLTP* é um tipo de processamento de dados que consiste na execução de várias transações que ocorrem simultaneamente (transações bancárias, compras online, entrada de pedidos ou envio de mensagens de texto, por exemplo). Essas transações são tradicionalmente chamadas de transações econômicas ou financeiras, registradas e protegidas para que uma empresa possa acessar as informações a qualquer momento para fins contabeis ou de relatórios**
***

### 🔖 Principais Características
- **Transações em Tempo Real:** Processam operações rapidamente de maneira eficiente, permitindo que as transações sejam concluídas em tempo real

- **Alta confiabilidade e Integridade:** Garantem que as transações sejam completadas de maneira consistente e confiável, usando propriedades ACID *(Atomicidade, Consistência, Isolamente, Durabilidade)*
- **Suporte a Operação CRUD:** Suportam operações de criação, leitura, atualização e exclusão de dados.
- **Baixa Latência:** São otimizados para operações rápidas com pouca latência.
- **Alta Concorrência:** Suporta um alto número de usuários simultâneos, mantendo a integridade dos dados.
***

### ➕ Propriedades ACID
**`Atomicidade`**

- Os controles de atomicidade garantem que todas as etapas de uma transação sejam concluídas com sucesso como um grupo. Em resumo, se alguma etapa entre as transações falhar, todas as outras etapas também deverão falhar ou serem revertidas. A conclusção bem sucedida de uma transação é chamado de _confirmar_. A falha de uma transação é chamada de _abortar_.

**`Consistente`**
- A transação preserva consistência interna ao banco de dados. Se você executar a transação sozinha em um banco de dados incialmente consistente, quando a transação terminar de ser executada, o banco de dados estará novamente consistente.

**`Isolado`**
- A transação é executada como se estivesse sendo executada isoladamente, sem outras transações. Ou seja, o efeito de executar um conjunto de transações e o mesmo que executá-las individualmente. Esse comportamente é implementado bloqueando as linhas específicas na tabela.

**`Durável`**
- Os resultados da transação não serão perdidos em caso de falhas.
***

### 🧱 Bases Transacionais

**PostgreSQL**
 - **Descrição:** *Um sistema de gerenciamento de banco de dados relacional de código aberto, conhcido por sua robustez e conformidade*
- **Características:** *Suporte a transações **ACID**, extensibilidade, tipos de dados avançados, e suporte a **JSON**.*
- **Uso:** *Aplicações empresariais, sistemas BI, aplicações de geolocalização.*

**Oracle Database**
- **Descrição:** *Um sistema de gerenciamento de banco de dados relacional proprietário amplamente utilizado em ambientes empresariais.*
- **Características:** *Suporte a transações **ACID**, alta disponibilidade, recuperação de desastres e recursos avançados de segurança.*
- **Uso:** *Sistemas financeiros, ERP's, grandes aplicações empresariais.*

**Microsoft SQL Server**
- **Descrição:** *Sistema de gerenciamento de banco de dados relacional, desenvolvido pela Microsoft.*
- **Características:** *Suporte a transações **ACID**, integração com o ecossistema Microsoft, ferramentas avançadas de BI e análises.*
- **Uso:** *Aplicações empresariais, sistema de gerenciamento de recursos, plataformas de dados corporativos.*
***
### 🔒️ Conclusão
**As Bases Transacionais são tecnologias essenciais para empresas que dependem de transações online. Ele permite o processamento de um grande volume de transações em tempo real, garantindo uma experiência de compra rápida e segura para os clientes. Embora apresenta desafios, como a escabilidade e disponibilidade, o *OLTP* é amplamente utilizado em setores como o *bancário* e *varejista*. É uma ferramenta poderosa para impulsionar os negócios e melhorar a experiência do cliente.**
***

**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github](https://github.com/Game-JAVA/data_engineer/blob/main/wiki/subpages/analitico.md)
- [Oracle](https://www.oracle.com/br/database/what-is-oltp/)
- [Artigo](https://nobug.com.br/glossario/o-que-e-oltp-online-transaction-processing/)

***
&nbsp;

## ✨ Mensageria
 ### 💫 Conceito
 **Mensageria é um conceito fundamental em sistemas distribuídos em redes de computadores, que envolve a troca de mensagem entre diferentes componentes ou sistemas. O objetivo principal da mensageria é facilitar a comunicação e a coordenação entre as partes de um sistema ou entre sistemas distintos de maneira assíncrona e desacopla**

***
 ### 🔖 Principais Características

 **Mensagem**
 
 Unidades de dados que são transmitidas entre sistemas ou componentes. Cada mensagem pode conter um _payload_ (dados reais) e _metadados_ (informações adicionais como cabeçalho e atributos).
 
 **Pub/Sub**
 
 Em um sistema de mensageria baseado em _PUB/SUB_ (publicação/inscrição), um publicador envia mensagens para um tópico, enquanto um assinante se inscreve em tópicos para receber mensagens.

**Tópicos e Filas**

- **Tópicos:** Entidades para onde as mensagens são publicadas, assinantes se inscrevem em tópicos para receber mensagens. Esse modelo é comum em sistemas _pub/sub_.
- **Filas:** Estruturas que armazenam mensagens para que possam ser processadas pelos consumidores. As mensagens são retiradas da fila por consumidores, um de cada vez, típico em sistemas de filas de mensagem.

**Broker de Mensagens**

Componente que gerencia o envio e o recebimento de mensagens. Ele garante que as mensagens sejam entregues aos destinatários corretos e pode fornecer funcionalidades como persistência, roteamento e gerenciamento de transações 

**Desacoplamento:** 

Mensageria permite que os sistemas se comuniquem sem a necessidade de um conhcimento direto sobre o estado ou a disponiblidade dos outros sistemas, promovendo um acomplamento fraco.

**Assíncro:**

 Em sistemas de mensageria, a comunicação é frequentemente assíncrona, o que signifca que o remetente não precisa esperar que o destinatário recebe ou processe a mensagem antes de continuar com sua própria execução. 

***
### 🏷️ Tipos de Mensageria

1. **Pub/Sub:** O modelo _pub/sub_ permite que um componente (publicadas) envia mensagens para um tópico, e os componentes interessados (assinantes) recebem as mensagens. É importante para disseminar as informações para múltiplos consumidores simultaneamente.

2. **Fila de Mensagens:** As mensagens armazenadas em uma fila e processadas por consumidores. Este modelo é usado para garantir que as mensagens sejam processadas em ordem e para balancear a carga entre múltiplos consumidores.

3. **Mensagem Ponto a Ponto:** Envolve a troca de mensagens entre dois componentes diretamente, sem intermediários. É útil para comunicações diretas e específicas entre sistemas.

***
### ➕ Sistemas de Mensageria
- **RabbitMQ:** *Uma plataforma de mensagens que supostas filas e troca de mensagens baseada em tópicos.*
- **Apache Kafka:** *Uma plataforma distribuída para o processamento de sistemas de dados em tempo real.*
- **Google Cloud Pub/Sub:** *Serviço gerenciado para publicação e inscrição de mensagens*
- **Apache ActiveMQ:** *Sistema de mensagens de código aberto que suporta vários padróes de mensageria*

***
### 🔒️ Conclusão

A mensageria é uma tecnologia essencial para a construção de sistemas distribuídos modernos, permitindo comunicação eficiente, escalável e resiliente a diferentes componentes e serviços.


***
**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github](https://github.com/Game-JAVA/data_engineer/blob/main/wiki/subpages/mensageria.md)
- [Pesquisas no Google]
- [Artigo](https://crmpiperun.com/blog/mensageria/#:~:text=A%20mensageria%2C%20ou%20%E2%80%9Cmessaging%E2%80%9D,conversa%20direta%20com%20um%20vendedor.)
***
&nbsp;
**Desafios Encontrados:**  
*Acredito que no meu caso, o desafio é absorver todo conteúdo, considerando que venho de outra área de atuação e apesar de já ter evoluído bastante, ainda sinto dificuldade com as nomenclaturas e termos técnicos. Minha ideia é ir aprofundando os conteúdos conforme eu for absorvendo de fato o conteúdo.*

**Feedback e Ajustes:**  
*Descreva qualquer feedback que você recebeu e como você ajustou sua abordagem de estudo com base nesse feedback.*

**Próximos Passos:**  
*Os próximos passos são continuar a trilha de conhecimento, buscar alimentar mais as informações de cada trilha e continuar mantendo o padrão de estilização.*


**Relatórios:**

[**1ª Semana**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana1)

[**3ª Semana**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana3)

[**4ª Semana**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana4)
***
