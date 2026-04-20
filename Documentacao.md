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