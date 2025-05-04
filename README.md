# Know Your Fan: Análise de Perfil de Fã de Esports

![Jupyter](https://img.shields.io/badge/Jupyter-b54000?style=for-the-badge&logo=jupyter&logoColor=FFFFFF)
![Python](https://img.shields.io/badge/Python-d96d32?style=for-the-badge&logo=python&logoColor=FFFFFF)

Este Python Notebook implementa uma solução para coletar e analisar informações sobre o seu perfil como fã de esports. Inspirado na estratégia "Know Your Fan" utilizada por clubes e organizações, este projeto visa agregar dados de diversas fontes (simuladas neste projeto) para criar um panorama do seu engajamento, preferências e comportamento no ecossistema dos esports.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/anaperinii/know-your-fan/blob/main/knowyourfan.ipynb)

## ⚙️ Funcionalidades

### 📋 Cadastro de Fãs

* Formulário interativo com validação básica de e-mail e CPF.
* Utilização de Dropdowns e SelectMultiple para escolhas facilitadas.
* Feedback visual para campos obrigatórios e inválidos.
* Armazenamento dos dados em um DataFrame `pandas`.

### 🔍 Validação de Documentos com Inteligência Artificial

* **Upload de Arquivos:** Permite o upload de imagens nos formatos `.jpg`, `.png` e `.jpeg` para o documento de identificação e a selfie.
* **Reconhecimento Óptico de Caracteres (OCR):** Utiliza a biblioteca `pytesseract` para extrair texto da imagem do documento. Isso permite verificar se palavras-chave estão presentes, indicando um documento de identificação válido.
* **Verificação Facial:** Emprega a biblioteca `deepface`, com o modelo `VGG-Face` e o detector `opencv`, para comparar o rosto presente na foto do documento com o rosto na selfie. O resultado indica se os rostos são da mesma pessoa, juntamente com uma métrica de distância (quanto menor a distância, maior a similaridade).

### 📊 Dashboard de Engajamento e de Afinidades de Fãs de Esports

* **Análise Multiplataforma:** Permite analisar as afinidades/engajamento de um usuário (simuladamente) no Instagram, Twitter e Twitch.
* **Score de Engajamento (Médio):** Medida consolidada do envolvimento direto com a organização.
* **Classificação de Engajamento (Geral):** A categoria geral do fã com base no seu engajamento com a organização.
* **Score de Afinidade (Médio):** Medida consolidada do interesse e conexão com o ecossistema de esports em geral.
* **Classificação de Afinidade (Geral):** A categoria geral do fã com base nas suas afinidades no cenário de esports.
* **Detalhes de Engajamento por Plataforma:** Métricas específicas e informações sobre a interação do fã com a organização em cada plataforma analisada.
* **Detalhes de Afinidades por Plataforma:** Uma lista das afinidades do fã (times, jogadores, marcas, eventos) identificadas em cada plataforma.

### 👩🏻‍💻 Fan Analytics Dashboard

* **Cálculo do Fan Score:** Para cada plataforma, é calculado o "Fan Score" (0-100) com base em métricas simuladas como menções, interações com conteúdo, visualização de streams e interações com jogadores.
* **Classificação de Fãs por Nível de Engajamento:** Os usuários são classificados em diferentes níveis de engajamento (Observador, Fã Casual, Fã Engajado, Super Fã) com base no seu Fan Score.
* **Resumo do Perfil do Fã:** Apresenta um resumo consolidado do engajamento do usuário, incluindo o score médio entre as plataformas analisadas e a classificação geral como fã.
* **Análise Detalhada por Plataforma:** Para cada plataforma, são exibidas métricas específicas (simuladas) de engajamento, como número de menções, retweets, streams assistidos e interações com jogadores.
* **Identificação de Conteúdo e Interações Relevantes:** O dashboard destaca hashtags relacionadas à organização utilizadas pelo usuário, interações com jogadores específicos e preferências de jogos/eventos.

 ### 📡 Sistema de Análise de Perfis

* **Identificação de Plataforma:** Determina automaticamente a plataforma de mídia social a partir da URL fornecida.
* **Extração de Conteúdo (Mock):** Simula a obtenção de conteúdo relevante (texto de tweets, descrições de streams/posts) para as plataformas suportadas.
* **Análise de Relevância:** Utiliza um modelo de classificação zero-shot (`facebook/bart-large-mnli`) e uma análise baseada em palavras-chave para determinar a relevância do conteúdo para a organização e o cenário de esports.
* **Cálculo de Score Composto:** Gera um score único combinando a relevância do conteúdo, o número de seguidores (normalizado), a taxa de engajamento e, quando aplicável, o número de viewers (Twitch) e likes (Instagram).
* **Tier de Relevância:** Classifica os perfis em tiers de relevância ('baixa', 'média', 'alta') com base no score composto, ajustando os bins dinamicamente de acordo com a distribuição dos scores.

## 🚀 Como Executar:

1.  **Clique no badge "Open In Colab"** acima. Isso abrirá o notebook diretamente no ambiente do Google Colab em seu navegador.

2.  **Execute as Células de Código:**
    * O notebook é composto por células de texto e células de código Python.
    * Para executar uma célula de código, clique no ícone de "play" (▶️) à esquerda da célula ou pressione `Shift` + `Enter`.
    * Execute as células em sequência, de cima para baixo.

3.  **Visualize os Resultados:**
    * A saída da execução de cada célula será exibida logo abaixo da célula, incluindo texto, tabelas e gráficos.


## 🎲 Dados Simulados:

Os dados coletados e analisados neste notebook são simulados para fins de demonstração. Para uma análise real, se faz necessário integrar APIs das plataformas de interesse e autenticar suas contas para acessar seus dados reais.

