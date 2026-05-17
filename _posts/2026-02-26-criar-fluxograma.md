---
layout: post
title: "Criar Fluxograma"
date: 2026-02-26
---

&lt;p&gt;&amp;nbsp;&lt;/p&gt;&lt;!DOCTYPE html&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Criador de Fluxogramas - Exportar&lt;/title&gt;
    &lt;script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"&gt;&lt;/script&gt;
    &lt;style&gt;
        :root { --primary: #3498db; --secondary: #2ecc71; }
        body { font-family: 'Segoe UI', sans-serif; margin: 20px; background-color: #f0f2f5; }
        .header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 15px; }
        .container { display: flex; gap: 20px; height: 75vh; }
        .editor { flex: 1; display: flex; flex-direction: column; }
        .preview { flex: 1.5; background: white; border: 2px solid #cbd5e0; border-radius: 12px; overflow: auto; padding: 20px; position: relative; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }
        textarea { flex: 1; padding: 15px; border-radius: 12px; border: 2px solid #cbd5e0; font-family: 'Fira Code', monospace; font-size: 14px; resize: none; outline: none; }
        textarea:focus { border-color: var(--primary); }
        button { background-color: var(--secondary); color: white; border: none; padding: 10px 20px; border-radius: 8px; cursor: pointer; font-weight: bold; transition: 0.3s; }
        button:hover { background-color: #27ae60; transform: translateY(-2px); }
        .hint { background: #ebf8ff; padding: 10px; border-left: 4px solid var(--primary); margin-bottom: 15px; font-size: 0.9em; }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;

    &lt;div class="header"&gt;
        &lt;h2&gt;Lógica e Fluxo: Resolvendo a Incógnita&lt;/h2&gt;
        &lt;button onclick="downloadSVG()"&gt;Baixar como Imagem (SVG)&lt;/button&gt;
    &lt;/div&gt;

    &lt;div class="hint"&gt;
        &lt;strong&gt;Dica para os alunos:&lt;/strong&gt; Use &lt;code&gt;graph TD&lt;/code&gt; para vertical ou &lt;code&gt;graph LR&lt;/code&gt; para horizontal. O texto entre &lt;code&gt;( )&lt;/code&gt; cria bordas arredondadas e &lt;code&gt;{ }&lt;/code&gt; cria decisões.
    &lt;/div&gt;

    &lt;div class="container"&gt;
        &lt;div class="editor"&gt;
            &lt;textarea id="input" oninput="updateDiagram()"&gt;
graph TD
    A[Equação: 2x + 4 = 10] --&gt; B[Subtrair 4 de ambos os lados]
    B --&gt; C[2x = 6]
    C --&gt; D[Dividir ambos os lados por 2]
    D --&gt; E{x = 3}
    E --&gt; F[Valor da incógnita encontrado!]
    
    style E fill:#f9f,stroke:#333,stroke-width:4px&lt;/textarea&gt;
        &lt;/div&gt;
        &lt;div class="preview" id="preview-container"&gt;
            &lt;div id="diagram" class="mermaid"&gt;&lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        mermaid.initialize({ startOnLoad: true, theme: 'default' });

        function updateDiagram() {
            const input = document.getElementById('input').value;
            const output = document.getElementById('diagram');
            
            output.removeAttribute('data-processed');
            output.innerHTML = input;
            mermaid.contentLoaded();
        }

        function downloadSVG() {
            const svgElement = document.querySelector('#preview-container svg');
            if (!svgElement) return;

            const svgData = new XMLSerializer().serializeToString(svgElement);
            const svgBlob = new Blob([svgData], {type: "image/svg+xml;charset=utf-8"});
            const svgUrl = URL.createObjectURL(svgBlob);
            
            const downloadLink = document.createElement("a");
            downloadLink.href = svgUrl;
            downloadLink.download = "meu-fluxograma.svg";
            document.body.appendChild(downloadLink);
            downloadLink.click();
            document.body.removeChild(downloadLink);
        }
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;