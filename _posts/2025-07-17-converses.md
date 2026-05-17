---
layout: post
title: "Conversões"
date: 2025-07-17
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;
&lt;div class="separator" style="clear: both; text-align: center;"&gt;&lt;iframe allowfullscreen="" class="BLOG_video_class" height="266" src="https://www.youtube.com/embed/RLFSyXT8GW0" width="320" youtube-src-id="RLFSyXT8GW0"&gt;&lt;/iframe&gt;&lt;/div&gt;
&lt;html lang="pt-BR"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;&lt;/meta&gt;
    &lt;meta content="width=device-width, initial-scale=1.0" name="viewport"&gt;&lt;/meta&gt;
    &lt;title&gt;Conversor Interativo: Fração, Decimal e Porcentagem&lt;/title&gt;
    &lt;script src="https://cdn.tailwindcss.com"&gt;&lt;/script&gt;
    &lt;script src="https://cdn.jsdelivr.net/npm/chart.js"&gt;&lt;/script&gt;
    &lt;link href="https://fonts.googleapis.com" rel="preconnect"&gt;&lt;/link&gt;
    &lt;link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect"&gt;&lt;/link&gt;
    &lt;link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&amp;amp;display=swap" rel="stylesheet"&gt;&lt;/link&gt;
    &lt;!-- Chosen Palette: Warm Neutrals with Teal Accent --&gt;
    &lt;!-- Application Structure Plan: A task-oriented interactive converter is the core of the application. The user can input a value in any of the three formats (fraction, decimal, percentage), and the other two are updated in real-time. This active learning approach is more effective than the passive slideshow format. The structure includes: 1) The main converter tool. 2) A dynamic explanation panel showing the calculation steps. 3) A dynamic doughnut chart for visual representation. 4) Buttons with pre-set examples from the source report. This structure was chosen to turn a static lesson into a hands-on, exploratory learning tool, maximizing user engagement and understanding. --&gt;
    &lt;!-- Visualization &amp; Content Choices: 
        - Fraction Input: Report Info -&gt; User-defined fraction -&gt; Goal: Input/Display -&gt; Viz: Two HTML number inputs -&gt; Interaction: Typing updates other fields -&gt; Justification: Clear and standard way to input a fraction. -&gt; Method: Vanilla JS.
        - Decimal/Percent Input: Report Info -&gt; User-defined decimal/percent -&gt; Goal: Input/Display -&gt; Viz: Single HTML number input -&gt; Interaction: Typing updates other fields -&gt; Justification: Standard input method. -&gt; Method: Vanilla JS.
        - Calculation Explanation: Report Info -&gt; How-to steps -&gt; Goal: Explain -&gt; Viz: Dynamic text block -&gt; Interaction: Text updates based on user input -&gt; Justification: Provides immediate, contextual feedback, reinforcing the learning process. -&gt; Method: Vanilla JS.
        - Visual Representation: Report Info -&gt; Visual aids (pizza slices) -&gt; Goal: Visualize proportion -&gt; Viz: Doughnut Chart -&gt; Interaction: Chart updates with new percentage -&gt; Justification: A dynamic chart is more engaging and universally represents 'part-of-a-whole'. -&gt; Library: Chart.js (Canvas).
    --&gt;
    &lt;!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. --&gt;
    &lt;style&gt;
        body {
            font-family: 'Inter', sans-serif;
        }
        .input-field {
            transition: all 0.2s ease-in-out;
        }
        .input-field:focus {
            box-shadow: 0 0 0 3px rgba(13, 148, 136, 0.3);
            border-color: #0d9488;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 320px;
            margin-left: auto;
            margin-right: auto;
            height: 320px;
            max-height: 80vw;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body class="bg-stone-50 text-stone-800"&gt;

    &lt;div class="container mx-auto max-w-5xl px-4 py-8 md:py-12"&gt;
        &lt;header class="text-center mb-8 md:mb-12"&gt;
            &lt;h1 class="text-3xl md:text-4xl font-bold text-teal-800"&gt;Conversor de Números Interativo&lt;/h1&gt;
            &lt;p class="mt-2 text-lg text-stone-600"&gt;Aprenda na prática a converter frações, decimais e porcentagens.&lt;/p&gt;
        &lt;/header&gt;

        &lt;main class="grid grid-cols-1 lg:grid-cols-2 gap-8 lg:gap-12 items-start"&gt;
            
            &lt;div class="bg-white p-6 md:p-8 rounded-2xl shadow-lg border border-stone-200"&gt;
                &lt;div class="space-y-6"&gt;
                    &lt;div&gt;
                        &lt;label class="block text-sm font-medium text-stone-700 mb-1" for="frac-num"&gt;Fração&lt;/label&gt;
                        &lt;div class="flex items-center space-x-2"&gt;
                            &lt;input class="input-field w-full p-3 bg-stone-100 border border-stone-300 rounded-lg text-center" id="frac-num" placeholder="Numerador" type="number" /&gt;
                            &lt;span class="text-stone-500 text-2xl font-light"&gt;/&lt;/span&gt;
                            &lt;input class="input-field w-full p-3 bg-stone-100 border border-stone-300 rounded-lg text-center" id="frac-den" placeholder="Denominador" type="number" /&gt;
                        &lt;/div&gt;
                    &lt;/div&gt;

                    &lt;div&gt;
                        &lt;label class="block text-sm font-medium text-stone-700 mb-1" for="decimal"&gt;Decimal&lt;/label&gt;
                        &lt;input class="input-field w-full p-3 bg-stone-100 border border-stone-300 rounded-lg" id="decimal" placeholder="Ex: 0.75" type="number" /&gt;
                    &lt;/div&gt;

                    &lt;div&gt;
                        &lt;label class="block text-sm font-medium text-stone-700 mb-1" for="percentage"&gt;Porcentagem&lt;/label&gt;
                        &lt;div class="relative"&gt;
                            &lt;input class="input-field w-full p-3 bg-stone-100 border border-stone-300 rounded-lg" id="percentage" placeholder="Ex: 75" type="number" /&gt;
                            &lt;span class="absolute inset-y-0 right-0 flex items-center pr-4 text-stone-500 text-lg"&gt;%&lt;/span&gt;
                        &lt;/div&gt;
                    &lt;/div&gt;
                &lt;/div&gt;

                &lt;div class="mt-8 text-center"&gt;
                    &lt;p class="text-sm text-stone-600 mb-3"&gt;Ou use um exemplo:&lt;/p&gt;
                    &lt;div class="flex justify-center gap-3"&gt;
                        &lt;button class="px-4 py-2 bg-teal-600 text-white rounded-lg hover:bg-teal-700 transition-colors" id="example1"&gt;Exemplo: 3/4&lt;/button&gt;
                        &lt;button class="px-4 py-2 bg-teal-600 text-white rounded-lg hover:bg-teal-700 transition-colors" id="example2"&gt;Exemplo: 1/2&lt;/button&gt;
                    &lt;/div&gt;
                &lt;/div&gt;
            &lt;/div&gt;

            &lt;div class="bg-teal-50 bg-opacity-50 p-6 md:p-8 rounded-2xl border border-teal-200 h-full"&gt;
                &lt;div class="flex flex-col items-center justify-center h-full space-y-4"&gt;
                     &lt;div class="chart-container"&gt;
                        &lt;canvas id="representationChart"&gt;&lt;/canvas&gt;
                    &lt;/div&gt;
                    &lt;div class="text-center text-teal-800" id="explanation"&gt;
                        &lt;p class="font-medium"&gt;Como a conversão é feita:&lt;/p&gt;
                        &lt;p class="text-stone-700 mt-1" id="explanation-text"&gt;Insira um valor em qualquer campo para começar.&lt;/p&gt;
                    &lt;/div&gt;
                &lt;/div&gt;
            &lt;/div&gt;

        &lt;/main&gt;
    &lt;/div&gt;

    &lt;script&gt;
        const fracNumEl = document.getElementById('frac-num');
        const fracDenEl = document.getElementById('frac-den');
        const decimalEl = document.getElementById('decimal');
        const percentageEl = document.getElementById('percentage');
        const explanationTextEl = document.getElementById('explanation-text');
        
        const example1Btn = document.getElementById('example1');
        const example2Btn = document.getElementById('example2');

        let currentSource = null;

        const gcd = (a, b) =&gt; b ? gcd(b, a % b) : a;

        const updateExplanation = (text) =&gt; {
            explanationTextEl.innerHTML = text;
        };
        
        const updateValues = ({ fraction, decimal, percentage, source }) =&gt; {
            if (source !== 'fraction') {
                fracNumEl.value = fraction.num;
                fracDenEl.value = fraction.den;
            }
            if (source !== 'decimal') {
                decimalEl.value = decimal;
            }
            if (source !== 'percentage') {
                percentageEl.value = percentage;
            }

            updateChart(percentage);
        };

        const clearAll = () =&gt; {
            fracNumEl.value = '';
            fracDenEl.value = '';
            decimalEl.value = '';
            percentageEl.value = '';
            currentSource = null;
            updateChart(0);
            updateExplanation('Insira um valor em qualquer campo para começar.');
        };

        fracNumEl.addEventListener('input', () =&gt; {
            currentSource = 'fraction';
            const num = parseFloat(fracNumEl.value);
            const den = parseFloat(fracDenEl.value);
            
            if (!isNaN(num) &amp;&amp; !isNaN(den) &amp;&amp; den !== 0) {
                const dec = num / den;
                const perc = dec * 100;
                updateValues({
                    fraction: { num, den },
                    decimal: dec.toPrecision(4),
                    percentage: perc.toPrecision(4),
                    source: 'fraction'
                });
                updateExplanation(`&lt;b&gt;Fração para Decimal:&lt;/b&gt; Dividimos ${num} por ${den} para obter &lt;b&gt;${dec.toPrecision(4)}&lt;/b&gt;.&lt;br&gt;&lt;b&gt;Decimal para Porcentagem:&lt;/b&gt; Multiplicamos por 100 para obter &lt;b&gt;${perc.toPrecision(4)}%&lt;/b&gt;.`);
            } else if (fracNumEl.value === '' &amp;&amp; fracDenEl.value === '') {
                clearAll();
            }
        });

        fracDenEl.addEventListener('input', () =&gt; fracNumEl.dispatchEvent(new Event('input')));

        decimalEl.addEventListener('input', () =&gt; {
            currentSource = 'decimal';
            const dec = parseFloat(decimalEl.value);

            if (!isNaN(dec)) {
                const perc = dec * 100;

                let len = dec.toString().split('.')[1] ? dec.toString().split('.')[1].length : 0;
                let denominator = Math.pow(10, len);
                let numerator = dec * denominator;
                const divisor = gcd(numerator, denominator);
                
                const frac = { num: numerator / divisor, den: denominator / divisor };

                updateValues({
                    fraction: frac,
                    decimal: dec,
                    percentage: perc.toPrecision(4),
                    source: 'decimal'
                });
                updateExplanation(`&lt;b&gt;Decimal para Porcentagem:&lt;/b&gt; Multiplicamos ${dec} por 100 para obter &lt;b&gt;${perc.toPrecision(4)}%&lt;/b&gt;.&lt;br&gt;&lt;b&gt;Decimal para Fração:&lt;/b&gt; Convertemos para &lt;b&gt;${frac.num}/${frac.den}&lt;/b&gt;.`);
            } else if (decimalEl.value === '') {
                clearAll();
            }
        });

        percentageEl.addEventListener('input', () =&gt; {
            currentSource = 'percentage';
            const perc = parseFloat(percentageEl.value);

            if (!isNaN(perc)) {
                const dec = perc / 100;

                let denominator = 100;
                let numerator = perc;
                const divisor = gcd(numerator, denominator);
                
                const frac = { num: numerator / divisor, den: denominator / divisor };

                updateValues({
                    fraction: frac,
                    decimal: dec.toPrecision(4),
                    percentage: perc,
                    source: 'percentage'
                });
                updateExplanation(`&lt;b&gt;Porcentagem para Decimal:&lt;/b&gt; Dividimos ${perc} por 100 para obter &lt;b&gt;${dec.toPrecision(4)}&lt;/b&gt;.&lt;br&gt;&lt;b&gt;Decimal para Fração:&lt;/b&gt; Convertemos para &lt;b&gt;${frac.num}/${frac.den}&lt;/b&gt;.`);
            } else if (percentageEl.value === '') {
                clearAll();
            }
        });
        
        example1Btn.addEventListener('click', () =&gt; {
            fracNumEl.value = 3;
            fracDenEl.value = 4;
            fracNumEl.dispatchEvent(new Event('input'));
        });
        
        example2Btn.addEventListener('click', () =&gt; {
            fracNumEl.value = 1;
            fracDenEl.value = 2;
            fracNumEl.dispatchEvent(new Event('input'));
        });

        const ctx = document.getElementById('representationChart').getContext('2d');
        const representationChart = new Chart(ctx, {
            type: 'doughnut',
            data: {
                labels: ['Valor', 'Restante'],
                datasets: [{
                    data: [0, 100],
                    backgroundColor: [
                        '#0d9488', 
                        '#f5f5f4'
                    ],
                    borderColor: [
                        '#0f766e',
                        '#e7e5e4'
                    ],
                    borderWidth: 2
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                cutout: '70%',
                plugins: {
                    legend: {
                        display: false
                    },
                    tooltip: {
                        enabled: false
                    }
                }
            }
        });

        const updateChart = (percentage) =&gt; {
            const p = Math.max(0, Math.min(100, parseFloat(percentage) || 0));
            representationChart.data.datasets[0].data[0] = p;
            representationChart.data.datasets[0].data[1] = 100 - p;
            representationChart.update();
        };

        clearAll();

    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
&lt;script&gt;var pfHeaderImgUrl = '';var pfHeaderTagline = '';var pfdisableClickToDel = 0;var pfHideImages = 0;var pfImageDisplayStyle = 'right';var pfDisablePDF = 0;var pfDisableEmail = 0;var pfDisablePrint = 0;var pfCustomCSS = '';var pfBtVersion='1';(function(){var js, pf;pf = document.createElement('script');pf.type = 'text/javascript';if('https:' == document.location.protocol){js='https://pf-cdn.printfriendly.com/ssl/main.js'}else{js='http://cdn.printfriendly.com/printfriendly.js'}pf.src=js;document.getElementsByTagName('head')[0].appendChild(pf)})();&lt;/script&gt;&lt;a class="printfriendly" href="http://www.printfriendly.com" onclick="window.print();return false;" style="color: #6d9f00; text-decoration: none;" title="Printer Friendly and PDF"&gt;&lt;img alt="Print Friendly and PDF" src="http://cdn.printfriendly.com/button-print-grnw20.png" style="-webkit-box-shadow: none; border: none; box-shadow: none;" /&gt;&lt;/a&gt;