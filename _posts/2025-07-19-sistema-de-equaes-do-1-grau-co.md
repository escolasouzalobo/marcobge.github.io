---
layout: post
title: "Sistema de equações do 1º grau com duas incógnitas"
date: 2025-07-19
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Aula Interativa - Sistemas de Equações&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            color: #333;
        }
        h1, h2 {
            color: #2c3e50;
        }
        .equacao {
            background-color: #f8f9fa;
            padding: 10px;
            border-left: 4px solid #3498db;
            margin: 15px 0;
            font-family: monospace;
            font-size: 1.1em;
        }
        .passo {
            background-color: #e8f4f8;
            padding: 10px;
            border-radius: 5px;
            margin: 10px 0;
        }
        .exercicio {
            background-color: #eaf7ea;
            padding: 15px;
            border-radius: 5px;
            margin: 20px 0;
        }
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background-color: #2980b9;
        }
        #solucao {
            display: none;
            margin-top: 15px;
            padding: 10px;
            background-color: #f0f0f0;
            border-radius: 4px;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Aula Interativa: Sistema de Equações com Duas Incógnitas - Método da Substituição&lt;/h1&gt;
    
    &lt;p&gt;Bem-vindo à nossa aula interativa sobre resolução de sistemas de equações com duas incógnitas usando o método da substituição!&lt;/p&gt;
    
    &lt;h2&gt;Introdução&lt;/h2&gt;
    &lt;p&gt;Um sistema de equações com duas incógnitas consiste em duas equações que relacionam as mesmas variáveis.&lt;/p&gt;
    
    &lt;div class="equacao"&gt;
        &lt;p&gt;1) 2x + y = 7&lt;/p&gt;
        &lt;p&gt;2) x - y = -1&lt;/p&gt;
    &lt;/div&gt;
    
    &lt;h2&gt;Passo a Passo&lt;/h2&gt;
    
    &lt;div class="passo"&gt;
        &lt;h3&gt;Passo 1: Isolar uma variável&lt;/h3&gt;
        &lt;p&gt;Vamos isolar x na segunda equação:&lt;/p&gt;
        &lt;div class="equacao"&gt;
            x - y = -1&lt;br&gt;
            x = y - 1
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="passo"&gt;
        &lt;h3&gt;Passo 2: Substituir na outra equação&lt;/h3&gt;
        &lt;p&gt;Substituímos x = y - 1 na primeira equação:&lt;/p&gt;
        &lt;div class="equacao"&gt;
            2x + y = 7&lt;br&gt;
            2(y - 1) + y = 7
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="passo"&gt;
        &lt;h3&gt;Passo 3: Resolver para a variável restante&lt;/h3&gt;
        &lt;div class="equacao"&gt;
            2y - 2 + y = 7&lt;br&gt;
            3y - 2 = 7&lt;br&gt;
            3y = 9&lt;br&gt;
            y = 3
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="passo"&gt;
        &lt;h3&gt;Passo 4: Encontrar o valor da outra variável&lt;/h3&gt;
        &lt;div class="equacao"&gt;
            x = y - 1&lt;br&gt;
            x = 3 - 1&lt;br&gt;
            x = 2
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="passo"&gt;
        &lt;h3&gt;Verificação&lt;/h3&gt;
        &lt;p&gt;Verificando a solução (2, 3):&lt;/p&gt;
        &lt;div class="equacao"&gt;
            1) 2(2) + 3 = 7 ✔&lt;br&gt;
            2) 2 - 3 = -1 ✔
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="exercicio"&gt;
        &lt;h2&gt;Exercício Interativo&lt;/h2&gt;
        &lt;p&gt;Tente resolver este sistema usando o método da substituição:&lt;/p&gt;
        &lt;div class="equacao"&gt;
            1) 3x + 2y = 12&lt;br&gt;
            2) x - y = 1
        &lt;/div&gt;
        
        &lt;button onclick="mostrarSolucao()"&gt;Mostrar Solução&lt;/button&gt;
        
        &lt;div id="solucao"&gt;
            &lt;h3&gt;Solução passo a passo:&lt;/h3&gt;
            &lt;div class="equacao"&gt;
                1. Isolando x na segunda equação: x = y + 1&lt;br&gt;
                2. Substituindo na primeira: 3(y + 1) + 2y = 12&lt;br&gt;
                3. Desenvolvendo: 3y + 3 + 2y = 12 → 5y + 3 = 12 → 5y = 9 → y = 9/5&lt;br&gt;
                4. Encontrando x: x = (9/5) + 1 = 14/5
            &lt;/div&gt;
            &lt;p&gt;Solução: x = 14/5, y = 9/5&lt;/p&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;h2&gt;Dicas Importantes&lt;/h2&gt;
    &lt;ul&gt;
        &lt;li&gt;Comece isolando a variável que parece mais fácil&lt;/li&gt;
        &lt;li&gt;Preste atenção aos sinais ao substituir&lt;/li&gt;
        &lt;li&gt;Verifique sempre sua solução nas equações originais&lt;/li&gt;
        &lt;li&gt;Se chegar em uma contradição (como 0 = 5), o sistema não tem solução&lt;/li&gt;
        &lt;li&gt;Se chegar em uma identidade (como 0 = 0), o sistema tem infinitas soluções&lt;/li&gt;
    &lt;/ul&gt;
    
    &lt;script&gt;
        function mostrarSolucao() {
            const solucao = document.getElementById('solucao');
            if (solucao.style.display === 'block') {
                solucao.style.display = 'none';
            } else {
                solucao.style.display = 'block';
            }
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;