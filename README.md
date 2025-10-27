<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>TREFCO - Metalúrgica y Trefilación de Cobre</title>
  <link rel="stylesheet" href="style.css" />
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
    <p>© 2025 TREFCO — Todos los derechos reservados</p>
  </footer>
</body>
</html>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Montserrat", sans-serif;
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
// ================================
// NAVBAR RESPONSIVE
// ================================

const nav = document.querySelector("nav");
const menuBtn = document.createElement("div");
menuBtn.classList.add("menu-btn");
menuBtn.innerHTML = "☰";
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
// ANIMACIONES AL HACER SCROLL
// ================================

const elements = document.querySelectorAll(".section, .card, .hero-text");

function revealOnScroll() {
  const triggerBottom = window.innerHeight * 0.85;
  elements.forEach(el => {
    const boxTop = el.getBoundingClientRect().top;
    if (boxTop < triggerBottom) {
      el.classList.add("visible");
    } else {
      el.classList.remove("visible");
    }
  });
}

window.addEventListener("scroll", revealOnScroll);
revealOnScroll(); // correr al cargar

// ================================
// MENSAJE DE FORMULARIO (DEMO)
// ================================

const form = document.querySelector("form");
if (form) {
  form.addEventListener("submit", e => {
    e.preventDefault();
    alert("Gracias por contactarte con TREFCO. Te responderemos a la brevedad.");
    form.reset();
  });
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
/* ====== NAVBAR RESPONSIVE ====== */
.menu-btn {
  display: none;
  font-size: 2rem;
  cursor: pointer;
  color: white;
}

@media (max-width: 768px) {
  nav {
    display: none;
    flex-direction: column;
    background: #111;
    position: absolute;
    top: 70px;
    right: 0;
    width: 100%;
    text-align: center;
    padding: 10px 0;
  }

  nav.active {
    display: flex;
  }

  .menu-btn {
    display: block;
  }

  nav a {
    padding: 10px;
    border-top: 1px solid #222;
  }
}

/* ====== EFECTOS DE ANIMACIÓN ====== */
.section, .card, .hero-text {
  opacity: 0;
  transform: translateY(50px);
  transition: all 0.7s ease-out;
}

.visible {
  opacity: 1;
  transform: translateY(0);
}

<script src="script.js"></script>

  <footer>
    <p>© 2025 TREFCO — Todos los derechos reservados</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>


  
     


