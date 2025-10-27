<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>TREFCO - Metalúrgica y Trefilación de Cobre</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Montserrat", sans-serif; /* Asegúrate de tener esta fuente disponible o cámbiala */
    }

    body {
      color: #222;
      line-height: 1.6;
    }

    header {
      background: #111;
      color: #fff;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1.5rem 3rem;
    }

    header .logo h1 {
      margin-left: 10px;
      font-size: 1.8rem;
    }

    nav a {
      color: #fff;
      text-decoration: none;
      margin: 0 15px;
      font-weight: 500;
    }

    #hero {
      background: url("img/fondo-cobre.jpg") center/cover no-repeat;
      height: 80vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: white;
    }

    #hero .btn {
      display: inline-block;
      margin-top: 20px;
      background: #c47c39;
      padding: 12px 24px;
      color: #fff;
      border-radius: 5px;
      text-decoration: none;
    }

    .section {
      padding: 60px 20px;
      text-align: center;
    }

    .section.gray {
      background: #f5f5f5;
    }

    .productos-grid {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }

    .card {
      background: #fff;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      width: 300px;
      padding: 20px;
    }

    .card img {
      width: 100%;
      border-radius: 10px;
    }

    footer {
      background: #111;
      color: #fff;
      text-align: center;
      padding: 20px;
    }
    
    /* Nota: Faltaban los estilos responsive de la nav y la media query en tu CSS original. Los estilos de la nav se manejan con JavaScript en la parte final. */
  </style>

</head>
<body>
  <header>
    <div class="logo">
      <img src="img/logo.png" alt="Logo TREFCO" />
      <h1>TREFCO</h1>
      <p>Metalúrgica y Trefilación de Cobre</p>
    </div>
    <nav>
      <a href="#nosotros">Nosotros</a>
      <a href="#servicios">Servicios</a>
      <a href="#productos">Productos</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </header>

  <section id="hero">
    <div class="hero-text">
      <h2>Transformamos el cobre con precisión y calidad</h2>
      <p>Más de 20 años de experiencia en trefilación y metalurgia industrial.</p>
      <a href="#contacto" class="btn">Solicitá tu cotización</a>
    </div>
  </section>

  <section id="nosotros" class="section">
    <h2>Sobre Nosotros</h2>
    <p>En TREFCO nos especializamos en la trefilación y fabricación de productos derivados del cobre y sus aleaciones, garantizando estándares de calidad industrial y un servicio confiable para empresas del rubro eléctrico, automotriz y de manufactura.</p>
  </section>

  <section id="servicios" class="section gray">
    <h2>Servicios</h2>
    <ul>
      <li>Trefilado de cobre y bronce</li>
      <li>Corte a medida</li>
      <li>Desbobinado y rebobinado</li>
      <li>Asesoramiento técnico</li>
    </ul>
  </section>

  <section id="productos" class="section">
    <h2>Productos</h2>
    <div class="productos-grid">
      <div class="card">
        <img src="img/cobre1.jpg" alt="Alambre de cobre trefilado">
        <h3>Alambres trefilados</h3>
      </div>
      <div class="card">
        <img src="img/cobre2.jpg" alt="Barras de cobre">
        <h3>Barras de cobre</h3>
      </div>
      <div class="card">
        <img src="img/cobre3.jpg" alt="Tubos y piezas personalizadas">
        <h3>Piezas personalizadas</h3>
      </div>
    </div>
  </section>

  <section id="contacto" class="section gray">
    <h2>Contacto</h2>
    <p>📍 Parque Industrial Córdoba — Argentina</p>
    <p>📞 +54 9 351 123 4567</p>
    <p>📧 ventas@trefco.com</p>
    <form>
      <input type="text" placeholder="Nombre" required>
      <input type="email" placeholder="Email" required>
      <textarea placeholder="Mensaje"></textarea>
      <button type="submit">Enviar</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2025 TREFCO — Todos los derechos reservados</p>
  </footer>

  <script>
    // ================================
    // NAVBAR RESPONSIVE
    // ================================

    const nav = document.querySelector("nav");
    const menuBtn = document.createElement("div");
    menuBtn.classList.add("menu-btn");
    menuBtn.innerHTML = "&#9776;";
    nav.parentElement.insertBefore(menuBtn, nav);

    menuBtn.addEventListener("click", () => {
      nav.classList.toggle("active");
      menuBtn.classList.toggle("open");
    });

    // ================================
    // EFECTO DE SCROLL SUAVE
    // ================================

    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener("click", function(e) {
        e.preventDefault();
        document.querySelector(this.getAttribute("href")).scrollIntoView({
          behavior: "smooth"
        });
        if (nav.classList.contains("active")) {
          nav.classList.remove("active");
          menuBtn.classList.remove("open");
        }
      });
    });

    // ================================
    // ANIMACIONES AL HACER SCROLL (Código incompleto en el original)
    // Se ha omitido la función incompleta 'revealOnScroll' de tu archivo original para evitar errores. 
    // Si deseas agregar animaciones, deberás completar este código.
    // ================================
  </script>
</body>
</html>
