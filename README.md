# Parte 1
---

## 🧪 Exercício 1 — Classificação Multiclasse (Wine)
- **Camadas:** 2 ocultas (32 neurônios, ReLU)
- **Saída:** 3 neurônios (Softmax)
- **Loss:** `categorical_crossentropy`
- **Otimizador:** `Adam`

### 📊 Resultados
| Modelo | Acurácia | Observações |
|--------|-----------|--------------|
| Rede Neural (Keras) | 0.97 | Aprendizado estável após 20 épocas |
| RandomForest | 0.99 | Melhor desempenho geral e menor tempo de treino |

**Conclusão:** Modelos baseados em árvore ainda são mais eficazes em dados tabulares pequenos.

---

## 🏠 Exercício 2 — Regressão (California Housing)
- **Camadas:** 3 ocultas (64, 32, 16 neurônios – ReLU)
- **Saída:** 1 neurônio (Linear)
- **Loss:** `mse`
- **Otimizador:** `Adam`

### 📈 Resultados
| Modelo | RMSE | MAE | Observações |
|--------|------|-----|--------------|
| Rede Neural (Keras) | 0.58 | 0.45 | Boa generalização após normalização |
| RandomForest | 0.47 | 0.36 | Melhora o erro em ~15% |

**Conclusão:** Para dados estruturados/tabulares, RandomForest continua mais eficiente, mas a rede neural é competitiva com bom ajuste e normalização.

---

## ⚙️ Como Executar
1. Abrir os notebooks no **Google Colab**.
2. Rodar todas as células (os datasets são baixados automaticamente).
3. Conferir gráficos e métricas no final de cada notebook.

---

## 👩‍💻 Tecnologias Utilizadas
- Python 3.10+
- TensorFlow / Keras
- Scikit-learn
- Matplotlib / Seaborn

---

# Parte 2

## 🎯 Objetivo do Projeto

O objetivo deste projeto é treinar e comparar duas abordagens de visão computacional aplicadas à detecção e rastreamento de objetos:

O modelo YOLOv8, utilizado para detecção de veículos (carros e motos) em imagens estáticas, com base em um dataset customizado.

O modelo MediaPipe, utilizado para rastreamento em tempo real de estruturas corporais humanas, como mãos, rosto e corpo.

O projeto busca demonstrar como diferentes arquiteturas de visão computacional podem ser aplicadas em cenários de IoT e Inteligência Artificial embarcada, analisando desempenho, aplicabilidade e precisão.

## ⚙️ Ferramentas Utilizadas
Ferramenta	Finalidade
YOLOv8 (Ultralytics)	Treinamento e inferência de detecção de veículos (carros e motos).
MediaPipe (Google)	Rastreamento em tempo real de mãos, rosto e corpo humano.
Roboflow	Criação, anotação e exportação do dataset customizado (formato YOLOv8).
Google Colab (GPU)	Ambiente para treino e testes do modelo YOLOv8.
Python + OpenCV	Manipulação e visualização de imagens.
## 🧾 Dataset

Nome: Vehicle Detection Dataset – Cars and Motorcycles

Origem: Criado e rotulado no Roboflow

Formato: YOLOv8 (Train / Valid / Test)

Classes: carro e moto

Quantidade de imagens: 80 (60 treino, 10 validação, 10 teste)

Link público: https://app.roboflow.com/iot-c1gfq/cp-iot-vyhqw/models

## 🔧 Hiperparâmetros e Configurações Principais (YOLOv8)
Parâmetro	Valor
Modelo base	yolov8n.pt
Épocas de treino	50
Tamanho da imagem	640x640
Batch size	16
Taxa de aprendizado	Automática (Adam)
Confiança mínima (inferência)	0.25
Dataset path	/content/Cp-IoT-1/data.yaml
## 📈 Resultados – YOLOv8
Métrica	Valor
Precision	0.86
Recall	0.55
mAP@50	0.82
mAP@50-95	0.27

📊 O modelo YOLOv8 apresentou resultados satisfatórios, com precisão elevada e recall moderado, demonstrando boa capacidade de detectar veículos mesmo com um dataset pequeno.

## ⚖️ Comparativo entre as Duas Abordagens
| Critério          | YOLOv8                                                  | MediaPipe                                      |
| ----------------- | ------------------------------------------------------- | ---------------------------------------------- |
| Tipo de modelo    | Detecção supervisionada (Deep Learning)                 | Rastreamento não supervisionado (pré-treinado) |
| Necessita dataset | ✅ Sim                                                   | ❌ Não                                          |
| Tempo de execução | Médio (GPU recomendada)                                 | Instantâneo (CPU suficiente)                   |
| Aplicação ideal   | Detecção de objetos físicos (carros, motos, EPIs, etc.) | Reconhecimento humano, gestos e interação      |
| Facilidade de uso | Média (requer treino)                                   | Alta (sem necessidade de treino)               |
| Precisão          | Alta (dependente da base)                               | Alta em rastreamento de mãos/rosto             |
| Uso em IoT        | Ideal para câmeras fixas e análise de vídeo             | Ideal para sensores de movimento e AR/VR       |

## 💡 Observações e Análise de Desempenho

O modelo YOLOv8 mostrou-se mais adequado para detecção de objetos físicos com boa separação visual (como veículos).

O MediaPipe foi mais eficiente em tempo real, mas limitado a objetos humanos ou anatômicos.

A precisão do YOLOv8 pode ser melhorada com mais dados rotulados e aumento de epochs.

Em contextos de IoT, ambos os modelos podem ser combinados para criar sistemas híbridos de análise inteligente de vídeo.

## 🎥 Vídeo de Demonstração

📺 Assista à demonstração no YouTube: 

https://youtu.be/WRPY1VLblJE

## 👤 Autores
- Henrique Maciel — RM556480
- Gabriela Moguinho Gonçalves — RM556143
- Marina Christina Fernandes Rodrigues — RM554773
