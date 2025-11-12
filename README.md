Projeto de Deep Learning: Transfer Learning com 2 Classes
Este projeto é um classificador de imagens que utiliza Deep Learning para distinguir entre duas categorias. Foi desenvolvido em Python, com TensorFlow e Keras, e executado no ambiente Google Colab.

Objetivo
O objetivo principal é aplicar a técnica de Transfer Learning (Aprendizagem por Transferência) para treinar um classificador de imagens eficiente. Usei o modelo MobileNetV2 como base para adaptá-lo a um problema de classificação binária.

Dataset
O conjunto de dados (dataset) é composto por imagens de duas classes:

loide: [Fotos Loide]

debi: [Fotos Debi]

Para o correto funcionamento do script, os dados devem seguir a seguinte estrutura de pastas:

dataset/
├── train/
│   ├── loide/
│   └── debi/
└── validation/
    ├── loide/
    └── debi/
    
Metodologia: Transfer Learning
A metodologia utilizada foi o Transfer Learning. Este processo envolve três etapas principais:

Carregar Modelo Base: Utiliza-se a rede MobileNetV2, que já foi pré-treinada na extensa base de dados ImageNet.

Congelar Camadas: As camadas do MobileNetV2 são "congeladas". Seus pesos não são atualizados durante o treinamento inicial, preservando o conhecimento aprendido.

Adicionar Novo Classificador: Uma nova "cabeça" de classificação é adicionada ao final do modelo base. 
Ela é composta por:

GlobalAveragePooling2D

Dense(128, activation='relu')

Dropout(0.2)

Dense(1, activation='sigmoid') (para a saída de classificação binária)

Tecnologias Utilizadas
Google Colab: Ambiente de notebook para execução e treino.

Python 3

TensorFlow / Keras: Para a construção e treino da rede neural.

Matplotlib: Para visualização dos resultados gráficos.

NumPy: Para manipulação de arrays.
