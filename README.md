# 📜 Relatório de Estudos

**Nome do Estagiário: Ricardo Silva**  
**Data: 02/08/2024**

**Módulos/Etapas Feitas:**  
1. **Engenharia de Dados**
2. **Git**
3. **Big Data** 

***
# 📚 Resumo dos Módulos 
&nbsp;

## ✨ Engenharia de Dados

### 💫 Introdução
 #### A Engenharia de Dados faz parte da área de *Processamento e Análise de Dados* que se concentra na criação e manutenção de *Sistemas e Infraestruturas*, sendo necessário coletar, armazenar, processar e analisar os dados, geralmente em grandes volumes. Primeiramente qualquer dado recebido é tratado e posteriormente utilizado para tomadas de decisão, análise de negócios e até mesmo para desenvolvimento de modelos de aprendizado de máquinas (ML).

***
### 🔖 Principais Atividades
 #### `Aquisição de Dados`
  * #### **O principal objetivo de um sistema de aquisiçãode dados é aquisitar e armazenar os dadods. Entretanto ele também visa fornecer visualização e análise em tempo real e pós-gravação dos dados. A maioria dos sistemas de aquisição de dados possui alguma capacidade analítica e de geração de relatórios incorporada.**
  * #### **A aquisição de dados pode ser realizada de diversas fontes, como Bancos de Dados já existentes, API's, arquivos, sensores, entre outros.**

  #### `Armazenamento de Dados`
  * #### **Na Engenharia de Dados, o armazenamento de dados é uma das principais tarefas a serem realizadas. Visando garantir a segurança, disponibilidade e a eficiência dos dados, é importante entender as técnicas que podem ser aplicadas, como uso de *data lake* ou *data warehouse***
  * #### **Data Lake: O data lake é um repositório de diversos tipos de dados que permite o armazenamento dos dados em seu formato original, não relacional e diversas tipos de dados: *estruturados, semi estruturados, ou não estruturados*, ele é projeto para suportar a análise de big data, armazenando com bom custo-benefício, principalmente para grandes volumes de dados**
  * #### **Data Warehouse: É um banco de dados relacional, capaz de armazenar *dados estruturados* de diferentes fontes de dados. Projetado para ofecer aos usuários, principalmente anaçistas de big data e BI (business intelligence), gestores e outros interessados acesso aos data marts(mercados de dados)**

  #### `Processamento de Dados`
  * #### **Responsável pela transformação e limpeza de dados para melhorar a qualidade e adequação para análise. Isso pode incluir: remoção de duplicatas, tratamento de valores ausentes e normalização de dados**
  * #### ETL (Extract, Transform, Load) : Processo de extração de dados, de diversas fontes, posteriormente é realizado a transformação para o formato desejado e o próximo passo é realizar o carregamento para o sistema de armazenamento.
  * #### Processamento em Lote: Processamento de grandes volumes dados em intervalores regulares, utilizando as ferramentas Apachi Hadoop e Apache Spark.

  * #### Processamento em Tempo Real: Processamento de dados em tempo real ou quase real usando ferramentas como Apache Storm, Apache Flink, e Spark Streaming.

  #### `Integração de Dados`
  * #### Realiza a unificação de dados de diversas fontes, garantindo que estejam integros e integrados de maneira consistente. Para ser realizado de forma correta é necessários alguns passos importantes: 
  > 1. Extração dos Dados;
  > 2. Transformação dos Dados;
  > 3. Carregamento dos Dados;
  > 4. Harmonização e Deduplicação.

&nbsp;

#### `Segurança e Governança de Dados`
* #### Garantir que os dados armazenados e que serão armazenados serão manipulados em conformidade com regulamentações e políticas de privacidade.

***

**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github]
- [Pesquisas no Google]
- [Artigos]
***
&nbsp;

## ✨ Git
### 💫 Definição

* #### Sistema para controle de versão distribuído e massivamente utilizado para rastrear alterações  em arquivos, controle de versão da aplicação e acompanhar alterações no código-fonte de projetos tecnológicos, permitindo que múltiplos desenvolvedores trabalhem em paralelo, ajudando ainda a manter os históricos de todas mudanças no projeto.
***
### 🔖 Conceitos

* #### *`Repositório`*: O diretório onde armazena-se o histórico completo de mudanças no projeto, incluindo arquivos, pastas e alterações no código-fonte.

* #### *`Commit`*: Seria um *Snapshot*  do projeto em um ponto especifíco no tempo. Cada `commit` tem seu identificador único, comparação de alteração referente ao `commit` anterior e mensagem descritiva da alteração.

* #### *`Branchs`*: São ramificações do projeto que permite trabalhar em diferentes linhas, do projeto em desenvolvimento, ao mesmo tempo.

* #### *`Merge`*: É a combinação de diferentes branchs em uma unica branch (principal).

* #### *`Pull`*: Atualiza a cópia do repositório com as alterações mais recentes do repositório remoto.

* #### *`Push`*: Envia as mudanças locais para o repositório remoto após o '`commit`'.

* #### *`Clone`*: Criação de uma cópia local de um repositório remoto, preservando todos os arquivos e códigos-fonte.

* #### *`Fork`*: É a criação de uma cópia independente de um repositório, normalmente para contribuir com um projeto sem afetar ou acessar o repositório principal.

***
## 📦 Principais Componentes do GitFlow
###  Branches Principais

* #### *`Main`*: Contém  o código de produção estável, cada `commit` nesta branch representa uma nova versão de lançamento, mas antes de chegar na `main`, o mesmo código precisou passar por processsos de validação e branches 'temporárias'.

