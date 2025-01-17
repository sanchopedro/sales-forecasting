# Previsão de Vendas com Machine Learning e Integração de APIs

## Descrição do Projeto

Este projeto foi desenvolvido para prever vendas utilizando o dataset [Online Shopping Dataset](https://www.kaggle.com/datasets/jacksondivakarr/online-shopping-dataset/data) do Kaggle, complementado com dados de tempo e feriados obtidos em tempo real. O objetivo principal é aplicar técnicas de **machine learning** para criar modelos preditivos de vendas, ajudando a otimizar estoques e melhorar a gestão de inventário.

Principais fontes de dados:
- **Online Shopping Dataset**: Informações detalhadas de compras online.
- **OpenWeatherMap API**: Dados climáticos para enriquecer os modelos preditivos.
- **Holiday API**: Dados de feriados para capturar sazonalidades.

Resultados exibidos em um **dashboard interativo**, facilitando a tomada de decisão baseada em dados.

---

## Estrutura do Projeto

```plaintext
sales-forecasting/
|
├── LICENSE                # Licença do projeto
├── README.md              # Documentação do projeto
├── requirements.txt       # Dependências do projeto
|
├── data/                  # Dados utilizados no projeto
│   ├── raw/               # Dados brutos (dataset do Kaggle, APIs)
│   ├── processed/         # Dados processados e prontos para modelagem
│   └── external/          # Dados externos (tempo, feriados, etc.)
|
├── notebooks/             # Notebooks para exploração e experimentação
│   ├── data_analysis.ipynb        # Análise inicial do dataset
│   ├── api_integration.ipynb      # Integração com APIs
│   ├── feature_engineering.ipynb  # Criação de variáveis
│   └── model_training.ipynb       # Treinamento e avaliação de modelos
|
├── src/                   # Código-fonte principal
│   ├── api/               # Scripts de integração com APIs
│   │   ├── weather_api.py
│   │   └── holiday_api.py
│   ├── preprocessing/     # Scripts de processamento de dados
│   ├── features/          # Engenharia de features
│   ├── models/            # Treinamento e previsão de modelos
│   └── visualization/     # Dashboard e visualizações interativas
|
├── tests/                 # Scripts de teste
|
└── reports/               # Relatórios gerados
    ├── figures/           # Gráficos e imagens
    └── logs/              # Logs de execução
```

---

## Configuração do Ambiente Virtual

Siga os passos abaixo para configurar o ambiente virtual:

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/sanchopedro/sales-forecasting.git
   cd sales-forecasting
   ```

2. **Crie um ambiente virtual**:
   - No Linux/MacOS:
     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```
   - No Windows:
     ```bash
     python -m venv venv
     venv\Scripts\activate
     ```

3. **Instale as dependências**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure as credenciais das APIs**:
   - Crie um arquivo `.env` na raiz do projeto e adicione suas credenciais:
     ```env
     WEATHER_API_KEY=sua_weather_api_key
     HOLIDAY_API_KEY=sua_holiday_api_key
     ```

5. **Teste a configuração**:
   Execute os scripts de teste:
   ```bash
   pytest tests/
   ```

---

## Funcionalidades do Projeto

### **1. Exploração e Análise de Dados**
- Análise do dataset [Online Shopping Dataset](https://www.kaggle.com/datasets/jacksondivakarr/online-shopping-dataset/data):
  - Identificação de padrões de comportamento de compras.
  - Enriquecimento dos dados com clima e feriados.

### **2. Processamento e Engenharia de Features**
- Limpeza e transformação dos dados:
  - Tratamento de valores ausentes.
  - Normalização de colunas relevantes.
- Criação de novas variáveis:
  - Indicadores sazonais (feriados, finais de semana, etc.).
  - Agregações estatísticas (média de vendas, tendências climáticas).

### **3. Modelagem Preditiva**
A decidir

### **4. Visualização e Dashboard**
A decidir

---

## Como Executar o Projeto

1. **Etapa de Extração**:
   - Carregue o dataset do Kaggle:
     ```bash
     python src/preprocessing/load_data.py
     ```
   - Extraia dados das APIs:
     ```bash
     python src/api/weather_api.py
     python src/api/holiday_api.py
     ```

2. **Etapa de Processamento**:
   - Execute o script de processamento e criação de features:
     ```bash
     python src/features/feature_engineering.py
     ```

3. **Etapa de Modelagem**:
   - Treine os modelos:
     ```bash
     python src/models/train_model.py
     ```

4. **Etapa de Visualização**:
   - Inicie o dashboard:
     ```bash
     streamlit run src/visualization/dashboard.py
     ```

---

## Contribuição

Contribuições são bem-vindas! Siga os passos abaixo:
1. Faça um fork do projeto.
2. Crie uma nova branch:
   ```bash
   git checkout -b feature/nova-funcionalidade
   ```
3. Envie suas alterações:
   ```bash
   git push origin feature/nova-funcionalidade
   ```
4. Abra um Pull Request.

---

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

