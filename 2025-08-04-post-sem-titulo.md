---
layout: post
title: "Post Sem Titulo"
date: 2025-08-04
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Problemas Interativos de Divisão com Decimais&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f0f8ff;
            line-height: 1.6;
        }
        h1 {
            color: #1e3c72;
            text-align: center;
            margin-bottom: 30px;
        }
        .problema {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 25px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            border-left: 5px solid #4b6cb7;
        }
        button {
            background-color: #4b6cb7;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s;
            margin-top: 10px;
        }
        button:hover {
            background-color: #1e3c72;
        }
        input[type="number"] {
            padding: 8px;
            border: 2px solid #ddd;
            border-radius: 5px;
            width: 80px;
            margin: 0 5px;
            font-size: 16px;
        }
        .resposta-input {
            width: 120px;
            margin-right: 10px;
        }
        .feedback {
            margin-top: 15px;
            padding: 10px;
            border-radius: 5px;
            font-weight: bold;
        }
        .correto {
            background-color: #e6f7e6;
            color: #2e7d32;
            border-left: 5px solid #2e7d32;
        }
        .incorreto {
            background-color: #ffebee;
            color: #c62828;
            border-left: 5px solid #c62828;
        }
        .variavel {
            background-color: #f0f0f0;
            padding: 5px 10px;
            border-radius: 4px;
            font-weight: bold;
            color: #1e3c72;
        }
        .dica {
            font-style: italic;
            color: #555;
            margin-top: 10px;
            display: none;
        }
        .mostrar-dica {
            color: #4b6cb7;
            text-decoration: underline;
            cursor: pointer;
            font-size: 14px;
        }
        .atualizar {
            background-color: #2ecc71;
            margin-left: 10px;
        }
        .atualizar:hover {
            background-color: #27ae60;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Problemas Interativos de Divisão com Decimais&lt;/h1&gt;
    &lt;p style="text-align: center;"&gt;Altere os valores dos problemas e resolva com os novos números!&lt;/p&gt;
    
    &lt;div class="problema"&gt;
        &lt;h3&gt;Problema 1: Compra de Material Escolar&lt;/h3&gt;
        &lt;p&gt;Joana gastou R$ &lt;input type="number" step="0.01" id="valorTotal1" value="37.50" min="0"&gt; comprando 
           &lt;input type="number" id="quantidade1" value="5" min="1"&gt; cadernos iguais. Qual foi o preço de cada caderno?&lt;/p&gt;
        &lt;button onclick="atualizarProblema(1)"&gt;Atualizar Problema&lt;/button&gt;
        &lt;span class="mostrar-dica" onclick="mostrarDica(1)"&gt;Preciso de ajuda&lt;/span&gt;
        &lt;div id="dica1" class="dica"&gt;Dica: Divida o valor total pelo número de cadernos.&lt;/div&gt;
        &lt;input type="number" step="0.01" id="resposta1" placeholder="R$" class="resposta-input"&gt;
        &lt;button onclick="verificarResposta(1)"&gt;Verificar Resposta&lt;/button&gt;
        &lt;div id="feedback1" class="feedback"&gt;&lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="problema"&gt;
        &lt;h3&gt;Problema 2: Produção de Sucos&lt;/h3&gt;
        &lt;p&gt;Um restaurante preparou &lt;input type="number" step="0.1" id="litrosSuco2" value="18.9" min="0"&gt; litros de suco para distribuir igualmente em 
           &lt;input type="number" id="jarros2" value="6" min="1"&gt; jarros. Quantos litros em cada jarro?&lt;/p&gt;
        &lt;button onclick="atualizarProblema(2)"&gt;Atualizar Problema&lt;/button&gt;
        &lt;span class="mostrar-dica" onclick="mostrarDica(2)"&gt;Preciso de ajuda&lt;/span&gt;
        &lt;div id="dica2" class="dica"&gt;Dica: Divida o volume total pelo número de jarros.&lt;/div&gt;
        &lt;input type="number" step="0.01" id="resposta2" placeholder="Litros" class="resposta-input"&gt;
        &lt;button onclick="verificarResposta(2)"&gt;Verificar Resposta&lt;/button&gt;
        &lt;div id="feedback2" class="feedback"&gt;&lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="problema"&gt;
        &lt;h3&gt;Problema 3: Viagem de Férias&lt;/h3&gt;
        &lt;p&gt;Uma família percorreu &lt;input type="number" step="0.1" id="distancia3" value="256.5" min="0"&gt; km em 
           &lt;input type="number" step="0.1" id="tempo3" value="4.5" min="0.1"&gt; horas. Qual foi a velocidade média?&lt;/p&gt;
        &lt;button onclick="atualizarProblema(3)"&gt;Atualizar Problema&lt;/button&gt;
        &lt;span class="mostrar-dica" onclick="mostrarDica(3)"&gt;Preciso de ajuda&lt;/span&gt;
        &lt;div id="dica3" class="dica"&gt;Dica: Velocidade = distância ÷ tempo.&lt;/div&gt;
        &lt;input type="number" step="0.01" id="resposta3" placeholder="km/h" class="resposta-input"&gt;
        &lt;button onclick="verificarResposta(3)"&gt;Verificar Resposta&lt;/button&gt;
        &lt;div id="feedback3" class="feedback"&gt;&lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="problema"&gt;
        &lt;h3&gt;Problema 4: Receita de Bolo&lt;/h3&gt;
        &lt;p&gt;Para fazer &lt;input type="number" id="brigadeiros4" value="24" min="1"&gt; brigadeiros, usa-se 
           &lt;input type="number" step="0.1" id="chocolate4" value="1.8" min="0.1"&gt; kg de chocolate. Quantos kg por brigadeiro?&lt;/p&gt;
        &lt;button onclick="atualizarProblema(4)"&gt;Atualizar Problema&lt;/button&gt;
        &lt;span class="mostrar-dica" onclick="mostrarDica(4)"&gt;Preciso de ajuda&lt;/span&gt;
        &lt;div id="dica4" class="dica"&gt;Dica: Divida o chocolate total pelo número de brigadeiros.&lt;/div&gt;
        &lt;input type="number" step="0.001" id="resposta4" placeholder="kg" class="resposta-input"&gt;
        &lt;button onclick="verificarResposta(4)"&gt;Verificar Resposta&lt;/button&gt;
        &lt;div id="feedback4" class="feedback"&gt;&lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="problema"&gt;
        &lt;h3&gt;Problema 5: Economia Doméstica&lt;/h3&gt;
        &lt;p&gt;Pedro quer economizar R$ &lt;input type="number" step="0.01" id="meta5" value="157.50" min="0"&gt; em 
           &lt;input type="number" id="semanas5" value="6" min="1"&gt; semanas. Quanto guardar por semana?&lt;/p&gt;
        &lt;button onclick="atualizarProblema(5)"&gt;Atualizar Problema&lt;/button&gt;
        &lt;span class="mostrar-dica" onclick="mostrarDica(5)"&gt;Preciso de ajuda&lt;/span&gt;
        &lt;div id="dica5" class="dica"&gt;Dica: Divida o total pelo número de semanas.&lt;/div&gt;
        &lt;input type="number" step="0.01" id="resposta5" placeholder="R$/semana" class="resposta-input"&gt;
        &lt;button onclick="verificarResposta(5)"&gt;Verificar Resposta&lt;/button&gt;
        &lt;div id="feedback5" class="feedback"&gt;&lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        // Armazena as respostas corretas atualizadas
        let respostasCorretas = {
            1: 7.5,
            2: 3.15,
            3: 57,
            4: 0.075,
            5: 26.25
        };

        function atualizarProblema(numeroProblema) {
            switch(numeroProblema) {
                case 1:
                    const valorTotal1 = parseFloat(document.getElementById('valorTotal1').value);
                    const quantidade1 = parseInt(document.getElementById('quantidade1').value);
                    respostasCorretas[1] = valorTotal1 / quantidade1;
                    break;
                case 2:
                    const litrosSuco2 = parseFloat(document.getElementById('litrosSuco2').value);
                    const jarros2 = parseInt(document.getElementById('jarros2').value);
                    respostasCorretas[2] = litrosSuco2 / jarros2;
                    break;
                case 3:
                    const distancia3 = parseFloat(document.getElementById('distancia3').value);
                    const tempo3 = parseFloat(document.getElementById('tempo3').value);
                    respostasCorretas[3] = distancia3 / tempo3;
                    break;
                case 4:
                    const chocolate4 = parseFloat(document.getElementById('chocolate4').value);
                    const brigadeiros4 = parseInt(document.getElementById('brigadeiros4').value);
                    respostasCorretas[4] = chocolate4 / brigadeiros4;
                    break;
                case 5:
                    const meta5 = parseFloat(document.getElementById('meta5').value);
                    const semanas5 = parseInt(document.getElementById('semanas5').value);
                    respostasCorretas[5] = meta5 / semanas5;
                    break;
            }
            
            // Limpa o feedback quando o problema é atualizado
            document.getElementById(`feedback${numeroProblema}`).textContent = "";
            document.getElementById(`feedback${numeroProblema}`).className = "feedback";
            document.getElementById(`resposta${numeroProblema}`).value = "";
            
            alert(`Problema ${numeroProblema} atualizado! Resolva com os novos valores.`);
        }

        function verificarResposta(numeroProblema) {
            const respostaUsuario = parseFloat(document.getElementById(`resposta${numeroProblema}`).value);
            const feedbackElement = document.getElementById(`feedback${numeroProblema}`);
            
            if (isNaN(respostaUsuario)) {
                feedbackElement.textContent = "Por favor, insira um número válido.";
                feedbackElement.className = "feedback incorreto";
                return;
            }
            
            // Comparação com margem de erro para lidar com arredondamentos
            if (Math.abs(respostaUsuario - respostasCorretas[numeroProblema]) &lt; 0.0001) {
                feedbackElement.textContent = `✓ Correto! Cada unidade custa R$ ${respostasCorretas[numeroProblema].toFixed(2)}`;
                feedbackElement.className = "feedback correto";
            } else {
                feedbackElement.textContent = `✗ Incorreto. O valor correto é ${respostasCorretas[numeroProblema].toFixed(2)}. Tente novamente!`;
                feedbackElement.className = "feedback incorreto";
            }
        }

        function mostrarDica(numeroProblema) {
            const dicaElement = document.getElementById(`dica${numeroProblema}`);
            dicaElement.style.display = dicaElement.style.display === "block" ? "none" : "block";
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;