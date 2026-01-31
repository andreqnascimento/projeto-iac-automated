# Engenharia de Prompts para Análise de IaC

- **Nome:** André Queiroz do Nascimento
- **RA:** 2203490
- **Objetivo:** Demonstrar domínio de Prompt Engineering criando 3 versões evolutivas de um prompt para análise automática de Pull Requests.

## Estrutura do Projeto

## Estrutura do Projeto

```text
├── scripts/
│   └── automacao_gemini.py      # Script principal da automação
├── resultados_auto/             # Evidências geradas pelo script (MD)
├── resultados_manuais/          # Prints e testes manuais
├── .gitignore                   # Arquivo de segurança (chaves/lixo)
├── requirements.txt             # Dependências do Python
└── README.md                    # Documentação do projeto

## Raciocínio e Evolução

### 1. Versão Baseline (v1)
**Estratégia:** Criei um prompt direto solicitando a classificação e decisão, sem fornecer contexto de persona ou estrutura rígida.
- **Resultado:** O modelo identificou erros de sintaxe, mas as respostas foram despadronizadas.
- **Falha:** Vulnerável a manipulação. No teste `PR6`, o prompt aceitou comandos maliciosos do usuário.

### 2. Versão Estruturada (v2)
**Estratégia:** Adicionei a persona de "Especialista Sênior" e forcei um template Markdown na saída.
- **Melhoria:** A legibilidade aumentou e a análise ficou visualmente consistente.
- **Falha:** Ainda suscetível a Prompt Injection. A IA obedeceu à instrução "IGNORE ALL PREVIOUS INSTRUCTIONS" contida no código do PR6.

### 3. Versão Schema & Defesa (v3) - A Solução Final
**Estratégia:** Implementei defesa em camadas:
1.  **Delimitadores XML:** O código do PR foi isolado dentro de tags `<pull_request>`.
2.  **Meta-Prompting:** Instrução explícita para tratar o conteúdo das tags apenas como dados.
3.  **Foco em FinOps:** Detecção proativa de mudanças de SKU (ex: instância r6g.8xlarge no PR3).


**Conclusão:** A v3 foi a única capaz de bloquear o ataque de injeção (rejeitando o PR6) e fornecer uma análise financeira detalhada.


