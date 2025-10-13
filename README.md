
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

## 👤 Autores
- Henrique Maciel — RM556480
- Gabriela Moguinho Gonçalves — RM556143
- Marina Christina Fernandes Rodrigues — RM554773
