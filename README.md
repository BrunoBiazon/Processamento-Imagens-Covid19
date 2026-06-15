# COVID-19 Raio-x | ResNet50 🫁

Este projeto implementa um classificador automático de radiografias de tórax para o diagnóstico binário de COVID-19 (Normal vs. Covid). Desenvolvido como projeto de conclusão para a disciplina AS65F - Processamento de Imagens.

## 🚀 Tecnologias e Arquitetura
* **Linguagem:** Python 3
* **Bibliotecas: TensorFlow, Keras, NumPy, Scikit-Learn, Matplotlib, Seaborn
* **Arquitetura Base:** ResNet50 (ImageNet)
* **Ambiente:** Google Colab 

## Estratégias
1. **Extração de Características:** Utilizamos a arquitetura **ResNet50** com (`include_top=False`) e com os pesos congelados. Isso permite aproveitar a capacidade da rede de identificar formas complexas.
2. **Topologia Customizada:** Adição de uma nova "cabeça" de classificação contendo `GlobalAveragePooling2D`, uma camada Densa intermediária (64 neurônios com ativação ReLU), e uma saída Sigmoide. Proporcionando um Fine-Tuning direcionado para o nosso tema.
3. **Controle de Otimização:** Ajuste fino de hiperparâmetros, travando a taxa de aprendizado do otimizador Adam em `0.001` para estabilidade térmica dos gradientes.

## 📈 Resultados 
<img width="522" height="599" alt="image" src="https://github.com/user-attachments/assets/065f3f9b-aa8c-43cf-b381-d6f184831323" />


* **Acurácia:** 100% (1.00)
* **Precisão:** 100% (1.00)
* **Recall:** 100% (1.00)
* **F1-Score:** 100% (1.00)

## Dataset:
https://drive.google.com/drive/folders/1j36FvJGBQjEOhhYOFpWv-9736N-N9Q6o?hl=pt-br
## 🛠️ Como Executar
1. Clone este repositório.
2. Abra o arquivo `Projeto_Covid.ipynb` no Google Colab.
3. Conecte sua conta do Google Drive contendo o DataSet disponibilizado.
4. Ajuste as variáveis `caminho_treino` e `caminho_teste` apontando para os seus diretórios locais.
  ``` drive.mount('/content/drive'   )
   caminho_treino = '/content/drive/MyDrive/Projeto_Covid19/covid19/train'
   caminho_teste ='/content/drive/MyDrive/Projeto_Covid19/covid19/test' 
   ``` 
5. Execute a célula.
