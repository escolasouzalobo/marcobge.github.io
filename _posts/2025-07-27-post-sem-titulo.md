---
layout: post
title: "Post Sem Titulo"
date: 2025-07-27
---

&lt;div class="separator" style="clear: both;"&gt;&lt;a href="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgBdSz69ZuGKCxXsOFpUa0IiT23JTcPpSGTIzEg33az7idCbDswfILYpeQraloHoyYKTVhx8vC6PLsAWEgw6rMmj95FwOBo2I8uxVAhmP693qzuJSnsOWDQ_XUriX7AqKWhE8GcjhKt4Hn14wvT57W_lqw7DUQwQoksQJ1ltB8pp9uGUuVX3yA6Vlg1244/s573/YiE8oN.png" style="display: block; padding: 1em 0px; text-align: center;"&gt;&lt;img alt="" border="0" data-original-height="573" data-original-width="470" height="200" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgBdSz69ZuGKCxXsOFpUa0IiT23JTcPpSGTIzEg33az7idCbDswfILYpeQraloHoyYKTVhx8vC6PLsAWEgw6rMmj95FwOBo2I8uxVAhmP693qzuJSnsOWDQ_XUriX7AqKWhE8GcjhKt4Hn14wvT57W_lqw7DUQwQoksQJ1ltB8pp9uGUuVX3yA6Vlg1244/s200/YiE8oN.png" /&gt;&lt;/a&gt;&lt;/div&gt;&lt;p&gt;&amp;nbsp;&lt;/p&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;&lt;/meta&gt;
    &lt;meta content="width=device-width, initial-scale=1.0" name="viewport"&gt;&lt;/meta&gt;
    &lt;title&gt;Matemática Interativa - Estudo de Funções&lt;/title&gt;
    &lt;script src="https://cdn.jsdelivr.net/npm/chart.js"&gt;&lt;/script&gt;
    &lt;style&gt;
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 1rem;
            text-align: center;
        }
        .container {
            max-width: 1200px;
            margin: auto;
            padding: 20px;
        }
        .section {
            background: white;
            margin: 20px 0;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .graph-container {
            width: 100%;
            max-width: 600px;
            margin: 20px auto;
        }
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }
        .control-group {
            margin-right: 20px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 8px 16px;
            cursor: pointer;
            border-radius: 4px;
        }
        button:hover {
            background-color: #45a049;
        }
        input, select {
            padding: 8px;
            border-radius: 4px;
            border: 1px solid #ddd;
        }
        nav {
            background-color: #333;
            overflow: hidden;
        }
        nav a {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
        }
        nav a:hover {
            background-color: #ddd;
            color: black;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;header&gt;
        &lt;h1&gt;Estudo Interativo de Funções Matemáticas&lt;/h1&gt;
    &lt;/header&gt;
    
    &lt;nav&gt;
        &lt;a href="#conceito"&gt;Conceito de Função&lt;/a&gt;
        &lt;a href="#retas"&gt;Funções Lineares&lt;/a&gt;
        &lt;a href="#quadratica"&gt;Função Quadrática&lt;/a&gt;
    &lt;/nav&gt;
    
    &lt;div class="container"&gt;
        &lt;section class="section" id="conceito"&gt;
            &lt;h2&gt;Conceito de Função&lt;/h2&gt;
            &lt;p&gt;Em matemática, uma função é uma relação entre um conjunto de entradas (domínio) e um conjunto de saídas (contradomínio), onde cada entrada está associada a exatamente uma saída.&lt;/p&gt;
            
            &lt;div class="graph-container"&gt;
                &lt;canvas id="functionDiagram"&gt;&lt;/canvas&gt;
            &lt;/div&gt;
            
            &lt;p&gt;Notação: f: X → Y, onde f é a função, X é o domínio e Y é o contradomínio.&lt;/p&gt;
            &lt;p&gt;Exemplo: f(x) = 2x + 3&lt;/p&gt;
        &lt;/section&gt;
        
        &lt;section class="section" id="retas"&gt;
            &lt;h2&gt;Funções Representadas por Retas (Funções Lineares)&lt;/h2&gt;
            &lt;p&gt;Funções do primeiro grau têm a forma f(x) = ax + b, onde 'a' é o coeficiente angular e 'b' é o coeficiente linear.&lt;/p&gt;
            
            &lt;div class="controls"&gt;
                &lt;div class="control-group"&gt;
                    &lt;label for="linearA"&gt;Coeficiente angular (a):&lt;/label&gt;
                    &lt;input id="linearA" step="0.5" type="number" value="1" /&gt;
                &lt;/div&gt;
                &lt;div class="control-group"&gt;
                    &lt;label for="linearB"&gt;Coeficiente linear (b):&lt;/label&gt;
                    &lt;input id="linearB" step="0.5" type="number" value="0" /&gt;
                &lt;/div&gt;
                &lt;button onclick="updateLinearGraph()"&gt;Atualizar Gráfico&lt;/button&gt;
            &lt;/div&gt;
            
            &lt;div class="graph-container"&gt;
                &lt;canvas id="linearGraph"&gt;&lt;/canvas&gt;
            &lt;/div&gt;
            
            &lt;p&gt;Características:&lt;/p&gt;
            &lt;ul&gt;
                &lt;li&gt;Gráfico é uma reta&lt;/li&gt;
                &lt;li&gt;Raiz: x = -b/a&lt;/li&gt;
                &lt;li&gt;Crescimento: a &amp;gt; 0 (crescente), a &amp;lt; 0 (decrescente)&lt;/li&gt;
            &lt;/ul&gt;
        &lt;/section&gt;
        
        &lt;section class="section" id="quadratica"&gt;
            &lt;h2&gt;Função Quadrática (2º Grau)&lt;/h2&gt;
            &lt;p&gt;Funções do segundo grau têm a forma f(x) = ax² + bx + c, onde a ≠ 0.&lt;/p&gt;
            
            &lt;div class="controls"&gt;
                &lt;div class="control-group"&gt;
                    &lt;label for="quadA"&gt;Coeficiente a:&lt;/label&gt;
                    &lt;input id="quadA" step="0.5" type="number" value="1" /&gt;
                &lt;/div&gt;
                &lt;div class="control-group"&gt;
                    &lt;label for="quadB"&gt;Coeficiente b:&lt;/label&gt;
                    &lt;input id="quadB" step="0.5" type="number" value="0" /&gt;
                &lt;/div&gt;
                &lt;div class="control-group"&gt;
                    &lt;label for="quadC"&gt;Coeficiente c:&lt;/label&gt;
                    &lt;input id="quadC" step="0.5" type="number" value="0" /&gt;
                &lt;/div&gt;
                &lt;button onclick="updateQuadraticGraph()"&gt;Atualizar Gráfico&lt;/button&gt;
            &lt;/div&gt;
            
            &lt;div class="graph-container"&gt;
                &lt;canvas id="quadraticGraph"&gt;&lt;/canvas&gt;
            &lt;/div&gt;
            
            &lt;p&gt;Características:&lt;/p&gt;
            &lt;ul&gt;
                &lt;li&gt;Gráfico é uma parábola&lt;/li&gt;
                &lt;li&gt;Concavidade: a &amp;gt; 0 (para cima), a &amp;lt; 0 (para baixo)&lt;/li&gt;
                &lt;li&gt;Vértice: x = -b/2a, y = -Δ/4a (onde Δ = b² - 4ac)&lt;/li&gt;
                &lt;li&gt;Raízes: x = [-b ± √(b² - 4ac)] / 2a&lt;/li&gt;
            &lt;/ul&gt;
        &lt;/section&gt;
    &lt;/div&gt;
    
    &lt;script&gt;
        // Diagrama do conceito de função
        const conceptCtx = document.getElementById('functionDiagram').getContext('2d');
        // Implementar diagrama de conjuntos aqui
        
        // Gráfico de função linear
        const linearCtx = document.getElementById('linearGraph').getContext('2d');
        let linearChart = new Chart(linearCtx, {
            type: 'line',
            data: {
                datasets: [{
                    label: 'Função Linear',
                    borderColor: 'rgb(75, 192, 192)',
                    tension: 0.1,
                    fill: false
                }]
            },
            options: {
                scales: {
                    x: { type: 'linear', position: 'center' },
                    y: { type: 'linear', position: 'center' }
                }
            }
        });
        
        function updateLinearGraph() {
            const a = parseFloat(document.getElementById('linearA').value);
            const b = parseFloat(document.getElementById('linearB').value);
            
            const data = [];
            for (let x = -10; x &lt;= 10; x += 0.5) {
                data.push({x: x, y: a*x + b});
            }
            
            linearChart.data.datasets[0].data = data;
            linearChart.data.datasets[0].label = `f(x) = ${a}x + ${b}`;
            linearChart.update();
        }
        
        // Gráfico de função quadrática
        const quadCtx = document.getElementById('quadraticGraph').getContext('2d');
        let quadChart = new Chart(quadCtx, {
            type: 'line',
            data: {
                datasets: [{
                    label: 'Função Quadrática',
                    borderColor: 'rgb(255, 99, 132)',
                    tension: 0.1,
                    fill: false
                }]
            },
            options: {
                scales: {
                    x: { type: 'linear', position: 'center' },
                    y: { type: 'linear', position: 'center' }
                }
            }
        });
        
        function updateQuadraticGraph() {
            const a = parseFloat(document.getElementById('quadA').value);
            const b = parseFloat(document.getElementById('quadB').value);
            const c = parseFloat(document.getElementById('quadC').value);
            
            const data = [];
            for (let x = -10; x &lt;= 10; x += 0.5) {
                data.push({x: x, y: a*x*x + b*x + c});
            }
            
            quadChart.data.datasets[0].data = data;
            quadChart.data.datasets[0].label = `f(x) = ${a}x² + ${b}x + ${c}`;
            quadChart.update();
        }
        
        // Inicializar gráficos
        window.onload = function() {
            updateLinearGraph();
            updateQuadraticGraph();
        };
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
&lt;b&gt;&lt;a href="https://www.profmarcovargas.com.br/2025/07/funcao-de-1-grau.html" target="_blank"&gt;Como calcular uma função de 1º grau...&lt;/a&gt;&lt;/b&gt;