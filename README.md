# neural-miners-cancer-de-mama

Universidade Estadual de Campinas
Trabalho final do curso Mineração de dados Complexos

Grupo Neural Miners - Julho/2023

 - Anderson Tadeu Silva
 - Bárbara Diogo
 - Héber Scachetti
 - Rafaela Moretto
 - Viviane Veiga Colleoni



O projeto de conclusão de curso apresentado pelo grupo Neurominers, da Unicamp, foca na detecção de câncer de mama por meio da classificação de imagens de mamografias. Utilizando dados disponibilizados por uma competição do Kaggle, o desafio consiste em identificar se as imagens possuem indícios de câncer de mama ou não. Para desenvolver um modelo capaz de classificar as imagens, o grupo avaliou diferentes arquiteturas e combinações de algoritmos, além de realizar pré-processamentos de imagens e tratar o desbalanceamento de classes.

Foram utilizadas três tipos de arquiteturas e combinações de algoritmos, incluindo redes pré-treinadas com camadas de transfer learning e classificação. Os modelos testados incluem EfficientNet B0, DenseNet 121, ResNet 50 e ConvNext Large. Para tratar o desbalanceamento, foram adotadas estratégias como entrega de pesos das classes durante a etapa de treino e oversampling através do smooth. 

Diversas técnicas de pré-processamento de imagens também foram aplicadas, como geração de imagens sintéticas, aplicação de filtros e transformações, e uso do algoritmo YOLO v5 para identificar a região de interesse.
Os melhores resultados de acurácia balanceada foram obtidos com a DenseNet 121 descongelada e pré-processamento utilizando YOLO v5, alcançando 62,34% no conjunto de validação e 59,86% no conjunto de teste. 

Apesar dos resultados, os valores ainda são inferiores aos obtidos pelos vencedores da competição do Kaggle. O grupo acredita que o ambiente gratuito do Collab limitou os cenários de teste e que o conhecimento da área é fundamental para um pré-processamento adequado das imagens. Como pontos de melhoria, sugere-se o pré-processamento aplicado a um tamanho de imagem maior, outros métodos de balanceamento e o enriquecimento dos dados com imagens de outros datasets.

# Arquivos:
 - projeto_final_leitura_kaggle.ipynb: notebook do google colab contendo todo o código utilizado no desenvolvimento e avaliação dos modelos;
 -  colab_version_rsna_improved_roi_extraction_yolov5.ipynb: notebook do google colab utilizado para extração da região de interesse;
 - apresentacao.pdf: apresentação do projeto contendo resumo.

 # Informações adicionais:
  - Todas as instruções de execução do código estão presentes no próprio notebook;
  - O notebook do google colab tentará ler os checkpoints, presentes no caminho "/neural-miners-checkpoints/proc-{pré processamento}-target-{tamanho das imagens}/".
