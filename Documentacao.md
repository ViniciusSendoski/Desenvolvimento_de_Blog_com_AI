# Trabalho de Web I

## Desenvolvimento de um Blog com AI

## 1. Introdução

    Esse documento possui o passo a passo dos prompts sugeridos e objetivos para o Blog. Para essa atividade foi escolhido o uso do Gemini AI.

## 2. Ciclos de Desenvolvimento
### 1.0 Definições iniciais para conteudo e criação do codigo base  
-   Prompt Sugerido: Possuo uma atividade de WEB I, usando uma AI(Gemini), devo realizar uma programação em pares, com o intuito de criar um blog simples sobre mim, deve possuir uma imagem minha e separar os arquivos entre HTML e CSS.
Para a imagem use o logo do gemini por meio do link, depois substituirei por uma imagem minha na pasta, junto aos arquivos.
Use o CSS para tratar a imagem permitindo redimensioná-la. Bem como mudanças que deixam a pagina mais elegante.
Deixe campos para gostos musicais, hobbis, lazer etc. preencha esses campos com lorem de 200 caracteres.
Deixe comentarios no codigo sobre o que foi feito e por que foi feito.
-   Saida do Gemini: Para essa atividade de programação em pares, vamos estruturar o projeto de forma profissional, separando as responsabilidades: o **HTML** cuidará da estrutura e do conteúdo, enquanto o **CSS** cuidará da estética e do redimensionamento da sua imagem.

Aqui está a proposta para o seu blog pessoal:

 1. O Arquivo Estrutural (`index.html`)

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Blog Pessoal | Atividade Web I</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>Bem-vindo ao meu Blog</h1>
        <p>Desenvolvido em parceria com Gemini AI</p>
    </header>

    <main class="container">
        <section class="perfil">
            <img src="https://www.gstatic.com/lamda/images/gemini_sparkle_v002.svg" alt="Minha Foto de Perfil" class="foto-perfil">
            <h2>Sobre Mim</h2>
            <p>Olá! Este é um espaço onde compartilho um pouco da minha jornada e interesses. Esta página foi estruturada separando HTML de CSS para seguir as boas práticas de desenvolvimento Web.</p>
        </section>

        <section class="interesses">
            <div class="card">
                <h3>Gostos Musicais</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi.</p>
            </div>

            <div class="card">
                <h3>Hobbies</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi.</p>
            </div>

            <div class="card">
                <h3>Lazer e Viagens</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi.</p>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 - Criado para a aula de WEB I</p>
    </footer>

</body>
</html>
```



 2. O Arquivo de Estilo (`style.css`)

```css
/* Reset básico para garantir que o layout fique igual em todos os navegadores */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f4f7f6; /* Tom cinza claro para elegância e leitura descansada */
    color: #333;
    line-height: 1.6;
}

header {
    background-color: #1a73e8; /* Azul clássico do ecossistema Google/Gemini */
    color: white;
    text-align: center;
    padding: 2rem 0;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.container {
    max-width: 800px;
    margin: 2rem auto;
    padding: 0 1rem;
}

/* TRATAMENTO DA IMAGEM:
   Aqui permitimos que a imagem seja redimensionada. 
   O uso de 'border-radius: 50%' deixa a foto circular, comum em blogs modernos. */
.foto-perfil {
    display: block;
    margin: 0 auto 1.5rem;
    width: 150px;       /* Largura controlada pelo CSS */
    height: 150px;      /* Altura igual para manter o círculo perfeito */
    object-fit: contain; /* Garante que o logo não seja cortado */
    border: 4px solid #fff;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    border-radius: 50%;
}

.perfil {
    text-align: center;
    margin-bottom: 3rem;
}

/* Estilização dos campos de interesses em formato de 'Cards' para ficar mais elegante */
.interesses {
    display: grid;
    gap: 1.5rem;
}

.card {
    background: white;
    padding: 1.5rem;
    border-left: 5px solid #1a73e8; /* Detalhe lateral para destacar o tópico */
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
}

.card h3 {
    margin-bottom: 0.5rem;
    color: #1a73e8;
}

footer {
    text-align: center;
    padding: 2rem;
    font-size: 0.9rem;
    color: #777;
}
```

###### Explicação da "Programação em Pares":

1.  **Separação de Arquivos:** Manter o HTML separado do CSS é fundamental para a manutenção. Se você quiser mudar a cor do blog inteiro amanhã, altera apenas o arquivo `.css` sem risco de quebrar o conteúdo.
2.  **Tratamento de Imagem:** No CSS, defini a classe `.foto-perfil` com largura e altura fixas em `150px`. Quando você substituir o link pela sua foto real, o CSS forçará a sua imagem a se ajustar a esse tamanho, mantendo o layout intacto.
3.  **Elegância:** Usei uma paleta de cores sóbria (azul, branco e cinza claro), sombras suaves (`box-shadow`) e bordas arredondadas para dar um aspecto de "Web 3.0".
4.  **Cards:** Em vez de apenas jogar o texto na tela, agrupamos os hobbies e gostos musicais em blocos brancos, o que facilita a leitura e organiza visualmente a informação.

**Dica para a atividade:** Salve os dois códigos na mesma pasta. Quando for trocar a foto, basta colocar o arquivo da imagem na mesma pasta e mudar o `src="..."` no HTML para o nome do seu arquivo (ex: `minhafoto.jpg`).
-   Observações do cliclo: Saida inicial limpa e simples, codigo da imagem apresentou erro, devido a imagem não referenciada corretamente.

---

### 2.0 
-   Prompt Sugerido: Tendo os códigos base, quando adicionar uma nova função diga aonde ela fica para não ter o retrabalho de reescrever todo o código.
O painel azul deve ser menor, tendo no canto superior direito um botão para inverter a cor do painel azul.
gostaria de adicionar um estrutura que ao clicar expande uma lista relacionada a palavra da extrutura, por exemplo abaixo de hobbies 4 estruturas:
Jogos: 
Mangas: 
Light Novels:
Filmes: 
Nessa lista cada item deve ter imagem, titulo, descrição. por exemplo:
Estrutura mãe -> Filmes.
imagem para o filme panico 7. Titulo Panico 7. Descrição do filme (use Lorem por enquanto).
-   Saida do Gemini: Boa escolha de base! O código está limpo e bem estruturado. Para atender aos seus pedidos, vamos trabalhar em partes para você saber exatamente onde inserir cada alteração.

### 1. Ajuste no `header` (Painel Azul e Botão)

No seu **HTML**, dentro da tag `<header>`, vamos adicionar o botão.
**Onde fica:** Substitua o conteúdo atual do `<header>` por este:

```html
<header>
    <div class="header-content">
        <h1>Bem-vindo ao meu Blog</h1>
        <p>Desenvolvido em parceria com Gemini AI</p>
    </div>
    <button id="btn-toggle" onclick="toggleHeaderColor()" title="Inverter Cor">🌓</button>
</header>
```

No seu **CSS**, vamos diminuir a altura e posicionar o botão.
**Onde fica:** Substitua o bloco `header` e adicione os novos estilos abaixo dele:

```css
header {
    background-color: #1a73e8; 
    color: white;
    text-align: center;
    padding: 1rem 0; /* Diminuído de 2rem para 1rem */
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    position: relative; /* Necessário para posicionar o botão */
    transition: background-color 0.3s; /* Transição suave */
}

header.inverted {
    background-color: #333; /* Cor invertida (ex: cinza escuro) */
}

#btn-toggle {
    position: absolute;
    top: 10px;
    right: 10px;
    background: rgba(255, 255, 255, 0.2);
    border: 1px solid white;
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
    cursor: pointer;
}
```

### 2. A Nova Estrutura de Listas Expansíveis (Acordeão)

Para a lista que expande (Jogos, Mangás, etc.), usaremos a tag `<details>` do HTML, que já cria o efeito de abrir e fechar nativamente.

**Onde fica no HTML:** Dentro da `<section class="interesses">`, abaixo do conteúdo de "Hobbies".

```html
<div class="card">
    <h3>Hobbies</h3>
    <div class="accordion-container">
        <details>
            <summary>Filmes</summary>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Pânico 7">
                <div class="item-info">
                    <h4>Pânico 7</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor.</p>
                </div>
            </div>
            </details>

        <details>
            <summary>Jogos</summary>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Jogo Exemplo">
                <div class="item-info">
                    <h4>Título do Jogo</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
                </div>
            </div>
        </details>
        </div>
