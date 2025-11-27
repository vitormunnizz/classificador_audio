## 📌 Descrição do Projeto

Este projeto investiga estratégias de ampliação e balanceamento de dados para melhorar a detecção de áudios verdadeiros e falsos (DeepFake). O avanço das tecnologias de síntese de voz tem tornado cada vez mais difícil diferenciar áudios autênticos de falsificações. Assim, o trabalho explora como diferentes técnicas de **Data Augmentation** e **balanceamento de classes** influenciam o desempenho de modelos de aprendizado de máquina.

O objetivo principal é avaliar quais combinações de técnicas ajudam os modelos a **generalizar melhor** para diferentes condições, mantendo a qualidade perceptiva e evitando distorções excessivas.

## 📂 Dados

### Origem

Os dados foram organizados em dois diretórios principais:

* `real`: amostras de áudios autênticos
* `fake`: amostras geradas sinteticamente (DeepFake)

### Formato

* Arquivos `.wav` e `.mp3`
* Conjunto original balanceado entre as classes

## 🎛 Técnicas de Ampliação e Balanceamento

O projeto aplica **no máximo uma técnica de aumento por amostra**, limitando a expansão a **até o dobro do conjunto original**.

**Ampliação de Dados (Data Augmentation)**

* **Adição de Ruído**: adição de ruído para simular diferentes condições de gravação.
* **Variação de Velocidade**: acelera ou desacelera a taxa de reprodução, modificando as características temporais.
* **Variação de Tom**: simula variações vocais naturais sem comprometer a inteligibilidade.
* **Equalização Aleatória**: aplica modificações no espectro de frequências para representar diferentes equipamentos ou ambientes.
* **Mascaramento**: oculta regiões temporais ou frequenciais para simular perda parcial de informação.

**Balanceamento de Classes**

* **Random UnderSampling**: redução da classe majoritária.
* **SMOTE**: geração sintética de amostras minoritárias.

## 🤖 Modelos Avaliados

* **Random Forest (RF)**
* **LightGBM (LGBM)**
* **Naive Bayes**
* **Long Short-Term Memory (LSTM)**
* **K-Nearest Neighbors (KNN)**

Todos os modelos foram treinados com **validação cruzada** (80% treino, 20% teste), usando **parâmetros padrão** para isolar o efeito das técnicas de ampliação e balanceamento.

## 📏 Métricas de Avaliação

* **Acurácia**
* **Precisão**
* **Recall**
* **F1-Score**
* **Desvio Padrão** (para avaliar estabilidade entre execuções)## 👨‍💻 Autor

## 👨‍💻 Autor

**Vitor Hugo Muniz de Sousa Santos**

💼 Engenheiro de Computação | Cientista de Dados

📧 [vitormunnizzdev@gmail.com](mailto:vitormunnizzdev@gmail.com)
🌐 [www.linkedin.com/in/vitormunnizz](https://www.linkedin.com/in/vitormunnizz)

## 📝 Licença

Este projeto está licenciado sob a **MIT License**.
Sinta-se livre para usar e modificar conforme necessário, mantendo os créditos ao autor.

⭐ **Se este projeto te ajudou, deixe uma estrela no repositório!**```
