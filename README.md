# Classificador de Números MNIST

**Dependências:**
- Python 3.9  
  - Matplotlib  
  - NumPy  
- Jupyter  
- Keras 3.0  



### O que acontece:

1. Carrega o dataset **MNIST** com imagens de dígitos manuscritos.  
2. Divide em treino e teste.  
3. Normaliza os pixels, para o modelo ser treinado mais rápido e com mais estabilidade.  
4. Constrói o modelo:  
   - **Flatten** transforma cada imagem 28×28 em um vetor de 784 valores.  
   - **Dense(128, relu)** cria a camada com 128 neurônios que aprendem padrões.  
   - **Dense(10, softmax)** gera as probabilidades para cada dígito de 0 a 9.  
5. Compila o modelo com:  
   - Otimizador **Adam** para ajustar os pesos de forma eficiente.  
   - Função de perda **sparse categorical crossentropy** para medir o erro.  
   - Métrica de **acurácia** para acompanhar o desempenho.  
6. Treina o modelo, passando os dados 5 vezes.  
7. Avalia no conjunto de teste com **evaluate**, mostrando o erro e a acurácia final.  
8. Imprime a acurácia obtida nos dados de teste.  

Na **Célula 2**, os dados separados para *test* são passados para ver a previsão do modelo.