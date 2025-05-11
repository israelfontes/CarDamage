# Sistema de Análise de Danos em Veículos

Este repositório contém uma implementação de um sistema de visão computacional para segmentação de peças de veículos e classificação de avarias. O projeto utiliza técnicas de deep learning para identificar componentes de veículos em imagens e classificar o nível de dano presente em cada peça.

## 📋 Visão Geral

O sistema funciona em duas etapas principais:
1. **Segmentação de Peças**: Utilizando YOLOv11 para detectar e segmentar 21 componentes diferentes do veículo
2. **Classificação de Avarias**: Usando ResNet-50 para classificar o nível de dano em cada peça (focado em portas)

O resultado final é um mini-relatório que mostra visualmente as peças identificadas e seus respectivos níveis de avaria.

## 🗂️ Estrutura do Repositório

- **dataset/**: Contém os dados para treinamento e teste dos modelos
- **yolo_segmentation.ipynb**: Notebook para treinamento do modelo YOLOv11 de segmentação
- **resnet_classification.ipynb**: Notebook para treinamento do modelo ResNet de classificação de avarias
- **predict.ipynb**: Notebook para execução do pipeline completo e geração de relatório

## 🔧 Instalação e Requisitos

### Requisitos

- Python 3.8+
- PyTorch 1.10+
- Ultralytics (para YOLOv11)
- OpenCV
- NumPy
- Matplotlib
- Pandas

### Instalação

```bash
# Clone o repositório
git clone https://github.com/israelfontes/CarDamage.git
cd CarDamage

# Instale as dependências
pip install -r requirements.txt
```

## 🚀 Como Usar

### Treinamento dos Modelos

1. **Treinamento do YOLOv11**:
   - Abra `yolo_segmentation.ipynb` no Jupyter ou Google Colab
   - Configure o caminho para o dataset
   - Execute todas as células para treinar o modelo de segmentação

2. **Treinamento do ResNet**:
   - Abra `resnet_classification.ipynb` no Jupyter ou Google Colab
   - Configure o caminho para o dataset de imagens de portas com diferentes níveis de avaria
   - Execute todas as células para treinar o classificador

### Predição e Geração de Relatórios

- Abra `predict.ipynb` no Jupyter ou Google Colab
- Configure os caminhos para os modelos treinados
- Carregue uma imagem de veículo para análise
- Execute o notebook para obter o relatório de danos

## 📊 Resultados

- O modelo YOLOv11 alcança um mAP@0.5 de 0.91 na segmentação das peças do veículo
- O classificador ResNet atinge uma acurácia de 79.59% na identificação dos níveis de avaria em portas
- O sistema consegue classificar avarias em quatro categorias:
  - No Damage (Sem avarias)
  - Light Damage (Avarias leves)
  - Moderate Damage (Avarias moderadas)
  - Severe Damage (Avarias graves)

## 📝 Limitações e Trabalhos Futuros

- A classificação de avarias está atualmente implementada apenas para portas
- Como trabalho futuro, pretende-se expandir a classificação para outros componentes
- Explorar técnicas de aprendizado semi-supervisionado para reduzir a necessidade de rotulagem manual

## 🎓 Contexto Acadêmico

Este projeto foi desenvolvido como trabalho final para a disciplina de Visão Computacional do Programa de Pós-Graduação em Tecnologia da Informação, sob orientação do Prof. Helton Maia (2025.1).


## 👤 Autores

- [Israel Medeiros Fontes](https://github.com/israelfontes)

---

⭐️ Se este projeto foi útil para você, considere deixar uma estrela!