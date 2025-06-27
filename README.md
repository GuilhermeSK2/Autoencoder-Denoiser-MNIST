# Autoencoder Denoising de Imagens MNIST

Este projeto implementa um Autoencoder Denoising utilizando a biblioteca Keras para remover ruído de imagens de dígitos manuscritos. O modelo é treinado no dataset MNIST, onde imagens originais são corrompidas com ruído aleatório e, em seguida, o autoencoder aprende a reconstruir as imagens limpas a partir das versões ruidosas.

## Visão Geral

Autoencoders são redes neurais não supervisionadas que aprendem uma representação codificada (ou latente) dos dados de entrada. Um *denoising autoencoder* é uma variação onde o modelo é treinado para reconstruir uma entrada limpa a partir de uma versão corrompida dessa mesma entrada. Isso os torna eficazes para tarefas de remoção de ruído.

Neste projeto, as imagens do dataset MNIST são:
1.  Normalizadas para um intervalo de 0 a 1.
2.  Achadas (flattened) de 2D (28x28 pixels) para 1D (784 pixels).
3.  Adicionado ruído gaussiano às imagens de treinamento e teste.
4.  Um autoencoder simples com uma camada oculta é construído e treinado para reconstruir as imagens originais a partir das imagens ruidosas.

## Estrutura do Projeto

* `Autoencoders.ipynb`: O notebook Jupyter que contém todo o código para carregamento, pré-processamento, construção, treinamento e avaliação do autoencoder denoiser.

## Tecnologias Utilizadas

* **Python 3**
* **TensorFlow/Keras**: Para a construção e treinamento da rede neural.
* **NumPy**: Para manipulação de arrays e geração de ruído.
* **Matplotlib**: Para visualização das imagens originais, ruidosas e denoised.

## Resumo

O notebook inclui código para exibir três imagens lado a lado para um exemplo aleatório do conjunto de testes:
1.  A imagem original.
2.  A imagem com ruído adicionado.
3.  A imagem reconstruída pelo autoencoder (com ruído removido).

Isso permite uma comparação visual direta do desempenho do modelo na tarefa de denoising.

![Image](https://github.com/user-attachments/assets/9cc6e173-d091-424a-b4b0-185dabc617ec)
