# 🏆 TMDB Awards Database

[🇧🇷 Ler em Português](#-leia-em-português)

Welcome to the **TMDB Awards Database**! This project is the definitive Open-Source repository containing the structured history of the world's biggest movie, TV show, and anime awards (Oscars, Emmys, Golden Globes, Anime Awards, and many more).

We extract the official data from [The Movie Database (TMDB)](https://www.themoviedb.org) and serve it as clean, standardized `.json` files.

---

## 🎯 Why does this project exist?
Many systems, media servers (like Plex, Emby, and Jellyfin), and developers need the history of cultural award winners and nominees to create collections, build catalogs, and develop search engines.

TMDB has fantastic data, but accessing it repeatedly by scraping page by page eats up API quotas and is very slow.
This repository does the heavy lifting: **we generate pre-processed JSON files for each award so you can consume them instantly.**

---

## 📂 File Structure

The repository is organized in an extremely simple way:

*   [`index.json`](index.json) - **Master Catalog**: Contains the complete list of all available awards in this repository (with their respective TMDB IDs, names, and image URLs).
*   `awards/` - **The Historical Database**: Each award has its own file (e.g., `1-oscars.json`).

---

## 🛠️ How to Consume the Data (For Developers)

If you are a developer looking to integrate our data into your system, the path is very simple.

### 1. List the Awards
Make a GET request to the raw `index.json` using GitHub's Raw URL:
```bash
curl https://raw.githubusercontent.com/eunaumtenhoid/TMDB-Awards-Database/main/index.json
```

### 2. Download a Specific Award
Get the `tmdb_award_id` from the index (Example: `84` for the Anime Awards) and download the corresponding file from the `/awards` folder:
```bash
curl https://raw.githubusercontent.com/eunaumtenhoid/TMDB-Awards-Database/main/awards/84-anime-awards.json
```

---

## 📦 The JSON Format

All award files follow a strict standardized structure:

```json
{
  "award_info": {
    "tmdb_award_id": 84,
    "imdb_award_id": "",
    "name": "Crunchyroll Anime Awards",
    "slug": "anime-awards",
    "location": "Tokyo, Japan"
  },
  "years": {
    "2024": [
      {
        "category": "Anime of the Year",
        "tmdb_id": 114410,
        "media_type": "tv",
        "is_winner": true
      }
    ]
  }
}
```
* **Note**: All movies, series, and people listed use official TMDB IDs (`tmdb_id`) to ensure 100% cross-compatibility.

---

## 🤝 Contribute and Stay Updated
This repository is updated frequently as new ceremonies take place in the real world.
If you have any questions, feel free to open an **Issue**!

*Created with ❤️ for the Community.*

<br><br>

---
---

# 🇧🇷 Leia em Português

Bem-vindo ao **TMDB Awards Database**! Este projeto é um repositório Open-Source definitivo contendo o histórico estruturado das maiores premiações de filmes, séries e animes do mundo (Oscars, Emmy, Golden Globes, Anime Awards e muito mais).

Nós extraímos as informações oficiais da base de dados do [The Movie Database (TMDB)](https://www.themoviedb.org) e servimos arquivos `.json` limpos e padronizados.

---

## 🎯 Por que este projeto existe?
Muitos sistemas, servidores de mídia (como Plex, Emby e Jellyfin) e desenvolvedores precisam do histórico de vencedores e indicados de premiações culturais para criar coleções, montar catálogos e sistemas de busca.

O TMDB tem dados fantásticos, mas acessá-los repetidamente varrendo página por página gasta cota de API e é lento.
Este repositório faz o trabalho duro: **nós geramos os arquivos JSON mastigados de cada premiação para você consumir instantaneamente.**

---

## 📂 Estrutura de Arquivos

O repositório está organizado de forma extremamente simples:

*   [`index.json`](index.json) - **Catálogo Mestre**: Contém a lista completa de todas as premiações disponíveis neste repositório (com seus respectivos IDs do TMDB, nomes e URL da imagem).
*   `awards/` - **A Base de Dados Histórica**: Cada premiação tem seu próprio arquivo (ex: `1-oscars.json`).

---

## 🛠️ Como Consumir os Dados (Para Desenvolvedores)

Se você é um desenvolvedor querendo integrar nossos dados no seu sistema, o caminho é muito simples.

### 1. Liste as Premiações
Faça uma requisição GET para o `index.json` cru usando a URL Raw do GitHub:
```bash
curl https://raw.githubusercontent.com/eunaumtenhoid/TMDB-Awards-Database/main/index.json
```

### 2. Baixe uma Premiação Específica
Pegue o `tmdb_award_id` no index (Exemplo: `84` para o Anime Awards) e baixe o arquivo correspondente na pasta `/awards`:
```bash
curl https://raw.githubusercontent.com/eunaumtenhoid/TMDB-Awards-Database/main/awards/84-anime-awards.json
```

---

## 📦 O Formato JSON

Todos os arquivos de premiações seguem uma estrutura padronizada rigorosa:

```json
{
  "award_info": {
    "tmdb_award_id": 84,
    "imdb_award_id": "",
    "name": "Crunchyroll Anime Awards",
    "slug": "anime-awards",
    "location": "Tokyo, Japan"
  },
  "years": {
    "2024": [
      {
        "category": "Anime of the Year",
        "tmdb_id": 114410,
        "media_type": "tv",
        "is_winner": true
      }
    ]
  }
}
```
* **Nota**: Todos os filmes, séries e pessoas listados estão usando os IDs oficiais do TMDB (`tmdb_id`) para garantir 100% de compatibilidade cruzada.

---

## 🤝 Contribua e Mantenha-se Atualizado
Este repositório é atualizado frequentemente à medida que novas cerimônias acontecem no mundo real.
Se tiver alguma dúvida, sinta-se à vontade para abrir uma **Issue**!

*Criado com ❤️ para a Comunidade.*
