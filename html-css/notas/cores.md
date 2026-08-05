# Módulo 02 - Capítulo 13: Cores em HTML5 e CSS3

## 1. Psicologia e Fundamentos das Cores no Design

A escolha das cores impacta diretamente as emoções e a percepção do usuário sobre uma marca ou site:

* **Azul**: Transmite confiança, segurança e tranquilidade. Muito utilizado por empresas de tecnologia e corporativas.
* **Vermelho**: Estimula urgência, paixão e atenção.
* **Amarelo e Vermelho**: Combinação que estimula o apetite, amplamente usada na indústria alimentícia.
* **Verde**: Associado à natureza, saúde, sustentabilidade e esperança.
* **Marrom**: Traz sensação de solidez, rusticidade e terra.
* **Preto / Tons Escuros e Dourado**: Remetem ao luxo, sofisticação e minimalismo. *Atenção ao usar preto no background para não comprometer a leitura.*

---

## 2. Formatos de Representação de Cores no CSS

Existem diferentes formas de declarar cores nas folhas de estilo:

* **Nomes das Cores**: Representação direta em inglês (ex: `blue`, `red`).
* **Hexadecimal (`#RRGGBB`)**: Código de 6 dígitos base hexadecimal (utilizado com ferramentas como GIMP ou inspectores).
* **RGB (`rgb(r, g, b)`)**: Sistema aditivo com valores de 0 a 255 para Red, Green e Blue.
* **HSL (`hsl(h, s, l)`)**:
* **Matiz (Hue)**: Ângulo do círculo cromático (0 a 360).
* **Saturação (Saturation)**: Intensidade da cor (0% a 100%).
* **Luminosidade (Lightness)**: Brilho da cor (0% a 100%).


* **Transparência (Canal Alpha)**:
* `rgba(r, g, b, a)`
* `hsla(h, s, l, a)`
*(Sendo `a` a opacidade de 0.0 a 1.0).*


* **Dica de VS Code**: O editor possui um seletor visual (*Color Picker*) integrado para alternar e ajustar os formatos rapidamente.

---

## 3. Teoria e Harmonia de Cores

Como combinar cores de forma agradável usando o **Círculo Cromático**:

### Classificação das Cores

* **Primárias**: Cores puras base.
* **Secundárias**: Mistura de duas primárias.
* **Terciárias**: Mistura de uma primária com uma secundária.
* **Temperatura**: Divisão entre cores quentes (energia, vibração) e cores frias (calma, profundidade).

### Esquemas de Harmonia

* **Monocromia**: Variações de tom e saturação de uma única cor.
* **Cores Complementares**: Cores opostas no círculo cromático (alto contraste).
* **Cores Análogas**: Cores vizinhas no círculo cromático (harmonia suave).
* **Análogas + Complementar**: Mistura de harmonia suave com um ponto de destaque.
* **Triádicas e Tetrádicas (Quadrado)**: Combinações geométricas no círculo para esquemas multicoloridos e equilibrados.

---

## 4. Ferramentas para Criação de Paletas

Ferramentas essenciais para encontrar e gerar combinações profissionais:

* **[Adobe Color](https://color.adobe.com/)**: Regras automáticas de harmonia, extração de paletas e degradês a partir de imagens.
* **[Paletton](https://paletton.com/)**: Ferramenta clássica para simulação de esquemas de cores.
* **[Coolors](https://coolors.co/)**: Gerador rápido de paletas e navegação por combinações populares.

---

## 5. Estilização com Degradês (`gradients`)

Aplicação de transições de cores no CSS via `background-image`:

* **Linear Gradient**:
```css
background-image: linear-gradient(180deg, #ff0000, #0000ff);

```


Permite definir o ângulo (em graus) ou direção (`to right`, `to bottom`).
* **Radial Gradient**:
```css
background-image: radial-gradient(circle, #ffffff, #000000);

```


Cria transições circulares ou elípticas a partir do centro.
* **Ajustes Práticos**: Fixar o degradê ao rolar a página e evitar o exagero na saturação para manter a legibilidade.

---

## 6. Aplicação Prática no Projeto

Passos para construir um site harmonioso:

1. **Configurações Globais**: Reset básico e definição das variáveis de estilo.
2. **Plano de Fundo**: Aplicação de degradê sutil no `body`.
3. **Container de Conteúdo**: Uso de transparências (`rgba`/`hsla`) para criar camadas sem cobrir totalmente o fundo.
4. **Detalhes Visuais**:
* Bordas arredondadas (`border-radius`).
* Sombras suaves (`box-shadow`) para profundidade.
* Hierarquia de títulos usando paleta complementar ou monocromática.