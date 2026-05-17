---
layout: post
title: "Post Sem Titulo"
date: 2025-08-01
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Resolução de Inequações do 1º Grau&lt;/title&gt;
    &lt;style&gt;
        body {
            font-family: Arial, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        h1 {
            color: #2c3e50;
            text-align: center;
        }
        .problem-container {
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background-color: #2980b9;
        }
        input {
            padding: 8px;
            margin: 5px 0;
            width: 100px;
        }
        .solution {
            margin-top: 15px;
            padding: 10px;
            background-color: #e8f4fc;
            border-left: 4px solid #3498db;
            display: none;
        }
        .input-group {
            margin: 10px 0;
        }
        label {
            display: inline-block;
            width: 200px;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Resolução de Inequações do 1º Grau&lt;/h1&gt;

    &lt;!-- Problema 1: Economia Pessoal --&gt;
    &lt;div class="problem-container"&gt;
        &lt;h2&gt;1. Economia Pessoal&lt;/h2&gt;
        &lt;p&gt;João recebe um salário mensal de R$ 2.500,00 e gasta R$ 800,00 com aluguel e R$ 600,00 com outras despesas fixas. Quanto ele deseja economizar por mês?&lt;/p&gt;
        
        &lt;div class="input-group"&gt;
            &lt;label for="economia"&gt;Economia desejada (R$):&lt;/label&gt;
            &lt;input type="number" id="economia" value="500" min="0"&gt;
        &lt;/div&gt;
        
        &lt;button onclick="calcularLazer()"&gt;Calcular Máximo para Lazer&lt;/button&gt;
        
        &lt;div id="solution1" class="solution"&gt;
            &lt;h3&gt;Resolução:&lt;/h3&gt;
            &lt;p&gt;Salário: R$ 2500&lt;/p&gt;
            &lt;p&gt;Gastos fixos: R$ 800 (aluguel) + R$ 600 (outros) = R$ 1400&lt;/p&gt;
            &lt;p&gt;Economia desejada: ≥ R$ &lt;span id="valor-economia"&gt;500&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;Inequação: 2500 - 1400 - x ≥ &lt;span id="inequacao-economia"&gt;500&lt;/span&gt; → 1100 - x ≥ &lt;span id="inequacao-economia2"&gt;500&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;Resolvendo: -x ≥ &lt;span id="passo-intermediario"&gt;-600&lt;/span&gt; → x ≤ &lt;span id="resultado-final"&gt;600&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;&lt;strong&gt;Resposta: João pode gastar no máximo R$ &lt;span id="max-lazer"&gt;600&lt;/span&gt;,00 com lazer.&lt;/strong&gt;&lt;/p&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;!-- Problema 2: Produção Industrial --&gt;
    &lt;div class="problem-container"&gt;
        &lt;h2&gt;2. Produção Industrial&lt;/h2&gt;
        &lt;p&gt;Uma fábrica produz camisetas. Calcule quantas unidades precisam ser vendidas para atingir um lucro desejado:&lt;/p&gt;
        
        &lt;div class="input-group"&gt;
            &lt;label for="custo-camiseta"&gt;Custo por camiseta (R$):&lt;/label&gt;
            &lt;input type="number" id="custo-camiseta" value="12" min="0" step="0.01"&gt;
        &lt;/div&gt;
        
        &lt;div class="input-group"&gt;
            &lt;label for="preco-venda"&gt;Preço de venda (R$):&lt;/label&gt;
            &lt;input type="number" id="preco-venda" value="20" min="0" step="0.01"&gt;
        &lt;/div&gt;
        
        &lt;div class="input-group"&gt;
            &lt;label for="custo-fixo"&gt;Custo fixo mensal (R$):&lt;/label&gt;
            &lt;input type="number" id="custo-fixo" value="5000" min="0"&gt;
        &lt;/div&gt;
        
        &lt;div class="input-group"&gt;
            &lt;label for="lucro-desejado"&gt;Lucro desejado (R$):&lt;/label&gt;
            &lt;input type="number" id="lucro-desejado" value="3000" min="0"&gt;
        &lt;/div&gt;
        
        &lt;button onclick="calcularVendas()"&gt;Calcular Vendas Necessárias&lt;/button&gt;
        
        &lt;div id="solution2" class="solution"&gt;
            &lt;h3&gt;Resolução:&lt;/h3&gt;
            &lt;p&gt;Custo total: &lt;span id="custo-variavel"&gt;12&lt;/span&gt;x + &lt;span id="custo-fixo-res"&gt;5000&lt;/span&gt; (onde x = número de camisetas)&lt;/p&gt;
            &lt;p&gt;Receita total: &lt;span id="preco-venda-res"&gt;20&lt;/span&gt;x&lt;/p&gt;
            &lt;p&gt;Lucro: Receita - Custo &gt; &lt;span id="lucro-desejado-res"&gt;3000&lt;/span&gt; → &lt;span id="inequacao-completa"&gt;20x - (12x + 5000) &gt; 3000&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;Simplificando: &lt;span id="inequacao-simplificada"&gt;8x - 5000 &gt; 3000&lt;/span&gt; → &lt;span id="passo-final"&gt;8x &gt; 8000&lt;/span&gt; → x &gt; &lt;span id="resultado-camisetas"&gt;1000&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;&lt;strong&gt;Resposta: Devem ser vendidas mais de &lt;span id="vendas-necessarias"&gt;1000&lt;/span&gt; camisetas.&lt;/strong&gt;&lt;/p&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;!-- Problema 3: Transporte Escolar (Agora Interativo) --&gt;
    &lt;div class="problem-container"&gt;
        &lt;h2&gt;3. Transporte Escolar&lt;/h2&gt;
        &lt;p&gt;Um ônibus escolar tem capacidade para &lt;input type="number" id="capacidade-onibus" value="48" min="1" style="width: 50px;"&gt; passageiros. Se já estão garantidos &lt;input type="number" id="alunos-garantidos" value="30" min="0" style="width: 50px;"&gt; alunos, quantos lugares adicionais podem ser vendidos (a R$ &lt;input type="number" id="preco-lugar" value="10" min="0" style="width: 50px;"&gt; cada) para que a receita total não ultrapasse R$ &lt;input type="number" id="receita-maxima" value="500" min="0" style="width: 70px;"&gt;?&lt;/p&gt;
        
        &lt;button onclick="calcularLugares()"&gt;Calcular Lugares Disponíveis&lt;/button&gt;
        
        &lt;div id="solution3" class="solution"&gt;
            &lt;h3&gt;Resolução:&lt;/h3&gt;
            &lt;p&gt;Lugares disponíveis: &lt;span id="capacidade-res"&gt;48&lt;/span&gt; - &lt;span id="alunos-res"&gt;30&lt;/span&gt; = &lt;span id="lugares-disponiveis"&gt;18&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;Preço por lugar: R$ &lt;span id="preco-lugar-res"&gt;10&lt;/span&gt;,00&lt;/p&gt;
            &lt;p&gt;Inequação: &lt;span id="inequacao-transporte"&gt;10y ≤ 500&lt;/span&gt; → y ≤ &lt;span id="limite-financeiro"&gt;50&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;Limite físico do ônibus: y ≤ &lt;span id="limite-fisico"&gt;18&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;&lt;strong&gt;Resposta: Podem ser vendidos até &lt;span id="lugares-vendidos"&gt;18&lt;/span&gt; lugares adicionais.&lt;/strong&gt;&lt;/p&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        // Função para calcular o valor máximo para lazer (Problema 1)
        function calcularLazer() {
            const economia = parseFloat(document.getElementById("economia").value);
            const salario = 2500;
            const gastosFixos = 800 + 600;
            const maxLazer = salario - gastosFixos - economia;

            // Atualiza os valores na resolução
            document.getElementById("valor-economia").textContent = economia.toFixed(2);
            document.getElementById("inequacao-economia").textContent = economia.toFixed(2);
            document.getElementById("inequacao-economia2").textContent = economia.toFixed(2);
            document.getElementById("passo-intermediario").textContent = (economia - 1100).toFixed(2);
            document.getElementById("resultado-final").textContent = maxLazer.toFixed(2);
            document.getElementById("max-lazer").textContent = maxLazer.toFixed(2);

            // Mostra a solução
            document.getElementById("solution1").style.display = "block";
        }

        // Função para calcular vendas necessárias (Problema 2)
        function calcularVendas() {
            const custoCamiseta = parseFloat(document.getElementById("custo-camiseta").value);
            const precoVenda = parseFloat(document.getElementById("preco-venda").value);
            const custoFixo = parseFloat(document.getElementById("custo-fixo").value);
            const lucroDesejado = parseFloat(document.getElementById("lucro-desejado").value);

            // Cálculo da inequação
            const margemPorUnidade = precoVenda - custoCamiseta;
            const vendasNecessarias = Math.ceil((lucroDesejado + custoFixo) / margemPorUnidade);

            // Atualiza os valores na resolução
            document.getElementById("custo-variavel").textContent = custoCamiseta.toFixed(2);
            document.getElementById("custo-fixo-res").textContent = custoFixo.toFixed(2);
            document.getElementById("preco-venda-res").textContent = precoVenda.toFixed(2);
            document.getElementById("lucro-desejado-res").textContent = lucroDesejado.toFixed(2);
            
            const inequacaoCompleta = `${precoVenda}x - (${custoCamiseta}x + ${custoFixo}) &gt; ${lucroDesejado}`;
            document.getElementById("inequacao-completa").textContent = inequacaoCompleta;
            
            const inequacaoSimplificada = `${margemPorUnidade}x - ${custoFixo} &gt; ${lucroDesejado}`;
            document.getElementById("inequacao-simplificada").textContent = inequacaoSimplificada;
            
            const passoFinal = `${margemPorUnidade}x &gt; ${lucroDesejado + custoFixo}`;
            document.getElementById("passo-final").textContent = passoFinal;
            
            document.getElementById("resultado-camisetas").textContent = vendasNecessarias;
            document.getElementById("vendas-necessarias").textContent = vendasNecessarias;

            // Mostra a solução
            document.getElementById("solution2").style.display = "block";
        }

        // Função para calcular lugares disponíveis (Problema 3 interativo)
        function calcularLugares() {
            const capacidade = parseInt(document.getElementById("capacidade-onibus").value);
            const alunosGarantidos = parseInt(document.getElementById("alunos-garantidos").value);
            const precoLugar = parseFloat(document.getElementById("preco-lugar").value);
            const receitaMaxima = parseFloat(document.getElementById("receita-maxima").value);

            // Cálculos
            const lugaresDisponiveis = capacidade - alunosGarantidos;
            const limiteFinanceiro = Math.floor(receitaMaxima / precoLugar);
            const lugaresVendidos = Math.min(lugaresDisponiveis, limiteFinanceiro);

            // Atualiza os valores na resolução
            document.getElementById("capacidade-res").textContent = capacidade;
            document.getElementById("alunos-res").textContent = alunosGarantidos;
            document.getElementById("lugares-disponiveis").textContent = lugaresDisponiveis;
            document.getElementById("preco-lugar-res").textContent = precoLugar.toFixed(2);
            document.getElementById("inequacao-transporte").textContent = `${precoLugar}y ≤ ${receitaMaxima}`;
            document.getElementById("limite-financeiro").textContent = limiteFinanceiro;
            document.getElementById("limite-fisico").textContent = lugaresDisponiveis;
            document.getElementById("lugares-vendidos").textContent = lugaresVendidos;

            // Mostra a solução
            document.getElementById("solution3").style.display = "block";
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;