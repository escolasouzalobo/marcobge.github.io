---
layout: post
title: "Post Sem Titulo"
date: 2025-07-26
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Produtos Notáveis - Aprenda de Forma Divertida&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background-color: #f0f8ff;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 1em;
        }
        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            padding: 20px;
        }
        .card {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            margin: 15px;
            padding: 20px;
            width: 300px;
            transition: transform 0.3s;
        }
        .card:hover {
            transform: scale(1.05);
        }
        .formula {
            font-size: 1.5em;
            text-align: center;
            margin: 15px 0;
            color: #2E8B57;
        }
        .interactive-area {
            border: 2px dashed #4CAF50;
            padding: 15px;
            margin-top: 15px;
            border-radius: 8px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background-color: #45a049;
        }
        input {
            padding: 8px;
            margin: 5px 0;
            width: 100%;
            box-sizing: border-box;
        }
        #result {
            font-weight: bold;
            margin-top: 10px;
        }
        .visualization {
            width: 100%;
            height: 200px;
            background-color: #f9f9f9;
            margin-top: 15px;
            position: relative;
        }
        .square {
            position: absolute;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;header&gt;
        &lt;h1&gt;Produtos Notáveis&lt;/h1&gt;
        &lt;p&gt;Aprenda de forma interativa e divertida!&lt;/p&gt;
    &lt;/header&gt;

    &lt;div class="container"&gt;
        &lt;!-- Quadrado da Soma --&gt;
        &lt;div class="card"&gt;
            &lt;h2&gt;Quadrado da Soma&lt;/h2&gt;
            &lt;div class="formula"&gt;(a + b)² = a² + 2ab + b²&lt;/div&gt;
            &lt;p&gt;O quadrado da soma de dois termos é igual ao quadrado do primeiro, mais duas vezes o produto do primeiro pelo segundo, mais o quadrado do segundo.&lt;/p&gt;
            
            &lt;div class="interactive-area"&gt;
                &lt;h3&gt;Experimente!&lt;/h3&gt;
                &lt;label for="a1"&gt;Valor de a:&lt;/label&gt;
                &lt;input type="number" id="a1" placeholder="Digite um número"&gt;
                
                &lt;label for="b1"&gt;Valor de b:&lt;/label&gt;
                &lt;input type="number" id="b1" placeholder="Digite um número"&gt;
                
                &lt;button onclick="calcularQuadradoSoma()"&gt;Calcular&lt;/button&gt;
                &lt;div id="result1"&gt;&lt;/div&gt;
            &lt;/div&gt;
            
            &lt;div class="visualization" id="vis1"&gt;&lt;/div&gt;
        &lt;/div&gt;

        &lt;!-- Quadrado da Diferença --&gt;
        &lt;div class="card"&gt;
            &lt;h2&gt;Quadrado da Diferença&lt;/h2&gt;
            &lt;div class="formula"&gt;(a - b)² = a² - 2ab + b²&lt;/div&gt;
            &lt;p&gt;O quadrado da diferença de dois termos é igual ao quadrado do primeiro, menos duas vezes o produto do primeiro pelo segundo, mais o quadrado do segundo.&lt;/p&gt;
            
            &lt;div class="interactive-area"&gt;
                &lt;h3&gt;Experimente!&lt;/h3&gt;
                &lt;label for="a2"&gt;Valor de a:&lt;/label&gt;
                &lt;input type="number" id="a2" placeholder="Digite um número"&gt;
                
                &lt;label for="b2"&gt;Valor de b:&lt;/label&gt;
                &lt;input type="number" id="b2" placeholder="Digite um número"&gt;
                
                &lt;button onclick="calcularQuadradoDiferenca()"&gt;Calcular&lt;/button&gt;
                &lt;div id="result2"&gt;&lt;/div&gt;
            &lt;/div&gt;
            
            &lt;div class="visualization" id="vis2"&gt;&lt;/div&gt;
        &lt;/div&gt;

        &lt;!-- Produto da Soma pela Diferença --&gt;
        &lt;div class="card"&gt;
            &lt;h2&gt;Produto da Soma pela Diferença&lt;/h2&gt;
            &lt;div class="formula"&gt;(a + b)(a - b) = a² - b²&lt;/div&gt;
            &lt;p&gt;O produto da soma pela diferença de dois termos é igual ao quadrado do primeiro termo menos o quadrado do segundo termo.&lt;/p&gt;
            
            &lt;div class="interactive-area"&gt;
                &lt;h3&gt;Experimente!&lt;/h3&gt;
                &lt;label for="a3"&gt;Valor de a:&lt;/label&gt;
                &lt;input type="number" id="a3" placeholder="Digite um número"&gt;
                
                &lt;label for="b3"&gt;Valor de b:&lt;/label&gt;
                &lt;input type="number" id="b3" placeholder="Digite um número"&gt;
                
                &lt;button onclick="calcularSomaVezesDiferenca()"&gt;Calcular&lt;/button&gt;
                &lt;div id="result3"&gt;&lt;/div&gt;
            &lt;/div&gt;
            
            &lt;div class="visualization" id="vis3"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        // Funções para cálculos interativos
        function calcularQuadradoSoma() {
            const a = parseFloat(document.getElementById('a1').value) || 0;
            const b = parseFloat(document.getElementById('b1').value) || 0;
            const resultado = a*a + 2*a*b + b*b;
            document.getElementById('result1').innerHTML = 
                `(${a} + ${b})² = ${a}² + 2·${a}·${b} + ${b}² = ${resultado}`;
            
            // Atualizar visualização geométrica
            visualizarQuadrado(a, b, 'vis1', true);
        }
        
        function calcularQuadradoDiferenca() {
            const a = parseFloat(document.getElementById('a2').value) || 0;
            const b = parseFloat(document.getElementById('b2').value) || 0;
            const resultado = a*a - 2*a*b + b*b;
            document.getElementById('result2').innerHTML = 
                `(${a} - ${b})² = ${a}² - 2·${a}·${b} + ${b}² = ${resultado}`;
            
            // Atualizar visualização geométrica
            visualizarQuadrado(a, b, 'vis2', false);
        }
        
        function calcularSomaVezesDiferenca() {
            const a = parseFloat(document.getElementById('a3').value) || 0;
            const b = parseFloat(document.getElementById('b3').value) || 0;
            const resultado = a*a - b*b;
            document.getElementById('result3').innerHTML = 
                `(${a} + ${b})(${a} - ${b}) = ${a}² - ${b}² = ${resultado}`;
            
            // Atualizar visualização geométrica
            visualizarSomaDiferenca(a, b, 'vis3');
        }
        
        // Funções para visualização geométrica
        function visualizarQuadrado(a, b, elementId, isSoma) {
            const container = document.getElementById(elementId);
            container.innerHTML = '';
            
            const scale = 20; // Escala para visualização
            const total = a + b;
            
            // Criar quadrado grande (a+b)²
            const bigSquare = document.createElement('div');
            bigSquare.className = 'square';
            bigSquare.style.width = `${total*scale}px`;
            bigSquare.style.height = `${total*scale}px`;
            bigSquare.style.backgroundColor = '#4CAF50';
            bigSquare.style.border = '2px solid #2E8B57';
            bigSquare.innerText = `(${a} ${isSoma ? '+' : '-'} ${b})²`;
            container.appendChild(bigSquare);
            
            // Criar subdivisões
            if (a &gt; 0) {
                const aSquare = document.createElement('div');
                aSquare.className = 'square';
                aSquare.style.width = `${a*scale}px`;
                aSquare.style.height = `${a*scale}px`;
                aSquare.style.backgroundColor = '#FF6347';
                aSquare.innerText = `a² (${a*a})`;
                container.appendChild(aSquare);
            }
            
            if (b &gt; 0) {
                const bSquare = document.createElement('div');
                bSquare.className = 'square';
                bSquare.style.width = `${b*scale}px`;
                bSquare.style.height = `${b*scale}px`;
                bSquare.style.backgroundColor = '#4682B4';
                bSquare.style.left = `${isSoma ? (a*scale) : 0}px`;
                bSquare.style.top = `${isSoma ? (a*scale) : 0}px`;
                bSquare.innerText = `b² (${b*b})`;
                container.appendChild(bSquare);
                
                if (a &gt; 0) {
                    const abRect1 = document.createElement('div');
                    abRect1.className = 'square';
                    abRect1.style.width = `${a*scale}px`;
                    abRect1.style.height = `${b*scale}px`;
                    abRect1.style.backgroundColor = '#FFD700';
                    abRect1.style.left = `${isSoma ? 0 : (a*scale)}px`;
                    abRect1.style.top = `${isSoma ? (a*scale) : 0}px`;
                    abRect1.innerText = `ab (${a*b})`;
                    container.appendChild(abRect1);
                    
                    const abRect2 = document.createElement('div');
                    abRect2.className = 'square';
                    abRect2.style.width = `${b*scale}px`;
                    abRect2.style.height = `${a*scale}px`;
                    abRect2.style.backgroundColor = '#FFD700';
                    abRect2.style.left = `${isSoma ? (a*scale) : 0}px`;
                    abRect2.style.top = `${isSoma ? 0 : (b*scale)}px`;
                    abRect2.innerText = `ab (${a*b})`;
                    container.appendChild(abRect2);
                }
            }
        }
        
        function visualizarSomaDiferenca(a, b, elementId) {
            const container = document.getElementById(elementId);
            container.innerHTML = '';
            
            const scale = 20; // Escala para visualização
            
            // Criar quadrado a²
            const aSquare = document.createElement('div');
            aSquare.className = 'square';
            aSquare.style.width = `${a*scale}px`;
            aSquare.style.height = `${a*scale}px`;
            aSquare.style.backgroundColor = '#FF6347';
            aSquare.innerText = `a² (${a*a})`;
            container.appendChild(aSquare);
            
            if (b &gt; 0) {
                // Criar quadrado b² para subtrair
                const bSquare = document.createElement('div');
                bSquare.className = 'square';
                bSquare.style.width = `${b*scale}px`;
                bSquare.style.height = `${b*scale}px`;
                bSquare.style.backgroundColor = '#4682B4';
                bSquare.style.left = `${(a-b)*scale}px`;
                bSquare.style.top = `${(a-b)*scale}px`;
                bSquare.innerText = `b² (${b*b})`;
                container.appendChild(bSquare);
                
                // Adicionar marcação de subtração
                const minus = document.createElement('div');
                minus.className = 'square';
                minus.style.color = 'red';
                minus.style.fontSize = '24px';
                minus.style.left = `${a*scale + 10}px`;
                minus.style.top = '10px';
                minus.innerText = '-';
                minus.style.backgroundColor = 'transparent';
                container.appendChild(minus);
            }
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;