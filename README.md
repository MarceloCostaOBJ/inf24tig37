# EDUSPARK

Repository to host the project developed for 'some class', a fisrt year subject at SOMESCHOOL. Developed by Group ALPHA : [@MarceloCostaOBJ](https://github.com/MarceloCostaOBJ/), [add others].

## Short theme description

Este repositório documenta o desenvolvimento do projeto Eduspark, uma simulação de plataforma educativa interativa. O objetivo principal foi criar um conjunto de páginas web informativas com design moderno, funcionalidades básicas de navegação e estrutura organizada.

## Repository organization

Para ajudar o leitor a navegar, explicamos como o projeto está estruturado:
* **Build** is in the [src folder](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Build).
* Report chapters are in [doc folder](doc/).

## Gallery 

 [Galley](https://github.com/MarceloCostaOBJ/inf24tig37/tree/main/Gallery) 

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

- [Sketch da página Home](LINK_PARA_SKETCH_HOME)
- [Sketch da página About](LINK_PARA_SKETCH_ABOUT)
- [Sketch da página Prices](LINK_PARA_SKETCH_PRICES)
- [Sketch da página FAQ](LINK_PARA_SKETCH_FAQ)
- [Sitemap completo do projeto](LINK_PARA_SITEMAP)

### Galeria do Resultado Final
A galeria com capturas das páginas finais encontra-se disponível neste link:

- [Galeria de Capturas](LINK_PARA_GALERIA_FINAL)

### Ilustrações
As ilustrações utilizadas na secção inicial e em algumas áreas visuais do site foram retiradas da plataforma gratuita:  
🎨 [https://illustrationkit.com/](https://illustrationkit.com/)

### Repositório GitHub
O código-fonte do projeto encontra-se disponível em:  
🔗 [https://github.com/infYYtigXX](https://github.com/infYYtigXX)

---

## 3. Product – Produto

### Ligação para o Site no Netlify
O site encontra-se online em:  
🔗 [https://NOME_DO_SITE.netlify.app](https://NOME_DO_SITE.netlify.app)

### Instalação e Configuração

**Local:**
1. Fazer download dos ficheiros HTML, CSS e imagens.
2. Abrir o ficheiro `index.html` num browser moderno.

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

#### Resultado da validação CSS:
Não foram detetados **erros críticos**, apenas alguns **alertas**:

- ⚠️ **Linhas 24 e 36**: Uso de variáveis CSS (`--variavel`) que não são estaticamente verificadas.
  - ✅ Pode ser ignorado com segurança.

- ⚠️ **Linha 80**: Uso da propriedade `-webkit-backdrop-filter` (própria de navegadores WebKit).
  - ✅ Também pode ser ignorado. Tem suporte nos browsers modernos.

✅ **Conclusão**: O CSS está funcional, moderno e pronto para publicação.

### Cumprimento dos Requisitos

- ✅ 5 páginas HTML5 com marcação semântica (`section`, `article`, `nav`, `footer`, `figure`, `main`, etc.)
- ✅ CSS3 externo com:
  - ✅ seletores tipo, ID, classe, pseudo-classe (`:hover`, `:focus`) e atributo
  - ✅ pseudo-elementos (`::after`) e combinadores
  - ✅ fundo com imagem (`Back_MainTOTAL.jpg`) e cores
  - ✅ lista formatada, botão com `hover`, flutuação e posicionamento
  - ✅ responsividade via `@media` (mobile e desktop)
  - ✅ animações: `float`, `pulse-border`, `hover transform`
  - ✅ esconder elemento: `display: none` em media query (mobile)
  - ✅ substituição de texto por imagem: ex. avatar nos testemunhos
- ✅ Imagens com `img`, `figure` e `figcaption`
- ✅ Lista aninhada (`FAQ`)
- ✅ Destaque com `em`, `strong`, `mark` e CSS
- ✅ Tabela com `thead`, `tbody`, `tfoot`, `rowspan`, `colspan` (em `faq.html`)
- ✅ Formulário com campos obrigatórios (`signup.html`)
- ✅ Ligação para download de XML (`prices.html`)
- ✅ Documento XML + XSD (validado)

---

## 4. Efeito Visual de Glassmorphism com AI

Para simular o efeito visual conhecido como **glassmorphism** (vidro desfocado), recorremos a ferramentas de design com suporte a **inteligência artificial (AI)** que nos ajudaram a gerar rapidamente o código CSS necessário, com base em boas práticas modernas de UI.

O estilo foi inspirado em sistemas de design como o **Fluent Design da Microsoft**, **macOS Big Sur** e várias bibliotecas LLMS (Low-Level Modern Styling).

A geração do estilo foi realizada com apoio de ferramentas como:

- https://css.glass  
- https://getcssscan.com/css-glassmorphism

O código resultante foi aplicado a elementos como o **cabeçalho fixo** (`.modern-header`), o **painel de estatísticas** (`about.html`) e os **cartões de testemunhos**.

```css
backdrop-filter: blur(10px);
-webkit-backdrop-filter: blur(10px);
background-color: rgba(255, 255, 255, 0.1);


## Team
* Marcelo Pinto [@@MarceloCostaOBJ](https://github.com/MarceloCostaOBJ/))
* Other team members
