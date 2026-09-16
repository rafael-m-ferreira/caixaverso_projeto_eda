# **Projeto Análise Exploratória e Estatística de Dados**

## Descrição do Projeto

* **Papel:** Analista de dados prestando consultoria para uma loja de varejo.
* **Objetivo:** Fornecer insights práticos para a equipe de marketing combinando **Estatística Descritiva** (resumo e caracterização) e **Estatística Inferencial** (testes de hipótese e qualificação de incerteza).
* **Base de Dados:** Registros diários com preço, quantidade, desconto, valor total, categorias, data, idade e renda de clientes.

## 📂 Estrutura do Repositório

```
caixaverso_projeto_eda/
├── README.md                                         <- Apresentação executiva, documentação e conclusões.
├── notebooks/
│   └── eda.ipynb                                     <- Análises exploratórias em Jupyter Notebook.
├── data/
│   ├── raw/                                          <- Arquivos de dados brutos.
│   │    └── vendas_supermercado_com_cliente.csv      
│   └── processed/                                    <- Arquivos de dados processados.
├── reports/                                          <- Relatórios e arquivos gráficos.
├── venv/                                             <- Ambiente virtual do projeto.
├── .gitignore                                        <- Arquivos que serão ignorados pelo git.
└── .requirement.txt                                  <- Arquivo contendo as bibliotecas do projeto.
```

## ⚙️ Como Reproduzir este Projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/rafael-m-ferreira/caixaverso_projeto_eda.git
   cd caixaverso_projeto_eda
   ```
2. Crie e ative um ambiente virtual (opcional, mas recomendado):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   ou venv\Scripts\activate no Windows
   ```

3. Instale as dependências: `pip install -r requirements.txt`
