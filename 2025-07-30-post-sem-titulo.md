---
layout: post
title: "Post Sem Titulo"
date: 2025-07-30
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Propriedades da Subtração&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
            color: #333;
        }
        h1 {
            color: #2c3e50;
            text-align: center;
        }
        .property {
            background: white;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 15px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .property h2 {
            color: #3498db;
            margin-top: 0;
        }
        .example {
            background: #e8f4fc;
            padding: 10px;
            border-left: 4px solid #3498db;
            margin: 10px 0;
        }
        .interactive {
            background: #e8f4fc;
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
            text-align: center;
        }
        input, button {
            padding: 8px;
            margin: 5px;
            border-radius: 4px;
            border: 1px solid #ccc;
        }
        button {
            background: #3498db;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background: #2980b9;
        }
        #result {
            font-weight: bold;
            margin-top: 10px;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;🔢 Propriedades da Subtração&lt;/h1&gt;
    
    &lt;div class="property"&gt;
        &lt;h2&gt;1. Não Comutativa&lt;/h2&gt;
        &lt;p&gt;A ordem dos números altera o resultado.&lt;/p&gt;
        &lt;div class="example"&gt;
            &lt;p&gt;&lt;strong&gt;Exemplo:&lt;/strong&gt; &lt;code&gt;5 - 3 = 2&lt;/code&gt;, mas &lt;code&gt;3 - 5 = -2&lt;/code&gt;&lt;/p&gt;
        &lt;/div&gt;
        &lt;div class="interactive"&gt;
            &lt;p&gt;Teste você mesmo:&lt;/p&gt;
            &lt;input type="number" id="num1" placeholder="Número 1"&gt;
            &lt;input type="number" id="num2" placeholder="Número 2"&gt;
            &lt;button onclick="testComutativa()"&gt;Calcular&lt;/button&gt;
            &lt;div id="result-comutativa"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;div class="property"&gt;
        &lt;h2&gt;2. Não Associativa&lt;/h2&gt;
        &lt;p&gt;A forma como agrupamos os números muda o resultado.&lt;/p&gt;
        &lt;div class="example"&gt;
            &lt;p&gt;&lt;strong&gt;Exemplo:&lt;/strong&gt; &lt;code&gt;(10 - 5) - 2 = 3&lt;/code&gt;, mas &lt;code&gt;10 - (5 - 2) = 7&lt;/code&gt;&lt;/p&gt;
        &lt;/div&gt;
        &lt;div class="interactive"&gt;
            &lt;p&gt;Teste você mesmo:&lt;/p&gt;
            &lt;input type="number" id="numA" placeholder="Número A"&gt;
            &lt;input type="number" id="numB" placeholder="Número B"&gt;
            &lt;input type="number" id="numC" placeholder="Número C"&gt;
            &lt;button onclick="testAssociativa()"&gt;Calcular&lt;/button&gt;
            &lt;div id="result-associativa"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;div class="property"&gt;
        &lt;h2&gt;3. Elemento Neutro à Direita&lt;/h2&gt;
        &lt;p&gt;Subtrair zero não altera o número.&lt;/p&gt;
        &lt;div class="example"&gt;
            &lt;p&gt;&lt;strong&gt;Exemplo:&lt;/strong&gt; &lt;code&gt;7 - 0 = 7&lt;/code&gt;&lt;/p&gt;
        &lt;/div&gt;
        &lt;div class="interactive"&gt;
            &lt;p&gt;Teste você mesmo:&lt;/p&gt;
            &lt;input type="number" id="numNeutro" placeholder="Digite um número"&gt;
            &lt;button onclick="testNeutro()"&gt;Subtrair 0&lt;/button&gt;
            &lt;div id="result-neutro"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        function testComutativa() {
            const num1 = parseFloat(document.getElementById("num1").value);
            const num2 = parseFloat(document.getElementById("num2").value);
            const result1 = num1 - num2;
            const result2 = num2 - num1;
            document.getElementById("result-comutativa").innerHTML = 
                `&lt;p&gt;${num1} - ${num2} = ${result1}&lt;/p&gt;
                 &lt;p&gt;${num2} - ${num1} = ${result2}&lt;/p&gt;
                 &lt;p&gt;&lt;strong&gt;Resultados diferentes!&lt;/strong&gt;&lt;/p&gt;`;
        }

        function testAssociativa() {
            const numA = parseFloat(document.getElementById("numA").value);
            const numB = parseFloat(document.getElementById("numB").value);
            const numC = parseFloat(document.getElementById("numC").value);
            const result1 = (numA - numB) - numC;
            const result2 = numA - (numB - numC);
            document.getElementById("result-associativa").innerHTML = 
                `&lt;p&gt;(${numA} - ${numB}) - ${numC} = ${result1}&lt;/p&gt;
                 &lt;p&gt;${numA} - (${numB} - ${numC}) = ${result2}&lt;/p&gt;
                 &lt;p&gt;&lt;strong&gt;Resultados diferentes!&lt;/strong&gt;&lt;/p&gt;`;
        }

        function testNeutro() {
            const num = parseFloat(document.getElementById("numNeutro").value);
            const result = num - 0;
            document.getElementById("result-neutro").innerHTML = 
                `&lt;p&gt;${num} - 0 = ${result}&lt;/p&gt;
                 &lt;p&gt;&lt;strong&gt;O número não muda!&lt;/strong&gt;&lt;/p&gt;`;
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;