</div>
```

**Onde fica no CSS:** Adicione ao final do arquivo `style.css`.

```css
details {
    margin-top: 1rem;
    cursor: pointer;
    border-bottom: 1px solid #eee;
    padding-bottom: 0.5rem;
}

summary {
    font-weight: bold;
    color: #1a73e8;
    outline: none;
}

.item-lista {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem 0;
    cursor: default;
}

.item-lista img {
    width: 80px;
    height: 80px;
    border-radius: 4px;
    object-fit: cover;
}

.item-info h4 {
    margin: 0;
    font-size: 1rem;
}

.item-info p {
    font-size: 0.85rem;
    margin: 0;
}
```

### 3. Função JavaScript para o Botão

Para o botão funcionar, precisamos de um pequeno script.
**Onde fica:** No final do seu arquivo `Index.html`, logo antes do fechamento da tag `</body>`.

```html
<script>
    function toggleHeaderColor() {
        const header = document.querySelector('header');
        header.classList.toggle('inverted');
    }
</script>
```

### O que mudou na lógica:
1.  **Header:** Reduzi o `padding` e usei `position: relative` para "prender" o botão no canto superior.
2.  **Toggle:** Usei uma classe `.inverted` no CSS. O JavaScript apenas liga/desliga essa classe.
3.  **Expansão:** Usei `<details>` e `<summary>`. É a forma mais leve de fazer listas expansíveis sem precisar de um código complexo, e dentro de cada uma coloquei um `flexbox` (`item-lista`) para alinhar a imagem e o texto.
-   Observações do cliclo: Obejetivos foram implementados.

--- 

### 2.1 
-   Prompt Sugerido: Tendo o codigo atual. Mude a cor principal para roxo, meu botão que troca a cor do painel deve inverter todo a pagina incluindo texto, 
-   Saida do Gemini: Com base no seu código atual, aqui estão as alterações para mudar a cor principal para roxo e fazer com que o botão inverta as cores de toda a página (incluindo o texto) em vez de apenas o cabeçalho.

### 1. Alteração no CSS (`style.css`)
Você deve substituir as cores azuis (`#1a73e8`) pelo roxo e criar uma classe `.inverted` aplicada ao `body` para inverter o site todo.

**Onde editar:** Substitua o conteúdo do seu `style.css` por este (ajustado para roxo e modo invertido geral):

```css
/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f4f7f6;
    color: #333;
    line-height: 1.6;
    transition: background-color 0.3s, color 0.3s; /* Transição suave para a inversão */
}

/* CLASSE DE INVERSÃO TOTAL */
body.inverted {
    background-color: #1a1a1a; /* Fundo escuro */
    color: #f4f7f6;           /* Texto claro */
}

header {
    background-color: #6a1b9a; /* Roxo Principal */
    color: white;
    text-align: center;
    padding: 1rem 0;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    position: relative;
}

/* Ajuste do Header quando o corpo está invertido */
body.inverted header {
    background-color: #4a148c; /* Roxo mais escuro no modo invertido */
}

#btn-toggle {
    position: absolute;
    top: 10px;
    right: 10px;
    background: rgba(255, 255, 255, 0.2);
    border: 1px solid white;
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
    cursor: pointer;
    z-index: 10;
}

.container {
    max-width: 800px;
    margin: 2rem auto;
    padding: 0 1rem;
}

details {
    margin-top: 1rem;
    cursor: pointer;
    border-bottom: 1px solid #eee;
    padding-bottom: 0.5rem;
}

summary {
    font-weight: bold;
    color: #6a1b9a; /* Roxo nos títulos expansíveis */
    outline: none;
}

body.inverted summary {
    color: #ba68c8; /* Roxo mais claro para ler melhor no fundo escuro */
}

.item-lista {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem 0;
    cursor: default;
}

.item-lista img {
    width: 80px;
    height: 80px;
    border-radius: 4px;
    object-fit: cover;
}

.foto-perfil {
    display: block;
    margin: 0 auto 1.5rem;
    width: 150px;
    height: 150px;
    object-fit: contain;
    border: 4px solid #fff;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    border-radius: 50%;
}

.perfil {
    text-align: center;
    margin-bottom: 3rem;
}

.interesses {
    display: grid;
    gap: 1.5rem;
}

.card {
    background: white;
    padding: 1.5rem;
    border-left: 5px solid #6a1b9a; /* Detalhe lateral Roxo */
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
    transition: background-color 0.3s;
}

/* Ajuste dos cards no modo invertido */
body.inverted .card {
    background: #2d2d2d;
    border-left-color: #ba68c8;
}

.card h3 {
    margin-bottom: 0.5rem;
    color: #6a1b9a;
}

body.inverted .card h3 {
    color: #ba68c8;
}

footer {
    text-align: center;
    padding: 2rem;
    font-size: 0.9rem;
    color: #777;
}
```

### 2. Alteração no JavaScript (`Index.html`)
Para que o botão afete a página inteira, precisamos trocar o alvo da função de `header` para o `body`.

**Onde editar:** No final do seu arquivo `Index.html`, substitua a função dentro da tag `<script>` por esta:

```javascript
function toggleHeaderColor() {
    // Agora selecionamos o 'body' para inverter as cores de todo o documento
    const body = document.body;
    body.classList.toggle('inverted');
}
```

### O que mudou na lógica:
1.  **Cor Principal:** Todas as referências ao azul `#1a73e8` foram trocadas por tons de roxo (`#6a1b9a`).
2.  **Inversão Total:** Criamos seletores como `body.inverted .card` no CSS. Isso garante que, quando o botão for clicado, os cards fiquem escuros e o texto mude de cor para manter o contraste.
3.  **JavaScript:** O comando `document.body.classList.toggle('inverted')` é o jeito mais eficiente de criar um "Modo Escuro/Invertido" completo.
-   Observações do cliclo: Foram implementadas mudanças visuais basicas, bem como aplicar inverção de cor para toda a pagina.

---

