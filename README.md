<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Hefesto | Soluções em Tecnologia e Gestão de Pessoas</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg: #070707;
      --bg-soft: #0f0a0a;
      --wine: #2a0709;
      --wine-strong: #4e0c11;
      --gold: #d4a03a;
      --gold-soft: #f1d08a;
      --text: #f8f4ee;
      --muted: rgba(248, 244, 238, 0.74);
      --muted-2: rgba(248, 244, 238, 0.58);
      --line: rgba(255, 255, 255, 0.08);
      --card: linear-gradient(180deg, rgba(255,255,255,0.07), rgba(255,255,255,0.03));
      --card-border: rgba(212, 160, 58, 0.18);
      --shadow: 0 24px 70px rgba(0, 0, 0, 0.35);
      --radius-xl: 30px;
      --radius-lg: 22px;
      --radius-md: 16px;
      --max-width: 1200px;
      --transition: 0.32s ease;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Inter', sans-serif;
      color: var(--text);
      line-height: 1.6;
      background:
        radial-gradient(circle at top left, rgba(212, 160, 58, 0.10), transparent 20%),
        radial-gradient(circle at top right, rgba(139, 0, 0, 0.18), transparent 24%),
        radial-gradient(circle at 50% 20%, rgba(212, 160, 58, 0.05), transparent 30%),
        linear-gradient(180deg, #050505 0%, #110707 28%, #2a0709 62%, #4e0c11 100%);
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      background-image:
        linear-gradient(rgba(255,255,255,0.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.025) 1px, transparent 1px);
      background-size: 40px 40px;
      mask-image: linear-gradient(180deg, rgba(0,0,0,0.35), transparent 80%);
      opacity: 0.22;
      z-index: 0;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      display: block;
      max-width: 100%;
    }

    .container {
      width: min(92%, var(--max-width));
      margin: 0 auto;
      position: relative;
      z-index: 1;
    }

    .section {
      padding: 100px 0;
    }

    .section-header {
      max-width: 760px;
      margin-bottom: 42px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 18px;
      color: var(--gold-soft);
      font-size: 0.92rem;
      font-weight: 700;
      letter-spacing: 0.14em;
      text-transform: uppercase;
    }

    .eyebrow::before {
      content: "";
      width: 36px;
      height: 1px;
      background: linear-gradient(90deg, var(--gold), transparent);
    }

    .section-title {
      font-size: clamp(2.2rem, 4.5vw, 4rem);
      line-height: 1.03;
      letter-spacing: -0.04em;
      margin-bottom: 14px;
      font-weight: 800;
    }

    .section-subtitle {
      font-size: 1.05rem;
      color: var(--muted);
      max-width: 720px;
    }

    .card {
      background: var(--card);
      border: 1px solid var(--card-border);
      border-radius: var(--radius-xl);
      box-shadow: var(--shadow);
      backdrop-filter: blur(10px);
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 54px;
      padding: 0 24px;
      border-radius: 999px;
      font-weight: 700;
      transition: var(--transition);
      border: 1px solid transparent;
      cursor: pointer;
    }

    .btn-primary {
      background: linear-gradient(135deg, #d4a03a, #b98221);
      color: #140a02;
      box-shadow: 0 16px 34px rgba(0, 0, 0, 0.28);
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      filter: brightness(1.05);
    }

    .btn-secondary {
      border-color: rgba(212, 160, 58, 0.32);
      background: rgba(255,255,255,0.03);
      color: var(--text);
    }

    .btn-secondary:hover {
      transform: translateY(-2px);
      background: rgba(255,255,255,0.06);
    }

    header {
      position: sticky;
      top: 0;
      z-index: 50;
      background: rgba(5, 5, 5, 0.72);
      backdrop-filter: blur(16px);
      border-bottom: 1px solid rgba(255,255,255,0.06);
    }

    .nav {
      min-height: 82px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 14px;
      min-width: 0;
    }

    .brand-mark {
      width: 48px;
      height: 48px;
      border-radius: 16px;
      object-fit: cover;
      border: 1px solid rgba(212, 160, 58, 0.24);
      box-shadow: 0 10px 28px rgba(0, 0, 0, 0.22);
      flex-shrink: 0;
      background: #000;
    }

    .brand-text {
      display: flex;
      flex-direction: column;
      min-width: 0;
    }

    .brand-name {
      font-size: 0.96rem;
      font-weight: 800;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      white-space: nowrap;
    }

    .brand-subtitle {
      font-size: 0.76rem;
      color: var(--muted-2);
      letter-spacing: 0.08em;
      text-transform: uppercase;
      white-space: nowrap;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 26px;
    }

    .nav-links a {
      color: var(--muted);
      font-size: 0.95rem;
      font-weight: 500;
      transition: var(--transition);
      position: relative;
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -8px;
      width: 0;
      height: 1px;
      background: var(--gold);
      transition: var(--transition);
    }

    .nav-links a:hover {
      color: var(--text);
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .nav-toggle {
      display: none;
      background: transparent;
      border: 0;
      color: #fff;
      font-size: 1.7rem;
      cursor: pointer;
    }

    .hero {
  padding: 28px 0 36px;
}

.hero-premium {
  display: grid;
  gap: 34px;
}

.hero-banner-top {
  width: 100%;
  border-radius: 0;
  overflow: hidden;
}

.hero-banner-top img {
  width: 100%;
  height: auto;
  display: block;
  object-fit: cover;
}

.hero-content-block {
  width: 100%;
  max-width: 100%;
}

.hero-title {
  font-size: clamp(1.8rem, 3.2vw, 3rem);
  line-height: 1.15;
  font-weight: 800;
  letter-spacing: -0.02em;
  margin-bottom: 30px;
  color: #ffffff;
  max-width: 100%;
}

.hero-cards {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
}

.hero-card {
  padding: 24px 22px;
  border-radius: 22px;
  background: linear-gradient(180deg, rgba(0,0,0,0.78), rgba(20,20,20,0.62));
  border: 1px solid rgba(212, 160, 58, 0.14);
  box-shadow: 0 18px 40px rgba(0,0,0,0.18);
  transition: 0.3s ease;
}

.hero-card:nth-child(2) {
  background: linear-gradient(135deg, rgba(16,16,16,0.82), rgba(70,12,17,0.72));
}

.hero-card:nth-child(3) {
  background: linear-gradient(135deg, rgba(48,8,10,0.84), rgba(104,10,12,0.72));
}

.hero-card:hover {
  transform: translateY(-4px);
  border-color: rgba(212, 160, 58, 0.28);
}

.hero-card h3 {
  font-size: 1.08rem;
  line-height: 1.45;
  margin-bottom: 10px;
  color: #ffffff;
}

.hero-card p {
  font-size: 0.98rem;
  line-height: 1.65;
  color: rgba(255,255,255,0.82);
}

@media (max-width: 900px) {
  .hero-cards {
    grid-template-columns: 1fr;
  }

  .hero-title {
    margin-bottom: 22px;
  }
}

    .results-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 18px;
      margin-top: 26px;
    }

    .result-card {
      padding: 24px;
      border-radius: 22px;
      background: linear-gradient(180deg, rgba(255,255,255,0.06), rgba(255,255,255,0.03));
      border: 1px solid rgba(212, 160, 58, 0.14);
      transition: var(--transition);
    }

    .result-card:hover,
    .service-card:hover,
    .project-card:hover,
    .mvv-item:hover,
    .contact-item:hover {
      transform: translateY(-5px);
      border-color: rgba(212, 160, 58, 0.32);
    }

    .result-number {
      display: inline-block;
      margin-bottom: 14px;
      font-size: 2.2rem;
      line-height: 1;
      color: var(--gold);
      font-weight: 800;
      letter-spacing: -0.04em;
    }

    .result-card h3 {
      font-size: 1.08rem;
      margin-bottom: 6px;
    }

    .result-card p {
      color: var(--muted);
      font-size: 0.96rem;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 20px;
    }

    .service-card,
    .project-card {
      padding: 28px;
      border-radius: 24px;
      background: linear-gradient(180deg, rgba(255,255,255,0.06), rgba(255,255,255,0.03));
      border: 1px solid rgba(212, 160, 58, 0.14);
      box-shadow: 0 14px 38px rgba(0,0,0,0.16);
      transition: var(--transition);
    }

    .service-card strong {
      display: block;
      margin-bottom: 10px;
      font-size: 1.08rem;
      color: var(--gold-soft);
    }

    .service-card p,
    .project-card p {
      color: var(--muted);
      font-size: 0.98rem;
    }

    .mvv-wrap {
      width: min(100%, 1040px);
      margin: 0 auto;
    }

    .mvv-card {
      padding: 40px;
    }

    .mvv-top {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 18px;
      margin-bottom: 26px;
    }

    .mvv-mark {
      width: 58px;
      height: 58px;
      border-radius: 18px;
      object-fit: cover;
      border: 1px solid rgba(212, 160, 58, 0.22);
      background: #000;
      flex-shrink: 0;
    }

    .mvv-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
    }

    .mvv-item {
      padding: 24px;
      border-radius: 22px;
      background: rgba(255,255,255,0.035);
      border: 1px solid rgba(255,255,255,0.08);
      transition: var(--transition);
    }

    .mvv-item.full {
      grid-column: 1 / -1;
    }

    .mvv-item h3 {
      margin-bottom: 8px;
      font-size: 1.08rem;
      color: var(--gold-soft);
    }

    .mvv-item p,
    .mvv-item li {
      color: var(--muted);
    }

    .mvv-values {
      display: grid;
      gap: 10px;
      margin-top: 8px;
    }

    .mvv-values li {
      list-style: none;
      position: relative;
      padding-left: 18px;
    }

    .mvv-values li::before {
      content: "•";
      position: absolute;
      left: 0;
      top: 0;
      color: var(--gold);
    }

    .journey-grid {
      display: grid;
      grid-template-columns: 0.95fr 1.05fr;
      gap: 28px;
      align-items: start;
    }

    .journey-card {
      padding: 34px;
    }

    .journey-line {
      position: relative;
      padding-left: 28px;
      display: grid;
      gap: 28px;
    }

    .journey-line::before {
      content: "";
      position: absolute;
      left: 8px;
      top: 6px;
      bottom: 6px;
      width: 2px;
      background: linear-gradient(180deg, rgba(212,160,58,0.45), rgba(255,255,255,0.08));
    }

    .journey-step {
      position: relative;
    }

    .journey-step::before {
      content: "";
      position: absolute;
      left: -28px;
      top: 6px;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      background: var(--gold);
      box-shadow: 0 0 0 6px rgba(212,160,58,0.08);
    }

    .journey-step span {
      display: inline-block;
      margin-bottom: 6px;
      color: var(--gold-soft);
      font-size: 0.82rem;
      font-weight: 800;
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }

    .journey-step h4 {
      margin-bottom: 6px;
      font-size: 1.08rem;
    }

    .journey-step p {
      color: var(--muted);
    }

    .journey-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      margin-top: 4px;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 22px;
    }

    .project-meta {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin: 18px 0 16px;
    }

    .project-meta span {
      padding: 8px 12px;
      border-radius: 999px;
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(212,160,58,0.16);
      color: var(--gold-soft);
      font-size: 0.82rem;
      font-weight: 700;
    }

    .project-points {
      display: grid;
      gap: 10px;
      margin-top: 10px;
    }

    .project-points li {
      list-style: none;
      position: relative;
      padding-left: 18px;
      color: var(--muted);
      font-size: 0.95rem;
    }

    .project-points li::before {
      content: "•";
      position: absolute;
      left: 0;
      top: 0;
      color: var(--gold);
    }

    .contact-shell {
      padding: 34px;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 0.9fr 1.1fr;
      gap: 28px;
      align-items: start;
    }

    .contact-intro p {
      color: var(--muted);
      margin-bottom: 22px;
      max-width: 520px;
    }

    .contact-list {
      display: grid;
      gap: 16px;
    }

    .contact-item {
      display: flex;
      justify-content: space-between;
      gap: 18px;
      padding: 18px 20px;
      border-radius: 18px;
      background: rgba(255,255,255,0.03);
      border: 1px solid rgba(255,255,255,0.08);
      transition: var(--transition);
    }

    .contact-item strong {
      color: var(--gold-soft);
      flex-shrink: 0;
    }

    .contact-item span,
    .contact-item a {
      color: var(--muted);
      word-break: break-word;
      text-align: right;
    }

    .contact-links {
      display: grid;
      gap: 6px;
      text-align: right;
    }

    footer {
      padding: 40px 0 50px;
      position: relative;
      z-index: 1;
    }

    .footer-shell {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 14px;
      padding-top: 26px;
      border-top: 1px solid rgba(212, 160, 58, 0.16);
      text-align: center;
    }

    .footer-icon {
      width: 54px;
      height: 54px;
      border-radius: 18px;
      object-fit: cover;
      border: 1px solid rgba(212, 160, 58, 0.24);
      background: #000;
      box-shadow: 0 12px 26px rgba(0, 0, 0, 0.24);
    }

    .footer-shell p {
      color: var(--muted);
      font-size: 0.93rem;
      letter-spacing: 0.04em;
      text-transform: uppercase;
    }

    .reveal {
      opacity: 0;
      transform: translateY(28px);
      transition: 0.7s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    @media (max-width: 1100px) {
      .hero-grid,
      .journey-grid,
      .contact-grid {
        grid-template-columns: 1fr;
      }

      .results-grid,
      .services-grid,
      .projects-grid,
      .hero-points {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }

    @media (max-width: 760px) {
      .nav-toggle {
        display: block;
      }

      .nav-links {
        position: absolute;
        top: 82px;
        left: 0;
        width: 100%;
        padding: 24px 4%;
        background: rgba(8, 8, 8, 0.97);
        border-bottom: 1px solid rgba(255,255,255,0.08);
        flex-direction: column;
        align-items: flex-start;
        gap: 18px;
        display: none;
      }

      .nav-links.open {
        display: flex;
      }

      .brand-subtitle {
        display: none;
      }

      .hero-grid {
        padding: 22px;
      }

      .hero-title {
        font-size: 2.4rem;
      }

      .hero-actions,
      .journey-actions {
        flex-direction: column;
        align-items: stretch;
      }

      .btn {
        width: 100%;
      }

      .results-grid,
      .services-grid,
      .projects-grid,
      .hero-points,
      .mvv-grid {
        grid-template-columns: 1fr;
      }

      .mvv-card,
      .journey-card,
      .contact-shell,
      .service-card,
      .project-card,
      .result-card {
        padding: 24px;
      }

      .contact-item {
        flex-direction: column;
        align-items: flex-start;
      }

      .contact-item span,
      .contact-item a,
      .contact-links {
        text-align: left;
      }

      .hero-floating-card {
        position: static;
        width: 100%;
        margin-top: 16px;
      }

      .section {
        padding: 78px 0;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <a href="#inicio" class="brand">
        <img src="icone-hefesto.png" alt="Ícone Hefesto" class="brand-mark">
        <span class="brand-text">
          <span class="brand-name">Hefesto</span>
          <span class="brand-subtitle">Soluções em TI e Gestão de Pessoas</span>
        </span>
      </a>

      <button class="nav-toggle" id="navToggle" aria-label="Abrir menu">☰</button>

      <nav class="nav-links" id="navLinks">
        <a href="#sobre">Sobre</a>
        <a href="#especialidades">Especialidades</a>
        <a href="#mvv">MVV</a>
        <a href="#diferenciais">Diferenciais</a>
        <a href="#projetos">Projetos</a>
        <a href="#contato">Contato</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" id="inicio">
  <div class="container hero-premium">
    <div class="hero-banner-top reveal">
      <img src="hefesto.jpg" alt="Banner principal da Hefesto">
    </div>

    <div class="hero-content-block reveal" id="sobre">
      <h4 class="hero-title">
        Desenvolvemos, implementamos e aprimoramos N soluções tecnológicas para o sucesso da sua empresa.
      </h4>

      <div class="hero-cards">
        <article class="hero-card">
          <h3>Mapeamento</h3>
          <p>
            Identificamos gargalos e oportunidades de automação e melhoria em processos e estratégias.
          </p>
        </article>

        <article class="hero-card">
          <h3>Desenvolvimento Sob Medida</h3>
          <p>
            Criamos soluções adaptadas à realidade da sua operação, com foco em performance, organização e escalabilidade.
          </p>
        </article>

        <article class="hero-card">
          <h3>Integração entre Pessoas e Sistemas</h3>
          <p>
            Conectamos tecnologia, dados e gestão de pessoas para gerar fluidez e apoiar decisões mais inteligentes.
          </p>
        </article>
      </div>
    </div>
  </div>
</section>

    <section class="section" id="especialidades">
      <div class="container">
        <div class="section-header reveal">
          <div class="eyebrow">especialidades</div>
          <h2 class="section-title">O que fazemos</h2>
          <p class="section-subtitle">
            Atuamos na interseção entre pessoas, dados e tecnologia, desenvolvendo soluções com sofisticação visual, consistência técnica e foco prático na rotina da empresa.
          </p>
        </div>

        <div class="services-grid">
          <article class="service-card reveal">
            <strong>WebApps</strong>
            <p>Aplicações web sob medida para otimizar operação, experiência e controle interno.</p>
          </article>

          <article class="service-card reveal">
            <strong>People Analytics</strong>
            <p>Indicadores, dashboards e leitura estratégica de métricas como headcount, absenteísmo, turnover e NPS.</p>
          </article>

          <article class="service-card reveal">
            <strong>Automação de Processos</strong>
            <p>Fluxos mais inteligentes com integrações e automações para reduzir esforço manual.</p>
          </article>

          <article class="service-card reveal">
            <strong>Customização de ERP</strong>
            <p>Desenvolvimento em AdvPL com adaptação do TOTVS Protheus à realidade do negócio.</p>
          </article>

          <article class="service-card reveal">
            <strong>Integração de Sistemas</strong>
            <p>Conectamos plataformas e dados para gerar uma operação mais centralizada e confiável.</p>
          </article>

          <article class="service-card reveal">
            <strong>Gestão de Pessoas</strong>
            <p>Onboarding, T&amp;D, recrutamento por competências, DISC, banco de talentos e endomarketing.</p>
          </article>
        </div>
      </div>
    </section>

    <section class="section" id="mvv">
      <div class="container">
        <div class="mvv-wrap">
          <div class="card mvv-card reveal">
            <div class="mvv-top">
              <div>
                <div class="eyebrow">mvv</div>
                <h2 class="section-title" style="margin-bottom: 0;">Nossa missão, visão e valores</h2>
              </div>
              <img src="icone-hefesto.png" alt="Marca Hefesto" class="mvv-mark">
            </div>

            <div class="mvv-grid">
              <div class="mvv-item">
                <h3>Missão</h3>
                <p>Transformar tecnologia em vantagem real para empresas que precisam de estrutura, clareza e soluções com propósito.</p>
              </div>

              <div class="mvv-item">
                <h3>Visão</h3>
                <p>Ser referência em soluções tecnológicas integradas à gestão de pessoas, com entregas consistentes, elegantes e duradouras.</p>
              </div>

              <div class="mvv-item full">
                <h3>Valores</h3>
                <ul class="mvv-values">
                  <li>Cada projeto é construído sob medida, sem soluções genéricas.</li>
                  <li>Acreditamos em tecnologia com alma, porque todo processo impacta pessoas.</li>
                  <li>Valorizamos clareza, consistência, compromisso e profundidade na execução.</li>
                  <li>Entramos na operação para compreender o negócio antes de propor qualquer solução.</li>
                  <li>Evoluímos continuamente para manter a entrega atual, estratégica e sustentável.</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="diferenciais">
      <div class="container journey-grid">
        <div class="section-header reveal">
          <div class="eyebrow">diferenciais</div>
          <h2 class="section-title">Da compreensão humana à tecnologia aplicada</h2>
          <p class="section-subtitle">
            Nossa força está em unir sensibilidade humana, leitura organizacional e construção técnica. Isso torna a entrega mais profunda, mais alinhada ao contexto e mais eficiente na prática.
          </p>
        </div>

        <div class="card journey-card reveal">
          <div class="journey-line">
            <div class="journey-step">
              <span>01</span>
              <h4>Tecnologia</h4>
              <p>Desenvolvimento de soluções, automações e estruturas digitais com foco em performance e organização.</p>
            </div>

            <div class="journey-step">
              <span>02</span>
              <h4>Psicologia</h4>
              <p>Base para compreender comportamento, relações, desenvolvimento humano e dinâmicas organizacionais.</p>
            </div>

            <div class="journey-step">
              <span>03</span>
              <h4>RH Estratégico</h4>
              <p>Aplicação prática em gestão de pessoas, indicadores, rotinas e apoio à tomada de decisão.</p>
            </div>

            <div class="journey-actions">
              <a href="#projetos" class="btn btn-primary">Ver projetos</a>
              <a href="https://wa.me/556798338922" class="btn btn-secondary" target="_blank" rel="noreferrer">Fale conosco</a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="projetos">
      <div class="container">
        <div class="section-header reveal">
          <div class="eyebrow">projetos</div>
          <h2 class="section-title">Cases em destaque</h2>
          <p class="section-subtitle">
            Exemplos de como aplicamos tecnologia, análise e visão de negócio para resolver problemas reais com elegância e eficiência.
          </p>
        </div>

        <div class="projects-grid">
          <article class="project-card reveal">
            <h3>Automação de Relatórios no Protheus</h3>
            <p>Desenvolvimento de relatórios personalizados em AdvPL e SQL para reduzir retrabalho e acelerar a leitura de informações estratégicas.</p>

            <div class="project-meta">
              <span>AdvPL</span>
              <span>SQL</span>
              <span>Protheus</span>
            </div>

            <ul class="project-points">
              <li><strong>Problema:</strong> rotinas manuais e baixa padronização.</li>
              <li><strong>Solução:</strong> relatório customizado com regras de negócio.</li>
              <li><strong>Resultado:</strong> mais confiabilidade, organização e agilidade.</li>
            </ul>
          </article>

          <article class="project-card reveal">
            <h3>Dashboard de Indicadores de RH</h3>
            <p>Construção de dashboards voltados ao acompanhamento de métricas de gestão de pessoas e suporte à tomada de decisão.</p>

            <div class="project-meta">
              <span>Power BI</span>
              <span>SQL</span>
              <span>Analytics</span>
            </div>

            <ul class="project-points">
              <li><strong>Problema:</strong> dados dispersos e pouca visibilidade.</li>
              <li><strong>Solução:</strong> painel centralizado com KPIs relevantes.</li>
              <li><strong>Resultado:</strong> leitura mais rápida e decisões mais claras.</li>
            </ul>
          </article>

          <article class="project-card reveal">
            <h3>Integração entre Pessoas e Processos</h3>
            <p>Aplicação do olhar psicológico e estratégico na organização de fluxos, comunicação e melhoria contínua da rotina interna.</p>

            <div class="project-meta">
              <span>RH</span>
              <span>Processos</span>
              <span>Estratégia</span>
            </div>

            <ul class="project-points">
              <li><strong>Problema:</strong> gargalos operacionais e pouca fluidez.</li>
              <li><strong>Solução:</strong> estruturação de processos com visão humana.</li>
              <li><strong>Resultado:</strong> mais alinhamento, clareza e eficiência.</li>
            </ul>
          </article>
        </div>
      </div>
    </section>

    <section class="section" id="contato">
      <div class="container">
        <div class="card contact-shell reveal">
          <div class="contact-grid">
            <div class="contact-intro">
              <div class="eyebrow">contato</div>
              <h2 class="section-title">Vamos conversar</h2>
              <p>
                Venha construir conosco uma solução pensada com profundidade, estética profissional e impacto real na sua operação.
              </p>
              <a href="https://wa.me/5518996853097" class="btn btn-primary" target="_blank" rel="noreferrer">Entrar em contato</a>
            </div>

            <div class="contact-list">
              <div class="contact-item">
                <strong>Email</strong>
                <a href="mailto:hefesto@outlook.com">hefesto@outlook.com</a>
              </div>

              <div class="contact-item">
                <strong>LinkedIn</strong>
                <div class="contact-links">
                  <a href="https://www.linkedin.com/in/ka-ito/" target="_blank" rel="noreferrer">linkedin.com/in/ka-ito</a>
                  <a href="https://www.linkedin.com/in/victoria-sarti/" target="_blank" rel="noreferrer">linkedin.com/in/victoria-sarti</a>
                </div>
              </div>

              <div class="contact-item">
                <strong>GitHub</strong>

              <div class="contact-links"> 
                <a href="https://github.com/K4-it0" target="_blank" rel="noreferrer">github.com/K4-it0</a>
                             
                <a href="https://github.com/VictoriaCaroline" target="_blank" rel="noreferrer">github.com/VictoriaCaroline</a>
                             
              </div>

            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-shell">
      <img src="icone-hefesto.png" alt="Ícone Hefesto" class="footer-icon">
      <p>© 2026 Hefesto Soluções. Todos os direitos reservados.</p>
    </div>
  </footer>

  <script>
    const navToggle = document.getElementById('navToggle');
    const navLinks = document.getElementById('navLinks');
    const navItems = document.querySelectorAll('.nav-links a');

    navToggle.addEventListener('click', () => {
      navLinks.classList.toggle('open');
    });

    navItems.forEach(item => {
      item.addEventListener('click', () => navLinks.classList.remove('open'));
    });

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, { threshold: 0.12 });

    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
  </script>
</body>
</html>
