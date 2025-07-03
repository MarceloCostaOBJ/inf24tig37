
# EDUSPARK

Desenvolvido pelo grupo **inf24tig37**: [@MarceloCostaOBJ](https://github.com/MarceloCostaOBJ/), [@GandalfTheTech] AKA (https://github.com/GandalfTheTech) (Carlos Miguel Castro)

---

## Descrição do Tema

Este repositório documenta o desenvolvimento do projeto **EDUSPARK**, uma simulação de plataforma educativa interativa. O objetivo principal foi criar um conjunto de páginas web informativas com design moderno, funcionalidades básicas de navegação e estrutura organizada, respeitando os requisitos da unidade curricular.

---

## Organização do Repositório

Para facilitar a navegação:
- A **versão final** está na pasta [Build](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Build).
- A **galeria de imagens** com sketches e capturas está na pasta [Gallery](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Gallery/).

---

## Tecnologias Utilizadas

- [HTML5]
- [CSS3]


---

# Relatório do Projeto: EDUSPARK

## 1. Apresentação do Projeto

### Tema
Desenvolvimento de um website educativo com ênfase na aplicação correta de HTML5 semântico e CSS3 moderno, sem necessidade de JavaScript.

### Proposta
Criámos o site **EDUSPARK**, focado na promoção de cursos online de inglês, com 5 páginas estáticas:  
**Home, About, Prices, FAQ e Sign Up**

### Estrutura do Site
- Cabeçalho fixo (glassmorphism)
- Layout responsivo com flexbox
- Imagens com `<figure>` e `<figcaption>`
- Tabelas com `thead`, `tfoot`, `colspan` e `rowspan`
- Listas aninhadas
- Destaques com `<em>`, `<strong>`, `<mark>`
- Formulário funcional com validações `required`
- Link para download de ficheiro XML (planos de subscrição)

---

## 2. Interface com o Utilizador

### Sketches & Wireframes
Desenvolvemos o sitemap e o esboço da interface no início do projeto, disponíveis aqui:

- [Sketch da Página Inicial](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Gallery/SKETCH)

### Galeria de Resultados
Capturas finais de todas as páginas:  
🔗 [Ver Galeria](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Gallery/Print)

### Ilustrações
As imagens de apoio (ex: `Tea_main.svg`) foram retiradas de:  
🎨 [https://illustrationkit.com](https://illustrationkit.com)

### Repositório GitHub
Código-fonte disponível em:  
🔗 [https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Build](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Build)

---

## 3. Produto Final

### Ligação ao Site Online
Deploy via Netlify:  
🌐 [https://inf24tig37.netlify.app/](https://inf24tig37.netlify.app/)

### Instalação
A publicação foi feita por **upload manual** dos ficheiros `.html` e `.css` na plataforma Netlify.

### Navegação
- Menu presente em todas as páginas, com `hover` animado
- Cabeçalho fixo com efeito de vidro (glassmorphism)
- Estrutura clara com secções bem identificadas

### Formulário
- Campos: `first-name`, `last-name`, `email` com `required`
- Tipo `email` com validação automática
- Processado com [Formspree](https://formspree.io/)
- Redirecionamento automático para `obrigado.html`

---

## 4. Validação

Utilizámos os validadores da W3C:

- [Validador HTML](https://validator.w3.org/)  
- [Validador CSS](https://jigsaw.w3.org/css-validator/)
- [Validador XML](https://www.freeformatter.com/)


**Capturas de validação disponíveis aqui:**  
🖼️ [Validação HTML](https://github.com/MarceloCostaOBJ/inf24tig37/blob/main/Gallery/Validation/HTML.png)  
🖼️ [Validação CSS](https://github.com/MarceloCostaOBJ/inf24tig37/blob/main/Gallery/Validation/CSS.png)  
🖼️ [Validação XML & XSD](https://github.com/MarceloCostaOBJ/inf24tig37/blob/main/Gallery/Validation/XML_XSD.png)  

### Explicação Técnica da Validação

- ✅ O HTML passou sem erros nos testes W3C.
- ✅ O CSS passou sem erros críticos. Foram apenas gerados:
  - ⚠️ *Avisos sobre variáveis CSS (`--variavel`)* que não afetam o funcionamento.
  - ⚠️ *Avisos sobre `-webkit-backdrop-filter`*, utilizados para garantir compatibilidade com WebKit. Estes também são seguros.
- ✅ O XML (`planos.xml`) e o XSD (`planos.xsd`) foram validados com sucesso.
  - O ficheiro XML segue a estrutura definida no XSD e não apresenta erros de validação.
  - O XSD define os tipos de dados corretamente (ex: `xs:string`, `xs:decimal`, `xs:positiveInteger`) e todas as restrições foram respeitadas.

---

## 5. Cumprimento dos Requisitos


## Cumprimento dos Requisitos – Comprovação com Código e Explicação

### ✅ HTML5 semântico (`section`, `nav`, `main`, `figure`, `article`, `footer`, etc.)

- **Ficheiro:** `about.html`
- **Linha:** 49
```html
<section id="section2">
```
- **Explicação:**  
Utilização de `<section>` para estruturar semanticamente a página. Identifica uma secção temática com conteúdos relacionados.

---

### ✅ CSS3 externo com:

#### • Seletores de tipo, ID, classe, pseudo-classe (`:hover`, `:focus`)

- **Ficheiro:** `StyleSignup.css`
- **Linhas:** 92–98, 106–108
```css
.formulario-left input:focus {
  border-color: #7c3aed;
  box-shadow: 0 0 5px #7c3aed;
}
```
- **Explicação:**  
Quando o campo de input ganha foco (`:focus`), o contorno muda para realçar visualmente a interação.

---

#### • Pseudo-elementos (`::after`) e combinadores

- **Ficheiro:** `StyleAbout.css`
- **Linhas:** 97–101
```css
.nav-links a::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -6px;
  width: 0%;
  height: 2px;
  background: var(--purple);
  transition: width 0.3s ease;
}
```
- **Explicação:**  
O `::after` adiciona dinamicamente um sublinhado animado após os links de navegação, com uso de combinador `a::after`.

---

#### • Fundo com imagem (`Back_MainTOTAL.jpg`)

- **Ficheiro:** `StyleIndex.css`
- **Linha:** 30
```css
body.about-page {
  background: url('Back_MainTOTAL.jpg') no-repeat center/cover;
}
```
- **Explicação:**  
Define imagem de fundo aplicada à página com cobertura total e fixação ao scroll.

---

#### • Lista formatada, botão com `hover`, flutuação e `position`

- **Ficheiro:** `StyleIndex.css`
- **Linhas:** 123–125, 141–147
```css
.hero-illustration img {
  animation: float 6s ease-in-out infinite;
}
.btn:hover {
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}
```
- **Explicação:**  
Imagem com animação contínua de flutuação (`float`) e botão com destaque ao passar o rato (`:hover`).

---

#### • Responsividade via `@media`

- **Ficheiro:** `StyleAbout.css`
- **Linhas:** 102–114
```css
@media (max-width: 768px) {
  .header-inner {
    flex-direction: column;
  }
}
```
- **Explicação:**  
Adapta o layout para dispositivos móveis reorganizando elementos de navegação.

---

#### • Animações (`float`, `pulse-border`, `transform`)

- **Ficheiro:** `StyleAbout.css`
- **Linhas:** 194–207
```css
@keyframes pulse-border {
  0% { box-shadow: 0 0 12px ... }
  50% { box-shadow: 0 0 20px ... }
  100% { box-shadow: 0 0 12px ... }
}
```
- **Explicação:**  
Aplica um efeito visual animado ao contorno de elementos com `box-shadow` pulsante.

---

#### • `display: none` condicional por `@media`

- **Ficheiro:** `StyleAbout.css` ou `StyleIndex.css`
```css
@media (max-width: 768px) {
  .elemento-mobile-only {
    display: none;
  }
}
```
- **Explicação:**  
Oculta elementos que só devem aparecer em desktop.

---

#### • Substituição de texto por imagem (`.avatar`)

- **Ficheiro:** `about.html`
- **Linha:** 89
```html
<img class="avatar" src="avatar1.png" alt="Avatar 1">
```
- **Explicação:**  
Imagem circular usada no lugar de texto para identificar testemunhos de utilizadores.

---

### ✅ Imagens com `<img>`, `<figure>`, `<figcaption>`

- **Ficheiro:** `about.html`
- **Linha:** 90
```html
<figcaption class="testimonial-text">Ricardo</figcaption>
```
- **Explicação:**  
Elemento semântico para identificar a legenda associada à imagem do utilizador.

---

### ✅ Lista aninhada

- **Ficheiro:** `faq.html`
- **Linhas:** 63–69
```html
<ul>
  <li>Registration
    <ul>
      <li>Fill in all the required fields.</li>
    </ul>
  </li>
</ul>
```
- **Explicação:**  
Demonstração de lista dentro de outra lista, usada para detalhar passos ou estruturas.

---

### ✅ Destaques com `<em>`, `<strong>`, `<mark>`

- **Ficheiro:** `faq.html`
- **Linha:** 77
```html
<p><em>Online education</em> has grown... <strong>important</strong> ... <mark>offers flexibility</mark></p>
```
- **Explicação:**  
Texto destacado com semântica e estilo visual através de HTML e CSS.

---

### ✅ Tabela com `thead`, `tbody`, `tfoot`, `rowspan`, `colspan`

- **Ficheiro:** `faq.html`
- **Linhas:** 26–41
```html
<thead>
  <tr>
    <th rowspan="2">Question</th>
    <th colspan="2">Answers</th>
  </tr>
</thead>
```
- **Explicação:**  
Uso correto de cabeçalho, agrupamento de colunas e rodapé em tabelas de FAQ.

---

### ✅ Formulário com campos obrigatórios

- **Ficheiro:** `signup.html`
- **Linhas:** 24–36
```html
<input type="text" id="first-name" name="first-name" required>
```
- **Explicação:**  
Campo com atributo `required`, impedindo envio sem preenchimento.

---

### ✅ Ligação para download de ficheiro XML

- **Ficheiro:** `prices.html`
- **Linha:** 52
```html
<a href="planos.xml" download="planos.xml" class="select-btn">More Info</a>
```
- **Explicação:**  
Link com atributo `download` que permite ao utilizador guardar localmente o ficheiro XML.

---

### ✅ Documento XML e XSD válidos

- **Ficheiro:** `planos.xml` e `planos.xsd`
```xml
<xs:element name="preco" type="xs:decimal"/>
```
- **Explicação:**  
Ficheiro XML estruturado segundo um schema (XSD) que valida tipo de dados, elementos obrigatórios, restrições e hierarquia.


Requisitos obrigatórios implementados e comprovados:

- ✅ HTML5 semântico (`section`, `nav`, `main`, `figure`, `article`, `footer`, etc.)
- ✅ CSS3 externo com:
  - seletores de tipo, ID, classe, pseudo-classe (`:hover`, `:focus`)
  - pseudo-elementos (`::after`) e combinadores
  - fundo com imagem (`Back_MainTOTAL.jpg`)
  - lista formatada, botão com `hover`, flutuação e `position`
  - responsividade via `@media`
  - animações (`float`, `pulse-border`, `transform`)
  - `display: none` condicional por `@media`
  - substituição de texto por imagem (`.avatar`)
- ✅ Imagens com `<img>`, `<figure>`, `<figcaption>`
- ✅ Lista aninhada (ver `faq.html`)
- ✅ Destaques com `<em>`, `<strong>`, `<mark>`
- ✅ Tabela com `thead`, `tbody`, `tfoot`, `rowspan`, `colspan`
- ✅ Formulário com campos obrigatórios (`required`)
- ✅ Ligação para download de ficheiro XML (`prices.html`)
- ✅ Documento XML e XSD válidos

---

## . Glassmorphism e Estilo Visual

Usámos geradores e bibliotecas para criar efeitos como:

- `backdrop-filter` + `blur` para cabeçalho e cartões
- `pulse-border` animado no painel estatístico
- `hover transform` nos cartões de preços

Fontes utilizadas:
- [https://css.glass](https://css.glass)
- [https://getcssscan.com/css-glassmorphism](https://getcssscan.com/css-glassmorphism)

---

## Equipa

- **Marcelo Pinto** [@MarceloCostaOBJ](https://github.com/MarceloCostaOBJ)  
- **Carlos Miguel Castro** [@GandalfTheTech](https://github.com/GandalfTheTech)
