---
layout: post
title: "Post Sem Titulo"
date: 2025-08-06
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;&lt;/meta&gt;
    &lt;meta content="width=device-width, initial-scale=1.0" name="viewport"&gt;&lt;/meta&gt;
    &lt;title&gt;Sequências Recursivas&lt;/title&gt;
    &lt;!-- Inclui Tailwind CSS para estilização --&gt;
    &lt;script src="https://cdn.tailwindcss.com"&gt;&lt;/script&gt;
    &lt;link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&amp;amp;display=swap" rel="stylesheet"&gt;&lt;/link&gt;
    &lt;style&gt;
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f4f8; /* Cor de fundo suave */
        }
        .container {
            max-width: 800px;
        }
        .term {
            min-width: 60px; /* Garante que os termos tenham largura mínima */
            display: inline-flex;
            justify-content: center;
            align-items: center;
            height: 40px;
        }
        input[type="number"], input[type="text"] {
            -moz-appearance: textfield; /* Remove setas em Firefox */
        }
        input::-webkit-outer-spin-button,
        input::-webkit-inner-spin-button {
            -webkit-appearance: none; /* Remove setas em Chrome/Safari */
            margin: 0;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body class="flex items-center justify-center min-h-screen p-4"&gt;
    &lt;div class="container bg-white rounded-xl shadow-2xl p-8 sm:p-12 border-4 border-blue-500"&gt;
        &lt;h1 class="text-4xl font-extrabold text-center text-blue-700 mb-6"&gt;
            Desafio das Sequências Recursivas 🧠
        &lt;/h1&gt;
        &lt;p class="text-lg text-gray-700 text-center mb-8"&gt;
            Vamos praticar o que aprendemos sobre sequências recursivas!
        &lt;/p&gt;

        &lt;div class="bg-blue-50 p-6 rounded-lg shadow-inner mb-8"&gt;
            &lt;p class="text-xl font-semibold text-blue-800 mb-4 text-center" id="question-text"&gt;
                Carregando exercício...
            &lt;/p&gt;
            &lt;div class="flex flex-wrap justify-center items-center gap-2 sm:gap-4 mb-6" id="sequence-container"&gt;
                &lt;!-- A sequência será carregada aqui pelo JavaScript --&gt;
            &lt;/div&gt;
            &lt;div class="text-lg font-bold text-center mt-4" id="feedback-text"&gt;
                &lt;!-- Feedback sobre a resposta será exibido aqui --&gt;
            &lt;/div&gt;
        &lt;/div&gt;

        &lt;div class="flex justify-center gap-4"&gt;
            &lt;button class="px-8 py-3 bg-green-600 text-white font-bold rounded-lg shadow-md hover:bg-green-700 transition duration-300 ease-in-out transform hover:scale-105 focus:outline-none focus:ring-4 focus:ring-green-300" id="check-button"&gt;
                Verificar
            &lt;/button&gt;
            &lt;button class="hidden px-8 py-3 bg-blue-600 text-white font-bold rounded-lg shadow-md hover:bg-blue-700 transition duration-300 ease-in-out transform hover:scale-105 focus:outline-none focus:ring-4 focus:ring-blue-300" id="next-button"&gt;
                Próximo Exercício
            &lt;/button&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        // Dados dos exercícios, incluindo o tipo, a regra e a função para gerar a sequência
        const exercises = [
            {
                type: 'complete',
                sequenceType: 'geometric', // Cada termo é o dobro do anterior
                start: 1,
                length: 5, // Exibe 5 termos, o usuário preenche 2
                missingCount: 2,
                question: 'Complete a sequência (lembre-se da Sequência II do texto):',
                ruleDescription: 'Cada termo é o dobro do anterior.',
                generate: (start, length) =&gt; {
                    let seq = [start];
                    for (let i = 1; i &lt; length; i++) {
                        seq.push(seq[i - 1] * 2);
                    }
                    return seq;
                }
            },
            {
                type: 'complete',
                sequenceType: 'fibonacci',
                start: [1, 1], // Início da sequência de Fibonacci
                length: 7, // Exibe 7 termos, o usuário preenche 2
                missingCount: 2,
                question: 'Complete a sequência de Fibonacci (lembre-se da Sequência III do texto):',
                ruleDescription: 'Cada termo é a soma dos dois termos anteriores.',
                generate: (start, length) =&gt; {
                    let seq = [...start];
                    while (seq.length &lt; length) {
                        seq.push(seq[seq.length - 1] + seq[seq.length - 2]);
                    }
                    return seq;
                }
            },
            {
                type: 'complete',
                sequenceType: 'arithmetic', // Cada termo adiciona uma constante
                start: 2,
                commonDiff: 6, // Alterado de 3 para 6 para corresponder à sequência 2, 8, 14...
                length: 6, // Exibe 6 termos, o usuário preenche 2
                missingCount: 2,
                question: 'Complete a sequência:',
                ruleDescription: 'Cada termo é obtido adicionando 6 ao termo anterior.', // Regra atualizada
                generate: (start, commonDiff, length) =&gt; {
                    let seq = [start];
                    for (let i = 1; i &lt; length; i++) {
                        seq.push(seq[i - 1] + commonDiff);
                    }
                    return seq;
                }
            },
            {
                type: 'identify_rule',
                sequenceType: 'geometric',
                start: 5,
                length: 5,
                question: 'Observe a sequência. Qual é a regra de formação?',
                correctAnswer: 'multiplica por 2', // Resposta esperada para comparação
                ruleDescription: 'Cada termo é o anterior multiplicado por 2.',
                generate: (start, length) =&gt; {
                    let seq = [start];
                    for (let i = 1; i &lt; length; i++) {
                        seq.push(seq[i - 1] * 2);
                    }
                    return seq;
                }
            },
            {
                type: 'identify_rule',
                sequenceType: 'arithmetic',
                start: 10,
                commonDiff: -2,
                length: 5,
                question: 'Observe a sequência. Qual é a regra de formação?',
                correctAnswer: 'subtrai 2',
                ruleDescription: 'Cada termo é o anterior subtraído por 2.',
                generate: (start, commonDiff, length) =&gt; {
                    let seq = [start];
                    for (let i = 1; i &lt; length; i++) {
                        seq.push(seq[i - 1] + commonDiff);
                    }
                    return seq;
                }
            },
            {
                type: 'identify_rule',
                sequenceType: 'squared',
                start: 2,
                length: 4, // Gera: 2, 4, 16, 256
                question: 'Observe a sequência. Qual é a regra de formação?',
                correctAnswer: 'eleva ao quadrado',
                ruleDescription: 'Cada termo é o anterior elevado ao quadrado.',
                generate: (start, length) =&gt; {
                    let seq = [start];
                    for (let i = 1; i &lt; length; i++) {
                        seq.push(seq[i - 1] * seq[i - 1]);
                    }
                    return seq;
                }
            }
        ];

        let currentExerciseIndex = 0;
        let currentExercise = null;
        let sequenceData = []; // A sequência completa gerada para o exercício atual

        // Função para carregar um novo exercício
        function loadExercise() {
            currentExercise = exercises[currentExerciseIndex];
            let sequenceContainer = document.getElementById('sequence-container');
            let questionText = document.getElementById('question-text');
            let feedbackText = document.getElementById('feedback-text');
            let checkButton = document.getElementById('check-button');
            let nextButton = document.getElementById('next-button');

            questionText.textContent = currentExercise.question;
            feedbackText.textContent = ''; // Limpa feedback anterior
            checkButton.classList.remove('hidden'); // Mostra o botão Verificar
            nextButton.classList.add('hidden'); // Esconde o botão Próximo

            sequenceContainer.innerHTML = ''; // Limpa a sequência anterior

            if (currentExercise.type === 'complete') {
                // Gera a sequência completa
                sequenceData = currentExercise.generate(currentExercise.start, currentExercise.length, currentExercise.commonDiff);
                const displayLength = currentExercise.length - currentExercise.missingCount;

                // Cria os elementos da sequência (termos e inputs)
                for (let i = 0; i &lt; currentExercise.length; i++) {
                    let span = document.createElement('span');
                    span.className = 'term px-3 py-2 bg-blue-100 rounded-md shadow-sm text-blue-800 font-semibold';
                    if (i &lt; displayLength) {
                        span.textContent = sequenceData[i]; // Exibe termos conhecidos
                    } else {
                        let input = document.createElement('input');
                        input.type = 'number';
                        input.className = 'w-20 px-3 py-2 border-2 border-blue-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 text-center text-blue-800 font-semibold';
                        input.placeholder = '?';
                        input.dataset.index = i; // Armazena o índice para verificação
                        span.appendChild(input);
                    }
                    sequenceContainer.appendChild(span);
                    if (i &lt; currentExercise.length - 1) {
                        let separator = document.createElement('span');
                        separator.textContent = ', ';
                        separator.className = 'mx-1 text-gray-700';
                        sequenceContainer.appendChild(separator);
                    }
                }
                let ellipsis = document.createElement('span');
                ellipsis.textContent = '...';
                ellipsis.className = 'mx-1 text-gray-700';
                sequenceContainer.appendChild(ellipsis);

                checkButton.onclick = checkCompleteExercise; // Define a função de verificação
            } else if (currentExercise.type === 'identify_rule') {
                // Gera a sequência para identificação da regra
                sequenceData = currentExercise.generate(currentExercise.start, currentExercise.length, currentExercise.commonDiff);
                sequenceContainer.textContent = sequenceData.join(', ') + ', ...';

                // Cria o campo de input para a regra
                let input = document.createElement('input');
                input.type = 'text';
                input.className = 'w-full mt-4 px-3 py-2 border-2 border-blue-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 text-blue-800 font-semibold';
                input.placeholder = 'Digite a regra aqui (ex: "Soma 3", "Multiplica por 2")';
                input.id = 'rule-input';
                sequenceContainer.appendChild(input);

                checkButton.onclick = checkIdentifyRuleExercise; // Define a função de verificação
            }
        }

        // Função para verificar exercícios de completar sequência
        function checkCompleteExercise() {
            let inputs = document.querySelectorAll('#sequence-container input[type="number"]');
            let allCorrect = true;
            inputs.forEach(input =&gt; {
                const index = parseInt(input.dataset.index);
                const userAnswer = parseFloat(input.value); // Converte para número

                if (isNaN(userAnswer) || userAnswer !== sequenceData[index]) {
                    allCorrect = false;
                    input.classList.add('border-red-500');
                    input.classList.remove('border-blue-300', 'border-green-500');
                } else {
                    input.classList.add('border-green-500');
                    input.classList.remove('border-blue-300', 'border-red-500');
                }
            });

            let feedbackText = document.getElementById('feedback-text');
            let nextButton = document.getElementById('next-button');
            let checkButton = document.getElementById('check-button');

            if (allCorrect) {
                feedbackText.textContent = 'Parabéns! Resposta correta! 🎉';
                feedbackText.className = 'text-green-700 font-bold mt-4 text-center';
                checkButton.classList.add('hidden'); // Esconde o botão Verificar
                nextButton.classList.remove('hidden'); // Mostra o botão Próximo
            } else {
                feedbackText.textContent = 'Ops! Alguma resposta está incorreta. Tente novamente.';
                feedbackText.className = 'text-red-700 font-bold mt-4 text-center';
            }
        }

        // Função para verificar exercícios de identificar regra
        function checkIdentifyRuleExercise() {
            let ruleInput = document.getElementById('rule-input');
            const userAnswer = ruleInput.value.trim().toLowerCase(); // Pega a resposta do usuário
            const correctAnswer = currentExercise.correctAnswer.toLowerCase(); // Pega a resposta correta

            let feedbackText = document.getElementById('feedback-text');
            let nextButton = document.getElementById('next-button');
            let checkButton = document.getElementById('check-button');

            // Verifica se a resposta do usuário contém as palavras-chave da resposta correta
            if (userAnswer.includes(correctAnswer.split(' ')[0]) &amp;&amp; userAnswer.includes(correctAnswer.split(' ')[1])) {
                feedbackText.textContent = 'Excelente! A regra está correta! 🎉';
                feedbackText.className = 'text-green-700 font-bold mt-4 text-center';
                ruleInput.classList.add('border-green-500');
                ruleInput.classList.remove('border-blue-300', 'border-red-500');
                checkButton.classList.add('hidden');
                nextButton.classList.remove('hidden');
            } else {
                feedbackText.textContent = 'Hmm, a regra não está exatamente como esperado. Dica: ' + currentExercise.ruleDescription;
                feedbackText.className = 'text-red-700 font-bold mt-4 text-center';
                ruleInput.classList.add('border-red-500');
                ruleInput.classList.remove('border-blue-300', 'border-green-500');
            }
        }

        // Função para avançar para o próximo exercício
        function nextExercise() {
            currentExerciseIndex = (currentExerciseIndex + 1) % exercises.length; // Avança para o próximo, ou volta ao início
            loadExercise();
        }

        // Adiciona listeners aos botões
        document.getElementById('next-button').addEventListener('click', nextExercise);

        // Carrega o primeiro exercício quando a página é carregada
        window.onload = loadExercise;
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;&lt;span style="color: #800180;"&gt;&lt;b&gt;
SEQUÊNCIAS&amp;nbsp;&lt;/b&gt;&lt;/span&gt;&lt;div&gt;Na Matemática, utilizamos as sequências numéricas (ou de figuras), que são aquelas que apresentam números escritos (ou figuras dispostas) em determinada ordem preestabelecida. Cada elemento que compõe uma sequência é denominado termo.&amp;nbsp;&lt;/div&gt;&lt;div&gt;A ordem em que o termo aparece é a posição dele na sequência.

Observe estas sequências:&amp;nbsp;&lt;/div&gt;&lt;div&gt;I) 3; 0,5; –1; 4&amp;nbsp;&lt;/div&gt;&lt;div&gt;II) 1, 2, 4, 8, 16, 32, 64, 128, ...&amp;nbsp;&lt;/div&gt;&lt;div&gt;III) 1, 1, 2, 3, 5, 8, 13, 21, ...&amp;nbsp;&lt;/div&gt;&lt;div&gt;Com base nessas sequências, responda:&amp;nbsp;&lt;/div&gt;&lt;div&gt;a) Qual sequência apresenta um número finito de elementos? A sequência I.&amp;nbsp;&lt;/div&gt;&lt;div&gt;&lt;br /&gt;&lt;/div&gt;&lt;div&gt;b) Observe a sequência II: Anote o resultado da divisão de um termo pelo termo que vem imediatamente antes dele. Depois de escolher outros números e repetir o processo, escreva sua conclusão. Que relação podemos fazer entre um termo e o termo que vem imediatamente antes dele? Pode-se concluir que o resultado obtido é sempre o mesmo; cada termo é o dobro do termo anterior.&amp;nbsp;&lt;/div&gt;&lt;div&gt;&lt;br /&gt;&lt;/div&gt;&lt;div&gt;c) A sequência III se chama sequência de Fibonacci. A sequência de Fibonacci foi montada sem uma regra definida como a sequência I ou foi montada com uma regra definida, como a sequência II? Mesmo tipo da sequência II.

