---
layout: post
title: "Post Sem Titulo"
date: 2025-07-22
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Equações do 2º Grau&lt;/title&gt;
    &lt;!-- Tailwind CSS CDN --&gt;
    &lt;script src="https://cdn.tailwindcss.com"&gt;&lt;/script&gt;
    &lt;style&gt;
        /* Define a fonte Inter para todo o corpo */
        body {
            font-family: 'Inter', sans-serif;
        }
        /* Estilos para o display de fórmulas */
        .formula-display {
            font-size: 1.1rem;
            margin-bottom: 1rem;
        }
    &lt;/style&gt;
    &lt;!-- MathJax Configuration - MUST be before loading MathJax script --&gt;
    &lt;script&gt;
        window.MathJax = {
            tex: {
                inlineMath: [['$', '$'], ['\\(', '\\)']],
                displayMath: [['$$', '$$'], ['\\[', '\\]']]
            },
            svg: {
                fontCache: 'global'
            }
        };
    &lt;/script&gt;
    &lt;!-- MathJax Script --&gt;
    &lt;script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js" async&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body class="bg-gradient-to-r from-blue-500 to-purple-600 min-h-screen flex items-center justify-center p-4"&gt;

    &lt;div class="bg-white p-8 rounded-2xl shadow-2xl w-full max-w-md"&gt;
        &lt;h1 class="text-3xl font-extrabold text-center text-gray-800 mb-6"&gt;Equações Completas do 2º Grau&lt;/h1&gt;

        &lt;p class="text-gray-600 text-center mb-6"&gt;
            Uma equação completa do 2º grau tem a forma:
            &lt;span class="block text-lg font-semibold text-blue-700 mt-2 formula-display"&gt;
                $ax^2 + bx + c = 0$
            &lt;/span&gt;
            onde $a \neq 0$.
        &lt;/p&gt;

        &lt;div class="space-y-4 mb-6"&gt;
            &lt;div&gt;
                &lt;label for="a" class="block text-gray-700 text-sm font-bold mb-2"&gt;Coeficiente 'a':&lt;/label&gt;
                &lt;input type="number" id="a" placeholder="Ex: 1" value="1"
                       class="shadow appearance-none border rounded-xl w-full py-3 px-4 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition duration-200 ease-in-out"&gt;
            &lt;/div&gt;
            &lt;div&gt;
                &lt;label for="b" class="block text-gray-700 text-sm font-bold mb-2"&gt;Coeficiente 'b':&lt;/label&gt;
                &lt;input type="number" id="b" placeholder="Ex: -5" value="-5"
                       class="shadow appearance-none border rounded-xl w-full py-3 px-4 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition duration-200 ease-in-out"&gt;
            &lt;/div&gt;
            &lt;div&gt;
                &lt;label for="c" class="block text-gray-700 text-sm font-bold mb-2"&gt;Coeficiente 'c':&lt;/label&gt;
                &lt;input type="number" id="c" placeholder="Ex: 6" value="6"
                       class="shadow appearance-none border rounded-xl w-full py-3 px-4 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition duration-200 ease-in-out"&gt;
            &lt;/div&gt;
        &lt;/div&gt;

        &lt;button id="calculateBtn"
                class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-4 rounded-xl focus:outline-none focus:shadow-outline transform transition duration-300 ease-in-out hover:scale-105"&gt;
            Calcular Raízes
        &lt;/button&gt;

        &lt;div id="results" class="mt-8 p-6 bg-blue-50 rounded-xl shadow-inner hidden"&gt;
            &lt;h2 class="text-xl font-bold text-gray-800 mb-4"&gt;Resultados:&lt;/h2&gt;
            &lt;div id="steps" class="text-gray-700 space-y-3"&gt;
                &lt;!-- Steps will be inserted here by JavaScript --&gt;
            &lt;/div&gt;
            &lt;div id="errorMessage" class="text-red-600 font-semibold mt-4 hidden"&gt;&lt;/div&gt;
        &lt;/div&gt;
        &lt;div id="mathJaxStatus" class="text-xs text-center text-gray-500 mt-4"&gt;&lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        // Function to handle MathJax typesetting for dynamic content
        function typesetMathJaxDynamic() {
            if (window.MathJax) {
                window.MathJax.typesetPromise([document.getElementById('steps')]).catch(err =&gt; {
                    console.error('MathJax dynamic typesetting failed:', err);
                    document.getElementById('errorMessage').textContent = 'Erro ao processar fórmulas. Verifique o console.';
                    document.getElementById('errorMessage').classList.remove('hidden');
                });
            }
        }

        // Event listener for the calculate button
        document.getElementById('calculateBtn').addEventListener('click', calculateQuadraticEquation);

        function calculateQuadraticEquation() {
            const a = parseFloat(document.getElementById('a').value);
            const b = parseFloat(document.getElementById('b').value);
            const c = parseFloat(document.getElementById('c').value);

            const resultsDiv = document.getElementById('results');
            const stepsDiv = document.getElementById('steps');
            const errorMessageDiv = document.getElementById('errorMessage');

            stepsDiv.innerHTML = ''; // Limpa os passos anteriores
            errorMessageDiv.textContent = ''; // Limpa mensagens de erro
            resultsDiv.classList.add('hidden'); // Esconde os resultados por padrão

            // Validação do coeficiente 'a'
            if (isNaN(a) || isNaN(b) || isNaN(c)) {
                errorMessageDiv.textContent = 'Por favor, insira valores numéricos válidos para a, b e c.';
                errorMessageDiv.classList.remove('hidden');
                return;
            }

            if (a === 0) {
                errorMessageDiv.textContent = 'O coeficiente "a" não pode ser zero para uma equação do 2º grau completa.';
                errorMessageDiv.classList.remove('hidden');
                return;
            }

            // Mostra a seção de resultados
            resultsDiv.classList.remove('hidden');

            // Passo 1: Apresentar a equação
            addStep(`Equação: $${a}x^2 + ${b}x + ${c} = 0$`);

            // Passo 2: Calcular o discriminante (Delta)
            const delta = b * b - 4 * a * c;
            addStep(`Calculando o discriminante ($\\Delta$):`);
            addStep(`$\\Delta = b^2 - 4ac$`);
            addStep(`$\\Delta = (${b})^2 - 4(${a})(${c})$`);
            addStep(`$\\Delta = ${b*b} - ${4*a*c}$`);
            addStep(`$\\Delta = ${delta}$`);

            // Passo 3: Analisar o valor de Delta e calcular as raízes
            if (delta &lt; 0) {
                addStep(`Como $\\Delta &lt; 0$ (${delta} &lt; 0), a equação não possui raízes reais.`);
            } else if (delta === 0) {
                addStep(`Como $\\Delta = 0$, a equação possui uma única raiz real (ou duas raízes reais iguais).`);
                addStep(`Calculando a raiz:`);
                addStep(`$x = \\frac{-b \\pm \\sqrt{\\Delta}}{2a}$`);
                addStep(`$x = \\frac{-(${b}) \\pm \\sqrt{0}}{2(${a})}$`);
                addStep(`$x = \\frac{${-b}}{${2*a}}$`);
                const x = -b / (2 * a);
                addStep(`$x = ${x.toFixed(4)}$`);
            } else {
                addStep(`Como $\\Delta &gt; 0$ (${delta} &gt; 0), a equação possui duas raízes reais distintas.`);
                addStep(`Calculando as raízes usando a fórmula de Bhaskara:`);
                addStep(`$x = \\frac{-b \\pm \\sqrt{\\Delta}}{2a}$`);
                addStep(`$x_1 = \\frac{-(${b}) + \\sqrt{${delta}}}{2(${a})}$`);
                addStep(`$x_2 = \\frac{-(${b}) - \\sqrt{${delta}}}{2(${a})}$`);

                const sqrtDelta = Math.sqrt(delta);
                addStep(`$\\sqrt{\\Delta} = \\sqrt{${delta}} \\approx ${sqrtDelta.toFixed(4)}$`);

                const x1 = (-b + sqrtDelta) / (2 * a);
                const x2 = (-b - sqrtDelta) / (2 * a);

                addStep(`$x_1 = \\frac{${-b} + ${sqrtDelta.toFixed(4)}}{${2*a}}$`);
                addStep(`$x_1 = \\frac{${(-b + sqrtDelta).toFixed(4)}}{${(2*a)}}$`);
                addStep(`$x_1 \\approx ${x1.toFixed(4)}$`);

                addStep(`$x_2 = \\frac{${-b} - ${sqrtDelta.toFixed(4)}}{${2*a}}$`);
                addStep(`$x_2 = \\frac{${(-b - sqrtDelta).toFixed(4)}}{${(2*a)}}$`);
                addStep(`$x_2 \\approx ${x2.toFixed(4)}$`);
            }

            // Processa as novas fórmulas com MathJax
            typesetMathJaxDynamic();
        }

        // Função auxiliar para adicionar passos à div de resultados
        function addStep(text) {
            const p = document.createElement('p');
            p.innerHTML = text; // Usar innerHTML para interpretar tags MathJax
            document.getElementById('steps').appendChild(p);
        }

        // Initial MathJax typesetting for static content and status update
        document.addEventListener('DOMContentLoaded', () =&gt; {
            if (window.MathJax) {
                window.MathJax.typesetPromise().then(() =&gt; {
                    const statusDiv = document.getElementById('mathJaxStatus');
                    statusDiv.textContent = 'Fórmulas carregadas com MathJax.';
                    statusDiv.classList.add('text-green-600');
                    setTimeout(() =&gt; {
                        statusDiv.classList.remove('text-green-600');
                        statusDiv.textContent = '';
                    }, 3000);
                }).catch(err =&gt; {
                    console.error('MathJax initial typesetting failed:', err);
                    const statusDiv = document.getElementById('mathJaxStatus');
                    statusDiv.textContent = 'Erro ao carregar fórmulas. Verifique o console.';
                    statusDiv.classList.add('text-red-600');
                });
            } else {
                const statusDiv = document.getElementById('mathJaxStatus');
                statusDiv.textContent = 'MathJax não carregado. Verifique a conexão ou o console.';
                statusDiv.classList.add('text-red-600');
            }
        });
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;