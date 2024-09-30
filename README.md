# 📜 Relatório de Estudo - Terraform

## 📚 Sumário
1. 🌍 [Definição e Fundamentos do Terraform](https://github.com/2RP-Squad404/Ricardo_Silva/tree/Terraform?tab=readme-ov-file#-defini%C3%A7%C3%A3o-e-fundamentos-do-terraform)
2. 🔄 [Fluxo de Trabalho do Terraform](https://github.com/2RP-Squad404/Ricardo_Silva/tree/Terraform?tab=readme-ov-file#-fluxo-de-trabalho-do-terraform)
3. 🛠️ [Comandos HCL no Terraform](https://github.com/2RP-Squad404/Ricardo_Silva/tree/Terraform?tab=readme-ov-file#%EF%B8%8F-comandos-hcl-no-terraform)
4. 📦 [Casos de Uso e Benefícios de Módulos no Terraform](https://github.com/2RP-Squad404/Ricardo_Silva/tree/Terraform?tab=readme-ov-file#-casos-de-uso-e-benef%C3%ADcios-de-m%C3%B3dulos-no-terraform)
5. 🔧 [Variáveis e Outputs no Terraform](https://github.com/2RP-Squad404/Ricardo_Silva/tree/Terraform?tab=readme-ov-file#-vari%C3%A1veis-e-outputs-no-terraform)
6. 🗂️ [Estado do Terraform (Terraform State)](https://github.com/2RP-Squad404/Ricardo_Silva/tree/Terraform?tab=readme-ov-file#%EF%B8%8F-estado-do-terraform-terraform-state)
7. ✅ [Melhores Práticas e Segurança no Uso de Terraform](https://github.com/2RP-Squad404/Ricardo_Silva/tree/Terraform?tab=readme-ov-file#-melhores-pr%C3%A1ticas-e-seguran%C3%A7a-no-uso-de-terraform)
8. 🏁 [Conclusão](https://github.com/2RP-Squad404/Ricardo_Silva/tree/Terraform?tab=readme-ov-file#-conclus%C3%A3o)

<br>


## 🌍 Definição e Fundamentos do Terraform
### O que é Terraform?
Terraform é uma ferramenta de Infraestrutura como Código (IaC) que permite automatizar a criação, gerenciamento e provisionamento de infraestrutura. Em vez de configurar recursos manualmente via interfaces de cloud providers, o Terraform utiliza uma linguagem declarativa para definir como a infraestrutura deve ser criada e mantida.

- **Suporte a múltiplas nuvens:** Como Google Cloud, AWS, Azure e outros.
- **Linguagem HCL (HashiCorp Configuration Language):** Facilita a leitura e a manutenção das configurações de infraestrutura.

### Exemplo de uso do Terraform:
Imagine que você quer criar uma instância de VM no Google Cloud. Você escreve o código a seguir:

```hcl
resource "google_compute_instance" "default" {
  name         = "my-vm-instance"
  machine_type = "e2-medium"
  zone         = "us-central1-a"

  boot_disk {
    initialize_params {
      image = "debian-cloud/debian-10"
    }
  }

  network_interface {
    network = "default"
  }
}
```

### Provisionamento vs. Configuração
- **Provisionamento:** Criação de recursos, como máquinas virtuais e redes.
- **Configuração:** Ajustes internos no sistema operacional das VMs, como a instalação de pacotes.

**Exemplo:**
- **Provisionamento:** Criar uma instância de VM.
- **Configuração:** Instalar o Docker nessa VM automaticamente.

<br>

## 🔄 Fluxo de Trabalho do Terraform
1. **Escopo:** Definir quais recursos serão criados.
2. **Criação:** Escrever o código de configuração da infraestrutura.
3. **Inicialização:** Executar `terraform init` para configurar o ambiente.
4. **Planejamento:** Utilizar `terraform plan` para visualizar as mudanças que serão feitas.
5. **Aplicação:** Executar `terraform apply` para provisionar a infraestrutura.
6. **Validação (opcional):** Usar ferramentas como o Terraform Validator para garantir a conformidade da infraestrutura com políticas internas.

### Benefícios do Terraform Validator
- **Automação de validação:** Garante que a infraestrutura segue as melhores práticas e requisitos de compliance.
- **Redução de erros manuais:** Minimiza falhas humanas na criação de infraestruturas complexas.

<br>

## 🛠️ Comandos HCL no Terraform
- `terraform init`: Inicializa o diretório de trabalho com os plugins necessários.
- `terraform plan`: Gera um plano de execução que mostra o que será modificado.
- `terraform apply`: Aplica as mudanças descritas no plano, criando ou modificando recursos.
- `terraform fmt`: Formata os arquivos `.tf` para melhorar a legibilidade.
- `terraform destroy`: Remove todos os recursos gerenciados pelo Terraform.

### Exemplo de Execução:

```bash
terraform init
terraform plan
terraform apply
```

<br>

## 📦 Casos de Uso e Benefícios de Módulos no Terraform
### Onde e como os módulos podem ser úteis?
Os módulos no Terraform permitem organizar o código de maneira reutilizável e legível. Um módulo é basicamente um conjunto de arquivos Terraform agrupados em uma unidade lógica.

**Exemplo:** Ao criar uma rede VPC, você pode definir todas as sub-redes, regras de firewall e rotas em um único módulo reutilizável. Toda vez que precisar criar uma nova rede, basta chamar o módulo com as variáveis apropriadas.

### Benefícios dos Módulos:
- **Reutilização:** Escreva o código uma vez e reutilize em diferentes ambientes (produção, staging, dev).
- **Manutenção fácil:** Atualizações em um módulo automaticamente afetam todos os ambientes que o utilizam.
- **Abstração de complexidade:** Isola detalhes internos da infraestrutura, facilitando o uso por outros desenvolvedores.
- **Padronização:** Módulos permitem a implementação consistente de boas práticas.

### Estrutura de Módulos:

```bash
.
├── main.tf      # Código principal
├── variables.tf # Definição de variáveis
├── outputs.tf   # Definição de outputs
```

### Exemplo de Módulo:

```hcl
module "vpc" {
  source       = "./modules/vpc"
  region       = "us-central1"
  network_name = "my-vpc-network"
}
```

<br>

## 🔧 Variáveis e Outputs no Terraform
### Variáveis
As variáveis no Terraform permitem a parametrização da configuração, tornando o código reutilizável e adaptável para diferentes ambientes.

**Exemplo de Variável:**

```hcl
variable "region" {
  description = "Região onde os recursos serão criados"
  type        = string
  default     = "us-central1"
}
```

### Outputs
Outputs são utilizados para expor atributos de um recurso criado por um módulo para serem consumidos em outros módulos ou blocos.

**Exemplo de Output:**

```hcl
output "instance_ip" {
  description = "Endereço IP da instância"
  value       = google_compute_instance.default.network_interface[0].access_config[0].nat_ip
}
```

### Uso de Variáveis e Outputs em Módulos

**Exemplo:**
Você pode passar variáveis entre módulos e capturar outputs:

```hcl
module "vpc" {
  source       = "./modules/vpc"
  region       = var.region
}

module "server" {
  source       = "./modules/server"
  network_name = module.vpc.network_name
}
```

<br>

## 🗂️ Estado do Terraform (Terraform State)
### O que é o Terraform State?
O Terraform State é um arquivo que mantém o estado atual da infraestrutura gerenciada pelo Terraform. Ele mapeia o que foi definido nos arquivos de configuração com o que foi provisionado na realidade.

### Características:
- **terraform.tfstate:** Arquivo onde o estado é salvo localmente.
- **Armazenamento remoto:** Recomenda-se armazenar o estado de forma remota para equipes, como no Google Cloud Storage, para evitar conflitos e garantir segurança.

### Exemplo de Configuração de Estado Remoto:

```hcl
terraform {
  backend "gcs" {
    bucket = "my-terraform-state"
    prefix = "env/prod"
  }
}
```

### Armazenando Arquivos de Estado
- **Estado Local:** Funciona bem para um único desenvolvedor.
- **Estado Remoto:** Necessário para equipes, garantindo que todos compartilhem o mesmo arquivo de estado.

### Vantagens do Estado Remoto:
- **Sincronização automática:** Todos os desenvolvedores têm acesso ao estado mais recente.
- **Locking:** Impede que múltiplos usuários modifiquem o estado ao mesmo tempo.
- **Segurança:** Arquivos de estado podem conter dados sensíveis, e o armazenamento remoto oferece criptografia.

<br>

## ✅ Melhores Práticas e Segurança no Uso de Terraform
### Melhores Práticas:
- **Modularize o código:** Para evitar duplicação e facilitar a manutenção.
- **Use estado remoto:** Especialmente em equipes, para evitar problemas de concorrência.
- **Parâmetros sensíveis:** Marque variáveis confidenciais com `sensitive = true` para evitar que sejam exibidas em logs.
- **Criptografe o estado:** Mesmo que o bucket seja criptografado, utilize Customer-Managed Encryption Keys (CMEK) para controle extra.

### Segurança no Terraform:
- **Segredos no Estado:** Evite armazenar dados confidenciais no estado, como senhas e chaves de API.
- **Git Ignore:** Adicione `terraform.tfstate` no `.gitignore` para evitar comprometer o estado.
- **Permissões IAM:** Configure permissões rigorosas para quem pode acessar e modificar o estado.

<br>

## 🏁 Conclusão
O Terraform é uma ferramenta poderosa para o gerenciamento de infraestrutura como código. Entender os fundamentos de módulos, variáveis, outputs e o estado é essencial para a criação de infraestruturas seguras e escaláveis. Ao seguir as melhores práticas de modularização e segurança, você garante que sua infraestrutura esteja sempre em conformidade com as necessidades do seu projeto.

<br>



# 🌐 Exemplo para Criação de Dataset no BigQuery e Catálogo no Dataplex

<br>

## 1. Criação do Dataset no BigQuery

### 1.1 Configuração no Terraform

1. 📁 Definindo o recurso `google_bigquery_dataset` no arquivo `.tf`:

```hcl
resource "google_bigquery_dataset" "dataset" {
  dataset_id = var.dataset_id
  project    = var.project_id
  location   = "US"  # ou outra região de sua escolha

  labels = {
    env = "development"
  }
}
```

2. 📊 Definindo o recurso `google_bigquery_table` se precisar criar uma tabela no dataset:

```hcl
resource "google_bigquery_table" "table" {
  table_id   = var.table_id
  dataset_id = google_bigquery_dataset.dataset.dataset_id
  project    = var.project_id

  schema = <<EOF
[
  {
    "name": "id",
    "type": "STRING",
    "mode": "REQUIRED"
  },
  {
    "name": "name",
    "type": "STRING",
    "mode": "NULLABLE"
  }
]
EOF
}
```

### 1.2 Variáveis

🛠️ Adicionando as variáveis no arquivo `variables.tf`:

```hcl
variable "dataset_id" {
  description = "ID do dataset"
  type        = string
}

variable "table_id" {
  description = "ID da tabela"
  type        = string
}

variable "project_id" {
  description = "ID do projeto no GCP"
  type        = string
}
```

### 1.3 Outputs (opcional)

💡 Se for necessário exportar o ID do dataset ou tabela, adicionar no arquivo `outputs.tf`:

```hcl
output "dataset_id" {
  value = google_bigquery_dataset.dataset.dataset_id
}

output "table_id" {
  value = google_bigquery_table.table.table_id
}
```

---

## 2. Criação do Catálogo no Dataplex

### 2.1 Criação de um Lago no Dataplex

🏞️ Adicionando o recurso `google_dataplex_lake` no seu arquivo `.tf`:

```hcl
resource "google_dataplex_lake" "lake" {
  name     = var.lake_name
  project  = var.project_id
  location = "southamerica-east1"
}
```

### 2.2 Criação de uma Zona no Lago

🌍 Adicionando o recurso `google_dataplex_zone`:

```hcl
resource "google_dataplex_zone" "zone" {
  name     = var.zone_name
  project  = var.project_id
  lake     = google_dataplex_lake.lake.id
  location = "southamerica-east1"
  type     = "CURATED"  # Ou "RAW", dependendo do caso

  resource_spec {
    location_type = "SINGLE_REGION"  
  }

  discovery_spec {
    enabled = true
  }
}
```

### 2.3 Criação de um Asset no Dataplex

🗂️ Por fim, o recurso `google_dataplex_asset`:

```hcl
resource "google_dataplex_asset" "asset" {
  name          = "asset1"
  location      = "southamerica-east1"
  lake          = google_dataplex_lake.lake.id
  dataplex_zone = google_dataplex_zone.zone.id

  resource_spec {
    name = "spartan-avenue-434715-u7.campanhas_selecionadas.table_terraform"
    type = "BIGQUERY_DATASET"
  }

  discovery_spec {
    enabled = false
  }

  labels = {
    env     = "foo"
    asset   = "my_asset"
  }

  project = var.project_id
  depends_on = [
    google_bigquery_table.table_id
  ]
}
```

---

## 3. Aplicando o Terraform

1. 🏁 Inicializa o Terraform:
```bash
terraform init
```

2. ✅ Valida a configuração:
```bash
terraform validate
```

3. 🚀 Aplica a configuração:
```bash
terraform apply
```

---