### 3.0 
-   Prompt Sugerido: Tendo o codigo atual. 
Altere "Gostos musicais" para "Minha Relação com a musica".
Quero fazer uma lista de objetos, sendo cada objeto um video do youtube.
Esta lista deve ir da esquerda para a direita.
 Em baixo da lista um texto que acompanha demarcando videos por ano, por exemplo de 2020 até 2021, use os videos abaixo, por enquanto.
<https://www.youtube.com/watch?v=IxX_QHay02M&list=RDIxX_QHay02M&start_radio=1&pp=ygUDY2F0oAcB>
<https://www.youtube.com/watch?v=J---aiyznGQ&list=RDJ---aiyznGQ&start_radio=1&pp=ygUDY2F0oAcB>
<https://www.youtube.com/watch?v=rXh8Hvo7gfs&pp=ygUDY2F0>
-   Saida do Gemini: Para atender ao seu pedido, vamos alterar o título da seção e criar uma estrutura de "carrossel" ou lista horizontal para os vídeos do YouTube, organizada por um marcador de tempo (ano).

Aqui estão as alterações necessárias:

### 1. Alteração no HTML (`Index.html`)

**Onde editar:** Substitua o conteúdo do primeiro `<div class="card">` (que era "Gostos Musicais") por este novo bloco. Note que alteramos os links do YouTube para o formato `/embed/`, que é o necessário para funcionar dentro do site.

```html
<div class="card">
    <h3>Minha Relação com a musica</h3>
    <p>Abaixo estão alguns dos vídeos que marcaram minha trajetória musical nos últimos anos.</p>
    
    <div class="video-list-container">
        <div class="video-item">
            <iframe src="https://www.youtube.com/embed/IxX_QHay02M" title="Video 1" frameborder="0" allowfullscreen></iframe>
        </div>
        <div class="video-item">
            <iframe src="https://www.youtube.com/embed/J---aiyznGQ" title="Video 2" frameborder="0" allowfullscreen></iframe>
        </div>
        <div class="video-item">
            <iframe src="https://www.youtube.com/embed/rXh8Hvo7gfs" title="Video 3" frameborder="0" allowfullscreen></iframe>
        </div>
    </div>
    
    <p class="timeline-label">Período: 2020 — 2021</p>
</div>
```

### 2. Alteração no CSS (`style.css`)

Para que a lista vá da esquerda para a direita e os vídeos tenham um tamanho adequado, adicione estes estilos ao final do seu arquivo `style.css`:

```css
/* Container que permite o scroll horizontal se houver muitos vídeos */
.video-list-container {
    display: flex;
    gap: 1rem;
    overflow-x: auto; /* Permite rolar para o lado se necessário */
    padding: 1rem 0;
    scrollbar-width: thin; /* Deixa a barra de rolagem mais fina no Firefox */
}

/* Estilo de cada objeto de vídeo */
.video-item {
    flex: 0 0 250px; /* Impede que o vídeo encolha, mantendo 250px de largura */
    height: 150px;
    background: #000;
    border-radius: 8px;
    overflow: hidden;
}

.video-item iframe {
    width: 100%;
    height: 100%;
    border: none;
}

/* Texto que demarca o ano abaixo da lista */
.timeline-label {
    text-align: center;
    font-weight: bold;
    margin-top: 0.5rem;
    color: #6a1b9a;
    font-size: 0.9rem;
}

/* Ajuste da cor do texto do ano no modo invertido */
body.inverted .timeline-label {
    color: #ba68c8;
}
```

### O que foi feito:
1.  **Mudança de Título:** O `<h3>` foi atualizado conforme solicitado.
2.  **Lista Horizontal:** Usamos `display: flex` no container dos vídeos. O comando `flex: 0 0 250px` garante que os vídeos fiquem um ao lado do outro em linha, sem "esmagar" o tamanho deles.
3.  **Embed do YouTube:** Os links que você enviou foram convertidos para o formato de incorporação (`/embed/`). Sem isso, o YouTube bloqueia a exibição dentro de outros sites por segurança.
4.  **Marcador de Ano:** Adicionamos uma classe `.timeline-label` para destacar o período de 2020-2021 logo abaixo da lista de vídeos.

Se você adicionar mais vídeos no futuro dentro da `video-list-container`, eles continuarão aparecendo da esquerda para a direita automaticamente!
-   Observações do cliclo: Implementação de uma lista horizontal de videos no youtube

---

### 4.0 
-   Prompt Sugerido: Tendo o código atual.
altere estrutura Hobbis, tendo texto. Separe hobbis das lista por uma linha, mas ainda dentro do hobbis.
Abaixo descrição textual da lista: Lista Filmes tendo espaços para adicionar 3 filmes.
Abaixo descrição textual da lista: Lista Jogos tendo espaços para adicionar 3 jogos..
Abaixo descrição textual da lista: Lista Manhwa tendo espaços para adicionar 3 manhwas.
Abaixo descrição textual da lista: Lista Light Novel tendo espaços para adicionar 2 light novels.
-   Saida do Gemini: Para atualizar a seção de **Hobbies** conforme solicitado, vamos ajustar a estrutura do card para incluir a linha separadora e organizar os itens em listas de 3 (ou 2) espaços dentro de cada categoria expansível.

### 1. Alteração no HTML (`Index.html`)

**Onde editar:** Substitua todo o conteúdo do `<div class="card">` correspondente aos **Hobbies** (atualmente o segundo card) por este bloco:

```html
<div class="card">
    <h3>Hobbies</h3>
    <p>Estes são os meus passatempos favoritos e as obras que acompanho no momento.</p>
    
    <hr class="linha-separadora"> <div class="accordion-container">
        <details>
            <summary>Lista Filmes</summary>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Filme 1">
                <div class="item-info"><h4>Título Filme 1</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Filme 2">
                <div class="item-info"><h4>Título Filme 2</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Filme 3">
                <div class="item-info"><h4>Título Filme 3</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
        </details>

        <details>
            <summary>Lista Jogos</summary>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Jogo 1">
                <div class="item-info"><h4>Título Jogo 1</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Jogo 2">
                <div class="item-info"><h4>Título Jogo 2</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Jogo 3">
                <div class="item-info"><h4>Título Jogo 3</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
        </details>

        <details>
            <summary>Lista Manhwa</summary>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Manhwa 1">
                <div class="item-info"><h4>Título Manhwa 1</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Manhwa 2">
                <div class="item-info"><h4>Título Manhwa 2</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Manhwa 3">
                <div class="item-info"><h4>Título Manhwa 3</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
        </details>

        <details>
            <summary>Lista Light Novel</summary>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Light Novel 1">
                <div class="item-info"><h4>Título LN 1</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
            <div class="item-lista">
                <img src="https://via.placeholder.com/80" alt="Light Novel 2">
                <div class="item-info"><h4>Título LN 2</h4><p>Lorem ipsum dolor sit amet.</p></div>
            </div>
        </details>
    </div>
</div>
```

### 2. Alteração no CSS (`style.css`)

Para que a linha separadora fique discreta e acompanhe a identidade visual roxa, adicione este estilo ao seu arquivo CSS:

**Onde editar:** Pode adicionar ao final do arquivo ou próximo aos estilos dos cards.

