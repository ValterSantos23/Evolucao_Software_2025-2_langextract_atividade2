# Análise de Governança de Software com Modelos de Linguagem  
## Estudo de Caso: Projeto LangExtract

Este repositório contém os artefatos, códigos e documentação referentes à **Atividade 2 – Gerência de Configuração**, da disciplina **Engenharia de Software II**, da **Universidade Federal de Sergipe (UFS)**.

O trabalho propõe uma abordagem técnica para análise de **governança em projetos de software open source**, utilizando **modelos de linguagem de grande porte (LLMs)** como ferramentas de apoio à interpretação de dados reais extraídos de um repositório Git.

---
## 🔗 Links Importantes

- Repositório do LangExtract:  
  https://github.com/google/langextract

- Repositório da Atividade:  
  https://github.com/ValterSantos23/Evolucao_Software_2025-2_langextract_atividade2

- Vídeo tutorial:  
  https://www.youtube.com/watch?v=YYo4CtIqv24
---


## 📌 Objetivo do Trabalho

Analisar a governança do projeto open source **LangExtract** (Google), com foco em:

- Identificação do **modelo de fluxo de trabalho** (branching model)
- Identificação da **estratégia de releases**
- Comparação dos resultados obtidos por **diferentes modelos de linguagem**

A análise é baseada **exclusivamente em dados técnicos reais**, extraídos do histórico Git do projeto, como branches, merges, tags e métricas temporais entre releases.

---

## 📂 Estrutura do Repositório


- `codigo/`: Notebook Google Colab contendo todo o código de extração, processamento e análise.
- `documento/`: Relatório final da atividade em formato PDF.
- `README.md`: Documento descritivo do projeto (este arquivo).

---

## 🧪 Metodologia

A metodologia adotada é composta pelas seguintes etapas:

1. **Preparação do Ambiente**
   - Execução no Google Colab
   - Instalação das bibliotecas:
     - `transformers`
     - `bitsandbytes`
     - `accelerate`
     - `torch`

2. **Extração de Metadados do Repositório**
   - Clonagem do repositório `google/langextract`
   - Extração de:
     - Branches
     - Histórico de merges
     - Tags de release
     - Datas associadas às releases

3. **Processamento dos Dados**
   - Limpeza de códigos ANSI
   - Organização cronológica das releases
   - Cálculo de métricas temporais:
     - Intervalo médio
     - Intervalo mínimo e máximo
     - Desvio padrão

4. **Análise Assistida por Modelos de Linguagem**
   - Construção de um **contexto técnico estruturado**
   - Uso de um **prompt padronizado**
   - Execução independente da análise com múltiplos modelos

5. **Comparação e Discussão dos Resultados**
   - Avaliação da convergência e divergência entre modelos
   - Análise da consistência das conclusões

---

## 🤖 Modelos de Linguagem Utilizados

Foram utilizados **sete modelos distintos**, todos executados sob as mesmas condições experimentais:

| Modelo | Finalidade |
|------|-----------|
| mistralai/Mistral-7B-Instruct-v0.3 | Modelo generalista com bom equilíbrio entre desempenho e custo |
| NousResearch/Hermes-2-Pro-Mistral-7B | Ênfase em respostas longas e estruturadas |
| meta-llama/Llama-3.2-3B-Instruct | Avaliação de modelos compactos |
| HuggingFaceH4/zephyr-7b-beta | Clareza e alinhamento instrucional |
| deepseek-ai/deepseek-coder-6.7b-instruct | Especializado em código e engenharia de software |
| microsoft/Phi-3.5-mini-instruct | Modelo leve e otimizado |
| Qwen/Qwen2.5-7B-Instruct | Uso explícito de métricas quantitativas |

---

## 📊 Principais Resultados

### Convergência Observada
Todos os modelos identificaram:

- **Modelo de Fluxo de Trabalho:** GitHub Flow  
- **Estratégia de Release:** Continuous Delivery  

### Evidências Utilizadas
- Presença de uma única branch principal (`main`)
- Uso de branches de feature de curta duração
- Integração frequente via merges
- Releases frequentes sem ciclos temporais rígidos
- Ausência de versões LTS ou release trains

### Síntese Comparativa

| Modelo | Workflow | Estratégia de Release | Observações |
|------|---------|----------------------|------------|
| Mistral-7B | GitHub Flow | Continuous Delivery | Análise equilibrada |
| Zephyr-7B | GitHub Flow | Continuous Delivery | Ênfase em simplicidade |
| Llama-3.2-3B | GitHub Flow | Continuous Delivery | Coerência mesmo com menor porte |
| Qwen-2.5-7B | GitHub Flow | Continuous Delivery | Uso explícito de métricas |
| Hermes-2-Pro | GitHub Flow | Continuous Delivery | Análise detalhada |
| DeepSeek-Coder | GitHub Flow | Continuous Delivery | Foco estrutural |
| Phi-3.5-mini | GitHub Flow | Continuous Delivery | Bom custo-benefício |

---

## 🎯 Conclusão

Os resultados demonstram que **modelos de linguagem podem ser utilizados como ferramentas eficazes de apoio à análise de governança de software**, desde que:

- Baseados exclusivamente em dados técnicos reais
- Utilizados com prompts estruturados
- Interpretados de forma crítica por analistas humanos

A forte convergência dos resultados reforça a **consistência metodológica** da abordagem e indica que o projeto LangExtract apresenta um **nível adequado de maturidade de governança**, caracterizado por integração contínua e entregas frequentes.

---


---


