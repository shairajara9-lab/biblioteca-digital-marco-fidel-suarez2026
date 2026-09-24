<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Biblioteca Digital de la Institución Educativa Marco Fidel Suárez de Gualanday, Coello, Tolima.">
  <title>Biblioteca Digital | I.E. Marco Fidel Suárez</title>
  <style>
    :root{
      --primary:#173b6c;
      --primary-2:#245b9b;
      --accent:#e6b84a;
      --ink:#172033;
      --muted:#5f6b7a;
      --bg:#f5f7fb;
      --card:#ffffff;
      --line:#e4e8ef;
      --success:#2d7a59;
      --shadow:0 12px 35px rgba(23,59,108,.10);
      --radius:20px;
    }
    *{box-sizing:border-box;scroll-behavior:smooth}
    body{margin:0;font-family:Inter,Segoe UI,Arial,sans-serif;color:var(--ink);background:var(--bg);line-height:1.6}
    a{color:inherit}
    .topbar{background:var(--primary);color:#fff;text-align:center;padding:9px 18px;font-size:.9rem}
    header{position:sticky;top:0;z-index:50;background:rgba(255,255,255,.96);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
    .nav{max-width:1180px;margin:auto;padding:14px 20px;display:flex;align-items:center;justify-content:space-between;gap:20px}
    .brand{display:flex;align-items:center;gap:12px;text-decoration:none}
    .logo{width:48px;height:48px;border-radius:14px;background:linear-gradient(135deg,var(--primary),var(--primary-2));color:#fff;display:grid;place-items:center;font-weight:900;box-shadow:0 8px 20px rgba(23,59,108,.22)}
    .brand strong{display:block;font-size:1rem}.brand span{display:block;color:var(--muted);font-size:.78rem}
    nav{display:flex;gap:6px;flex-wrap:wrap;justify-content:flex-end}
    nav a{text-decoration:none;padding:9px 12px;border-radius:10px;font-weight:650;font-size:.92rem}
    nav a:hover{background:#edf3fb;color:var(--primary)}
    .hero{background:linear-gradient(135deg,#102d54 0%,#1c4e88 62%,#2e70a9 100%);color:#fff}
    .hero-inner{max-width:1180px;margin:auto;padding:76px 20px 72px;display:grid;grid-template-columns:1.35fr .65fr;gap:45px;align-items:center}
    .eyebrow{display:inline-flex;align-items:center;gap:8px;background:rgba(255,255,255,.12);border:1px solid rgba(255,255,255,.2);padding:7px 12px;border-radius:999px;font-size:.85rem}
    h1{font-size:clamp(2.5rem,6vw,4.7rem);line-height:1.02;margin:18px 0 20px;letter-spacing:-.04em}
    .hero p{font-size:1.1rem;max-width:720px;color:#e9f1fb}
    .actions{display:flex;gap:12px;flex-wrap:wrap;margin-top:28px}
    .btn{display:inline-flex;align-items:center;justify-content:center;gap:8px;text-decoration:none;border-radius:12px;padding:12px 17px;font-weight:800;border:1px solid transparent}
    .btn-light{background:#fff;color:var(--primary)}.btn-outline{border-color:rgba(255,255,255,.45);color:#fff;background:transparent}
    .hero-card{background:rgba(255,255,255,.1);border:1px solid rgba(255,255,255,.18);border-radius:24px;padding:25px;box-shadow:0 20px 50px rgba(0,0,0,.16)}
    .hero-card .big{font-size:3.2rem;font-weight:900;line-height:1}
    .hero-card p{font-size:.95rem;margin-bottom:0}
    section{max-width:1180px;margin:auto;padding:72px 20px}
    .section-head{display:flex;justify-content:space-between;gap:25px;align-items:end;margin-bottom:28px}
    .section-head h2{margin:0;font-size:2rem;letter-spacing:-.025em}.section-head p{margin:6px 0 0;color:var(--muted);max-width:700px}
    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
    .card{background:var(--card);border:1px solid var(--line);border-radius:var(--radius);padding:24px;box-shadow:var(--shadow)}
    .icon{width:45px;height:45px;border-radius:13px;background:#edf4fd;color:var(--primary);display:grid;place-items:center;font-size:1.35rem;margin-bottom:15px}
    .card h3{margin:0 0 8px}.card p{margin:0;color:var(--muted)}
    .about{display:grid;grid-template-columns:1fr 1fr;gap:20px}
    .facts{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-top:18px}
    .fact{padding:16px;background:#f8fafc;border:1px solid var(--line);border-radius:14px}
    .fact b{display:block;color:var(--primary);font-size:.82rem;text-transform:uppercase;letter-spacing:.05em}.fact span{font-weight:700}
    .searchbox{display:flex;gap:10px;margin:20px 0}
    input,select{width:100%;padding:13px 14px;border:1px solid #ccd4df;border-radius:12px;background:#fff;font:inherit;outline:none}
    input:focus,select:focus{border-color:var(--primary-2);box-shadow:0 0 0 3px rgba(36,91,155,.12)}
    .notice{padding:18px;border-left:4px solid var(--accent);background:#fffaf0;border-radius:0 14px 14px 0;color:#604b17}
    .catalog-empty{grid-column:1/-1;text-align:center;padding:42px;border:1px dashed #b9c5d4;background:#fff;border-radius:18px;color:var(--muted)}
    .steps{counter-reset:step}.step{position:relative;padding-left:58px}.step:before{counter-increment:step;content:counter(step);position:absolute;left:0;top:0;width:40px;height:40px;border-radius:50%;display:grid;place-items:center;background:var(--primary);color:#fff;font-weight:900}
    .contact{background:#102d54;color:#fff;border-radius:28px;padding:35px}.contact p{color:#dbe8f6}.contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:30px}
    footer{background:#0b1f3a;color:#c8d6e6;padding:28px 20px}.footer-inner{max-width:1180px;margin:auto;display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap;font-size:.88rem}
    footer a{color:#fff}
    .small{font-size:.85rem;color:var(--muted)}
    @media(max-width:850px){.hero-inner,.about,.contact-grid{grid-template-columns:1fr}.grid{grid-template-columns:1fr 1fr}nav{display:none}}
    @media(max-width:560px){.grid,.facts{grid-template-columns:1fr}.hero-inner{padding-top:55px}.section-head{display:block}}
  </style>
</head>
<body>
  <div class="topbar">I.E. Marco Fidel Suárez · Gualanday, Coello, Tolima</div>

  <header>
    <div class="nav">
      <a class="brand" href="#inicio" aria-label="Inicio Biblioteca Digital">
        <div class="logo">BD</div>
        <div><strong>Biblioteca Digital</strong><span>I.E. Marco Fidel Suárez</span></div>
      </a>
      <nav aria-label="Navegación principal">
        <a href="#inicio">Inicio</a>
        <a href="#biblioteca">Biblioteca</a>
        <a href="#categorias">Categorías</a>
        <a href="#institucion">Institución</a>
        <a href="#uso">Cómo usarla</a>
        <a href="#contacto">Contacto</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" id="inicio" style="max-width:none;padding:0">
      <div class="hero-inner">
        <div>
          <span class="eyebrow">📚 Aprender · Investigar · Crear</span>
          <h1>Tu espacio para aprender en línea.</h1>
          <p>Una propuesta de Biblioteca Digital para la comunidad educativa de la Institución Educativa Marco Fidel Suárez: un espacio organizado para consultar, descubrir y compartir recursos de apoyo académico.</p>
          <div class="actions">
            <a class="btn btn-light" href="#biblioteca">Explorar biblioteca</a>
            <a class="btn btn-outline" href="#institucion">Conocer la institución</a>
          </div>
        </div>
        <aside class="hero-card">
          <div class="big">24/7</div>
          <p>Acceso a la plataforma desde cualquier dispositivo con conexión a internet, sujeto a la disponibilidad de los recursos publicados por la institución.</p>
        </aside>
      </div>
    </section>

    <section id="biblioteca">
      <div class="section-head">
        <div>
          <h2>Biblioteca digital</h2>
          <p>Busca y organiza los recursos que quieras incorporar al catálogo institucional.</p>
        </div>
      </div>

      <div class="searchbox">
        <input id="search" type="search" placeholder="Buscar por título, autor o tema..." aria-label="Buscar recursos">
        <select id="category" aria-label="Filtrar por categoría">
          <option value="all">Todas las categorías</option>
          <option value="lenguaje">Lenguaje y literatura</option>
          <option value="matematicas">Matemáticas</option>
          <option value="ciencias">Ciencias</option>
          <option value="sociales">Ciencias sociales</option>
          <option value="tecnologia">Tecnología</option>
          <option value="ingles">Inglés</option>
        </select>
      </div>

      <div class="notice">
        <strong>Catálogo institucional:</strong> esta página no inventa libros ni enlaces. Los recursos deben ser agregados por la institución o por docentes autorizados, indicando título, autor, categoría y fuente.
      </div>

      <div class="grid" id="catalog" style="margin-top:20px">
        <div class="catalog-empty">
          <strong>Aún no hay recursos publicados en el catálogo.</strong>
          <p>Cuando la institución incorpore libros, guías, documentos o recursos educativos, aparecerán aquí y podrán filtrarse por categoría.</p>
        </div>
      </div>
    </section>

    <section id="categorias">
      <div class="section-head">
        <div>
          <h2>Áreas de consulta</h2>
          <p>Una organización sencilla para facilitar la búsqueda de material académico.</p>
        </div>
      </div>
      <div class="grid">
        <article class="card"><div class="icon">📖</div><h3>Lenguaje y literatura</h3><p>Lectura, escritura, literatura, comprensión textual y comunicación.</p></article>
        <article class="card"><div class="icon">➗</div><h3>Matemáticas</h3><p>Álgebra, geometría, estadística, razonamiento y resolución de problemas.</p></article>
        <article class="card"><div class="icon">🔬</div><h3>Ciencias</h3><p>Biología, química, física, ambiente y pensamiento científico.</p></article>
        <article class="card"><div class="icon">🌎</div><h3>Ciencias sociales</h3><p>Historia, geografía, ciudadanía, cultura y sociedad.</p></article>
        <article class="card"><div class="icon">💻</div><h3>Tecnología</h3><p>Informática, pensamiento computacional, innovación y herramientas digitales.</p></article>
        <article class="card"><div class="icon">🌐</div><h3>Inglés</h3><p>Comprensión, vocabulario, gramática y práctica comunicativa.</p></article>
      </div>
    </section>

    <section id="institucion">
      <div class="section-head">
        <div>
          <h2>Sobre la institución</h2>
          <p>Información institucional verificada en el sitio oficial de la I.E. Marco Fidel Suárez de Gualanday.</p>
        </div>
      </div>
      <div class="about">
        <article class="card">
          <h3>I.E. Marco Fidel Suárez</h3>
          <p>La institución está ubicada en el corregimiento de Gualanday, municipio de Coello, departamento del Tolima. Su sitio oficial identifica a la institución como pública y de población mixta, con jornada de mañana.</p>
          <div class="facts">
            <div class="fact"><b>Ubicación</b><span>Gualanday · Coello · Tolima</span></div>
            <div class="fact"><b>Carácter</b><span>Público</span></div>
            <div class="fact"><b>Población</b><span>Mixta</span></div>
            <div class="fact"><b>Jornada</b><span>Mañana</span></div>
          </div>
        </article>
        <article class="card">
          <h3>Propósito de la biblioteca</h3>
          <p>Facilitar el acceso organizado a recursos educativos digitales que apoyen las actividades de estudiantes y docentes, fomentando la lectura, la investigación, el uso responsable de la tecnología y el aprendizaje autónomo.</p>
          <p class="small" style="margin-top:18px"><strong>Nota:</strong> este propósito corresponde a la propuesta de esta página y no se presenta como la misión oficial de la institución.</p>
        </article>
      </div>
    </section>

    <section id="uso">
      <div class="section-head">
        <div>
          <h2>¿Cómo utilizarla?</h2>
          <p>Pasos sencillos para aprovechar el catálogo cuando existan recursos publicados.</p>
        </div>
      </div>
      <div class="grid steps">
        <article class="card step"><h3>Busca</h3><p>Escribe palabras relacionadas con el título, autor o tema que necesitas.</p></article>
        <article class="card step"><h3>Filtra</h3><p>Selecciona un área para encontrar recursos de una asignatura específica.</p></article>
        <article class="card step"><h3>Consulta</h3><p>Revisa la información del recurso y utiliza únicamente fuentes autorizadas.</p></article>
      </div>
    </section>

    <section id="contacto">
      <div class="contact">
        <div class="contact-grid">
          <div>
            <h2>Información de contacto</h2>
            <p>Para información institucional, trámites o recursos oficiales, consulta los canales publicados por la institución.</p>
          </div>
          <div>
            <p><strong>Dirección:</strong> Calle 1A No. 1-13, corregimiento de Gualanday, Coello, Tolima.</p>
            <p><strong>Correo:</strong> coello.iemarcofidelsuarez@sedtolima.edu.co</p>
            <p><strong>Atención:</strong> lunes a viernes</p>
            <a class="btn btn-light" href="https://marcofidelsuarezcoello.edu.co/" target="_blank" rel="noopener">Visitar sitio oficial ↗</a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="footer-inner">
      <div>© 2026 Biblioteca Digital · Propuesta web para la I.E. Marco Fidel Suárez</div>
      <div>Fuente institucional: <a href="https://marcofidelsuarezcoello.edu.co/" target="_blank" rel="noopener">marcofidelsuarezcoello.edu.co</a></div>
    </div>
  </footer>

  <script>
    // Buscador preparado para cuando se agreguen recursos al catálogo.
    const search = document.getElementById('search');
    const category = document.getElementById('category');
    const catalog = document.getElementById('catalog');

    function filterCatalog(){
      const q = search.value.toLowerCase().trim();
      const cards = [...catalog.querySelectorAll('[data-title]')];
      cards.forEach(card => {
        const matchesText = !q || card.dataset.title.toLowerCase().includes(q);
        const matchesCat = category.value === 'all' || card.dataset.category === category.value;
        card.style.display = matchesText && matchesCat ? '' : 'none';
      });
    }
    search.addEventListener('input', filterCatalog);
    category.addEventListener('change', filterCatalog);
  </script>
</body>
</html>
