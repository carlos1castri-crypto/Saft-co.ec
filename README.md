<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Saft&Co | Servicios Financieros y Administrativos</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Arial', Helvetica, sans-serif;
      background: #f5f7fa;
      color: #1f2933;
      line-height: 1.6;
    }

    header {
      background: #0f172a;
      color: white;
      padding: 20px 40px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }

    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      max-width: 1200px;
      margin: 0 auto;
    }

    nav h1 {
      margin: 0;
      font-size: 24px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    nav img {
      height: 40px;
      width: 40px;
      object-fit: contain;
    }

    .hero {
      background: linear-gradient(rgba(15,23,42,0.8), rgba(15,23,42,0.8)), 
                  url('https://images.unsplash.com/photo-1554224154-22dec7ec8818?w=1200&h=500&fit=crop');
      background-size: cover;
      background-position: center;
      color: white;
      padding: 100px 40px;
      text-align: center;
      min-height: 400px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }

    .hero h2 {
      font-size: 32px;
      margin-bottom: 20px;
      font-weight: bold;
    }

    .hero p {
      font-size: 18px;
      max-width: 700px;
    }

    .section {
      padding: 60px 40px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .section h2 {
      font-size: 28px;
      margin-bottom: 30px;
      color: #0f172a;
      text-align: center;
    }

    .section p {
      font-size: 16px;
      line-height: 1.8;
      margin-bottom: 20px;
    }

    .services {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
      margin-bottom: 30px;
    }

    .card {
      background: white;
      padding: 25px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.08);
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 20px rgba(0,0,0,0.12);
    }

    .card h3 {
      margin-top: 0;
      font-size: 20px;
      color: #0f172a;
      margin-bottom: 12px;
    }

    .card p {
      margin: 0;
      font-size: 14px;
      color: #4a5568;
    }

    .image-banner {
      width: 100%;
      height: auto;
      border-radius: 14px;
      margin-top: 30px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      display: block;
    }

    .contact {
      background: #e2e8f0;
      border-radius: 12px;
      padding: 30px;
      border-left: 4px solid #0f172a;
    }

    .contact p {
      margin: 10px 0;
      font-size: 16px;
    }

    .contact strong {
      color: #0f172a;
    }

    .whatsapp {
      display: inline-block;
      margin-top: 15px;
      background: #25D366;
      color: white;
      padding: 14px 24px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: bold;
      font-size: 16px;
      border: none;
      cursor: pointer;
      transition: background 0.3s;
    }

    .whatsapp:hover {
      background: #20ba5a;
    }

    footer {
      background: #0f172a;
      color: white;
      text-align: center;
      padding: 25px 20px;
      margin-top: 60px;
      font-size: 14px;
    }

    /* Responsive design */
    @media (max-width: 768px) {
      header {
        padding: 15px 20px;
      }

      nav {
        flex-direction: column;
        gap: 10px;
      }

      nav h1 {
        font-size: 20px;
      }

      .hero {
        padding: 60px 20px;
        min-height: 300px;
      }

      .hero h2 {
        font-size: 24px;
      }

      .hero p {
        font-size: 16px;
      }

      .section {
        padding: 40px 20px;
      }

      .section h2 {
        font-size: 24px;
      }

      .services {
        grid-template-columns: 1fr;
        gap: 20px;
      }

      .card {
        padding: 20px;
      }
    }

    @media (max-width: 480px) {
      nav h1 {
        font-size: 18px;
      }

      .hero h2 {
        font-size: 20px;
      }

      .section h2 {
        font-size: 20px;
      }

      .card h3 {
        font-size: 18px;
      }
    }
  </style>
</head>
<body>

<header>
  <nav>
    <h1>
      <img src="https://via.placeholder.com/40" alt="Saft&Co logo">
      Saft&Co
    </h1>
    <div>Servicios Financieros y Administrativos</div>
  </nav>
</header>

<section class="hero">
  <h2>Soluciones contables, tributarias y financieras para empresas y personas</h2>
  <p>Asesoría profesional, confiable y adaptada a las necesidades de cada organización y contribuyente.</p>
</section>

<section class="section">
  <h2>Servicios para Personas Naturales</h2>
  <div class="services">
    <div class="card">
      <h3>Declaraciones y Anexos</h3>
      <p>Gestión de IVA, impuesto a la renta y anexos tributarios para profesionales y emprendedores.</p>
    </div>
    <div class="card">
      <h3>Gestión Contable Mensual</h3>
      <p>Organización contable básica y cumplimiento de obligaciones con el SRI.</p>
    </div>
    <div class="card">
      <h3>Devoluciones y Trámites</h3>
      <p>Procesos de devolución de IVA y asesoría tributaria personalizada.</p>
    </div>
  </div>
  <img class="image-banner" src="https://images.unsplash.com/photo-1554224155-6726b3ff858f?w=1200&h=400&fit=crop" alt="Contabilidad">
</section>

<section class="section">
  <h2>Servicios para Empresas</h2>
  <div class="services">
    <div class="card">
      <h3>Contabilidad Empresarial</h3>
      <p>Contabilidad integral, elaboración de balances, cumplimiento tributario y reportes financieros.</p>
    </div>
    <div class="card">
      <h3>Asesoría Tributaria</h3>
      <p>Planificación fiscal, cumplimiento normativo y acompañamiento ante entidades de control.</p>
    </div>
    <div class="card">
      <h3>Gestión Laboral</h3>
      <p>Manejo de nómina, IESS, Ministerio del Trabajo y procesos de finiquito.</p>
    </div>
    <div class="card">
      <h3>Constitución de Empresas</h3>
      <p>Creación de SAS, formalización empresarial y estructuración administrativa.</p>
    </div>
  </div>
  <img class="image-banner" src="https://images.unsplash.com/photo-1454165205744-3b78555e5572?w=1200&h=400&fit=crop" alt="Finanzas empresariales">
</section>

<section class="section">
  <h2>Consultoría Financiera</h2>
  <p>Evaluación económica, análisis de negocios, auditorías y acompañamiento estratégico para la toma de decisiones.</p>
  <img class="image-banner" src="https://images.unsplash.com/photo-1556740758-90de374c12ad?w=1200&h=400&fit=crop" alt="Consultoría financiera">
</section>

<section class="section">
  <h2>Precios</h2>
  <p>Los valores se establecen según el tipo de contribuyente, volumen de operaciones y necesidades específicas. Contamos con planes flexibles para personas naturales, microempresas y compañías.</p>
</section>

<section class="section">
  <h2>Contacto</h2>
  <div class="contact">
    <p><strong>WhatsApp:</strong> 0995698547</p>
    <p><strong>Atención:</strong> Servicios contables, administrativos y financieros.</p>
    <a class="whatsapp" href="https://wa.me/593995698547" target="_blank">Contactar por WhatsApp</a>
  </div>
</section>

<footer>
  © 2026 Saft&Co | Servicios Financieros y Administrativos
</footer>

</body>
</html>