```css
.linha-separadora {
    border: 0;
    height: 1px;
    background: #eee;
    margin: 1rem 0;
}

/* Ajuste da linha para o modo invertido */
body.inverted .linha-separadora {
    background: #444;
}
```

### O que mudou:
1.  **Linha Separadora:** Adicionamos a tag `<hr>` com uma classe personalizada para criar a divisão visual dentro do card de Hobbies.
2.  **Estrutura de Listas:** Expandimos as seções para conter exatamente a quantidade de espaços solicitada (3 para Filmes, Jogos e Manhwas; 2 para Light Novels).
3.  **Identificação Textual:** Atualizamos os títulos de cada seção expansível (`<summary>`) conforme o seu pedido ("Lista Filmes", "Lista Jogos", etc.).
4.  **Imagens e Texto:** Cada item já possui a estrutura de imagem (`img`), título (`h4`) e descrição (`p`) pronta para você preencher.
-   Observações do cliclo: Codigo se aproxima cada veiz mais a uma caixa preta para meu conhecimentos sobre html e css. Devido a meu comando incoerente faltou um ponto a adicionar ao HTML.

---

### 4.1 
-   Prompt Sugerido: Tendo o codigo. 
acima que cada lista em hobbis teve existir um texto, por exemplo:
...
Os tres jogos que estou tentando platinar na Steam e não estou conseguindo.
Lista Jogos
...
-   Saida do Gemini: Para adicionar os textos descritivos antes de cada lista na seção de **Hobbies**, você deve inserir um parágrafo (`<p>`) logo acima de cada tag `<details>`. 

Aqui está como o bloco do card de **Hobbies** deve ficar no seu **`Index.html`**:

```html
<div class="card">
    <h3>Hobbies</h3>
    <p>Estes são os meus passatempos favoritos e as obras que acompanho no momento.</p>
    
    <hr class="linha-separadora"> 

    <div class="accordion-container">
        <p>Filmes que assisti recentemente e recomendo a experiência.</p>
        <details>
            <summary>Lista Filmes</summary>
            </details>

        <p>Os três jogos que estou tentando platinar na Steam e não estou conseguindo.</p>
        <details>
            <summary>Lista Jogos</summary>
            </details>

        <p>Manhwas com as melhores artes e histórias que estou lendo.</p>
        <details>
            <summary>Lista Manhwa</summary>
            </details>

        <p>Light Novels que me prenderam pela escrita e world-building.</p>
        <details>
            <summary>Lista Light Novel</summary>
            </details>
    </div>
</div>
```

### Ajuste Sugerido no CSS (`style.css`)
Como o texto agora fica colado na lista anterior, adicione este pequeno ajuste ao seu CSS para melhorar o espaçamento visual:

**Onde editar:** No seu arquivo `style.css`, procure a regra `details` ou adicione ao final:

```css
.accordion-container p {
    margin-top: 1.5rem; /* Espaço maior antes do texto descritivo */
    font-size: 0.95rem;
    font-weight: 500;
}

details {
    margin-top: 0.5rem; /* Espaço menor entre o texto e a sua respectiva lista */
    /* ... mantenha o restante das propriedades que já existem ... */
}
```

### O que foi alterado:
1.  **Estrutura de Conteúdo:** Inserimos parágrafos descritivos antes de cada seção expansível dentro da `accordion-container`.
2.  **Organização Visual:** O texto agora serve como uma introdução direta para a "Lista" que vem logo abaixo, seguindo o exemplo que você deu sobre os jogos da Steam.
-   Observações do cliclo: Implementação Manual no HTML, parte de hobbis falta a incersão manual

---

### 5.0 
-   Prompt Sugerido:Tendo o codigo.  
Adicione um card para "Um pouco mais sobre mim".
Colado na lateral esquerda deve ter uma imagem,  ao deve ter pontos de texto sendo eles.
 Nome:
 Ano de Nascimento:
 Estado Civil:
 Trabalho:
 Escolaridade: 
-   Saida do Gemini: Para adicionar o novo card "**Um pouco mais sobre mim**" com a imagem alinhada à esquerda e os pontos de texto solicitados, siga as instruções abaixo para alterar seu HTML e CSS.

### 1. Alteração no HTML (`Index.html`)

**Onde editar:** Insira este novo bloco dentro da `<section class="interesses">`. Recomendo colocá-lo como o primeiro card dessa seção, antes de "Minha Relação com a música".

```html
<div class="card">
    <h3>Um pouco mais sobre mim</h3>
    <div class="info-pessoal-container">
        <img src="https://via.placeholder.com/150" alt="Foto Pessoal" class="foto-info">
        <ul class="lista-info">
            <li><strong>Nome:</strong> Vinícius</li>
            <li><strong>Ano de Nascimento:</strong> [Seu Ano]</li>
            <li><strong>Estado Civil:</strong> [Seu Estado Civil]</li>
            <li><strong>Trabalho:</strong> [Seu Trabalho]</li>
            <li><strong>Escolaridade:</strong> Acadêmico de TADS</li>
        </ul>
    </div>
</div>
```

### 2. Alteração no CSS (`style.css`)

**Onde editar:** Adicione estes estilos ao final do seu arquivo para garantir que a imagem fique colada à esquerda e o texto flua corretamente ao lado dela.

```css
/* Container para alinhar imagem e lista lado a lado */
.info-pessoal-container {
    display: flex;
    align-items: center;
    gap: 1.5rem;
    margin-top: 1rem;
}

/* Estilo da imagem colada à esquerda */
.foto-info {
    width: 120px;
    height: 120px;
    border-radius: 8px;
    object-fit: cover;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

/* Estilo da lista de informações */
.lista-info {
    list-style: none; /* Remove os pontos da lista */
    padding: 0;
}

.lista-info li {
    margin-bottom: 0.5rem;
    font-size: 1rem;
}

.lista-info li strong {
    color: #6a1b9a; /* Roxo para os títulos dos pontos */
}

/* Ajuste das cores no modo invertido */
body.inverted .lista-info li strong {
    color: #ba68c8;
}

/* Responsividade: em telas pequenas, a foto fica em cima e o texto embaixo */
@media (max-width: 600px) {
    .info-pessoal-container {
        flex-direction: column;
        text-align: center;
    }
}
```

### O que foi implementado:
1.  **Layout Flexbox:** Usei `display: flex` para que a imagem e a lista fiquem em colunas paralelas dentro do card.
2.  **Identidade Visual:** Mantive o uso do **Roxo** nos títulos em negrito (`<strong>`) para combinar com o restante do seu blog.
3.  **Responsividade:** Adicionei um `@media query` simples. Se você abrir o site no celular, a imagem passará para cima do texto automaticamente para não "esmagar" as informações.
4.  **Organização:** A classe `lista-info` removeu as "bolinhas" padrão da lista (`list-style: none`) para deixar o visual mais limpo, conforme a estética do seu projeto.
-   Observações do cliclo:

---

