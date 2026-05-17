---
layout: post
title: "Post Sem Titulo"
date: 2025-08-09
---

&lt;!DOCTYPE html&gt;
&lt;html lang="pt-br"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Vídeo Interativo - Aprendizado&lt;/title&gt;
    &lt;style&gt;
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 20px;
        }

        .container {
            max-width: 800px;
            width: 100%;
        }

        .video-container {
            position: relative;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            overflow: hidden;
            background: #000;
        }

        video {
            width: 100%;
            height: auto;
            display: block;
            background: #000;
        }

        video:focus {
            outline: none;
        }

        #opcoes {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(255, 255, 255, 0.98);
            padding: 35px;
            border-radius: 20px;
            text-align: center;
            width: 90%;
            max-width: 450px;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
            border: 2px solid rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
        }

        #opcoes h3 {
            margin: 0 0 20px 0;
            color: #333;
            font-size: 1.5em;
            font-weight: 600;
            line-height: 1.4;
        }

        #opcoes p {
            color: #666;
            margin-bottom: 25px;
            font-size: 1.1em;
        }

        .botoes-container {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }

        #opcoes button {
            margin: 5px;
            padding: 15px 30px;
            font-size: 1.1em;
            cursor: pointer;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 180px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        #opcaoA {
            background: linear-gradient(135deg, #ff6b6b, #ff4757);
            color: white;
        }

        #opcaoA:hover {
            background: linear-gradient(135deg, #ff4757, #ff6b6b);
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(255, 71, 87, 0.3);
        }

        #opcaoB {
            background: linear-gradient(135deg, #51cf66, #37b24d);
            color: white;
        }

        #opcaoB:hover {
            background: linear-gradient(135deg, #37b24d, #51cf66);
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(55, 178, 77, 0.3);
        }

        .oculto {
            display: none !important;
        }

        .controles-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 20px;
            color: white;
            font-size: 0.9em;
        }

        .tempo-info {
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 15px;
            border-radius: 50px;
            backdrop-filter: blur(5px);
        }

        .mensagem-flutuante {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 15px 25px;
            border-radius: 50px;
            color: white;
            font-weight: 600;
            animation: slideIn 0.3s ease;
            z-index: 1000;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .mensagem-sucesso {
            background: linear-gradient(135deg, #51cf66, #37b24d);
        }

        .mensagem-erro {
            background: linear-gradient(135deg, #ff6b6b, #ff4757);
        }

        @keyframes slideIn {
            from {
                transform: translateX(100%);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        .instrucao {
            text-align: center;
            margin-top: 15px;
            color: rgba(255, 255, 255, 0.9);
            font-size: 1em;
        }

        .instrucao i {
            font-style: normal;
            background: rgba(255, 255, 255, 0.2);
            padding: 5px 10px;
            border-radius: 20px;
            margin: 0 5px;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;div class="container"&gt;
    &lt;div class="video-container"&gt;
        &lt;!-- Vídeo de exemplo (Big Buck Bunny - vídeo livre para uso) --&gt;
        &lt;video controls id="meuvideo" width="640" poster="https://images.unsplash.com/photo-1536240474400-95dad987e71b?w=800&amp;auto=format&amp;fit=crop"&gt;
            &lt;source src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4" type="video/mp4"&gt;
            &lt;source src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4" type="video/webm"&gt;
            Seu navegador não suporta a tag de vídeo. Atualize seu navegador para assistir.
        &lt;/video&gt;
        
        &lt;div class="oculto" id="opcoes"&gt;
            &lt;h3&gt;⏸️ Vídeo Pausado&lt;/h3&gt;
            &lt;p&gt;Qual é a capital do Brasil?&lt;/p&gt;
            &lt;div class="botoes-container"&gt;
                &lt;button id="opcaoA"&gt;🚫 Rio de Janeiro&lt;/button&gt;
                &lt;button id="opcaoB"&gt;✅ Brasília&lt;/button&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;div class="controles-info"&gt;
        &lt;span class="tempo-info" id="tempoAtual"&gt;0:00 / 0:00&lt;/span&gt;
        &lt;span class="tempo-info"&gt;⏰ Interação em: 10 segundos&lt;/span&gt;
    &lt;/div&gt;
    
    &lt;div class="instrucao"&gt;
        &lt;i&gt;🎯&lt;/i&gt; O vídeo pausará automaticamente aos 10 segundos para uma pergunta!
    &lt;/div&gt;
&lt;/div&gt;

&lt;script&gt;
    // Aguardar o DOM carregar completamente
    document.addEventListener('DOMContentLoaded', function() {
        const video = document.getElementById('meuvideo');
        const opcoes = document.getElementById('opcoes');
        const opcaoA = document.getElementById('opcaoA');
        const opcaoB = document.getElementById('opcaoB');
        const tempoAtual = document.getElementById('tempoAtual');
        
        // Variáveis de controle
        const tempoDeInteracao = 10;
        let interacaoJaOcorreu = false;
        let timeoutMensagem;

        // Função para formatar tempo (segundos para MM:SS)
        function formatarTempo(segundos) {
            const mins = Math.floor(segundos / 60);
            const secs = Math.floor(segundos % 60);
            return `${mins}:${secs &lt; 10 ? '0' : ''}${secs}`;
        }

        // Atualizar display do tempo
        function atualizarTempo() {
            if (video.duration) {
                tempoAtual.textContent = `${formatarTempo(video.currentTime)} / ${formatarTempo(video.duration)}`;
            }
        }

        // Mostrar mensagem temporária
        function mostrarMensagem(texto, tipo) {
            // Limpar timeout anterior
            if (timeoutMensagem) {
                clearTimeout(timeoutMensagem);
            }

            // Remover mensagem existente
            const mensagemExistente = document.querySelector('.mensagem-flutuante');
            if (mensagemExistente) {
                mensagemExistente.remove();
            }

            // Criar nova mensagem
            const mensagem = document.createElement('div');
            mensagem.className = `mensagem-flutuante mensagem-${tipo}`;
            mensagem.textContent = texto;
            document.body.appendChild(mensagem);

            // Remover após 3 segundos
            timeoutMensagem = setTimeout(() =&gt; {
                mensagem.remove();
            }, 3000);
        }

        // Verificar se o vídeo está pronto
        video.addEventListener('loadedmetadata', function() {
            console.log('Vídeo carregado. Duração:', video.duration);
            atualizarTempo();
        });

        // Evento de tempo do vídeo
        video.addEventListener('timeupdate', function() {
            atualizarTempo();
            
            // Verificar se atingiu o tempo de interação e ainda não ocorreu
            if (!interacaoJaOcorreu &amp;&amp; Math.floor(video.currentTime) === tempoDeInteracao) {
                video.pause();
                opcoes.classList.remove('oculto');
                interacaoJaOcorreu = true;
                mostrarMensagem('⏸️ Vídeo pausado para pergunta!', 'info');
            }
        });

        // Ação ao clicar na opção incorreta
        opcaoA.addEventListener('click', function() {
            mostrarMensagem('❌ Resposta incorreta! Tente novamente.', 'erro');
            
            // Reiniciar o vídeo e a interação
            video.currentTime = 0;
            interacaoJaOcorreu = false;
            opcoes.classList.add('oculto');
            video.play().catch(e =&gt; console.log('Erro ao reproduzir:', e));
        });

        // Ação ao clicar na opção correta
        opcaoB.addEventListener('click', function() {
            mostrarMensagem('✅ Resposta correta! Parabéns! 🎉', 'sucesso');
            opcoes.classList.add('oculto');
            
            // Continuar o vídeo
            video.play().catch(e =&gt; console.log('Erro ao reproduzir:', e));
        });

        // Evento quando o vídeo termina
        video.addEventListener('ended', function() {
            mostrarMensagem('🎬 Vídeo finalizado! Obrigado por assistir!', 'sucesso');
        });

        // Evento de erro no vídeo
        video.addEventListener('error', function(e) {
            console.error('Erro no vídeo:', e);
            mostrarMensagem('⚠️ Erro ao carregar o vídeo. Verifique sua conexão.', 'erro');
        });

        // Opção de pular a interação (se o usuário passar do tempo)
        video.addEventListener('seeking', function() {
            if (video.currentTime &gt; tempoDeInteracao &amp;&amp; !interacaoJaOcorreu) {
                interacaoJaOcorreu = true;
            }
        });

        console.log('Página carregada! O vídeo pausará em', tempoDeInteracao, 'segundos.');
    });
&lt;/script&gt;

&lt;!-- Nota: O vídeo usado é um sample livre (Big Buck Bunny) --&gt;
&lt;/body&gt;
&lt;/html&gt;