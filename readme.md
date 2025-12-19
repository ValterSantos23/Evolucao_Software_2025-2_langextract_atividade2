# Análise de Governança de Software com Modelos de Linguagem  
## Estudo de Caso: Projeto LangExtract

Este repositório contém os artefatos e códigos desenvolvidos para a **Atividade 2 – Gerência de Configuração**, da disciplina **Engenharia de Software II**, com foco na análise de governança em projetos open source utilizando modelos de linguagem de grande porte (LLMs).

---

## 🎯 Objetivo

Analisar a governança do projeto open source **LangExtract** (Google), identificando:

- O **modelo de fluxo de trabalho** (branching model)
- A **estratégia de releases**
- A **convergência de resultados** entre diferentes modelos de linguagem

A análise é baseada exclusivamente em **dados técnicos reais** extraídos do repositório Git do projeto.

---
## 🔗 Links Importantes

- Repositório do LangExtract:  
  https://github.com/google/langextract

- Repositório da Atividade:  
  https://github.com/ValterSantos23/Evolucao_Software_2025-2_langextract_atividade2

- Vídeo tutorial:  
  https://www.youtube.com/watch?v=YYo4CtIqv24
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

## ⚙️ Configuração de Hardware Utilizada

Os experimentos foram executados no ambiente **Google Colab**, utilizando a infraestrutura padrão disponibilizada gratuitamente pela plataforma.

### Hardware

- **GPU:** NVIDIA Tesla T4  
- **Memória da GPU:** 16 GB  
- **Memória RAM:** aproximadamente 12 GB  
- **Processador:** Intel Xeon (arquitetura x86_64, virtualizado)  
- **Armazenamento:** Ambiente temporário do Google Colab  

### Justificativa da Configuração

A GPU NVIDIA Tesla T4 foi utilizada por oferecer suporte adequado à execução de modelos de linguagem de médio porte (entre 3B e 7B parâmetros), permitindo inferência eficiente em precisão reduzida (`float16`) sem comprometer a qualidade das respostas.

---

## 🧰 Dependências de Software

- Python 3.10+
- Bibliotecas principais:
  - `torch`
  - `transformers`
  - `accelerate`
  - `git`

---

## ▶️ Como Executar o Código

### Passo 1 — Abrir o ambiente

1. Acesse o **Google Colab**:  
   https://colab.research.google.com
2. Faça upload do notebook localizado em `codigo/analise_langextract.ipynb`
3. Ative a GPU:
   - Menu **Ambiente de execução**
   - **Alterar tipo de ambiente de execução**
   - Selecione **GPU**

---

### Passo 2 — Instalar dependências

Execute a célula inicial do notebook:

```bash
!pip install -q -U transformers accelerate torch

