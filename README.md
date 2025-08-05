# 📈 Predição da Direção do IBOVESPA - Tech Challenge Fase 2

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)
[![Accuracy](https://img.shields.io/badge/Accuracy-76.7%25-brightgreen.svg)]()
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 🎯 Objetivo

Desenvolvimento de modelo de machine learning para predição da direção do índice IBOVESPA com **acurácia superior a 75%**, utilizando análise de séries temporais e feature engineering avançado.

## 🏆 Resultados Alcançados

- ✅ **Acurácia: 76.7%** (Meta de 75% superada)
- 🛡️ **Proteção Patrimonial: 94.7%** de acerto em quedas
- 📊 **AUC: 0.665** - Capacidade discriminatória superior
- 🎯 **F1-Score: 0.667** - Performance equilibrada

## 🔬 Metodologia

### Modelos Implementados
- **Random Forest**: Baseline com 60% de acurácia
- **XGBoost**: Modelo final otimizado com 76.7% de acurácia

### Feature Engineering
- Retornos multi-período (3, 5, 7, 14, 21 dias)
- Indicadores técnicos (RSI, MACD, Médias Móveis)
- Regimes de volatilidade
- Features de volume e momentum

### Validação
- **TimeSeriesSplit**: Validação temporal sem data leakage
- **30 dias de teste**: Período out-of-sample
- **Grid/RandomizedSearchCV**: Otimização de hiperparâmetros

## 🚀 Como Executar

### Pré-requisitos
- Python 3.8+
- Jupyter Notebook
- 8GB RAM recomendado

### Instalação
```bash
# 1. Clonar repositório
git clone https://github.com/seu-usuario/tech-challenge-ibovespa-prediction.git
cd tech-challenge-ibovespa-prediction

# 2. Criar ambiente virtual
python -m venv venv
source venv/bin/activate  # Linux/Mac
# ou
venv\Scripts\activate     # Windows

# 3. Instalar dependências
pip install -r requirements.txt

# 4. Executar notebook
jupyter notebook notebooks/Tech_Challenge_Final.ipynb
```

## 📊 Estrutura dos Dados

```
Dados Históricos do IBOVESPA (4 anos)
├── Período: 2020-2024
├── Frequência: Diária
├── Features: Abertura, Fechamento, Máxima, Mínima, Volume
└── Target: Direção do movimento (Alta/Baixa)
```

## 📈 Principais Visualizações

### Performance Comparativa

| Modelo | Acurácia | F1-Score | AUC | Característica |
|--------|----------|----------|-----|----------------|
| Random Forest | 70.0% | 0.621 | 0.469 | Baseline conservador |
| **XGBoost** | **76.7%** | **0.667** | **0.665** | **Modelo final otimizado** |

### Features Mais Importantes
1. **Volatilidade 10 dias**: Principal driver de decisão
2. **Momentum 21 dias**: Tendência de longo prazo
3. **RSI suavizado**: Análise técnica refinada
4. **Posição vs MA50**: Contexto de tendência

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **pandas & numpy**: Manipulação de dados
- **scikit-learn**: Machine learning
- **XGBoost**: Gradient boosting
- **matplotlib & seaborn**: Visualizações
- **ta**: Análise técnica

## 📁 Estrutura do Projeto

```
├── README.md               # Documentação principal
├── requirements.txt        # Dependências Python
├── .gitignore             # Arquivos a ignorar
├── LICENSE                # Licença do projeto
├── data/                  # Dados 
