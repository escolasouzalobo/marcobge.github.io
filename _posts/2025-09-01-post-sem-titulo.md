---
layout: post
title: "Post Sem Titulo"
date: 2025-09-01
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;&lt;/meta&gt;
    &lt;meta content="width=device-width, initial-scale=1.0" name="viewport"&gt;&lt;/meta&gt;
    &lt;title&gt;Quiz: Triângulos e suas Classificações&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: #333;
            margin: 0;
            padding: 20px;
            min-height: 100vh;
        }
        .quiz-container {
            max-width: 800px;
            margin: 20px auto;
            background-color: #fff;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2em;
        }
        .subtitle {
            text-align: center;
            color: #7f8c8d;
            margin-bottom: 30px;
            font-size: 1.1em;
        }
        .question-item {
            margin-bottom: 30px;
            padding: 20px;
            background-color: #e9f5ff;
            border-radius: 10px;
            border-left: 5px solid #3498db;
            transition: transform 0.3s ease;
        }
        .question-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        .question-text {
            font-size: 1.2em;
            margin-bottom: 20px;
            line-height: 1.5;
            color: #2c3e50;
            font-weight: 500;
        }
        .options-list {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        .options-list button {
            padding: 15px;
            border: 2px solid #ddd;
            border-radius: 8px;
            background-color: #fff;
            font-size: 1em;
            text-align: left;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        .options-list button:hover:not(:disabled) {
            background-color: #f8f9fa;
            border-color: #3498db;
            transform: translateX(5px);
        }
        .options-list button.correct {
            background-color: #d4edda;
            border-color: #28a745;
            color: #155724;
            font-weight: bold;
        }
        .options-list button.incorrect {
            background-color: #f8d7da;
            border-color: #dc3545;
            color: #721c24;
            font-weight: bold;
        }
        .options-list button:disabled {
            cursor: not-allowed;
            opacity: 0.8;
        }
        .rationale {
            margin-top: 15px;
            padding: 15px;
            border-left: 4px solid #3498db;
            background-color: #f0f7ff;
            font-size: 0.95em;
            line-height: 1.5;
            border-radius: 0 5px 5px 0;
            display: none;
            animation: fadeIn 0.5s ease;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .score-container {
            text-align: center;
            margin-top: 30px;
            padding: 20px;
            background-color: #e9f5ff;
            border-radius: 10px;
            display: none;
        }
        .score-container h2 {
            color: #2c3e50;
            margin-bottom: 15px;
        }
        .score {
            font-size: 2em;
            font-weight: bold;
            color: #3498db;
        }
        .restart-btn {
            margin-top: 20px;
            padding: 12px 25px;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1em;
            transition: background-color 0.3s;
        }
        .restart-btn:hover {
            background-color: #2980b9;
        }
        .header-decoration {
            text-align: center;
            margin-bottom: 20px;
        }
        .triangle-icon {
            font-size: 2.5em;
            color: #3498db;
            margin: 0 10px;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;div class="quiz-container"&gt;
    &lt;div class="header-decoration"&gt;
        &lt;span class="triangle-icon"&gt;▲&lt;/span&gt;
        &lt;span class="triangle-icon" style="transform: rotate(90deg);"&gt;▲&lt;/span&gt;
        &lt;span class="triangle-icon" style="transform: rotate(180deg);"&gt;▲&lt;/span&gt;
        &lt;span class="triangle-icon" style="transform: rotate(270deg);"&gt;▲&lt;/span&gt;
    &lt;/div&gt;
    
    &lt;h1&gt;Quiz: Triângulos e suas Classificações&lt;/h1&gt;
    &lt;p class="subtitle"&gt;Teste seus conhecimentos sobre triângulos, seus elementos e classificações!&lt;/p&gt;

    &lt;div id="quiz-content"&gt;&lt;/div&gt;
    
    &lt;div class="score-container" id="score-container"&gt;
        &lt;h2&gt;Seu Resultado&lt;/h2&gt;
        &lt;p&gt;Você acertou &lt;span class="score" id="score"&gt;0&lt;/span&gt; de &lt;span id="total-questions"&gt;10&lt;/span&gt; questões!&lt;/p&gt;
        &lt;button class="restart-btn" onclick="restartQuiz()"&gt;Refazer Quiz&lt;/button&gt;
    &lt;/div&gt;
&lt;/div&gt;

&lt;script&gt;
    const quizData = {
        "questions": [
            {
                "questionNumber": 1,
                "question": "Um triângulo é uma figura geométrica plana que possui quantos lados, vértices e ângulos?",
                "answerOptions": [
                    { "text": "Dois lados, três vértices e dois ângulos", "isCorrect": false, "rationale": "Um triângulo, por definição, tem três de cada um desses elementos." },
                    { "text": "Três lados, três vértices e três ângulos", "isCorrect": true, "rationale": "A palavra 'triângulo' refere-se aos 'três ângulos', e essa figura é caracterizada por ter três lados e três vértices." },
                    { "text": "Quatro lados, quatro vértices e quatro ângulos", "isCorrect": false, "rationale": "Uma figura com quatro lados, vértices e ângulos é um quadrilátero, não um triângulo." },
                    { "text": "Três lados, dois vértices e três ângulos", "isCorrect": false, "rationale": "O número de vértices em qualquer polígono é sempre igual ao número de lados e ângulos." }
                ]
            },
            {
                "questionNumber": 2,
                "question": "Qual é a soma dos ângulos internos de qualquer triângulo?",
                "answerOptions": [
                    { "text": "90", "isCorrect": false, "rationale": "A soma dos ângulos internos de um triângulo é maior que 90 graus." },
                    { "text": "120", "isCorrect": false, "rationale": "A soma dos ângulos internos é um valor maior que 120 graus." },
                    { "text": "180", "isCorrect": true, "rationale": "A soma dos ângulos internos de qualquer triângulo, independentemente do tipo, é sempre 180 graus." },
                    { "text": "360", "isCorrect": false, "rationale": "A soma dos ângulos internos de um quadrilátero é 360 graus, não de um triângulo." }
                ]
            },
            {
                "questionNumber": 3,
                "question": "Se um triângulo tem todos os lados com a mesma medida, como ele é classificado?",
                "answerOptions": [
                    { "text": "Isósceles", "isCorrect": false, "rationale": "Um triângulo isósceles tem apenas dois lados iguais." },
                    { "text": "Escaleno", "isCorrect": false, "rationale": "Um triângulo escaleno tem todos os lados com medidas diferentes." },
                    { "text": "Equilátero", "isCorrect": true, "rationale": "A classificação 'equilátero' é dada a triângulos com os três lados de igual comprimento." },
                    { "text": "Retângulo", "isCorrect": false, "rationale": "A classificação de triângulo retângulo é baseada nos ângulos, não nos lados." }
                ]
            },
            {
                "questionNumber": 4,
                "question": "Qual tipo de triângulo tem todos os lados com medidas diferentes?",
                "answerOptions": [
                    { "text": "Isósceles", "isCorrect": false, "rationale": "O triângulo isósceles tem dois lados com a mesma medida." },
                    { "text": "Escaleno", "isCorrect": true, "rationale": "A palavra 'escaleno' deriva do grego 'skalenos', que significa 'irregular' ou 'desigual', referindo-se aos seus lados de comprimentos diferentes." },
                    { "text": "Equilátero", "isCorrect": false, "rationale": "O triângulo equilátero tem todos os lados de medidas iguais." },
                    { "text": "Acutângulo", "isCorrect": false, "rationale": "A classificação de triângulo acutângulo é baseada nos ângulos, não nos lados." }
                ]
            },
            {
                "questionNumber": 5,
                "question": "Um triângulo com um ângulo de 90° é classificado como:",
                "answerOptions": [
                    { "text": "Triângulo obtusângulo", "isCorrect": false, "rationale": "Um triângulo obtusângulo tem um ângulo maior que 90°." },
                    { "text": "Triângulo acutângulo", "isCorrect": false, "rationale": "Um triângulo acutângulo tem todos os ângulos menores que 90°." },
                    { "text": "Triângulo escaleno", "isCorrect": false, "rationale": "A classificação escaleno é baseada nos lados, não nos ângulos." },
                    { "text": "Triângulo retângulo", "isCorrect": true, "rationale": "A classificação 'retângulo' é dada a triângulos que contêm um ângulo reto (90°)." }
                ]
            },
            {
                "questionNumber": 6,
                "question": "Qual a classificação de um triângulo em que todos os ângulos são menores que 90°?",
                "answerOptions": [
                    { "text": "Obtusângulo", "isCorrect": false, "rationale": "Um triângulo obtusângulo tem um ângulo maior que 90°." },
                    { "text": "Acutângulo", "isCorrect": true, "rationale": "A classificação 'acutângulo' se refere a um triângulo em que todos os seus ângulos são agudos (menores que 90°)." },
                    { "text": "Retângulo", "isCorrect": false, "rationale": "Um triângulo retângulo tem um ângulo que é exatamente 90°." },
                    { "text": "Escaleno", "isCorrect": false, "rationale": "A classificação escaleno é baseada nos lados, não nos ângulos." }
                ]
            },
            {
                "questionNumber": 7,
                "question": "Um triângulo com um ângulo de 110° é classificado como:",
                "answerOptions": [
                    { "text": "Retângulo", "isCorrect": false, "rationale": "Um triângulo retângulo tem um ângulo de 90°." },
                    { "text": "Isósceles", "isCorrect": false, "rationale": "A classificação isósceles é baseada nos lados, não nos ângulos." },
                    { "text": "Acutângulo", "isCorrect": false, "rationale": "Um triângulo acutângulo não pode ter um ângulo maior que 90°." },
                    { "text": "Obtusângulo", "isCorrect": true, "rationale": "Um triângulo que possui um ângulo obtuso, ou seja, maior que 90°, é classificado como obtusângulo." }
                ]
            },
            {
                "questionNumber": 8,
                "question": "Um triângulo equilátero é sempre:",
                "answerOptions": [
                    { "text": "Retângulo", "isCorrect": false, "rationale": "Triângulos equiláteros não podem ter um ângulo de 90°." },
                    { "text": "Obtusângulo", "isCorrect": false, "rationale": "Um triângulo equilátero não pode ter um ângulo maior que 90°." },
                    { "text": "Acutângulo", "isCorrect": true, "rationale": "Como os triângulos equiláteros têm todos os ângulos internos de 60°, eles são sempre classificados como acutângulos." },
                    { "text": "Escaleno", "isCorrect": false, "rationale": "Um triângulo escaleno tem lados de comprimentos diferentes, o que é o oposto de um triângulo equilátero." }
                ]
            },
            {
                "questionNumber": 9,
                "question": "Um triângulo isósceles pode ser:",
                "answerOptions": [
                    { "text": "Apenas acutângulo", "isCorrect": false, "rationale": "Um triângulo isósceles também pode ser retângulo ou obtusângulo." },
                    { "text": "Apenas obtusângulo", "isCorrect": false, "rationale": "Um triângulo isósceles também pode ser acutângulo ou retângulo." },
                    { "text": "Acutângulo, retângulo ou obtusângulo", "isCorrect": true, "rationale": "Um triângulo isósceles pode ter ângulos que o classificam em qualquer um desses três tipos." },
                    { "text": "Apenas retângulo", "isCorrect": false, "rationale": "Um triângulo isósceles também pode ser acutângulo ou obtusângulo." }
                ]
            },
            {
                "questionNumber": 10,
                "question": "O que diferencia um triângulo escaleno de um triângulo isósceles?",
                "answerOptions": [
                    { "text": "A classificação pelos ângulos.", "isCorrect": false, "rationale": "Ambos os tipos de triângulos podem ser acutângulos, obtusângulos ou retângulos." },
                    { "text": "A classificação pelos lados.", "isCorrect": true, "rationale": "A principal diferença é que o triângulo isósceles tem dois lados de igual comprimento, enquanto o escaleno tem todos os lados de comprimentos diferentes." },
                    { "text": "A soma de seus ângulos internos.", "isCorrect": false, "rationale": "A soma dos ângulos internos é sempre 180° para todos os triângulos." },
                    { "text": "O número de vértices.", "isCorrect": false, "rationale": "Todos os triângulos têm três vértices." }
                ]
            }
        ]
    };

    let score = 0;
    let answeredQuestions = 0;
    const totalQuestions = quizData.questions.length;
    const quizContent = document.getElementById('quiz-content');
    const scoreContainer = document.getElementById('score-container');
    const scoreElement = document.getElementById('score');
    const totalQuestionsElement = document.getElementById('total-questions');

    // Inicializar o quiz
    function initQuiz() {
        score = 0;
        answeredQuestions = 0;
        quizContent.innerHTML = '';
        scoreContainer.style.display = 'none';
        
        quizData.questions.forEach(q =&gt; {
            const questionItem = document.createElement('div');
            questionItem.classList.add('question-item');
            questionItem.id = `question-${q.questionNumber}`;

            const questionText = document.createElement('p');
            questionText.classList.add('question-text');
            questionText.innerHTML = `&lt;strong&gt;Questão ${q.questionNumber}:&lt;/strong&gt; ${q.question}`;
            questionItem.appendChild(questionText);

            const optionsList = document.createElement('div');
            optionsList.classList.add('options-list');

            // Criar elemento de racional (apenas um por pergunta)
            const rationale = document.createElement('div');
            rationale.classList.add('rationale');
            optionsList.appendChild(rationale);

            q.answerOptions.forEach(option =&gt; {
                const button = document.createElement('button');
                button.textContent = option.text;
                button.setAttribute('data-rationale', option.rationale);
                button.setAttribute('data-is-correct', option.isCorrect);

                button.addEventListener('click', () =&gt; {
                    // Desativar todos os botões para esta pergunta
                    optionsList.querySelectorAll('button').forEach(btn =&gt; {
                        btn.disabled = true;
                    });
                    
                    // Mostrar o racional para a opção selecionada
                    rationale.textContent = option.rationale;
                    rationale.style.display = 'block';

                    if (option.isCorrect) {
                        button.classList.add('correct');
                        score++;
                    } else {
                        button.classList.add('incorrect');
                        // Encontrar e destacar a resposta correta
                        const correctButton = optionsList.querySelector('[data-is-correct="true"]');
                        if (correctButton) {
                            correctButton.classList.add('correct');
                        }
                    }
                    
                    answeredQuestions++;
                    
                    // Verificar se todas as questões foram respondidas
                    if (answeredQuestions === totalQuestions) {
                        showScore();
                    }
                });

                optionsList.insertBefore(button, rationale);
            });

            questionItem.appendChild(optionsList);
            quizContent.appendChild(questionItem);
        });
        
        totalQuestionsElement.textContent = totalQuestions;
    }

    function showScore() {
        scoreElement.textContent = score;
        scoreContainer.style.display = 'block';
        
        // Rolar suavemente para o resultado
        scoreContainer.scrollIntoView({ behavior: 'smooth' });
    }

    function restartQuiz() {
        initQuiz();
    }

    // Iniciar o quiz quando a página carregar
    window.onload = initQuiz;
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;