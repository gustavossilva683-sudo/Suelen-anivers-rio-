# Suelen-anivers-rio-
index.html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Feliz Aniversário, Meu Amor!</title>
    <style>
        /* --- ESTILOS CSS --- */
        body {
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background: linear-gradient(135deg, #ffc0cb 0%, #ff8c00 100%); /* Rosa a Laranja - Cores de Amor e Alegria */
            color: #4a4a4a;
            text-align: center;
            padding: 20px;
        }

        .container {
            background-color: rgba(255, 255, 255, 0.95);
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            max-width: 600px;
            width: 100%;
            transition: all 0.5s ease-in-out;
        }

        h1 {
            color: #d81b60; /* Rosa Escuro */
            margin-bottom: 10px;
            font-size: 2.5em;
        }

        p {
            font-size: 1.1em;
            margin-bottom: 25px;
            line-height: 1.6;
        }

        .heart-button {
            background-color: #e91e63; /* Rosa Vivo */
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.2em;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(233, 30, 99, 0.5);
            transition: background-color 0.3s, transform 0.1s;
        }

        .heart-button:hover {
            background-color: #c2185b;
            transform: translateY(-2px);
        }

        .heart-button:active {
            transform: translateY(0);
        }

        #final-message {
            display: none;
            margin-top: 30px;
            padding: 20px;
            background-color: #fff3e0; /* Amarelo claro/Pêssego */
            border: 2px solid #ff7043; /* Laranja */
            border-radius: 10px;
            font-size: 1.3em;
            color: #ff7043;
            animation: fadeIn 2s;
        }

        #final-message strong {
            display: block;
            margin-top: 10px;
            font-size: 1.5em;
            color: #d81b60;
        }

        /* Animação para a mensagem final */
        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.9); }
            to { opacity: 1; transform: scale(1); }
        }

    </style>
</head>
<body>

    <div class="container" id="main-container">

        <h1>🎉 Uma Missão de Aniversário! 🎉</h1>
        
        <p>Meu amor, antes de ver a mensagem do seu marido, você precisa realizar uma tarefa simples, mas muito importante:</p>

        <h2>O Desafio: "Encha o Coração!"</h2>

        <p>O coração do Gustavo só ficará completo e a mensagem será revelada quando você clicar no botão abaixo **5 vezes**. Cada clique representa um pedacinho do amor que ele sente por você!</p>

        <button class="heart-button" id="click-task">
            Clique Aqui e Encha o Coração! ❤️ (<span id="count">0</span>/5)
        </button>

        <div id="final-message">
            🥳 **MENSAGEM SECRETA REVELADA!** 🥳
            <p>Essa é uma mensagem do seu marido **Gustavo** que deseja **FELIZ ANIVERSÁRIO** e te **AMA** com todas as forças desse mundo! Você é a luz da vida dele.</p>
            <strong>Com todo o meu amor, Gustavo.</strong>
        </div>

    </div>

    <script>
        /* --- LÓGICA JAVASCRIPT --- */
        const button = document.getElementById('click-task');
        const finalMessage = document.getElementById('final-message');
        const clickCountSpan = document.getElementById('count');
        const mainContainer = document.getElementById('main-container');
        
        let clickCount = 0;
        const requiredClicks = 5;

        button.addEventListener('click', function() {
            if (clickCount < requiredClicks) {
                clickCount++;
                clickCountSpan.textContent = clickCount;
            }

            if (clickCount === requiredClicks) {
                // Altera o estado para mostrar a mensagem
                button.style.display = 'none'; // Esconde o botão
                finalMessage.style.display = 'block'; // Mostra a mensagem
                mainContainer.querySelector('h1').textContent = 'Surpresa Revelada! 🎁';
                mainContainer.querySelector('p').style.display = 'none'; // Esconde a instrução
                mainContainer.querySelector('h2').style.display = 'none'; // Esconde o título do desafio
            }
        });
    </script>

</body>
</html>
