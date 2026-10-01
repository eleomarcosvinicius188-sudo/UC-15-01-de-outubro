# UC-15-01-de-outubro

<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfólio — Aula 35</title>
  <link rel="stylesheet" href="marcos.css">
</head>
<body>

  <header class="menu">
    <span class="menu-logo" id="logo">MedTec</span>
    <nav class="menu-nav">
      <a href="#" class="menu-link">Início</a>
      <a href="#" class="menu-link">Projetos</a>
      <a href="#" class="menu-link">Sobre</a>
      <a href="#" class="menu-link">Contato</a>
    </nav>
  </header>

  <section class="hero" id="hero">
    <h1 id="titulo">Meu Portfólio</h1>
    <p class="hero-texto" id="subtitulo">Estudante do MedTec SENAC Natal</p>
    <button class="btn-hero" id="btn-hero">Ver meus projetos</button>
  </section>

  <section class="secao" id="projetos">
    <h2 class="secao-titulo">Projetos</h2>
    <div class="grade">
      <div class="projeto-card" id="card-1">
        <h3>Loja Online</h3>
        <p class="card-tech">HTML · CSS · Flask</p>
      </div>
      <div class="projeto-card" id="card-2">
        <h3>Blog Pessoal</h3>
        <p class="card-tech">Flexbox · Grid</p>
      </div>
      <div class="projeto-card" id="card-3">
        <h3>App de Clima</h3>
        <p class="card-tech">JavaScript · API</p>
      </div>
      <div class="projeto-card" id="card-4">
        <h3>Lista de Tarefas</h3>
        <p class="card-tech">HTML · CSS · JS</p>
      </div>
    </div>
  </section>

  <section class="secao" id="habilidades">
    <h2 class="secao-titulo">Habilidades</h2>
    <div class="skills-wrap" id="skills-wrap">
      <span class="skill-tag">HTML5</span>
      <span class="skill-tag">CSS3</span>
      <span class="skill-tag">JavaScript</span>
    </div>
  </section>

  <section class="secao" id="sobre">
    <h2 class="secao-titulo">Sobre mim</h2>
    <p id="texto-sobre">Apaixonado por tecnologia e desenvolvimento web.</p>
  </section>

  <script src="script.js"></script>
</body>
</html>

// Selecionar o h1 e mudar o texto
const titulo = document.querySelector('h1');
titulo.textContent = 'JavaScript chegou!';

// Selecionar pelo nome da classe — com o ponto, igual ao CSS
const logo = document.querySelector('.menu-logo');
logo.textContent = '<Dev/>';

// Tentar selecionar algo que não existe
const inexistente = document.querySelector('.xyz');
console.log(inexistente); // null

inexistente.textContent = 'Oi';

if (inexistente) {
  inexistente.textContent = 'Oi';
} else {
  console.log('Não encontrou o elemento!');
}

// Pegar todos os links do menu de uma vez
const links = document.querySelectorAll('.menu-link');
console.log('Quantidade:', links.length); // 4

// Acessar pelo índice — começa em 0
console.log(links[0].textContent); // Início
console.log(links[1].textContent); // Projetos

links[0].textContent = 'Início';
links[1].textContent = 'Projetos';
links[2].textContent = 'Sobre';
links[3].textContent = 'Contato';

// NodeList vazia — não é null, é length 0
const nada = document.querySelectorAll('.xyz');
console.log(nada.length); // 0 — sem erro!

querySelector('seletor')
querySelectorAll('seletor')

tag:     querySelector('h1')
classe:  querySelector('.card')
id:      querySelector('#logo')

:root {
  --fundo:    #0f1117;
  --card-bg:  #22263a;
  --primaria: #2E75B6;
  --texto:    #e8eaf0;
  --suave:    #8890aa;
  --borda:    #2e3450;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: Arial, sans-serif;
  background: var(--fundo);
  color: var(--texto);
  min-height: 100vh;
}

.menu {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 16px 32px;
  background: var(--card-bg);
  border-bottom: 1px solid var(--borda);
  position: sticky;
  top: 0;
}

.menu-logo { font-weight: bold; font-size: 1.1rem; color: var(--primaria); }

.menu-nav { display: flex; gap: 12px; }

.menu-link {
  color: var(--suave);
  text-decoration: none;
  font-size: 0.9rem;
  padding: 6px 14px;
  border-radius: 6px;
  border: 1px solid var(--borda);
}

.hero {
  text-align: center;
  padding: 60px 32px;
  border-bottom: 1px solid var(--borda);
}

.hero h1 { font-size: 2.5rem; margin-bottom: 12px; }

.hero-texto { font-size: 1.1rem; color: var(--suave); margin-bottom: 24px; }

.btn-hero {
  padding: 12px 28px;
  background: var(--primaria);
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
}

.secao { padding: 40px 32px; border-bottom: 1px solid var(--borda); }

.secao-titulo { font-size: 1.4rem; color: var(--primaria); margin-bottom: 24px; }

.grade {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
  gap: 16px;
}

.projeto-card {
  background: var(--card-bg);
  border: 1px solid var(--borda);
  border-radius: 10px;
  padding: 20px;
}

.projeto-card h3 { font-size: 1rem; margin-bottom: 6px; }

.card-tech { font-size: 0.82rem; color: var(--suave); }

.skills-wrap { display: flex; flex-wrap: wrap; gap: 8px; }

.skill-tag {
  font-size: 0.82rem;
  padding: 4px 14px;
  border-radius: 20px;
  border: 1px solid var(--primaria);
  color: var(--primaria);
  background: rgba(46, 117, 182, 0.1);
}

#sobre p { font-size: 0.95rem; color: var(--suave); line-height: 1.7; }
