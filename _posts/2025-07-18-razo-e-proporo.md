---
layout: post
title: "Razão e proporção"
date: 2025-07-18
---

&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;&lt;/meta&gt;
    &lt;meta content="width=device-width, initial-scale=1.0" name="viewport"&gt;&lt;/meta&gt;
    &lt;title&gt;Razão e Proporção - 7º Ano&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f9ff;
        }
        
        h1, h2, h3 {
            color: #2c3e50;
        }
        
        h1 {
            text-align: center;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
        }
        
        .conteudo {
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .exemplo {
            background-color: #e8f4fc;
            padding: 15px;
            border-left: 4px solid #3498db;
            margin: 15px 0;
            border-radius: 0 5px 5px 0;
        }
        
        .atividade {
            background-color: #e8f8f0;
            padding: 15px;
            border-left: 4px solid #2ecc71;
            margin: 15px 0;
            border-radius: 0 5px 5px 0;
        }
        
        .calculadora {
            background-color: #fef9e7;
            padding: 20px;
            border-radius: 8px;
            margin: 20px 0;
            border: 1px solid #f1c40f;
        }
        
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: #2980b9;
        }
        
        input, select {
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
            margin: 5px 0;
        }
        
        .resultado {
            font-weight: bold;
            color: #e74c3c;
            margin-top: 10px;
        }
        
        .imagem-exemplo {
            text-align: center;
            margin: 15px 0;
        }
        
        .imagem-exemplo img {
            max-width: 100%;
            height: auto;
            border-radius: 5px;
        }
        
        .dica {
            background-color: #fffde7;
            padding: 10px;
            border-left: 4px solid #f39c12;
            margin: 10px 0;
            font-style: italic;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Razões e Proporções&lt;/h1&gt;
    
    &lt;div class="conteudo"&gt;
        &lt;h2&gt;O que é uma Razão?&lt;/h2&gt;
        &lt;p&gt;Uma &lt;strong&gt;razão&lt;/strong&gt; é uma comparação entre duas grandezas. Podemos escrever uma razão de três formas:&lt;/p&gt;
        &lt;ol&gt;
            &lt;li&gt;Usando a palavra "para": 3 para 4&lt;/li&gt;
            &lt;li&gt;Usando dois pontos: 3:4&lt;/li&gt;
            &lt;li&gt;Como uma fração: 3/4&lt;/li&gt;
        &lt;/ol&gt;
        
        &lt;div class="exemplo"&gt;
            &lt;h3&gt;Exemplo:&lt;/h3&gt;
            &lt;p&gt;Em uma sala de aula há 12 meninas e 18 meninos. A razão entre meninas e meninos é:&lt;/p&gt;
            &lt;p&gt;12 para 18, ou 12:18, ou 12/18 (que pode ser simplificada para 2/3)&lt;/p&gt;
        &lt;/div&gt;
        
        &lt;div class="imagem-exemplo"&gt;
            &lt;img alt="Exemplo de razão" src="https://via.placeholder.com/600x200?text=Exemplo+de+Razão:+12+meninas+e+18+meninos" /&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="conteudo"&gt;
        &lt;h2&gt;O que é uma Proporção?&lt;/h2&gt;
        &lt;p&gt;Uma &lt;strong&gt;proporção&lt;/strong&gt; é uma igualdade entre duas razões. Por exemplo:&lt;/p&gt;
        &lt;p&gt;2/3 = 4/6 (lê-se "2 está para 3 assim como 4 está para 6")&lt;/p&gt;
        
        &lt;div class="exemplo"&gt;
            &lt;h3&gt;Propriedade Fundamental das Proporções&lt;/h3&gt;
            &lt;p&gt;Em qualquer proporção, o produto dos extremos é igual ao produto dos meios.&lt;/p&gt;
            &lt;p&gt;a/b = c/d → a × d = b × c&lt;/p&gt;
            &lt;p&gt;Exemplo: 2/3 = 4/6 → 2 × 6 = 3 × 4 → 12 = 12&lt;/p&gt;
        &lt;/div&gt;
        
        &lt;div class="calculadora"&gt;
            &lt;h3&gt;Verificador de Proporções&lt;/h3&gt;
            &lt;p&gt;Digite quatro valores para verificar se formam uma proporção:&lt;/p&gt;
            &lt;input id="num1" placeholder="a" type="number" /&gt; / &lt;input id="den1" placeholder="b" type="number" /&gt; = 
            &lt;input id="num2" placeholder="c" type="number" /&gt; / &lt;input id="den2" placeholder="d" type="number" /&gt;
            &lt;button onclick="verificarProporcao()"&gt;Verificar&lt;/button&gt;
            &lt;div class="resultado" id="resultadoProporcao"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="conteudo"&gt;
        &lt;h2&gt;Resolvendo Problemas com Proporções&lt;/h2&gt;
        &lt;p&gt;Podemos usar proporções para resolver problemas do tipo "Se 3 lápis custam R$ 6,00, quanto custam 5 lápis?"&lt;/p&gt;
        
        &lt;div class="exemplo"&gt;
            &lt;h3&gt;Exemplo:&lt;/h3&gt;
            &lt;p&gt;Se 3 lápis custam R$ 6,00, então 5 lápis custam x.&lt;/p&gt;
            &lt;p&gt;Montamos a proporção: 3/6 = 5/x&lt;/p&gt;
            &lt;p&gt;Pela propriedade fundamental: 3 × x = 6 × 5 → 3x = 30 → x = 10&lt;/p&gt;
            &lt;p&gt;Resposta: 5 lápis custam R$ 10,00&lt;/p&gt;
        &lt;/div&gt;
        
        &lt;div class="calculadora"&gt;
            &lt;h3&gt;Calculadora de Proporções&lt;/h3&gt;
            &lt;p&gt;Resolva problemas do tipo "Se a está para b, então c está para x":&lt;/p&gt;
            &lt;input id="valorA" placeholder="a" type="number" /&gt; / &lt;input id="valorB" placeholder="b" type="number" /&gt; = 
            &lt;input id="valorC" placeholder="c" type="number" /&gt; / &lt;input disabled="" id="valorX" placeholder="x" type="number" /&gt;
            &lt;button onclick="calcularProporcao()"&gt;Calcular x&lt;/button&gt;
            &lt;div class="resultado" id="resultadoCalculo"&gt;&lt;/div&gt;
        &lt;/div&gt;
        
        &lt;div class="dica"&gt;
            &lt;p&gt;Dica: Sempre verifique se as grandezas estão na mesma ordem na proporção. Se estiver comparando lápis com preço em ambos os lados, mantenha essa ordem!&lt;/p&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="conteudo"&gt;
        &lt;h2&gt;Escalas e Mapas&lt;/h2&gt;
        &lt;p&gt;As escalas em mapas são um ótimo exemplo de proporções no dia a dia.&lt;/p&gt;
        
        &lt;div class="exemplo"&gt;
            &lt;h3&gt;Exemplo:&lt;/h3&gt;
            &lt;p&gt;Se um mapa tem escala 1:100.000, isso significa que 1cm no mapa representa 100.000cm (ou 1km) na realidade.&lt;/p&gt;
        &lt;/div&gt;
        
        &lt;div class="calculadora"&gt;
            &lt;h3&gt;Calculadora de Escala&lt;/h3&gt;
            &lt;p&gt;Calcule distâncias reais ou no mapa:&lt;/p&gt;
            &lt;select id="tipoCalculoEscala"&gt;
                &lt;option value="real"&gt;Distância real → Distância no mapa&lt;/option&gt;
                &lt;option value="mapa"&gt;Distância no mapa → Distância real&lt;/option&gt;
            &lt;/select&gt;
            &lt;br /&gt;
            &lt;label for="escala"&gt;Escala do mapa (1:&lt;/label&gt;
            &lt;input id="escala" type="number" value="100000" /&gt;
            )&lt;br /&gt;
            &lt;label for="distancia1"&gt;Distância:&lt;/label&gt;
            &lt;input id="distancia1" type="number" /&gt;
            &lt;button onclick="calcularEscala()"&gt;Calcular&lt;/button&gt;
            &lt;div class="resultado" id="resultadoEscala"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="conteudo"&gt;
        &lt;h2&gt;Atividades Práticas&lt;/h2&gt;
        
        &lt;div class="atividade"&gt;
            &lt;h3&gt;Atividade 1: Razões na Cozinha&lt;/h3&gt;
            &lt;p&gt;Uma receita de bolo usa 2 xícaras de farinha para 3 ovos. Se você quiser usar 9 ovos, quantas xícaras de farinha precisará?&lt;/p&gt;
            &lt;input id="respostaAtividade1" placeholder="Sua resposta" type="number" /&gt;
            &lt;button onclick="verificarAtividade1()"&gt;Verificar&lt;/button&gt;
            &lt;div class="resultado" id="resultadoAtividade1"&gt;&lt;/div&gt;
        &lt;/div&gt;
        
        &lt;div class="atividade"&gt;
            &lt;h3&gt;Atividade 2: Proporções no Esporte&lt;/h3&gt;
            &lt;p&gt;Um jogador de basquete acertou 8 cestas em 10 tentativas. Se ele mantiver essa proporção, quantas cestas acertará em 25 tentativas?&lt;/p&gt;
            &lt;input id="respostaAtividade2" placeholder="Sua resposta" type="number" /&gt;
            &lt;button onclick="verificarAtividade2()"&gt;Verificar&lt;/button&gt;
            &lt;div class="resultado" id="resultadoAtividade2"&gt;&lt;/div&gt;
        &lt;/div&gt;
        
        &lt;div class="atividade"&gt;
            &lt;h3&gt;Atividade 3: Desafio&lt;/h3&gt;
            &lt;p&gt;Em uma escola, a razão entre o número de professores e alunos é 1:15. Se há 45 professores, quantos alunos há na escola?&lt;/p&gt;
            &lt;input id="respostaAtividade3" placeholder="Sua resposta" type="number" /&gt;
            &lt;button onclick="verificarAtividade3()"&gt;Verificar&lt;/button&gt;
            &lt;div class="resultado" id="resultadoAtividade3"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;script&gt;
        function verificarProporcao() {
            const a = parseFloat(document.getElementById('num1').value);
            const b = parseFloat(document.getElementById('den1').value);
            const c = parseFloat(document.getElementById('num2').value);
            const d = parseFloat(document.getElementById('den2').value);
            
            if (a * d === b * c) {
                document.getElementById('resultadoProporcao').innerHTML = "É uma proporção! " + a + "×" + d + " = " + b + "×" + c + " = " + (a*d);
            } else {
                document.getElementById('resultadoProporcao').innerHTML = "Não é uma proporção. " + a + "×" + d + " = " + (a*d) + " e " + b + "×" + c + " = " + (b*c);
            }
        }
        
        function calcularProporcao() {
            const a = parseFloat(document.getElementById('valorA').value);
            const b = parseFloat(document.getElementById('valorB').value);
            const c = parseFloat(document.getElementById('valorC').value);
            
            if (a &amp;&amp; b &amp;&amp; c) {
                const x = (b * c) / a;
                document.getElementById('resultadoCalculo').innerHTML = "x = " + x;
            } else {
                document.getElementById('resultadoCalculo').innerHTML = "Preencha todos os valores conhecidos (a, b e c)";
            }
        }
        
        function calcularEscala() {
            const escala = parseFloat(document.getElementById('escala').value);
            const distancia = parseFloat(document.getElementById('distancia1').value);
            const tipo = document.getElementById('tipoCalculoEscala').value;
            
            if (tipo === "real") {
                const noMapa = distancia / escala;
                document.getElementById('resultadoEscala').innerHTML = "Distância no mapa: " + noMapa.toFixed(6) + " unidades";
            } else {
                const real = distancia * escala;
                document.getElementById('resultadoEscala').innerHTML = "Distância real: " + real + " unidades (" + (real/100000).toFixed(2) + " km)";
            }
        }
        
        function verificarAtividade1() {
            const resposta = parseFloat(document.getElementById('respostaAtividade1').value);
            const correta = 6; // 2/3 = x/9 → x=6
            verificarResposta(resposta, correta, 'resultadoAtividade1');
        }
        
        function verificarAtividade2() {
            const resposta = parseFloat(document.getElementById('respostaAtividade2').value);
            const correta = 20; // 8/10 = x/25 → x=20
            verificarResposta(resposta, correta, 'resultadoAtividade2');
        }
        
        function verificarAtividade3() {
            const resposta = parseFloat(document.getElementById('respostaAtividade3').value);
            const correta = 675; // 1/15 = 45/x → x=675
            verificarResposta(resposta, correta, 'resultadoAtividade3');
        }
        
        function verificarResposta(resposta, correta, elementoId) {
            if (isNaN(resposta)) {
                document.getElementById(elementoId).innerHTML = "Digite um número para verificar!";
                return;
            }
            
            if (Math.abs(resposta - correta) &lt; 0.001) {
                document.getElementById(elementoId).innerHTML = "Correto! Parabéns!";
            } else {
                document.getElementById(elementoId).innerHTML = "Ops! A resposta correta é " + correta + ". Tente novamente!";
            }
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;