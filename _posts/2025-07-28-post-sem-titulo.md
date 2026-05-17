---
layout: post
title: "Post Sem Titulo"
date: 2025-07-28
---

&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;&lt;/meta&gt;
    &lt;meta content="width=device-width, initial-scale=1.0" name="viewport"&gt;&lt;/meta&gt;
    &lt;title&gt;Números Racionais para o EF&lt;/title&gt;
    &lt;!-- Tailwind CSS CDN --&gt;
    &lt;script src="https://cdn.tailwindcss.com"&gt;&lt;/script&gt;
    &lt;!-- Font Awesome for icons --&gt;
    &lt;link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet"&gt;&lt;/link&gt;
    &lt;link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&amp;amp;display=swap" rel="stylesheet"&gt;&lt;/link&gt;
    &lt;!-- MathJax CDN for LaTeX rendering --&gt;
    &lt;script async="" id="MathJax-script" src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js" type="text/javascript"&gt;
    &lt;/script&gt;
    &lt;style&gt;
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f4f8; /* Light blue-gray background */
        }
        .section-card {
            background-color: #ffffff;
            border-radius: 1.5rem; /* More rounded corners */
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            padding: 2rem;
            margin-bottom: 2rem;
        }
        .header-gradient {
            background: linear-gradient(to right, #6366f1, #8b5cf6); /* Purple-blue gradient */
        }
        .btn-primary {
            background-color: #6366f1; /* Indigo */
            color: white;
            padding: 0.75rem 1.5rem;
            border-radius: 0.75rem;
            transition: background-color 0.3s ease;
        }
        .btn-primary:hover {
            background-color: #4f46e5; /* Darker indigo */
        }
        .quiz-option {
            background-color: #e0e7ff; /* Light blue */
            border: 2px solid #a5b4fc; /* Medium blue */
            padding: 0.75rem 1.25rem;
            border-radius: 0.75rem;
            cursor: pointer;
            transition: background-color 0.2s ease, border-color 0.2s ease;
        }
        .quiz-option:hover {
            background-color: #c7d2fe; /* Lighter blue on hover */
            border-color: #818cf8;
        }
        .quiz-option.correct {
            background-color: #d1fae5; /* Green for correct */
            border-color: #34d399;
        }
        .quiz-option.incorrect {
            background-color: #fee2e2; /* Red for incorrect */
            border-color: #ef4444;
        }
        .fraction-display {
            display: flex;
            flex-direction: column;
            align-items: center;
            font-size: 2.5rem; /* Larger font for fractions */
            font-weight: bold;
            color: #374151; /* Dark gray */
        }
        .fraction-line {
            width: 80%; /* Line width */
            height: 4px;
            background-color: #374151;
            margin: 0.2rem 0;
        }
        /* Custom styles for number line */
        .number-line-container {
            width: 100%;
            height: 50px;
            background-color: #f9fafb;
            border: 1px solid #d1d5db;
            border-radius: 0.75rem;
            position: relative;
            margin-top: 2rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 1rem;
            overflow: hidden; /* Hide overflow for draggable elements */
        }
        .number-line-mark {
            position: absolute;
            top: 0;
            bottom: 0;
            width: 2px;
            background-color: #6b7280;
        }
        .number-line-label {
            position: absolute;
            top: 55px; /* Position below the line */
            transform: translateX(-50%);
            font-size: 0.9rem;
            color: #4b5563;
        }
        .draggable-fraction {
            position: absolute;
            background-color: #a78bfa; /* Purple */
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 0.5rem;
            cursor: grab;
            font-size: 1.1rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            z-index: 10;
        }
        .draggable-fraction:active {
            cursor: grabbing;
        }
        .feedback-message {
            margin-top: 1rem;
            padding: 0.75rem;
            border-radius: 0.5rem;
            font-weight: 600;
            text-align: center;
        }
        .feedback-message.success {
            background-color: #d1fae5;
            color: #065f46;
        }
        .feedback-message.error {
            background-color: #fee2e2;
            color: #991b1b;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body class="min-h-screen flex flex-col"&gt;

    &lt;!-- Header Section --&gt;
    &lt;header class="header-gradient text-white p-6 md:p-8 shadow-lg rounded-b-3xl"&gt;
        &lt;div class="container mx-auto text-center"&gt;
            &lt;h1 class="text-3xl md:text-5xl font-extrabold mb-2"&gt;Números Racionais 🌎&lt;/h1&gt;
            &lt;p class="text-xl md:text-2xl font-light"&gt;Desvendando o Mundo das Frações e Decimais!&lt;/p&gt;
        &lt;/div&gt;
    &lt;/header&gt;

    &lt;!-- Main Content --&gt;
    &lt;main class="container mx-auto p-4 md:p-8 flex-grow"&gt;

        &lt;!-- Introduction Section --&gt;
        &lt;section class="section-card" id="introducao"&gt;
            &lt;h2 class="text-2xl md:text-3xl font-bold text-gray-800 mb-4 flex items-center"&gt;
                &lt;i class="fas fa-question-circle text-indigo-500 mr-3"&gt;&lt;/i&gt; O Que São Números Racionais?
            &lt;/h2&gt;
            &lt;p class="text-gray-700 leading-relaxed mb-4"&gt;
                Os &lt;strong&gt;números racionais&lt;/strong&gt; são todos os números que podem ser escritos como uma &lt;strong&gt;fração&lt;/strong&gt;, ou seja, como uma divisão de dois números inteiros, onde o número de baixo (o denominador) nunca pode ser zero. Eles são representados pela letra Q.
            &lt;/p&gt;
            &lt;div class="bg-blue-50 p-4 rounded-xl border border-blue-200"&gt;
                &lt;p class="font-semibold text-blue-800 mb-2"&gt;Pense assim:&lt;/p&gt;
                &lt;ul class="list-disc list-inside text-blue-700"&gt;
                    &lt;li&gt;Uma fatia de pizza: &lt;span class="font-mono text-lg"&gt;1/8&lt;/span&gt; (uma parte de oito)&lt;/li&gt;
                    &lt;li&gt;Metade de um copo de suco: &lt;span class="font-mono text-lg"&gt;1/2&lt;/span&gt; (uma parte de duas)&lt;/li&gt;
                &lt;/ul&gt;
                &lt;p class="mt-3 text-blue-800 font-medium"&gt;
                    &lt;i class="fas fa-lightbulb text-yellow-500 mr-2"&gt;&lt;/i&gt; &lt;strong&gt;Curiosidade:&lt;/strong&gt; Todo número inteiro também é um número racional! Por exemplo, o número 3 pode ser escrito como &lt;span class="font-mono text-lg"&gt;3/1&lt;/span&gt;.
                &lt;/p&gt;
            &lt;/div&gt;
        &lt;/section&gt;

        &lt;!-- Representation Section --&gt;
        &lt;section class="section-card" id="representacao"&gt;
            &lt;h2 class="text-2xl md:text-3xl font-bold text-gray-800 mb-4 flex items-center"&gt;
                &lt;i class="fas fa-chart-pie text-green-500 mr-3"&gt;&lt;/i&gt; Representação dos Números Racionais
            &lt;/h2&gt;
            &lt;p class="text-gray-700 leading-relaxed mb-6"&gt;
                Os números racionais podem aparecer de diferentes formas. Vamos ver as principais:
            &lt;/p&gt;

            &lt;!-- 1. Fração --&gt;
            &lt;div class="mb-8 p-6 bg-gray-50 rounded-xl border border-gray-200"&gt;
                &lt;h3 class="text-xl md:text-2xl font-semibold text-gray-800 mb-3 flex items-center"&gt;
                    &lt;i class="fas fa-pizza-slice text-orange-500 mr-2"&gt;&lt;/i&gt; 1. Fração
                &lt;/h3&gt;
                &lt;p class="text-gray-700 leading-relaxed mb-4"&gt;
                    A forma mais comum de um número racional é a &lt;strong&gt;fração&lt;/strong&gt;. Ela é composta por:
                &lt;/p&gt;
                &lt;ul class="list-disc list-inside text-gray-700 mb-4"&gt;
                    &lt;li&gt;&lt;strong&gt;Numerador:&lt;/strong&gt; O número de cima, que indica quantas partes estamos considerando.&lt;/li&gt;
                    &lt;li&gt;&lt;strong&gt;Denominador:&lt;/strong&gt; O número de baixo, que indica em quantas partes iguais o todo foi dividido.&lt;/li&gt;
                &lt;/ul&gt;

                &lt;!-- Quiz de Frações --&gt;
                &lt;div class="bg-white p-5 rounded-xl shadow-inner"&gt;
                    &lt;p class="font-semibold text-gray-800 mb-4"&gt;
                        &lt;i class="fas fa-question-circle text-purple-500 mr-2"&gt;&lt;/i&gt; &lt;strong&gt;Teste seu conhecimento!&lt;/strong&gt;
                    &lt;/p&gt;
                    &lt;p class="text-gray-700 mb-4"&gt;
                        Quantas fatias você comeria se pegasse &lt;span class="font-mono text-lg"&gt;3/4&lt;/span&gt; de uma pizza de 8 fatias?
                    &lt;/p&gt;
                    &lt;div class="grid grid-cols-1 md:grid-cols-2 gap-4" id="quiz-options"&gt;
                        &lt;div class="quiz-option" data-answer="2"&gt;A) 2&lt;/div&gt;
                        &lt;div class="quiz-option" data-answer="3"&gt;B) 3&lt;/div&gt;
                        &lt;div class="quiz-option" data-answer="4"&gt;C) 4&lt;/div&gt;
                        &lt;div class="quiz-option" data-answer="6"&gt;D) 6&lt;/div&gt;
                    &lt;/div&gt;
                    &lt;div class="feedback-message hidden" id="quiz-feedback"&gt;&lt;/div&gt;
                &lt;/div&gt;
            &lt;/div&gt;

            &lt;!-- 2. Decimal --&gt;
            &lt;div class="mb-8 p-6 bg-gray-50 rounded-xl border border-gray-200"&gt;
                &lt;h3 class="text-xl md:text-2xl font-semibold text-gray-800 mb-3 flex items-center"&gt;
                    &lt;i class="fas fa-dollar-sign text-teal-500 mr-2"&gt;&lt;/i&gt; 2. Decimal
                &lt;/h3&gt;
                &lt;p class="text-gray-700 leading-relaxed mb-4"&gt;
                    Os números decimais são aqueles que usam uma &lt;strong&gt;vírgula&lt;/strong&gt; para separar a parte inteira da parte "quebrada" ou fracionária. Eles são muito usados no nosso dia a dia, como no dinheiro e nas medidas.
                &lt;/p&gt;
                &lt;p class="text-gray-700 leading-relaxed mb-4"&gt;
                    &lt;strong&gt;Como transformar fração em decimal?&lt;/strong&gt; É só dividir o numerador pelo denominador!
                &lt;/p&gt;
                &lt;div class="bg-white p-5 rounded-xl shadow-inner"&gt;
                    &lt;p class="font-semibold text-gray-800 mb-4"&gt;
                        &lt;i class="fas fa-calculator text-blue-500 mr-2"&gt;&lt;/i&gt; &lt;strong&gt;Conversor de Fração para Decimal:&lt;/strong&gt;
                    &lt;/p&gt;
                    &lt;div class="flex flex-col md:flex-row items-center space-y-4 md:space-y-0 md:space-x-4"&gt;
                        &lt;input class="w-full md:w-1/3 p-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500" id="numerator" placeholder="Numerador" type="number" /&gt;
                        &lt;span class="text-3xl font-bold text-gray-700"&gt;/&lt;/span&gt;
                        &lt;input class="w-full md:w-1/3 p-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500" id="denominator" placeholder="Denominador" type="number" /&gt;
                        &lt;button class="btn-primary w-full md:w-auto" id="convert-btn"&gt;Converter&lt;/button&gt;
                    &lt;/div&gt;
                    &lt;div class="mt-4 text-center text-2xl font-bold text-indigo-700" id="decimal-result"&gt;&lt;/div&gt;
                    &lt;div class="feedback-message hidden" id="conversion-feedback"&gt;&lt;/div&gt;
                &lt;/div&gt;
            &lt;/div&gt;

            &lt;!-- 3. Reta Numérica --&gt;
            &lt;div class="mb-8 p-6 bg-gray-50 rounded-xl border border-gray-200"&gt;
                &lt;h3 class="text-xl md:text-2xl font-semibold text-gray-800 mb-3 flex items-center"&gt;
                    &lt;i class="fas fa-ruler-horizontal text-red-500 mr-2"&gt;&lt;/i&gt; 3. Reta Numérica
                &lt;/h3&gt;
                &lt;p class="text-gray-700 leading-relaxed mb-4"&gt;
                    Podemos colocar os números racionais na &lt;strong&gt;reta numérica&lt;/strong&gt;! Eles ficam entre os números inteiros.
                &lt;/p&gt;
                &lt;div class="bg-white p-5 rounded-xl shadow-inner"&gt;
                    &lt;p class="font-semibold text-gray-800 mb-4"&gt;
                        &lt;i class="fas fa-hand-pointer text-yellow-500 mr-2"&gt;&lt;/i&gt; &lt;strong&gt;Arraste e Solte na Reta Numérica:&lt;/strong&gt;
                        &lt;br /&gt;&lt;span class="text-sm font-normal text-gray-600"&gt;Arraste a fração para o local correto na reta.&lt;/span&gt;
                    &lt;/p&gt;
                    &lt;div class="number-line-container relative"&gt;
                        &lt;!-- Marks for 0, 1, 2, 3 --&gt;
                        &lt;div class="number-line-mark" style="left: 0%;"&gt;&lt;/div&gt;
                        &lt;span class="number-line-label" style="left: 0%;"&gt;0&lt;/span&gt;
                        &lt;div class="number-line-mark" style="left: 33.3%;"&gt;&lt;/div&gt;
                        &lt;span class="number-line-label" style="left: 33.3%;"&gt;1&lt;/span&gt;
                        &lt;div class="number-line-mark" style="left: 66.6%;"&gt;&lt;/div&gt;
                        &lt;span class="number-line-label" style="left: 66.6%;"&gt;2&lt;/span&gt;
                        &lt;div class="number-line-mark" style="left: 99.9%;"&gt;&lt;/div&gt;
                        &lt;span class="number-line-label" style="left: 99.9%;"&gt;3&lt;/span&gt;

                        &lt;!-- Draggable Fraction --&gt;
                        &lt;div class="draggable-fraction" id="draggable-fraction" style="left: 50%; top: 50%; transform: translate(-50%, -50%);"&gt;1/2&lt;/div&gt;
                    &lt;/div&gt;
                    &lt;div class="feedback-message hidden" id="number-line-feedback"&gt;&lt;/div&gt;
                    &lt;button class="btn-primary mt-4 w-full md:w-auto" id="check-number-line"&gt;Verificar Posição&lt;/button&gt;
                    &lt;button class="btn-primary mt-4 w-full md:w-auto ml-2" id="reset-number-line"&gt;Reiniciar&lt;/button&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/section&gt;

        &lt;!-- Operations Section --&gt;
        &lt;section class="section-card" id="operacoes"&gt;
            &lt;h2 class="text-2xl md:text-3xl font-bold text-gray-800 mb-4 flex items-center"&gt;
                &lt;i class="fas fa-calculator text-purple-500 mr-3"&gt;&lt;/i&gt; Operações com Números Racionais
            &lt;/h2&gt;
            &lt;p class="text-gray-700 leading-relaxed mb-6"&gt;
                Assim como os números inteiros, podemos fazer operações com os números racionais!
            &lt;/p&gt;

            &lt;!-- 1. Adição e Subtração --&gt;
            &lt;div class="mb-8 p-6 bg-gray-50 rounded-xl border border-gray-200"&gt;
                &lt;h3 class="text-xl md:text-2xl font-semibold text-gray-800 mb-3 flex items-center"&gt;
                    &lt;i class="fas fa-plus-minus text-blue-500 mr-2"&gt;&lt;/i&gt; 1. Adição e Subtração
                &lt;/h3&gt;
                &lt;p class="text-gray-700 leading-relaxed mb-2"&gt;
                    &lt;strong&gt;Com o mesmo denominador:&lt;/strong&gt; É fácil! É só somar ou subtrair os numeradores e manter o denominador.
                    &lt;br /&gt;&lt;span class="font-mono text-lg text-gray-800"&gt;Ex: 1/5 + 2/5 = 3/5&lt;/span&gt;
                &lt;/p&gt;
                &lt;p class="text-gray-700 leading-relaxed"&gt;
                    &lt;strong&gt;Com denominadores diferentes:&lt;/strong&gt; Aí precisamos encontrar um "denominador comum" antes de somar ou subtrair. Usamos o Mínimo Múltiplo Comum (MMC)!
                &lt;/p&gt;
            &lt;/div&gt;

            &lt;!-- 2. Multiplicação e Divisão --&gt;
            &lt;div class="mb-8 p-6 bg-gray-50 rounded-xl border border-gray-200"&gt;
                &lt;h3 class="text-xl md:text-2xl font-semibold text-gray-800 mb-3 flex items-center"&gt;
                    &lt;i class="fas fa-times text-green-500 mr-2"&gt;&lt;/i&gt; &lt;i class="fas fa-divide text-red-500 mr-2"&gt;&lt;/i&gt; 2. Multiplicação e Divisão
                &lt;/h3&gt;
                &lt;p class="text-gray-700 leading-relaxed mb-2"&gt;
                    &lt;strong&gt;Multiplicação:&lt;/strong&gt; Multiplica-se numerador por numerador e denominador por denominador. Simples assim!
                    &lt;br /&gt;&lt;span class="font-mono text-lg text-gray-800"&gt;Ex: 1/2 × 3/4 = (1 × 3) / (2 × 4) = 3/8&lt;/span&gt;
                &lt;/p&gt;
                &lt;p class="text-gray-700 leading-relaxed"&gt;
                    &lt;strong&gt;Divisão:&lt;/strong&gt; A regra é: "mantém a primeira e multiplica pelo inverso da segunda".
                    &lt;br /&gt;&lt;span class="font-mono text-lg text-gray-800"&gt;Ex: 1/2 ÷ 3/4 = 1/2 × 4/3 = (1 × 4) / (2 × 3) = 4/6 (que pode ser simplificado para 2/3)&lt;/span&gt;
                &lt;/p&gt;
            &lt;/div&gt;
        &lt;/section&gt;

        &lt;!-- Curiosities Section --&gt;
        &lt;section class="section-card" id="curiosidades"&gt;
            &lt;h2 class="text-2xl md:text-3xl font-bold text-gray-800 mb-4 flex items-center"&gt;
                &lt;i class="fas fa-lightbulb text-yellow-500 mr-3"&gt;&lt;/i&gt; Curiosidades dos Números Racionais
            &lt;/h2&gt;
            &lt;ul class="list-disc list-inside text-gray-700 leading-relaxed space-y-2"&gt;
                &lt;li&gt;Você sabia que o nosso sistema monetário (dinheiro) é baseado em números decimais? R$ 2,50 é um exemplo!&lt;/li&gt;
                &lt;li&gt;A culinária utiliza muito as frações! Meia xícara de farinha, um terço de uma colher de chá...&lt;/li&gt;
                &lt;li&gt;As partituras musicais usam frações para indicar a duração das notas!&lt;/li&gt;
            &lt;/ul&gt;
        &lt;/section&gt;

    &lt;/main&gt;

    &lt;script&gt;
        // Quiz de Frações
        document.addEventListener('DOMContentLoaded', () =&gt; {
            const quizOptions = document.querySelectorAll('#quiz-options .quiz-option');
            const quizFeedback = document.getElementById('quiz-feedback');
            const correctAnswer = "6"; // The correct answer for 3/4 of 8 is 6

            quizOptions.forEach(option =&gt; {
                option.addEventListener('click', () =&gt; {
                    // Reset previous selections
                    quizOptions.forEach(opt =&gt; {
                        opt.classList.remove('correct', 'incorrect');
                    });

                    const selectedAnswer = option.dataset.answer;
                    if (selectedAnswer === correctAnswer) {
                        option.classList.add('correct');
                        quizFeedback.textContent = 'Parabéns! Resposta correta!';
                        quizFeedback.classList.remove('hidden', 'error');
                        quizFeedback.classList.add('success');
                    } else {
                        option.classList.add('incorrect');
                        quizFeedback.textContent = 'Ops! Resposta incorreta. Tente novamente!';
                        quizFeedback.classList.remove('hidden', 'success');
                        quizFeedback.classList.add('error');
                    }
                });
            });

            // Conversor de Fração para Decimal
            const numeratorInput = document.getElementById('numerator');
            const denominatorInput = document.getElementById('denominator');
            const convertBtn = document.getElementById('convert-btn');
            const decimalResult = document.getElementById('decimal-result');
            const conversionFeedback = document.getElementById('conversion-feedback');

            convertBtn.addEventListener('click', () =&gt; {
                const numerator = parseFloat(numeratorInput.value);
                const denominator = parseFloat(denominatorInput.value);

                conversionFeedback.classList.add('hidden'); // Hide previous feedback
                conversionFeedback.classList.remove('success', 'error');

                if (isNaN(numerator) || isNaN(denominator)) {
                    conversionFeedback.textContent = 'Por favor, insira números válidos.';
                    conversionFeedback.classList.remove('hidden');
                    conversionFeedback.classList.add('error');
                    decimalResult.textContent = '';
                    return;
                }

                if (denominator === 0) {
                    conversionFeedback.textContent = 'O denominador não pode ser zero!';
                    conversionFeedback.classList.remove('hidden');
                    conversionFeedback.classList.add('error');
                    decimalResult.textContent = '';
                    return;
                }

                const result = numerator / denominator;
                decimalResult.textContent = `Resultado: ${result.toFixed(4)}`; // Limit to 4 decimal places for clarity
                conversionFeedback.textContent = 'Conversão realizada com sucesso!';
                conversionFeedback.classList.remove('hidden');
                conversionFeedback.classList.add('success');
            });

            // Reta Numérica Interativa (Arrastar e Soltar)
            const draggableFraction = document.getElementById('draggable-fraction');
            const numberLineContainer = document.querySelector('.number-line-container');
            const checkNumberLineBtn = document.getElementById('check-number-line');
            const resetNumberLineBtn = document.getElementById('reset-number-line');
            const numberLineFeedback = document.getElementById('number-line-feedback');

            let isDragging = false;
            let initialX;
            let offsetX = 0; // Offset from the left of the container

            // Set initial position for the draggable fraction (1/2 = 0.5)
            // The line goes from 0 to 3. So 0.5 is at (0.5 / 3) * 100% = 16.66%
            const initialFractionValue = 0.5; // Represents 1/2
            const lineRange = 3; // The number line goes from 0 to 3
            const initialPositionPercentage = (initialFractionValue / lineRange) * 100;
            draggableFraction.style.left = `${initialPositionPercentage}%`;
            draggableFraction.style.transform = 'translate(-50%, -50%)'; // Center it

            draggableFraction.addEventListener('mousedown', (e) =&gt; {
                isDragging = true;
                initialX = e.clientX;
                offsetX = draggableFraction.offsetLeft;
                draggableFraction.style.cursor = 'grabbing';
            });

            document.addEventListener('mousemove', (e) =&gt; {
                if (!isDragging) return;

                const containerRect = numberLineContainer.getBoundingClientRect();
                let newX = e.clientX - containerRect.left;

                // Clamp the position within the container boundaries
                newX = Math.max(0, Math.min(newX, containerRect.width));

                draggableFraction.style.left = `${(newX / containerRect.width) * 100}%`;
            });

            document.addEventListener('mouseup', () =&gt; {
                isDragging = false;
                draggableFraction.style.cursor = 'grab';
            });

            checkNumberLineBtn.addEventListener('click', () =&gt; {
                const containerRect = numberLineContainer.getBoundingClientRect();
                const fractionRect = draggableFraction.getBoundingClientRect();

                // Calculate the position of the center of the draggable element relative to the container
                const fractionCenter = fractionRect.left + (fractionRect.width / 2) - containerRect.left;

                // Convert pixel position to a value on the number line (0 to 3)
                const valueOnLine = (fractionCenter / containerRect.width) * lineRange;

                // For 1/2, the target value is 0.5
                const targetValue = 0.5;
                const tolerance = 0.1; // Allow for a small margin of error

                numberLineFeedback.classList.add('hidden'); // Hide previous feedback
                numberLineFeedback.classList.remove('success', 'error');

                if (Math.abs(valueOnLine - targetValue) &lt; tolerance) {
                    numberLineFeedback.textContent = 'Excelente! Você posicionou 1/2 corretamente!';
                    numberLineFeedback.classList.remove('hidden');
                    numberLineFeedback.classList.add('success');
                } else {
                    numberLineFeedback.textContent = `Tente novamente! 1/2 está mais próximo de ${targetValue.toFixed(1)}. Sua posição: ${valueOnLine.toFixed(2)}`;
                    numberLineFeedback.classList.remove('hidden');
                    numberLineFeedback.classList.add('error');
                }
            });

            resetNumberLineBtn.addEventListener('click', () =&gt; {
                draggableFraction.style.left = `${initialPositionPercentage}%`;
                draggableFraction.style.transform = 'translate(-50%, -50%)';
                numberLineFeedback.classList.add('hidden');
            });

            // Handle touch events for draggable fraction
            draggableFraction.addEventListener('touchstart', (e) =&gt; {
                isDragging = true;
                initialX = e.touches[0].clientX;
                offsetX = draggableFraction.offsetLeft;
                draggableFraction.style.cursor = 'grabbing';
                e.preventDefault(); // Prevent scrolling while dragging
            });

            document.addEventListener('touchmove', (e) =&gt; {
                if (!isDragging) return;

                const containerRect = numberLineContainer.getBoundingClientRect();
                let newX = e.touches[0].clientX - containerRect.left;

                newX = Math.max(0, Math.min(newX, containerRect.width));

                draggableFraction.style.left = `${(newX / containerRect.width) * 100}%`;
                e.preventDefault(); // Prevent scrolling while dragging
            });

            document.addEventListener('touchend', () =&gt; {
                isDragging = false;
                draggableFraction.style.cursor = 'grab';
            });

            console.log("Script JavaScript carregado e executado."); // Adicionado para depuração
        });
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;