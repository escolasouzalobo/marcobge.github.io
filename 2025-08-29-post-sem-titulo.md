---
layout: post
title: "Post Sem Titulo"
date: 2025-08-29
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Quiz de Triângulos&lt;/title&gt;
    &lt;!-- Tailwind CSS CDN --&gt;
    &lt;script src="https://cdn.tailwindcss.com"&gt;&lt;/script&gt;
    &lt;!-- Font Inter --&gt;
    &lt;link rel="preconnect" href="https://fonts.googleapis.com"&gt;
    &lt;link rel="preconnect" href="https://fonts.gstatic.com" crossorigin&gt;
    &lt;link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&amp;display=swap" rel="stylesheet"&gt;
    &lt;style&gt;
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6;
        }
        .correct-answer {
            background-color: #d1fae5;
            border-color: #34d399;
        }
        .incorrect-answer {
            background-color: #fee2e2;
            border-color: #f87171;
        }
        .button-selected {
            border-color: #3b82f6;
            background-color: #eff6ff;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body class="flex items-center justify-center min-h-screen p-4"&gt;

    &lt;div id="quiz-container" class="bg-white p-8 rounded-2xl shadow-xl w-full max-w-lg transition-all duration-300"&gt;
        &lt;h1 class="text-3xl font-bold text-center text-gray-800 mb-6"&gt;Quiz de Triângulos&lt;/h1&gt;
        
        &lt;div id="quiz-content" class="transition-all duration-300"&gt;
            &lt;div id="question-header" class="flex justify-between items-center mb-4 text-sm text-gray-500"&gt;
                &lt;span id="question-count"&gt;Questão 1 de 10&lt;/span&gt;
            &lt;/div&gt;
            &lt;h2 id="question-text" class="text-xl font-medium text-gray-700 mb-6"&gt;&lt;/h2&gt;
            
            &lt;div id="options-container" class="space-y-4 mb-6"&gt;
                &lt;!-- Botões das opções serão injetados aqui via JS --&gt;
            &lt;/div&gt;
            
            &lt;div id="feedback" class="mb-4 text-center p-4 rounded-lg hidden"&gt;
                &lt;p id="feedback-text" class="font-medium"&gt;&lt;/p&gt;
                &lt;p id="rationale-text" class="text-sm mt-2 text-gray-600"&gt;&lt;/p&gt;
            &lt;/div&gt;
            
            &lt;button id="next-button" class="w-full bg-blue-500 text-white font-semibold py-3 px-6 rounded-xl shadow-md hover:bg-blue-600 transition-colors duration-200 focus:outline-none" disabled&gt;
                Próximo
            &lt;/button&gt;
        &lt;/div&gt;
        
        &lt;div id="score-container" class="hidden text-center transition-all duration-300"&gt;
            &lt;h2 class="text-2xl font-bold text-gray-800 mb-4"&gt;Quiz Concluído!&lt;/h2&gt;
            &lt;p id="final-score" class="text-xl text-gray-700 mb-6"&gt;Sua pontuação foi de 0 de 10.&lt;/p&gt;
            &lt;button id="restart-button" class="w-full bg-blue-500 text-white font-semibold py-3 px-6 rounded-xl shadow-md hover:bg-blue-600 transition-colors duration-200 focus:outline-none"&gt;
                Recomeçar
            &lt;/button&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        const questions = [
            {
                question: "1. Qual dos conjuntos de medidas pode formar um triângulo?",
                options: ["3 cm, 4 cm, 8 cm", "5 cm, 5 cm, 10 cm", "6 cm, 7 cm, 12 cm", "2 cm, 2 cm, 5 cm"],
                correctAnswerIndex: 2,
                rationale: "A soma dos dois lados menores (6 + 7 = 13) é maior que o lado maior (12), satisfazendo a condição de existência para formar um triângulo."
            },
            {
                question: "2. Se os comprimentos de dois lados de um triângulo são 4 cm e 9 cm, qual dos seguintes valores pode ser o comprimento do terceiro lado?",
                options: ["3 cm", "5 cm", "13 cm", "10 cm"],
                correctAnswerIndex: 3,
                rationale: "O terceiro lado deve ser maior que a diferença dos outros dois (9 - 4 = 5) e menor que a soma (9 + 4 = 13). O único valor que se encaixa é 10."
            },
            {
                question: "3. Dado um triângulo com lados de x cm, 7 cm e 10 cm, quais são os possíveis valores inteiros para x?",
                options: ["3, 4, 5, 6, ..., 16", "4, 5, 6, ..., 17", "3, 4, 5, ..., 17", "4, 5, 6, ..., 16"],
                correctAnswerIndex: 3,
                rationale: "O valor de x deve ser maior que a diferença entre os lados conhecidos (10 - 7 = 3) e menor que a soma (10 + 7 = 17). Então, os inteiros possíveis são de 4 a 16."
            },
            {
                question: "4. Um triângulo tem dois lados medindo 5 cm e 9 cm. Se o terceiro lado for um número inteiro, qual é o seu valor mínimo e máximo?",
                options: ["Mínimo 4 cm e máximo 14 cm", "Mínimo 5 cm e máximo 13 cm", "Mínimo 5 cm e máximo 14 cm", "Mínimo 6 cm e máximo 12 cm"],
                correctAnswerIndex: 1,
                rationale: "O terceiro lado deve ser maior que a diferença (9 - 5 = 4) e menor que a soma (9 + 5 = 14). Assim, o menor inteiro possível é 5 e o maior é 13."
            },
            {
                question: "5. A soma dos comprimentos de dois lados de um triângulo é 15 cm. O terceiro lado pode medir:",
                options: ["16 cm", "15 cm", "14 cm", "17 cm"],
                correctAnswerIndex: 2,
                rationale: "O terceiro lado deve ser estritamente menor que a soma dos outros dois lados. Como a soma é 15 cm, o terceiro lado pode ser 14 cm."
            },
            {
                question: "6. Em um triângulo, os ângulos internos medem 45°, 60° e x. Qual é o valor de x?",
                options: ["90°", "65°", "75°", "100°"],
                correctAnswerIndex: 2,
                rationale: "A soma dos ângulos internos de um triângulo é 180°. Então, 180 - (45 + 60) = 180 - 105 = 75°."
            },
            {
                question: "7. Um triângulo tem ângulos internos que medem 2x, 3x e 4x. Qual é o valor de x?",
                options: ["20°", "15°", "30°", "25°"],
                correctAnswerIndex: 0,
                rationale: "A soma dos ângulos é 180°. Então, 2x + 3x + 4x = 180 -&gt; 9x = 180 -&gt; x = 20."
            },
            {
                question: "8. Em um triângulo isósceles, um dos ângulos da base mede 40°. Quais são as medidas dos outros dois ângulos?",
                options: ["40° e 100°", "40° e 90°", "50° e 90°", "70° e 70°"],
                correctAnswerIndex: 0,
                rationale: "Em um triângulo isósceles, os ângulos da base são iguais. Se um é 40°, o outro também é. O terceiro ângulo é 180 - (40 + 40) = 100°."
            },
            {
                question: "9. A figura mostra um triângulo retângulo. Qual é o valor do ângulo y?",
                options: ["40°", "50°", "60°", "45°"],
                correctAnswerIndex: 0,
                rationale: "Em um triângulo retângulo, a soma dos dois ângulos agudos é 90°. Então, 90 - 50 = 40°."
            },
            {
                question: "10. Se um triângulo equilátero tem todos os seus lados com a mesma medida, qual a medida de cada um de seus ângulos internos?",
                options: ["90°", "45°", "60°", "120°"],
                correctAnswerIndex: 2,
                rationale: "Em um triângulo equilátero, os três ângulos são iguais. A soma é 180°, então 180 / 3 = 60°."
            }
        ];

        let currentQuestionIndex = 0;
        let score = 0;

        const questionCountElement = document.getElementById('question-count');
        const questionTextElement = document.getElementById('question-text');
        const optionsContainer = document.getElementById('options-container');
        const feedbackContainer = document.getElementById('feedback');
        const feedbackTextElement = document.getElementById('feedback-text');
        const rationaleTextElement = document.getElementById('rationale-text');
        const nextButton = document.getElementById('next-button');
        const quizContent = document.getElementById('quiz-content');
        const scoreContainer = document.getElementById('score-container');
        const finalScoreElement = document.getElementById('final-score');
        const restartButton = document.getElementById('restart-button');

        function loadQuestion() {
            const currentQuestion = questions[currentQuestionIndex];
            
            questionCountElement.textContent = `Questão ${currentQuestionIndex + 1} de ${questions.length}`;
            questionTextElement.textContent = currentQuestion.question;
            optionsContainer.innerHTML = '';
            
            currentQuestion.options.forEach((option, index) =&gt; {
                const button = document.createElement('button');
                button.textContent = option;
                button.classList.add('w-full', 'bg-gray-100', 'text-gray-800', 'py-3', 'px-4', 'rounded-xl', 'text-left', 'border-2', 'border-transparent', 'hover:bg-gray-200', 'transition-colors', 'duration-200', 'focus:outline-none');
                button.addEventListener('click', () =&gt; selectAnswer(button, index));
                optionsContainer.appendChild(button);
            });

            feedbackContainer.classList.add('hidden');
            nextButton.disabled = true;
            nextButton.textContent = "Próximo";
        }

        function selectAnswer(button, selectedIndex) {
            const currentQuestion = questions[currentQuestionIndex];
            const isCorrect = selectedIndex === currentQuestion.correctAnswerIndex;
            
            // Disable all buttons after selection
            Array.from(optionsContainer.children).forEach(btn =&gt; btn.disabled = true);
            
            // Mark the selected button
            Array.from(optionsContainer.children).forEach(btn =&gt; {
                btn.classList.remove('button-selected');
                btn.classList.remove('incorrect-answer', 'correct-answer');
            });
            button.classList.add('button-selected');

            // Show feedback
            if (isCorrect) {
                score++;
                feedbackTextElement.textContent = 'Resposta Correta!';
                feedbackContainer.classList.remove('incorrect-answer');
                feedbackContainer.classList.add('correct-answer');
            } else {
                feedbackTextElement.textContent = 'Resposta Incorreta!';
                feedbackContainer.classList.remove('correct-answer');
                feedbackContainer.classList.add('incorrect-answer');
            }
            rationaleTextElement.textContent = currentQuestion.rationale;
            feedbackContainer.classList.remove('hidden');

            nextButton.disabled = false;
        }

        function showNextQuestion() {
            currentQuestionIndex++;
            if (currentQuestionIndex &lt; questions.length) {
                loadQuestion();
            } else {
                showFinalScore();
            }
        }
        
        function showFinalScore() {
            quizContent.classList.add('hidden');
            scoreContainer.classList.remove('hidden');
            finalScoreElement.textContent = `Sua pontuação final foi: ${score} de ${questions.length}.`;
        }
        
        function restartQuiz() {
            currentQuestionIndex = 0;
            score = 0;
            quizContent.classList.remove('hidden');
            scoreContainer.classList.add('hidden');
            loadQuestion();
        }

        nextButton.addEventListener('click', showNextQuestion);
        restartButton.addEventListener('click', restartQuiz);

        // Initial load
        window.onload = loadQuestion;
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;