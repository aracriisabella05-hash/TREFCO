<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Sitio web moderno, rápido y responsive para tu fábrica metalúrgica." />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

  <title>TREFCO - Industria Metalúrgica</title>

  <style>
    :root {
      --bg: #f5f5f5;
      --card: #ffffff;
      --primary: #0a3d62; /* Azul marino */
      --secondary: #E4E4E4;
      --accent: #083057; /* Azul más oscuro para hover */
      --text: #333;
      --radius: 12px;
      --shadow: 0 4px 20px rgba(0,0,0,0.15);
    }

    * { box-sizing:border-box; margin:0; padding:0; }
    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height:1.6;
      text-align:center;
      overflow-x:hidden;
    }

    a { text-decoration:none; color:inherit; }

    header {
      position: sticky;
      top:0;
      background: rgba(255,255,255,0.95);
      padding: 12px 20px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      z-index: 50;
    }

    .container { max-width:1100px; margin:0 auto; padding:0 20px; }
    .nav { display:flex; justify-content: space-between; align-items: center; }
    .brand { font-weight:700; font-size:1.5rem; color: var(--primary); }
    .menu { display:flex; gap:20px; align-items:center; }
    .menu a:hover { color: var(--accent); }
    .burger { display:none; font-size:1.8rem; background:none; border:none; cursor:pointer; color: var(--primary); }

    main { padding: 60px 0; }
    section { padding:60px 0; }
    h1, h2 { color: var(--primary); }
    h2 { font-size:2rem; margin-bottom:20px; }
    .subtitle { color: #555; }
    .grid-3 { display:grid; grid-template-columns:repeat(3,1fr); gap:20px; }
    .grid-4 { display:grid; grid-template-columns:repeat(4,1fr); gap:20px; }
    .card { background: var(--card); padding:20px; border-radius: var(--radius); box-shadow: var(--shadow); }
    img { max-width:100%; border-radius: var(--radius); }
    .btn { padding:10px 16px; border-radius: var(--radius); font-weight:600; display:inline-block; }
    .btn-primary { background-color: var(--primary); color:#fff; }
    .btn-primary:hover { background-color: var(--accent); }
    footer { padding:20px 0; text-align:center; color:#777; border-top:1px solid #ddd; }

    /* Centrar secciones */
    #productos, #acerca-de, #servicios { text-align: center; }
    #productos img { margin-top:20px; display:block; margin-left:auto; margin-right:auto; }

    ul {
      list-style-position: inside;
      padding-left: 0;
      text-align: left;
      max-width: 600px;
      margin: 0 auto;
    }

    .producto { display: inline-block; margin: 20px; text-align: center; }

    input, textarea {
      padding:10px;
      border-radius: var(--radius);
      border:1px solid #ccc;
      font-family:'Inter',sans-serif;
    }

    /* ANIMACIONES */
    .section, .card, .hero-text {
      opacity: 0;
      transform: translateY(40px);
      transition: all 0.7s ease-out;
    }
    .visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* Responsive */
    @media(max-width:900px){
      .menu { display:none; flex-direction:column; gap:12px; }
      .burger { display:block; }
      .grid-3, .grid-4 { grid-template-columns:1fr; }
      ul { text-align: center; }
    }
  </style>
</head>

<body>

<header class="container">
  <div class="nav">
    <div class="brand">TREFCO</div>
    <nav class="menu">
      <a href="#acerca-de">Acerca de</a>
      <a href="#servicios">Servicios</a>
      <a href="#productos">Productos</a>
      <a href="#contacto" class="btn btn-primary">Contacto</a>
    </nav>
    <button class="burger" id="burger">☰</button>
  </div>
</header>

<main class="container">
  <section class="hero hero-text">
    <h1>Industria Metalúrgica TREFCO</h1>
    <p class="subtitle">Más de 25 años de experiencia en alambres, hilos y cuerdas de metales no ferrosos.</p>
    <div style="margin-top:20px;">
      <a class="btn btn-primary" href="#contacto">Solicitar presupuesto</a>
      <a class="btn" href="#productos">Ver productos</a>
    </div>
  </section>

  <section id="acerca-de" class="section">
    <h2>Acerca de Nosotros</h2>
    <p>Emplazados en Avellaneda, Buenos Aires, somos especialistas en producción de alambres, hilos y cuerdas de cobre, aluminio y metales no ferrosos. Contamos con más de 25 años de trayectoria ofreciendo calidad y confianza.</p>
    <img src="images/planta.jpg" alt="Planta industrial">
  </section>

  <section id="productos" class="section">
    <h2>Productos</h2>
    <ul>
      <li>Alambres de cobre reciclado: Ø 0.30 mm hasta Ø 5.00 mm</li>
      <li>Alambres de cobre electrolítico: Ø 0.20 mm hasta Ø 1.80 mm</li>
      <li>Alambres de aluminio puro / aleado: Ø 0.50 hasta Ø 5.20 mm</li>
      <li>Cuerdas de cobre de Ø 10 mm² a Ø 50 mm² en 7 hilos</li>
      <li>Cuerdas de aluminio de Ø 16 mm² a Ø 50 mm² en 7 hilos</li>
    </ul>
  </section>

  <section id="servicios" class="section">
    <h2>Servicios</h2>
    <div class="grid-3">
      <div class="card"><h3>Fabricación</h3><p>Producción adaptada a las necesidades de cada industria.</p></div>
      <div class="card"><h3>Calidad y confianza</h3><p>Normas IRAM y compromiso con el medio ambiente.</p></div>
      <div class="card"><h3>Trayectoria</h3><p>Más de 25 años garantizando experiencia y excelencia.</p></div>
    </div>
  </section>

  <section id="contacto" class="section">






  
     