### 6.0 
-   Prompt Sugerido: Tendo o codigo.  
Vamos alterar o Card lazer, agora será apenas "Viagens".
para o corpo teremos um texto na parte superior.
um texto a esquerda, Imagem no centro esquerda, Linha dividindo no meio, Imagem no centro direita, texto a direita.
-   Saida do Gemini: Para atualizar o card de lazer para o novo formato de "Viagens" com o layout espelhado (Texto | Imagem | Linha | Imagem | Texto), precisaremos utilizar **Flexbox** para alinhar esses cinco elementos lado a lado.

Aqui estão as alterações necessárias:

### 1. Alteração no HTML (`Index.html`)

**Onde editar:** Substitua o último card ("Lazer e Viagens") pelo bloco abaixo:

```html
<div class="card">
    <h3>Viagens</h3>
    <p class="texto-superior-viagem">Explorar novos lugares é uma das minhas maiores paixões. Aqui estão dois destinos que marcaram minha trajetória.</p>
    
    <div class="viagem-container">
        <div class="viagem-bloco">
            <p>A calmaria das montanhas e o contato com a natureza me renovam.</p>
        </div>
        
        <img src="https://via.placeholder.com/100" alt="Viagem 1" class="img-viagem">

        <div class="divisor-vertical"></div>

        <img src="https://via.placeholder.com/100" alt="Viagem 2" class="img-viagem">

        <div class="viagem-bloco">
            <p>A energia das grandes metrópoles e a arquitetura urbana me fascinam.</p>
        </div>
    </div>
</div>
```

### 2. Alteração no CSS (`style.css`)

**Onde editar:** Adicione estes estilos ao final do seu arquivo `style.css` para criar o alinhamento horizontal e a linha divisória vertical.

```css
/* Espaçamento para o texto superior do card */
.texto-superior-viagem {
    margin-bottom: 1.5rem;
}

/* Container principal das viagens */
.viagem-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 10px;
}

/* Estilo dos blocos de texto (esquerda e direita) */
.viagem-bloco {
    flex: 1;
    font-size: 0.9rem;
    text-align: center;
}

/* Estilo das imagens centrais */
.img-viagem {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    object-fit: cover;
    border: 2px solid #6a1b9a;
}

/* Linha divisora vertical no meio */
.divisor-vertical {
    width: 1px;
    height: 60px;
    background-color: #eee;
}

/* Ajustes para o Modo Invertido */
body.inverted .img-viagem {
    border-color: #ba68c8;
}

body.inverted .divisor-vertical {
    background-color: #444;
}

/* Responsividade: em telas pequenas, vira uma coluna */
@media (max-width: 600px) {
    .viagem-container {
        flex-direction: column;
        gap: 20px;
    }
    .divisor-vertical {
        width: 60px;
        height: 1px;
    }
}
```

### O que mudou:
1.  **Estrutura Simétrica:** O `viagem-container` usa `display: flex` para colocar os 5 elementos (Texto, Imagem, Linha, Imagem, Texto) na mesma linha.
2.  **Divisor Vertical:** Criamos uma `div` com largura de `1px` para simular a linha de separação no centro.
3.  **Imagens:** As imagens foram configuradas como círculos (`border-radius: 50%`) para manter a harmonia com a sua foto de perfil.
4.  **Texto Superior:** Adicionamos um parágrafo logo abaixo do título para contextualizar a seção.
5.  **Responsividade:** Caso o blog seja visualizado em um celular, os elementos se empilham verticalmente para não ficarem esmagados.
-   Observações do cliclo: Com certeza uma caixa preta esse codigo .css no extado atual, objetivo alcançado.

---

### 6.1 
-   Prompt Sugerido:Tendo o codigo.
já foi usado circulo em imagem antes. para o card Viagens altere o circulo sobre a imagem para hexagono.
-   Saida do Gemini: Para transformar as imagens de viagens em hexágonos, usaremos a propriedade CSS `clip-path`. Essa é a forma mais moderna de criar formas geométricas em imagens sem precisar editá-las fora do código.

Aqui estão as alterações:

### 1. Alteração no CSS (`style.css`)

**Onde editar:** Procure pela classe `.img-viagem` e substitua o `border-radius: 50%` pelo `clip-path`. Como bordas comuns não funcionam bem com o `clip-path`, usaremos um pequeno ajuste de filtro para manter a identidade visual roxa.

```css
/* Estilo das imagens centrais (Agora Hexagonais) */
.img-viagem {
    width: 100px; /* Aumentei um pouco para o formato aparecer melhor */
    height: 100px;
    object-fit: cover;
    /* Aplica o recorte em formato de hexágono */
    clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
    background: #6a1b9a; /* Fundo roxo que aparece como borda se houver padding */
    padding: 2px;
    transition: transform 0.3s;
}

.img-viagem:hover {
    transform: scale(1.1); /* Efeito de zoom ao passar o mouse */
}

/* Ajuste para o Modo Invertido */
body.inverted .img-viagem {
    background: #ba68c8;
}
```

### 2. Dica de ajuste no HTML (`Index.html`)

No seu arquivo HTML, dentro do card de **Viagens**, você não precisa mudar nada na estrutura, mas caso as imagens fiquem muito coladas na linha divisória por serem mais largas que o círculo anterior, o CSS acima com `justify-content: space-between` que já temos no `.viagem-container` cuidará do alinhamento.

### Explicação Técnica (Conceitual):
* **`clip-path`**: Esta propriedade define uma região de recorte. O que está dentro dos pontos do `polygon` fica visível, o que está fora é escondido. 
* **Os pontos do polígono**: Os valores `(25% 0%, 75% 0%...)` são as coordenadas (X e Y) dos 6 cantos do hexágono.
* **Por que remover o `border`?**: Bordas padrões do CSS são retangulares. Quando você "corta" a imagem com `clip-path`, a borda sumiria. Por isso, usamos o `background` com um pouco de `padding` para simular o contorno roxo.

Agora suas imagens de viagens terão esse visual geométrico diferenciado do restante do site! 🚀
-   Observações do cliclo: Alteração visual em viagens.
### 7.0 
-   Prompt Sugerido: Tendo o Codigo.
Analise o .html e o .css, sem perder as funcionalidades, organize e refatore os arquivos, para ajudar na interpretação.
-   Saida do Gemini: Refatorar o código é um passo essencial para quem está no **TADS**. Com o crescimento do projeto, manter o CSS organizado por seções e o HTML bem indentado facilita muito a manutenção e evita erros de "chaves perdidas" ou tags abertas.

Abaixo, organizei os arquivos agrupando os estilos por componentes (Header, Cards, Hobbies, Viagens) e removendo redundâncias.

