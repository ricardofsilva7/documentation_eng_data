# 📜 Relatório de Estudo - Terraform

<br>

## Parte 1: Definição e Fundamentos do Terraform

### O que é Terraform?
Terraform é uma ferramenta de **Infraestrutura como Código** (IaC). No conceito de IaC, é possível escrever código utilizando uma linguagem de configuração para definir, provisionar e gerenciar sua infraestrutura. Com a IaC, você só precisa declarar o estado final desejado da infraestrutura, e as ferramentas cuidam do gerenciamento e provisionamento automaticamente.

O Terraform permite que você provisione recursos no Google Cloud por meio de arquivos de configuração declarativos. Exemplos de recursos incluem **máquinas virtuais (VMs)**, **contêineres**, **armazenamento** e **redes**. Em um nível mais alto, o Terraform permite que os operadores criem arquivos contendo definições de recursos no provedor Google Cloud e automatizem a criação desses recursos.

#### Recursos do Terraform
- **Suporte a múltiplas nuvens** e **APIs variadas**: O Terraform oferece suporte a todos os principais provedores de nuvem, além do Google Cloud e serviços expostos via API, como GitHub e Kubernetes.

### Provisionamento vs. Configuração
- **Provisionar**: Refere-se ao processo de criar e gerenciar recursos de infraestrutura, como máquinas virtuais e clusters.
- **Configurar**: Refere-se à configuração interna do sistema operacional (SO) das VMs.

#### Exemplo:
- **Provisionamento**: A IaC automatiza a criação de um cluster do GKE no Google Cloud.
- **Configuração**: Automatiza a implantação de contêineres dentro do cluster do GKE.

> "Concentre-se em como a infraestrutura deve ser, enquanto a automação determina como chegar ao estado desejado."

<br>

## Parte 2: Fluxo de Trabalho do Terraform

1. **Escopo**: Defina quais recursos precisam ser criados.
2. **Criação**: Escreva o código de configuração da infraestrutura desejada.
3. **Inicialização**: Use `terraform init` para instalar plugins e módulos necessários.
4. **Planejamento**: Utilize `terraform plan` para gerar um plano de execução.
5. **Aplicação**: Execute `terraform apply` para criar a infraestrutura.
6. **Fase de Validação (opcional)**: Utilize ferramentas como o **Terraform Validator** para garantir compliance.

#### Benefícios do Terraform Validator:
1. Aplicação de políticas em qualquer fase.
2. Automatização da validação de políticas.
3. Redução de erros manuais.

<br>

## Parte 3: Comandos HCL no Terraform

1. **`terraform init`**: Inicializa o provedor com um plugin.
2. **`terraform plan`**: Fornece uma prévia dos recursos a serem criados.
3. **`terraform apply`**: Aplica o plano e cria os recursos.
4. **`terraform fmt`**: Formata automaticamente os arquivos de configuração.
5. **`terraform destroy`**: Remove todos os recursos gerenciados pelo Terraform.

<br>

## Parte 4: Casos de Uso do Terraform

- **Gerenciamento de Infraestrutura**: Reduz a complexidade de modificar serviços.
- **Rastreamento de Alterações**: O Terraform mantém um estado detalhado da infraestrutura.
- **Automatização de Alterações**: A infraestrutura é gerenciada automaticamente pelo código declarativo.
- **Padronização de Configurações**: Módulos garantem a implementação de práticas recomendadas.

<br>

## Parte 5: Variáveis no Terraform

### 5.1 Definição e Parametrização
- **Variáveis no Terraform** permitem parametrizar a configuração, tornando-a flexível.

### 5.2 Declaração de Variáveis
- Variáveis são declaradas no bloco `variable` e salvas em um arquivo separado chamado `variables.tf`.

### 5.3 Tipos de Variáveis
- `bool`, `number`, `string` são alguns dos tipos suportados.

### 5.4 Argumentos Meta
- **Default**: Define um valor padrão.
- **Sensitive**: Protege informações sensíveis.

### 5.5 Atribuição de Valores em Tempo de Execução
- Valores podem ser fornecidos via arquivos `.tfvars`, CLI, ou variáveis de ambiente.

### 5.6 Precedência de Valores
1. Valor fornecido pela opção `-var`.
2. Arquivos `.tfvars`.
3. Variáveis de ambiente.
4. Valores padrão.

### 5.7 Validação de Variáveis
- Blocos de **validação** podem ser usados para garantir que os valores atribuídos estejam dentro de um conjunto de regras.

<br>

## Parte 6: Melhores Práticas para o Uso de Variáveis

1. **Parametrização Seletiva**: Apenas variáveis que realmente necessitam de mudanças.
2. **Arquivos `.tfvars`**: Use-os para fornecer valores.
3. **Nomes Descritivos**: Inclua unidades quando necessário (ex: `disk_size_gb`).
4. **Variáveis Booleanas**: Use nomes positivos (`enable_external_access`).
5. **Descrições de Variáveis**: Sempre inclua descrições nas variáveis.

<br>

## Parte 7: Valores de Saída no Terraform

### 7.1 O que são valores de saída?
- **Valores de saída** são como valores de retorno e permitem visualizar informações sobre os recursos criados.

### 7.2 Uso entre Recursos
- Permitem passar informações de um recurso para outro.

### 7.3 Declaração de Valores de Saída
- São declarados com o bloco `output` e podem ser armazenados em `output.tf`.

### 7.4 Argumentos do Bloco de Saída
- **`value`**: Valor a ser retornado.
- **`description`**: Explica o propósito do output.
- **`sensitive`**: Oculta valores sensíveis.

<br>

## Parte 8: Melhores Práticas para Valores de Saída

1. **Informe apenas dados úteis**: Evite repetir informações.
2. **Nomes Significativos**: Utilize nomes e descrições claras para os outputs.
3. **Marque valores sensíveis**: Utilize o suporte do Terraform para valores sensíveis.

<br>

## Conclusão

**O Terraform é uma ferramenta poderosa para gerenciar infraestrutura com código, aplicando automação e boas práticas em ambientes complexos, e suportando múltiplos provedores de nuvem.**
