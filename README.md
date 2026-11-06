
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Fisiología del Entrenamiento</title>

  <meta name="description" content="Fisiología del Entrenamiento: ciencia, conocimiento y aplicación al ejercicio y el rendimiento humano.">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --navy: #102b46;
      --blue: #176b87;
      --cyan: #43c3ca;
      --white: #ffffff;
      --light: #e0edf2;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      min-height: 100vh;
      font-family: 'DM Sans', sans-serif;
      background: var(--navy);
      color: var(--white);
    }

    .page {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      background:
        radial-gradient(circle at 80% 35%, rgba(67,195,202,.17), transparent 30%),
        linear-gradient(120deg, #102b46 0%, #12445e 55%, #176b87 100%);
      overflow: hidden;
      position: relative;
    }

    .page::before {
      content: "";
      position: absolute;
      width: 600px;
      height: 600px;
      border: 1px solid rgba(255,255,255,.09);
      border-radius: 50%;
      right: -220px;
      top: 10%;
      box-shadow:
        0 0 0 55px rgba(255,255,255,.025),
        0 0 0 110px rgba(255,255,255,.02);
      pointer-events: none;
    }

    header {
      width: min(1200px, 88%);
      margin: auto;
      padding: 28px 0;
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: relative;
      z-index: 2;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 13px;
      font-family: 'Manrope', sans-serif;
      font-weight: 800;
      letter-spacing: .5px;
      font-size: .95rem;
      line-height: 1.2;
    }

    .brand-icon {
      width: 43px;
      height: 43px;
      border: 1px solid rgba(255,255,255,.35);
      border-radius: 12px;
      display: grid;
      place-items: center;
      color: var(--cyan);
      font-size: 23px;
      font-weight: 800;
    }

    .header-label {
      color: #c3dbe4;
      font-size: .8rem;
      letter-spacing: 1.5px;
      text-transform: uppercase;
    }

    main {
      width: min(1200px, 88%);
      margin: auto;
      flex: 1;
      display: grid;
      grid-template-columns: 1.15fr .85fr;
      align-items: center;
      gap: 45px;
      padding: 55px 0 85px;
      position: relative;
      z-index: 1;
    }

    .eyebrow {
      color: #83e0df;
      font-size: .82rem;
      font-weight: 700;
      letter-spacing: 3px;
      text-transform: uppercase;
      margin-bottom: 24px;
    }

    h1 {
      font-family: 'Manrope', sans-serif;
      font-size: clamp(3rem, 6vw, 5.5rem);
      font-weight: 800;
      line-height: 1.04;
      letter-spacing: -3px;
      max-width: 760px;
      margin-bottom: 28px;
    }

    h1 span {
      color: #70d5d9;
    }

    .description {
      max-width: 650px;
      color: var(--light);
      font-size: clamp(1.05rem, 2vw, 1.25rem);
      line-height: 1.8;
      margin-bottom: 35px;
    }

    .keywords {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .keywords span {
      border: 1px solid rgba(255,255,255,.28);
      border-radius: 30px;
      padding: 8px 15px;
      color: #e2f3f5;
      font-size: .85rem;
    }

    .visual {
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 390px;
      position: relative;
    }

    .circle {
      width: min(350px, 85%);
      aspect-ratio: 1;
      border: 1px solid rgba(255,255,255,.25);
      border-radius: 50%;
      display: grid;
      place-items: center;
      position: relative;
      background: radial-gradient(circle, rgba(67,195,202,.2), transparent 68%);
      box-shadow: 0 0 90px rgba(67,195,202,.1);
    }

    .circle::before,
    .circle::after {
      content: "";
      position: absolute;
      inset: 25px;
      border: 1px solid rgba(255,255,255,.15);
      border-radius: 50%;
    }

    .circle::after {
      inset: 60px;
    }

    .symbol {
      font-size: 100px;
      z-index: 1;
      filter: drop-shadow(0 8px 25px rgba(0,0,0,.2));
    }

    .visual-caption {
      position: absolute;
      bottom: 15px;
      text-align: center;
      color: #c5e4e9;
      font-size: .8rem;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    footer {
      width: min(1200px, 88%);
      margin: auto;
      padding: 22px 0;
      border-top: 1px solid rgba(255,255,255,.17);
      color: #c0d6df;
      font-size: .82rem;
      position: relative;
      z-index: 2;
    }

    @media (max-width: 800px) {
      main {
        grid-template-columns: 1fr;
        text-align: center;
        padding-top: 65px;
        gap: 20px;
      }

      .description {
        margin-left: auto;
        margin-right: auto;
      }

      .keywords {
        justify-content: center;
      }

      .visual {
        min-height: 300px;
      }

      .circle {
        width: 260px;
      }

      .symbol {
        font-size: 78px;
      }

      h1 {
        letter-spacing: -1.5px;
      }

      .header-label {
        display: none;
      }
    }

    @media (max-width: 480px) {
      header, main, footer {
        width: 90%;
      }

      .brand {
        font-size: .82rem;
      }

      .eyebrow {
        font-size: .72rem;
      }

      .visual {
        min-height: 260px;
      }
    }
  </style>
</head>

<body>

  <div class="page">

    <header>
      <div class="brand">
        <div class="brand-icon">F</div>
        <div>FISIOLOGÍA DEL<br>ENTRENAMIENTO</div>
      </div>

      <div class="header-label">
        Ciencia · Formación · Aplicación
      </div>
    </header>

    <main>
      <div class="intro">

        <div class="eyebrow">
          Ciencia del ejercicio y rendimiento humano
        </div>

        <h1>
          Fisiología del
          <span>Entrenamiento.</span>
        </h1>

        <p class="description">
          Un espacio para comprender las respuestas y adaptaciones
          del organismo al ejercicio, analizar el entrenamiento
          desde la evidencia científica y conectar el conocimiento
          con su aplicación práctica.
        </p>

        <div class="keywords">
          <span>Fisiología del ejercicio</span>
          <span>Metodología del entrenamiento</span>
          <span>Evaluación del rendimiento</span>
        </div>

      </div>

      <div class="visual">
        <div class="circle">
          <div class="symbol">🫀</div>
        </div>

        <div class="visual-caption">
          Comprender · Analizar · Aplicar
        </div>
      </div>
    </main>

    <footer>
      Fisiología del Entrenamiento · Ciencia, formación y aplicación.
    </footer>

  </div>

</body>
</html>
