---
layout: post
title: "Post Sem Titulo"
date: 2025-08-08
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Explorador de Sequências Numéricas&lt;/title&gt;
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
            margin-bottom: 30px;
        }
        
        .sequence-container {
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .sequence-title {
            font-weight: bold;
            margin-bottom: 10px;
            color: #3498db;
        }
        
        .sequence {
            font-family: monospace;
            font-size: 16px;
            margin-bottom: 15px;
        }
        
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 4px;
            cursor: pointer;
            margin-right: 10px;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: #2980b9;
        }
        
        input {
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
            width: 50px;
            margin-right: 10px;
        }
        
        .result {
            margin-top: 10px;
            padding: 10px;
            background-color: #e8f4fc;
            border-radius: 4px;
            display: none;
        }
        
        .active {
            display: block;
        }
        
        .controls {
            margin-top: 15px;
        }
        
        .explanation {
            font-style: italic;
            color: #7f8c8d;
            margin-top: 10px;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Explorador de Sequências Numéricas&lt;/h1&gt;
    
    &lt;div class="sequence-container"&gt;
        &lt;div class="sequence-title"&gt;Sequência a) 2, 5, 8, 11,…&lt;/div&gt;
        &lt;div class="sequence" id="seq-a"&gt;2, 5, 8, 11&lt;/div&gt;
        &lt;div class="explanation"&gt;Padrão: Soma +3 a cada termo&lt;/div&gt;
        &lt;div class="controls"&gt;
            &lt;button onclick="nextTerm('seq-a', 3)"&gt;Próximo Termo&lt;/button&gt;
            &lt;button onclick="showMore('seq-a', 3, 2)"&gt;Mostrar Mais 2 Termos&lt;/button&gt;
        &lt;/div&gt;
        &lt;div class="result" id="result-a"&gt;&lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="sequence-container"&gt;
        &lt;div class="sequence-title"&gt;Sequência b) 6, 18, 54, 162,…&lt;/div&gt;
        &lt;div class="sequence" id="seq-b"&gt;6, 18, 54, 162&lt;/div&gt;
        &lt;div class="explanation"&gt;Padrão: Multiplica por 3 a cada termo&lt;/div&gt;
        &lt;div class="controls"&gt;
            &lt;button onclick="nextTerm('seq-b', '*3')"&gt;Próximo Termo&lt;/button&gt;
            &lt;button onclick="showMore('seq-b', '*3', 2)"&gt;Mostrar Mais 2 Termos&lt;/button&gt;
        &lt;/div&gt;
        &lt;div class="result" id="result-b"&gt;&lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="sequence-container"&gt;
        &lt;div class="sequence-title"&gt;Sequência c) 1, 2, 4, 8, 16, 32,…&lt;/div&gt;
        &lt;div class="sequence" id="seq-c"&gt;1, 2, 4, 8, 16, 32&lt;/div&gt;
        &lt;div class="explanation"&gt;Padrão: Multiplica por 2 a cada termo (potências de 2)&lt;/div&gt;
        &lt;div class="controls"&gt;
            &lt;button onclick="nextTerm('seq-c', '*2')"&gt;Próximo Termo&lt;/button&gt;
            &lt;button onclick="showMore('seq-c', '*2', 2)"&gt;Mostrar Mais 2 Termos&lt;/button&gt;
        &lt;/div&gt;
        &lt;div class="result" id="result-c"&gt;&lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="sequence-container"&gt;
        &lt;div class="sequence-title"&gt;Sequência j) 3, 7, 11, 15, 19,…&lt;/div&gt;
        &lt;div class="sequence" id="seq-j"&gt;3, 7, 11, 15, 19&lt;/div&gt;
        &lt;div class="explanation"&gt;Padrão: Soma +4 a cada termo&lt;/div&gt;
        &lt;div class="controls"&gt;
            &lt;button onclick="nextTerm('seq-j', 4)"&gt;Próximo Termo&lt;/button&gt;
            &lt;button onclick="showMore('seq-j', 4, 2)"&gt;Mostrar Mais 2 Termos&lt;/button&gt;
            &lt;button onclick="calculateTerm('seq-j', 4, 10)"&gt;Calcular 10º Termo&lt;/button&gt;
        &lt;/div&gt;
        &lt;div class="result" id="result-j"&gt;&lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="sequence-container"&gt;
        &lt;div class="sequence-title"&gt;Crie sua própria sequência&lt;/div&gt;
        &lt;div class="controls"&gt;
            &lt;input type="number" id="start-term" placeholder="Primeiro termo"&gt;
            &lt;input type="number" id="step" placeholder="Passo"&gt;
            &lt;button onclick="createSequence()"&gt;Criar Sequência&lt;/button&gt;
        &lt;/div&gt;
        &lt;div class="sequence" id="custom-seq"&gt;&lt;/div&gt;
        &lt;div class="controls" id="custom-controls" style="display: none;"&gt;
            &lt;button onclick="nextTerm('custom-seq', 'custom')"&gt;Próximo Termo&lt;/button&gt;
            &lt;button onclick="showMore('custom-seq', 'custom', 2)"&gt;Mostrar Mais 2 Termos&lt;/button&gt;
        &lt;/div&gt;
        &lt;div class="result" id="result-custom"&gt;&lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        // Função para adicionar o próximo termo a uma sequência
        function nextTerm(seqId, pattern) {
            const seqElement = document.getElementById(seqId);
            let sequence = seqElement.textContent.split(', ').map(Number);
            let lastTerm = sequence[sequence.length - 1];
            let nextTerm;
            
            if (pattern === 'custom') {
                const step = parseInt(document.getElementById('step').value);
                nextTerm = lastTerm + step;
            } else if (typeof pattern === 'string' &amp;&amp; pattern.startsWith('*')) {
                const multiplier = parseInt(pattern.substring(1));
                nextTerm = lastTerm * multiplier;
            } else {
                nextTerm = lastTerm + pattern;
            }
            
            sequence.push(nextTerm);
            seqElement.textContent = sequence.join(', ');
            
            // Mostrar o resultado
            const resultElement = document.getElementById('result-' + seqId.split('-')[1]);
            resultElement.textContent = `Próximo termo: ${nextTerm}`;
            resultElement.classList.add('active');
            
            // Esconder o resultado após 3 segundos
            setTimeout(() =&gt; {
                resultElement.classList.remove('active');
            }, 3000);
        }
        
        // Função para mostrar vários termos de uma vez
        function showMore(seqId, pattern, count) {
            const seqElement = document.getElementById(seqId);
            let sequence = seqElement.textContent.split(', ').map(Number);
            let lastTerm = sequence[sequence.length - 1];
            let newTerms = [];
            
            for (let i = 0; i &lt; count; i++) {
                if (pattern === 'custom') {
                    const step = parseInt(document.getElementById('step').value);
                    lastTerm += step;
                } else if (typeof pattern === 'string' &amp;&amp; pattern.startsWith('*')) {
                    const multiplier = parseInt(pattern.substring(1));
                    lastTerm *= multiplier;
                } else {
                    lastTerm += pattern;
                }
                newTerms.push(lastTerm);
            }
            
            sequence = sequence.concat(newTerms);
            seqElement.textContent = sequence.join(', ');
            
            // Mostrar o resultado
            const resultElement = document.getElementById('result-' + seqId.split('-')[1]);
            resultElement.textContent = `Próximos ${count} termos: ${newTerms.join(', ')}`;
            resultElement.classList.add('active');
            
            // Esconder o resultado após 3 segundos
            setTimeout(() =&gt; {
                resultElement.classList.remove('active');
            }, 3000);
        }
        
        // Função para calcular um termo específico
        function calculateTerm(seqId, pattern, position) {
            const seqElement = document.getElementById(seqId);
            let sequence = seqElement.textContent.split(', ').map(Number);
            const firstTerm = sequence[0];
            let term;
            
            if (typeof pattern === 'string' &amp;&amp; pattern.startsWith('*')) {
                const multiplier = parseInt(pattern.substring(1));
                term = firstTerm * Math.pow(multiplier, position - 1);
            } else {
                term = firstTerm + (pattern * (position - 1));
            }
            
            // Mostrar o resultado
            const resultElement = document.getElementById('result-' + seqId.split('-')[1]);
            resultElement.textContent = `O ${position}º termo é: ${term}`;
            resultElement.classList.add('active');
        }
        
        // Função para criar uma sequência personalizada
        function createSequence() {
            const startTerm = parseInt(document.getElementById('start-term').value);
            const step = parseInt(document.getElementById('step').value);
            
            if (isNaN(startTerm) || isNaN(step)) {
                alert("Por favor, insira valores válidos para o primeiro termo e o passo.");
                return;
            }
            
            const seqElement = document.getElementById('custom-seq');
            seqElement.textContent = startTerm;
            
            document.getElementById('custom-controls').style.display = 'block';
            
            // Mostrar o resultado
            const resultElement = document.getElementById('result-custom');
            resultElement.textContent = `Sequência criada começando com ${startTerm} e passo ${step}`;
            resultElement.classList.add('active');
            
            // Esconder o resultado após 3 segundos
            setTimeout(() =&gt; {
                resultElement.classList.remove('active');
            }, 3000);
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;