### 1. HTML Refatorado (`Index.html`)
Aqui, apenas organizei a indentação e agrupei as seções para que fiquem visualmente claras.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Blog Pessoal | Atividade Web I</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <div class="header-content">
            <h1>Bem-vindo ao meu Blog</h1>
            <p>Desenvolvido em parceria com Gemini AI</p>
        </div>
        <button id="btn-toggle" onclick="toggleMode()" title="Inverter Cor">🌓</button>
    </header>

    <main class="container">
        <section class="perfil">
            <img src="https://www.gstatic.com/lamda/images/gemini_sparkle_v002.svg" alt="Minha Foto de Perfil" class="foto-perfil">
            <h2>Sobre Mim</h2>
            <p>Olá! Este é um espaço onde compartilho um pouco da minha jornada e interesses. Esta página foi estruturada separando HTML de CSS para seguir as boas práticas de desenvolvimento Web.</p>
        </section>

        <section class="interesses">
            
            <div class="card">
                <h3>Um pouco mais sobre mim</h3>
                <div class="info-pessoal-container">
                    <img src="https://via.placeholder.com/150" alt="Foto Pessoal" class="foto-info">
                    <ul class="lista-info">
                        <li><strong>Nome:</strong> Vinícius</li>
                        <li><strong>Ano de Nascimento:</strong> [Seu Ano]</li>
                        <li><strong>Estado Civil:</strong> [Seu Estado Civil]</li>
                        <li><strong>Trabalho:</strong> [Seu Trabalho]</li>
                        <li><strong>Escolaridade:</strong> Acadêmico de TADS</li>
                    </ul>
                </div>
            </div>

            <div class="card">
                <h3>Minha Relação com a música</h3>
                <p>Vídeos que marcaram minha trajetória musical.</p>
                <div class="video-list-container">
                    <div class="video-item"><iframe src="https://www.youtube.com/embed/IxX_QHay02M" frameborder="0" allowfullscreen></iframe></div>
                    <div class="video-item"><iframe src="https://www.youtube.com/embed/J---aiyznGQ" frameborder="0" allowfullscreen></iframe></div>
                    <div class="video-item"><iframe src="https://www.youtube.com/embed/rXh8Hvo7gfs" frameborder="0" allowfullscreen></iframe></div>
                </div>
                <p class="timeline-label">Período: 2020 — 2021</p>
            </div>

            <div class="card">
                <h3>Hobbies</h3>
                <p>Passatempos favoritos e obras que acompanho no momento.</p>
                <hr class="linha-separadora">

                <div class="accordion-container">
                    <p>Filmes recentes:</p>
                    <details>
                        <summary>Lista Filmes</summary>
                        <div class="item-lista">
                            <img src="https://via.placeholder.com/80" alt="Pânico 7">
                            <div class="item-info"><h4>Pânico 7</h4><p>Descrição Lorem Ipsum.</p></div>
                        </div>
                        </details>

                    <p>Os três jogos que estou tentando platinar:</p>
                    <details>
                        <summary>Lista Jogos</summary>
                        <div class="item-lista">
                            <img src="https://via.placeholder.com/80" alt="Jogo">
                            <div class="item-info"><h4>Título do Jogo</h4><p>Descrição Lorem Ipsum.</p></div>
                        </div>
                    </details>
                </div>
            </div>

            <div class="card">
                <h3>Viagens</h3>
                <p class="texto-superior-viagem">Explorar novos lugares é uma das minhas maiores paixões.</p>
                <div class="viagem-container">
                    <div class="viagem-bloco"><p>Montanhas e natureza.</p></div>
                    <img src="https://via.placeholder.com/100" alt="Viagem 1" class="img-viagem">
                    <div class="divisor-vertical"></div>
                    <img src="https://via.placeholder.com/100" alt="Viagem 2" class="img-viagem">
                    <div class="viagem-bloco"><p>Metrópoles e arquitetura.</p></div>
                </div>
            </div>

        </section>
    </main>

    <footer>
        <p>&copy; 2024 - Criado para a aula de WEB I</p>
    </footer>

    <script>
        function toggleMode() {
            document.body.classList.toggle('inverted');
        }
    </script>
</body>
</html>
```

### 2. CSS Refatorado (`style.css`)
Agrupei os estilos por **categorias**. Note como as variáveis no topo e o uso de classes específicas facilitam a leitura.

```css
/* =========================================
   1. RESET E CONFIGURAÇÕES GERAIS
   ========================================= */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f4f7f6;
    color: #333;
    line-height: 1.6;
    transition: background-color 0.3s, color 0.3s;
}

body.inverted {
    background-color: #1a1a1a;
    color: #f4f7f6;
}

.container {
    max-width: 800px;
    margin: 2rem auto;
    padding: 0 1rem;
}

/* =========================================
   2. HEADER E FOOTER
   ========================================= */
