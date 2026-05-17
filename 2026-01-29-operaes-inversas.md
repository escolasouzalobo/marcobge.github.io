---
layout: post
title: "Operações inversas"
date: 2026-01-29
---

&lt;!DOCTYPE html&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Máquina de Operações Inversas&lt;/title&gt;
    &lt;style&gt;
        * {
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            margin: 0;
            padding: 20px;
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            color: #333;
        }
        
        .container {
            background-color: white;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            padding: 30px;
            max-width: 900px;
            width: 100%;
            margin: 20px 0;
        }
        
        h1 {
            text-align: center;
            color: #2575fc;
            margin-top: 0;
            font-size: 2.2rem;
        }
        
        .subtitle {
            text-align: center;
            color: #666;
            margin-bottom: 30px;
            font-size: 1.1rem;
        }
        
        .game-area {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .machine-section {
            flex: 1;
            min-width: 300px;
            background: #f8f9fa;
            border-radius: 15px;
            padding: 20px;
            border: 2px dashed #ddd;
        }
        
        .machine-section h2 {
            text-align: center;
            color: #6a11cb;
            margin-top: 0;
            font-size: 1.5rem;
        }
        
        .machine {
            background: white;
            border-radius: 10px;
            padding: 15px;
            margin: 20px 0;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            min-height: 150px;
        }
        
        .operation-step {
            display: flex;
            align-items: center;
            margin: 15px 0;
            padding: 10px;
            background: #f1f8ff;
            border-radius: 8px;
        }
        
        .number-box {
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            font-weight: bold;
            background: #4dabf7;
            color: white;
            border-radius: 10px;
            margin: 0 15px;
        }
        
        .operation-box {
            width: 80px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
            font-weight: bold;
            background: #ff922b;
            color: white;
            border-radius: 8px;
            margin: 0 10px;
        }
        
        .arrow {
            font-size: 2rem;
            color: #495057;
            margin: 0 10px;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin: 25px 0;
        }
        
        .operation-btn {
            padding: 12px 20px;
            font-size: 1.1rem;
            background: #40c057;
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: bold;
            min-width: 120px;
        }
        
        .operation-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 10px rgba(0,0,0,0.1);
        }
        
        .operation-btn.reset {
            background: #fa5252;
        }
        
        .operation-btn.undo {
            background: #ff922b;
        }
        
        .input-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin: 20px 0;
        }
        
        input {
            padding: 12px;
            font-size: 1.2rem;
            border: 2px solid #4dabf7;
            border-radius: 8px;
            width: 150px;
            text-align: center;
            margin-bottom: 15px;
        }
        
        button {
            padding: 12px 25px;
            font-size: 1.1rem;
            background: #5c7cfa;
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s;
        }
        
        button:hover {
            background: #4263eb;
        }
        
        .explanation {
            background: #e7f5ff;
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
            border-left: 5px solid #4dabf7;
        }
        
        .explanation h3 {
            color: #1971c2;
            margin-top: 0;
        }
        
        .feedback {
            text-align: center;
            padding: 15px;
            border-radius: 10px;
            margin: 15px 0;
            font-weight: bold;
            font-size: 1.1rem;
            display: none;
        }
        
        .feedback.correct {
            background: #d3f9d8;
            color: #2b8a3e;
            border: 2px solid #51cf66;
            display: block;
        }
        
        .feedback.incorrect {
            background: #ffe3e3;
            color: #c92a2a;
            border: 2px solid #ff6b6b;
            display: block;
        }
        
        .challenge-section {
            background: #fff9db;
            border-radius: 10px;
            padding: 20px;
            margin-top: 30px;
            border: 2px solid #ffd43b;
        }
        
        .challenge-section h3 {
            color: #e67700;
            margin-top: 0;
        }
        
        .challenge-problem {
            font-size: 1.2rem;
            margin: 15px 0;
        }
        
        .level-indicator {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin: 20px 0;
        }
        
        .level-dot {
            width: 15px;
            height: 15px;
            border-radius: 50%;
            background: #dee2e6;
        }
        
        .level-dot.active {
            background: #40c057;
        }
        
        @media (max-width: 768px) {
            .game-area {
                flex-direction: column;
            }
            
            .container {
                padding: 20px;
            }
            
            h1 {
                font-size: 1.8rem;
            }
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;div class="container"&gt;
        &lt;h1&gt;🏭 Máquina de Operações Inversas&lt;/h1&gt;
        &lt;p class="subtitle"&gt;Aprenda a "desfazer" operações matemáticas com este jogo interativo!&lt;/p&gt;
        
        &lt;div class="level-indicator"&gt;
            &lt;div class="level-dot active" id="level1"&gt;&lt;/div&gt;
            &lt;div class="level-dot" id="level2"&gt;&lt;/div&gt;
            &lt;div class="level-dot" id="level3"&gt;&lt;/div&gt;
        &lt;/div&gt;
        
        &lt;div class="game-area"&gt;
            &lt;div class="machine-section"&gt;
                &lt;h2&gt;📊 MÁQUINA DIRETA&lt;/h2&gt;
                &lt;div class="machine" id="direct-machine"&gt;
                    &lt;!-- Conteúdo gerado por JavaScript --&gt;
                &lt;/div&gt;
                &lt;div class="controls"&gt;
                    &lt;button class="operation-btn" onclick="addOperation('+', 5)"&gt;+ 5&lt;/button&gt;
                    &lt;button class="operation-btn" onclick="addOperation('-', 3)"&gt;- 3&lt;/button&gt;
                    &lt;button class="operation-btn" onclick="addOperation('×', 2)"&gt;× 2&lt;/button&gt;
                    &lt;button class="operation-btn" onclick="addOperation('÷', 2)"&gt;÷ 2&lt;/button&gt;
                    &lt;button class="operation-btn undo" onclick="undoOperation()"&gt;↶ Desfazer&lt;/button&gt;
                    &lt;button class="operation-btn reset" onclick="resetMachine()"&gt;🔄 Reiniciar&lt;/button&gt;
                &lt;/div&gt;
            &lt;/div&gt;
            
            &lt;div class="machine-section"&gt;
                &lt;h2&gt;🔙 MÁQUINA INVERSA&lt;/h2&gt;
                &lt;div class="machine" id="inverse-machine"&gt;
                    &lt;!-- Conteúdo gerado por JavaScript --&gt;
                &lt;/div&gt;
                &lt;div class="input-section"&gt;
                    &lt;p&gt;&lt;strong&gt;Número inicial:&lt;/strong&gt; &lt;span id="start-number"&gt;?&lt;/span&gt;&lt;/p&gt;
                    &lt;input type="number" id="guess-input" placeholder="Digite sua resposta"&gt;
                    &lt;button onclick="checkAnswer()"&gt;✅ Verificar Resposta&lt;/button&gt;
                &lt;/div&gt;
                &lt;div class="feedback" id="feedback"&gt;&lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;div class="explanation"&gt;
            &lt;h3&gt;💡 Como funciona o pensamento reverso?&lt;/h3&gt;
            &lt;p&gt;1. A &lt;strong&gt;Máquina Direta&lt;/strong&gt; aplica operações em um número inicial&lt;/p&gt;
            &lt;p&gt;2. Seu desafio é descobrir qual era o número inicial, conhecendo apenas o resultado final&lt;/p&gt;
            &lt;p&gt;3. Para isso, use a &lt;strong&gt;Máquina Inversa&lt;/strong&gt; que desfaz as operações na ordem contrária&lt;/p&gt;
            &lt;p&gt;&lt;strong&gt;Operações inversas:&lt;/strong&gt; + ↔ - &amp;nbsp;&amp;nbsp;&amp;nbsp; × ↔ ÷&lt;/p&gt;
        &lt;/div&gt;
        
        &lt;div class="challenge-section"&gt;
            &lt;h3&gt;🎯 Desafio do Pensamento Reverso&lt;/h3&gt;
            &lt;div class="challenge-problem" id="challenge-text"&gt;&lt;/div&gt;
            &lt;div class="input-section"&gt;
                &lt;input type="number" id="challenge-input" placeholder="Sua resposta"&gt;
                &lt;button onclick="checkChallenge()"&gt;🧠 Resolver Desafio&lt;/button&gt;
            &lt;/div&gt;
            &lt;div class="feedback" id="challenge-feedback"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        // Estado do jogo
        let operations = [];
        let startNumber = Math.floor(Math.random() * 20) + 1;
        let currentLevel = 1;
        
        // Desafios por nível
        const challenges = [
            {
                text: "Pensei em um número, somei 8 e obtive 15. Qual era o número inicial?",
                answer: 7,
                explanation: "15 - 8 = 7"
            },
            {
                text: "Pensei em um número, multipliquei por 3, subtraí 4 e obtive 11. Qual era o número?",
                answer: 5,
                explanation: "Inverso: 11 + 4 = 15, 15 ÷ 3 = 5"
            },
            {
                text: "Pensei em um número, subtraí 7, multipliquei por 2 e obtive 20. Qual era o número?",
                answer: 17,
                explanation: "Inverso: 20 ÷ 2 = 10, 10 + 7 = 17"
            }
        ];
        
        // Inicializar o jogo
        function initGame() {
            updateDisplays();
            updateChallenge();
        }
        
        // Adicionar uma operação à máquina direta
        function addOperation(operator, value) {
            operations.push({operator, value});
            updateDisplays();
        }
        
        // Desfazer a última operação
        function undoOperation() {
            if (operations.length &gt; 0) {
                operations.pop();
                updateDisplays();
            }
        }
        
        // Reiniciar a máquina
        function resetMachine() {
            operations = [];
            startNumber = Math.floor(Math.random() * 20) + 1;
            updateDisplays();
            document.getElementById('feedback').className = 'feedback';
        }
        
        // Atualizar as máquinas na tela
        function updateDisplays() {
            updateDirectMachine();
            updateInverseMachine();
            updateStartNumber();
        }
        
        // Atualizar a máquina direta
        function updateDirectMachine() {
            const machine = document.getElementById('direct-machine');
            let html = '';
            
            if (operations.length === 0) {
                html = '&lt;p style="text-align: center; color: #666;"&gt;Use os botões para adicionar operações&lt;/p&gt;';
            } else {
                // Calcular passo a passo
                let currentValue = startNumber;
                
                html += '&lt;div class="operation-step"&gt;';
                html += `&lt;div class="number-box"&gt;${currentValue}&lt;/div&gt;`;
                html += '&lt;div class="arrow"&gt;→&lt;/div&gt;';
                html += '&lt;div style="font-weight: bold; color: #495057;"&gt;Início&lt;/div&gt;';
                html += '&lt;/div&gt;';
                
                operations.forEach((op, index) =&gt; {
                    // Calcular novo valor
                    if (op.operator === '+') currentValue += op.value;
                    else if (op.operator === '-') currentValue -= op.value;
                    else if (op.operator === '×') currentValue *= op.value;
                    else if (op.operator === '÷') currentValue /= op.value;
                    
                    html += '&lt;div class="operation-step"&gt;';
                    html += `&lt;div class="operation-box"&gt;${op.operator} ${op.value}&lt;/div&gt;`;
                    html += '&lt;div class="arrow"&gt;→&lt;/div&gt;';
                    html += `&lt;div class="number-box"&gt;${currentValue}&lt;/div&gt;`;
                    html += '&lt;/div&gt;';
                });
                
                html += `&lt;p style="text-align: center; margin-top: 15px; font-weight: bold;"&gt;Resultado final: &lt;span style="color: #e64980; font-size: 1.3rem;"&gt;${currentValue}&lt;/span&gt;&lt;/p&gt;`;
            }
            
            machine.innerHTML = html;
        }
        
        // Atualizar a máquina inversa
        function updateInverseMachine() {
            const machine = document.getElementById('inverse-machine');
            
            if (operations.length === 0) {
                machine.innerHTML = '&lt;p style="text-align: center; color: #666;"&gt;Adicione operações na máquina direta primeiro&lt;/p&gt;';
                return;
            }
            
            let html = '';
            let currentValue;
            
            // Se não temos resultado ainda, começamos do final
            const lastResult = calculateFinalResult();
            
            html += '&lt;div class="operation-step"&gt;';
            html += `&lt;div class="number-box"&gt;${lastResult}&lt;/div&gt;`;
            html += '&lt;div class="arrow"&gt;→&lt;/div&gt;';
            html += '&lt;div style="font-weight: bold; color: #495057;"&gt;Final&lt;/div&gt;';
            html += '&lt;/div&gt;';
            
            // Mostrar operações inversas na ordem reversa
            for (let i = operations.length - 1; i &gt;= 0; i--) {
                const op = operations[i];
                let inverseOp, inverseValue;
                
                // Determinar operação inversa
                if (op.operator === '+') {
                    inverseOp = '-';
                    inverseValue = op.value;
                } else if (op.operator === '-') {
                    inverseOp = '+';
                    inverseValue = op.value;
                } else if (op.operator === '×') {
                    inverseOp = '÷';
                    inverseValue = op.value;
                } else if (op.operator === '÷') {
                    inverseOp = '×';
                    inverseValue = op.value;
                }
                
                html += '&lt;div class="operation-step"&gt;';
                html += `&lt;div class="operation-box" style="background: #51cf66;"&gt;${inverseOp} ${inverseValue}&lt;/div&gt;`;
                html += '&lt;div class="arrow"&gt;→&lt;/div&gt;';
                html += '&lt;div class="number-box"&gt;?&lt;/div&gt;';
                html += '&lt;/div&gt;';
            }
            
            html += '&lt;p style="text-align: center; margin-top: 15px;"&gt;Aplique as operações inversas para descobrir o número inicial!&lt;/p&gt;';
            
            machine.innerHTML = html;
        }
        
        // Atualizar o número inicial
        function updateStartNumber() {
            document.getElementById('start-number').textContent = '?';
        }
        
        // Calcular o resultado final
        function calculateFinalResult() {
            let currentValue = startNumber;
            operations.forEach(op =&gt; {
                if (op.operator === '+') currentValue += op.value;
                else if (op.operator === '-') currentValue -= op.value;
                else if (op.operator === '×') currentValue *= op.value;
                else if (op.operator === '÷') currentValue /= op.value;
            });
            return currentValue;
        }
        
        // Verificar a resposta do usuário
        function checkAnswer() {
            const input = document.getElementById('guess-input');
            const feedback = document.getElementById('feedback');
            const userAnswer = parseInt(input.value);
            
            if (isNaN(userAnswer)) {
                feedback.textContent = "Digite um número válido!";
                feedback.className = "feedback incorrect";
                return;
            }
            
            if (userAnswer === startNumber) {
                feedback.textContent = `✅ Correto! O número inicial era ${startNumber}. Você usou o pensamento reverso!`;
                feedback.className = "feedback correct";
                
                // Avançar de nível após alguns acertos
                setTimeout(() =&gt; {
                    if (operations.length &gt;= 2) {
                        advanceLevel();
                    }
                }, 1500);
            } else {
                // Dar uma dica
                const diff = userAnswer - startNumber;
                let hint = "";
                
                if (diff &gt; 0) {
                    hint = `Tente um número ${Math.abs(diff)} menor`;
                } else {
                    hint = `Tente um número ${Math.abs(diff)} maior`;
                }
                
                feedback.textContent = `❌ Não é isso. ${hint}. Tente novamente!`;
                feedback.className = "feedback incorrect";
            }
        }
        
        // Avançar de nível
        function advanceLevel() {
            if (currentLevel &lt; 3) {
                currentLevel++;
                updateLevelIndicator();
                updateChallenge();
                resetMachine();
                
                // Adicionar operações automaticamente para o novo nível
                if (currentLevel === 2) {
                    setTimeout(() =&gt; {
                        addOperation('+', 8);
                        addOperation('×', 2);
                    }, 500);
                } else if (currentLevel === 3) {
                    setTimeout(() =&gt; {
                        addOperation('×', 3);
                        addOperation('-', 5);
                        addOperation('÷', 2);
                    }, 500);
                }
            }
        }
        
        // Atualizar indicador de nível
        function updateLevelIndicator() {
            for (let i = 1; i &lt;= 3; i++) {
                const dot = document.getElementById(`level${i}`);
                if (i &lt;= currentLevel) {
                    dot.classList.add('active');
                } else {
                    dot.classList.remove('active');
                }
            }
        }
        
        // Atualizar desafio
        function updateChallenge() {
            const challenge = challenges[currentLevel - 1];
            document.getElementById('challenge-text').textContent = challenge.text;
            document.getElementById('challenge-feedback').className = 'feedback';
            document.getElementById('challenge-input').value = '';
        }
        
        // Verificar resposta do desafio
        function checkChallenge() {
            const input = document.getElementById('challenge-input');
            const feedback = document.getElementById('challenge-feedback');
            const challenge = challenges[currentLevel - 1];
            const userAnswer = parseInt(input.value);
            
            if (isNaN(userAnswer)) {
                feedback.textContent = "Digite um número válido!";
                feedback.className = "feedback incorrect";
                return;
            }
            
            if (userAnswer === challenge.answer) {
                feedback.textContent = `🎉 Excelente! ${challenge.explanation}`;
                feedback.className = "feedback correct";
            } else {
                feedback.textContent = `Tente novamente! Lembre-se: ${challenge.explanation}`;
                feedback.className = "feedback incorrect";
            }
        }
        
        // Inicializar quando a página carregar
        document.addEventListener('DOMContentLoaded', initGame);
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;