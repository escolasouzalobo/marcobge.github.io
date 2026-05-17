---
layout: post
title: "Valor numérico de uma expressão algébrica"
date: 2025-08-02
---

&lt;p&gt;&lt;/p&gt;&lt;div class="separator" style="clear: both; text-align: center;"&gt;&lt;iframe allowfullscreen="" class="BLOG_video_class" height="266" src="https://www.youtube.com/embed/nC0G78HC91Q" width="320" youtube-src-id="nC0G78HC91Q"&gt;&lt;/iframe&gt;&lt;/div&gt;&lt;br /&gt;&amp;nbsp;&lt;p&gt;&lt;/p&gt;&lt;div&gt;&lt;br /&gt;&lt;/div&gt;
&lt;!DOCTYPE html&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Calculadora de Expressões Algébricas&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
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
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        label {
            display: block;
            margin: 10px 0 5px;
            font-weight: bold;
        }
        input, button {
            width: 100%;
            padding: 10px;
            margin: 5px 0 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
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
            font-size: 18px;
            margin-top: 20px;
            padding: 10px;
            background-color: #e8f4fc;
            border-radius: 4px;
            display: none;
        }
        .example {
            font-style: italic;
            color: #7f8c8d;
            margin: 10px 0;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;div class="container"&gt;
        &lt;h1&gt;Calculadora de Valor Numérico&lt;/h1&gt;
        &lt;p&gt;Insira uma expressão algébrica e os valores das variáveis para calcular o resultado.&lt;/p&gt;
        
        &lt;label for="expression"&gt;Expressão Algébrica:&lt;/label&gt;
        &lt;input type="text" id="expression" placeholder="Ex: 3*x + 2*y - z"&gt;
        &lt;div class="example"&gt;Dica: Use * para multiplicação (ex: 2*x em vez de 2x).&lt;/div&gt;
        
        &lt;label for="variables"&gt;Variáveis e Valores (separados por vírgula):&lt;/label&gt;
        &lt;input type="text" id="variables" placeholder="Ex: x=5, y=3, z=2"&gt;
        &lt;div class="example"&gt;Formato: nome=valor (ex: a=10, b=5).&lt;/div&gt;
        
        &lt;button onclick="calculate()"&gt;Calcular&lt;/button&gt;
        
        &lt;div id="result"&gt;&lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        function calculate() {
            // Obter os valores dos inputs
            const expression = document.getElementById('expression').value;
            const variablesInput = document.getElementById('variables').value;
            
            // Validar inputs
            if (!expression || !variablesInput) {
                alert("Preencha todos os campos!");
                return;
            }
            
            try {
                // Processar variáveis (transformar "x=5, y=3" em um objeto {x: 5, y: 3})
                const variables = {};
                variablesInput.split(',').forEach(pair =&gt; {
                    const [name, value] = pair.trim().split('=');
                    variables[name.trim()] = parseFloat(value);
                });
                
                // Substituir variáveis na expressão (ex: "3*x" → "3*5")
                let exprToEval = expression;
                for (const [name, value] of Object.entries(variables)) {
                    exprToEval = exprToEval.replace(new RegExp(name, 'g'), value);
                }
                
                // Calcular o resultado (usando eval - cuidado em produção!)
                const result = eval(exprToEval);
                
                // Exibir o resultado
                document.getElementById('result').innerHTML = `
                    &lt;strong&gt;Expressão:&lt;/strong&gt; ${expression} &lt;br&gt;
                    &lt;strong&gt;Substituição:&lt;/strong&gt; ${exprToEval} &lt;br&gt;
                    &lt;strong&gt;Resultado:&lt;/strong&gt; ${result}
                `;
                document.getElementById('result').style.display = 'block';
                
            } catch (error) {
                alert("Erro ao calcular! Verifique a expressão e as variáveis.");
                console.error(error);
            }
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;