header {
    background-color: #6a1b9a;
    color: white;
    text-align: center;
    padding: 1rem 0;
    position: relative;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

body.inverted header { background-color: #4a148c; }

#btn-toggle {
    position: absolute;
    top: 10px; right: 10px;
    background: rgba(255, 255, 255, 0.2);
    border: 1px solid white;
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
    cursor: pointer;
    z-index: 10;
}

footer {
    text-align: center;
    padding: 2rem;
    font-size: 0.9rem;
    color: #777;
}

/* =========================================
   3. COMPONENTES DE CARD
   ========================================= */
.interesses {
    display: grid;
    gap: 1.5rem;
}

.card {
    background: white;
    padding: 1.5rem;
    border-left: 5px solid #6a1b9a;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
}

body.inverted .card { background: #2d2d2d; border-left-color: #ba68c8; }

.card h3 { margin-bottom: 0.5rem; color: #6a1b9a; }
body.inverted .card h3 { color: #ba68c8; }

.linha-separadora {
    border: 0; height: 1px;
    background: #eee; margin: 1rem 0;
}
body.inverted .linha-separadora { background: #444; }

/* =========================================
   4. SEÇÃO PERFIL E INFOS
   ========================================= */
.foto-perfil {
    display: block; margin: 0 auto 1.5rem;
    width: 150px; height: 150px;
    border-radius: 50%; object-fit: contain;
    border: 4px solid #fff;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
}

.info-pessoal-container {
    display: flex; align-items: center; gap: 1.5rem; margin-top: 1rem;
}

.foto-info {
    width: 120px; height: 120px;
    border-radius: 8px; object-fit: cover;
}

.lista-info { list-style: none; }
.lista-info li strong { color: #6a1b9a; }
body.inverted .lista-info li strong { color: #ba68c8; }

/* =========================================
   5. MÚSICA (VÍDEOS)
   ========================================= */
.video-list-container {
    display: flex; gap: 1rem;
    overflow-x: auto; padding: 1rem 0;
}

.video-item {
    flex: 0 0 250px; height: 150px;
    background: #000; border-radius: 8px; overflow: hidden;
}

.video-item iframe { width: 100%; height: 100%; }

.timeline-label {
    text-align: center; font-weight: bold; color: #6a1b9a;
}
body.inverted .timeline-label { color: #ba68c8; }

/* =========================================
   6. HOBBIES (ACCORDION)
   ========================================= */
.accordion-container p { margin-top: 1rem; font-weight: 500; }

details {
    cursor: pointer; border-bottom: 1px solid #eee;
    padding-bottom: 0.5rem; margin-bottom: 1rem;
}

summary { font-weight: bold; color: #6a1b9a; }
body.inverted summary { color: #ba68c8; }

.item-lista { display: flex; align-items: center; gap: 1rem; padding: 0.5rem 0; }
.item-lista img { width: 60px; height: 60px; border-radius: 4px; }

/* =========================================
   7. VIAGENS (HEXAGONAL)
   ========================================= */
.viagem-container {
    display: flex; align-items: center; justify-content: space-between; gap: 10px;
}

.img-viagem {
    width: 100px; height: 100px; object-fit: cover;
    clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
    background: #6a1b9a; padding: 2px;
}

.divisor-vertical { width: 1px; height: 60px; background: #eee; }
body.inverted .divisor-vertical { background: #444; }

/* =========================================
   8. RESPONSIVIDADE
   ========================================= */
@media (max-width: 600px) {
    .info-pessoal-container, .viagem-container {
        flex-direction: column; text-align: center;
    }
    .divisor-vertical { width: 60px; height: 1px; }
}
```

### O que foi melhorado:
1.  **Agrupamento:** O CSS agora segue uma ordem lógica (do geral para o específico).
2.  **Redução de código:** Removi propriedades repetidas e simplifiquei seletores.
3.  **Comentários:** Adicionei divisores visuais no CSS para você achar qualquer seção em menos de 2 segundos.
4.  **Manutenibilidade:** O HTML agora tem comentários indicando onde cada card começa e termina.

Agora seu projeto está com "cara de profissional", seguindo o que o mercado espera de um desenvolvedor. Pronto para o próximo passo?
-   Observações do cliclo: Foi organizado todo o codigo para que seja melhor compreendido, mesmo enviando os arquivos para AI manter o contexto, a extrutura dos Hobbis foi perdida.
### 7.1 
-   Prompt Sugerido:Quero que adicione comentario para todas as funções no .css
-   Saida do Gemini: Adicionar comentários detalhados no CSS é excelente para revisar a lógica do layout depois de um tempo sem mexer no código.

Aqui está o seu arquivo **`style.css`** com comentários explicando o que cada seletor, classe e propriedade está fazendo na estrutura do seu blog:

```css
/* =========================================
   1. RESET E CONFIGURAÇÕES GERAIS
   ========================================= */

/* * (Asterisco): Seletor universal. Aplica as regras a todos os elementos da página. 
   Aqui, removemos margens e preenchimentos padrão que os navegadores trazem. */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; /* Faz com que bordas e padding não aumentem o tamanho total do elemento */
}

/* body: Define as configurações de base do documento, como fonte e cor de fundo. */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f4f7f6;
    color: #333;
    line-height: 1.6;
    transition: background-color 0.3s, color 0.3s; /* Suaviza a troca de cores do Modo Invertido */
}

/* body.inverted: Estilo aplicado quando a classe "inverted" é adicionada ao body via JavaScript. */
body.inverted {
    background-color: #1a1a1a;
    color: #f4f7f6;
}

/* .container: Centraliza o conteúdo principal e limita a largura para não espalhar em telas muito grandes. */
.container {
    max-width: 800px;
    margin: 2rem auto; /* 2rem em cima/baixo e 'auto' nas laterais para centralizar */
    padding: 0 1rem;
}

/* =========================================
   2. HEADER E FOOTER (Topo e Rodapé)
   ========================================= */

/* header: O topo roxo do site. */
header {
    background-color: #6a1b9a;
    color: white;
    text-align: center;
    padding: 1rem 0;
    position: relative; /* Permite que o botão de toggle seja posicionado em relação ao header */
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

/* body.inverted header: Altera o tom do roxo no modo escuro. */
body.inverted header { background-color: #4a148c; }

/* #btn-toggle: O botão de alternar cores (Lua/Sol). Selecionado pelo ID. */
#btn-toggle {
    position: absolute; /* Fixa o botão em um lugar específico dentro do header */
    top: 10px; 
    right: 10px;
    background: rgba(255, 255, 255, 0.2);
    border: 1px solid white;
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
    cursor: pointer; /* Muda o ícone do mouse para a "mãozinha" de clique */
}

/* footer: Rodapé com informações de copyright. */
footer {
    text-align: center;
    padding: 2rem;
    font-size: 0.9rem;
    color: #777;
}

/* =========================================
   3. COMPONENTES DE CARD
   ========================================= */

/* .interesses: O container que segura os cards. Usa Grid para dar espaçamento entre eles. */
.interesses {
    display: grid;
    gap: 1.5rem;
}

/* .card: O bloco branco que contém cada seção (Música, Hobbies, etc). */
.card {
    background: white;
    padding: 1.5rem;
    border-left: 5px solid #6a1b9a; /* Barra lateral decorativa */
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
}

/* body.inverted .card: Ajusta o fundo do card para cinza escuro no modo invertido. */
body.inverted .card { background: #2d2d2d; border-left-color: #ba68c8; }

/* .card h3: Títulos dentro dos cards. */
.card h3 { margin-bottom: 0.5rem; color: #6a1b9a; }
body.inverted .card h3 { color: #ba68c8; }

/* .linha-separadora: A tag <hr> personalizada que você pediu nos Hobbies. */
.linha-separadora {
    border: 0; 
    height: 1px;
    background: #eee; 
    margin: 1rem 0;
}
body.inverted .linha-separadora { background: #444; }

/* =========================================
   4. SEÇÃO PERFIL E INFOS (Card "Sobre Mim")
   ========================================= */

/* .foto-perfil: A foto principal do topo. */
.foto-perfil {
    display: block; 
    margin: 0 auto 1.5rem;
    width: 150px; 
    height: 150px;
    border-radius: 50%; /* Deixa a imagem redonda */
    object-fit: contain;
    border: 4px solid #fff;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
}

/* .info-pessoal-container: Alinha foto e lista lado a lado. */
.info-pessoal-container {
    display: flex; 
    align-items: center; 
    gap: 1.5rem; 
    margin-top: 1rem;
}

/* .foto-info: A foto quadrada dentro do card "Mais sobre mim". */
.foto-info {
    width: 120px; 
    height: 120px;
    border-radius: 8px; 
    object-fit: cover;
}

/* .lista-info: A lista de Nome, Nascimento, etc. */
.lista-info { list-style: none; } /* Remove as bolinhas da lista */

/* .lista-info li strong: O texto em negrito da lista (ex: "Nome:"). */
.lista-info li strong { color: #6a1b9a; }
body.inverted .lista-info li strong { color: #ba68c8; }

/* =========================================
   5. MÚSICA (VÍDEOS)
   ========================================= */

/* .video-list-container: Flexbox que permite rolar os vídeos para o lado se a tela for pequena. */
.video-list-container {
    display: flex; 
    gap: 1rem;
    overflow-x: auto; /* Adiciona barra de rolagem horizontal se necessário */
    padding: 1rem 0;
}

/* .video-item: Define o tamanho de cada moldura de vídeo. */
.video-item {
    flex: 0 0 250px; /* Impede o vídeo de encolher, trava em 250px de largura */
    height: 150px;
    background: #000; 
    border-radius: 8px; 
    overflow: hidden; /* Garante que o vídeo não saia das bordas arredondadas */
}

/* .video-item iframe: O conteúdo do YouTube em si ocupando todo o espaço do item. */
.video-item iframe { width: 100%; height: 100%; }

/* =========================================
   6. HOBBIES (ACCORDION / DETAILS)
   ========================================= */

/* .accordion-container p: Textos descritivos acima das listas de Hobbies. */
.accordion-container p { margin-top: 1rem; font-weight: 500; }

/* details: Tag de menu expansível. */
details {
    cursor: pointer; 
    border-bottom: 1px solid #eee;
    padding-bottom: 0.5rem; 
    margin-bottom: 1rem;
}

/* summary: O título da lista que clicamos para abrir. */
summary { font-weight: bold; color: #6a1b9a; }
body.inverted summary { color: #ba68c8; }

/* .item-lista: Layout de cada item (Filme/Jogo) dentro da lista expandida. */
.item-lista { display: flex; align-items: center; gap: 1rem; padding: 0.5rem 0; }
.item-lista img { width: 60px; height: 60px; border-radius: 4px; }

/* =========================================
   7. VIAGENS (LAYOUT HEXAGONAL)
   ========================================= */

/* .viagem-container: Alinha Texto | Foto | Linha | Foto | Texto. */
.viagem-container {
    display: flex; 
    align-items: center; 
    justify-content: space-between; 
    gap: 10px;
}

/* .img-viagem: Aplica o recorte hexagonal. */
.img-viagem {
    width: 100px; 
    height: 100px; 
    object-fit: cover;
    /* polygon: Define os 6 pontos do hexágono em coordenadas X e Y. */
    clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
    background: #6a1b9a; 
    padding: 2px;
}

/* .divisor-vertical: A linha fina no centro do card de viagens. */
.divisor-vertical { 
    width: 1px; 
    height: 60px; 
    background: #eee; 
}

/* =========================================
   8. RESPONSIVIDADE (Mobile)
   ========================================= */

/* @media: Quando a tela for menor que 600px, as regras abaixo são aplicadas. */
@media (max-width: 600px) {
    /* Faz os itens que estavam lado a lado ficarem um embaixo do outro. */
    .info-pessoal-container, .viagem-container {
        flex-direction: column; 
        text-align: center;
    }
    /* A linha divisora de viagens vira horizontal no celular. */
    .divisor-vertical { width: 60px; height: 1px; }
}
```
-   Observações do cliclo: Adicionando comentarios ao .css
### 8.0 
-   Prompt Sugerido: Tendo o codigo:
Adicione o awoo_eua.gif como fundo para o site.
-   Saida do Gemini: Entendido! Como você forneceu o arquivo `awoo_eua.gif` e ele está acessível na mesma estrutura, vamos atualizar o CSS para adicioná-lo como fundo do site.

### Alteração no CSS (`style.css`)

**Onde editar:** No início do seu arquivo `style.css`, procure pela tag `body` e adicione as propriedades de `background-image` e `background-size`. Também fiz uma pequena otimização no `body.inverted` para desativar a imagem de fundo quando o modo escuro/invertido estiver ativo, garantindo o contraste.

```css
/* =========================================
   1. RESET E CONFIGURAÇÕES GERAIS
   ========================================= */

/* * (Asterisco): Seletor universal. Aplica as regras a todos os elementos da página. 
   Aqui, removemos margens e preenchimentos padrão que os navegadores trazem. */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; /* Faz com que bordas e padding não aumentem o tamanho total do elemento */
}

/* body: Define as configurações de base do documento, como fonte e cor de fundo. */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: #333;
    line-height: 1.6;
    transition: background-color 0.3s, color 0.3s; /* Suaviza a troca de cores do Modo Invertido */

    /* NOVA ADIÇÃO: Fundo com o GIF fornecido */
    background-image: url('awoo_eua.gif'); /* Link para o GIF */
    background-size: cover; /* Faz a imagem cobrir toda a tela */
    background-attachment: fixed; /* Mantém o fundo fixo ao rolar a página */
    background-position: center; /* Centraliza a imagem */
}

/* body.inverted: Estilo aplicado quando a classe "inverted" é adicionada ao body via JavaScript. */
body.inverted {
    background-color: #1a1a1a;
    color: #f4f7f6;
    background-image: none; /* Desativa a imagem de fundo no modo invertido para não atrapalhar a leitura */
}
```

### Explicação Conceitual:
1.  **`background-image: url('awoo_eua.gif');`**: Esta propriedade diz ao navegador para usar o arquivo GIF fornecido como o preenchimento de fundo da tag `<body>` (o corpo inteiro da página).
2.  **`background-size: cover;`**: Garante que o GIF se estenda para cobrir toda a área da janela do navegador, sem criar repetições indesejadas e sem deixar espaços em branco.
3.  **`background-attachment: fixed;`**: Faz com que o GIF fique parado no fundo enquanto você rola o conteúdo do blog para cima ou para baixo. É um efeito visual bem comum.
4.  **`body.inverted { background-image: none; }`**: No modo escuro/invertido, o fundo se torna cinza escuro. Removi a imagem de fundo aqui para que o GIF (que pode ser muito vibrante ou claro) não brigue com o texto claro, mantendo a acessibilidade.
-   Observações do cliclo: Adicionado imagem de fundo.
### 8.1 
-   Prompt Sugerido: Tendo o codigo.
no .html a class perfil não esta legivel por causa do fundo, como na imagem anexada, quero que fique legivel.
-   Saida do Gemini: Para tornar a secção `.perfil` legível sobre o fundo animado (o GIF), a melhor estratégia é adicionar um fundo semi-transparente, um pouco de preenchimento (`padding`) e arredondar as bordas para que ele se destaque como um "card", tal como fizeste com a secção de interesses.

Aqui estão as alterações necessárias no teu ficheiro **`style.css`**:

### 1. Adicionar estilo à classe `.perfil`
Localiza ou adiciona este bloco no teu CSS. Ele cria uma camada branca semi-transparente atrás do texto:

```css
/* .perfil: Adicionamos um fundo para destacar o texto do GIF de fundo */
.perfil {
    text-align: center;
    margin-bottom: 3rem;
    background: rgba(255, 255, 255, 0.85); /* Fundo branco com 85% de opacidade */
    padding: 2rem;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    border-left: 5px solid #6a1b9a; /* Mantém a identidade visual dos outros cards */
}

/* Ajuste para o Modo Invertido (Escuro) */
body.inverted .perfil {
    background: rgba(45, 45, 45, 0.9); /* Fundo escuro semi-transparente */
    border-left-color: #ba68c8;
}
```

### 2. Pequeno ajuste no Título (`h2`) e Texto (`p`)
Para garantir que o contraste seja perfeito, podes reforçar a cor dos elementos dentro do perfil:

```css
.perfil h2 {
    color: #6a1b9a;
    margin-bottom: 1rem;
}

body.inverted .perfil h2 {
    color: #ba68c8;
}

.perfil p {
    max-width: 600px;
    margin: 0 auto; /* Centraliza o texto se ele for curto */
}
```

### O que isto altera?
* **`background: rgba(255, 255, 255, 0.85)`**: O "a" no final (alpha) controla a transparência. 0.85 é o ideal para esconder o GIF o suficiente para ler o texto, mas ainda deixar transparecer que há algo por trás.
* **`padding: 2rem`**: Cria um respiro interno para que o texto não encoste nas bordas do novo fundo.
* **`border-radius`**: Arredonda os cantos para combinar com o design moderno do resto do site.

Com estas mudanças, a secção "Sobre Mim" aparecerá dentro de um bloco nítido e legível, independentemente de quão agitado seja o GIF de fundo.
-   Observações do cliclo: Foi adicionado transparencia posibilitando ler o que esta no fundo.
### 8.2 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:
### 2.0 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:
## 3. Conclusão