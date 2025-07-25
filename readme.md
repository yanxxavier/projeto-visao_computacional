# 🌟 Desenvolvimento do Projeto

Aqui está meu registro pessoal das etapas, dúvidas, descobertas e soluções durante a jornada do projeto de detecção com YOLOv8.

---

## 🚀 Início

- Comecei com a ideia de montar um detector de pessoas usando YOLOv8, já pensando no Orange Pi pra rodar depois.
- O projeto foi pensado no meu sogro, que tinha câmeras, mas não conseguia ter esse controle de movimentação na sua rua.

---

## 🖼️ Montando o Dataset

- Busquei vídeos de monitoramento públicos no [Kitware Data](https://data.kitware.com/) 
- Usei o Roboflow pra criar as anotações no formato YOLO. Tive algumas dificuldades em rotular dezenas de imagens, mas deu certo.
- Separei as imagens assim:
  - **Treino:** 111 imagens
  - **Validação:** 22 imagens
  - **Teste:** 6 imagens
- Na fase inicial, trabalhei com só duas classes: "pessoa" e "carro", mas já penso em aumentar essa pool no futuro.

---

## 🏋️‍♂️ Primeiros Treinos

- Testei treinar com o modelo base `yolov8n.pt`, poucas épocas só pra ver como funcionava. Foi um choque de realidade, pois estava muito longe do mínimo desejado, não conseguia identificar NADA nas inferências que estava fazendo.
- Tentei treinar por mais 50 épocas, melhorou quase nada, mas pelo menos já conseguia ver o resultado nos treinos (validação ainda estava bem longe).

---

## 🕵️‍♂️ Caçando Problemas

- Descobri que estava usando um modelo antigo (`train1.pt`) pra fazer inferência, por isso estava ruim.
- Troquei pro peso mais atual do treinamento (`best.pt`) e já melhorou bastante.

---

## 🔧 Ajustes & Aprendizados

- Nada ainda funcionava, tive que voltar ao Roboflow para aumentar meu dataset. Coloquei mais imagens, ainda com foco em pessoas e carros.
- Num primeiro momento, a mudança não foi tão significativa, mas já conseguia ter resultados na validação.
- No primeiro dataset, nem usando limiar de 0.5, tinha quaisquer resultados na validação.
- Tivemos um grande pulo no segundo dataset, consegui começar a identificar pessoas de maneira desejada, com um limiar de 0.3.
- Ainda está longe do target, mas já fiquei bem feliz.

---

## 🗂️ Estrutura do Projeto

- Estruturei o repositório para facilitar manutenção e reuso.
- **Estrutura básica:**
  ```
  ├── main.ipynb                     # Notebook principal do projeto
  ├── requirements.txt               # Dependências do projeto
  ├── data.yaml                      # Configuração do dataset
  ├── .gitignore                     # Arquivos e pastas ignorados
  ├── README.md                      # Guia do projeto
  ├── dataSet/                       # Dataset anotado (não subir no git)
  ├── runs/                          # Resultados de treinamento (não subir no git)
  ```
- **Pipeline:**  
  1. Coleta e anotação das imagens e vídeos  
  2. Montagem do dataset e configuração do `data.yaml`  
  3. Treinamento do modelo com YOLOv8  
  4. Testes de inferência com imagens/vídeos  
  5. Validação dos resultados  
  6. Preparação para deploy no Orange Pi (primeiro com imagens/vídeos, depois webcam)

---

## 🍊 Foco no Orange Pi

- Preparei tudo pensando no ARM (Orange Pi) – dependências, comandos de instalação.
- Decidi: vou testar primeiro só com imagens e vídeos, depois parto pra webcam.
- Meu intuito é um MVP, o Orange Pi vai dar um grande up para o projeto.

---

## 💬 Conclusão

- Uma das principais coisas que aprendi foi dar importância para o dataset. Uma boa qualidade de dados muitas vezes se torna mais importante que o código ou implementações.
- Meu projeto só foi andar verdadeiramente quando aumentei o dataset em cerca de 100%.
- Tive alguns problemas pessoais durante o desenvolvimento que prejudicaram meu desempenho na disciplina. Mas não vou deixar de trabalhar neste projeto, mesmo depois que acabar — quero continuar refinando ele.
- Essa disciplina e esse projeto me abriram portas para fazer parte de uma bolsa, onde trabalhamos no monitoramento de reservatórios de petróleo usando Machine Learning.
- Só tenho a agradecer ao professor pela oportunidade desse conhecimento e peço desculpas por não ter aproveitado o quanto podia.

---

✨ Projeto feito com curiosidade, paciência e muita mão na massa!
