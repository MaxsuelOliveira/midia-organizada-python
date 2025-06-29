# 🗂️ Organizador de Imagens e Vídeos por Data com Python

Este script organiza automaticamente **imagens** e **vídeos** da pasta `upload/` em pastas separadas por **ano, mês e semana**, com base na **data original de criação** dos arquivos.

---

## ✅ Funcionalidades

- 📸 Extrai data de imagens via **EXIF** (`DateTimeOriginal`)
- 🎥 Extrai data de vídeos via **ffprobe** (`creation_time`)
- 🗃️ Cria estrutura: `organizado_YYYYMMDD_HHMM/ano-mes/semana-XX/`
- ❌ Arquivos sem data são movidos para: `organizado_YYYYMMDD_HHMM/SEM-DATA/`
- 🔒 Gera nova pasta com timestamp para não sobrescrever resultados anteriores

---

## ⚙️ Requisitos

- Python 3.7+
- Dependências:

```bash
pip install Pillow
ffprobe (vem com ffmpeg)
```

## Instalação do ffmpeg

### Linux

```bash
sudo apt install ffmpeg
```

### Windows

```bash
choco install ffmpeg
```

## 🚀 Como usar

1. Coloque seus arquivos em:
./upload/

2. Execute o script:
python organizar.py

Os arquivos serão organizados em uma nova pasta com timestamp, como:

    organizado_20250622_0215/
    ├── 2025-06/
    │   └── semana-25/
    │       ├── foto1.jpg
    │       └── video1.mp4
    └── SEM-DATA/
        └── arquivo_sem_data.png

## 🧩 Suporte a formatos

Tipo	Extensões
Imagens	.jpg, .jpeg, .png
Vídeos	.mp4, .mov, .avi, .mkv

## 📌 Observações

Arquivos sem data válida são enviados para SEM-DATA/

## Author

### Maxsuel David

<div align=center id="footer-default">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/maxsuelOliveiradev/?utm_source=rocketseat&utm_medium=organic&utm_campaign=profile&utm_term=share&utm_content=md-04583-links)
[![Instagram](https://img.shields.io/badge/Instagram-C13584?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/david_o.santos/)
[![GitHub](https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MaxsuelOliveira)
[![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/channels/@MaxDavid#7163)
[![Rocketseat](https://img.shields.io/badge/Rocketseat-7159C1?style=for-the-badge&logo=rocketseat&logoColor=white)](https://app.rocketseat.com.br/me/md-04583)
[![Telegram](https://img.shields.io/badge/Telegram-40A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/@oliveiraMaxsuel)
</div>
