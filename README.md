<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Saft&Co | Servicios Financieros y Administrativos</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --primary-dark: #0f172a;
      --primary-blue: #1e40af;
      --secondary-blue: #3b82f6;
      --accent-green: #10b981;
      --accent-teal: #06b6d4;
      --light-bg: #f8fafc;
      --card-bg: #ffffff;
      --text-dark: #1e293b;
      --text-light: #64748b;
      --border-color: #e2e8f0;
      --shadow-sm: 0 2px 8px rgba(15, 23, 42, 0.08);
      --shadow-md: 0 4px 16px rgba(15, 23, 42, 0.12);
      --shadow-lg: 0 8px 24px rgba(15, 23, 42, 0.16);
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--light-bg);
      color: var(--text-dark);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* ===== HEADER ===== */
    header {
      background: linear-gradient(135deg, var(--primary-dark) 0%, #1a2d4a 100%);
      color: white;
      padding: 16px 40px;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: var(--shadow-md);
      backdrop-filter: blur(10px);
    }

    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      max-width: 1400px;
      margin: 0 auto;
      gap: 30px;
    }

    nav h1 {
      margin: 0;
      font-size: 26px;
      font-weight: 700;
      display: flex;
      align-items: center;
      gap: 12px;
      letter-spacing: -0.5px;
    }

    nav img {
      height: 45px;
      width: 45px;
      object-fit: contain;
      filter: drop-shadow(0 2px 4px rgba(255,255,255,0.1));
    }

    nav > div {
      font-size: 13px;
      font-weight: 500;
      letter-spacing: 1px;
      opacity: 0.9;
      text-transform: uppercase;
      color: var(--accent-teal);
    }

    /* ===== HERO SECTION ===== */
    .hero {
      background: linear-gradient(135deg, rgba(15,23,42,0.9) 0%, rgba(30,64,175,0.8) 100%), 
                  url('https://images.unsplash.com/photo-1554224154-22dec7ec8818?w=1400&h=600&fit=crop');
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
      color: white;
      padding: 140px 40px;
      text-align: center;
      min-height: 500px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: radial-gradient(circle at 20% 50%, rgba(59, 130, 246, 0.1) 0%, transparent 50%);
      pointer-events: none;
    }

    .hero > * {
      position: relative;
      z-index: 2;
    }

    .hero h2 {
      font-size: 48px;
      font-weight: 700;
      margin-bottom: 20px;
      letter-spacing: -1px;
      line-height: 1.2;
      animation: slideInDown 0.8s ease-out;
    }

    .hero p {
      font-size: 18px;
      max-width: 650px;
      opacity: 0.95;
      font-weight: 300;
      letter-spacing: 0.3px;
      margin: 0 auto;
      animation: slideInUp 0.8s ease-out 0.2s both;
    }

    /* ===== SECTIONS ===== */
    .section {
      padding: 80px 40px;
      max-width: 1400px;
      margin: 0 auto;
    }

    .section h2 {
      font-size: 36px;
      font-weight: 700;
      margin-bottom: 50px;
      color: var(--primary-dark);
      text-align: center;
      position: relative;
      letter-spacing: -0.5px;
    }

    .section h2::after {
      content: '';
      display: block;
      width: 60px;
      height: 4px;
      background: linear-gradient(90deg, var(--secondary-blue), var(--accent-teal));
      margin: 20px auto 0;
      border-radius: 2px;
    }

    .section p {
      font-size: 16px;
      line-height: 1.8;
      margin-bottom: 20px;
      color: var(--text-light);
    }

    /* ===== SERVICES GRID ===== */
    .services {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      margin-bottom: 40px;
    }

    .card {
      background: var(--card-bg);
      padding: 32px;
      border-radius: 16px;
      box-shadow: var(--shadow-sm);
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      border: 1px solid var(--border-color);
      position: relative;
      overflow: hidden;
    }

    .card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: linear-gradient(90deg, var(--secondary-blue), var(--accent-teal));
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.4s ease-out;
    }

    .card:hover {
      transform: translateY(-8px);
      box-shadow: var(--shadow-lg);
      border-color: var(--secondary-blue);
    }

    .card:hover::before {
      transform: scaleX(1);
    }

    .card h3 {
      margin-top: 0;
      font-size: 20px;
      font-weight: 600;
      color: var(--primary-dark);
      margin-bottom: 16px;
      letter-spacing: -0.3px;
    }

    .card p {
      margin: 0;
      font-size: 14px;
      color: var(--text-light);
      line-height: 1.7;
    }

    /* ===== IMAGE BANNERS ===== */
    .image-banner {
      width: 100%;
      height: auto;
      border-radius: 16px;
      margin-top: 40px;
      box-shadow: var(--shadow-md);
      display: block;
      object-fit: cover;
      transition: transform 0.6s ease-out;
    }

    .image-banner:hover {
      transform: scale(1.02);
    }

    /* ===== CONTACT SECTION ===== */
    .contact {
      background: linear-gradient(135deg, #f0f9ff 0%, #f0fdf4 100%);
      border-radius: 16px;
      padding: 40px;
      border-left: 5px solid var(--secondary-blue);
      position: relative;
      overflow: hidden;
    }

    .contact::before {
      content: '';
      position: absolute;
      top: -50%;
      right: -50%;
      width: 500px;
      height: 500px;
      background: radial-gradient(circle, rgba(59, 130, 246, 0.1) 0%, transparent 70%);
      pointer-events: none;
    }

    .contact > * {
      position: relative;
      z-index: 2;
    }

    .contact p {
      margin: 12px 0;
      font-size: 16px;
      color: var(--text-dark);
    }

    .contact strong {
      color: var(--primary-dark);
      font-weight: 600;
    }

    .whatsapp {
      display: inline-flex;
      align-items: center;
      margin-top: 20px;
      background: linear-gradient(135deg, var(--accent-green), #059669);
      color: white;
      padding: 14px 32px;
      border-radius: 10px;
      text-decoration: none;
      font-weight: 600;
      font-size: 15px;
      border: none;
      cursor: pointer;
      transition: all 0.3s ease;
      gap: 8px;
      box-shadow: 0 4px 12px rgba(16, 185, 129, 0.3);
    }

    .whatsapp::before {
      content: '💬';
      font-size: 18px;
    }

    .whatsapp:hover {
      background: linear-gradient(135deg, #059669, #047857);
      box-shadow: 0 8px 24px rgba(16, 185, 129, 0.4);
      transform: translateY(-2px);
    }

    /* ===== FOOTER ===== */
    footer {
      background: linear-gradient(135deg, var(--primary-dark) 0%, #1a2d4a 100%);
      color: white;
      text-align: center;
      padding: 30px 40px;
      margin-top: 60px;
      font-size: 14px;
      border-top: 1px solid rgba(255,255,255,0.1);
    }

    /* ===== ANIMATIONS ===== */
    @keyframes slideInDown {
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes slideInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* ===== RESPONSIVE DESIGN ===== */
    @media (max-width: 1024px) {
      .section {
        padding: 60px 30px;
      }

      .section h2 {
        font-size: 32px;
      }

      .hero {
        padding: 100px 30px;
        min-height: 400px;
      }

      .hero h2 {
        font-size: 40px;
      }
    }

    @media (max-width: 768px) {
      header {
        padding: 12px 20px;
      }

      nav {
        gap: 15px;
      }

      nav h1 {
        font-size: 22px;
      }

      nav > div {
        font-size: 11px;
      }

      .hero {
        padding: 80px 20px;
        min-height: 350px;
        background-attachment: scroll;
      }

      .hero h2 {
        font-size: 32px;
      }

      .hero p {
        font-size: 16px;
      }

      .section {
        padding: 50px 20px;
      }

      .section h2 {
        font-size: 28px;
        margin-bottom: 35px;
      }

      .services {
        grid-template-columns: 1fr;
        gap: 20px;
      }

      .card {
        padding: 24px;
      }

      .contact {
        padding: 30px 24px;
      }
    }

    @media (max-width: 480px) {
      nav {
        flex-direction: column;
        gap: 10px;
        text-align: center;
      }

      nav h1 {
        font-size: 20px;
        justify-content: center;
      }

      .hero h2 {
        font-size: 26px;
      }

      .hero p {
        font-size: 14px;
      }

      .section h2 {
        font-size: 24px;
      }

      .card h3 {
        font-size: 18px;
      }

      .whatsapp {
        width: 100%;
        justify-content: center;
      }
    }
  </style>
</head>
<body>

<header>
  <nav>
    <h1>
      <img src="logo.png" alt="Saft&Co logo">
      SAFT&CO
    </h1>
    <div>SOLUCIONES FINANCIERAS</div>
  </nav>
</header>

<section class="hero">
  <h2>Soluciones Contables, Tributarias y Financieras</h2>
  <p>Asesoría profesional, confiable y adaptada a las necesidades de cada organización y contribuyente. Transformamos desafíos administrativos en oportunidades de crecimiento.</p>
</section>

<section class="section">
  <h2>Servicios para Personas Naturales</h2>
  <div class="services">
    <div class="card">
      <h3>📋 Declaraciones y Anexos</h3>
      <p>Gestión integral de IVA, impuesto a la renta y anexos tributarios para profesionales y emprendedores. Cumplimiento normativo garantizado con el SRI.</p>
    </div>
    <div class="card">
      <h3>📊 Gestión Contable Mensual</h3>
      <p>Organización contable básica y avanzada. Cumplimiento de obligaciones con el SRI y generación de reportes financieros mensuales detallados.</p>
    </div>
    <div class="card">
      <h3>💰 Devoluciones y Trámites</h3>
      <p>Procesos de devolución de IVA y asesoría tributaria personalizada. Gestión completa de trámites administrativos ante entidades de control.</p>
    </div>
  </div>
  <img class="image-banner" src="https://images.unsplash.com/photo-1554224155-6726b3ff858f?w=1400&h=500&fit=crop" alt="Contabilidad">
</section>

<section class="section">
  <h2>Servicios para Empresas</h2>
  <div class="services">
    <div class="card">
      <h3>🏢 Contabilidad Empresarial</h3>
      <p>Contabilidad integral, elaboración de balances, cumplimiento tributario y reportes financieros profesionales para la toma de decisiones.</p>
    </div>
    <div class="card">
      <h3>⚖️ Asesoría Tributaria</h3>
      <p>Planificación fiscal estratégica, cumplimiento normativo actualizado y acompañamiento directo ante entidades de control y auditorías.</p>
    </div>
    <div class="card">
      <h3>👥 Gestión Laboral</h3>
      <p>Manejo profesional de nómina, IESS, Ministerio del Trabajo y procesos de finiquito. Cumplimiento laboral garantizado y actualizado.</p>
    </div>
    <div class="card">
      <h3>🎯 Constitución de Empresas</h3>
      <p>Creación de SAS, formalización empresarial completa y estructuración administrativa. Asesoría en selección del régimen tributario óptimo.</p>
    </div>
  </div>
  <img class="image-banner" src="https://images.unsplash.com/photo-1454165205744-3b78555e5572?w=1400&h=500&fit=crop" alt="Finanzas empresariales">
</section>

<section class="section">
  <h2>Consultoría Financiera</h2>
  <p>Evaluación económica profunda, análisis de negocios detallado, auditorías financieras y acompañamiento estratégico para la toma de decisiones empresariales informadas.</p>
  <img class="image-banner" src="https://images.unsplash.com/photo-1556740758-90de374c12ad?w=1400&h=500&fit=crop" alt="Consultoría financiera">
</section>

<section class="section">
  <h2>Planes y Precios</h2>
  <p>Los valores se establecen según el tipo de contribuyente, volumen de operaciones y necesidades específicas. Contamos con planes flexibles y personalizados para personas naturales, microempresas y compañías medianas. Solicita una evaluación gratuita de tu situación financiera.</p>
</section>

<section class="section">
  <h2>Contacto</h2>
  <div class="contact">
    <p><strong>📞 WhatsApp:</strong> +593 99 569 8547</p>
    <p><strong>⏰ Atención:</strong> Servicios contables, administrativos y financieros disponibles de lunes a viernes.</p>
    <a class="whatsapp" href="https://wa.me/593995698547" target="_blank">Contactar por WhatsApp</a>
  </div>
</section>

<footer>
  © 2026 Saft&Co | Servicios Financieros y Administrativos. Todos los derechos reservados.
</footer>

</body>
</html>

</body>
</html>
