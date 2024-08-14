# 📜 Relatório de Estudos

**Nome do Estagiário: Ricardo Silva**  
**Data: 14/08/2024**

**Módulos/Etapas Feitas:**  
1. [**Virtualização**](https://github.com/2RP-Squad404/Ricardo_Silva#-virtualiza%C3%A7%C3%A3o)
2. [**Docker**](https://github.com/2RP-Squad404/Ricardo_Silva#-docker)
3. [**Kubernetes**](https://github.com/2RP-Squad404/Ricardo_Silva#-kubernetes)
4. [**Computação em Nuvem**](https://github.com/2RP-Squad404/Ricardo_Silva#-computa%C3%A7%C3%A3o-em-nuvem)
5. [**CI/CD**](https://github.com/2RP-Squad404/Ricardo_Silva#-cicd)

***

# 📚 Resumo dos Módulos 
&nbsp;

## ✨ Virtualização

### 💫 Conceito
**Uma Máquina Virtual (VM) é um ambiente de computação que funciona como um sistema isolado com *CPU*, *Memória*, *Interface de rede* e *armazenamento* próprios, criado a partir de um pool de recursos de hardware. O software chamado *hipervisor* isola os recursos computacionais necessários e permite a criação e o gerenciamento de Máquinas Virtuais. A máquina física que executa os VM's é chamado de *máquina host* ou simplesmente *host*. As várias VM's que usam os recursos do host são *máquinas guest* ou simplesmente *guest*. O hipervisor trata os recursos de computação (CPU, memória e armazenamento) como um pool que pode ser realocado com facilidade entre os guests existentes ou para novas máquinas virtuais**

***
### 🔖 Tipos de Virtualização 
**A virtualização é uma tecnologia que usa recursos tradicionalmente vinculados ao hardware. Com ela, é possível usar a capacidade total de uma máquina física, distribuindo seus recursos entre muitos usuários ou ambientes; Os tipos incluem:**

- **Virtualização de Dados:** *Permite as organizações consolidar fontes de dados em um único recurso dinâmico.*
- **Virtualização de Desktop:** *Possibilita implantar e controlar vários ambientes de desktop simulados por meio de um Administrador Central.*
- **Virtualização de Servidores:** *Permite aos administradores particionar servidores em configurações distintas a desempenhar funções específicas.*
- **Virtualização de Sistema Operacional:** *Torna possível a execução de vários sistemas operacionais em um único computador.*
- **Virtualização de Função de Rede:** *Supera as funções de uma rede (como serviços de diretório, compartilhamento de arquivos e configuração de IP) para distribuí-las entre os ambientes.*
***

### 📝 Principais Características

1. **Isolamento:** Cada máquina virtual é isolada das demais e do sistema host, oque permite que distintas máquinas virtuais executem diferentes sistemas operacionais e aplicativos de maneira independente.

2. **Recursos Compartilhados:** Máquinas virtuais compartilham os recursos físicos do hardware subjacente, como CPU, Memória e Armazenamento, más operam de maneira independente.

3. **Portabilidade:** VM's podem ser movidas entre diferentes servidores físicos, permitindo a flexibilidade e recuperação de desastres. Imagens de máquinas virtuais podem ser replicadas e transportadas facilmente.

4. **Escalabilidade:** Facilita a criação e o gerenciamento de múltiplas instâncias de servidores para escalar aplicações conforme a demanda.

5. **Gerenciamento Simplificado:** Permite o gerenciamento centralizado e automatizado das máquinas virtuais, facilitando a administração e a manutenção.
***

### 🔧 Principais Componentes

**Hipervisor:** *O software que gerencia e cria máquinas virtuais. Existem dois tipos principais e hipervisor*

- **Tipo 1 (Bare-metal):** Executa diretamente no hardware do servidor, como *VMware ESXI* e *Microsoft Hyper-V*
- **Tipo 2 (Hosted):** Executa sobre um sistema host, como *VMware* e *Oracle VirtualBox*

**Imagens de VM's:** *Arquivos que contém o sistema operacional, dados necessários e aplicativos para iniciar e operar uma máquina virtual.*

**Virtualização de Hardware:** *A camada de virtualização emula recursos de hardware(CPU's, Memória e Discos) para as maquinas virtuais, permitindo que elas funcionem da mesma maneira, como se estivessem em um hardware físico dedicado*

**Recursos Virtuais:** *Recursos como CPU's virtuais, memória virtual e armazenamento virtual são alocados para as máquinas virtuais conforme necessidade.*

***
### 💡 Vantagens das Máquinas Virtuais
- **Utilização de recursos e ROI melhorado:** Como vários VM's são executadis em um único computador físico, os clientes não precisam comprar um novo servidor toda vez que quiserem executar outro S.O. e podem obter mais retorno de cada peça de hardware que já possuem.

- **Escala:** Com a computação em nuvem, é facil implementar várias cópias da mesma máquina virtual para melhor acomodar aumentos em carga.

- **Portabilidade:** VM's podem ser realocadas conforme necessário entre os computadores físicos em uma rede. Isso possibilita a alocação de computação sobressalente. As VM's podem até se mover entre ambientes locais em nuvem.

- **Flexibilidade:** Criar uma Máquina Virtual é mais rápido e mais fácil do que instalar uma S.O. em um servidor físico, já que é possível clonar uma VM com o S.O. ja instalado. Desenvolvedores e testadores de software podem criar novos ambientes sob demanda para lidar com novas tarefas à medida que demandam.

- **Segurança:** VM's melhoram a segurança de várias maneiras se comparados a sistemas operacionais sendo executados diretamente em hardware. Uma máquina virtual é um arquivo que pode ser varrido por um programa externo em busca de software maliciosos. É possível criar uma captura instantânea inteira da VM a qualquer momento e em seguida, restaurá-la para esse estudo caso ela ja infectada por um malware, recuperando-a de forma rápida e eficaz. A criação rápida e fácil de VM's também possibilita excluir completamente uma VM comprometida e, em seguida, recriá-la rapidamente, acelarando a recuperação de infecções por vírus.
***

**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github](https://github.com/Game-JAVA/data_engineer/blob/main/wiki/subpages/virtualizacao.md)
- [Artigo - Red Hat](https://www.redhat.com/pt-br/topics/virtualization/what-is-a-virtual-machine)
***
&nbsp;

## ✨ Docker

### 💫 Conceito
**A palavra *Docker* tem várias definições; Um projeto da comunidade open source, ferramentas resultantes desse projeto, a empresa *Docker Inc*, principal apoiadora do projeto, e as ferramentas compatíveis formalmente com a empresa. O fato da empresa e das tecnologias terem o mesmo nome pode causar alguma confusão**

- *O software de TI **Docker** é uma tecnologia de containerização para criação e uso de conteineres Linux.*
- *A comunidade open source do Docker trabalha gratuitamente para melhorar essas tecnologias para todos usuários.*
- *A empresa **Docker Inc.** se baseia no trabalho feito pela comunidade do Docker, tornando-o mais seguro em geral. Depoi, ela oferece aos clientes empresariais o suporte necessário para as tecnologias, que foram aprimoradas e fortalecidas.*

**Com o Docker, é possível lidar com os conteiners como se fossem máquinas virtuais modulares e extremamente lightweight. Além disso, os conteineres oferecem maior flexibilidade para você criar, implantar, copiar e migrar um contêiner de um ambiente para outro.**
***


### 🔖 Como o Docker funciona

A tecnologia **Docker** usa o *Kernel* do *Linux* e funcionalidades do Kernel, como *Groups* e *homespaces*, para segregar processos. Assim, eles podem ser executados de maneira independente. O objetivo dos contêineres é criar independência: a habilidade de executar diversos processos e app's separadamente para utilizar melhor a infraestrutura e, ao mesmo tempo, manter a segurança que você teria em sistemas separados.

 As ferramentas de contêiner, incluindo o Docker, incluem um modelo de implantação com base em imagens. Isso facilita o compartilhamento de uma aplicação ou conjunto de serviços, incluindo todas as dependências deles em vários ambientes. O Docker também automatiza a implantação da aplicação *(ou de conjunto de processos que constituem um app)* dentro desse ambiente de contêiner. Essas ferramentas baseadas no contêiner Linux fazem com que o Docker seja exclusivo e fácil de usar. Elas também oferecem aos usuários acesso sem precedentes a apps e total controle sobre as versões  distribuição, além da habilidade de impantar com rapidez.
***

 ### ✔️ Docker e Contêineres Linux: qual a diferença?

 Embora isso posta causar confusão, o Docker não é o mesmo que um contêiner Linux tradicional. A tecnologia Docker foi desenvolvida inicialmente com base na tecnologia LXC, que a maioria das pessoas associa aos contêineres Linux "tradicionais". No entanto, mas não oferecia uma boa experiência para usuários e desenvolvedores. A tecnologia Docker oferece mais do que a habilidade de executar contêineres, o envio e o controle de versão de imagens, entre outros.

 ![Docker](/assets/docker.png)

 Os Contêineres Linux tradicionais usam um sistema *init* capaz de gerenciar vários processos. Isso significa que aplicações inteiras são executadas como uma. A tecnologia Docker incentiva a segregação de aplicações em processos separados e oferece as ferramentas para fazer isso. Essa abordagem granular tem algumas vantagens.
 ***

 ### 🔧 Principais Componentes

 `Containers:` Unidades leves e potáteis que encapsulam o aplicativo e suas dependências em um ambiente isolado.

 `Imagens Docker:` São modelos para ciração de contêineres, contêm o código-fonte, bibliotecas eoutras dependências necessárias para o aplicativo.

 `Dockerfile:` É um script que contém uma série de instruções para construir uma imagem Docker, define o ambiente necessário para o aplicativo e como deve ser configurado.

 `Docker Hub:` Registro público de imagens Docker, onde você pode encontrar e compartilhar imagens de contêiner.
 
 `Docker Compose:` Uma ferramenta para definir e gerenciar aplicações multi-contêineres. Usando um arquivo **YAML**, você pode configurar serviços, redes e volumes necessários para execuar uma aplicação composta por vários contêineres.
***

### 🏷️ Casos de Uso
**Aplicações e microsserviços distribuídos**

Podemos utilizar contêiners para criar aplicações distribuídas, dividindo-as em tarefas ou processos independentes (microsserviços). Por exemplo, você pode ter contêineres separados para o servidor web, servidor de aplicações, a fila de mensagens e operadores de back-end, os contêineres são ideais para executar tarefas ou processos simples e podem ser usados como a unidade básica de uma tarefa ao aumentar ou diminuir escala.

**Integração e implantação contínuas**

O Docker oferece um sistema de versionamento de imagens, permitindo o uso de contêineres para integração e implantação contínuas. Você pode configurar o processo de criação para obter código de um repositório, compilá-lo, empacotá-lo em uma imagem do  Docker e enviá-la a um repositório de imagnes. Em seguida, o processo de implantação pode obter a imagem do repositório , testar a aplicação. É possível evitar que uma aplicação funcione no ambiente de desenvolvimento e falhe no ambiente de produção, pois o *daemon* do Docker é o mesmo nas máquinas de desenvolvimento preparação e produção.
***

### ✅ Benefícios do Docker

- *O Docker permite um uso mais eficiente dos recursos do sistema.*
- *As instâncias de aplicativos em contêiner usam muito menos memória do que máquinas virtuais, elas são inicializadas e interrompidas mais rapidamente podem ser armazenadas muito mais densamente em um **hardware host**.*
- *O Docker permite ciclos de entrega de software mais rápido.*
- *O software corporativo deve responder rapidamente a mudanças de condições. Isso significa que o escalonamento fácil atenda à demanda e facilita a atualização para adicionar novos recursos conforme a necessidade do negócio.*
- *O Docker permite a portabilidade de aplicativos.*
- *Os contêineres são leves, portáteis e facilitam a construção de software em linhas de pensamento avançadas, de modo que o desenvolvedor não está tentando resolver os problemas de amanhã com os métodos de desenvolvimento de ontem.*

***
### 🔒️ Conclusão
 **Mesmo com desafios a serem enfrentados, não é por acaso que os contêineres estão se tornando cada vez mais populares. Eles reduzem a necessidade de contar com uma grande estrutura e permitem utilizar apenas um sistema operacional normal. Como os contêineres ficam dispostos neste único ambiente, é muito mais fácil realizar a manutenção além de ser mais leve e permite a portabilidade.**
***
**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github](https://github.com/Game-JAVA/data_engineer/blob/main/wiki/subpages/virtualizacao.md)
- [Aws](https://aws.amazon.com/pt/docker/)
- [Atlassian](https://www.atlassian.com/microservices/microservices-architecture/kubernetes-vs-docker)
- [Dynatrace](https://www.dynatrace.com/news/blog/kubernetes-vs-docker/)
***
&nbsp;

## ✨ Kubernetes
### 💫 Conceito
**Kubernetes (também conhecido como *K8S* ou *KUBE*) é uma plataforma de orquestração de contêiner para agendar e automatizar a implantação, o gerenciamento e o dimensionamento de app's em contêineres. Kubernetes foi inicialmente desenvolvido por engenheiros da Google antes de ser disponibilizado como código aberto em 2014. É descendente da *Borg*, uma plataforma de orquestração de contêineres usada internamente no Google. *Kuvernetes* siginfica "timoneiro" ou "piloto" em grego, dai o leme no logotipo do Kubernetes. Atualmente o Kubernetes e o amplo ecossistema de contêineres estão se desenvolvendo como uma plataforma de computação de uso geral que concorre, e em alguns casos supera, as máquinas virtuais como os elementos fundamentais da infraestrutura de nuvem moderna e das aplicações. Esse ecossitema permite que organizações forneçam uma plataforma como serviços *PaaS* de alta produtividade que aborda diversas tarefas e problemas relacionados à infraestrutura e as operações que envolvem o desenvolvimento *nativo da nuvem*, para que as equipes de desenvolvimento possam concetrar exclusivamente na codificação e na inovação.**
***

### 🔍️ Oque são Contêineres

Os contêineres são componentes de aplicativos leves e executáveis que combinam o código-fonte do aplicativo com todas as bibliotecas do sistema operacional (S.O.) e as depedências necessárias para executar o código em qualquer ambiente. Os contêineres aproveitam uma forma de virtualização do sistema operacional que permite à várias aplicações compartilharem um única instância de um S.O, isolando processos e controlando a quantidade de *CPU*, *Memória* e *Disco* que esses processos podem acessar. Como são menores e mais eficientes em termos de recursos e com maior portabilidade do que as VM's, os contêineres se tornaram as unidades de computação de fato dosmodernos aplicativos nativos em nuvem.
***

### 🔧 Principais Componentes
`Pod:` Menor unidade de implantação no Kubernetes, pode conter um ou mais contêineres que compartilham armazenamento e rede.

`Node:` Máquina física ou virtual que executa os *Pods* e fornece recursos necessários para execução de contêineres. Cada node é gerenciado pelo Master e executa Kubelet e contêineres

`Master Node:` o Nó Central que cordena o cluster, gerenciando a comunicação entre os Nodes e controlando a execução do pods: Ele contém componentes como o *API Server*, *Controller Manager* e *Scheduler*.

`Deployment:` Objetivo que direciona um conjunto de Pods, deve ser executado e gerenciado incluindo as estratégias de atualização e escala.

`Service:` Abstração que define um conjunto de Pods e fornece uma forma de expor eses Pods como um serviço de rede, permitindo a comunicação entre eles e com o mundo externo.

`ConfigMap e Secret:` Objetos que permitem a separação de configurações e informações sensíveis do código dos contêineres, facilitando o gerenciamento e a segurança das configurações.

`Ingress:` Gerencia os acessos externos aos serviços dentro do Cluster, fornecendo balanceamento de carga e roteamento de tráfego baseado em regras de *URL* e *Host*
***

### 🏷️ Casos de Uso
*A Kubernetes programa e automatiza tarefas relacionadas ao contetor durante todo o ciclo de vida do aplicativo, incluindo:*

**Implantação:** *Implemente um número específico de contêineres em um host específicado e mantenha-os funcionando no estado desejado.*

**Implementações:** *Uma implementação é uma alteração em uma implantação. O Kubernetes permite iniciar, pausar, retomar ou reverter lançamentos.*

**Descoberta de Serviços:** *Possibilita expor automaticamente um contêiner à internet ou a outros contêineires usando um nome **DNS** ou  **endereço IP**.*

**provisionamento de armazenamento:** Define o Kubernetes para montar armazenamento local persistente ou na nuvem para seus contêineres, conforme necessário.

**Balanceamento de cargo:** *Com base na uilização da CPU ou métricas personalizadas, o balanceamento de carga do Kubernetes pode distribuir a carga de trabalho em toda a arede para manter o desempenho e estabilidade.*

**Expansão automática:** *Quando o tráfego aumenta, o dimensionamento automático do Kubernetes pode criar novos Clusters conforme necessário para lidar com a carga de trabalho adicional.*

**Autocorreção para alta qualidade:** *Quando um contêiner falha, o Kubernetes pode renunciá-lo ou substituí-lo automaticamente para evitar "downtime". Possibilita derrubar contêineres que não atendem aos requisitos de verificação de integridade.*
***

### ⚡Kubernetes vs. Docker

O Docker é um conjunto de ferramentas de desenvolvimento de software para criar, compartilhar e executar contêineres individuais; O Kubernetes é um sistema para operar aplicativos em contêineres padronizadas para microsserviços como todo o código de aplicativo e dependências necessárias dentro. Criar esses contêineres é o domínio do Docker.

Um aplicativo moderno consiste em muitos contêineres, operá-los em produção é o trabalho do Kubernetes. Como os contêineres são fáceis de replicar, os aplicativos pode serem dimensionados automaticamente.

**Docker** e **Kubernetes** são, em sua maioria, tecnologias complementares. No entanto, o Docker também fornece um sistema para operar aplicativos em contêineres em escala, chamado **Docker Swarm**.
***

### 🔒️ Conclusão
 **O Kubernetes representa uma revolução na forma como os aplicativos são gerenciados, fornecendo uma plataforma poderosa e flexível para a implantação e orquestração eficientes de contêineres em escala. Com a adoçao generalizada e evolução contínua, o Kubernetes se tornou um pilar fundamental da infraestrutura moderna de TI, capacitando as empresas a impulsionar a invocação e fornecer serviços confiáveis em um mundo cada vez mais digital.**
***

**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github](https://github.com/Game-JAVA/data_engineer/blob/main/wiki/subpages/virtualizacao.md)
- [IBM](https://www.ibm.com/br-pt/topics/kubernetes)
- [UEPG](https://deinfo.uepg.br/~alunoso/2023/SO/kubernets/Introdu%C3%A7%C3%A3o,%20Conceitos%20Basicos%20e%20Hist%C3%B3ria/Kubernetes.html)
- [Dynatrace](https://www.dynatrace.com/news/blog/kubernetes-vs-docker/)
***

&nbsp;
## ✨ Computação em Nuvem
### 💫 Conceito

**A Computação em Nuvem é a disponibilidade sob demanda dos recursos de computação como serviços na internet. Assim, elimina a necessidade das empresas comprarem, configurarem ou gerenciarem a Infraestrutura. Desse modo, elas pagam apenas pela utilização, nesse modelo não há licenças ou contratos rígidos de prestação de serviço. Tudo é adquirido conforme a necessidade dp cliente e do negócio.**

**Existem três tipos de modelos de serviços de computação em nuvem:**

- *A infraestrutura como serviço, oferece serviços de computação e armazenamento **(IaaS)**.*
- *A plataforma como serviço, ofere um ambiente de desenvolvimento **(PaaS)**.*
- *Implantação para criação de aplicativos em nuvem e o software como serviço entrega os aplicativos como serviços **(SaaS)**.*
***
### ✔️ Vantagens da Computação em Nuvem
Há diversas vantagens de usar a computação em nuvem. Entenda as principais:

**Eficiência:** É possível desenvolver novas aplicações e lançá-las rapidamente sem se preocupar com a infraestrutura.

**Flexibilidade:** Através da arquitetura da *Computação em Nuvem*, as empresas podem acessar os serviços de nuvem de qualquer lugar com uma conexão com a internet, aumentando ou reduzindo a escala de acordo com a necessidade.

**Valor Estratégico:** Provedores de Nuvem, como o *Google Cloud*, estão alinhados às recentes inovações para fonecê-las como serviços. Assim, as empresas tornam-se mais competitivas e alcançam um retorno de investimento maior do que se tivesse adquirido tecnologias que podem se tornar obsoletas em curto prazo.

**Segurança:** Os riscos de segurança da computação em nuvem são considerados baixos. A segurança da computação da Cloud é reconhecido como mais forte do que a de data centers corporativos, por exemplo, graças à profundidade e amplitude dos mecanismos de segurança que os processos de nuvem implementam.
**Economia:** Independente do modelo de serviço de computação em nuvem escolhido, as companhias pagam somente pelos recursos utilizados. Assim, você não precisa  sobrecarregar a capacidade do data center para atender a picos de demanda ou ao crescimento dos negócios, Com isso, a equipe de TI pode se dedicar a projetos mais estratégicos.
***

### 🏷️ Casos de Uso
O serviço de nuvem da Google por exemplo, oferece uma ampla variedade de aplicativos que podem beneficiar as organizações. Veja os principais:

- **Escalonamento de Infraestrutura:** As organizações das diferentes indústrias tem demandas e necessidades particulares nas quais a nuvem pode ajudar. A computação em nuvem atende as exigências por aumento de infraestrutura a qualquer momento.

- **Recuperação de desastres:** As empresas utilizam a computação em nuvem para fazer Backup de Segurança dos recursos digitais, em vez de deixar todos os dados no data center que pode sofrer algum prejuízo, como inovações, desastres naturais.

- **Armazenamento de Dados:** Possibilita aliviar data centers sobrecarregados armazenando grandes volumes de dados, tornando-os mais acessíveis, simplificando a análise e o backup dos mesmos.

- **Análise de dados:** A nuvem forcene inúmeros recursos para processar grandes volumes de dados (*Big Data*), acelerando a pequisa e reduzindo o tempo de insights.
***

### 🗃️ Google Cloud Dataflow
O **Google Cloud Dataflow** é um serviço de processamento de dados em tempo real, e em lote, oferecido pela *Google Cloud Platform*. Permite que os desenvolvedores criem e executem pipelines de processamento de dados de forma escalável e eficiete, sem se preocupar com a infraestrutura subjacente.
***

### ✅ Vantagens do Google Cloud Dataflow
O Dataflow oferece uma série de benefícios para os desenvolvedores e empresas que precisam lidar com grandes volumes de dados: 

- **Escalabilidade:** O serviço é capaz de processar grandes quantidades de dados de forma eficiente, escalando automaticamente de acordo com a demanda.

- **Flexibilidade:** Possibilita escrever códigos em várias linguagens e utilizar bibliotecas e frameworks populares, como *Apache Beam*, para implementar suas transformações de dados.

- **Integração com outros serviços Google:** O Dataflow pode ser facilmente integrado com outros serviços da plataforma, como *Big Query*, *Pub/Sub* e *Cloud Storage*, permitindo a criação de pipelines de dados ompletos.

- **Monitoramento e gerenciamento simplificados:** O Dataflow oferece ferramentas avançadas de monitoramente e gerenciamento, permitindo que os desenvolvedores acompanham o desempenho de seus pipelines e identifiquem possíveis problemas.
***

### 🔒️ Conclusão
O Dataflow é uma poderosa ferramenta para processamento de dados em tempo real e em lote. Com sua escalabiliade, flexibilidade e integração com outros serviços do Google Cloud Platform, ele ofece uma solução completa para lidar com grandes volumes de dados e realizar análises avançadas.
***

**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github](https://github.com/Game-JAVA/data_engineer/blob/main/wiki/subpages/virtualizacao.md)
- [GeoAmbiente](https://www.geoambiente.com.br/blog/google-cloud-o-que-e-computacao-em-nuvem-e-por-que-e-essencial-para-o-seu-negocio/?utm_term=&utm_campaign=Data+Soul+%7C+PMax+%7C+Cloud+Platform&utm_source=adwords&utm_medium=ppc&hsa_acc=4018137608&hsa_cam=20723657208&hsa_grp=&hsa_ad=&hsa_src=x&hsa_tgt=&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gad_source=1&gclid=Cj0KCQjw5ea1BhC6ARIsAEOG5py0RkLbM-gAbx6SJBUHk6OesvHE0527PdJ-4VyhsO9CuoWSFoq5NhcaAqtkEALw_wcB)
- [Azure](https://azure.microsoft.com/pt-br/resources/cloud-computing-dictionary/what-is-cloud-computing)
***
&nbsp;
## ✨ CI/CD

### 💫 Conceito
**A Integração Contínua *(CI)* é a prática de integrar, de forma automática e frequente, mudanças a um repositóio de código-fonte compartilhado. Já a Implantação e/ou Entrega Contínua *(CD)* é um processo em duas etapas relacionado a integração, teste e entrega de mudanças no código. A entrega contínua é quase uma implantação automática em produção, enquanto a implantação contínua implica em automaticamente lançar atualizações no ambiente de produção**


![ci/cd](/assets/cicd2.png)

**Juntas, essas práticas relacionadas são muitas vezes chamadas de *piplines de CI/CD*. Para implementá-las, é preciso que as equipes de operações e desenvolvimento trabalhem em conjunto seguindo princípios ágeis, com uma abordagem de *DevOps* ou de *Engenharia* de confiabilidade de sites (SRE)**
***

### 🔍️ Por que CI/CD é importante?

Com uma abordagem de **CI/CD**, as empresas podem evitar bugs e falhas no código, além de manter um ciclo contínuo de desenvolvimento e atualização de software. À medida que os apps evoluem, as funcionalidades de **CI/CD** ajudam a reduzir a complexidade, aumentar a eficiência e simplificar os fluxos de trabalho.

E como o pipeline de **CI/CD** automatiza o trabalho humano que em geral é necessário para que um novo código passe de um *commit* à produção, o downtime é minimizado e as versões atualizadas do código são disponibilizados mais rápido. Além disso, com a capacidade de agilizar a integração de incoporar o feedback dos usuários de maneira mais frequente e eficaz. Isso gera resultados positivos para os usuárops e uma maior satisfação dos clientes em geral.
***

### 🏷️ Integração Contínua (CI)

**Integração Contínua** é a prática de integrar o código produzido por diferentes membors de uma equipe em um repositório compartilhado com frequência, várias vezes é verificado automaticamente por meio da execução de testes automatizados. O objetivo da *CI* é detectar erros de integração o mais cedo possível, antes que eles causem problemas.
***

### 🔖 Entrega Contínua (CD)

A **Entrega Contínua** é uma extensão da *Integração Contínua* que se concentra em automatizar a construção, o teste e a implantação de uma solução para um ambiente de produção. A entrega contínua garante que o código esteja sempre em um estado pronto para implantação em produção, tornando a implantação um processo simples e escalável.
***

### ➕ Fluxo de Trabalho

Aqui está um exemplo simplificado de um fluxo de **CI/CD** para um projeto:

1. *Um desenvolvedor envia o código para um repositório Git.*
2. *Um Servidor de Integração (CI) monitora o repositório e detecta a alteração.*
3. *O Servidor CI realiza a construção do código e executa testes automatizados.*
4. *Se os testes forem bem-sucessidas, o código é implantado automaticamente em um ambiente de homologação.*
5. *Testes adicionais, como testes de aceitação são executados no ambiente de homologação.*
6. *Se todos os testes forem aprovados, o código é implantado em produção.*
7. *O aplicativo é monitorado em produção, e quaisquer problemas são detectados e tratados imediatamente.*
***

### 🔧 Ferramentas e Frameworks
As ferramentas de **CI/CD** ajudam a equipe a automatizar o desenvolvimento, a implantação e os testes. Algumas ferramentas tratam especificamente da *Integração (CI)*, algumas gerenciam o desenvolvimento e a *Implantação (CD)* e outras são especializadas em testes contínuos ou funções relacionadas. **Tekton Pipelines** é um framework para plataformas [Kubernetes](https://github.com/2RP-Squad404/Ricardo_Silva#-kubernetes) que proporciona uma experiência de *CI/CD* nativo em nuvem padrão com containers.

Além do **Tekton Pipelines**, existem outras ferramentas open source de **CI/CD**:

- **Jenkins:** *Projetado para lidar com tudo, desde um simples servidor de CI até um Hub de CD completo.*
- **Spinnaker:** *Uma plataforma de CD criado para ambientes **MultiCloud**.*
- **GoCD:** *Um servidor de CI/CD voltado para modelagem e visualização.*
- **Concourse:** *Plataforma open source contínua.*
- **Screwdriver:** *Plataforma de compilação criada para **CD**.*
***

### ✅ Vantagens do CI/CD

A **CI/CD** oferece uma gama de benefícios significativos, tais como:

- **Detecção Precoce de Erros:** A **CI** verifica constantemente o código, identificando erros e problemas de integração no estágio mais inicial do desenvolvimento.

- **Maior Qualidade de Software:** A execução de testes automatizados e a revisão contínua do código ajudam a garantir que o software seja mais confiável e livre de bugs.

- **Automatização de Tarefas:** A **CD** automatiza a construção, teste e implantação, economizando tempo e reduzindo a possibilidade de erros humanos.

- **Implantações mais rápidas:** Com  a **CD**, as implantações em produção podem ser feitas com mais frequência e mais facilidade, resultando em ciclos de desenvolvimento mais curtos.

- **Colaboração Eficiente:** A **CI** promove a colaboração contínua entre membros de equipe, garantindo que o código seja integrado e testado.

- **Maior Confiança e Transparência:** Com a **CI/CD**, a equipe temais confiança na estabilidade do código e pode rastrear as alterações com maior facilidade.
***

### 🔒️ Conclusão

**Em resumo, CI/CD não é apenas uma abordagem moderna para o desenvolvimento de software, mas também uma maneira eficaz de melhorar a qualidade, a eficiência e a colaboração no desenvolvimento de software. É um investimentoque vale a pena para equipes que buscam otimizar seus processos de entrega de software e melhorar a experiência do cliente. A medida que as organizações adotam a cultura DevOps, a CI/CD se torna cada vez mais um componente crítico para entregar softwares de alta qualidade de maneira eficiente e confiável.**
***

**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github](https://github.com/Game-JAVA/data_engineer/blob/main/wiki/subpages/cicd.md)
- [Red Hat](https://www.redhat.com/pt-br/topics/devops/what-is-ci-cd)
- [Unity](https://unity.com/pt/topics/what-is-ci-cd)
***
**Desafios Encontrados:**  
*Os assuntos abordados nessa trilha, foram um pouco mais fácil para entender, pois algumas ferramentas como CRM, ERP, até mesmo o Big Query, eu ja utilizei recentemente ou no passado, porem o restante do conteúdo, ainda sinto mais dificuldade relativamente alta para absorver.*

**Feedback e Ajustes:**  
*Descreva qualquer feedback que você recebeu e como você ajustou sua abordagem de estudo com base nesse feedback.*

**Próximos Passos:**  
*Os próximos passos são continuar a trilha de conhecimento, buscar alimentar mais as informações de cada trilha e continuar mantendo o padrão de estilização e organização.*


**Relatórios:**

[**1ª Semana**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana1)

[**2ª Semana**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana2)
***