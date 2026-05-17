---
layout: post
title: "Post Sem Titulo"
date: 2025-07-23
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;&lt;/meta&gt;
    &lt;meta content="width=device-width, initial-scale=1.0" name="viewport"&gt;&lt;/meta&gt;
    &lt;title&gt;Regra de Três Simples para Pequenos Gênios!&lt;/title&gt;
    &lt;!-- Inclui o Tailwind CSS para estilização fácil e responsiva --&gt;
    &lt;script src="https://cdn.tailwindcss.com"&gt;&lt;/script&gt;
    &lt;!-- Define a fonte Inter para todo o documento --&gt;
    &lt;style&gt;
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f9ff; /* Azul claro de fundo */
            color: #333;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
        }
        .card {
            background-color: #fff;
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            border: 2px solid #a7d9f7; /* Borda azul clara */
        }
        .interactive-button {
            background-color: #60a5fa; /* Azul vibrante */
            color: white;
            padding: 12px 25px;
            border-radius: 10px;
            font-weight: bold;
            transition: background-color 0.3s ease, transform 0.2s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            border: none;
            cursor: pointer;
        }
        .interactive-button:hover {
            background-color: #3b82f6; /* Azul mais escuro no hover */
            transform: translateY(-2px);
        }
        .interactive-button:active {
            transform: translateY(0);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }
        .result-message {
            margin-top: 15px;
            padding: 10px;
            border-radius: 8px;
            font-weight: bold;
            text-align: center;
        }
        .correct {
            background-color: #d1fae5; /* Verde claro */
            color: #065f46; /* Verde escuro */
        }
        .incorrect {
            background-color: #fee2e2; /* Vermelho claro */
            color: #991b1b; /* Vermelho escuro */
        }
        .challenge-input {
            width: 80px;
            padding: 8px;
            border-radius: 8px;
            border: 2px solid #a7d9f7;
            text-align: center;
            font-size: 1.1em;
        }
        .image-container {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap; /* Permite que as imagens quebrem a linha em telas menores */
            gap: 15px;
            margin: 20px 0;
        }
        .image-container img {
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            max-width: 100%; /* Garante que a imagem não ultrapasse o contêiner */
            height: auto;
        }
        /* Estilos para as maçãs "pulando" */
        .apple {
            width: 50px;
            height: 50px;
            background-color: #ef4444; /* Vermelho maçã */
            border-radius: 50%;
            display: inline-flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-weight: bold;
            font-size: 1.2em;
            margin: 5px;
            transition: transform 0.5s ease-out, opacity 0.5s ease-out;
        }
        .apple.hidden {
            opacity: 0;
            transform: translateY(-20px);
        }
        .apple.visible {
            opacity: 1;
            transform: translateY(0);
        }
        .basket-content {
            min-height: 60px; /* Garante espaço para as maçãs */
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body class="p-4"&gt;
    &lt;div class="container"&gt;
        &lt;header class="text-center mb-10"&gt;
            &lt;h1 class="text-5xl font-extrabold text-blue-700 mb-4"&gt;🍎🥕 Regra de Três Simples para Pequenos Gênios! 🐻⚽&lt;/h1&gt;
            &lt;p class="text-xl text-gray-600"&gt;Olá, amiguinho(a)! Vamos aprender uma coisa muito legal sobre como as coisas se combinam? É como mágica, mas é matemática! ✨&lt;/p&gt;
        &lt;/header&gt;

        &lt;!-- Seção O que é a Regra de Três --&gt;
        &lt;section class="card"&gt;
            &lt;h2 class="text-3xl font-bold text-blue-600 mb-4"&gt;🧸 O que é a Regra de Três?&lt;/h2&gt;
            &lt;p class="text-lg mb-4"&gt;Imagina que você tem ursinhos de pelúcia e quer dar uma balinha para cada um. Se você tem &lt;strong class="text-red-500"&gt;1 ursinho&lt;/strong&gt;, precisa de &lt;strong class="text-red-500"&gt;1 balinha&lt;/strong&gt;, certo?&lt;/p&gt;
            &lt;p class="text-lg"&gt;Se você tiver &lt;strong class="text-green-500"&gt;2 ursinhos&lt;/strong&gt;, vai precisar de... &lt;strong class="text-green-500"&gt;2 balinhas&lt;/strong&gt;! Isso é a Regra de Três: descobrir quantos de uma coisa você precisa se souber quantos de outra coisa você tem!&lt;/p&gt;
        &lt;/section&gt;

        &lt;!-- Seção Vamos Brincar e Aprender! --&gt;
        &lt;section class="card"&gt;
            &lt;h2 class="text-3xl font-bold text-blue-600 mb-6"&gt;🎨 Vamos Brincar e Aprender!&lt;/h2&gt;

            &lt;!-- Exemplo 1: Maçãs e Cestas --&gt;
            &lt;div class="mb-8 p-6 bg-blue-50 rounded-lg border border-blue-200"&gt;
                &lt;h3 class="text-2xl font-semibold text-blue-700 mb-3"&gt;Exemplo 1: Maçãs e Cestas&lt;/h3&gt;
                &lt;p class="text-lg mb-4"&gt;&lt;strong&gt;Pergunta:&lt;/strong&gt; Se &lt;strong class="text-purple-600"&gt;1 cesta&lt;/strong&gt; tem espaço para &lt;strong class="text-purple-600"&gt;3 maçãs&lt;/strong&gt;, quantas maçãs cabem em &lt;strong class="text-purple-600"&gt;2 cestas&lt;/strong&gt;?&lt;/p&gt;

                &lt;div class="image-container"&gt;
                    &lt;div class="text-center"&gt;
                        &lt;img alt="Uma cesta com três maçãs" class="w-48 h-36 object-cover" src="https://placehold.co/200x150/FFDDC1/000?text=1+cesta+com+3+maçãs" /&gt;
                        &lt;p class="mt-2 text-sm text-gray-500"&gt;1 Cesta&lt;/p&gt;
                        &lt;div class="basket-content" id="basket1-content"&gt;
                            &lt;div class="apple"&gt;🍎&lt;/div&gt;
                            &lt;div class="apple"&gt;🍎&lt;/div&gt;
                            &lt;div class="apple"&gt;🍎&lt;/div&gt;
                        &lt;/div&gt;
                    &lt;/div&gt;
                    &lt;div class="text-center" id="basket2-container"&gt;
                        &lt;img alt="Duas cestas vazias" class="w-48 h-36 object-cover" src="https://placehold.co/200x150/FFDDC1/000?text=2+cestas+vazias" /&gt;
                        &lt;p class="mt-2 text-sm text-gray-500"&gt;2 Cestas&lt;/p&gt;
                        &lt;div class="basket-content" id="basket2-content"&gt;
                            &lt;!-- Maçãs serão adicionadas aqui via JS --&gt;
                        &lt;/div&gt;
                    &lt;/div&gt;
                &lt;/div&gt;

                &lt;div class="flex justify-center gap-4 mt-6"&gt;
                    &lt;button class="interactive-button" id="addApplesBtn"&gt;Colocar Maçãs na Segunda Cesta&lt;/button&gt;
                &lt;/div&gt;
                &lt;div class="result-message hidden" id="applesResult"&gt;&lt;/div&gt;
            &lt;/div&gt;

            &lt;!-- Exemplo 2: Bolas e Caixas --&gt;
            &lt;div class="mb-8 p-6 bg-green-50 rounded-lg border border-green-200"&gt;
                &lt;h3 class="text-2xl font-semibold text-green-700 mb-3"&gt;Exemplo 2: Bolas e Caixas&lt;/h3&gt;
                &lt;p class="text-lg mb-4"&gt;&lt;strong&gt;Pergunta:&lt;/strong&gt; Se &lt;strong class="text-orange-600"&gt;1 caixa&lt;/strong&gt; guarda &lt;strong class="text-orange-600"&gt;2 bolas&lt;/strong&gt;, quantas bolas guardam &lt;strong class="text-orange-600"&gt;3 caixas&lt;/strong&gt;?&lt;/p&gt;

                &lt;div class="image-container"&gt;
                    &lt;div class="text-center"&gt;
                        &lt;img alt="Uma caixa com duas bolas" class="w-48 h-36 object-cover" src="https://placehold.co/200x150/D1FAE5/000?text=1+caixa+com+2+bolas" /&gt;
                        &lt;p class="mt-2 text-sm text-gray-500"&gt;1 Caixa&lt;/p&gt;
                    &lt;/div&gt;
                    &lt;div class="text-center"&gt;
                        &lt;img alt="Caixas vazias" class="w-48 h-36 object-cover" src="https://placehold.co/200x150/D1FAE5/000?text=Caixas+vazias" /&gt;
                        &lt;p class="mt-2 text-sm text-gray-500"&gt;Mais Caixas&lt;/p&gt;
                    &lt;/div&gt;
                &lt;/div&gt;

                &lt;div class="flex justify-center gap-4 mt-6"&gt;
                    &lt;button class="interactive-button bg-green-600 hover:bg-green-700" id="addBoxBtn"&gt;Adicionar uma Caixa&lt;/button&gt;
                    &lt;button class="interactive-button bg-red-500 hover:bg-red-600" id="resetBoxesBtn"&gt;Reiniciar&lt;/button&gt;
                &lt;/div&gt;
                &lt;div class="mt-4 text-center text-xl font-bold text-green-800"&gt;Total de Caixas: &lt;span id="boxCount"&gt;1&lt;/span&gt;&lt;/div&gt;
                &lt;div class="mt-2 text-center text-xl font-bold text-green-800"&gt;Total de Bolas: &lt;span id="ballCount"&gt;2&lt;/span&gt;&lt;/div&gt;
                &lt;div class="result-message hidden" id="boxesResult"&gt;&lt;/div&gt;
            &lt;/div&gt;
        &lt;/section&gt;

        &lt;!-- Seção Seu Turno de Desafios! --&gt;
        &lt;section class="card"&gt;
            &lt;h2 class="text-3xl font-bold text-blue-600 mb-6"&gt;🌟 Seu Turno de Desafios!&lt;/h2&gt;

            &lt;!-- Desafio 1: Flores e Vasos --&gt;
            &lt;div class="mb-8 p-6 bg-yellow-50 rounded-lg border border-yellow-200"&gt;
                &lt;h3 class="text-2xl font-semibold text-yellow-700 mb-3"&gt;Desafio 1: Flores e Vasos&lt;/h3&gt;
                &lt;p class="text-lg mb-4"&gt;&lt;strong&gt;Pergunta:&lt;/strong&gt; Se em &lt;strong class="text-pink-600"&gt;1 vaso&lt;/strong&gt; cabem &lt;strong class="text-pink-600"&gt;4 flores&lt;/strong&gt;, quantas flores cabem em &lt;strong class="text-pink-600"&gt;2 vasos&lt;/strong&gt;?&lt;/p&gt;

                &lt;div class="image-container"&gt;
                    &lt;img alt="Um vaso com quatro flores" class="w-48 h-36 object-cover" src="https://placehold.co/200x150/FEE2E2/000?text=1+vaso+com+4+flores" /&gt;
                    &lt;img alt="Dois vasos vazios" class="w-48 h-36 object-cover" src="https://placehold.co/200x150/FEE2E2/000?text=2+vasos+vazios" /&gt;
                &lt;/div&gt;

                &lt;div class="flex flex-col items-center gap-4 mt-6"&gt;
                    &lt;input class="challenge-input" id="flowersAnswer" placeholder="Sua resposta" type="number" /&gt;
                    &lt;button class="interactive-button bg-yellow-600 hover:bg-yellow-700" id="checkFlowersBtn"&gt;Verificar Resposta&lt;/button&gt;
                &lt;/div&gt;
                &lt;div class="result-message hidden" id="flowersResult"&gt;&lt;/div&gt;
            &lt;/div&gt;

            &lt;!-- Desafio 2: Carros e Rodas --&gt;
            &lt;div class="mb-8 p-6 bg-purple-50 rounded-lg border border-purple-200"&gt;
                &lt;h3 class="text-2xl font-semibold text-purple-700 mb-3"&gt;Desafio 2: Carros e Rodas&lt;/h3&gt;
                &lt;p class="text-lg mb-4"&gt;&lt;strong&gt;Pergunta:&lt;/strong&gt; Se &lt;strong class="text-indigo-600"&gt;1 carro&lt;/strong&gt; tem &lt;strong class="text-indigo-600"&gt;4 rodas&lt;/strong&gt;, quantas rodas têm &lt;strong class="text-indigo-600"&gt;3 carros&lt;/strong&gt;?&lt;/p&gt;

                &lt;div class="image-container"&gt;
                    &lt;img alt="Um carro com quatro rodas" class="w-48 h-36 object-cover" src="https://placehold.co/200x150/E0BBE4/000?text=1+carro+com+4+rodas" /&gt;
                    &lt;img alt="Três carros vazios" class="w-48 h-36 object-cover" src="https://placehold.co/200x150/E0BBE4/000?text=3+carros+vazios" /&gt;
                &lt;/div&gt;

                &lt;div class="flex flex-col items-center gap-4 mt-6"&gt;
                    &lt;input class="challenge-input" id="carsAnswer" placeholder="Sua resposta" type="number" /&gt;
                    &lt;button class="interactive-button bg-purple-600 hover:bg-purple-700" id="checkCarsBtn"&gt;Verificar Resposta&lt;/button&gt;
                &lt;/div&gt;
                &lt;div class="result-message hidden" id="carsResult"&gt;&lt;/div&gt;
            &lt;/div&gt;
        &lt;/section&gt;

        &lt;!-- Seção de Conclusão --&gt;
        &lt;section class="card text-center"&gt;
            &lt;h2 class="text-3xl font-bold text-blue-600 mb-4"&gt;🎉 Parabéns, Pequeno Matemático!&lt;/h2&gt;
            &lt;p class="text-lg mb-6"&gt;Você está ficando muito esperto com a Regra de Três! Ela vai te ajudar muito a entender como as coisas funcionam no mundo!&lt;/p&gt;
            &lt;img alt="Crianças felizes com medalhas" class="mx-auto rounded-lg shadow-md" src="https://placehold.co/200x150/C3F8FF/000?text=Crianças+felizes+com+medalhas" /&gt;
        &lt;/section&gt;    
    &lt;/div&gt;

    &lt;script&gt;
        // Função para mostrar mensagens de resultado
        function showResult(elementId, message, isCorrect) {
            const resultElement = document.getElementById(elementId);
            resultElement.textContent = message;
            resultElement.classList.remove('hidden', 'correct', 'incorrect');
            if (isCorrect) {
                resultElement.classList.add('correct');
            } else {
                resultElement.classList.add('incorrect');
            }
            // Torna a mensagem visível
            resultElement.style.display = 'block';
            setTimeout(() =&gt; {
                // Esconde a mensagem após 3 segundos
                resultElement.style.display = 'none';
                resultElement.classList.add('hidden');
            }, 3000);
        }

        // --- Lógica para o Exemplo 1: Maçãs e Cestas ---
        const addApplesBtn = document.getElementById('addApplesBtn');
        const basket2Content = document.getElementById('basket2-content');
        const applesResult = document.getElementById('applesResult');

        addApplesBtn.addEventListener('click', () =&gt; {
            // Remove maçãs existentes para evitar duplicação em cliques repetidos
            basket2Content.innerHTML = '';
            // Adiciona 3 maçãs à segunda cesta, uma por uma com um pequeno atraso
            for (let i = 0; i &lt; 3; i++) {
                setTimeout(() =&gt; {
                    const apple = document.createElement('div');
                    apple.classList.add('apple', 'hidden');
                    apple.textContent = '🍎';
                    basket2Content.appendChild(apple);
                    // Força o reflow para a transição funcionar
                    void apple.offsetWidth;
                    apple.classList.remove('hidden');
                    apple.classList.add('visible');
                }, i * 200); // Pequeno atraso entre as maçãs
            }

            // Mostra o resultado final após todas as maçãs serem adicionadas
            setTimeout(() =&gt; {
                showResult('applesResult', 'Você viu? Duas cestas podem guardar 6 maçãs!', true);
            }, 3 * 200 + 500); // Espera as maçãs aparecerem + um pequeno buffer
        });

        // --- Lógica para o Exemplo 2: Bolas e Caixas ---
        const addBoxBtn = document.getElementById('addBoxBtn');
        const resetBoxesBtn = document.getElementById('resetBoxesBtn');
        const boxCountSpan = document.getElementById('boxCount');
        const ballCountSpan = document.getElementById('ballCount');
        const boxesResult = document.getElementById('boxesResult');

        let currentBoxes = 1; // Começa com 1 caixa
        let currentBalls = 2; // Começa com 2 bolas (1 caixa * 2 bolas/caixa)

        addBoxBtn.addEventListener('click', () =&gt; {
            if (currentBoxes &lt; 3) { // Limita a 3 caixas para este exemplo
                currentBoxes++;
                currentBalls += 2; // Cada caixa adiciona 2 bolas
                boxCountSpan.textContent = currentBoxes;
                ballCountSpan.textContent = currentBalls;

                if (currentBoxes === 3) {
                    showResult('boxesResult', `Muito bem! Três caixas podem guardar ${currentBalls} bolas!`, true);
                }
            } else {
                showResult('boxesResult', 'Você já adicionou o máximo de caixas para este exemplo!', false);
            }
        });

        resetBoxesBtn.addEventListener('click', () =&gt; {
            currentBoxes = 1;
            currentBalls = 2;
            boxCountSpan.textContent = currentBoxes;
            ballCountSpan.textContent = currentBalls;
            boxesResult.classList.add('hidden'); // Esconde a mensagem de resultado
        });

        // --- Lógica para o Desafio 1: Flores e Vasos ---
        const flowersAnswerInput = document.getElementById('flowersAnswer');
        const checkFlowersBtn = document.getElementById('checkFlowersBtn');
        const flowersResult = document.getElementById('flowersResult');

        checkFlowersBtn.addEventListener('click', () =&gt; {
            const userAnswer = parseInt(flowersAnswerInput.value);
            const correctAnswer = 8; // 2 vasos * 4 flores/vaso

            if (userAnswer === correctAnswer) {
                showResult('flowersResult', '🎉 Parabéns! Resposta correta!', true);
            } else if (isNaN(userAnswer)) {
                showResult('flowersResult', 'Por favor, digite um número.', false);
            } else {
                showResult('flowersResult', 'Ops! Tente novamente. Lembre-se: se 1 vaso tem 4 flores, 2 vasos terão o dobro!', false);
            }
        });

        // --- Lógica para o Desafio 2: Carros e Rodas ---
        const carsAnswerInput = document.getElementById('carsAnswer');
        const checkCarsBtn = document.getElementById('checkCarsBtn');
        const carsResult = document.getElementById('carsResult');

        checkCarsBtn.addEventListener('click', () =&gt; {
            const userAnswer = parseInt(carsAnswerInput.value);
            const correctAnswer = 12; // 3 carros * 4 rodas/carro

            if (userAnswer === correctAnswer) {
                showResult('carsResult', '🥳 Incrível! Você acertou!', true);
            } else if (isNaN(userAnswer)) {
                showResult('carsResult', 'Por favor, digite um número.', false);
            } else {
                showResult('carsResult', 'Quase lá! Pense bem: se 1 carro tem 4 rodas, e você tem 3 carros...', false);
            }
        });
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;