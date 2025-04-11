# 🚀 Dload - Fast & Interactive Video Downloader for the Terminal

![Python](https://img.shields.io/badge/Python-3.7%2B-blue)
![yt-dlp](https://img.shields.io/badge/yt--dlp-powered-blueviolet)
![GitHub stars](https://img.shields.io/github/stars/GuilhermesFreitas/dload?style=social)

**Dload** é uma ferramenta de terminal super rápida para baixar vídeos e músicas do YouTube (e muitos outros sites), usando o poderoso [`yt-dlp`](https://github.com/yt-dlp/yt-dlp) — com interface amigável, organização automática e recursos inteligentes!

---

## 🌟 Por que usar o Dload?

| Recurso                | Dload | yt-dlp Padrão |
|------------------------|-------|---------------|
| 🖥️ Interface amigável  | ✅    | ❌            |
| 📂 Auto-organização    | ✅    | ❌            |
| 🧠 Verificações úteis  | ✅    | ❌            |
| 📜 Histórico           | ✅    | ❌            |
| 🎯 Multiplataforma     | ✅    | ✅            |

---

## ✨ Principais Features

- **🎯 Download inteligente**
  - MP4 (vídeo) e MP3 (música) em alta qualidade
  - Suporte a playlists e vídeos privados (com `cookies.txt`)

- **🖥️ Interface premium**
  - Menus interativos com emojis, cores e banners estilizados

- **📂 Organização automática**
  - Arquivos salvos em:
    ```
    ~/Downloads/
    ~/Vídeos/
    ~/Músicas/
    ```

- **🧠 Verificações inteligentes**
  - Checa espaço em disco antes de baixar
  - Verifica atualizações do yt-dlp
  - Detecta cookies para conteúdo restrito

- **⚙️ Extras**
  - 📜 Histórico de downloads (`~/.dload_history`)
  - 🔄 Atualização automática do yt-dlp
  - 🐍 Código simples e único (fácil de entender e contribuir)

---

## 📑 Tabela de Conteúdo

- [✅ Requisitos](#-requisitos)
- [✨ Principais Features](#-principais-features)
- [🚀 Instalação](#-instalação)
- [💡 Como Usar](#-como-usar)
- [🛠️ Solução de Problemas](#️-solução-de-problemas)
- [🧼 Desinstalação](#-desinstalação)
- [✨ Como Ajudar](#-como-ajudar)

---

## ✅ Requisitos

### 📦 Dependências

- [Python 3.7+](https://www.python.org/downloads/)
- [FFmpeg](https://ffmpeg.org/)
- [yt-dlp](https://github.com/yt-dlp/yt-dlp)

### 🔧 Instalando Dependências

#### Debian/Ubuntu:

```bash
sudo apt update
```
```
sudo apt install -y python3 python3-pip ffmpeg
```
```
python3 -m pip install --user yt-dlp
```

#### Para Linux (Arch/Manjaro):
```bash
sudo pacman -S python python-pip ffmpeg
```
```
pip install --user yt-dlp
```

#### Para macOS (via Homebrew):
```bash
brew install python ffmpeg
```
```
pip install yt-dlp
```
#### Para Windows (PowerShell):
```powershell
winget install Python.Python.3.11
```
```
winget install Gyan.FFmpeg
```
```
pip install yt-dlp
```
#### Pipx (Opcional - Recomendado)

Para instalação isolada do Dload:

#### Instale o pipx primeiro
```
python3 -m pip install --user pipx
python3 -m pipx ensurepath
```
#### Ou em sistemas Linux via package manager
#### Debian/Ubuntu:
```
sudo apt install pipx
```
#### Arch/Manjaro:
```
sudo pacman -S python-pipx
```
#### Configure o PATH
```
pipx ensurepath
```
---


### 🚀 Instalação

```
git clone https://github.com/GuilhermesFreitas/dload
```
```
cd dload
```
```
cp dload ~/.local/bin/
```
Certifique-se de que ~/.local/bin está no seu $PATH.

## 🔍 Verifique:
```
which dload
```
Se não aparecer, adicione ao seu .bashrc ou .zshrc:
```
export PATH="$HOME/.local/bin:$PATH"
```
## 💡 Como Usar

Execute no terminal:
```
dload
```
Você verá um menu interativo para escolher entre:
```
========================================
          Dload - Fastdownload
========================================
1 - Baixar como MP3 (Música)
2 - Baixar como MP4 (Vídeo)
3 - Sair
========================================
```
Você poderá escolher onde salvar o conteúdo: Downloads, Vídeos ou Músicas.
```
 🔗 Cole aqui a URL do vídeo: 

 📂 Escolha onde salvar:
1 - Pasta Downloads
2 - Pasta Videos
3 - Pasta Músicas
Digite o número da opção (1-3):

```
## 🛠️ Solução de Problemas

- Se encontrar erros, certifique-se que:
  
  1. FFmpeg está instalado (`ffmpeg -version`)
  2. yt-dlp está atualizado (`yt-dlp -U`)
  3. Tem permissão na pasta destino

---

## 🧼 Desinstalação
```
rm ~/.local/bin/dload
```
Opcional: remova o diretório clonado do repositório:
```
rm -rf ~/dload
```
---
## Projeto Open Source

Este projeto é open source e contribuições são bem-vindas!

### ✨ Como ajudar:

Dando estrela ⭐ no repositório

Sugerindo melhorias ou reportando bugs

Enviando pull requests
