<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Relacione os Itens 🧩</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }
        body {
            background: #1a1a2e;
            color: white;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }
        h1 {
            margin-bottom: 10px;
            color: #00f5d4;
        }
        .painel {
            display: flex;
            gap: 30px;
            margin: 20px 0;
            width: 90%;
            max-width: 700px;
        }
        .coluna {
            flex: 1;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        .item {
            background: #16213e;
            padding: 14px;
            border-radius: 10px;
            text-align: center;
            cursor: pointer;
            transition: 0.3s;
            border: 2px solid transparent;
        }
        .item:hover {
            background: #0f3460;
            transform: scale(1.03);
        }
        .item.selecionado {
            border-color: #00f5d4;
            background: #0f3460;
        }
        .item.correto {
            background: #00b489;
            border-color: #00f5d4;
            cursor: default;
            pointer-events: none;
        }
        .item.errado {
            animation: tremer 0.3s;
        }
        @keyframes tremer {
            0%,100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }
        .status {
            display: flex;
            gap: 20px;
            margin: 10px 0;
            font-size: 18px;
        }
        button {
            background: #e94560;
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 8px;
            font-size: 16px;
            cursor: pointer;
            margin-top: 15px;
            transition: 0.2s;
        }
        button:hover {
            background: #ff6b81;
        }
        .mensagem {
            margin-top: 15px;
            font-size: 18px;
            font-weight: bold;
            height: 30px;
        }
        .vitoria {
            color: #00f5d4;
            font-size: 22px;
            margin-top: 10px;
        }
    </style>
</head>
<body>

    <h1>🧩 Relacione os Pares!</h1>
    <p>Escolha um item da esquerda e depois seu par correspondente da direita</p>

    <div class="status">
        <div>✅ Acertos: <span id="acertos">0</span></div>
        <div>❌ Erros: <span id="erros">0</span></div>
    </div>

    <div class="painel">
        <div class="coluna" id="coluna-esq"></div>
        <div class="coluna" id="coluna-dir"></div>
    </div>

    <div class="mensagem" id="mensagem"></div>
    <button onclick="reiniciar()">🔄 Reiniciar Jogo</button>

<script>
    // 🔧 Lista de pares — edite aqui seus itens!
    const pares = [
        { esq: "🌞 Sol", dir: "Dia" },
        { esq: "🌙 Lua", dir: "Noite" },
        { esq: "🌊 Mar", dir: "Água" },
        { esq: "🔥 Fogo", dir: "Calor" },
        { esq: "🌲 Árvore", dir: "Planta" },
        { esq: "❄️ Gelo", dir: "Frio" }
    ];

    let itensEsq = [];
    let itensDir = [];
    let selecionadoEsq = null;
    let selecionadoDir = null;
    let acertos = 0;
    let erros = 0;

    function embaralhar(array) {
        return [...array].sort(() => Math.random() - 0.5);
    }

    function carregarJogo() {
        acertos = 0;
        erros = 0;
        selecionadoEsq = null;
        selecionadoDir = null;
        atualizarStatus();
        document.getElementById('mensagem').textContent = '';

        itensEsq = embaralhar(pares);
        itensDir = embaralhar(pares);

        const colEsq = document.getElementById('coluna-esq');
        const colDir = document.getElementById('coluna-dir');
        colEsq.innerHTML = '';
        colDir.innerHTML = '';

        itensEsq.forEach((par, i) => {
            const div = document.createElement('div');
            div.className = 'item';
            div.textContent = par.esq;
            div.dataset.indiceReal = pares.indexOf(par);
            div.onclick = () => escolherEsq(div);
            colEsq.appendChild(div);
        });

        itensDir.forEach((par, i) => {
            const div = document.createElement('div');
            div.className = 'item';
            div.textContent = par.dir;
            div.dataset.indiceReal = pares.indexOf(par);
            div.onclick = () => escolherDir(div);
            colDir.appendChild(div);
        });
    }

    function escolherEsq(el) {
        if (el.classList.contains('correto')) return;
        document.querySelectorAll('#coluna-esq .item').forEach(i => i.classList.remove('selecionado'));
        el.classList.add('selecionado');
        selecionadoEsq = el;
        verificarPar();
    }

    function escolherDir(el) {
        if (el.classList.contains('correto')) return;
        document.querySelectorAll('#coluna-dir .item').forEach(i => i.classList.remove('selecionado'));
        el.classList.add('selecionado');
        selecionadoDir = el;
        verificarPar();
    }

    function verificarPar() {
        if (!selecionadoEsq || !selecionadoDir) return;

        const iEsq = selecionadoEsq.dataset.indiceReal;
        const iDir = selecionadoDir.dataset.indiceReal;

        if (iEsq === iDir) {
            selecionadoEsq.classList.add('correto');
            selecionadoDir.classList.add('correto');
            acertos++;
            document.getElementById('mensagem').textContent = '✅ Par correto!';
            document.getElementById('mensagem').style.color = '#00f5d4';
        } else {
            selecionadoEsq.classList.add('errado');
            selecionadoDir.classList.add('errado');
            erros++;
            document.getElementById('mensagem').textContent = '❌ Tente novamente!';
            document.getElementById('mensagem').style.color = '#e94560';
            setTimeout(() => {
                selecionadoEsq.classList.remove('errado');
                selecionadoDir.classList.remove('errado');
            }, 300);
        }

        selecionadoEsq.classList.remove('selecionado');
        selecionadoDir.classList.remove('selecionado');
        selecionadoEsq = null;
        selecionadoDir = null;
        atualizarStatus();

        setTimeout(() => document.getElementById('mensagem').textContent = '', 1500);

        if (acertos === pares.length) {
            document.getElementById('mensagem').innerHTML = '<span class="vitoria">🎉 Parabéns! Você acertou tudo!</span>';
        }
    }

    function atualizarStatus() {
        document.getElementById('acertos').textContent = acertos;
        document.getElementById('erros').textContent = erros;
    }

    function reiniciar() {
        carregarJogo();
    }

    // Inicia o jogo ao carregar a página
    window.onload = carregarJogo;
</script>
</body>
</html>
