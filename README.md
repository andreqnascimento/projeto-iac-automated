# Engenharia de Prompts para Análise de IaC

- **Nome:** André Queiroz do Nascimento
- **RA:** 2203490
- **Objetivo:** Demonstrar domínio de Prompt Engineering criando 3 versões evolutivas de um prompt para análise automática de Pull Requests.

# 🤖 Automação de Code Review de IaC com Google Gemini

Este projeto implementa um **Agente de IA** utilizando a API do Google Gemini para automatizar a revisão de Pull Requests (PRs) de Infraestrutura como Código (Terraform).

O objetivo é garantir segurança, conformidade e otimização de custos (FinOps) antes que o código seja aprovado, além de demonstrar técnicas de defesa contra ataques adversariais em LLMs.

## 🚀 Funcionalidades

* **Análise de Segurança:** Identifica vulnerabilidades em recursos AWS (ex: Buckets S3 públicos, Security Groups abertos).
* **Análise FinOps:** Avalia o impacto financeiro das mudanças (ex: instâncias de banco de dados superdimensionadas).
* **Defesa Anti-Injection:** Utiliza a técnica de *Sandwich Defense* e prompts estruturados para bloquear tentativas de "Prompt Injection".
* **Relatórios Automáticos:** Gera arquivos Markdown (`.md`) com o parecer detalhado da IA (Aprovar/Rejeitar).

## 📂 Estrutura do Projeto

```text
├── scripts/
│   └── automacao_gemini.py      # Script Python principal (Lógica da IA)
├── resultados_auto/             # Relatórios gerados automaticamente pelo script
├── resultados_manuais/          # Evidências de testes manuais e prints
├── .gitignore                   # Arquivos ignorados pelo Git (segurança)
├── requirements.txt             # Lista de dependências do Python
└── README.md                    # Documentação do projeto
