# 🚀 Dload - Fast & Interactive Video Downloader for the Terminal

![Python](https://img.shields.io/badge/Python-3.7%2B-blue)
![yt-dlp](https://img.shields.io/badge/yt--dlp-powered-blueviolet)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
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
| 📣 Pré-visualização    | ✅    | ❌            |
| 📦 Pronto para empacote| ✅    | ❌            |
| 🎯 Multiplataforma     | ✅    | ✅            |

---

## ✨ Principais Features

- **🎯 Download inteligente**
  - MP4 (vídeo) e MP3 (música) em alta qualidade
  - Suporte a playlists e vídeos privados (com `cookies.txt`)

- **🖥️ Interface premium**
  - Menus interativos com emojis, cores e banners estilizados
  - Confirmação de título do vídeo antes do download

- **📂 Organização automática**
  - Arquivos salvos de forma intuitiva em:
    ```
    ~/Downloads/
    ~/Vídeos/
    ~/Músicas/
    ```
  - Integração com XDG (`~/.config/user-dirs.dirs`)

- **🧠 Verificações inteligentes**
  - Checagem de espaço em disco antes de baixar
  - Verificação de atualizações do yt-dlp
  - Detecção de cookies para conteúdo restrito

- **⚙️ Extras**
  - 📜 Histórico de downloads detalhado (`~/.dload_history`)
  - 📁 Log de atividades (`~/.dload.log`)
  - 🔄 Atualização automática do yt-dlp
  - 📦 Estrutura pronta para empacotamento (.deb, AUR, pipx etc.)
  - 🐍 Código simples, tudo em um único arquivo (`dload`)

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
- [yt-dlp](https://github.com/yt-dlp/yt-dlp)
- [FFmpeg](https://ffmpeg.org/)

## 🧩 Instalação Isolada com `pipx`

O **Dload** utiliza o `pipx` para instalar o `yt-dlp` de forma isolada, evitando conflitos com outras versões ou pacotes do Python no sistema. Isso garante que o **yt-dlp** funcione de maneira independente, sem afetar outras dependências ou aplicações do seu ambiente Python.

### O que é o `pipx`?
- **`pipx`** é uma ferramenta que permite a instalação e execução de pacotes Python em ambientes isolados, de forma que eles não interfiram no sistema ou em outras dependências. Isso é especialmente útil para ferramentas de linha de comando como o **yt-dlp**, garantindo que cada ferramenta tenha suas dependências controladas e isoladas.

### Benefícios do `pipx`:
- **Isolamento**: Cada pacote instalado via `pipx` tem seu próprio ambiente isolado, evitando conflitos com outras bibliotecas ou versões do Python no sistema.
- **Facilidade**: A instalação e atualização de pacotes se tornam mais simples e sem impacto em outras dependências do sistema.
- **Segurança**: Pacotes são executados em ambientes separados, o que reduz o risco de afetar outras partes do sistema.

### Como o Dload usa o `pipx`?

O **Dload** verifica automaticamente se o `pipx` está instalado no seu sistema. Caso não esteja, ele tenta instalar o `pipx` através do gerenciador de pacotes da sua distribuição (como `apt`, `pacman`, `brew` etc.). Em seguida, o **yt-dlp** é instalado de maneira isolada usando o `pipx`, garantindo que o processo de download de vídeos e áudios ocorra sem interferências externas.

---

## 🚀 Instalação

 O Dload verifica se as dependências necessárias estão instaladas no seu sistema e tenta instalá-las automaticamente, caso contrário. As dependências incluem `pipx`, `yt-dlp` e `ffmpeg`. 

### 🧠 Instalação Automática de Dependências

 O Dload tentará instalar as dependências ausentes automaticamente utilizando o gerenciador de pacotes da sua distro. Caso as dependências não sejam encontradas, o Dload tentará instalar cada uma delas de maneira isolada.

#### O que será instalado automaticamente:
- **pipx**: Para instalação isolada do Dload (recomendado)
- **yt-dlp**: Para download de vídeos e áudios
- **ffmpeg**: Para converter e processar vídeos

---

### 🐧 Linux/macOS:

1. Clone o repositório:

    ```bash
    git clone https://github.com/GuilhermesFreitas/dload
    ```

2. Navegue até o diretório do repositório:

    ```bash
    cd dload
    ```

3. Copie o script para o diretório de binários local:

    ```bash
    cp dload ~/.local/bin/
    ```

4. Certifique-se de que `~/.local/bin` está no seu `$PATH`.

### 🪟 Windows (PowerShell - Método Recomendado):

1. Clone o repositório:

    ```powershell
    git clone https://github.com/GuilhermesFreitas/dload
    ```

2. Navegue até o diretório do repositório:

    ```powershell
    cd dload
    ```

3. Crie uma pasta para scripts locais, caso ainda não exista:

    ```powershell
    New-Item -ItemType Directory -Force "$env:USERPROFILE\.local\bin"
    ```

4. Copie o script `dload` para a pasta:

    ```powershell
    Copy-Item .\dload "$env:USERPROFILE\.local\bin\dload"
    ```

5. Adicione a pasta ao `PATH`, se necessário:

    ```powershell
    [Environment]::SetEnvironmentVariable("PATH", $env:PATH + ";$env:USERPROFILE\.local\bin", [System.EnvironmentVariableTarget]::User)
    ```

6. Reinicie o terminal ou use:

    ```powershell
    $env:PATH += ";$env:USERPROFILE\.local\bin"
    ```

7. Teste a instalação:

    ```powershell
    dload
    ```

#### Se não funcionar, adicione ao seu `.bashrc` ou `.zshrc`:

```bash
export PATH="$HOME/.local/bin:$PATH"
```

## 💡 Como Usar

Após instalar o Dload, você pode usá-lo diretamente no terminal. Se você já tiver as dependências necessárias (como `yt-dlp` e `ffmpeg`) instaladas, o Dload verificará automaticamente se há algo faltando e tentará instalar o que for necessário, de forma automatizada.

#### 1. Execute o comando no terminal:
```
dload
```
#### Você verá um menu interativo para escolher entre:
```
    ========================================
          Dload - Fastdownload      
    ========================================


1. 🎵 Baixar Áudio (MP3)
2. 🎮 Baixar Vídeo (MP4)
3. 📜 Mostrar Histórico
4. 🧹 Limpar Histórico
5. ❌ Sair
```
#### Você poderá escolher onde salvar o conteúdo: Downloads, Vídeos ou Músicas.
```
🌍 Cole a URL do vídeo: 

📋 Título: 
✔️  Confirmar? [S/n]: 

 📂 Escolha onde salvar:
1 - Downloads
2 - Vídeos
3 - Músicas
Digite o número (1-3):

```
## 🛠️ Solução de Problemas

#### - Se encontrar erros, certifique-se que:
  
  1. FFmpeg está instalado (`ffmpeg -version`)
  2. yt-dlp está atualizado (`yt-dlp -U`)
  3. Tem permissão na pasta destino

---

## 🧼 Desinstalação
```
rm ~/.local/bin/dload
```
#### Opcional: remova o diretório clonado do repositório:
```
rm -rf ~/dload
```
---
## Projeto Open Source

#### Este projeto é open source e contribuições são bem-vindas!

### ✨ Como ajudar:

Dando estrela ⭐ no repositório

Sugerindo melhorias ou reportando bugs

Enviando pull requests

## 📝 Licença

### Este projeto está licenciado sob a Licença MIT.

Você pode usar, modificar e distribuir este projeto, desde que inclua o aviso de direitos autorais e a licença.
Para mais detalhes, veja o arquivo LICENSE.

