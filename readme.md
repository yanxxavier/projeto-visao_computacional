# Projeto de Visão Computacional 2025.1

Este repositório contém o desenvolvimento do projeto da disciplina **Visão Computacional 2025.1**. O objetivo é construir uma solução modular para detecção, recorte, classificação de objetos em vídeo e notificação ao usuário, utilizando técnicas clássicas de visão computacional.

---

## 📑 Sumário

- [Descrição do Projeto](#descrição-do-projeto)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Requisitos](#requisitos)
- [Instalação](#instalação)
- [Como Executar](#como-executar)
- [Pipeline do Projeto](#pipeline-do-projeto)
- [Resultados e Métricas](#resultados-e-métricas)
- [Possíveis Extensões](#possíveis-extensões)
- [Referências](#referências)

---

## Descrição do Projeto
> O projeto visa detectar movimento em vídeos, recortar regiões de interesse (ROI), classificar o objeto identificado e notificar o usuário via telegram.

---

## Estrutura do Projeto

```
projeto-visao_computacional/
│
├── src/                 # Códigos-fonte do projeto
│   ├── captura_video.py
│   ├── detector_movimento.py
│   ├── recorte_roi.py
│   ├── classificador.py
│   └── notificacao.py
│
├── dataset/             # Imagens e vídeos para testes/classificação (se aplicável)
├── resultados/          # Imagens/vídeos/resultados gerados pelo sistema
├── requirements.txt     # Dependências do projeto
├── README.md            # Este arquivo
└── ...                  # Outros arquivos (config, scripts, etc)
```

---

## Requisitos

- Python >= 3.8
- Bibliotecas:
  - opencv-python
  - numpy
  - scikit-learn
  - (opcionais: Pillow, matplotlib, requests)

Veja o arquivo `requirements.txt` para detalhes.

---

## Instalação

Clone o repositório e instale as dependências:

```bash
git clone https://github.com/yanxxavier/projeto-visao_computacional.git
cd projeto-visao_computacional
pip install -r requirements.txt
```

---

## Como Executar

Explique aqui como rodar o pipeline completo ou cada módulo isoladamente.

Exemplo:
```bash
python src/captura_video.py --input video.mp4
python src/detector_movimento.py --input video.mp4
python src/recorte_roi.py --input video.mp4
python src/classificador.py --input roi.jpg
python src/notificacao.py --mensagem "Objeto detectado"
```

Ou descreva um script principal que integra tudo:

```bash
python src/main.py --input video.mp4
```

---

## Pipeline do Projeto

1. **Captura do vídeo**
   - Descreva o método/fonte (ex: webcam, arquivo .mp4).
2. **Detecção de movimento**
   - Explique a técnica utilizada (ex: background subtraction, frame differencing).
3. **Recorte da região de interesse (ROI)**
   - Critérios para recorte e salvamento.
4. **Classificação**
   - Método de extração de características e algoritmo de classificação.
5. **Notificação**
   - Como o usuário é notificado (print/log, Telegram, e-mail etc.).

---

## Resultados e Métricas

- Insira aqui exemplos de resultados obtidos (prints, imagens, vídeos).
- Apresente métricas de desempenho: acurácia, tempo de processamento, etc.
- Faça análise crítica dos resultados e possíveis limitações.

---

## Possíveis Extensões

Liste ideias para futuras melhorias, tais como:
- Uso de modelos de deep learning.
- Inclusão de múltiplos canais de notificação.
- Suporte a múltiplas classes de objetos.

---

## Referências

Liste artigos, tutoriais, livros e documentação usados no desenvolvimento.

---

> **Nota:** O código-fonte e os dados devem ficar disponíveis neste repositório, conforme exigência da disciplina.