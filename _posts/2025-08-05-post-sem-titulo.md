---
layout: post
title: "Post Sem Titulo"
date: 2025-08-05
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;&lt;/meta&gt;
    &lt;meta content="width=device-width, initial-scale=1.0" name="viewport"&gt;&lt;/meta&gt;
    &lt;title&gt;Frações&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f8ff;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }
        
        .slide-container {
            width: 80%;
            max-width: 800px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            padding: 30px;
            margin: 20px 0;
            display: none;
        }
        
        .active {
            display: block;
        }
        
        h1 {
            color: #2c3e50;
            text-align: center;
            margin-bottom: 30px;
        }
        
        h2 {
            color: #3498db;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
        }
        
        .formula {
            background-color: #eaf2f8;
            padding: 15px;
            border-radius: 10px;
            font-family: 'Courier New', monospace;
            text-align: center;
            margin: 20px 0;
            font-size: 1.2em;
        }
        
        .exemplo {
            background-color: #e8f8f5;
            padding: 15px;
            border-left: 5px solid #1abc9c;
            margin: 20px 0;
        }
        
        .dica {
            background-color: #fef9e7;
            padding: 15px;
            border-left: 5px solid #f39c12;
            margin: 20px 0;
            font-style: italic;
        }
        
        .controls {
            display: flex;
            justify-content: space-between;
            width: 80%;
            max-width: 800px;
            margin-bottom: 20px;
        }
        
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: #2980b9;
        }
        
        .fraction {
            display: inline-block;
            vertical-align: middle;
            text-align: center;
        }
        
        .fraction span {
            display: block;
        }
        
        .fraction .numerator {
            border-bottom: 1px solid black;
        }
        
        .operation {
            font-size: 1.5em;
            margin: 0 10px;
            vertical-align: middle;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;div class="slide-container active" id="slide1"&gt;
        &lt;h1&gt;Multiplicação e Divisão de Frações&lt;/h1&gt;
        &lt;p&gt;Vamos aprender de forma simples e divertida como multiplicar e dividir frações!&lt;/p&gt;
        &lt;div style="margin-top: 40px; text-align: center;"&gt;
            &lt;div style="display: inline-block; margin: 0 20px;"&gt;
                &lt;div class="fraction"&gt;
                    &lt;span class="numerator"&gt;a&lt;/span&gt;
                    &lt;span class="denominator"&gt;b&lt;/span&gt;
                &lt;/div&gt;
                &lt;span class="operation"&gt;×&lt;/span&gt;
                &lt;div class="fraction"&gt;
                    &lt;span class="numerator"&gt;c&lt;/span&gt;
                    &lt;span class="denominator"&gt;d&lt;/span&gt;
                &lt;/div&gt;
            &lt;/div&gt;
            &lt;div style="display: inline-block; margin: 0 20px;"&gt;
                &lt;div class="fraction"&gt;
                    &lt;span class="numerator"&gt;a&lt;/span&gt;
                    &lt;span class="denominator"&gt;b&lt;/span&gt;
                &lt;/div&gt;
                &lt;span class="operation"&gt;÷&lt;/span&gt;
                &lt;div class="fraction"&gt;
                    &lt;span class="numerator"&gt;c&lt;/span&gt;
                    &lt;span class="denominator"&gt;d&lt;/span&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="slide-container" id="slide2"&gt;
        &lt;h1&gt;Multiplicação de Frações&lt;/h1&gt;
        &lt;p&gt;Para multiplicar frações, seguimos uma regra simples:&lt;/p&gt;
        
        &lt;div class="formula"&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;a&lt;/span&gt;
                &lt;span class="denominator"&gt;b&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;×&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;c&lt;/span&gt;
                &lt;span class="denominator"&gt;d&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;=&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;a × c&lt;/span&gt;
                &lt;span class="denominator"&gt;b × d&lt;/span&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;div class="exemplo"&gt;
            &lt;h3&gt;Exemplo:&lt;/h3&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;2&lt;/span&gt;
                &lt;span class="denominator"&gt;3&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;×&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;4&lt;/span&gt;
                &lt;span class="denominator"&gt;5&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;=&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;8&lt;/span&gt;
                &lt;span class="denominator"&gt;15&lt;/span&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;div class="dica"&gt;
            &lt;strong&gt;Dica:&lt;/strong&gt; Sempre que possível, simplifique antes de multiplicar!
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="slide-container" id="slide3"&gt;
        &lt;h1&gt;Divisão de Frações&lt;/h1&gt;
        &lt;p&gt;Para dividir frações, usamos um truque especial:&lt;/p&gt;
        
        &lt;div class="formula"&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;a&lt;/span&gt;
                &lt;span class="denominator"&gt;b&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;÷&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;c&lt;/span&gt;
                &lt;span class="denominator"&gt;d&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;=&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;a&lt;/span&gt;
                &lt;span class="denominator"&gt;b&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;×&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;d&lt;/span&gt;
                &lt;span class="denominator"&gt;c&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;=&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;a × d&lt;/span&gt;
                &lt;span class="denominator"&gt;b × c&lt;/span&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;div class="exemplo"&gt;
            &lt;h3&gt;Exemplo:&lt;/h3&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;3&lt;/span&gt;
                &lt;span class="denominator"&gt;4&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;÷&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;2&lt;/span&gt;
                &lt;span class="denominator"&gt;5&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;=&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;3&lt;/span&gt;
                &lt;span class="denominator"&gt;4&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;×&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;5&lt;/span&gt;
                &lt;span class="denominator"&gt;2&lt;/span&gt;
            &lt;/div&gt;
            &lt;span class="operation"&gt;=&lt;/span&gt;
            &lt;div class="fraction"&gt;
                &lt;span class="numerator"&gt;15&lt;/span&gt;
                &lt;span class="denominator"&gt;8&lt;/span&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;div class="dica"&gt;
            &lt;strong&gt;Dica:&lt;/strong&gt; Lembre-se que dividir é o mesmo que multiplicar pelo inverso!
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="slide-container" id="slide4"&gt;
        &lt;h1&gt;Exercício Prático&lt;/h1&gt;
        &lt;h2&gt;Tente resolver:&lt;/h2&gt;
        
        &lt;div style="margin: 30px 0; text-align: center;"&gt;
            &lt;div style="display: inline-block; margin: 0 20px;"&gt;
                &lt;div class="fraction"&gt;
                    &lt;span class="numerator"&gt;5&lt;/span&gt;
                    &lt;span class="denominator"&gt;6&lt;/span&gt;
                &lt;/div&gt;
                &lt;span class="operation"&gt;×&lt;/span&gt;
                &lt;div class="fraction"&gt;
                    &lt;span class="numerator"&gt;3&lt;/span&gt;
                    &lt;span class="denominator"&gt;10&lt;/span&gt;
                &lt;/div&gt;
                &lt;span class="operation"&gt;=&lt;/span&gt;
                &lt;input id="mult-resposta" placeholder="Resposta" style="text-align: center; width: 60px;" type="text" /&gt;
                &lt;button onclick="verificarMultiplicacao()"&gt;Verificar&lt;/button&gt;
                &lt;p id="mult-resultado"&gt;&lt;/p&gt;
            &lt;/div&gt;
            
            &lt;div style="display: inline-block; margin: 0 20px;"&gt;
                &lt;div class="fraction"&gt;
                    &lt;span class="numerator"&gt;7&lt;/span&gt;
                    &lt;span class="denominator"&gt;8&lt;/span&gt;
                &lt;/div&gt;
                &lt;span class="operation"&gt;÷&lt;/span&gt;
                &lt;div class="fraction"&gt;
                    &lt;span class="numerator"&gt;1&lt;/span&gt;
                    &lt;span class="denominator"&gt;4&lt;/span&gt;
                &lt;/div&gt;
                &lt;span class="operation"&gt;=&lt;/span&gt;
                &lt;input id="div-resposta" placeholder="Resposta" style="text-align: center; width: 60px;" type="text" /&gt;
                &lt;button onclick="verificarDivisao()"&gt;Verificar&lt;/button&gt;
                &lt;p id="div-resultado"&gt;&lt;/p&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="slide-container" id="slide5"&gt;
        &lt;h1&gt;Resumo&lt;/h1&gt;
        
        &lt;div style="display: flex; flex-wrap: wrap; justify-content: space-around;"&gt;
            &lt;div style="width: 45%;"&gt;
                &lt;h3&gt;Multiplicação&lt;/h3&gt;
                &lt;div class="formula"&gt;
                    &lt;div class="fraction"&gt;
                        &lt;span class="numerator"&gt;a&lt;/span&gt;
                        &lt;span class="denominator"&gt;b&lt;/span&gt;
                    &lt;/div&gt;
                    &lt;span class="operation"&gt;×&lt;/span&gt;
                    &lt;div class="fraction"&gt;
                        &lt;span class="numerator"&gt;c&lt;/span&gt;
                        &lt;span class="denominator"&gt;d&lt;/span&gt;
                    &lt;/div&gt;
                    &lt;span class="operation"&gt;=&lt;/span&gt;
                    &lt;div class="fraction"&gt;
                        &lt;span class="numerator"&gt;a × c&lt;/span&gt;
                        &lt;span class="denominator"&gt;b × d&lt;/span&gt;
                    &lt;/div&gt;
                &lt;/div&gt;
            &lt;/div&gt;
            
            &lt;div style="width: 45%;"&gt;
                &lt;h3&gt;Divisão&lt;/h3&gt;
                &lt;div class="formula"&gt;
                    &lt;div class="fraction"&gt;
                        &lt;span class="numerator"&gt;a&lt;/span&gt;
                        &lt;span class="denominator"&gt;b&lt;/span&gt;
                    &lt;/div&gt;
                    &lt;span class="operation"&gt;÷&lt;/span&gt;
                    &lt;div class="fraction"&gt;
                        &lt;span class="numerator"&gt;c&lt;/span&gt;
                        &lt;span class="denominator"&gt;d&lt;/span&gt;
                    &lt;/div&gt;
                    &lt;span class="operation"&gt;=&lt;/span&gt;
                    &lt;div class="fraction"&gt;
                        &lt;span class="numerator"&gt;a × d&lt;/span&gt;
                        &lt;span class="denominator"&gt;b × c&lt;/span&gt;
                    &lt;/div&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;div style="margin-top: 40px; text-align: center;"&gt;
            &lt;h3&gt;Parabéns por aprender sobre frações!&lt;/h3&gt;
            &lt;p&gt;Continue praticando para ficar ainda melhor!&lt;/p&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="controls"&gt;
        &lt;button id="prev-btn" onclick="prevSlide()"&gt;Anterior&lt;/button&gt;
        &lt;span id="slide-indicator"&gt;Slide 1 de 5&lt;/span&gt;
        &lt;button id="next-btn" onclick="nextSlide()"&gt;Próximo&lt;/button&gt;
    &lt;/div&gt;
    
    &lt;script&gt;
        let currentSlide = 1;
        const totalSlides = 5;
        
        function updateSlide() {
            // Esconde todos os slides
            document.querySelectorAll('.slide-container').forEach(slide =&gt; {
                slide.classList.remove('active');
            });
            
            // Mostra o slide atual
            document.getElementById(`slide${currentSlide}`).classList.add('active');
            
            // Atualiza o indicador
            document.getElementById('slide-indicator').textContent = `Slide ${currentSlide} de ${totalSlides}`;
            
            // Desabilita/habilita botões conforme necessário
            document.getElementById('prev-btn').disabled = currentSlide === 1;
            document.getElementById('next-btn').disabled = currentSlide === totalSlides;
        }
        
        function nextSlide() {
            if (currentSlide &lt; totalSlides) {
                currentSlide++;
                updateSlide();
            }
        }
        
        function prevSlide() {
            if (currentSlide &gt; 1) {
                currentSlide--;
                updateSlide();
            }
        }
        
        function verificarMultiplicacao() {
            const resposta = document.getElementById('mult-resposta').value.trim();
            const resultadoElement = document.getElementById('mult-resultado');
            
            if (resposta === '1/4' || resposta === '0.25' || resposta === '25/100') {
                resultadoElement.textContent = '✅ Correto! 5/6 × 3/10 = 15/60 = 1/4';
                resultadoElement.style.color = 'green';
            } else {
                resultadoElement.textContent = '❌ Tente novamente! Lembre-se: multiplique numeradores e denominadores';
                resultadoElement.style.color = 'red';
            }
        }
        
        function verificarDivisao() {
            const resposta = document.getElementById('div-resposta').value.trim();
            const resultadoElement = document.getElementById('div-resultado');
            
            if (resposta === '7/2' || resposta === '3.5' || resposta === '3 1/2') {
                resultadoElement.textContent = '✅ Correto! 7/8 ÷ 1/4 = 7/8 × 4/1 = 28/8 = 7/2';
                resultadoElement.style.color = 'green';
            } else {
                resultadoElement.textContent = '❌ Tente novamente! Lembre-se: inverta a segunda fração e multiplique';
                resultadoElement.style.color = 'red';
            }
        }
        
        // Inicializa a apresentação
        updateSlide();
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;