# EDUSPARK

Developed by Group inf24tig37 : [@MarceloCostaOBJ](https://github.com/MarceloCostaOBJ/), [@GandalfTheTech](https://github.com/GandalfTheTech) AKA Carlos Miguel Castro 

## Short theme description

Este repositório documenta o desenvolvimento do projeto Eduspark, uma simulação de plataforma educativa interativa. O objetivo principal foi criar um conjunto de páginas web informativas com design moderno, funcionalidades básicas de navegação e estrutura organizada.

## Repository organization

Para ajudar o leitor a navegar, explicamos como o projeto está estruturado:
* **Build** is in the [src folder](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Build).

## Gallery 

 [Galley](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Gallery/) 

## Technologies

_Indicate the technologies you have used in this assignment. Please provide links for the user to read more about those technologies._
* XML
* HTML5 + CSS3

# Relatório do Projeto: EDUSPARK

## 1. Project Presentation – Apresentação do Projeto

### Tema
Este projeto foi desenvolvido no âmbito da unidade curricular de Tecnologias Web, com o objetivo de criar um site educativo com base em HTML5, CSS3 e, opcionalmente, JavaScript.

### Proposta
Criámos um site chamado **EDUSPARK**, dedicado à promoção de cursos online de inglês, acessível e moderno, composto por cinco páginas estáticas: Home, About, Prices, FAQ e Sign Up.

### Estrutura do Site
O site inclui:
- Um cabeçalho fixo comum a todas as páginas;
- Layout responsivo com estilos modernos e uso de `flexbox`;
- Imagens, tabelas, listas aninhadas, e textos destacados;
- Formulário funcional (com validações `required`);
- Link para download de um documento XML com os planos de subscrição.

### Justificação das Tecnologias
Optámos por **não incluir JavaScript** para manipulação dinâmica do DOM, focando na implementação completa de todos os **requisitos mínimos** com animações CSS3 e semântica HTML5.

### Animações CSS3 Utilizadas
- `@keyframes float`: aplicado às imagens na `index.html` e nos testemunhos na `about.html`;
- `hover + transform + scale`: aplicado nas `pricing cards` na `prices.html`;
- `pulse-border`: aplicado ao painel de estatísticas na `about.html`.

---

## 2. User Interface – Interface com o Utilizador

### Sketches e Wireframes
Durante a fase de planeamento, desenvolvemos os sketches e o sitemap da aplicação, que serviram de base à construção da interface final. As imagens encontram-se organizadas numa galeria e estão disponíveis nos seguintes ficheiros:

- [Sketch da páginas Home](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Gallery/SKETCH)

### Galeria do Resultado Final
A galeria com capturas das páginas finais encontra-se disponível neste link:

- [Galeria de Capturas](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Gallery/Print)

### Ilustrações
As ilustrações utilizadas na secção inicial e em algumas áreas visuais do site foram retiradas da plataforma gratuita:  
🎨 [https://illustrationkit.com/](https://illustrationkit.com/)

### Repositório GitHub
O código-fonte do projeto encontra-se disponível em:  
🔗 [https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Build](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Build)

---

## 3. Product – Produto

### Ligação para o Site no Netlify
O site encontra-se online em:  
🔗 [https://inf24tig37.netlify.app/](https://inf24tig37.netlify.app/)

### Instalação e Configuração

**Netlify:**
A publicação foi realizada através de **upload manual de ficheiros**, dado que a integração com o GitHub apresentou falhas.

### Regras de Utilização
O site é estático e não requer autenticação nem registo. Está disponível publicamente sem limitações de acesso.

### Ajuda à Navegação
- O **menu de navegação** está presente em todas as páginas, com efeito visual hover.
- Está fixo no topo com estilo `glassmorphism`, garantindo navegação intuitiva.
- Os botões têm destaque visual com `hover` e `box-shadow`.

### Validação de Formulários
- O formulário de inscrição (`signup.html`) utiliza o atributo `required` para todos os campos (`first-name`, `last-name`, `email`).
- Os tipos de campo (`type="email"`) garantem validação automática nos browsers modernos.
- Recorremos ao serviço **Formspree** para processar os envios do formulário e recolher todos os endereços de email submetidos pelos utilizadores.
- Foi também configurado um **redirecionamento para uma página de agradecimento (obrigado.html)** e uma opção de resposta automática.

### Validação HTML e CSS
Foram utilizados os validadores da W3C:

- [W3C HTML Validator](https://validator.w3.org/)
- [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)

#### Resultado da validação HTML:
Não foram detetados **erros**.

#### Resultado da validação CSS:
Não foram detetados **erros críticos**, apenas alguns **alertas**:

- ⚠️ **Linhas 24 e 36**: Uso de variáveis CSS (`--variavel`) que não são estaticamente verificadas.
  - ✅ Pode ser ignorado com segurança.

- ⚠️ **Linha 80**: Uso da propriedade `-webkit-backdrop-filter` (própria de navegadores WebKit).
  - ✅ Também pode ser ignorado. Tem suporte nos browsers modernos.

✅ **Conclusão**: O CSS está funcional, moderno e pronto para publicação.

### Cumprimento dos Requisitos

- ✅ 5 páginas HTML5 com marcação semântica (`section`, `article`, `nav`, `footer`, `figure`, `main`, etc.)
- 
- ✅ CSS3 externo com:

- ## Cumprimento dos Requisitos – Explicação Técnica Detalhada (PT-PT)

### ✅ 2. CSS3 com seletores de tipo, ID, classe, pseudo-classe (`:hover`, `:focus`) e atributo

- **Ficheiro:** `StyleSignup.css`  
- **Linhas:** 92–98 e 106–108  
- **Código:**  
```css
.formulario-left input {
  font-family: 'Arial', sans-serif; 
  padding: 0.75rem; 
  font-size: 1rem; 
  border-radius: 1rem; 
  border: 6px solid #fff; 
  outline: none; 
  background-color: #ffffff; 
}
.formulario-left input:focus {
  border-color: #7c3aed; 
  box-shadow: 0 0 5px #7c3aed; 
}
```
- **Explicação:**  
Este bloco mostra o uso de seletores de **classe** (formulario-left), **tipo** (input) e **pseudo-classe** `:focus`. Quando o utilizador clica no campo de input, este muda de cor e aplica uma sombra, destacando-o visualmente e melhorando a experiência de preenchimento.

---

### ✅ 3. Pseudo-elementos (`::after`) e combinadores

- **Ficheiro:** `StyleAbout.css`  
- **Linhas:** 97–101  
- **Código:**  
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
Este pseudo-elemento `::after` adiciona uma barra animada de sublinhado nos links de navegação. A linha cresce suavemente ao passar o rato, criando um efeito visual elegante. É também um exemplo de **combinador**: `.nav-links a`.

---

### ✅ 4. Fundo com imagem (`Back_MainTOTAL.jpg`) e cores

- **Ficheiro:** `StyleIndex.css`  
- **Linha:** 30  
- **Código:**  
```css
body.about-page {
  background: url('Back_MainTOTAL.jpg') no-repeat center/cover;
  background-attachment: fixed;
  font-family: 'Montserrat', sans-serif;
  color: #111827;
  line-height: 1.6;
}
```
- **Explicação:**  
Este estilo aplica uma **imagem de fundo** fixa que cobre todo o ecrã (`cover`) e mantém-se estática durante o scroll. O visual é enriquecido com fonte personalizada e cor escura para o texto.

---

### ✅ 5. Lista formatada, botão com `hover`, flutuação e posicionamento

- **Ficheiro:** `StyleIndex.css`  
- **Linhas:** 123–125 (imagem), 141–147 (botão)  
- **Código:**  
```css
.hero-illustration img {
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0%   { transform: translateY(0); }
  50%  { transform: translateY(-10px); }
  100% { transform: translateY(0); }
}

.btn:hover {
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}
```
- **Explicação:**  
A imagem flutua suavemente com a animação `float`, dando um toque dinâmico à secção principal. O botão `.btn` ganha uma sombra ao passar o rato (`:hover`), destacando-se na página. Estes efeitos melhoram a estética e a interatividade do site.

---

### ✅ 6. Responsividade com `@media` (versão mobile e desktop)

- **Ficheiro:** `StyleAbout.css`  
- **Linhas:** 102–114  
- **Código:**  
```css
@media (max-width: 768px) {
  .header-inner {
    flex-direction: column;
    align-items: center;
  }

  .nav-area {
    width: 100%;
    overflow-x: auto;
  }
}
```
- **Explicação:**  
Através da `@media query`, o layout adapta-se automaticamente para dispositivos com ecrã mais pequeno (até 768px), tornando o cabeçalho vertical e garantindo boa usabilidade em smartphones e tablets.

---

### ✅ 7. Animações: `float`, `pulse-border`, `hover transform`

- **Ficheiro:** `StyleAbout.css`  
- **Linhas:** 194–207 e 246–248  
- **Código:**  
```css
@keyframes pulse-border {
  0% { box-shadow: 0 0 12px rgba(124, 58, 237, 0.3), inset 0 0 8px rgba(124, 58, 237, 0.05); }
  50% { box-shadow: 0 0 20px rgba(124, 58, 237, 0.2), inset 0 0 14px rgba(124, 58, 237, 0.1); }
  100% { box-shadow: 0 0 12px rgba(124, 58, 237, 0.3), inset 0 0 8px rgba(124, 58, 237, 0.05); }
}

.stat-card:hover {
  transform: translateY(-5px);
}
```
- **Explicação:**  
A animação `pulse-border` faz o contorno do painel de estatísticas "vibrar", como se estivesse a pulsar. Já o `:hover` nas `.stat-card` desloca o cartão para cima, criando um efeito moderno e intuitivo ao utilizador.

---

  - ✅ seletores tipo, ID, classe, pseudo-classe (`:hover`, `:focus`) e atributo
  - 
  - ✅ pseudo-elementos (`::after`) e combinadores
  - 
  - ✅ fundo com imagem (`Back_MainTOTAL.jpg`) e cores
  - 
  - ✅ lista formatada, botão com `hover`, flutuação e posicionamento
  - 
  - ✅ responsividade via `@media` (mobile e desktop)
  - 
  - ✅ animações: `float`, `pulse-border`, `hover transform`
  - 
  - ✅ esconder elemento: `display: none` em media query (mobile)
  - 
  - ✅ substituição de texto por imagem: ex. avatar nos testemunhos
- ✅ Imagens com `img`, `figure` e `figcaption`
- 
- ✅ Lista aninhada (`FAQ`)
- 
- ✅ Destaque com `em`, `strong`, `mark` e CSS
- 
- ✅ Tabela com `thead`, `tbody`, `tfoot`, `rowspan`, `colspan` (em `faq.html`)
- 
- ✅ Formulário com campos obrigatórios (`signup.html`)
- 
- ✅ Ligação para download de XML (`prices.html`)
- 
- ✅ Documento XML + XSD (validado)

---

Efeito Visual de Glassmorphism com AI

Para simular o efeito visual conhecido como **glassmorphism** (vidro desfocado), recorremos a ferramentas de design com suporte a **inteligência artificial (AI)** que nos ajudaram a gerar rapidamente o código CSS necessário, com base em boas práticas modernas de UI.

O estilo foi inspirado em sistemas de design como o **Fluent Design da Microsoft**, **macOS Big Sur** e várias bibliotecas LLMS (Low-Level Modern Styling).

A geração do estilo foi realizada com apoio de ferramentas como:

- https://css.glass  
- https://getcssscan.com/css-glassmorphism

O código resultante foi aplicado a elementos como o **cabeçalho fixo** (`.modern-header`), o **painel de estatísticas** (`about.html`) e os **cartões de testemunhos**.
Além disso, para a implementação das **animações em CSS** e do sistema de **envio de emails via Formspree**, também foram consultadas fontes online para assegurar a correta integração e compatibilidade com navegadores modernos.

## Team
* Marcelo Pinto [@@MarceloCostaOBJ](https://github.com/MarceloCostaOBJ)
* Carlos Miguel Castro [@GandalfTheTech](https://github.com/GandalfTheTech) 

