---
layout: post
title: "Divisão com números decimais"
date: 2025-07-29
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;div class="separator" style="clear: both; text-align: center;"&gt;&lt;br /&gt;&lt;/div&gt;&lt;div class="separator" style="clear: both; text-align: center;"&gt;&lt;iframe allowfullscreen="" class="BLOG_video_class" height="266" src="https://www.youtube.com/embed/r8nRG0AHlu4" width="320" youtube-src-id="r8nRG0AHlu4"&gt;&lt;/iframe&gt;&lt;/div&gt;&lt;br /&gt;&lt;p&gt;&lt;/p&gt;


&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;&lt;/meta&gt;
    &lt;meta content="width=device-width, initial-scale=1.0" name="viewport"&gt;&lt;/meta&gt;
    &lt;title&gt;Propriedades da Divisão&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
            color: #333;
        }
        h1 {
            color: #2c3e50;
            text-align: center;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
        }
        .property-card {
            background-color: white;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        .property-card:hover {
            transform: translateY(-5px);
        }
        .property-title {
            color: #3498db;
            margin-top: 0;
        }
        .example {
            background-color: #e8f4fc;
            padding: 10px;
            border-left: 4px solid #3498db;
            margin: 10px 0;
            border-radius: 0 4px 4px 0;
        }
        .calculator {
            background-color: #2c3e50;
            color: white;
            padding: 20px;
            border-radius: 8px;
            margin-top: 30px;
        }
        input, button {
            padding: 8px;
            margin: 5px 0;
            border-radius: 4px;
            border: 1px solid #ddd;
        }
        button {
            background-color: #3498db;
            color: white;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #2980b9;
        }
        #result {
            font-weight: bold;
            margin-top: 10px;
            min-height: 20px;
        }
        .warning {
            color: #e74c3c;
            font-weight: bold;
        }
        .interactive-example {
            margin: 15px 0;
            padding: 10px;
            background-color: #f9f9f9;
            border-radius: 5px;
        }
        .tab {
            overflow: hidden;
            border: 1px solid #ccc;
            background-color: #f1f1f1;
            border-radius: 5px 5px 0 0;
        }
        .tab button {
            background-color: inherit;
            float: left;
            border: none;
            outline: none;
            cursor: pointer;
            padding: 10px 16px;
            transition: 0.3s;
            color: #333;
        }
        .tab button:hover {
            background-color: #ddd;
        }
        .tab button.active {
            background-color: #3498db;
            color: white;
        }
        .tabcontent {
            display: none;
            padding: 15px;
            border: 1px solid #ccc;
            border-top: none;
            border-radius: 0 0 5px 5px;
            background-color: white;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Propriedades da Divisão Matemática&lt;/h1&gt;
    
    &lt;div class="property-card"&gt;
        &lt;h2 class="property-title"&gt;1. Não é Comutativa&lt;/h2&gt;
        &lt;p&gt;A ordem dos números altera o resultado da divisão.&lt;/p&gt;
        &lt;div class="example"&gt;
            &lt;p&gt;&lt;strong&gt;Exemplo:&lt;/strong&gt; 10 ÷ 2 = 5, mas 2 ÷ 10 = 0,2&lt;/p&gt;
        &lt;/div&gt;
        &lt;div class="interactive-example"&gt;
            &lt;p&gt;Experimente:&lt;/p&gt;
            &lt;input id="num1" placeholder="Primeiro número" type="number" /&gt;
            &lt;input id="num2" placeholder="Segundo número" type="number" /&gt;
            &lt;button onclick="testComutativa()"&gt;Testar Comutatividade&lt;/button&gt;
            &lt;div id="comutativa-result"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="property-card"&gt;
        &lt;h2 class="property-title"&gt;2. Não é Associativa&lt;/h2&gt;
        &lt;p&gt;A forma como agrupamos os números afeta o resultado.&lt;/p&gt;
        &lt;div class="example"&gt;
            &lt;p&gt;&lt;strong&gt;Exemplo:&lt;/strong&gt; (12 ÷ 3) ÷ 2 = 2, mas 12 ÷ (3 ÷ 2) = 8&lt;/p&gt;
        &lt;/div&gt;
        &lt;div class="interactive-example"&gt;
            &lt;p&gt;Experimente com três números:&lt;/p&gt;
            &lt;input id="a" placeholder="a" type="number" /&gt;
            &lt;input id="b" placeholder="b" type="number" /&gt;
            &lt;input id="c" placeholder="c" type="number" /&gt;
            &lt;button onclick="testAssociativa()"&gt;Testar Associatividade&lt;/button&gt;
            &lt;div id="associativa-result"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="property-card"&gt;
        &lt;h2 class="property-title"&gt;3. Elemento Neutro&lt;/h2&gt;
        &lt;p&gt;Dividir por 1 mantém o número original.&lt;/p&gt;
        &lt;div class="example"&gt;
            &lt;p&gt;&lt;strong&gt;Exemplo:&lt;/strong&gt; 7 ÷ 1 = 7&lt;/p&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="property-card"&gt;
        &lt;h2 class="property-title"&gt;4. Divisão por Zero&lt;/h2&gt;
        &lt;p class="warning"&gt;Não é definida na matemática!&lt;/p&gt;
        &lt;div class="example"&gt;
            &lt;p&gt;Tentar dividir qualquer número por zero resulta em um valor indefinido.&lt;/p&gt;
        &lt;/div&gt;
        &lt;div class="interactive-example"&gt;
            &lt;p&gt;Teste o que acontece:&lt;/p&gt;
            &lt;input id="dividendo" placeholder="Número qualquer" type="number" /&gt;
            &lt;button onclick="dividirPorZero()"&gt;Dividir por zero&lt;/button&gt;
            &lt;div id="zero-result"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="calculator"&gt;
        &lt;h2&gt;Calculadora de Divisão&lt;/h2&gt;
        &lt;input id="dividend" placeholder="Dividendo" type="number" /&gt;
        &lt;input id="divisor" placeholder="Divisor" type="number" /&gt;
        &lt;button onclick="calcular()"&gt;Calcular&lt;/button&gt;
        &lt;div id="result"&gt;&lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="property-card"&gt;
        &lt;h2 class="property-title"&gt;Resumo das Propriedades&lt;/h2&gt;
        &lt;div class="tab"&gt;
            &lt;button class="tablinks" onclick="openTab(event, 'Tabela')"&gt;Tabela&lt;/button&gt;
            &lt;button class="tablinks" onclick="openTab(event, 'Dicas')"&gt;Dicas&lt;/button&gt;
            &lt;button class="tablinks" onclick="openTab(event, 'Exercicios')"&gt;Exercícios&lt;/button&gt;
        &lt;/div&gt;
        
        &lt;div class="tabcontent" id="Tabela"&gt;
            &lt;table border="1" style="border-collapse: collapse; width: 100%;"&gt;
                &lt;tr style="background-color: #3498db; color: white;"&gt;
                    &lt;th&gt;Propriedade&lt;/th&gt;
                    &lt;th&gt;Exemplo&lt;/th&gt;
                &lt;/tr&gt;
                &lt;tr&gt;
                    &lt;td&gt;Não comutativa&lt;/td&gt;
                    &lt;td&gt;8 ÷ 4 ≠ 4 ÷ 8&lt;/td&gt;
                &lt;/tr&gt;
                &lt;tr&gt;
                    &lt;td&gt;Não associativa&lt;/td&gt;
                    &lt;td&gt;(16 ÷ 4) ÷ 2 ≠ 16 ÷ (4 ÷ 2)&lt;/td&gt;
                &lt;/tr&gt;
                &lt;tr&gt;
                    &lt;td&gt;Elemento neutro (÷1)&lt;/td&gt;
                    &lt;td&gt;9 ÷ 1 = 9&lt;/td&gt;
                &lt;/tr&gt;
                &lt;tr&gt;
                    &lt;td&gt;Divisão por zero&lt;/td&gt;
                    &lt;td&gt;5 ÷ 0 → Indefinido&lt;/td&gt;
                &lt;/tr&gt;
            &lt;/table&gt;
        &lt;/div&gt;
        
        &lt;div class="tabcontent" id="Dicas"&gt;
            &lt;h3&gt;Dicas para lembrar:&lt;/h3&gt;
            &lt;ul&gt;
                &lt;li&gt;A divisão é a operação inversa da multiplicação&lt;/li&gt;
                &lt;li&gt;Sempre verifique se o divisor não é zero&lt;/li&gt;
                &lt;li&gt;Para números decimais, você pode multiplicar ambos por 10 até virar inteiros&lt;/li&gt;
            &lt;/ul&gt;
        &lt;/div&gt;
        
        &lt;div class="tabcontent" id="Exercicios"&gt;
            &lt;h3&gt;Exercícios para praticar:&lt;/h3&gt;
            &lt;ol&gt;
                &lt;li&gt;Qual é o resultado de (20 ÷ 5) ÷ 2?&lt;/li&gt;
                &lt;li&gt;É verdade que 15 ÷ 3 é o mesmo que 3 ÷ 15?&lt;/li&gt;
                &lt;li&gt;O que acontece se você tentar calcular 7 ÷ 0?&lt;/li&gt;
            &lt;/ol&gt;
            &lt;button onclick="mostrarRespostas()"&gt;Mostrar Respostas&lt;/button&gt;
            &lt;div id="respostas" style="display: none;"&gt;
                &lt;p&gt;1. 2&lt;/p&gt;
                &lt;p&gt;2. Não, 15 ÷ 3 = 5 e 3 ÷ 15 = 0,2&lt;/p&gt;
                &lt;p&gt;3. Operação indefinida (não existe)&lt;/p&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        // Funções para os exemplos interativos
        function testComutativa() {
            const num1 = parseFloat(document.getElementById('num1').value);
            const num2 = parseFloat(document.getElementById('num2').value);
            const resultDiv = document.getElementById('comutativa-result');
            
            if (isNaN(num1) || isNaN(num2)) {
                resultDiv.innerHTML = "Por favor, insira dois números válidos.";
                return;
            }
            
            const div1 = num1 / num2;
            const div2 = num2 / num1;
            
            resultDiv.innerHTML = `
                &lt;p&gt;${num1} ÷ ${num2} = ${div1}&lt;/p&gt;
                &lt;p&gt;${num2} ÷ ${num1} = ${div2}&lt;/p&gt;
                &lt;p&gt;&lt;strong&gt;Resultados diferentes → não é comutativa!&lt;/strong&gt;&lt;/p&gt;
            `;
        }
        
        function testAssociativa() {
            const a = parseFloat(document.getElementById('a').value);
            const b = parseFloat(document.getElementById('b').value);
            const c = parseFloat(document.getElementById('c').value);
            const resultDiv = document.getElementById('associativa-result');
            
            if (isNaN(a) || isNaN(b) || isNaN(c)) {
                resultDiv.innerHTML = "Por favor, insira três números válidos.";
                return;
            }
            
            const div1 = (a / b) / c;
            const div2 = a / (b / c);
            
            resultDiv.innerHTML = `
                &lt;p&gt;(${a} ÷ ${b}) ÷ ${c} = ${div1}&lt;/p&gt;
                &lt;p&gt;${a} ÷ (${b} ÷ ${c}) = ${div2}&lt;/p&gt;
                &lt;p&gt;&lt;strong&gt;Resultados diferentes → não é associativa!&lt;/strong&gt;&lt;/p&gt;
            `;
        }
        
        function dividirPorZero() {
            const num = parseFloat(document.getElementById('dividendo').value);
            const resultDiv = document.getElementById('zero-result');
            
            if (isNaN(num)) {
                resultDiv.innerHTML = "Por favor, insira um número válido.";
                return;
            }
            
            if (num === 0) {
                resultDiv.innerHTML = "&lt;p class='warning'&gt;0 ÷ 0 é uma indeterminação!&lt;/p&gt;";
            } else {
                resultDiv.innerHTML = "&lt;p class='warning'&gt;" + num + " ÷ 0 é indefinido na matemática!&lt;/p&gt;";
            }
        }
        
        function calcular() {
            const dividend = parseFloat(document.getElementById('dividend').value);
            const divisor = parseFloat(document.getElementById('divisor').value);
            const resultDiv = document.getElementById('result');
            
            if (isNaN(dividend) {
                resultDiv.innerHTML = "Por favor, insira um dividendo válido.";
                return;
            }
            
            if (isNaN(divisor)) {
                resultDiv.innerHTML = "Por favor, insira um divisor válido.";
                return;
            }
            
            if (divisor === 0) {
                resultDiv.innerHTML = "&lt;span class='warning'&gt;Erro: Divisão por zero não é definida!&lt;/span&gt;";
            } else {
                resultDiv.innerHTML = "Resultado: " + (dividend / divisor);
            }
        }
        
        function openTab(evt, tabName) {
            const tabcontent = document.getElementsByClassName("tabcontent");
            for (let i = 0; i &lt; tabcontent.length; i++) {
                tabcontent[i].style.display = "none";
            }
            
            const tablinks = document.getElementsByClassName("tablinks");
            for (let i = 0; i &lt; tablinks.length; i++) {
                tablinks[i].className = tablinks[i].className.replace(" active", "");
            }
            
            document.getElementById(tabName).style.display = "block";
            evt.currentTarget.className += " active";
        }
        
        function mostrarRespostas() {
            const respostasDiv = document.getElementById('respostas');
            if (respostasDiv.style.display === "none") {
                respostasDiv.style.display = "block";
            } else {
                respostasDiv.style.display = "none";
            }
        }
        
        // Mostrar a primeira aba por padrão
        document.getElementById('Tabela').style.display = "block";
        document.getElementsByClassName('tablinks')[0].className += " active";
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
&lt;b&gt;&lt;a href="https://www.profmarcovargas.com.br/2025/08/blog-post.html" target="_blank"&gt;Próxima página: pratique mais...&lt;/a&gt;&lt;/b&gt;