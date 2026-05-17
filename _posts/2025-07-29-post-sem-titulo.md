---
layout: post
title: "Post Sem Titulo"
date: 2025-07-29
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;&lt;/meta&gt;
    &lt;meta content="width=device-width, initial-scale=1.0" name="viewport"&gt;&lt;/meta&gt;
    &lt;title&gt;Explorando Unidades de Medida&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background-color: #f0f8ff;
            margin: 0;
            padding: 0;
            color: #333;
        }
        
        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 1em;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        nav {
            display: flex;
            justify-content: center;
            background-color: #333;
            padding: 0.5em;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            padding: 0.5em 1em;
            margin: 0 0.5em;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        
        nav a:hover {
            background-color: #4CAF50;
        }
        
        .container {
            max-width: 900px;
            margin: 2em auto;
            padding: 0 1em;
        }
        
        .card {
            background-color: white;
            border-radius: 10px;
            padding: 1.5em;
            margin-bottom: 1.5em;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .interactive-tool {
            border: 2px dashed #4CAF50;
            padding: 1em;
            margin: 1em 0;
            border-radius: 10px;
        }
        
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 0.5em 1em;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1em;
            margin: 0.5em 0;
        }
        
        button:hover {
            background-color: #45a049;
        }
        
        input, select {
            padding: 0.5em;
            margin: 0.5em 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        
        footer {
            text-align: center;
            padding: 1em;
            background-color: #333;
            color: white;
            margin-top: 2em;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;header&gt;
        &lt;h1&gt;Explorando Unidades de Medida&lt;/h1&gt;
        &lt;p&gt;Aprenda sobre medidas de forma divertida e interativa!&lt;/p&gt;
    &lt;/header&gt;
    
    &lt;nav&gt;
        &lt;a href="#comprimento"&gt;Comprimento&lt;/a&gt;
        &lt;a href="#massa"&gt;Massa&lt;/a&gt;
        &lt;a href="#capacidade"&gt;Capacidade&lt;/a&gt;
        &lt;a href="#tempo"&gt;Tempo&lt;/a&gt;
        &lt;a href="#jogos"&gt;Jogos&lt;/a&gt;
    &lt;/nav&gt;
    
    &lt;div class="container"&gt;
        &lt;section class="card" id="comprimento"&gt;
            &lt;h2&gt;Medidas de Comprimento&lt;/h2&gt;
            &lt;p&gt;As medidas de comprimento nos ajudam a saber o tamanho das coisas. As principais unidades são:&lt;/p&gt;
            &lt;ul&gt;
                &lt;li&gt;Milímetro (mm)&lt;/li&gt;
                &lt;li&gt;Centímetro (cm)&lt;/li&gt;
                &lt;li&gt;Metro (m)&lt;/li&gt;
                &lt;li&gt;Quilômetro (km)&lt;/li&gt;
            &lt;/ul&gt;
            
            &lt;div class="interactive-tool"&gt;
                &lt;h3&gt;Conversor de Comprimento&lt;/h3&gt;
                &lt;input id="comprimento-valor" placeholder="Digite o valor" type="number" /&gt;
                &lt;select id="comprimento-de"&gt;
                    &lt;option value="mm"&gt;Milímetro (mm)&lt;/option&gt;
                    &lt;option selected="" value="cm"&gt;Centímetro (cm)&lt;/option&gt;
                    &lt;option value="m"&gt;Metro (m)&lt;/option&gt;
                    &lt;option value="km"&gt;Quilômetro (km)&lt;/option&gt;
                &lt;/select&gt;
                &lt;span&gt;para&lt;/span&gt;
                &lt;select id="comprimento-para"&gt;
                    &lt;option value="mm"&gt;Milímetro (mm)&lt;/option&gt;
                    &lt;option value="cm"&gt;Centímetro (cm)&lt;/option&gt;
                    &lt;option selected="" value="m"&gt;Metro (m)&lt;/option&gt;
                    &lt;option value="km"&gt;Quilômetro (km)&lt;/option&gt;
                &lt;/select&gt;
                &lt;button onclick="converterComprimento()"&gt;Converter&lt;/button&gt;
                &lt;p id="comprimento-resultado"&gt;&lt;/p&gt;
            &lt;/div&gt;
            
            &lt;div class="interactive-tool"&gt;
                &lt;h3&gt;Atividade: Estime o Comprimento&lt;/h3&gt;
                &lt;p&gt;Quanto mede um lápis comum?&lt;/p&gt;
                &lt;input id="estimativa-lapis" placeholder="Sua estimativa em cm" type="number" /&gt;
                &lt;button onclick="verificarEstimativa('lapis', 18)"&gt;Verificar&lt;/button&gt;
                &lt;p id="resultado-lapis"&gt;&lt;/p&gt;
            &lt;/div&gt;
        &lt;/section&gt;
        
        &lt;section class="card" id="massa"&gt;
            &lt;h2&gt;Medidas de Massa&lt;/h2&gt;
            &lt;p&gt;As medidas de massa nos ajudam a saber o peso das coisas. As principais unidades são:&lt;/p&gt;
            &lt;ul&gt;
                &lt;li&gt;Grama (g)&lt;/li&gt;
                &lt;li&gt;Quilograma (kg)&lt;/li&gt;
                &lt;li&gt;Tonelada (t)&lt;/li&gt;
            &lt;/ul&gt;
            
            &lt;div class="interactive-tool"&gt;
                &lt;h3&gt;Conversor de Massa&lt;/h3&gt;
                &lt;input id="massa-valor" placeholder="Digite o valor" type="number" /&gt;
                &lt;select id="massa-de"&gt;
                    &lt;option selected="" value="g"&gt;Grama (g)&lt;/option&gt;
                    &lt;option value="kg"&gt;Quilograma (kg)&lt;/option&gt;
                    &lt;option value="t"&gt;Tonelada (t)&lt;/option&gt;
                &lt;/select&gt;
                &lt;span&gt;para&lt;/span&gt;
                &lt;select id="massa-para"&gt;
                    &lt;option value="g"&gt;Grama (g)&lt;/option&gt;
                    &lt;option selected="" value="kg"&gt;Quilograma (kg)&lt;/option&gt;
                    &lt;option value="t"&gt;Tonelada (t)&lt;/option&gt;
                &lt;/select&gt;
                &lt;button onclick="converterMassa()"&gt;Converter&lt;/button&gt;
                &lt;p id="massa-resultado"&gt;&lt;/p&gt;
            &lt;/div&gt;
        &lt;/section&gt;
        
        &lt;section class="card" id="capacidade"&gt;
            &lt;h2&gt;Medidas de Capacidade&lt;/h2&gt;
            &lt;p&gt;As medidas de capacidade nos ajudam a saber o volume de líquidos. As principais unidades são:&lt;/p&gt;
            &lt;ul&gt;
                &lt;li&gt;Mililitro (mL)&lt;/li&gt;
                &lt;li&gt;Litro (L)&lt;/li&gt;
            &lt;/ul&gt;
            
            &lt;div class="interactive-tool"&gt;
                &lt;h3&gt;Conversor de Capacidade&lt;/h3&gt;
                &lt;input id="capacidade-valor" placeholder="Digite o valor" type="number" /&gt;
                &lt;select id="capacidade-de"&gt;
                    &lt;option selected="" value="ml"&gt;Mililitro (mL)&lt;/option&gt;
                    &lt;option value="l"&gt;Litro (L)&lt;/option&gt;
                &lt;/select&gt;
                &lt;span&gt;para&lt;/span&gt;
                &lt;select id="capacidade-para"&gt;
                    &lt;option value="ml"&gt;Mililitro (mL)&lt;/option&gt;
                    &lt;option selected="" value="l"&gt;Litro (L)&lt;/option&gt;
                &lt;/select&gt;
                &lt;button onclick="converterCapacidade()"&gt;Converter&lt;/button&gt;
                &lt;p id="capacidade-resultado"&gt;&lt;/p&gt;
            &lt;/div&gt;
            
            &lt;div class="interactive-tool"&gt;
                &lt;h3&gt;Desafio: Quantos copos?&lt;/h3&gt;
                &lt;p&gt;Um copo comum tem cerca de 200mL. Quantos copos são necessários para encher uma garrafa de 1,5L?&lt;/p&gt;
                &lt;input id="resposta-copos" placeholder="Sua resposta" type="number" /&gt;
                &lt;button onclick="verificarCopos()"&gt;Verificar&lt;/button&gt;
                &lt;p id="resultado-copos"&gt;&lt;/p&gt;
            &lt;/div&gt;
        &lt;/section&gt;
        
        &lt;section class="card" id="tempo"&gt;
            &lt;h2&gt;Medidas de Tempo&lt;/h2&gt;
            &lt;p&gt;As medidas de tempo nos ajudam a organizar nosso dia. As principais unidades são:&lt;/p&gt;
            &lt;ul&gt;
                &lt;li&gt;Segundo (s)&lt;/li&gt;
                &lt;li&gt;Minuto (min)&lt;/li&gt;
                &lt;li&gt;Hora (h)&lt;/li&gt;
                &lt;li&gt;Dia&lt;/li&gt;
            &lt;/ul&gt;
            
            &lt;div class="interactive-tool"&gt;
                &lt;h3&gt;Conversor de Tempo&lt;/h3&gt;
                &lt;input id="tempo-valor" placeholder="Digite o valor" type="number" /&gt;
                &lt;select id="tempo-de"&gt;
                    &lt;option value="s"&gt;Segundo (s)&lt;/option&gt;
                    &lt;option selected="" value="min"&gt;Minuto (min)&lt;/option&gt;
                    &lt;option value="h"&gt;Hora (h)&lt;/option&gt;
                    &lt;option value="d"&gt;Dia&lt;/option&gt;
                &lt;/select&gt;
                &lt;span&gt;para&lt;/span&gt;
                &lt;select id="tempo-para"&gt;
                    &lt;option value="s"&gt;Segundo (s)&lt;/option&gt;
                    &lt;option value="min"&gt;Minuto (min)&lt;/option&gt;
                    &lt;option selected="" value="h"&gt;Hora (h)&lt;/option&gt;
                    &lt;option value="d"&gt;Dia&lt;/option&gt;
                &lt;/select&gt;
                &lt;button onclick="converterTempo()"&gt;Converter&lt;/button&gt;
                &lt;p id="tempo-resultado"&gt;&lt;/p&gt;
            &lt;/div&gt;
        &lt;/section&gt;
        
        &lt;section class="card" id="jogos"&gt;
            &lt;h2&gt;Jogos e Desafios&lt;/h2&gt;
            
            &lt;div class="interactive-tool"&gt;
                &lt;h3&gt;Jogo da Memória das Unidades&lt;/h3&gt;
                &lt;p&gt;Encontre os pares de unidades equivalentes!&lt;/p&gt;
                &lt;button onclick="iniciarJogoMemoria()"&gt;Iniciar Jogo&lt;/button&gt;
                &lt;div id="jogo-memoria" style="display: none; margin-top: 1em;"&gt;
                    &lt;!-- As cartas do jogo serão inseridas aqui pelo JavaScript --&gt;
                &lt;/div&gt;
            &lt;/div&gt;
            
            &lt;div class="interactive-tool"&gt;
                &lt;h3&gt;Quiz das Medidas&lt;/h3&gt;
                &lt;p&gt;Teste seus conhecimentos com este quiz divertido!&lt;/p&gt;
                &lt;button onclick="iniciarQuiz()"&gt;Começar Quiz&lt;/button&gt;
                &lt;div id="quiz-container" style="display: none; margin-top: 1em;"&gt;
                    &lt;p id="pergunta-quiz"&gt;&lt;/p&gt;
                    &lt;div id="opcoes-quiz"&gt;&lt;/div&gt;
                    &lt;p id="resultado-quiz"&gt;&lt;/p&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/section&gt;
    &lt;/div&gt;
    
        &lt;script&gt;
        // Funções para os conversores
        function converterComprimento() {
            const valor = parseFloat(document.getElementById('comprimento-valor').value);
            const de = document.getElementById('comprimento-de').value;
            const para = document.getElementById('comprimento-para').value;
            
            if (isNaN(valor)) {
                alert("Por favor, digite um número válido!");
                return;
            }
            
            // Converter para metros primeiro (unidade base)
            let metros;
            switch(de) {
                case 'mm': metros = valor / 1000; break;
                case 'cm': metros = valor / 100; break;
                case 'm': metros = valor; break;
                case 'km': metros = valor * 1000; break;
            }
            
            // Converter para unidade desejada
            let resultado;
            switch(para) {
                case 'mm': resultado = metros * 1000; break;
                case 'cm': resultado = metros * 100; break;
                case 'm': resultado = metros; break;
                case 'km': resultado = metros / 1000; break;
            }
            
            document.getElementById('comprimento-resultado').innerHTML = 
                `${valor} ${de} = ${resultado.toFixed(4)} ${para}`;
        }
        
        function converterMassa() {
            const valor = parseFloat(document.getElementById('massa-valor').value);
            const de = document.getElementById('massa-de').value;
            const para = document.getElementById('massa-para').value;
            
            if (isNaN(valor)) {
                alert("Por favor, digite um número válido!");
                return;
            }
            
            // Converter para gramas primeiro (unidade base)
            let gramas;
            switch(de) {
                case 'g': gramas = valor; break;
                case 'kg': gramas = valor * 1000; break;
                case 't': gramas = valor * 1000000; break;
            }
            
            // Converter para unidade desejada
            let resultado;
            switch(para) {
                case 'g': resultado = gramas; break;
                case 'kg': resultado = gramas / 1000; break;
                case 't': resultado = gramas / 1000000; break;
            }
            
            document.getElementById('massa-resultado').innerHTML = 
                `${valor} ${de} = ${resultado.toFixed(4)} ${para}`;
        }
        
        function converterCapacidade() {
            const valor = parseFloat(document.getElementById('capacidade-valor').value);
            const de = document.getElementById('capacidade-de').value;
            const para = document.getElementById('capacidade-para').value;
            
            if (isNaN(valor)) {
                alert("Por favor, digite um número válido!");
                return;
            }
            
            // Converter para mililitros primeiro (unidade base)
            let ml;
            switch(de) {
                case 'ml': ml = valor; break;
                case 'l': ml = valor * 1000; break;
            }
            
            // Converter para unidade desejada
            let resultado;
            switch(para) {
                case 'ml': resultado = ml; break;
                case 'l': resultado = ml / 1000; break;
            }
            
            document.getElementById('capacidade-resultado').innerHTML = 
                `${valor} ${de} = ${resultado.toFixed(4)} ${para}`;
        }
        
        function converterTempo() {
            const valor = parseFloat(document.getElementById('tempo-valor').value);
            const de = document.getElementById('tempo-de').value;
            const para = document.getElementById('tempo-para').value;
            
            if (isNaN(valor)) {
                alert("Por favor, digite um número válido!");
                return;
            }
            
            // Converter para segundos primeiro (unidade base)
            let segundos;
            switch(de) {
                case 's': segundos = valor; break;
                case 'min': segundos = valor * 60; break;
                case 'h': segundos = valor * 3600; break;
                case 'd': segundos = valor * 86400; break;
            }
            
            // Converter para unidade desejada
            let resultado;
            switch(para) {
                case 's': resultado = segundos; break;
                case 'min': resultado = segundos / 60; break;
                case 'h': resultado = segundos / 3600; break;
                case 'd': resultado = segundos / 86400; break;
            }
            
            document.getElementById('tempo-resultado').innerHTML = 
                `${valor} ${de} = ${resultado.toFixed(4)} ${para}`;
        }
        
        // Funções para as atividades
        function verificarEstimativa(objeto, valorReal) {
            const estimativa = parseFloat(document.getElementById(`estimativa-${objeto}`).value);
            
            if (isNaN(estimativa)) {
                alert("Por favor, digite um número válido!");
                return;
            }
            
            const diferenca = Math.abs(estimativa - valorReal);
            const porcentagemErro = (diferenca / valorReal) * 100;
            
            let mensagem;
            if (porcentagemErro &lt; 10) {
                mensagem = `Parabéns! Sua estimativa de ${estimativa}cm está muito próxima do valor real (${valorReal}cm).`;
            } else if (porcentagemErro &lt; 30) {
                mensagem = `Boa tentativa! O valor real é ${valorReal}cm.`;
            } else {
                mensagem = `Continue praticando! Um lápis comum mede cerca de ${valorReal}cm.`;
            }
            
            document.getElementById(`resultado-${objeto}`).innerHTML = mensagem;
        }
        
        function verificarCopos() {
            const resposta = parseFloat(document.getElementById('resposta-copos').value);
            const respostaCorreta = 7.5; // 1500mL / 200mL
            
            if (isNaN(resposta)) {
                alert("Por favor, digite um número válido!");
                return;
            }
            
            if (Math.abs(resposta - respostaCorreta) &lt; 0.5) {
                document.getElementById('resultado-copos').innerHTML = 
                    "Correto! São necessários 7,5 copos de 200mL para encher uma garrafa de 1,5L.";
            } else {
                document.getElementById('resultado-copos').innerHTML = 
                    "Quase lá! Lembre-se: 1,5L = 1500mL. Divida 1500 por 200 para encontrar a resposta.";
            }
        }
        
        // Funções para os jogos
        function iniciarJogoMemoria() {
            const container = document.getElementById('jogo-memoria');
            container.style.display = 'block';
            container.innerHTML = '';
            
            const pares = [
                { unidade: '1m', equivalente: '100cm' },
                { unidade: '1km', equivalente: '1000m' },
                { unidade: '1kg', equivalente: '1000g' },
                { unidade: '1L', equivalente: '1000mL' },
                { unidade: '1h', equivalente: '60min' },
                { unidade: '1min', equivalente: '60s' }
            ];
            
            // Duplicar e embaralhar as cartas
            let cartas = [];
            pares.forEach(par =&gt; {
                cartas.push({ texto: par.unidade, tipo: 'unidade', par: par.equivalente });
                cartas.push({ texto: par.equivalente, tipo: 'equivalente', par: par.unidade });
            });
            
            cartas = embaralhar(cartas);
            
            // Criar as cartas na tela
            cartas.forEach((carta, index) =&gt; {
                const cartaElement = document.createElement('div');
                cartaElement.className = 'carta';
                cartaElement.dataset.index = index;
                cartaElement.dataset.texto = carta.texto;
                cartaElement.dataset.par = carta.par;
                cartaElement.style.display = 'inline-block';
                cartaElement.style.width = '80px';
                cartaElement.style.height = '60px';
                cartaElement.style.margin = '5px';
                cartaElement.style.backgroundColor = '#4CAF50';
                cartaElement.style.color = 'white';
                cartaElement.style.textAlign = 'center';
                cartaElement.style.lineHeight = '60px';
                cartaElement.style.cursor = 'pointer';
                cartaElement.style.borderRadius = '5px';
                cartaElement.innerHTML = '?';
                
                cartaElement.addEventListener('click', virarCarta);
                container.appendChild(cartaElement);
            });
        }
        
        let cartaVirada = null;
        let paresEncontrados = 0;
        
        function virarCarta() {
            if (this.innerHTML !== '?') return; // Carta já virada
            
            this.innerHTML = this.dataset.texto;
            this.style.backgroundColor = 'white';
            this.style.color = '#333';
            
            if (!cartaVirada) {
                cartaVirada = this;
            } else {
                if (cartaVirada.dataset.texto === this.dataset.par) {
                    // Par encontrado!
                    cartaVirada.style.backgroundColor = '#45a049';
                    cartaVirada.style.color = 'white';
                    this.style.backgroundColor = '#45a049';
                    this.style.color = 'white';
                    
                    cartaVirada.removeEventListener('click', virarCarta);
                    this.removeEventListener('click', virarCarta);
                    
                    paresEncontrados++;
                    if (paresEncontrados === 6) {
                        setTimeout(() =&gt; {
                            alert("Parabéns! Você encontrou todos os pares!");
                        }, 500);
                    }
                } else {
                    // Par errado, virar de volta após um tempo
                    const primeiraCarta = cartaVirada;
                    const segundaCarta = this;
                    
                    setTimeout(() =&gt; {
                        primeiraCarta.innerHTML = '?';
                        primeiraCarta.style.backgroundColor = '#4CAF50';
                        primeiraCarta.style.color = 'white';
                        
                        segundaCarta.innerHTML = '?';
                        segundaCarta.style.backgroundColor = '#4CAF50';
                        segundaCarta.style.color = 'white';
                    }, 1000);
                }
                
                cartaVirada = null;
            }
        }
        
        function embaralhar(array) {
            for (let i = array.length - 1; i &gt; 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [array[i], array[j]] = [array[j], array[i]];
            }
            return array;
        }
        
        function iniciarQuiz() {
            const container = document.getElementById('quiz-container');
            container.style.display = 'block';
            
            const perguntas = [
                {
                    pergunta: "Quantos centímetros tem um metro?",
                    opcoes: ["10cm", "100cm", "1000cm", "0,1cm"],
                    resposta: 1
                },
                {
                    pergunta: "Qual unidade é maior?",
                    opcoes: ["Milímetro", "Centímetro", "Metro", "Quilômetro"],
                    resposta: 3
                },
                {
                    pergunta: "Quantos gramas tem um quilograma?",
                    opcoes: ["10g", "100g", "500g", "1000g"],
                    resposta: 3
                },
                {
                    pergunta: "Quantos mililitros tem um litro?",
                    opcoes: ["10mL", "100mL", "500mL", "1000mL"],
                    resposta: 3
                },
                {
                    pergunta: "Quantos minutos tem uma hora?",
                    opcoes: ["30min", "60min", "100min", "360min"],
                    resposta: 1
                }
            ];
            
            let perguntaAtual = 0;
            let pontuacao = 0;
            
            function mostrarPergunta() {
                if (perguntaAtual &gt;= perguntas.length) {
                    document.getElementById('pergunta-quiz').innerHTML = 
                        `Quiz concluído! Sua pontuação: ${pontuacao} de ${perguntas.length}`;
                    document.getElementById('opcoes-quiz').innerHTML = '';
                    return;
                }
                
                const pergunta = perguntas[perguntaAtual];
                document.getElementById('pergunta-quiz').innerHTML = pergunta.pergunta;
                
                const opcoesDiv = document.getElementById('opcoes-quiz');
                opcoesDiv.innerHTML = '';
                
                pergunta.opcoes.forEach((opcao, index) =&gt; {
                    const botao = document.createElement('button');
                    botao.innerHTML = opcao;
                    botao.style.display = 'block';
                    botao.style.margin = '5px 0';
                    botao.onclick = () =&gt; verificarResposta(index);
                    opcoesDiv.appendChild(botao);
                });
            }
            
            function verificarResposta(resposta) {
                const pergunta = perguntas[perguntaAtual];
                if (resposta === pergunta.resposta) {
                    pontuacao++;
                    document.getElementById('resultado-quiz').innerHTML = "Correto!";
                } else {
                    document.getElementById('resultado-quiz').innerHTML = 
                        `Incorreto. A resposta correta é: ${pergunta.opcoes[pergunta.resposta]}`;
                }
                
                perguntaAtual++;
                setTimeout(() =&gt; {
                    document.getElementById('resultado-quiz').innerHTML = '';
                    mostrarPergunta();
                }, 1500);
            }
            
            mostrarPergunta();
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;