* #### *``Develop``*: Contém o código em desenvolvimento contendo as últimas alterações aprovadas, serve como base para novas funcionalidades e integrações.

### Branches de Suporte
* #### *`Feature`*: Utilizada para desenvolver novas funcionalidades. Deriva de *`develop`* e é mesclada de volta  `develop` após a funcionalidade for concluída.
* #### *`Release`*: Utilizadao para quando é lançado uma nova versão. Deriva de `develop`, após ajustes finais, é mescaldo em *`main`* e *`develop`*  após correção/revisão.

***
## ✔️ Fluxo de Trabalho
### 1. Desenvovimento de funcionalidades
 * #### Crie uma btanch de *`feature`* a partir de *`develop`*.
 * #### Desenvolva a nova funcionalidade
 * #### Mescal a branch de *`feature`* de volta em *`develop`*.
 ### 2. Preparação para lançamento
 * #### Crie uma brnach de *`release`* a partir de *`develop`*.
 * #### Faça os ajustes finais e correção. 
 * #### Mescala a branch de *`release`* em *`main`* e *`develop`*, e marca o `commit` com uma tag.
 ### 3. Correções urgentes
* #### Crie uma branch de *hotfix* a partir de *`main`*.
* #### Faça as correções necessárias.
* #### Mescle a brnach *hotfix* em *`main`* e *`develop`*, e marque o `commit` com uma tag
***
>## ✅ Vantagens do Git
>
>* #### Distribuído: Cada desenvolvedor tem uma cópia completa do repositório, incluindo todo o histórico do projeto; 
>
>* #### Colaboração: Torna mais simples o trabalho de equipes e a mesma coisa para vários desenvolvedores, alterando diferentes partes do projeto ao mesmo tempo;
>
>* #### História da Revisão: Mantém um registro completo de todas as alterações feitas ao projeto e simplifica o trabalho com elas. Isso pode ser usado para reverter alterações, se necessário;
>
>* #### Branches e Merges: Simplifica a criação e manutenção de branches onde o desenvolvimento é feito simultaneamente; existem ferramentas implementadas para integrar as mudanças em uma mesclagem; 
>
>* #### Desempenho: Embora o Git tenha algumas pegadas, isso não é o problema mesmo com projetos grandes.
***
&nbsp;

**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github]
- [Pesquisas no Google]
- [Artigos]

**Principais comandos:**
- [*"git init"*]
- [*"git `commit`"*]
- [*"git push"*]
***
&nbsp;

## ✨ Big Data
### 💡 Introdução ao Big Data
#### Big Data refere-se ao conjunto de tecnologias e práticas usadas para coletar, armazenar, processar e analisar grande volumes de dados que não podem ser gerenciados de maneira eficiente com as ferramentas habituais de *Banco de Dados*. Os dados do Big Data s~~ao caracterizados pelo que é conhecimo como os `4V's`.

* #### `Volume`: A quantidade de dados que são gerados e coletados é gigante e, muitas vezes medida em *petabytes* e *exabytes*
* #### `Variedade`: Os dados vem de diversas fontes e podem ser, tanto dados *estruturados*, *semiestruturados* ou *não estruturados*
* #### `Velocidade`: Atualmente, as informações circulam em alta velocidade e em tempo real. Por exemplo, em redes sociais, milhões de posts são publicados a cada segundo. Para aproveitar ao máximo os dados, é necessário que a velocidade de resposta seja rápida e eficiente.
* #### `Veracidade`: O último “V” destaca a importância da confiabilidade e qualidade dos dados. Como lidamos com uma quantidade tão grande de informações, é fundamental garantir a veracidade dos dados para evitar decisões equivocadas. A veracidade está relacionada à autenticidade, integridade e precisão dos dados, garantindo que eles sejam confiáveis e relevantes para as análises.
&nbsp;

### 📦 Aplicações ao Big Data

* #### `Negócios`: Análise de comportamente como consumidor, personalização de marketing, otimização de processos empresariais
* #### `Saúde`: Análise de dados genômicos, monitoramento de epidemias e até mesmo medecina personalizada.
* #### `Governo`: Análise de políticas públicas, prevenção de crimes, gerenciamento de cidades inteligentes, controle de gastos e prevenções
* #### `Ciência`: Pesquisas científicas, análise de dados astronômicos, estudos climáticos e ambientais.
&nbsp;

### 🚧 Desafios do Big Data
* #### `Armazenamento`: Gerenciar  e armazenar grandes volumes de dados de maneira eficiente e sólida.
* #### `Processamento`: Processar rapidamente grandes quantidades de dados para extrair insight em tempo real.
* #### `Privacidade e Segurança`: Proteger dados sensíveis e garantir a conformidade com regulamentações e principalmente privacidade.
* #### `Qualidade dos dados`: Garantir a precisão dos dados, manter os dados completos e livres de erros.
***
&nbsp;

**Recursos Utilizados:**  
- *[Trilha de Conhecimento - Github]*
- *[Pesquisas no Google]*
- *[Artigos]*


**Desafios Encontrados:**  
*Acredito que no meu caso, o desafio é absorver todo conteúdo, considerando que venho de outra área de atuação e apesar de já ter evoluído bastante, ainda sinto dificuldade com as nomenclaturas, termos técnicos. Meu plano é ir aprofundando os conteúdos conforme eu for sentindo que realmente aprendi.*

**Feedback e Ajustes:**  
*Descreva qualquer feedback que você recebeu e como você ajustou sua abordagem de estudo com base nesse feedback.*

**Próximos Passos:**  
*Próximos passos são continuar a trilha de conhecimento, buscar alimentar mais as informações de cada trilha e continuar mantendo o padrão de estilização.*

&nbsp;

***