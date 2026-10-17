# Site — Matheus Rodrigues Tattoo Artist

Site estático (HTML + CSS + JavaScript), sem servidor e sem instalação.
Abertura com vídeo em repetição, seções Realismo, Cicatrizados, Quem sou eu? (com vídeo) e Contato (WhatsApp e Google Maps).

## Estrutura

```
index.html            página principal
css/style.css         visual do site
js/app.js             funcionamento (animação, galerias, vídeo, botões)
data/content.js       TODOS os textos, número de WhatsApp, endereço e nomes das imagens
assets/media/         fotos, logotipo do topo e vídeo do artista
assets/logo-hero.png  logo (sem fundo) que fica acima do nome na abertura
```

## Como colocar no ar com o GitHub Pages

1. Crie uma conta em github.com e clique em **New repository** (pode ser público).
2. Dê um nome (ex.: `site-matheus`) e crie o repositório.
3. Clique em **uploading an existing file** e arraste TODO o conteúdo desta pasta
   (as pastas `css`, `js`, `data`, `assets` e o arquivo `index.html`). Clique em **Commit changes**.
   - Se o navegador não deixar arrastar pastas, descompacte o zip e envie as pastas por partes, ou use o aplicativo GitHub Desktop.
4. Vá em **Settings → Pages**. Em *Source*, escolha **Deploy from a branch**, branch **main**, pasta **/ (root)**, e salve.
5. Em 1 a 2 minutos o site abre em `https://SEU-USUARIO.github.io/site-matheus/`.

## Como editar

- **Textos, WhatsApp, endereço, link do mapa, Instagram:** abra `data/content.js`, altere o texto entre aspas e salve (no GitHub: abra o arquivo → ícone de lápis → *Commit changes*).
  - O WhatsApp fica em `"wa"`, só números com DDI e DDD (ex.: `556291442969`).
  - O nome no topo é `"name"`. Vazio = aparece só o logotipo `logo-topo.jpg`.
- **Trocar uma foto:** envie a nova imagem para `assets/media/` com o MESMO nome da antiga (ex.: `realismo-01.jpg`). Ela substitui a atual.
- **Adicionar uma foto:** envie o arquivo para `assets/media/` e acrescente um bloco `{ "id": "nome-do-arquivo.jpg", "t": "", "s": "", "d": "" }` na lista `"realismo"` ou `"cicatrizados"` em `data/content.js`.
  (`t` = título, `s` = estilo, `d` = descrição; em cicatrizados também há `h` = tempo de cicatrização, `dt` = data AAAA-MM-DD e `n` = observações.)
- **Trocar o vídeo do artista:** substitua `assets/media/artista-video.mp4` (mantenha o nome). Use MP4, de preferência até 20 MB.
- **Trocar o vídeo da abertura:** substitua `assets/media/hero-video.mp4` (mantenha o nome). Prefira MP4 leve, sem áudio, de até uns 5 MB.

## Importante

Esta versão **não tem o painel do dono online**: as edições são feitas nos arquivos, como acima.
Um painel com login e upload de fotos exige um servidor (por exemplo Supabase). A versão com painel continua disponível no link do claude.ai, mas só abre para quem está logado na sua organização.
