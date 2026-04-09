<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>CONFERÊNCIA DO EVANGELHO – Conteúdos</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --bg-body: #f0dfb8;
      --bg-card: #f7e6c2;
      --bg-dark: #3c2b1d;
      --accent: #c28a3b;
      --accent-soft: #e2b868;
      --text-main: #2d1b10;
      --text-muted: #6b4a2a;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    body {
      background: radial-gradient(circle at top, #fcefd3 0, var(--bg-body) 40%, #e3c798 100%);
      color: var(--text-main);
      line-height: 1.6;
      min-height: 100vh;
    }

    .texture {
      position: fixed;
      inset: 0;
      pointer-events: none;
      opacity: 0.25;
      mix-blend-mode: multiply;
      background-image:
        radial-gradient(circle at 10% 20%, rgba(0,0,0,0.08) 0, transparent 55%),
        radial-gradient(circle at 80% 10%, rgba(0,0,0,0.1) 0, transparent 55%),
        radial-gradient(circle at 50% 80%, rgba(0,0,0,0.06) 0, transparent 55%);
      z-index: -1;
    }

    header {
      text-align: center;
      padding: 28px 16px 12px;
    }

    header .sub-top {
      font-size: 0.9rem;
      color: var(--text-muted);
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }

    header h1 {
      font-family: "Georgia", "Times New Roman", serif;
      font-size: 1.9rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      margin-top: 10px;
      margin-bottom: 4px;
    }

    header h1 span {
      display: block;
      font-size: 2.1rem;
    }

    header .tagline {
      font-style: italic;
      font-size: 0.95rem;
      color: var(--text-muted);
      max-width: 520px;
      margin: 8px auto 0;
    }

    main {
      max-width: 960px;
      margin: 0 auto;
      padding: 8px 16px 32px;
    }

    .card {
      background: linear-gradient(135deg, #f9ebc7, var(--bg-card));
      border-radius: 18px;
      border: 1px solid rgba(76, 51, 32, 0.35);
      box-shadow:
        0 18px 40px rgba(62, 41, 25, 0.32),
        0 0 0 1px rgba(255, 255, 255, 0.4);
      padding: 18px 16px 22px;
      backdrop-filter: blur(4px);
    }

    .aviso {
      font-size: 0.9rem;
      color: var(--text-muted);
      background: rgba(255, 255, 255, 0.6);
      border-radius: 12px;
      padding: 10px 12px;
      border: 1px solid rgba(179, 135, 71, 0.5);
      margin-bottom: 18px;
    }

    .aviso strong {
      font-weight: 600;
      color: var(--text-main);
    }

    .tabs {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 14px;
    }

    .tab {
      padding: 7px 14px;
      border-radius: 999px;
      border: 1px solid rgba(124, 78, 35, 0.4);
      background: rgba(120, 77, 40, 0.09);
      color: var(--text-main);
      font-size: 0.9rem;
      cursor: pointer;
      transition: all 0.15s ease;
      backdrop-filter: blur(3px);
    }

    .tab span {
      font-size: 0.78rem;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      color: var(--text-muted);
    }

    .tab strong {
      display: block;
      font-size: 0.95rem;
    }

    .tab.active {
      background: radial-gradient(circle at top, #f9e0a3, #c28a3b);
      color: #2a1a0d;
      border-color: rgba(107, 70, 29, 0.7);
      box-shadow: 0 0 0 1px rgba(255,255,255,0.5), 0 3px 8px rgba(97, 61, 22, 0.45);
      transform: translateY(-1px);
    }

    .conteudo-dia {
      display: none;
      background: rgba(255, 255, 255, 0.72);
      border-radius: 16px;
      border: 1px solid rgba(170, 120, 60, 0.6);
      padding: 16px 14px 18px;
      box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.8);
    }

    .conteudo-dia.active {
      display: block;
    }

    .conteudo-dia h2 {
      font-family: "Georgia", "Times New Roman", serif;
      font-size: 1.1rem;
      margin-bottom: 4px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--text-main);
    }

    .conteudo-dia .tema {
      font-size: 0.9rem;
      font-style: italic;
      color: var(--text-muted);
      margin-bottom: 10px;
    }

    .linha {
      height: 1px;
      background: linear-gradient(to right, transparent, rgba(120,81,38,0.5), transparent);
      margin: 10px 0 8px;
    }

    .blocos {
      display: grid;
      grid-template-columns: 1fr;
      gap: 14px;
    }

    .bloco {
      background: #fbf2dd;
      border-radius: 12px;
      padding: 10px 11px 11px;
      border: 1px solid rgba(162, 115, 60, 0.55);
      box-shadow: 0 1px 4px rgba(100, 65, 32, 0.25);
    }

    .bloco-titulo {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 6px;
    }

    .icone-circulo {
      width: 30px;
      height: 30px;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 20%, #fff7dd, #c28a3b);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #2b1608;
      font-size: 0.9rem;
      box-shadow: 0 2px 6px rgba(96, 58, 26, 0.6);
    }

    .bloco-titulo h3 {
      font-size: 0.95rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--text-main);
    }

    .descricao {
      font-size: 0.88rem;
      color: var(--text-muted);
      margin-bottom: 6px;
    }

    ul.arquivos {
      list-style: none;
      margin-top: 2px;
    }

    ul.arquivos li {
      display: flex;
      align-items: center;
      gap: 6px;
      padding: 5px 0;
      border-bottom: 1px dashed rgba(179, 135, 71, 0.4);
      font-size: 0.9rem;
    }

    ul.arquivos li:last-child {
      border-bottom: none;
    }

    .icone-arquivo {
      width: 22px;
      height: 22px;
      border-radius: 6px;
      background: #3f2a1b;
      color: #fef3c7;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.78rem;
      flex-shrink: 0;
    }

    .icone-arquivo.audio {
      background: #7a3a2a;
    }

    .arquivo-nome {
      flex: 1;
    }

    .arquivo-tipo {
      font-size: 0.78rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--text-muted);
    }

    a {
      color: #8a5521;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    footer {
      text-align: center;
      font-size: 0.78rem;
      color: var(--text-muted);
      margin-top: 18px;
      padding-bottom: 10px;
    }

    @media (min-width: 720px) {
      header {
        padding-top: 34px;
      }

      header h1 {
        font-size: 2.2rem;
      }

      header h1 span {
        font-size: 2.6rem;
      }

      main {
        padding: 12px 16px 40px;
      }

      .card {
        padding: 22px 22px 26px;
      }

      .blocos {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .conteudo-dia {
        padding: 18px 16px 20px;
      }
    }
  </style>
</head>
<body>
  <div class="texture"></div>

  <header>
    <div class="sub-top">09 a 12 de Abril</div>
    <h1>
      CONFERÊNCIA DO
      <span>EVANGELHO</span>
    </h1>
    <p class="tagline">
      Confrontando as crenças erradas que distorcem a fé e desviam o foco de Cristo na igreja atual.
    </p>
  </header>

  <main>
    <div class="card">
      <div class="aviso">
        <strong>Bem-vindo!</strong> Esta página reúne os materiais de apoio da
        <strong>Conferência do Evangelho</strong>. Use durante as ministrações
        e depois do evento para revisar os conteúdos.
      </div>

      <!-- Abas dos 4 dias -->
      <div class="tabs">
        <button class="tab active" data-target="dia1">
          <span>Dia 1</span>
          <strong>Fundamentos do Evangelho</strong>
        </button>
        <button class="tab" data-target="dia2">
          <span>Dia 2</span>
          <strong>Graça e Verdade</strong>
        </button>
        <button class="tab" data-target="dia3">
          <span>Dia 3</span>
          <strong>Vida em Cristo</strong>
        </button>
        <button class="tab" data-target="dia4">
          <span>Dia 4</span>
          <strong>Missão e Proclamação</strong>
        </button>
      </div>

      <!-- Conteúdo Dia 1 -->
      <section id="dia1" class="conteudo-dia active">
        <h2>Dia 1</h2>
        <div class="tema">Tema sugerido: Fundamentos do Evangelho</div>
        <div class="linha"></div>

        <div class="blocos">
          <!-- PDFs -->
          <div class="bloco">
            <div class="bloco-titulo">
              <div class="icone-circulo">📄</div>
              <h3>Esboços & PDFs</h3>
            </div>
            <p class="descricao">
              Materiais de estudo, esboços das mensagens e leituras recomendadas.
            </p>
            <ul class="arquivos">
              <!-- EXEMPLOS – troque o href e o texto -->
              <li>
                <div class="icone-arquivo">PDF</div>
                <div class="arquivo-nome">
                  <a href="arquivos/dia1-esboco.pdf" target="_blank">
                    Esboço – Fundamentos do Evangelho
                  </a>
                </div>
                <div class="arquivo-tipo">Estudo</div>
              </li>
              <li>
                <div class="icone-arquivo">PDF</div>
                <div class="arquivo-nome">
                  <a href="arquivos/dia1-textos-base.pdf" target="_blank">
                    Textos bíblicos de apoio
                  </a>
                </div>
                <div class="arquivo-tipo">Referência</div>
              </li>
            </ul>
          </div>

          <!-- Áudios -->
          <div class="bloco">
            <div class="bloco-titulo">
              <div class="icone-circulo">🎧</div>
              <h3>Áudios</h3>
            </div>
            <p class="descricao">
              Mensagens gravadas ou devocionais em áudio relacionados ao tema.
            </p>
            <ul class="arquivos">
              <li>
                <div class="icone-arquivo audio">AUD</div>
                <div class="arquivo-nome">
                  <a href="audios/dia1-mensagem.mp3" target="_blank">
                    Mensagem principal – Dia 1
                  </a>
                </div>
                <div class="arquivo-tipo">Mensagem</div>
              </li>
            </ul>
          </div>
        </div>
      </section>

      <!-- Conteúdo Dia 2 -->
      <section id="dia2" class="conteudo-dia">
        <h2>Dia 2</h2>
        <div class="tema">Tema sugerido: Graça e Verdade</div>
        <div class="linha"></div>

        <div class="blocos">
          <div class="bloco">
            <div class="bloco-titulo">
              <div class="icone-circulo">📄</div>
              <h3>Esboços & PDFs</h3>
            </div>
            <p class="descricao">Adicione aqui os PDFs do segundo dia.</p>
            <ul class="arquivos">
              <li>
                <div class="icone-arquivo">PDF</div>
                <div class="arquivo-nome">
                  <a href="#" target="_blank">
                    [Adicionar link de PDF]
                  </a>
                </div>
                <div class="arquivo-tipo">Estudo</div>
              </li>
            </ul>
          </div>

          <div class="bloco">
            <div class="bloco-titulo">
              <div class="icone-circulo">🎧</div>
              <h3>Áudios</h3>
            </div>
            <p class="descricao">Adicione aqui os áudios do segundo dia.</p>
            <ul class="arquivos">
              <li>
                <div class="icone-arquivo audio">AUD</div>
                <div class="arquivo-nome">
                  <a href="#" target="_blank">
                    [Adicionar link de áudio]
                  </a>
                </div>
                <div class="arquivo-tipo">Mensagem</div>
              </li>
            </ul>
          </div>
        </div>
      </section>

      <!-- Conteúdo Dia 3 -->
      <section id="dia3" class="conteudo-dia">
        <h2>Dia 3</h2>
        <div class="tema">Tema sugerido: Vida em Cristo</div>
        <div class="linha"></div>

        <div class="blocos">
          <div class="bloco">
            <div class="bloco-titulo">
              <div class="icone-circulo">📄</div>
              <h3>Esboços & PDFs</h3>
            </div>
            <p class="descricao">Adicione aqui os PDFs do terceiro dia.</p>
            <ul class="arquivos">
              <li>
                <div class="icone-arquivo">PDF</div>
                <div class="arquivo-nome">
                  <a href="#" target="_blank">
                    [Adicionar link de PDF]
                  </a>
                </div>
                <div class="arquivo-tipo">Estudo</div>
              </li>
            </ul>
          </div>

          <div class="bloco">
            <div class="bloco-titulo">
              <div class="icone-circulo">🎧</div>
              <h3>Áudios</h3>
            </div>
            <p class="descricao">Adicione aqui os áudios do terceiro dia.</p>
            <ul class="arquivos">
              <li>
                <div class="icone-arquivo audio">AUD</div>
                <div class="arquivo-nome">
                  <a href="#" target="_blank">
                    [Adicionar link de áudio]
                  </a>
                </div>
                <div class="arquivo-tipo">Mensagem</div>
              </li>
            </ul>
          </div>
        </div>
      </section>

      <!-- Conteúdo Dia 4 -->
      <section id="dia4" class="conteudo-dia">
        <h2>Dia 4</h2>
        <div class="tema">Tema sugerido: Missão e Proclamação</div>
        <div class="linha"></div>

        <div class="blocos">
          <div class="bloco">
            <div class="bloco-titulo">
              <div class="icone-circulo">📄</div>
              <h3>Esboços & PDFs</h3>
            </div>
            <p class="descricao">Adicione aqui os PDFs do quarto dia.</p>
            <ul class="arquivos">
              <li>
                <div class="icone-arquivo">PDF</div>
                <div class="arquivo-nome">
                  <a href="#" target="_blank">
                    [Adicionar link de PDF]
                  </a>
                </div>
                <div class="arquivo-tipo">Estudo</div>
              </li>
            </ul>
          </div>

          <div class="bloco">
            <div class="bloco-titulo">
              <div class="icone-circulo">🎧</div>
              <h3>Áudios</h3>
            </div>
            <p class="descricao">Adicione aqui os áudios do quarto dia.</p>
            <ul class="arquivos">
              <li>
                <div class="icone-arquivo audio">AUD</div>
                <div class="arquivo-nome">
                  <a href="#" target="_blank">
                    [Adicionar link de áudio]
                  </a>
                </div>
                <div class="arquivo-tipo">Mensagem</div>
              </li>
            </ul>
          </div>
        </div>
      </section>
    </div>

    <footer>
      &copy; <span id="ano"></span> Conferência do Evangelho – Materiais para participantes.
    </footer>
  </main>

  <script>
    // Tabs
    const tabs = document.querySelectorAll(".tab");
    const dias = document.querySelectorAll(".conteudo-dia");

    tabs.forEach(tab => {
      tab.addEventListener("click", () => {
        const alvo = tab.getAttribute("data-target");
        tabs.forEach(t => t.classList.remove("active"));
        dias.forEach(d => d.classList.remove("active"));
        tab.classList.add("active");
        document.getElementById(alvo).classList.add("active");
      });
    });

    // Ano rodapé
    document.getElementById("ano").textContent = new Date().getFullYear();
  </script>
</body>
</html>
