# Clonar ou baixar o repositório
- git clone https://github.com/seuusuario/monitoramento-ar-iot.git
- cd monitoramento-ar-iot

# Abrir o notebook
- jupyter notebook monitoramento_qualidade_ar_iot_V01.ipynb

- Executar a simulação
  - Ajuste os slides de temperatura, umidade e CO₂.
  - Clique em Tempo + para avançar uma hora (12 amostras geradas).
  - Observe os gráficos e alertas automáticos.
  - Treinar o modelo de IA
    - O notebook já inclui a etapa de treinamento com Random Forest.
    - Verifique o relatório de classificação e a matriz de confusão.
  - Exportar dados
    - Clique em Baixar CSV para salvar todas as amostras coletadas.
    - O arquivo incluirá estatísticas gerais da simulação.

# Código no kaggle
- https://www.kaggle.com/code/fabiojuniordossantos/monitoramento-qualidade-ar-iot

# Monitoramento da Qualidade do Ar com IA (Dados Simulados de IoT)

Projeto desenvolvido na disciplina **Internet das Coisas e Aplicações de IA (Big Data)** da **Universidade do Vale do Rio dos Sinos - UNISINOS**.

Professores:  
- Cristiano André da Costa  
- Rodrigo da Costa Righi  

Autores:  
- Fabio Junior dos Santos  
- Filipe Torres da Rosa  
- Paulo Cesar Ortiz de Freitas  

---

## Resumo

Este projeto apresenta uma solução de **Monitoramento da Qualidade do Ar** baseada na integração de **IoT, Big Data e Inteligência Artificial**, utilizando dados simulados de sensores ambientais (temperatura, umidade e CO₂).  

A arquitetura implementada contempla:
- Simulação de sensores
- Coleta e processamento de dados
- Classificação por regras e por modelo de IA (Random Forest)
- Interface interativa com alertas automáticos
- Exportação de dados para análise externa

---

## Objetivos

- Monitorar em tempo real a qualidade do ar.  
- Prever a qualidade do ar em curto prazo.  
- Detectar anomalias e gerar alertas persistentes.  
- Apoiar decisões individuais (casas inteligentes) e coletivas (políticas públicas).  

---

## Arquitetura

### Arquitetura implementada (simulação):
- [Sensores IoT simulados] → [Gateway/Edge] → [Plataforma Big Data] → [Modelos de IA] → [Dashboard/API]


### Arquitetura sugerida (aplicação real):
- ESP32 / Raspberry Pi  
- Sensores PMS5003, SDS011, Plantower, BME680, MQ-135  
- Backend: AWS IoT Core / Azure IoT Hub  
- Armazenamento: PostgreSQL  
- Visualização: Grafana  
- Processamento/IA: Python, Scikit-learn, XGBoost, TensorFlow  

---

## ⚙️ Tecnologias Utilizadas

- **IoT (simulado):** sensores de temperatura, umidade e CO₂  
- **Big Data:** Pandas, NumPy  
- **IA:** Scikit-learn (RandomForestClassifier)  
- **Visualização:** Matplotlib, Seaborn  
- **Interatividade:** ipywidgets  
- **Exportação:** CSV  

---

## 📌 Metodologia

1. Simulação de sensores com ocupação variável e ruídos realistas  
2. Classificação por regras (faixas de CO₂)  
3. Treinamento de IA com Random Forest  
4. Interface interativa para simulação  
5. Alertas automáticos com recomendações práticas  
6. Exportação de dados para análise externa  
7. Integração via API REST  

---

## 🚀 Implementação

- Cada hora avançada gera 12 amostras de sensores  
- 720 registros simulados usados para treinar o modelo  
- Comparação entre classificação por regras e IA  
- Interface com sliders e gráficos em tempo real  
- Alertas automáticos (CO₂, temperatura, umidade)  
- Exportação de dados em CSV com estatísticas gerais  

---

## 📊 Resultados Práticos

- **Distribuição das classes:**  
  - Excelente: 391 registros  
  - Bom: 129 registros  
  - Ruim: 191 registros  
  - Péssimo: 9 registros  

- **Desempenho do modelo de IA:**  
  - Acurácia: 86%  
  - Excelente: precisão e recall de 100%  
  - Ruim: recall de 90%  
  - Bom: precisão 74%, recall 44%  
  - Péssimo: baixa precisão (poucos exemplos)  

---

## 🔍 Insights da IA

- Ambientes ocupados apresentaram aumento significativo de CO₂  
- Horários de maior ocupação coincidiram com picos de CO₂  
- Temperatura e umidade influenciaram indiretamente os níveis de CO₂  
- Relatórios semanais/mensais podem apoiar políticas públicas  
- O modelo pode ser adaptado para diferentes contextos  

---

## ✅ Validação da Solução

- Robustez frente a ruídos e dados incompletos  
- Integração IoT + Big Data + IA eficaz para monitoramento e previsão  
- Recomendações práticas acionadas corretamente  
- Escalabilidade para residências, escritórios, escolas e cidades inteligentes  

---

## 📝 Conclusão

O projeto comprova que a sinergia entre **IoT, Big Data e IA** é capaz de transformar dados brutos em informações úteis e acionáveis, apoiando tanto decisões individuais (casas inteligentes) quanto estratégias coletivas (políticas públicas).  

Mais do que um protótipo técnico, esta solução representa um caminho para ambientes mais saudáveis, sustentáveis e inteligentes, alinhando tecnologia com bem-estar e qualidade de vida.  

---

## 🔑 Palavras-chave

- Internet das Coisas (IoT)  
- Big Data  
- Inteligência Artificial (IA)  
- Qualidade do Ar  
- Monitoramento em Tempo Real  
- Sustentabilidade  
- Smart Homes  
- Cidades Inteligentes  

---

## ▶️ Instruções de Execução

### Pré-requisitos
- Python 3.10+  
- Jupyter Notebook ou Google Colab  
- Bibliotecas:  
  ```bash
  pip install numpy pandas matplotlib seaborn scikit-learn ipywidgets
