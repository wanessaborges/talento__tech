# talento__tech
git clone https://github.com/seu-usuario/sistema-gerenciamento-eventos.git
cd sistema-gerenciamento-eventos
mkdir css js
touch index.html cadastro.html lista.html css/style.css js/script.js README.md
# Sistema de Gerenciamento de Eventos

## Objetivo
Criar um sistema simples para gerenciar eventos, permitindo cadastro e exibição de uma lista de eventos.

## Funcionalidades
1. Página inicial com introdução ao sistema.
2. Página de cadastro de eventos.
3. Página de listagem de eventos cadastrados.

## Cronograma de Desenvolvimento
| Etapa               | Descrição                        | Prazo        |
|---------------------|----------------------------------|--------------|
| Configuração inicial| Criar repositório e estruturação | 1 dia        |
| Desenvolvimento     | Criar HTML, CSS, lógica e JS     | 3 dias       |
| Revisão final       | Revisar e organizar commits      | 1 dia        |
git add README.md
git commit -m "Adicionado README.md com planejamento"
git push
sistema-gerenciamento-eventos/
│
├── css/
│   └── style.css
├── js/
│   └── script.js
├── index.html
├── cadastro.html
├── lista.html
└── README.md
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gerenciamento de Eventos</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Sistema de Gerenciamento de Eventos</h1>
        <nav>
            <a href="cadastro.html">Cadastrar Evento</a>
            <a href="lista.html">Lista de Eventos</a>
        </nav>
    </header>
    <main>
        <p>Bem-vindo ao sistema de gerenciamento de eventos. Use as opções acima para cadastrar ou visualizar eventos.</p>
    </main>
    <footer>
        <p>&copy; 2024 Sistema de Gerenciamento de Eventos</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadastrar Evento</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Cadastrar Evento</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="lista.html">Lista de Eventos</a>
        </nav>
    </header>
    <main>
        <form id="eventForm">
            <label for="title">Título:</label>
            <input type="text" id="title" required>
            
            <label for="description">Descrição:</label>
            <textarea id="description" required></textarea>
            
            <label for="date">Data:</label>
            <input type="date" id="date" required>
            
            <label for="location">Local:</label>
            <input type="text" id="location" required>
            
            <button type="submit">Cadastrar</button>
        </form>
    </main>
    <footer>
        <p>&copy; 2024 Sistema de Gerenciamento de Eventos</p>
    </footer>
    <script src="js/script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lista de Eventos</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Lista de Eventos</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="cadastro.html">Cadastrar Evento</a>
        </nav>
    </header>
    <main>
        <ul id="eventList"></ul>
    </main>
    <footer>
        <p>&copy; 2024 Sistema de Gerenciamento de Eventos</p>
    </footer>
    <script src="js/script.js"></script>
</body>
</html>
// Lista de eventos
const events = [];

// Função para salvar evento
document.getElementById('eventForm')?.addEventListener('submit', function (e) {
    e.preventDefault();
    const title = document.getElementById('title').value;
    const description = document.getElementById('description').value;
    const date = document.getElementById('date').value;
    const location = document.getElementById('location').value;

    events.push({ title, description, date, location });
    alert('Evento cadastrado com sucesso!');
    this.reset();
});

// Função para exibir eventos na lista
window.onload = function () {
    const eventList = document.getElementById('eventList');
    if (eventList) {
        eventList.innerHTML = events
            .map(event => `<li>${event.date} - ${event.title} (${event.location})</li>`)
            .join('');
    }
};
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #007BFF;
    color: white;
    padding: 1rem;
    text-align: center;
}

nav a {
    margin: 0 15px;
    color: white;
    text-decoration: none;
}

main {
    padding: 2rem;
    text-align: center;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1rem;
    margin-top: 2rem;
}
git checkout -b feature-home
# Adicione a funcionalidade e faça commits
git checkout -b feature-cadastro
# Adicione o cadastro e faça commits
git checkout -b feature-lista
# Adicione a lista e faça commits
git checkout main
git merge feature-home
git merge feature-cadastro
git merge feature-lista
