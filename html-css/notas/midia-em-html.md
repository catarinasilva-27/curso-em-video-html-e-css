# Apontamentos: Mídias em HTML5

Este documento resume as técnicas fundamentais de integração de conteúdos multimédia em páginas web utilizando HTML5, com base no código analisado.

## Imagens Dinâmicas e Responsivas

As imagens dinâmicas em HTML5 servem para adaptar o conteúdo visual ao ecrã do utilizador, poupando largura de banda e melhorando o desempenho em dispositivos móveis.

Utiliza-se o elemento `<picture>` como um contentor flexível que agrupa várias fontes alternativas através de tags `<source>`, terminando sempre com uma tag `<img>` padrão. O navegador lê as regras de cima para baixo e carrega o primeiro ficheiro cuja condição do atributo `media` seja verdadeira. Se nenhuma condição for cumprida, aplica-se a imagem definida na tag `<img>`.

* **`<source>`**: Define condições específicas através do atributo `media` (ex: `max-width`). O navegador avalia as regras de cima para baixo e carrega a primeira correspondência válida.
* **`<img>`**: Serve como elemento de suporte obrigatório no final da estrutura, atuando como fallback caso nenhuma regra das tags `<source>` seja cumprida ou para garantir compatibilidade geral.

```html
<picture>
    <source media="(max-width: 750px)" srcset="imagens/pequeno.png" type="image/png">
    <source media="(max-width: 1050px)" srcset="imagens/medio.png" type="image/png">
    <img src="imagens/grande.png" alt="Imagem grande">
</picture>

```

## Reprodução de Áudio

O elemento `<audio>` integra ficheiros de som de forma nativa, dispensando plugins externos.

* **Atributos principais**:
* `controls`: Exibe os controlos de reprodução nativos (play, pausa, volume, barra de progresso).
* `autoplay`: Inicia a reprodução automaticamente ao carregar a página.
* `loop`: Reinicia o áudio continuamente após o término.
* `preload`: Controla o carregamento prévio dos dados. O valor `metadata` descarrega apenas as informações básicas (duração, dimensões).


* **Múltiplas Fontes**: Utilizar a tag `<source>` no interior de `<audio>` assegura compatibilidade entre diferentes navegadores, ordenando os formatos suportados (como MP3, OGG e WAV). Inclui-se sempre uma mensagem alternativa para navegadores obsoletos.

```html
<audio preload="metadata" controls loop>
    <source src="midia/wildfire-jessievilla.mp3" type="audio/mpeg">
    <source src="midia/wildfire-jessievilla.ogg" type="audio/ogg">
    <source src="midia/wildfire-jessievilla.wav" type="audio/wav">
    <p>Infelizmente o teu navegador não consegue reproduzir este áudio.</p>
</audio>

```

## Reprodução de Vídeo

A gestão de vídeos divide-se entre conteúdos locais e incorporados de servidores externos.

### Vídeos Hospedados Localmente

O elemento `<video>` funciona de forma semelhante ao elemento de áudio, permitindo o controlo de dimensões (`width`, `height`), atributos de reprodução e múltiplas fontes através da tag `<source>`.

* **Boa prática**: Organizar as fontes do formato mais leve para o mais pesado.
* **Formatos comuns**: MP4, M4V, WEBM, OGV.

```html
<video src="midia/video.mp4" controls width="500px"></video>

```

### Vídeos em Servidores Externos

Para conteúdos alojados em plataformas terceiras, utiliza-se a tag `<iframe>` para incorporar o leitor através de um URL de embed.

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/nCKwUB8EVbc" title="YouTube video player" allowfullscreen></iframe>

```

### YouTube vs Vimeo

A escolha da plataforma externa depende dos objetivos de exibição e do modelo de negócio pretendido.

* **YouTube**:
* Focado no consumo em massa e na descoberta de conteúdos.
* Modelo de negócio baseado em anúncios e publicidade, sendo gratuito para utilizadores e criadores.
* Público geral, abrangendo entretenimento, tutoriais e vídeos corporativos públicos.
* Ferramentas diretas de monetização por visualizações e subscrições.


* **Vimeo**:
* Direcionado a profissionais, criadores e empresas que exigem controlo estrito sobre a apresentação.
* Modelo de negócio baseado em subscrições pagas, garantindo privacidade avançada e ausência de anúncios intrusivos.
* Público focado em cinema, design, portefólios ou comunicação interna.
* Controlo granular de privacidade, personalização do leitor e ferramentas avançadas de colaboração.