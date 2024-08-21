<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Árvore Interativa</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
        }
        .container {
            position: relative;
            display: inline-block;
        }
        .fruit {
            cursor: pointer;
            position: absolute;
            background-color: transparent;
            border: none;
            padding: 5px;
            text-align: center;
            line-height: 1.2;
            font-size: 18px; /* Tamanho padrão da palavra original */
            font-family: 'Arial', sans-serif;
            color: black;
            white-space: normal;
            overflow: hidden;
            width: 200px;
        }
        .large-word {
            font-size: 12px; /* Tamanho maior da nova palavra */
            font-weight: bold; /* Negrito, opcional */
            color: black; /* Cor diferente, opcional */
        }
        /* Estilos específicos para as posições dos frutos */
        #fruit1 { top: 4%; left: -4%; }
        #fruit2 { top: 19%; left: 58%; }
        #fruit3 { top: 20%; left: 5%; }
        #fruit4 { top: 33%; left: 12%; }
        #fruit5 { top: 59%; left: 26%; }
        #fruit6 { top: 85%; left: 41%; }
        #fruit7 { top: 72%; left: 34%; }
        #fruit8 { top: 46%; left: 19%; }
        #fruit9 { top: 44%; left: 69%; }
        #fruit10 { top: 64%; left: 69%; }
    </style>
</head>
<body>
    <h1>Teste</h1>
    <div class="container">
        <img src="https://pbs.twimg.com/media/GVc80JWXMAAcDTY?format=png&name=900x900" alt="Árvore com frutos" width="600px">
        <div id="fruit1" class="fruit" onclick="toggleWord('fruit1')">BNCC</div>
        <div id="fruit2" class="fruit" onclick="toggleWord('fruit2')">Palavra</div>
        <div id="fruit3" class="fruit" onclick="toggleWord('fruit3')">Palavra</div>
        <div id="fruit4" class="fruit" onclick="toggleWord('fruit4')">Palavra</div>
        <div id="fruit5" class="fruit" onclick="toggleWord('fruit5')">Palavra</div>
        <div id="fruit6" class="fruit" onclick="toggleWord('fruit6')">Palavra</div>
        <div id="fruit7" class="fruit" onclick="toggleWord('fruit7')">Palavra</div>
        <div id="fruit8" class="fruit" onclick="toggleWord('fruit8')">Palavra</div>
        <div id="fruit9" class="fruit" onclick="toggleWord('fruit9')">Palavra</div>
        <div id="fruit10" class="fruit" onclick="toggleWord('fruit10')">Palavra</div>
    </div>

    <script>
        // Mapeia o ID dos frutos para as palavras original e nova
        const words = {
            fruit1: { original: 'BNCC', new: 'teste' },
            fruit2: { original: 'Palavra', new: 'Nova Palavra' },
            fruit3: { original: 'Palavra', new: 'Nova Palavra' },
            fruit4: { original: 'Palavra', new: 'Nova Palavra' },
            fruit5: { original: 'Palavra', new: 'associam o conteúdo curricular a operações cognitivas, indicando as habilidades que serão avalidas' },
            fruit6: { original: 'Palavra', new: 'Nova Palavra' },
            fruit7: { original: 'Palavra', new: 'Nova Palavra' },
            fruit8: { original: 'Palavra', new: 'Nova Palavra' },
            fruit9: { original: 'Palavra', new: 'Nova Palavra' },
            fruit10: { original: 'Palavra', new: 'Nova Palavra' },
        };

        function toggleWord(fruitId) {
            const fruit = document.getElementById(fruitId);
            const currentWord = fruit.textContent.trim();
            const wordData = words[fruitId];

            if (currentWord === wordData.original) {
                fruit.textContent = wordData.new;
                fruit.classList.add('large-word'); // Adiciona a classe para a nova palavra
            } else {
                fruit.textContent = wordData.original;
                fruit.classList.remove('large-word'); // Remove a classe para voltar ao tamanho original
            }
        }
    </script>
</body>
</html>

