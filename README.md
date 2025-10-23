# 🩺 Análise Preditiva de Custos de Seguro de Saúde

![Linguagem](https://img.shields.io/badge/Linguagem-R-blue.svg)
![Licença](https://img.shields.io/badge/Licença-MIT-green.svg)

Este repositório contém o **trabalho final da disciplina Introdução à Ciência de Dados com R**.
O projeto consiste na construção de um **modelo de regressão linear múltipla** para prever os custos de seguro de saúde com base em características demográficas e de estilo de vida dos segurados.

---

## 📚 Tabela de Conteúdos

- [📖 Contexto do Projeto](#-contexto-do-projeto)
- [🎯 Objetivo](#-objetivo)
- [🗂️ O Dataset](#️-o-dataset)
- [🔎 Metodologia](#-metodologia)
- [📊 Principais Resultados](#-principais-resultados)
- [⚙️ Como Executar o Projeto](#️-como-executar-o-projeto)
- [👨‍💻 Autores](#-autores)

---

## 📖 Contexto do Projeto

Este trabalho foi desenvolvido como avaliação final para a disciplina **Introdução à Ciência de Dados**.
O objetivo foi aplicar de forma prática todas as etapas de um projeto de ciência de dados, desde a coleta e limpeza dos dados até a modelagem estatística, validação e comunicação dos resultados.

---

## 🎯 Objetivo

Identificar e quantificar o impacto de fatores demográficos e de estilo de vida nos custos de seguro de saúde. A análise evoluiu de um modelo de regressão linear geral para uma abordagem segmentada, que modela separadamente os grupos de fumantes e não fumantes para capturar com maior precisão a dinâmica de custos de cada um.

---

## 🗂️ O Dataset

O estudo utilizou o conjunto de dados **"Medical Cost Personal Datasets"**, disponível publicamente no Kaggle.

- **Fonte:** [Kaggle - Medical Cost Personal Datasets](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- **Observações:** 1.338
- **Variáveis principais:**
  - `age`
  - `sex`
  - `bmi`
  - `children`
  - `smoker`
  - `region`
  - `charges` (variável alvo)

---

## 🔎 Metodologia

1. **Análise Exploratória e Pré-processamento:** Investigação inicial das relações entre variáveis e tratamento da assimetria da variável alvo charges com transformação logarítmica.

2. **Modelo Geral Inicial:** Construção de um primeiro modelo de regressão linear múltipla com todos os dados. Este modelo alcançou um R² ajustado de 74,4%, mas a análise de resíduos indicou heterocedasticidade, motivando a segmentação.

3. **Modelagem Segmentada:** Desenvolvimento de dois modelos distintos e mais robustos:

- Um para o subgrupo de não fumantes.

- Um modelo de interação para o subgrupo de fumantes, capturando o efeito combinado dos fatores de risco.

---

## 📊 Principais Resultados

A abordagem segmentada foi crucial para entender a estrutura de custos, revelando dois comportamentos distintos:

**Para Não Fumantes**

Os custos seguem um padrão previsível e moderado, com o modelo explicando **69% da variabilidade (R² ajustado = 0.686)**.

- Principais Preditores: `Idade` (com efeito curvo), `número de filhos` e `região`.

- O IMC não se mostrou um fator de forte impacto isoladamente para este grupo.

**Para Fumantes**

A dinâmica de custos é mais complexa e de maior magnitude. O tabagismo atua como um amplificador de risco.

- O modelo de interação explicou **91,4% da variabilidade dos custos (R² ajustado = 0.914)**.

- **Principal Descoberta:** A combinação de **tabagismo, obesidade (IMC ≥ 30) e idade** eleva os custos de forma exponencial.

---

## ⚙️ Como Executar o Projeto

### 1. Pré-requisitos

- **R** (versão 4.0 ou superior)
- **RStudio**

### 2. Instalação

Clone este repositório para a sua máquina local:

```bash
git clone https://github.com/zbrusco/health_cost_analysis
```

Abra o projeto no **RStudio** clicando em `health_cost_analysis.Rproj`.
Isso irá configurar o diretório de trabalho automaticamente.

---

## 👨‍💻 Autores

Este projeto foi desenvolvido por:

- [Andre Loureiro Montini Ferreira](https://github.com/jfandre00)
- [Lucas Amorim Brusco](https://github.com/zbrusco)
- [Pedro Conceição Costa](https://github.com/dev-pedr0)
- [Marcelo De Azevedo Sampaio](https://github.com/marcelosampaio)
- [Kauan Lima Oliveira](https://github.com/devKauanLima)

---
