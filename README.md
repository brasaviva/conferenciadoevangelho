<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Conferência do Evangelho</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;0,700;1,400;1,600&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />

  <style>
    :root {
      --bege:     #e8d4a8;
      --bege-claro: #f5e9cc;
      --bege-escuro: #c9aa72;
      --marrom:   #3a2310;
      --marrom-medio: #6b4423;
      --dourado:  #b8893a;
      --dourado-claro: #d4a85a;
      --texto:    #2c1a0a;
      --muted:    #7a5530;
    }

    *, *::before, *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html { scroll-behavior: smooth; }

    body {
      background-color: var(--bege);
      color: var(--texto);
      font-family: "Inter", sans-serif;
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* ── FUNDO GREGO ── */
    body::before {
      content: "εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον εὐαγγέλιον";
      position: fixed;
      inset: 0;
      font-family: "Cormorant Garamond", serif;
      font-size: 1.3rem;
      font-style: italic;
      color: rgba(90, 55, 20, 0.08);
      word-break: break-all;
      line-height: 2.2;
      padding: 20px;
      pointer-events: none;
      z-index: 0;
      overflow: hidden;
    }

    /* ── HERO ── */
    .hero {
      position: relative;
      z-index: 1;
      text-align: center;
      padding: 56px 24px 40px;
      background: linear-gradient(180deg, rgba(245,233,204,0.96) 0%, rgba(232,212,168,0.85) 100%);
      border-bottom: 1px solid rgba(184,137,58,0.35);
    }

    .hero-data {
      font-family: "Cormorant Garamond", serif;
      font-size: 1.2rem;
      font-style: italic;
      font-weight: 600;
      letter-spacing: 0.08em;
      color: var(--marrom-medio);
      margin-bottom: 6px;
    }

    .hero-pastores {
      font-family: "Cormorant Garamond", serif;
      font-size: 1rem;
      font-style: italic;
      color: var(--muted);
      margin-bottom: 28px;
      letter-spacing: 0.04em;
    }

    .hero-titulo-sup {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(1.1rem, 4vw, 1.5rem);
      font-weight: 400;
      letter-spacing: 0.35em;
      text-transform: uppercase;
      color: var(--marrom);
      margin-bottom: 4px;
    }

    .hero-titulo-principal {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(3.5rem, 14vw, 7.5rem);
      font-weight: 700;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      line-height: 0.92;
      color: var(--marrom);
      margin-bottom: 20px;
      text-shadow: 2px 4px 18px rgba(60,35,16,0.18);
    }

    .hero-tagline {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(1rem, 3vw, 1.2rem);
      font-style: italic;
      color: var(--marrom-medio);
      max-width: 520px;
      margin: 0 auto 24px;
      line-height: 1.6;
    }

    .hero-grego {
      display: inline-block;
      font-family: "Cormorant Garamond", serif;
      font-style: italic;
      font-size: 0.88rem;
      color: var(--muted);
      border-top: 1px solid rgba(184,137,58,0.4);
      padding-top: 10px;
      margin-top: 8px;
    }

    .hero-grego strong {
      display: block;
      font-size: 1.1rem;
      font-weight: 600;
      color: var(--marrom);
    }

    /* ── CHAMA / ÍCONE ── */
    .icone-chama {
      font-size: 2rem;
      margin-bottom: 20px;
      display: block;
    }

    /* ── MAIN ── */
    main {
      position: relative;
      z-index: 1;
      max-width: 880px;
      margin: 0 auto;
      padding: 32px 16px 48px;
    }

    /* ── AVISO ── */
    .aviso {
      background: rgba(255,255,255,0.55);
      border: 1px solid rgba(184,137,58,0.45);
      border-radius: 14px;
      padding: 13px 16px;
      font-size: 0.88rem;
      color: var(--marrom-medio);
      margin-bottom: 24px;
      backdrop-filter: blur(6px);
      text-align: center;
      font-family: "Inter", sans-serif;
    }

    /* ── TABS ── */
    .tabs {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 16px;
    }

    .tab {
      flex: 1 1 calc(50% - 4px);
      padding: 10px 12px;
      border-radius: 12px;
      border: 1px solid rgba(107,68,35,0.35);
      background: rgba(245,233,204,0.6);
      cursor: pointer;
      transition: all 0.18s ease;
      text-align: left;
      backdrop-filter: blur(4px);
    }

    .tab:hover {
      background: rgba(245,233,204,0.9);
      border-color: var(--dourado);
    }

    .tab .tab-label {
      font-family: "Inter", sans-serif;
      font-size: 0.7rem;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      color: var(--muted);
      margin-bottom: 2px;
    }

    .tab .tab-nome {
      font-family: "Cormorant Garamond", serif;
      font-size: 1rem;
      font-weight: 600;
      color: var(--marrom);
    }

    .tab.active {
      background: linear-gradient(135deg, #f9e4a8, var(--dourado));
      border-color: var(--marrom-medio);
      box-shadow: 0 4px 14px rgba(100,60,20,0.28), 0 0 0 1px rgba(255,255,255,0.5);
      transform: translateY(-1px);
    }

    .tab.active .tab-label {
      color: rgba(42,20,4,0.7);
    }

    .tab.active .tab-nome {
      color: var(--marrom);
    }

    /* ── PAINEL DE DIA ── */
    .conteudo-dia {
      display: none;
      background: rgba(255,255,255,0.6);
      border-radius: 18px;
      border: 1px solid rgba(184,137,58,0.5);
      padding: 22px 18px 24px;
      backdrop-filter: blur(8px);
      box-shadow: 0 8px 32px rgba(60,35,16,0.1);
    }

    .conteudo-dia.active {
      display: block;
      animation: fadeIn 0.25s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(6px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    .dia-titulo {
      font-family: "Cormorant Garamond", serif;
      font-size: 1.5rem;
      font-weight: 700;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--marrom);
      margin-bottom: 2px;
    }

    .dia-tema {
      font-family: "Cormorant Garamond", serif;
      font-size: 1rem;
      font-style: italic;
      color: var(--muted);
      margin-bottom: 14px;
    }

    .divisor {
      height: 1px;
      background: linear-gradient(to right, transparent, var(--dourado), transparent);
      margin: 12px 0 16px;
    }

    /* ── GRID DE BLOCOS ── */
    .blocos {
      display: grid;
      grid-template-columns: 1fr;
      gap: 14px;
    }

    @media (min-width: 600px) {
      .blocos { grid-template-columns: 1fr 1fr; }
    }

    /* ── BLOCO (PDF / ÁUDIO) ── */
    .bloco {
      background: linear-gradient(145deg, #fdf5e0, #f5e6c0);
      border: 1px solid rgba(160,110,50,0.45);
      border-radius: 14px;
      padding: 14px 13px 16px;
      box-shadow: 0 2px 10px rgba(80,48,18,0.1);
    }

    .bloco-header {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 10px;
    }

    .bloco-icone {
      width: 36px;
      height: 36px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.1rem;
      flex-shrink: 0;
      box-shadow: 0 2px 6px rgba(60,35,16,0.25);
    }

    .bloco-icone.pdf  { background: linear-gradient(135deg, #c0392b, #e74c3c); }
    .bloco-icone.audio { background: linear-gradient(135deg, #5a2d82, #8e44ad); }

    .bloco-titulo {
      font-family: "Inter", sans-serif;
      font-size: 0.82rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--marrom);
    }

    /* ── ITENS DE ARQUIVO ── */
    .arquivo-item {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 8px 10px;
      border-radius: 10px;
      background: rgba(255,255,255,0.65);
      border: 1px solid rgba(184,137,58,0.3);
      margin-bottom: 6px;
      transition: background 0.15s, transform 0.12s;
      text-decoration: none;
      color: inherit;
    }

    .arquivo-item:last-child { margin-bottom: 0; }

    .arquivo-item:hover {
      background: rgba(255,255,255,0.9);
      transform: translateX(3px);
      border-color: var(--dourado);
    }

    .arquivo-badge {
      font-family: "Inter", sans-serif;
      font-size: 0.62rem;
      font-weight: 700;
      letter-spacing: 0.08em;
      padding: 3px 6px;
      border-radius: 6px;
      flex-shrink: 0;
    }

    .arquivo-badge.pdf   { background: #fde8e8; color: #c0392b; }
    .arquivo-badge.audio { background: #f0e6f8; color: #7d3c98; }

    .arquivo-nome {
      font-family: "Inter", sans-serif;
      font-size: 0.88rem;
      font-weight: 400;
      color: var(--marrom);
      flex: 1;
    }

    .arquivo-seta {
      font-size: 0.8rem;
      color: var(--dourado);
    }

    /* placeholder "em breve" */
    .em-breve {
      font-family: "Inter", sans-serif;
      font-size: 0.82rem;
      color: var(--muted);
      font-style: italic;
      padding: 6px 2px;
    }

    /* ── FOOTER ── */
    footer {
      position: relative;
      z-index: 1;
      text-align: center;
      padding: 0 16px 32px;
      font-family: "Cormorant Garamond", serif;
      font-style: italic;
      font-size: 0.9rem;
      color: var(--muted);
    }

    @media (min-width: 720px) {
      .hero { padding: 64px 24px 48px; }
      main  { padding: 36px 20px 56px; }
      .tab  { flex: 1 1 calc(25% - 6px); }
    }
  </style>
</head>
<body>

  <!-- ══ HERO ══ -->
  <div class="hero">
    <div class="hero-data">09 a 12 de Abril</div>
    <div class="hero-pastores">
      Pastor Herso Meus &nbsp;|&nbsp; Pastor Aroní Padilha &nbsp;|&nbsp; Pastor Paulo Duarte
    </div>

    <div class="hero-titulo-sup">Conferência do</div>
    <div class="hero-titulo-principal">Evangelho</div>

    <p class="hero-tagline">
      Confrontando as crenças erradas que distorcem a fé<br />
      e desviam o foco de Cristo na igreja atual.
    </p>

    <span class="icone-chama">🔥</span>

    <div class="hero-grego">
      <strong>ευαγγελιον</strong>
      <em>Euangelion</em> — palavra grega que significa "boa notícia" ou "boas novas"
    </div>
  </div>

  <!-- ══ CONTEÚDOS ══ -->
  <main>
    <div class="aviso">
      Materiais exclusivos para participantes · Acesse durante e após as ministrações
    </div>

    <!-- Abas -->
    <div class="tabs">
      <button class="tab active" data-target="dia1">
        <div class="tab-label">Dia 1</div>
        <div class="tab-nome">09 de Abril</div>
      </button>
      <button class="tab" data-target="dia2">
        <div class="tab-label">Dia 2</div>
        <div class="tab-nome">10 de Abril</div>
      </button>
      <button class="tab" data-target="dia3">
        <div class="tab-label">Dia 3</div>
        <div class="tab-nome">11 de Abril</div>
      </button>
      <button class="tab" data-target="dia4">
        <div class="tab-label">Dia 4</div>
        <div class="tab-nome">12 de Abril</div>
      </button>
    </div>

    <!-- ── DIA 1 ── -->
    <section id="dia1" class="conteudo-dia active">
      <div class="dia-titulo">Dia 1</div>
      <div class="dia-tema">Tema — 09 de Abril</div>
      <div class="divisor"></div>

      <div class="blocos">
        <div class="bloco">
          <div class="bloco-header">
            <div class="bloco-icone pdf">📄</div>
            <div class="bloco-titulo">Esboços & PDFs</div>
          </div>
          <!-- ADICIONE SEUS PDFs AQUI -->
          <a class="arquivo-item" href="arquivos/dia1-esboco.pdf" target="_blank">
            <span class="arquivo-badge pdf">PDF</span>
            <span class="arquivo-nome">Esboço – Dia 1</span>
            <span class="arquivo-seta">↗</span>
          </a>
          <!-- Duplicar o bloco acima para adicionar mais PDFs -->
        </div>

        <div class="bloco">
          <div class="bloco-header">
            <div class="bloco-icone audio">🎧</div>
            <div class="bloco-titulo">Áudios</div>
          </div>
          <!-- ADICIONE SEUS ÁUDIOS AQUI -->
          <a class="arquivo-item" href="audios/dia1-mensagem.mp3" target="_blank">
            <span class="arquivo-badge audio">ÁUD</span>
            <span class="arquivo-nome">Mensagem – Dia 1</span>
            <span class="arquivo-seta">↗</span>
          </a>
        </div>
      </div>
    </section>

    <!-- ── DIA 2 ── -->
    <section id="dia2" class="conteudo-dia">
      <div class="dia-titulo">Dia 2</div>
      <div class="dia-tema">Tema — 10 de Abril</div>
      <div class="divisor"></div>

      <div class="blocos">
        <div class="bloco">
          <div class="bloco-header">
            <div class="bloco-icone pdf">📄</div>
            <div class="bloco-titulo">Esboços & PDFs</div>
          </div>
          <p class="em-breve">Materiais serão adicionados em breve.</p>
        </div>

        <div class="bloco">
          <div class="bloco-header">
            <div class="bloco-icone audio">🎧</div>
            <div class="bloco-titulo">Áudios</div>
          </div>
          <p class="em-breve">Áudios serão adicionados em breve.</p>
        </div>
      </div>
    </section>

    <!-- ── DIA 3 ── -->
    <section id="dia3" class="conteudo-dia">
      <div class="dia-titulo">Dia 3</div>
      <div class="dia-tema">Tema — 11 de Abril</div>
      <div class="divisor"></div>

      <div class="blocos">
        <div class="bloco">
          <div class="bloco-header">
            <div class="bloco-icone pdf">📄</div>
            <div class="bloco-titulo">Esboços & PDFs</div>
          </div>
          <p class="em-breve">Materiais serão adicionados em breve.</p>
        </div>

        <div class="bloco">
          <div class="bloco-header">
            <div class="bloco-icone audio">🎧</div>
            <div class="bloco-titulo">Áudios</div>
          </div>
          <p class="em-breve">Áudios serão adicionados em breve.</p>
        </div>
      </div>
    </section>

    <!-- ── DIA 4 ── -->
    <section id="dia4" class="conteudo-dia">
      <div class="dia-titulo">Dia 4</div>
      <div class="dia-tema">Tema — 12 de Abril</div>
      <div class="divisor"></div>

      <div class="blocos">
        <div class="bloco">
          <div class="bloco-header">
            <div class="bloco-icone pdf">📄</div>
            <div class="bloco-titulo">Esboços & PDFs</div>
          </div>
          <p class="em-breve">Materiais serão adicionados em breve.</p>
        </div>

        <div class="bloco">
          <div class="bloco-header">
            <div class="bloco-icone audio">🎧</div>
            <div class="bloco-titulo">Áudios</div>
          </div>
          <p class="em-breve">Áudios serão adicionados em breve.</p>
        </div>
      </div>
    </section>
  </main>

  <footer>
    &copy; <span id="ano"></span> &nbsp;·&nbsp; Conferência do Evangelho &nbsp;·&nbsp; Materiais para participantes
  </footer>

  <script>
    // Tabs
    const tabs = document.querySelectorAll(".tab");
    const dias  = document.querySelectorAll(".conteudo-dia");

    tabs.forEach(tab => {
      tab.addEventListener("click", () => {
        const alvo = tab.dataset.target;
        tabs.forEach(t => t.classList.remove("active"));
        dias.forEach(d => d.classList.remove("active"));
        tab.classList.add("active");
        document.getElementById(alvo).classList.add("active");
      });
    });

    document.getElementById("ano").textContent = new Date().getFullYear();
  </script>
</body>
</html>
