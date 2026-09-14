# Google Maps Comment Collector 📍💬

[![License: Custom ANCL](https://img.shields.io/badge/License-ANCL-blue.svg)](LICENSE)
[![Python Version](https://img.shields.io/badge/Python-3.8%2B-brightgreen.svg)](https://www.python.org/)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--2107--7170-green.svg)](https://orcid.org/0009-0003-2107-7170)

O **Google Maps Comment Collector** é uma ferramenta desenvolvida em Python para **coleta automatizada de comentários e avaliações no Google Maps**. O sistema utiliza **Selenium WebDriver** para navegação dinâmica e extração padronizada de dados para pesquisas quantitativas e qualitativas.

---

## 📋 Sumário
- [📌 Sobre o Projeto](#-sobre-o-projeto)
- [✨ Funcionalidades](#-funcionalidades)
- [🛠️ Tecnologias Utilizadas](#️-tecnologias-utilizadas)
- [📦 Pré-requisitos](#-pré-requisitos)
- [🚀 Como Instalar e Executar](#-como-instalar-e-executar)
- [📊 Estrutura dos Dados Coletados](#-estrutura-dos-dados-coletados)
- [📜 Licença](#-licença)
- [🎓 Como Citar](#-como-citar)
- [✉️ Autor e Contato](#️-autor-e-contato)

---

## 📌 Sobre o Projeto

A coleta manual de dados de opinião pública e avaliações em plataformas de geolocalização é um processo moroso e vulnerável a erros. Esta solução busca **otimizar o processo de obtenção de dados em grande escala**, garantindo:
- **Eficiência**: Raspagem automatizada em lote.
- **Confiabilidade**: Redução de erros de extração manual.
- **Padronização**: Exportação estruturada pronta para análise estatística ou Processamento de Linguagem Natural (PLN).

---

## ✨ Funcionalidades

O collector é capaz de extrair as seguintes informações de cada avaliação:
- [x] **ID do Comentário**: Identificador único da avaliação.
- [x] **Usuário / Autor**: Nome de exibição do perfil.
- [x] **Status de Local Guide**: Identificação de selo e nível de contribuição.
- [x] **Avaliação em Estrelas**: Nota atribuída (1 a 5 estrelas).
- [x] **Data de Publicação**: Período/data relativa do comentário.
- [x] **Texto da Avaliação**: Conteúdo textual da opinião.
- [x] **Presença de Mídia**: Indicador de fotos ou vídeos anexados.

---

## 🛠️ Tecnologias Utilizadas

- **[Python 3.x](https://www.python.org/)** — Linguagem base do projeto.
- **[Selenium WebDriver](https://www.selenium.dev/)** — Automação e navegação web dinâmica.
- **[Pandas](https://pandas.pydata.org/)** — Manipulação e estruturação dos dados coletados.

---

## 📦 Pré-requisitos

Certifique-se de possuir instalado em sua máquina:
1. **Python 3.8** ou superior.
2. Navegador **Google Chrome** atualizado.
3. **ChromeDriver** compatível com a sua versão do Chrome (ou gerenciado via `webdriver-manager`).

---

## 🚀 Como Instalar e Executar

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/Henrique-Sc/Google-Maps-Comment-Collector.git](https://github.com/Henrique-Sc/Google-Maps-Comment-Collector.git)
   cd Google-Maps-Comment-Collector
   
