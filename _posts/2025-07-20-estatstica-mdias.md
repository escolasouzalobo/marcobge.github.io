---
layout: post
title: "Estatística: Médias"
date: 2025-07-20
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Estatística Básica - 7º Ano&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: 'Arial', sans-serif;
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
        .conceito {
            background-color: white;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .conceito h2 {
            color: #3498db;
            border-bottom: 2px solid #3498db;
            padding-bottom: 5px;
        }
        .calculadora {
            background-color: #e8f4fc;
            padding: 15px;
            border-radius: 10px;
            margin-top: 15px;
        }
        input, button {
            padding: 8px;
            margin: 5px 0;
            border-radius: 5px;
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
        #resultados {
            margin-top: 15px;
            font-weight: bold;
        }
        .exemplo {
            font-style: italic;
            color: #7f8c8d;
        }
        .dica {
            background-color: #fffde7;
            padding: 10px;
            border-left: 4px solid #ffd600;
            margin: 10px 0;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Estatística Básica&lt;/h1&gt;
    
    &lt;div class="conceito"&gt;
        &lt;h2&gt;Média Aritmética&lt;/h2&gt;
        &lt;p&gt;A média aritmética é calculada somando todos os valores e dividindo pelo número de valores.&lt;/p&gt;
        &lt;p class="exemplo"&gt;Exemplo: Na lista 5, 7, 9, a média é (5 + 7 + 9) ÷ 3 = 7&lt;/p&gt;
        
        &lt;div class="calculadora"&gt;
            &lt;h3&gt;Calcular Média&lt;/h3&gt;
            &lt;p&gt;Digite números separados por vírgula:&lt;/p&gt;
            &lt;input type="text" id="valoresMedia" placeholder="Ex: 5, 7, 9"&gt;
            &lt;button onclick="calcularMedia()"&gt;Calcular Média&lt;/button&gt;
            &lt;div id="resultadoMedia"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="conceito"&gt;
        &lt;h2&gt;Mediana&lt;/h2&gt;
        &lt;p&gt;A mediana é o valor central em uma lista ordenada. Se houver dois valores centrais, calcula-se a média entre eles.&lt;/p&gt;
        &lt;p class="exemplo"&gt;Exemplo: Na lista ordenada 3, 5, 7, a mediana é 5. Na lista 3, 5, 7, 9, a mediana é (5 + 7) ÷ 2 = 6&lt;/p&gt;
        
        &lt;div class="calculadora"&gt;
            &lt;h3&gt;Calcular Mediana&lt;/h3&gt;
            &lt;p&gt;Digite números separados por vírgula:&lt;/p&gt;
            &lt;input type="text" id="valoresMediana" placeholder="Ex: 3, 5, 7"&gt;
            &lt;button onclick="calcularMediana()"&gt;Calcular Mediana&lt;/button&gt;
            &lt;div id="resultadoMediana"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="conceito"&gt;
        &lt;h2&gt;Moda&lt;/h2&gt;
        &lt;p&gt;A moda é o valor que aparece com mais frequência em um conjunto de dados.&lt;/p&gt;
        &lt;p class="exemplo"&gt;Exemplo: Na lista 2, 3, 3, 5, a moda é 3. Na lista 2, 3, 4, 5, não há moda.&lt;/p&gt;
        
        &lt;div class="calculadora"&gt;
            &lt;h3&gt;Calcular Moda&lt;/h3&gt;
            &lt;p&gt;Digite números separados por vírgula:&lt;/p&gt;
            &lt;input type="text" id="valoresModa" placeholder="Ex: 2, 3, 3, 5"&gt;
            &lt;button onclick="calcularModa()"&gt;Calcular Moda&lt;/button&gt;
            &lt;div id="resultadoModa"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="dica"&gt;
        &lt;h3&gt;Dica importante!&lt;/h3&gt;
        &lt;p&gt;Lembre-se de sempre ordenar os números antes de calcular a mediana. A moda pode não existir (quando todos os valores aparecem com a mesma frequência) ou pode haver mais de uma moda (quando vários valores aparecem com a mesma frequência máxima).&lt;/p&gt;
    &lt;/div&gt;

    &lt;script&gt;
        function converterParaArray(texto) {
            return texto.split(',').map(item =&gt; parseFloat(item.trim())).filter(num =&gt; !isNaN(num));
        }
        
        function calcularMedia() {
            const valores = converterParaArray(document.getElementById('valoresMedia').value);
            if (valores.length === 0) {
                document.getElementById('resultadoMedia').innerHTML = "Por favor, insira números válidos.";
                return;
            }
            
            const soma = valores.reduce((a, b) =&gt; a + b, 0);
            const media = soma / valores.length;
            document.getElementById('resultadoMedia').innerHTML = `Média: ${media.toFixed(2)}`;
        }
        
        function calcularMediana() {
            const valores = converterParaArray(document.getElementById('valoresMediana').value);
            if (valores.length === 0) {
                document.getElementById('resultadoMediana').innerHTML = "Por favor, insira números válidos.";
                return;
            }
            
            const ordenados = [...valores].sort((a, b) =&gt; a - b);
            const meio = Math.floor(ordenados.length / 2);
            
            let mediana;
            if (ordenados.length % 2 === 0) {
                mediana = (ordenados[meio - 1] + ordenados[meio]) / 2;
            } else {
                mediana = ordenados[meio];
            }
            
            document.getElementById('resultadoMediana').innerHTML = `Mediana: ${mediana}`;
        }
        
        function calcularModa() {
            const valores = converterParaArray(document.getElementById('valoresModa').value);
            if (valores.length === 0) {
                document.getElementById('resultadoModa').innerHTML = "Por favor, insira números válidos.";
                return;
            }
            
            const frequencia = {};
            valores.forEach(num =&gt; {
                frequencia[num] = (frequencia[num] || 0) + 1;
            });
            
            const maxFrequencia = Math.max(...Object.values(frequencia));
            const modas = Object.keys(frequencia).filter(num =&gt; frequencia[num] === maxFrequencia);
            
            if (modas.length === Object.keys(frequencia).length) {
                document.getElementById('resultadoModa').innerHTML = "Não há moda (todos os valores aparecem com a mesma frequência).";
            } else if (modas.length &gt; 1) {
                document.getElementById('resultadoModa').innerHTML = `Modas: ${modas.join(', ')} (cada uma aparece ${maxFrequencia} vezes)`;
            } else {
                document.getElementById('resultadoModa').innerHTML = `Moda: ${modas[0]} (aparece ${maxFrequencia} vezes)`;
            }
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;