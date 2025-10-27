<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Sitio web moderno, rápido y responsive para tu fábrica metalúrgica." />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

  <title>TREFCO - Industria Metalúrgica</title>

  <style>
    :root{
      --bg: #f5f5f5;
      --card: #ffffff;
      --primary: #0a3d62; /* Azul marino */
      --secondary: #E4E4E4;
      --accent: #083057; /* Azul más oscuro para hover */
      --text: #333;
      --radius: 12px;
      --shadow: 0 4px 20px rgba(0,0,0,0.15);
    }

    *{box-sizing:border-box; margin:0; padding:0;}
    body{
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height:1.6;
      text-align:center;
    }
    a{text-decoration:none; color:inherit;}
    header{
      position: sticky; top:0;
      background: rgba(255,255,255,0.95);
      padding: 12px 20px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      z-index: 50;
    }
    .container{max-width:1100px; margin:0 auto; padding:0 20px;}
    .nav{display:flex; justify-content: space-between; align-items: center;}
    .brand{font-weight:700; font-size:1.5rem; color: var(--primary);}
    .menu{display:flex; gap:20px; align-items:center;}
    .menu a:hover{color: var(--accent);}
    .burger{display:none; font-size:1.5rem; background:none; border:none; cursor:pointer;}
    main{padding: 60px 0;}
    section{padding:60px 0;}
    h1, h2{color: var(--primary);}
    h2{font-size:2rem; margin-bottom:20px;}
    .subtitle{color: #555;}
    .grid-3{display:grid; grid-template-columns:repeat(3,1fr); gap:20px;}
    .grid-4{display:grid; grid-template-columns:repeat(4,1fr); gap:20px;}
    .card{background: var(--card); padding:20px; border-radius: var(--radius); box-shadow: var(--shadow);}
    img{max-width:100%; border-radius: var(--radius);}
    .btn{padding:10px 16px; border-radius: var(--radius); font-weight:600; text-align:center; display:inline-block;}
    .btn-primary{background-color: var(--primary); color:#fff;}
    .btn-primary:hover{background-color: var(--accent);}
    footer{padding:20px 0; text-align:center; color:#777; border-top:1px solid #ddd;}

    /* Centrar secciones */
    #productos, 
    #acerca-de,
    #servicios {
      text-align: center;
    }
    #productos img {
      margin-top:20px;
      display:block;
      margin-left:auto;
      margin-right:auto;
    }
    ul { 
      list-style-position: inside; 
      padding-left: 0;
      text-align: left; 
      max-width: 600px;
      margin: 0 auto; 
    }

    .producto {
      display: inline-block;
      margin: 20px;
      text-align: center;
    }

    input, textarea {
      padding:10px;
      border-radius: var(--radius);
      border:1px solid #ccc;
      font-family:'Inter',sans-serif;
    }

    /* Responsive */
    @media(max-width:900px){
      .menu{display:none; flex-direction:column; gap:12px;}
      .burger{display:block;}
      .grid-3, .grid-4{grid-template-columns:1fr;}
      ul {text-align: center;}
    }
  </style>
</head>
<body>

<header class="container">
  <div class="nav">
    <div class="brand">TREFCO</div>
    <nav class="menu">
      <a href="#acerca-de">Acerca de nosotros</a>
      <a href="#servicios">Servicios</a>
      <a href="#productos">Productos</a>
      <a href="#contacto" class="btn btn-primary">Contacto</a>
    </nav>
    <button class="burger" id="burger">☰</button>
  </div>
</header>

<main class="container">
  <!-- Hero -->
  <section class="hero">
    <h1>Industria Metalúrgica TREFCO</h1>
    <p class="subtitle">Más de 25 años de experiencia en alambres, hilos y cuerdas de metales no ferrosos.</p>
    <div style="margin-top:20px;">
      <a class="btn btn-primary" href="#contacto">Solicitar presupuesto</a>
      <a class="btn" href="#productos">Ver productos</a>
    </div>
  </section>

  <!-- Acerca de -->
  <section id="acerca-de">
    <h2>Acerca de Nosotros</h2>
    <p>Emplazados en Avellaneda, Buenos Aires, somos especialistas en producción de alambres, hilos y cuerdas de cobre, aluminio y metales no ferrosos. Contamos con más de 25 años de trayectoria ofreciendo calidad y confianza a nuestros clientes y proveedores.</p>
    <img src="images/planta.jpg" alt="Planta industrial">
  </section>

  <!-- Productos -->
  <section id="productos">
    <h2>Productos</h2>
    <p class="subtitle">Nuestra gama incluye:</p>
    <ul>
      <li>Alambres redondos de cobre reciclado: Ø 0.30 mm hasta Ø 5.00 mm</li>
      <li>Alambres redondos de cobre electrolítico: Ø 0.20 mm hasta Ø 1.80 mm</li>
      <li>Alambres de aluminio puro / aleado: Ø 0.50 hasta Ø 5.20 mm</li>
      <li>Cuerdas de cobre de Ø 10 mm² a Ø 50 mm² en 7 hilos</li>
      <li>Cuerdas de aluminio de Ø 16 mm² a Ø 50 mm² en 7 hilos</li>
    </ul>
    <div class="grid-4" style="margin-top:20px;">
      <div class="card producto" title="Producto 1"></div>
      <div class="card producto" title="Producto 2"></div>
      <div class="card producto" title="Producto 3"></div>
      <div class="card producto" title="Producto 4"></div>
    </div>
  </section>

  <!-- Servicios -->
  <section id="servicios">
    <h2>Servicios</h2>
    <div class="grid-3">
      <div class="card">
        <h3>Fabricación</h3>
        <p>Producción de conductores, electrodos, alambres para cierres y más, adaptándonos a las necesidades de cada industria.</p>
      </div>
      <div class="card">
        <h3>Calidad y confianza</h3>
        <p>Productos bajo altos estándares, relaciones sólidas con clientes y compromiso con recursos humanos y medio ambiente.</p>
      </div>
      <div class="card">
        <h3>Trayectoria</h3>
        <p>Más de 25 años en el mercado garantizando experiencia, confianza y excelencia.</p>
      </div>
    </div>
  </section>

  <!-- Contacto -->
  <section id="contacto" class="container">
    <h2 style="color:var(--primary);">Contactate con nosotros</h2>
    <div style="display:flex; gap:40px; flex-wrap:wrap; justify-content:center; margin-top:30px;">
      <div style="flex:1; min-width:250px; text-align:left;">
        <p><strong>Mail:</strong> trefco@trefco.com.ar</p>
        <p><strong>Tel / Cel:</strong> 11 4201 4735 / 11 2649 0109</p>
        <p><strong>Horarios:</strong> 8 hs a 16 hs</p>
        <p><strong>Dirección:</strong> Dean Funes 450 / 52, Avellaneda</p>
      </div>

      <form id="contactForm" style="flex:1; min-width:250px; text-align:left;" novalidate>
        <input type="text" name="nombre" placeholder="Nombre" required style="width:100%; margin-bottom:10px;">
        <input type="email" name="email" placeholder="Email" required style="width:100%; margin-bottom:10px;">
        <input type="text" name="asunto" placeholder="Asunto" style="width:100%; margin-bottom:10px;">
        <textarea name="mensaje" placeholder="Cuéntanos sobre tu proyecto…" required style="width:100%; margin-bottom:10px;"></textarea>
        <button class="btn btn-primary" type="submit" style="width:100%;">Enviar</button>
        <p id="formMsg" class="subtitle"></p>
      </form>
    </div>
  </section>
</main>

<footer>
  © <span id="year"></span> TREFCO - Todos los derechos reservados.
</footer>

<script>
  document.getElementById('year').textContent = new Date().getFullYear();

  const burger = document.getElementById('burger');
  const nav = document.querySelector('.menu');
  burger?.addEventListener('click', ()=>{
    const open = nav.style.display === 'flex';
    nav.style.display = open ? 'none' : 'flex';
    nav.style.flexDirection = 'column';
    nav.style.gap = '12px';
  });

  const form = document.getElementById('contactForm');
  const msg = document.getElementById('formMsg');
  form.addEventListener('submit', (e)=>{
    e.preventDefault();
    const data = Object.fromEntries(new FormData(form).entries());
    if(!data.nombre || !data.email || !data.mensaje){
      msg.textContent = 'Por favor, completa los campos requeridos.';
      return;
    }
    msg.textContent = '¡Gracias! Tu mensaje ha sido enviado (demo).';
    form.reset();
  });
</script>

</body>
</html>




  
     


