---
layout: post
title: "Post Sem Titulo"
date: 2025-08-07
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Sequências Recursivas&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: Arial, sans-serif;
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
        .exercicio {
            background-color: white;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background-color: #2980b9;
        }
        input {
            padding: 5px;
            margin: 5px 0;
            width: 50px;
        }
        .resposta {
            font-weight: bold;
            margin-top: 10px;
            color: #27ae60;
            display: none;
        }
        .correcao {
            margin-top: 10px;
            padding: 10px;
            border-radius: 5px;
            display: none;
        }
        .certo {
            background-color: #d5f5e3;
        }
        .errado {
            background-color: #fadbd8;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Exercícios Interativos de Sequências Recursivas&lt;/h1&gt;
    
    &lt;div class="exercicio" id="ex1"&gt;
        &lt;h3&gt;Exercício 1: Sequência Recursiva Simples&lt;/h3&gt;
        &lt;p&gt;&lt;strong&gt;Lei de formação:&lt;/strong&gt;&lt;br&gt;
        a₁ = 4&lt;br&gt;
        aₙ = aₙ₋₁ + 3 (cada termo é o anterior + 3)&lt;/p&gt;
        &lt;p&gt;Quais são os 5 primeiros termos?&lt;/p&gt;
        &lt;input type="number" id="ex1a1" placeholder="a₁"&gt; 
        &lt;input type="number" id="ex1a2" placeholder="a₂"&gt; 
        &lt;input type="number" id="ex1a3" placeholder="a₃"&gt; 
        &lt;input type="number" id="ex1a4" placeholder="a₄"&gt; 
        &lt;input type="number" id="ex1a5" placeholder="a₅"&gt;
        &lt;button onclick="verificarEx1()"&gt;Verificar&lt;/button&gt;
        &lt;div id="resposta1" class="resposta"&gt;Resposta correta: 4, 7, 10, 13, 16&lt;/div&gt;
        &lt;div id="correcao1" class="correcao"&gt;&lt;/div&gt;
    &lt;/div&gt;

    &lt;div class="exercicio" id="ex2"&gt;
        &lt;h3&gt;Exercício 2: Descubra a Lei de Formação&lt;/h3&gt;
        &lt;p&gt;&lt;strong&gt;Sequência dada:&lt;/strong&gt; 5, 10, 20, 40, 80, ...&lt;/p&gt;
        &lt;p&gt;Complete a fórmula recursiva:&lt;/p&gt;
        &lt;p&gt;a₁ = &lt;input type="number" id="ex2a1"&gt;&lt;/p&gt;
        &lt;p&gt;aₙ = &lt;input type="number" id="ex2mult"&gt; × aₙ₋₁&lt;/p&gt;
        &lt;button onclick="verificarEx2()"&gt;Verificar&lt;/button&gt;
        &lt;div id="resposta2" class="resposta"&gt;Resposta correta: a₁ = 5; aₙ = 2 × aₙ₋₁&lt;/div&gt;
        &lt;div id="correcao2" class="correcao"&gt;&lt;/div&gt;
    &lt;/div&gt;

    &lt;div class="exercicio" id="ex3"&gt;
        &lt;h3&gt;Exercício 3: Sequência com Subtração&lt;/h3&gt;
        &lt;p&gt;&lt;strong&gt;Lei de formação:&lt;/strong&gt;&lt;br&gt;
        b₁ = 100&lt;br&gt;
        bₙ = bₙ₋₁ - 10&lt;/p&gt;
        &lt;p&gt;Qual é o quarto termo (b₄)?&lt;/p&gt;
        &lt;input type="number" id="ex3b4" placeholder="b₄"&gt;
        &lt;button onclick="verificarEx3()"&gt;Verificar&lt;/button&gt;
        &lt;div id="resposta3" class="resposta"&gt;Resposta correta: 70&lt;/div&gt;
        &lt;div id="correcao3" class="correcao"&gt;&lt;/div&gt;
    &lt;/div&gt;

    &lt;div class="exercicio" id="ex4"&gt;
        &lt;h3&gt;Exercício 4: Desafio com Multiplicação e Soma&lt;/h3&gt;
        &lt;p&gt;&lt;strong&gt;Lei de formação:&lt;/strong&gt;&lt;br&gt;
        c₁ = 1&lt;br&gt;
        cₙ = 3 × cₙ₋₁ + 1&lt;/p&gt;
        &lt;p&gt;Calcule c₃:&lt;/p&gt;
        &lt;input type="number" id="ex4c3" placeholder="c₃"&gt;
        &lt;button onclick="verificarEx4()"&gt;Verificar&lt;/button&gt;
        &lt;div id="resposta4" class="resposta"&gt;Resposta correta: 13&lt;/div&gt;
        &lt;div id="correcao4" class="correcao"&gt;&lt;/div&gt;
    &lt;/div&gt;

    &lt;div class="exercicio" id="ex5"&gt;
        &lt;h3&gt;Exercício 5: Sequência de Fibonacci Adaptada&lt;/h3&gt;
        &lt;p&gt;&lt;strong&gt;Lei de formação:&lt;/strong&gt;&lt;br&gt;
        d₁ = 2&lt;br&gt;
        d₂ = 3&lt;br&gt;
        dₙ = dₙ₋₁ + dₙ₋₂ (soma os dois termos anteriores)&lt;/p&gt;
        &lt;p&gt;Qual é o quinto termo (d₅)?&lt;/p&gt;
        &lt;input type="number" id="ex5d5" placeholder="d₅"&gt;
        &lt;button onclick="verificarEx5()"&gt;Verificar&lt;/button&gt;
        &lt;div id="resposta5" class="resposta"&gt;Resposta correta: 13&lt;/div&gt;
        &lt;div id="correcao5" class="correcao"&gt;&lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        function verificarEx1() {
            const a1 = parseInt(document.getElementById('ex1a1').value);
            const a2 = parseInt(document.getElementById('ex1a2').value);
            const a3 = parseInt(document.getElementById('ex1a3').value);
            const a4 = parseInt(document.getElementById('ex1a4').value);
            const a5 = parseInt(document.getElementById('ex1a5').value);
            const correcao = document.getElementById('correcao1');
            
            if (a1 === 4 &amp;&amp; a2 === 7 &amp;&amp; a3 === 10 &amp;&amp; a4 === 13 &amp;&amp; a5 === 16) {
                correcao.innerHTML = "Parabéns! Todos os termos estão corretos!";
                correcao.className = "correcao certo";
            } else {
                correcao.innerHTML = "Alguns termos estão incorretos. Lembre-se: começa com 4 e cada termo seguinte é o anterior + 3.";
                correcao.className = "correcao errado";
            }
            correcao.style.display = "block";
            document.getElementById('resposta1').style.display = "block";
        }

        function verificarEx2() {
            const a1 = parseInt(document.getElementById('ex2a1').value);
            const mult = parseInt(document.getElementById('ex2mult').value);
            const correcao = document.getElementById('correcao2');
            
            if (a1 === 5 &amp;&amp; mult === 2) {
                correcao.innerHTML = "Correto! A sequência dobra a cada termo.";
                correcao.className = "correcao certo";
            } else {
                correcao.innerHTML = "Não é isso. Observe que: 5×2=10, 10×2=20, etc.";
                correcao.className = "correcao errado";
            }
            correcao.style.display = "block";
            document.getElementById('resposta2').style.display = "block";
        }

        function verificarEx3() {
            const b4 = parseInt(document.getElementById('ex3b4').value);
            const correcao = document.getElementById('correcao3');
            
            if (b4 === 70) {
                correcao.innerHTML = "Exato! A sequência é: 100, 90, 80, 70...";
                correcao.className = "correcao certo";
            } else {
                correcao.innerHTML = "Incorreto. Lembre-se: começa em 100 e subtrai 10 a cada termo.";
                correcao.className = "correcao errado";
            }
            correcao.style.display = "block";
            document.getElementById('resposta3').style.display = "block";
        }

        function verificarEx4() {
            const c3 = parseInt(document.getElementById('ex4c3').value);
            const correcao = document.getElementById('correcao4');
            
            if (c3 === 13) {
                correcao.innerHTML = "Isso mesmo! c₂ = 4 e c₃ = 13.";
                correcao.className = "correcao certo";
            } else {
                correcao.innerHTML = "Não é o valor correto. Calcule passo a passo: c₂ = 3×1+1 = 4, depois c₃ = 3×4+1 = ?";
                correcao.className = "correcao errado";
            }
            correcao.style.display = "block";
            document.getElementById('resposta4').style.display = "block";
        }

        function verificarEx5() {
            const d5 = parseInt(document.getElementById('ex5d5').value);
            const correcao = document.getElementById('correcao5');
            
            if (d5 === 13) {
                correcao.innerHTML = "Correto! A sequência é: 2, 3, 5, 8, 13...";
                correcao.className = "correcao certo";
            } else {
                correcao.innerHTML = "Ops! A sequência soma os dois anteriores: 2+3=5, 3+5=8, 5+8=?";
                correcao.className = "correcao errado";
            }
            correcao.style.display = "block";
            document.getElementById('resposta5').style.display = "block";
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;