# Google Maps Comment Collector 📍💬

[![License: Custom ANCL](https://img.shields.io/badge/License-ANCL-blue.svg)](LICENSE)
[![Python Version](https://img.shields.io/badge/Python-3.8%2B-brightgreen.svg)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg?logo=jupyter)](https://jupyter.org/)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--2107--7170-green.svg)](https://orcid.org/0009-0003-2107-7170)

O **Google Maps Comment Collector** é um projeto interativo desenvolvido em **Jupyter Notebook** para a **coleta automatizada de comentários e avaliações no Google Maps**. O sistema utiliza **Selenium WebDriver** para navegação dinâmica e extração padronizada de dados para análises quantitativas e qualitativas.

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

A coleta manual de dados de opinião pública e avaliações em plataformas de geolocalização é um processo moroso e vulnerável a erros. Esta solução visa **otimizar o processo de obtenção de informações em grande escala**, reduzindo a necessidade de trabalho manual e garantindo:
- **Eficiência**: Raspagem automatizada ordenada por avaliações mais recentes.
- **Confiabilidade**: Tratamento para remoção de duplicatas e rolagem dinâmica.
- **Padronização**: Exportação automática para planilha Excel (`.xlsx`) pronta para análise estatística ou Processamento de Linguagem Natural (PLN).

---

## ✨ Funcionalidades

O collector é capaz de extrair as seguintes informações de cada avaliação:
- [x] **ID do Comentário (`id`)**: Identificador único extraído da DOM.
- [x] **Nome do Usuário (`usuario`)**: Nome de exibição do autor do comentário.
- [x] **Ano de Postagem (`ano_postagem`)**: Estimativa calculada com base na data relativa informada pelo Google Maps.
- [x] **Avaliação em Estrelas (`avaliacao`)**: Texto com a nota em estrelas atribuída (ex: "5 estrelas").
- [x] **Texto do Comentário (`comentario`)**: Conteúdo textual (com expansão automática de botões "mais").
- [x] **Status de Local Guide (`local_guide`)**: Indicador booleano (`True`/`False`).
- [x] **Presença de Foto (`foto`)**: Indicador booleano (`True`/`False`) de mídia anexada.

---

## 🛠️ Tecnologias Utilizadas

- **[Python 3.x](https://www.python.org/)** — Linguagem base do projeto.
- **[Jupyter Notebook](https://jupyter.org/)** — Ambiente interativo de desenvolvimento e execução.
- **[Selenium WebDriver](https://www.selenium.dev/)** — Automação e navegação web dinâmica.
- **[WebDriver Manager](https://github.com/SergeyPirogov/webdriver_manager)** — Gerenciamento automático do driver do Chrome.
- **[Pandas](https://pandas.pydata.org/)** & **[openpyxl](https://openpyxl.readthedocs.io/)** — Estruturação e exportação para planilhas Excel.

---

## 📦 Pré-requisitos

Antes de iniciar, certifique-se de possuir instalado em sua máquina:
1. **Python 3.8** ou superior.
2. Navegador **Google Chrome** instalado e atualizado.
3. Ambiente de execução para notebooks (**JupyterLab**, **Jupyter Notebook** ou extensão do **VS Code**).

---

## 🚀 Como Instalar e Executar

1. **Clone o repositório:**
```bash
git clone [https://github.com/Henrique-Sc/Google-Maps-Comment-Collector.git](https://github.com/Henrique-Sc/Google-Maps-Comment-Collector.git)
cd Google-Maps-Comment-Collector
```

2. **Crie e ative um ambiente virtual (opcional, porém recomendado):**
   
* Criação do Virtual Environment
 ```bash
 python -m venv venv
```

* Ativação
- No Linux/macOS:
    ```bash
    source venv/bin/activate


- No Windows:
    ```bash
    venv\Scripts\activate

 * Instale as dependências:
   pip install -r requirements.txt

 * Inicie o Jupyter Notebook:
   jupyter notebook

 * Executando a Coleta:
   * Abra o arquivo de notebook (.ipynb) no seu navegador ou editor de código.
   * Na célula de configuração, insira o link do local desejado na variável web_scrapping_target:
     web_scrapping_target = "[https://maps.app.goo.gl/SUA_URL_AQUI](https://maps.app.goo.gl/SUA_URL_AQUI)"

   * Execute as células em sequência.
   * O programa acessará a página, ordenará os comentários por mais recentes e fará a raspagem em lote.
   * Os dados serão salvos automaticamente em uma planilha Excel com o nome gerado no padrão:
     Comentarios_{nome_local}_{place_id}_{data_atual}.xlsx

📊 Estrutura dos Dados Coletados
Os dados são exportados diretamente para o arquivo Excel no seguinte formato:
| Campo | Tipo | Descrição | Exemplo |
|---|---|---|---|
| id | Texto | Identificador único da avaliação | ChZDSUhNMG9nS0VJQ0FnSUN... |
| usuario | Texto | Nome de exibição do autor | João Silva |
| ano_postagem | Número | Ano estimado da publicação | 2025 |
| comentario | Texto | Conteúdo do comentário publicado | Excelente atendimento e estrutura. |
| avaliacao | Texto | Nota em estrelas extraída | Classificado com 5,0 de 5 estrelas |
| foto | Booleano | Presença de mídia anexada | True / False |
| local_guide | Booleano | Se o usuário é Local Guide | True / False |
🎓 Como Citar
Se você utilizar este software em pesquisas científicas, Trabalhos de Conclusão de Curso (TCC), dissertações ou teses, por favor cite-o utilizando o arquivo CITATION.cff do repositório ou a referência BibTeX abaixo:
@software{Costa_Google_Maps_Comment_2026,
  author = {Costa, Henrique da Silva},
  title = {{Google Maps Comment Collector}},
  version = {1.0.0},
  year = {2026},
  publisher = {GitHub},
  url = {[https://github.com/Henrique-Sc/Google-Maps-Comment-Collector](https://github.com/Henrique-Sc/Google-Maps-Comment-Collector)},
  license = {ANCL}
}

📜 Licença
Este projeto está licenciado sob a Academic Non-Commercial License (ANCL).
Permite o uso, modificação e redistribuição para fins exclusivamente acadêmicos, educacionais e de pesquisa, sendo vedado o uso comercial sem autorização prévia do autor.
Para mais detalhes, consulte o arquivo LICENSE.
✉️ Autor e Contato
Henrique da Silva Costa
 * 🏛️ Instituição: Instituto Federal de Educação, Ciência e Tecnologia de São Paulo (IFSP)
 * 📧 E-mail: henrique.costa3@aluno.ifsp.edu.br
 * 🆔 ORCID: 0009-0003-2107-7170
 * 📄 Currículo Lattes: lattes.cnpq.br/1693985798432329
 * 🐙 GitHub: @Henrique-Sc

---

## 2. Recomendado: Crie o arquivo `requirements.txt`

Para facilitar a instalação por outros usuários que baixarem seu repositório, crie um arquivo chamado `requirements.txt` na raiz do projeto com o seguinte conteúdo:

```text
selenium>=4.0.0
webdriver-manager
pandas
openpyxl
notebook

