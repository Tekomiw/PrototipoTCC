Título: Reconhecimento de Imagens de Alimentos – Implementação de algoritmos de Deep Learning para cálculo de calorias e macronutrientes

Descrição geral:
O projeto realiza o reconhecimento de alimentos por meio de Deep Learning, estima a massa da porção utilizando um objeto de referência (moeda) e retorna calorias e macronutrientes com base na tabela TACO. O backend foi desenvolvido em Python utilizando FastAPI e um modelo YOLO treinado, enquanto o aplicativo Android foi desenvolvido em Kotlin. A comunicação ocorre por meio de uma API que envia e recebe dados em JSON.

Tecnologias utilizadas:

Backend (Python):

YOLO (Ultralytics) para detecção dos alimentos

FastAPI para criação da API

PyTorch para treinamento e inferência

OpenCV para manipulação de imagens

NumPy para cálculos numéricos

Aplicativo Android (Kotlin):

Consumo da API

Envio de imagem para análise

Exibição dos resultados nutricionais

Funcionalidades:

Reconhecimento de alimentos da dieta brasileira

Estimativa de volume usando moeda como referência

Cálculo de massa estimada

Retorno de calorias e macronutrientes (proteínas, carboidratos e lipídeos)

Dados nutricionais extraídos da Tabela TACO

Comunicação entre Python (cálculos) e Android (exibição dos dados)

Estrutura do projeto:

Parte Python:
main.py – código principal da API, inferência do YOLO e cálculos
model.pt – modelo YOLO treinado
utils/ – funções auxiliares

Parte Kotlin (Android):
com.example.app
Service → ApiService.kt
MainActivity.kt

Como executar:

Instalar dependências Python:
pip install fastapi
pip install uvicorn
pip install ultralytics
pip install opencv-python
pip install numpy
pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu130

Para escolher a versão correta do CUDA, consulte o site:
https://pytorch.org/get-started/locally

Executar a API:
uvicorn main:app --reload

A API ficará disponível para receber imagens enviadas pelo aplicativo Android.

Imagens do aplicativo:
O projeto contém três telas principais:

Menu principal
![menu_inicial](https://github.com/user-attachments/assets/72cc6956-4c0f-4935-a552-b5b1c5e43dfc)

Tela de carregamento aguardando resposta do servidor
![aguardando_retorno](https://github.com/user-attachments/assets/233e63b3-3f44-4762-a84d-110370f5a773)

Tela com os resultados da análise nutricional
![tela_resultados](https://github.com/user-attachments/assets/06059a49-67d0-405c-be6c-c7aaeead1b41)

Autor:
Bernardo Bissotto
Email: bissotto.bernardo@gmail.com

Observação:
Projeto desenvolvido para fins acadêmicos, integrando visão computacional, estimativa nutricional e desenvolvimento mobile.
