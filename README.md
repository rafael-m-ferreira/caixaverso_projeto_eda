# 🛒 Análise Exploratória e Estatística de Vendas no Varejo

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-1.5+-150458?style=for-the-badge&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-1.9+-8CA1AF?style=for-the-badge&logo=scipy&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-3776AB?style=for-the-badge)

## 📌 Visão Geral do Projeto

Este projeto consiste em uma **Análise Exploratória de Dados (EDA)** detalhada combinada com **Testes de Hipóteses (Testes A/B e Testes Paramétricos/Não-Paramétricos)** aplicados à base de dados de vendas de uma rede de supermercados.

O objetivo principal é traduzir métricas estatísticas e padrões de consumo em **diretrizes estratégicas acionáveis para a equipe de Marketing e Gestão Comercial**, respondendo a **14 perguntas chave de negócio**.

**Base de Dados:** Registros diários com preço, quantidade, desconto, valor total, categorias, data, idade e renda de clientes.

---

## 🎯 As 14 Perguntas de Negócio Mapeadas

1. **Picos por Categoria:** Quais categorias geram maior faturamento e em quais meses atingem seu ápice?
2. **Impacto de Descontos:** Quais produtos possuem maior sensibilidade de volume de vendas quando ofertados com desconto?
3. **Média Diária por Categoria:** Qual a receita diária esperada por segmento de produto?
4. **Sazonalidade (CV):** Quais produtos apresentam maior variação de demanda ao longo do ano?
5. **Representatividade Demográfica:** Como o faturamento se distribui entre as diferentes faixas etárias?
6. **Padrão Semanal:** Qual o comportamento das vendas ao longo dos dias da semana?
7. **Aquecimento para Black Friday:** Como Outubro (pré-Black Friday) se compara a Novembro?
8. **Ticket Médio x Demografia:** Qual a distribuição do ticket médio por categoria e faixa etária?
9. **Idade x Ticket de Compra:** Existe correlação entre a idade do cliente e o valor total gasto por transação?
10. **Black Friday vs. Natal:** Qual das duas maiores datas do varejo gera maior volume de vendas diárias?
11. **Validação das Promoções (Teste U Mann-Whitney):** A concessão de descontos gera um ganho estatisticamente significante nas vendas?
12. **Incerteza e IC 95% (Black Friday vs. Natal):** Qual o intervalo de confiança do faturamento diário médio nestes dois eventos?
13. **Precisão da Estimativa do Ticket Médio:** Qual o intervalo de confiança de 95% do ticket médio geral e por perfil demográfico?
14. **Efeito Mês Black Friday (Teste t):** O mês de Novembro como um todo é superior ao mês de Outubro estatisticamente?

---

## 🔬 Metodologia Estatística Aplicada

Para garantir que os *insights* de negócio não fossem baseados em flutuações aleatórias, a análise seguiu um rigoroso fluxo de validação científica:

* **Tratamento & Engenharia de Atributos:** Criação de variáveis temporais (`Mes`, `Dia_Semana`, `Data`), categorias demográficas (`Faixa_Etaria`) e flags promocionais (`Com_Desconto`).
* **Verificação de Premissas:**
  * **Teste de Shapiro-Wilk:** Para checagem de Normalidade da distribuição dos dados de vendas.
  * **Teste de Levene:** Para validação da Homocedasticidade (igualdade de variâncias).
* **Testes de Hipótese:**
  * **Teste U de Mann-Whitney:** Utilizado para validar o impacto promocional em distribuições não normais.
  * **Teste $t$ de Student / Welch:** Aplicado na comparação do desempenho diário entre meses e semanas festivas.
  * **Intervalos de Confiança (95%):** Cálculo de margem de erro e amplitude para estimativa precisa do ticket médio e faturamento esperado.

---

## 📊 Principais Descobertas & Insights de Negócio

1. **Eficiência Provada dos Descontos ($p < 0,05$):** As vendas sob ação promocional têm impacto positivo e estatisticamente significante na receita total, comprovando que a estratégia de descontos não erosiona a margem sem retorno.
2. **Natal > Black Friday:** A semana do Natal apresentou uma **média de vendas diárias ~12,7% superior** à semana da Black Friday. A Black Friday atua fortemente em volume e atração, enquanto o Natal concentra compras de maior valor unitário.
3. **Perfil Sustentador (36–59 anos):** A faixa etária de Adultos responde por **42,58% de todo o faturamento da rede**.
4. **Ausência de Correlação Idade x Valor ($r = 0,0077$):** Clientes de todas as idades têm potencial de gasto similar; a diferença está nas *categorias selecionadas*, e não no limite do ticket.
5. **Concentração no Domingo:** O domingo registra o maior faturamento da semana, enquanto terças e quartas-feiras demandam ações de ativação para equilibrar o fluxo.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3.9+
* **Manipulação de Dados:** `pandas`, `numpy`
* **Análise Estatística:** `scipy.stats`
* **Visualização de Dados:** `matplotlib`, `seaborn`

---

## 📂 Estrutura do Repositório

```
caixaverso_projeto_eda/
├── README.md                                         # Documentação e resumo geral do projeto
├── notebooks/
│   └── eda.ipynb                                     # Notebook com o código Python, gráficos e testes de hipótese
├── data/
│   ├── raw/                                          # Arquivo de dados brutos
│   │    └── vendas_supermercado_com_cliente.csv      
│   └── processed/                                    
├── reports/                                          # Relatório Executivo e arquivos gráficos
│   └── relatorio_executivo.md               
├── venv/                                             
├── .gitignore                                        
└── .requirement.txt                                  
```

---

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
