# Estilos CSS: Inline, Internos e Externos

Os estilos CSS dividem-se em três tipos principais consoante o local onde são aplicados. O código fornecido nos exemplos demonstra a utilização prática destas abordagens.

## 1. Estilos Inline

Aplicam-se diretamente na tag HTML através do atributo `style`. Têm a maior prioridade de especificidade mas dificultam a manutenção se usados em excesso.

No exemplo apresentado, o alinhamento do parágrafo final é definido desta forma:

```html
<p style="text-align: right;"><a href="page02.html" target="_self">Ir para a próxima página</a></p>
```

## 2. Estilos Internos (ou Incorporados)

Definem-se dentro da própria página HTML, no bloco `<style>` localizado no interior da secção `<head>`. Afetam apenas o documento onde se encontram.

O código abaixo ilustra a aplicação de um estilo interno para sublinhar os títulos principais:

```html
<head>
    <style>
        h1 {
            text-decoration: underline;
        }
    </style>
</head>
```

## 3. Estilos Externos

Encontram-se num ficheiro CSS separado (por exemplo, `style.css`) e são ligados ao documento HTML através da tag `<link>` na secção `<head>`. É o método recomendado para projetos reais porque centraliza a formatação e permite reutilizar regras em várias páginas.

O ficheiro externo define o aspeto geral do corpo da página, títulos, parágrafos e hiperligações:

```css
@charset "UTF-8";

body {
    background-color: darkslategray;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 20px;
}

h1 {
    color: darkblue;
    background-color: lightblue;
}

h2 {
    color: lightblue;
}

p {
    color: aliceblue;
    text-align: justify;
}

a {
    color: lightseagreen;
}
```

A ligação a este ficheiro é feita no cabeçalho do HTML:

```html
<link rel="stylesheet" href="style.css">
```