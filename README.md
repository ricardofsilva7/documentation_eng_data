# 📜 Relatório de Estudos

**Nome do Estagiário: Ricardo Silva**  
**Data: 07/08/2024**

**Módulos/Etapas Feitas:**  
1. [**Virtualização**]()
2. [**Docker**]()
3. [**Kubernetes**]()
4. [**Computação em Nuvem**]()

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

 ### Docker e Contêineres Linux: qual a diferença?

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
**Desafios Encontrados:**  
*Acredito que no meu caso, o desafio é absorver todo conteúdo, considerando que venho de outra área de atuação e apesar de já ter evoluído bastante, ainda sinto dificuldade com as nomenclaturas e termos técnicos. Minha ideia é ir aprofundando os conteúdos conforme eu for absorvendo de fato o conteúdo.*

**Feedback e Ajustes:**  
*Descreva qualquer feedback que você recebeu e como você ajustou sua abordagem de estudo com base nesse feedback.*

**Próximos Passos:**  
*Os próximos passos são continuar a trilha de conhecimento, buscar alimentar mais as informações de cada trilha e continuar mantendo o padrão de estilização.*


**Relatórios:**

[**1ª Semana**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana1)
[**2ª Semana**]((https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana2))