Sequências como as sequências II e III são chamadas de sequências &lt;span style="color: red;"&gt;recursivas,&lt;/span&gt; enquanto
sequências como a sequência I são chamadas de sequências &lt;span style="color: red;"&gt;não recursivas&lt;/span&gt;.
Uma sequência é recursiva quando cada termo depende do termo anterior ou de termos anteriores (conhecido o termo inicial).&amp;nbsp;&lt;/div&gt;&lt;div&gt;São exemplos de sequências recursivas:
• 4, 16, 256, 65536 -&amp;gt; o primeiro termo é o número 4 e cada termo seguinte é o termo anterior elevado ao quadrado.&amp;nbsp;&lt;/div&gt;&lt;div class="separator" style="clear: both; text-align: center;"&gt;&lt;a href="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg9dUnSW7SOGk2PtbKQdr8hoFAMIt1x8YlaJJ1dptt661a0JXGzqC2sx7aucKSAhI87vP-5J2dcuel8nIQAzjXhowg_lmOf2m6DlrGcK56m9VXLuQYjhP-WNMMUjAkNp7MN4pQqIzavS_P2yKm-sOPFDwTbBtQ_UR28c9U8ZSCEdpGqaDvd57d0Bz-moCk/s234/sequencia.png" style="clear: left; float: left; margin-bottom: 1em; margin-right: 1em;"&gt;&lt;img border="0" data-original-height="74" data-original-width="234" height="74" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg9dUnSW7SOGk2PtbKQdr8hoFAMIt1x8YlaJJ1dptt661a0JXGzqC2sx7aucKSAhI87vP-5J2dcuel8nIQAzjXhowg_lmOf2m6DlrGcK56m9VXLuQYjhP-WNMMUjAkNp7MN4pQqIzavS_P2yKm-sOPFDwTbBtQ_UR28c9U8ZSCEdpGqaDvd57d0Bz-moCk/s1600/sequencia.png" width="234" /&gt;&lt;/a&gt;&lt;/div&gt;&lt;br /&gt;&lt;div&gt;&lt;br /&gt;&lt;/div&gt;&lt;div&gt;&lt;br /&gt;&lt;/div&gt;&lt;div&gt;&lt;br /&gt;&lt;/div&gt;&lt;div&gt;&lt;br /&gt;&lt;/div&gt;&lt;div&gt;O primeiro termo é um quadradinho e a cada termo adicionam-se dois quadradinhos, um alinhado acima e um alinhado à direita.As duas sequências que vimos como exemplo possuem uma regra que chamamos de &lt;b&gt;lei de formação da sequência.
&lt;/b&gt;&lt;/div&gt;&lt;div&gt;&lt;b&gt;Fonte: A Conquista da Matemática - 7º ano&lt;/b&gt;&lt;/div&gt;