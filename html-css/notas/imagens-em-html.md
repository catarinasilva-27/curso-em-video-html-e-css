# Inserção de Imagens e Favicons

## Imagens

Usa a tag `<img>` para colocar imagens. Define sempre dois atributos essenciais:

* `src`: Caminho do ficheiro. Funciona na mesma pasta (`logo.png`), em subpastas (`imagens/logo.png`) ou através de um endereço web completo.
* `alt`: Descrição da imagem. Garante acessibilidade e serve de alternativa se o carregamento falhar.
* `width`: Define a largura em pixéis de forma opcional.

## Favicon

O ícone que aparece no separador do navegador coloca-se no cabeçalho (`<head>`) com esta estrutura:

```html
<link rel="icon" href="favicon.ico" type="image/x-icon">

```