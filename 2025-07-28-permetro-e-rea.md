---
layout: post
title: "Perímetro e área"
date: 2025-07-28
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Perímetro e Área - Aprendendo Geometria&lt;/title&gt;
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
        
        h1, h2 {
            color: #2c3e50;
            text-align: center;
        }
        
        .conceito {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            margin: 20px 0;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .calculadora {
            background-color: #e8f4f8;
            border-radius: 10px;
            padding: 20px;
            margin: 30px 0;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .formula {
            font-family: 'Courier New', monospace;
            background-color: #f0f0f0;
            padding: 5px 10px;
            border-radius: 5px;
            display: inline-block;
        }
        
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
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
            color: #27ae60;
            font-size: 18px;
            margin-top: 10px;
        }
        
        .figura {
            width: 150px;
            height: 150px;
            margin: 20px auto;
            background-color: #bdc3c7;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }
        
        .circulo {
            border-radius: 50%;
        }
        
        .retangulo {
            width: 200px;
        }
        
        .triangulo {
            width: 0;
            height: 0;
            border-left: 75px solid transparent;
            border-right: 75px solid transparent;
            border-bottom: 150px solid #bdc3c7;
            background-color: transparent;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        
        .exemplo {
            flex-basis: 30%;
            min-width: 250px;
            margin-bottom: 20px;
        }
        
        @media (max-width: 768px) {
            .exemplo {
                flex-basis: 100%;
            }
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Perímetro e Área&lt;/h1&gt;
    
    &lt;div class="conceito"&gt;
        &lt;h2&gt;O que é Perímetro?&lt;/h2&gt;
        &lt;p&gt;O &lt;strong&gt;perímetro&lt;/strong&gt; é a medida do contorno de uma figura geométrica, ou seja, a soma de todos os seus lados.&lt;/p&gt;
        &lt;p&gt;Podemos pensar no perímetro como o "caminho" que percorremos ao redor de uma figura.&lt;/p&gt;
    &lt;/div&gt;
    
    &lt;div class="conceito"&gt;
        &lt;h2&gt;O que é Área?&lt;/h2&gt;
        &lt;p&gt;A &lt;strong&gt;área&lt;/strong&gt; é a medida da superfície de uma figura geométrica, ou seja, o espaço que ela ocupa.&lt;/p&gt;
        &lt;p&gt;Podemos pensar na área como a "quantidade de tinta" que precisaríamos para pintar uma figura.&lt;/p&gt;
    &lt;/div&gt;
    
    &lt;div class="calculadora"&gt;
        &lt;h2&gt;Calculadora de Perímetro e Área&lt;/h2&gt;
        
        &lt;label for="forma"&gt;Selecione a forma geométrica:&lt;/label&gt;
        &lt;select id="forma" onchange="mudarForma()"&gt;
            &lt;option value="quadrado"&gt;Quadrado&lt;/option&gt;
            &lt;option value="retangulo"&gt;Retângulo&lt;/option&gt;
            &lt;option value="triangulo"&gt;Triângulo&lt;/option&gt;
            &lt;option value="circulo"&gt;Círculo&lt;/option&gt;
        &lt;/select&gt;
        
        &lt;div id="inputs"&gt;
            &lt;!-- Os inputs serão gerados dinamicamente aqui --&gt;
        &lt;/div&gt;
        
        &lt;button onclick="calcular()"&gt;Calcular&lt;/button&gt;
        
        &lt;div id="resultado" class="resultado"&gt;&lt;/div&gt;
    &lt;/div&gt;
    
    &lt;h2&gt;Exemplos de Cálculo&lt;/h2&gt;
    
    &lt;div class="container"&gt;
        &lt;div class="exemplo"&gt;
            &lt;h3&gt;Quadrado&lt;/h3&gt;
            &lt;div class="figura"&gt;□&lt;/div&gt;
            &lt;p&gt;&lt;span class="formula"&gt;Perímetro = 4 × lado&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;&lt;span class="formula"&gt;Área = lado × lado&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;Exemplo: lado = 5cm&lt;/p&gt;
            &lt;p&gt;Perímetro = 4 × 5 = 20cm&lt;/p&gt;
            &lt;p&gt;Área = 5 × 5 = 25cm²&lt;/p&gt;
        &lt;/div&gt;
        
        &lt;div class="exemplo"&gt;
            &lt;h3&gt;Retângulo&lt;/h3&gt;
            &lt;div class="figura retangulo"&gt;▭&lt;/div&gt;
            &lt;p&gt;&lt;span class="formula"&gt;Perímetro = 2 × (base + altura)&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;&lt;span class="formula"&gt;Área = base × altura&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;Exemplo: base = 6cm, altura = 4cm&lt;/p&gt;
            &lt;p&gt;Perímetro = 2 × (6 + 4) = 20cm&lt;/p&gt;
            &lt;p&gt;Área = 6 × 4 = 24cm²&lt;/p&gt;
        &lt;/div&gt;
        
        &lt;div class="exemplo"&gt;
            &lt;h3&gt;Triângulo&lt;/h3&gt;
            &lt;div class="figura triangulo"&gt;&lt;/div&gt;
            &lt;p&gt;&lt;span class="formula"&gt;Perímetro = lado1 + lado2 + lado3&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;&lt;span class="formula"&gt;Área = (base × altura) / 2&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;Exemplo: lados = 5cm, 6cm, 7cm, base = 6cm, altura = 4cm&lt;/p&gt;
            &lt;p&gt;Perímetro = 5 + 6 + 7 = 18cm&lt;/p&gt;
            &lt;p&gt;Área = (6 × 4) / 2 = 12cm²&lt;/p&gt;
        &lt;/div&gt;
        
        &lt;div class="exemplo"&gt;
            &lt;h3&gt;Círculo&lt;/h3&gt;
            &lt;div class="figura circulo"&gt;○&lt;/div&gt;
            &lt;p&gt;&lt;span class="formula"&gt;Perímetro (circunferência) = 2 × π × raio&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;&lt;span class="formula"&gt;Área = π × raio²&lt;/span&gt;&lt;/p&gt;
            &lt;p&gt;Exemplo: raio = 3cm (π ≈ 3.14)&lt;/p&gt;
            &lt;p&gt;Perímetro ≈ 2 × 3.14 × 3 ≈ 18.84cm&lt;/p&gt;
            &lt;p&gt;Área ≈ 3.14 × 9 ≈ 28.26cm²&lt;/p&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;script&gt;
        function mudarForma() {
            const forma = document.getElementById('forma').value;
            const inputsDiv = document.getElementById('inputs');
            let html = '';
            
            switch(forma) {
                case 'quadrado':
                    html = `
                        &lt;label for="lado"&gt;Lado (cm):&lt;/label&gt;
                        &lt;input type="number" id="lado" step="0.01" min="0"&gt;
                    `;
                    break;
                case 'retangulo':
                    html = `
                        &lt;label for="base"&gt;Base (cm):&lt;/label&gt;
                        &lt;input type="number" id="base" step="0.01" min="0"&gt;&lt;br&gt;
                        &lt;label for="altura"&gt;Altura (cm):&lt;/label&gt;
                        &lt;input type="number" id="altura" step="0.01" min="0"&gt;
                    `;
                    break;
                case 'triangulo':
                    html = `
                        &lt;label for="lado1"&gt;Lado 1 (cm):&lt;/label&gt;
                        &lt;input type="number" id="lado1" step="0.01" min="0"&gt;&lt;br&gt;
                        &lt;label for="lado2"&gt;Lado 2 (cm):&lt;/label&gt;
                        &lt;input type="number" id="lado2" step="0.01" min="0"&gt;&lt;br&gt;
                        &lt;label for="lado3"&gt;Lado 3 (cm):&lt;/label&gt;
                        &lt;input type="number" id="lado3" step="0.01" min="0"&gt;&lt;br&gt;
                        &lt;label for="baseTri"&gt;Base (cm):&lt;/label&gt;
                        &lt;input type="number" id="baseTri" step="0.01" min="0"&gt;&lt;br&gt;
                        &lt;label for="alturaTri"&gt;Altura (cm):&lt;/label&gt;
                        &lt;input type="number" id="alturaTri" step="0.01" min="0"&gt;
                    `;
                    break;
                case 'circulo':
                    html = `
                        &lt;label for="raio"&gt;Raio (cm):&lt;/label&gt;
                        &lt;input type="number" id="raio" step="0.01" min="0"&gt;
                    `;
                    break;
            }
            
            inputsDiv.innerHTML = html;
        }
        
        function calcular() {
            const forma = document.getElementById('forma').value;
            const resultadoDiv = document.getElementById('resultado');
            let perimetro, area;
            
            switch(forma) {
                case 'quadrado':
                    const lado = parseFloat(document.getElementById('lado').value);
                    if (isNaN(lado) || lado &lt;= 0) {
                        resultadoDiv.innerHTML = "Por favor, insira um valor válido para o lado.";
                        return;
                    }
                    perimetro = 4 * lado;
                    area = lado * lado;
                    resultadoDiv.innerHTML = `Perímetro: ${perimetro.toFixed(2)} cm&lt;br&gt;Área: ${area.toFixed(2)} cm²`;
                    break;
                    
                case 'retangulo':
                    const base = parseFloat(document.getElementById('base').value);
                    const altura = parseFloat(document.getElementById('altura').value);
                    if (isNaN(base) || base &lt;= 0 || isNaN(altura) || altura &lt;= 0) {
                        resultadoDiv.innerHTML = "Por favor, insira valores válidos para base e altura.";
                        return;
                    }
                    perimetro = 2 * (base + altura);
                    area = base * altura;
                    resultadoDiv.innerHTML = `Perímetro: ${perimetro.toFixed(2)} cm&lt;br&gt;Área: ${area.toFixed(2)} cm²`;
                    break;
                    
                case 'triangulo':
                    const lado1 = parseFloat(document.getElementById('lado1').value);
                    const lado2 = parseFloat(document.getElementById('lado2').value);
                    const lado3 = parseFloat(document.getElementById('lado3').value);
                    const baseTri = parseFloat(document.getElementById('baseTri').value);
                    const alturaTri = parseFloat(document.getElementById('alturaTri').value);
                    
                    if (isNaN(lado1) || lado1 &lt;= 0 || isNaN(lado2) || lado2 &lt;= 0 || 
                        isNaN(lado3) || lado3 &lt;= 0 || isNaN(baseTri) || baseTri &lt;= 0 || 
                        isNaN(alturaTri) || alturaTri &lt;= 0) {
                        resultadoDiv.innerHTML = "Por favor, insira valores válidos para todos os campos.";
                        return;
                    }
                    
                    perimetro = lado1 + lado2 + lado3;
                    area = (baseTri * alturaTri) / 2;
                    resultadoDiv.innerHTML = `Perímetro: ${perimetro.toFixed(2)} cm&lt;br&gt;Área: ${area.toFixed(2)} cm²`;
                    break;
                    
                case 'circulo':
                    const raio = parseFloat(document.getElementById('raio').value);
                    if (isNaN(raio) || raio &lt;= 0) {
                        resultadoDiv.innerHTML = "Por favor, insira um valor válido para o raio.";
                        return;
                    }
                    perimetro = 2 * Math.PI * raio;
                    area = Math.PI * raio * raio;
                    resultadoDiv.innerHTML = `Circunferência: ${perimetro.toFixed(2)} cm&lt;br&gt;Área: ${area.toFixed(2)} cm²`;
                    break;
            }
        }
        
        // Inicializa os inputs para o quadrado ao carregar a página
        window.onload = mudarForma;
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;