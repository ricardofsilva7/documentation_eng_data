# 📜 Relatório de Estudos

**Nome do Estagiário: Ricardo Silva**  
**Data: 14/08/2024**

**Módulos/Etapas Feitas:**  
1. [**Virtualização**](https://github.com/2RP-Squad404/Ricardo_Silva#-virtualiza%C3%A7%C3%A3o)
2. [**Docker**](https://github.com/2RP-Squad404/Ricardo_Silva#-docker)
3. [**Kubernetes**]()

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
- **Virtualização de Função de Rede:** *Supera as funções de uma rede (como serviços de diretório, compartilhamento de arquivos e configuração de IP) para distribuí-las entre os ambientes.
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
- [Trilha de Conhecimento - Github]
- [Pesquisas no Google]
- [Artigos]
***
&nbsp;

## ✨ Docker

### 💫 Conceito
**A palavra *Docker* tem várias definições; Um projeto da comunidade open source, ferramentas resultantes desse projeto, a empresa *Docker Inc*, principal apoiadora do projeto, e as ferrametnas compatíveis formalmente com a empresa. O fato da empresa e das tecnologias terem o mesmo nome pode causar alguma confusão**

- *O software de TI **Docker** é uma tecnologia de conteinerização para criação e uso de conteineres Linux.*
- *A comunidade open source do Docker trabalha gratuitamente para melhorar essas tecnologias para todos usuários.*
- *A empresa **Docker Inc.** se baseia no trabalho feito pela comunidade do Docker, tornando-o mais seguro em geral. Depoi, ela oferece aos clientes empresariais o suporte necessário para as tecnologias, que foram aprimoradas e fortalecidas.*

**Com o Docker, é possível lidar com os conteiners como se fossem máquinas virtuais modulares e extremamente lightweight. Além disso, os conteineres oferecem maior flexibilidade para você criar, implantar, copiar e migrar um contêiner de um ambiente para outro.**

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

 `Containers:` Unidades leves e potáteis que encapsulam o aplicativo e suas dependências em um ambiente isolado
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
- [Trilha de Conhecimento - Github]
- [Pesquisas no Google]
- [Artigos]
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

**Expansão automática:** *Quando o tráfego aumenta, o dimensionamento automático do Kubernetes pode criar novos Clusters conforme necessário para lidar com a carga de trabalho adcional.*

**Autocorreção para alta qualidade:** *Quando um contêiner falha, o Kubernetes pode renunciá-lo ou substituí-lo automaticamente para evitar "downtime". Possibilita derrubar contêineres que não atendem aos requisitos de verificação de integridade.*
***

### ⚡Kubernetes vs. Docker

O Docker é um conjunto de ferramentas de desenvolvimento de software para criar, compartilhar e executar contêineres individuais; O Kubernetes é um sistema para operar aplicativos em contêineres padronizadas para microsserviços como todo o código de aplicativo e dependências necessárias dentro. Criar esses contêineres é o domínio do Docker.

Um aplicativo moderno consiste em muitos contêineres, operá-los em produção é o trabalho do Kubernetes. Como os contêineres são fáceis de replicar, os aplicativos pode serm dimensionados automaticamente.

**Docker** e **Kubernetes** são, em sua maioria, tecnologias complementares. No entanto, o Docker também fornece um sistema para operar aplicativos em contêineres em escala, chamado **Docker Swarm**.
***

### 🔒️ Conclusão
 **O Kubernetes representa uma revolução na forma como os aplicativos são gerenciados, fornecendo uma plataforma poderosa e flexível para a implantação e orquestração eficientes de contêineres em escala. Com a adoçao generalizada e evolução contínua, o Kubernetes se tornou um pilar fundamental da infraestrutura moderna de TI, capaitando as empresas a impulsionar a invocação e fornecer serviços confiáveis em um mundo cada vez mais digital.**

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

[**2ª Semana**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana2)