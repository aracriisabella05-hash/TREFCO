<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Fábrica Metalúrgica — Sitio One‑Page</title>
  <meta name="description" content="Sitio web moderno, rápido y responsive para tu fábrica metalúrgica." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #0b0d12;
      --card: #11141a;
      --muted: #6b7280;
      --text: #e5e7eb;
      --brand: #7c3aed;
      --brand-2: #06b6d4;
      --ring: rgba(124,58,237,.3);
      --radius: 16px;
      --shadow: 0 10px 30px rgba(0,0,0,.35);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family:Inter,system-ui,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
      color:var(--text); background: radial-gradient(1200px 600px at 10% -10%, rgba(124,58,237,.25), transparent 60%),
                radial-gradient(900px 500px at 110% 10%, rgba(6,182,212,.18), transparent 60%),
                var(--bg);
      line-height:1.6;
    }
    a{color:inherit; text-decoration:none}
    .container{max-width:1100px; margin:0 auto; padding:0 20px}
    header{position:sticky; top:0; z-index:50; backdrop-filter:saturate(140%) blur(8px); background:rgba(11,13,18,.6); border-bottom:1px solid rgba(255,255,255,.06)}
    .nav{display:flex; align-items:center; justify-content:space-between; padding:14px 0}
    .brand{display:flex; gap:10px; align-items:center; font-weight:700}
    .badge{width:34px; height:34px; border-radius:10px; background:linear-gradient(135deg,var(--brand),var(--brand-2)); display:grid; place-items:center; box-shadow:var(--shadow)}
    .badge span{font-size:18px}
    .menu{display:flex; gap:18px; align-items:center}
    .menu a{opacity:.9}
    .menu a:hover{opacity:1}
    .cta{background:linear-gradient(135deg,var(--brand),var(--brand-2)); padding:10px 14px; border-radius:12px; font-weight:600; box-shadow:var(--shadow)}
    .burger{display:none; border:1px solid rgba(255,255,255,.1); border-radius:12px; padding:8px 10px}
    .hero{padding:80px 0 30px}
    .hero-grid{display:grid; grid-template-columns:1.1fr .9fr; gap:36px; align-items:center}
    .title{font-size:clamp(28px, 4.2vw, 56px); line-height:1.1; margin:0 0 14px; letter-spacing:-.02em}
    .subtitle{color:var(--muted); margin:0 0 24px}
    .actions{display:flex; gap:12px; flex-wrap:wrap}
    .btn{display:inline-flex; align-items:center; gap:8px; padding:12px 16px; border-radius:12px; font-weight:600; border:1px solid rgba(255,255,255,.12)}
    .btn-primary{background:linear-gradient(135deg,var(--brand),var(--brand-2)); border:none}
    .card{background:var(--card); border:1px solid rgba(255,255,255,.06); border-radius:var(--radius); padding:18px; box-shadow:var(--shadow)}
    .section{padding:60px 0}
    .section h2{font-size:clamp(22px, 3vw, 34px); margin:0 0 10px}
    .grid-3{display:grid; grid-template-columns:repeat(3, 1fr); gap:16px}
    .grid-4{display:grid; grid-template-columns:repeat(4, 1fr); gap:12px}
    .shot{aspect-ratio:4/3; border-radius:14px; background:linear-gradient(135deg,#1f2430,#151923); border:1px solid rgba(255,255,255,.06); position:relative; overflow:hidden}
    .shot::after{content:""; position:absolute; inset:0; background:radial-gradient(600px 200px at -20% -20%, rgba(124,58,237,.2), transparent 40%), radial-gradient(500px 160px at 120% -10%, rgba(6,182,212,.18), transparent 40%)}
    .about{display:grid; grid-template-columns:1fr 1fr; gap:24px}
    form{display:grid; gap:12px}
    input, textarea{background:#090c11; color:var(--text); border:1px solid rgba(255,255,255,.09); border-radius:12px; padding:12px}
    input:focus, textarea:focus{outline:2px solid var(--ring)}
    textarea{min-height:120px}
    footer{padding:26px 0; color:#9aa3b2; border-top:1px solid rgba(255,255,255,.06)}
    @media (max-width: 900px){.hero-grid{grid-template-columns:1fr}.grid-3{grid-template-columns:1fr}.grid-4{grid-template-columns:1fr 1fr}.about{grid-template-columns:1fr}.menu{display:none}.burger{display:inline-flex}}
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <a class="brand" href="#inicio">
        <div class="badge"><span>◆</span></div>
        <span>Fábrica Metalúrgica</span>
      </a>
      <nav class="menu">
        <a href="#productos">Productos</a>
        <a href="#servicios">Servicios</a>
        <a href="#acerca">Acerca de nosotros</a>
        <a href="#contacto" class="cta">Contacto</a>
      </nav>
      <button class="burger" id="burger">☰</button>
    </div>
  </header>

  <section class="hero container" id="inicio">
    <div class="hero-grid">
      <div>
        <h1 class="title">Soluciones metalúrgicas de calidad y precisión</h1>
        <p class="subtitle">Fabricamos productos a medida con tecnología de punta y experiencia comprobada.</p>
        <div class="actions">
          <a class="btn btn-primary" href="#contacto">Solicitar presupuesto</a>
          <a class="btn" href="#productos">Ver productos</a>
        </div>
      </div>
      <div class="card">
        <strong>Nuestros servicios incluyen:</strong>
        <ul>
          <li>Fabricación de piezas metálicas</li>
          <li>Tratamientos de superficie</li>
          <li>Diseño y prototipos</li>
          <li>Asesoramiento técnico</li>
        </ul>
      </div>
    </div>
  </section>

  <section class="section container" id="productos">
    <h2>Productos</h2>
    <p class="subtitle">Descubre nuestra gama de productos metalúrgicos.</p>
    <div class="grid-4">
      <div class="shot" title="Producto 1"></div>
      <div class="shot" title="Producto 2"></div>
      <div class="shot" title="Producto 3"></div>
      <div class="shot" title="Producto 4"></div>
    </div>
  </section>

  <section class="section container" id="servicios">
    <h2>Servicios</h2>
    <div class="grid-3">
      <div class="card">
        <h3>Fabricación</h3>
        <p>Producción de piezas según planos y especificaciones técnicas.</p>
      </div>
      <div class="card">
        <h3>Tratamientos</h3>
        <p>Acabados, galvanizados y tratamientos especiales para tus productos.</p>
      </div>
      <div class="card">
        <h3>Prototipos</h3>
        <p>Diseño, prototipado y validación de piezas antes de la producción masiva.</p>
      </div>
    </div>
  </section>

  <section class="section container about" id="acerca">
    <div>
      <h2>Acerca de nosotros</h2>
      <p>Somos una fábrica metalúrgica con años de experiencia, comprometidos con la calidad y la innovación en cada proyecto que emprendemos.</p>
    </div>
    <div class="card">
      <h3>Nuestra ventaja</h3>
      <ul>
        <li>Equipos modernos y especializados</li>
        <li>Entrega puntual y confiable</li>
        <li>Soporte técnico profesional</li>
      </ul>
    </div>
  </section>

  <section class="section container" id="contacto">
    <h2>Contacto</h2>
    <form id="contactForm" novalidate>
      <div class="grid-3" style="grid-template-columns:1fr 1fr; gap:12px">
        <input type="text" name="nombre" placeholder="Nombre" required />
        <input type="email" name="email" placeholder="Email" required />
      </div>
      <input type="text" name="asunto" placeholder="Asunto" />
      <textarea name="mensaje" placeholder="Cuéntanos sobre tu proyecto…" required></textarea>
      <button class="btn btn-primary" type="submit">Enviar</button>
      <p id="formMsg" class="subtitle"></p>
    </form>
  </section>

  <footer>
    <div class="container">© <span id="year"></span> Fábrica Metalúrgica. Todos los derechos reservados.</div>
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
      nav.style.padding = '12px 0';
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

