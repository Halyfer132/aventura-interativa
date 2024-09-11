<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aventura Interativa</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="game-container">
        <h1>Escolha sua aventura</h1>
        <div id="story"></div>
        <div id="choices"></div>
    </div>
    <script src="script.js"></script>
</body>
</html>
/* styles.css */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

#game-container {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
    width: 300px;
}

h1 {
    font-size: 1.5em;
    margin-bottom: 20px;
}

#choices button {
    display: block;
    width: 100%;
    margin: 5px 0;
    padding: 10px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
}

#choices button:hover {
    background-color: #0056b3;
}
// script.js
document.addEventListener('DOMContentLoaded', function() {
    const storyElement = document.getElementById('story');
    const choicesElement = document.getElementById('choices');

    const game = {
        storyIndex: 0,
        stories: [
            {
                text: "Você está em uma floresta sombria. Para onde deseja ir?",
                choices: [
                    { text: "Seguir pela trilha iluminada", nextIndex: 1 },
                    { text: "Entrar na cabana misteriosa", nextIndex: 2 }
                ]
            },
            {
                text: "Você segue pela trilha iluminada e encontra uma ponte. O que fazer?",
                choices: [
                    { text: "Cruzá-la", nextIndex: 3 },
                    { text: "Voltar para a floresta", nextIndex: 0 }
                ]
            },
            {
                text: "Você entra na cabana e encontra um velho mago. O que fazer?",
                choices: [
                    { text: "Perguntar sobre o destino", nextIndex: 4 },
                    { text: "Sair correndo", nextIndex: 0 }
                ]
            },
            {
                text: "Você cruzou a ponte e encontrou um tesouro! Você ganhou o jogo!",
                choices: []
            },
            {
                text: "O velho mago te dá um mapa mágico. Você ganhou o jogo!",
                choices: []
            }
        ],
        showStory: function() {
            const currentStory = this.stories[this.storyIndex];
            storyElement.textContent = currentStory.text;
            choicesElement.innerHTML = '';
            
            currentStory.choices.forEach(choice => {
                const button = document.createElement('button');
                button.textContent = choice.text;
                button.addEventListener('click', () => {
                    this.storyIndex = choice.nextIndex;
                    this.showStory();
                });
                choicesElement.appendChild(button);
            });
        }
    };

    game.showStory();
});
