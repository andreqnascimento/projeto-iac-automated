# Engenharia de Prompts para Análise de IaC

* **Nome:** André Queiroz do Nascimento
* **RA:** 2203490
* **Objetivo:** Demonstrar domínio de Prompt Engineering criando 3 versões evolutivas de um prompt para análise automática de Pull Requests, focando em segurança e FinOps.
* **RepoGit** https://github.com/andreqnascimento/projeto-iac-automated

---

## 🤖 Automação de Code Review com Google Gemini

Este projeto implementa um **Agente de IA** utilizando a API do Google Gemini para automatizar a revisão de código Terraform. O sistema analisa riscos de segurança e custos antes da aprovação.

## 🛠️ Guia de Instalação e Execução (Passo a Passo)

Siga este roteiro para executar o projeto em qualquer máquina (Windows, Linux ou Mac).

### 1. Pré-requisitos
* Ter o **Python 3.8+** instalado. [Baixar Python aqui](https://www.python.org/downloads/).
* Ter uma **API Key do Google Gemini** (Gratuita). [Gerar Key aqui](https://aistudio.google.com/app/apikey).
* Ter o **Git** instalado (Opcional, caso queira clonar).

### 2. Baixar o Projeto
Abra o terminal (Prompt de Comando ou PowerShell) e clone o repositório:

```bash
git clone [https://github.com/andreqnascimento/projeto-iac-automated.git](https://github.com/andreqnascimento/projeto-iac-automated.git)
cd projeto-iac-automated

### 🚀 Funcionalidades

* **Análise de Segurança:** Detecta vulnerabilidades (ex: Buckets públicos, Security Groups abertos).
* **Análise FinOps:** Identifica recursos caros ou superdimensionados (ex: instâncias DB muito grandes).
* **Defesa Anti-Injection:** Bloqueia tentativas de manipulação da IA (Prompt Injection) usando estratégias de defesa em camadas.
* **Relatórios Automáticos:** Gera arquivos `.md` com o parecer detalhado (Aprovar/Rejeitar).

### 📂 Estrutura do Projeto



```text
├── resultados_auto/             # Relatórios gerados automaticamente (Evidências)
├── resultados_manuais/          # Prints e testes iniciais
├── .gitignore                   # Arquivo de segurança (Ignora chaves/lixo)
├── automacao_gemini.py          # Script principal da automação (Python)
├── requirements.txt             # Lista de dependências do projeto
└── README.md                    # Documentação do projeto
