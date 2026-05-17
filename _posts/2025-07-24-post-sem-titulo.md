---
layout: post
title: "Post Sem Titulo"
date: 2025-07-24
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Sistema de Numeração Decimal&lt;/title&gt;
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
        .container {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .number-input {
            text-align: center;
            margin: 20px 0;
        }
        input {
            font-size: 24px;
            padding: 10px;
            width: 200px;
            text-align: center;
            border: 2px solid #3498db;
            border-radius: 5px;
        }
        .position-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        .position-table th, .position-table td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: center;
        }
        .position-table th {
            background-color: #3498db;
            color: white;
        }
        .position-table tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        .explanation {
            background-color: #e8f4fc;
            padding: 15px;
            border-radius: 5px;
            margin-top: 20px;
        }
        .digit {
            font-weight: bold;
            color: #e74c3c;
        }
        .place-value {
            font-weight: bold;
            color: #27ae60;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;div class="container"&gt;
        &lt;h1&gt;Sistema de Numeração Decimal&lt;/h1&gt;
        
        &lt;p&gt;O sistema decimal é um sistema de numeração posicional que utiliza a base 10. Ele utiliza 10 algarismos (0 a 9) e o valor de cada dígito depende de sua posição no número.&lt;/p&gt;
        
        &lt;div class="number-input"&gt;
            &lt;label for="number"&gt;Digite um número:&lt;/label&gt;&lt;br&gt;
            &lt;input type="number" id="number" min="0" value="1234" oninput="updateNumber()"&gt;
        &lt;/div&gt;
        
        &lt;table class="position-table" id="positionTable"&gt;
            &lt;thead&gt;
                &lt;tr&gt;
                    &lt;th&gt;Número&lt;/th&gt;
                    &lt;th&gt;Posição&lt;/th&gt;
                    &lt;th&gt;Valor Posicional&lt;/th&gt;
                    &lt;th&gt;Valor do Dígito&lt;/th&gt;
                &lt;/tr&gt;
            &lt;/thead&gt;
            &lt;tbody id="tableBody"&gt;
                &lt;!-- Conteúdo será gerado por JavaScript --&gt;
            &lt;/tbody&gt;
        &lt;/table&gt;
        
        &lt;div class="explanation" id="explanation"&gt;
            &lt;!-- Explicação será gerada por JavaScript --&gt;
        &lt;/div&gt;
        
        &lt;h2&gt;Como funciona o sistema decimal?&lt;/h2&gt;
        &lt;ul&gt;
            &lt;li&gt;Utiliza 10 algarismos: 0, 1, 2, 3, 4, 5, 6, 7, 8 e 9&lt;/li&gt;
            &lt;li&gt;Cada posição representa uma potência de 10&lt;/li&gt;
            &lt;li&gt;O valor do dígito é multiplicado pelo valor posicional&lt;/li&gt;
            &lt;li&gt;Exemplo: 345 = 3×100 + 4×10 + 5×1&lt;/li&gt;
        &lt;/ul&gt;
    &lt;/div&gt;

    &lt;script&gt;
        function updateNumber() {
            const numberInput = document.getElementById('number').value;
            const numberStr = numberInput.toString();
            const tableBody = document.getElementById('tableBody');
            const explanation = document.getElementById('explanation');
            
            // Limpa a tabela
            tableBody.innerHTML = '';
            
            // Cria as linhas da tabela para cada dígito
            let totalValue = 0;
            let explanationHTML = '&lt;p&gt;O número &lt;span class="digit"&gt;' + numberStr + '&lt;/span&gt; é composto por:&lt;/p&gt;&lt;ul&gt;';
            
            for (let i = 0; i &lt; numberStr.length; i++) {
                const digit = numberStr[numberStr.length - 1 - i];
                const placeValue = Math.pow(10, i);
                const digitValue = parseInt(digit) * placeValue;
                totalValue += digitValue;
                
                const positionName = getPositionName(i);
                
                // Adiciona linha na tabela
                const row = document.createElement('tr');
                row.innerHTML = `
                    &lt;td&gt;${digit}&lt;/td&gt;
                    &lt;td&gt;${positionName}&lt;/td&gt;
                    &lt;td&gt;${placeValue.toLocaleString()}&lt;/td&gt;
                    &lt;td&gt;${digitValue.toLocaleString()}&lt;/td&gt;
                `;
                tableBody.appendChild(row);
                
                // Adiciona à explicação
                explanationHTML += `&lt;li&gt;Dígito &lt;span class="digit"&gt;${digit}&lt;/span&gt; na posição de &lt;span class="place-value"&gt;${positionName}&lt;/span&gt; (${placeValue.toLocaleString()}): ${digit} × ${placeValue.toLocaleString()} = ${digitValue.toLocaleString()}&lt;/li&gt;`;
            }
            
            explanationHTML += `&lt;/ul&gt;&lt;p&gt;Somando todos os valores: &lt;strong&gt;${totalValue.toLocaleString()}&lt;/strong&gt;&lt;/p&gt;`;
            explanation.innerHTML = explanationHTML;
        }
        
        function getPositionName(positionIndex) {
            const names = [
                "unidades",
                "dezenas",
                "centenas",
                "unidades de milhar",
                "dezenas de milhar",
                "centenas de milhar",
                "unidades de milhão",
                "dezenas de milhão",
                "centenas de milhão",
                "unidades de bilhão"
            ];
            
            return positionIndex &lt; names.length ? names[positionIndex] : `10^${positionIndex}`;
        }
        
        // Inicializa a página
        window.onload = updateNumber;
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;