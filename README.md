# 📜 Relatório de Estudos

**Nome do Estagiário: Ricardo Silva**  
**Data: 20/08/2024**

**Módulos/Etapas Feitas:**  
1. [**Linux/Shell**]()

***

# 📚 Resumo dos Módulos 
&nbsp;

## ✨ Linux/Shell

### 💫 Conceito
**Shell Script é o nome dado a um arquivo que será interpretado por algum programa tipo Shell. Atualmente existem vários progamas tipo Shell. Além dos principais _sh_ e _bash_, exsitem também *KSH, ZSH, CSH, TCSH*. Um Shell Script necessita basicamente do _Interpretador Shell_. Algumas operações tipicas são executadas por uma linguagem de script em Shell incluem; manipulação de arquivos, execução de programas e impressão de texto.**
***
### 🔖  Principais Componentes 


- **Script:** Um script é um arquivo que contém uma sequênciade comandos que são executados pelo Shell. Ele pode incluir variáveis, loops, condicionais e funções para executar tarefas automatizadas.
- **Comandos:** Shell scripts consistem em comandos que o shell pode executar, como _ls_ para listar arquivos, _grep_ para buscar padrões e _CP_ para copiar arquivos.
- **Variáveis:** Variáveis em Shell scripts são usados para armazenar dados que podem ser utilizados em comandos e operações. Elas são definidas com um nome e podem armazenar valores como _strings_ e _números_.
- **Loops e condicionais:** Shell scripts podem incluir estruturas de controle, como loops (_for, while_) e condicionais (_if/else_), para executar comandos repetidamente ou tomar decisções com base nas condições.
- **Funções:** Funções permitem encapsular um conjunto de comandos em um bloco reutilizável, facilitando a moduralização e manutenção do script.
***

### 📝 Casos de Uso

É possível utilizar o Shell de forma interativa. Quando o usuário realiza uma operação simples, como execução de algum comando _ls, cat ou od_, o Shell está sendo utilizado interativamente. Porém, essa forma de uso pode ser cansativa, se as operações são repetidas continuamente, sendo mais prático colocar esses comandos em um arquivo para reaproveitamento, isto é, criar um script.

O uso automatizado (não-interativo) do Shell script (utilizando arquivos com comandos) deve ser feito quando é necessário criar uma rotina a ser executada por todos os usuários sem necessitar digitá-lo comando por comando; procedimentos complexos usando muitas linhas de comando; execução de uma tarefa planejada para ocorre em uma determinada data; interação de informações de vários sistemas existentes, tarefas rotineiras e etc.

***
### 💡 Funcionalidades e Capacidades

- **Selecionar Shell:** Para selecionar qual Shell será utilizado, use a combinação de hashtagh **(#)** mais exclamação **(!)** e o caminho do excutável na primeira linha do script, isso vem a ser conhecido como **Shebang**. Para declarar que o script deve ser interpretado por _Bourn Shell (sh)_, a primeira linha será ecrita da seguinte forma:

~~~
                                          #!/bin/sh
~~~~

Para declarar que o script deve ser interpretado por _Bourne-Again shell(Bash)_ é recomendável utilização do comando **env**, pelo fato que apesar de o Bash já vir instalado em muitas distribuições _Linux_, não sabemos se estará em todas elas no mesmo diretório _/bin/_, então deve usar da seguinte forma:

~~~
                                    #!/usr/bin/env bash
~~~


- **Variáveis:** Em uma breve explicação uma variável é um nome/objeto simbólico ao qual podemos atribuir valor, ler ou manipular o conteúdo. Os scripts em Shell podem lidar com diferentes tipos de variáveis sem precisar definir o tipo:
~~~~
                            mensagem_tipo1 = "Unix Shell"
                            MENSAGEM_NOME = "Bourne Shell"
                            mensagem_autor = "Stephen Bourne"
                            MENSGEM = "Olá"
~~~~

&nbsp;

 **Variáveis pré-definidas:** Os scripts em Shell  possuem as seguintes variáveis pré-definidas:
 
 - **#?** - Armazena o status de saída do último programa executado
 - **$#** - Armazena a quantidade de parâmetros de linha de comando.
 - **$$** - Armazena o valor **PID (Process Identifier)** do script em shell que estiver em execução.
 - **$@** - Armazena o valor de todos os parâmetros passados, similar a variável _argv_ presente nas linguagens de programação _C_ e _C#_.
 - **$!** - Armazena o PID do último processo em segundo plano. Isso é útil para acompanhar o processo à medida que o trabalho é realizado.


 **Variáveis Globais:** São variáveis criadas/definidas com o comando expert e podem ser utilizados por múltipos scripts em Shell. Um exemplo é a variável de ambiente _Lang(Pré definida em diversas distribuições Linux)_, podendo ser acessado por diversos arquivos de script em Shell - outras variáveis pré-definidas são:

- **PATH :** *Define diretórios de procura por programas executados no Shell.*
- **USER :** *Informa o nome do usuário shell*
- **HOME :** *Informa o caminho do diretório home do usuário.*
- **LANG :** *Idioma - Linguagem, especificado como locale.*
- **PWD :** *diretório atual.*
- **TERM :** *Tipo terminal atual em uso.*
- **UID :** *UID do usuário atual.*
- **RANDOM :** *Gera um número aleatório.*
***

### 🔒️ Conclusão
**O Shell script permite explorar e personalizar o ambiente e combinar comandos de forma a realizar tarefas que vão da criação de arquvos até a realização de backups. Esta variação demosntra a importância de se dominar o foco deste estudo. Com ele é possível automatizar tarefas e tomar nossas atividades de administração de sistemas muito mais simples.**
***
**Recursos Utilizados:**  
- [Trilha de Conhecimento - Github](https://github.com/Game-JAVA/data_engineer/blob/main/wiki/subpages/linux_shell.md)
- [Artigo - DevMedia](https://www.devmedia.com.br/introducao-ao-shell-script-no-linux/25778)
***

**Desafios Encontrados:**  
*Os assuntos dessa semana foram relativamente dificeis, como a parte do Shell e comandos, pois é um assunto que nunca me aprofundei, apesar de ja ter utilizado comandos Shell, o restante dos asssuntos estudados foram um pouco mais tranquilo em realação ao assunto do Linux/Shell.*

**Feedback e Ajustes:**  
*Descreva qualquer feedback que você recebeu e como você ajustou sua abordagem de estudo com base nesse feedback.*

**Próximos Passos:**  
*Os próximos passos são continuar a trilha de conhecimento de acordo com a demanda que será enviado para nós nos proximos dias, pois tive pouco tempo para focar na parte prática da trilha de conhecimento.*

&nbsp;

**Relatórios:**

[**1ª Semana**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana1)

[**2ª Semana**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana2)

[**3ª Semana**](https://github.com/2RP-Squad404/Ricardo_Silva/tree/semana3)
***