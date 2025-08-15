## Hi there 👋
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Daniel — Portafolio</title>
  <meta name="description" content="Portafolio de Daniel: proyectos y habilidades en Python, Java y Bases de Datos." />
  <meta name="color-scheme" content="light dark" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0b0f19;
      --bg-soft: #11162a;
      --text: #e6e8ee;
      --muted: #aab1c5;
      --primary: #6aa1ff;
      --card: #0f1527;
      --accent: #7cf1c8;
      --border: #1f2742;
      --shadow: 0 10px 30px rgba(0,0,0,.25);
    }
    :root:has(body.light) {
      --bg: #f7f9fc; --bg-soft: #ffffff; --text: #0f172a; --muted: #475569; --primary: #2563eb; --card: #ffffff; --accent: #10b981; --border: #e2e8f0; --shadow: 0 10px 30px rgba(2,6,23,.08);
    }
    @media (prefers-color-scheme: light) {
      :root { --bg: #f7f9fc; --bg-soft: #ffffff; --text: #0f172a; --muted: #475569; --primary: #2563eb; --card: #ffffff; --accent: #10b981; --border: #e2e8f0; --shadow: 0 10px 30px rgba(2,6,23,.08); }
    }
    * { box-sizing: border-box }
    html, body { margin: 0; padding: 0 }
    body { font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans, Arial, "Apple Color Emoji", "Segoe UI Emoji"; background: var(--bg); color: var(--text); line-height: 1.6; }
    a { color: inherit; text-decoration: none }
    .container { max-width: 1100px; margin: 0 auto; padding: 0 1.2rem }
    header { position: sticky; top: 0; backdrop-filter: blur(10px); background: color-mix(in oklab, var(--bg) 80%, transparent); border-bottom: 1px solid var(--border); z-index: 50 }
    .nav { display: flex; align-items: center; justify-content: space-between; height: 64px }
    .brand { display: flex; align-items: center; gap: 10px; font-weight: 800; letter-spacing: .4px }
    .brand .logo { width: 32px; height: 32px; border-radius: 12px; background: linear-gradient(135deg, var(--primary), var(--accent)); box-shadow: var(--shadow) }
    .nav-links { display: flex; gap: 1rem; align-items: center }
    .nav-links a { padding: .5rem .75rem; border-radius: 10px; color: var(--muted); transition: .2s ease }
    .nav-links a:hover { color: var(--text); background: color-mix(in oklab, var(--primary) 12%, transparent) }
    .btn { display: inline-flex; align-items: center; gap: .5rem; background: linear-gradient(135deg, var(--primary), var(--accent)); color: #0b1020; font-weight: 700; padding: .7rem 1rem; border-radius: 14px; box-shadow: var(--shadow); border: 0; cursor: pointer }
    .btn.outline { background: transparent; color: var(--text); border: 1px solid var(--border) }

    /* Hero */
    .hero { padding: 72px 0 40px }
    .hero-grid { display: grid; grid-template-columns: 1.2fr .8fr; gap: 24px }
    .hero h1 { font-size: clamp(2rem, 3.8vw, 3.25rem); line-height: 1.1; margin: 0 0 12px }
    .hero p.lead { font-size: clamp(1rem, 1.5vw, 1.15rem); color: var(--muted); margin: 0 0 24px }
    .pill { display: inline-flex; gap: .5rem; align-items: center; padding: .4rem .7rem; border: 1px solid var(--border); border-radius: 999px; color: var(--muted); font-size: .9rem }
    .hero-card { background: var(--card); border: 1px solid var(--border); border-radius: 18px; padding: 18px; box-shadow: var(--shadow) }
    .stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; margin-top: 12px }
    .stat { background: var(--bg-soft); border: 1px solid var(--border); border-radius: 14px; padding: 14px; text-align: center }
    .stat h3 { margin: 0; font-size: 1.3rem }
    .stat p { margin: 4px 0 0; color: var(--muted); font-size: .9rem }

    /* Sections */
    section { padding: 40px 0 }
    .section-title { font-size: 1.6rem; margin-bottom: 18px }

    /* Skills */
    .skills { display: flex; flex-wrap: wrap; gap: 12px }
    .chip { border: 1px solid var(--border); background: var(--bg-soft); padding: .55rem .75rem; border-radius: 12px; font-weight: 600 }
    .chip small { color: var(--muted); font-weight: 500 }

    /* Projects */
    .grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 18px }
    .card { background: var(--card); border: 1px solid var(--border); border-radius: 18px; padding: 18px; box-shadow: var(--shadow); display: flex; flex-direction: column; gap: 12px }
    .card h3 { margin: 0 }
    .card p { margin: 0; color: var(--muted) }
    .card .links { display: flex; gap: 10px; margin-top: auto }

    /* Contact */
    .contact { display: grid; grid-template-columns: 1.2fr .8fr; gap: 18px }
    .contact .box { background: var(--card); border: 1px solid var(--border); border-radius: 18px; padding: 18px; box-shadow: var(--shadow) }

    footer { padding: 40px 0; color: var(--muted); border-top: 1px solid var(--border); margin-top: 40px }

    /* Responsive */
    @media (max-width: 920px) {
      .hero-grid, .contact { grid-template-columns: 1fr; }
      .grid { grid-template-columns: 1fr 1fr }
    }
    @media (max-width: 640px) {
      .nav-links { display: none }
      .grid { grid-template-columns: 1fr }
      .stats { grid-template-columns: 1fr 1fr }
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <a class="brand" href="#">
        <div class="logo" aria-hidden="true"></div>
        <span>Daniel</span>
      </a>
      <nav class="nav-links" aria-label="Principal">
        <a href="#sobre-mi">Sobre mí</a>
        <a href="#habilidades">Habilidades</a>
        <a href="#proyectos">Proyectos</a>
        <a href="#contacto">Contacto</a>
        <a class="btn outline" href="https://github.com/USUARIO" target="_blank" rel="noopener">GitHub</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <div class="hero-grid">
        <div>
          <span class="pill">🧑‍💻 Desarrollador en formación</span>
          <h1>Hola, soy Daniel.<br/>Construyo proyectos con <span style="background: linear-gradient(135deg, var(--primary), var(--accent)); -webkit-background-clip: text; background-clip: text; color: transparent">Python</span>, <span style="background: linear-gradient(135deg, var(--accent), var(--primary)); -webkit-background-clip: text; background-clip: text; color: transparent">Java</span> y <span style="background: linear-gradient(135deg, var(--primary), var(--accent)); -webkit-background-clip: text; background-clip: text; color: transparent">Bases de Datos</span>.</h1>
          <p class="lead">Me enfoco en resolver problemas reales con código limpio y buen diseño de datos. Aquí encontrarás una selección de mis proyectos, habilidades y formas de contacto.</p>
          <div style="display:flex; gap:10px; flex-wrap: wrap">
            <a class="btn" href="#proyectos">Ver proyectos</a>
            <a class="btn outline" href="#contacto">Contactar</a>
          </div>
        </div>
        <aside class="hero-card" aria-label="Resumen">
          <h3 style="margin: 0 0 8px">Resumen rápido</h3>
          <ul style="margin: 0; padding-left: 18px; color: var(--muted)">
            <li>Python (scripts, automatización, análisis básico)</li>
            <li>Java (POO, apps consola, fundamentos)</li>
            <li>SQL y modelado de datos</li>
          </ul>
          <div class="stats">
            <div class="stat">
              <h3>+10</h3>
              <p>Repos en GitHub</p>
            </div>
            <div class="stat">
              <h3>3</h3>
              <p>Stacks clave</p>
            </div>
            <div class="stat">
              <h3>100%</h3>
              <p>Aprendizaje continuo</p>
            </div>
          </div>
        </aside>
      </div>
    </section>

    <section id="sobre-mi">
      <h2 class="section-title">Sobre mí</h2>
      <p>
        Soy un entusiasta del desarrollo de software que disfruta convertir ideas en productos funcionales. Me interesa la calidad del código, el diseño de bases de datos y la creación de utilidades que mejoren la vida de las personas.
      </p>
      <p>
        Actualmente profundizo en estructuras de datos, patrones de diseño y buenas prácticas con <strong>Python</strong> y <strong>Java</strong>, además de <strong>SQL</strong> para consultas eficientes y modelado relacional.
      </p>
    </section>

    <section id="habilidades">
      <h2 class="section-title">Habilidades</h2>
      <div class="skills">
        <div class="chip">🐍 Python <small>• scripts, CLI, datos</small></div>
        <div class="chip">☕ Java <small>• POO, colecciones</small></div>
        <div class="chip">🗄️ Bases de Datos <small>• SQL, modelado</small></div>
        <div class="chip">🧰 Git & GitHub <small>• ramas, PRs</small></div>
        <div class="chip">🧪 Pruebas <small>• unitarias básicas</small></div>
        <div class="chip">🌐 HTML & CSS <small>• estáticos</small></div>
      </div>
    </section>

    <section id="proyectos">
      <h2 class="section-title">Proyectos destacados</h2>
      <div class="grid">
        <!-- Proyecto 1 -->
        <article class="card" aria-labelledby="p1-title">
          <h3 id="p1-title">ETL simple en Python</h3>
          <p>Script que extrae datos CSV, los transforma (limpieza y agregación) y los carga a una base SQLite. Incluye CLI y logs básicos.</p>
          <div class="links">
            <a class="btn outline" href="https://github.com/USUARIO/proyecto-etl" target="_blank" rel="noopener">Código</a>
            <a class="btn" href="#" aria-disabled="true">Demo</a>
          </div>
        </article>
        <!-- Proyecto 2 -->
        <article class="card" aria-labelledby="p2-title">
          <h3 id="p2-title">Gestor de tareas (Java)</h3>
          <p>Aplicación de consola con persistencia en archivos/SQLite, CRUD de tareas, filtros y exportación a CSV. Enfoque en POO.</p>
          <div class="links">
            <a class="btn outline" href="https://github.com/USUARIO/gestor-tareas-java" target="_blank" rel="noopener">Código</a>
            <a class="btn" href="#" aria-disabled="true">Demo</a>
          </div>
        </article>
        <!-- Proyecto 3 -->
        <article class="card" aria-labelledby="p3-title">
          <h3 id="p3-title">API de notas + SQL</h3>
          <p>API REST básica (Python/Flask) para notas con endpoints CRUD y base de datos relacional. Tests y documentación.</p>
          <div class="links">
            <a class="btn outline" href="https://github.com/USUARIO/api-notas" target="_blank" rel="noopener">Código</a>
            <a class="btn" href="#" aria-disabled="true">Demo</a>
          </div>
        </article>
      </div>
    </section>

    <section id="contacto" class="contact">
      <div class="box">
        <h2 class="section-title" style="margin-top:0">Contacto</h2>
        <p>¿Te interesa colaborar o tienes una propuesta? Escríbeme:</p>
        <p><strong>Email:</strong> <a id="email" href="mailto:tu.correo@ejemplo.com">tu.correo@ejemplo.com</a></p>
        <p><strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/USUARIO" target="_blank" rel="noopener">linkedin.com/in/USUARIO</a></p>
        <p><strong>GitHub:</strong> <a href="https://github.com/USUARIO" target="_blank" rel="noopener">github.com/USUARIO</a></p>
        <button class="btn outline" id="copiarEmail">Copiar email</button>
      </div>
      <div class="box" aria-label="CV">
        <h3 style="margin-top:0">CV / Resumen</h3>
        <p>Descarga mi CV actualizado:</p>
        <a class="btn" href="./cv.pdf" download>Descargar CV</a>
        <p style="color: var(--muted); margin-top: 10px">(Coloca tu archivo <code>cv.pdf</code> en el mismo repositorio.)</p>
      </div>
    </section>

    <footer class="container">
      <div style="display:flex; align-items:center; justify-content:space-between; gap:12px; flex-wrap: wrap">
        <small>© <span id="year"></span> Daniel. Hecho con ❤️ y café.</small>
        <div style="display:flex; gap:8px">
          <a class="chip" href="#sobre-mi">Arriba ↑</a>
          <button class="chip" id="toggleTheme" title="Cambiar tema">Tema</button>
        </div>
      </div>
    </footer>
  </main>

  <script>
    // Año dinámico
    document.getElementById('year').textContent = new Date().getFullYear();

    // Copiar email
    document.getElementById('copiarEmail').addEventListener('click', async () => {
      const email = document.getElementById('email').textContent.trim();
      try { await navigator.clipboard.writeText(email); alert('Email copiado: ' + email); } 
      catch { alert('No se pudo copiar, intenta manualmente.'); }
    });

    // Toggle tema (fuerza modo claro/oscuro)
    const toggleBtn = document.getElementById('toggleTheme');
    const body = document.body; 
    const THEME_KEY = 'theme-preference';
    function setTheme(mode){
      if(mode === 'light'){ body.classList.add('light'); }
      else { body.classList.remove('light'); }
      localStorage.setItem(THEME_KEY, mode);
    }
    const saved = localStorage.getItem(THEME_KEY);
    if(saved){ setTheme(saved); }
    toggleBtn.addEventListener('click', () => {
      const now = body.classList.contains('light') ? 'dark' : 'light';
      setTheme(now);
    });
  </script>
</body>
</html>
