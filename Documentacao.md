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
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:

---

### 2.0 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:

---

### 2.0 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:

---

### 2.0 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:
### 2.0 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:
### 2.0 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:
### 2.0 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:
### 2.0 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:
### 2.0 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:
### 2.0 
-   Prompt Sugerido:
-   Saida do Gemini: 
-   Observações do cliclo:
## 3. Conclusão