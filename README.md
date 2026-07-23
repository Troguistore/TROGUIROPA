<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TROGÜI</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500;600;700;800;900&family=Nunito:wght@400;600;700;800;900&display=swap" rel="stylesheet">
<style>
:root{
  --orange:#FF5200;
  --dark:#1a1a2e;
  --green:#00b050;
  --red:#e00;
  --gray:#555;
  --border:#e8e8e8;
  --shadow:0 4px 24px rgba(0,0,0,.10);
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:'Nunito',sans-serif;background:#faf9f7;color:var(--dark);font-size:19px;line-height:1.6}
a{text-decoration:none;color:inherit}
img{max-width:100%;display:block}
button{font-family:'Nunito',sans-serif;cursor:pointer}
h1,h2,h3{font-family:'Poppins',sans-serif}

/* TOPBAR */
.topbar{position:relative;overflow:hidden;background:var(--dark);color:#fff;text-align:center;padding:12px 14px;font-size:16px;font-weight:800}
.topbar-inner{display:inline-block;animation:swayTopbar 2.2s ease-in-out infinite}
@keyframes swayTopbar{
  0%,100%{transform:translateX(0)}
  25%{transform:translateX(-14px)}
  75%{transform:translateX(14px)}
}
.topbar::after{content:'';position:absolute;top:0;left:-60%;width:40%;height:100%;background:linear-gradient(120deg,transparent,rgba(255,255,255,.18),transparent);transform:skewX(-20deg);animation:shineMove 3.2s ease-in-out infinite}
.topbar span{color:var(--orange)}

/* HEADER */
header{background:#fff;box-shadow:0 2px 14px rgba(0,0,0,.08);position:sticky;top:0;z-index:900;padding:14px 16px}
.header-inner{max-width:1100px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;gap:14px;flex-wrap:wrap}
.logo-text{font-family:'Poppins',sans-serif;font-weight:900;font-size:32px;background:var(--orange);color:var(--dark);padding:4px 16px;border-radius:12px;letter-spacing:-1px}
.wa-btn-header{display:flex;align-items:center;gap:8px;background:#25D366;color:#fff;padding:14px 22px;border-radius:16px;font-weight:900;font-size:19px;box-shadow:0 4px 14px rgba(37,211,102,.35)}
.catalog-btn-header{display:flex;align-items:center;gap:8px;background:var(--orange);color:#fff;padding:14px 22px;border-radius:16px;font-weight:900;font-size:19px;box-shadow:0 4px 14px rgba(255,82,0,.35)}

/* HERO */
.hero{max-width:1100px;margin:0 auto;padding:30px 16px 10px;display:grid;grid-template-columns:1fr 1fr;gap:36px;align-items:start}
@media(max-width:820px){.hero{grid-template-columns:1fr}}

.gallery-main{background:#fff;border-radius:22px;box-shadow:var(--shadow);padding:16px;text-align:center}
.gallery-main img{width:100%;border-radius:16px;cursor:zoom-in;object-fit:cover;max-height:420px;margin:0 auto}
.gallery-thumbs{display:flex;gap:10px;margin-top:12px;justify-content:center;flex-wrap:wrap}
.gallery-thumbs img{width:70px;height:70px;object-fit:cover;border-radius:10px;border:3px solid transparent;cursor:pointer}
.gallery-thumbs img.active{border-color:var(--orange)}
.media-video{width:100%;border-radius:16px;margin-top:12px}

.info-box h1{font-size:clamp(26px,4vw,36px);font-weight:900;line-height:1.25;margin-bottom:10px;color:var(--dark)}
.stars-row{color:#f5c518;font-size:22px;margin-bottom:10px}
.stars-row span{color:var(--gray);font-size:17px;margin-left:8px;font-weight:700}

.price-box{background:#fff8f0;border:3px solid var(--orange);border-radius:20px;padding:20px;margin:16px 0}
.price-old{font-size:20px;color:#999;text-decoration:line-through;font-weight:700}
.price-new{font-size:46px;font-weight:900;color:var(--orange);line-height:1.1}
.price-off{display:inline-block;background:var(--orange);color:#fff;font-weight:900;font-size:15px;padding:5px 14px;border-radius:20px;margin-left:10px;vertical-align:middle}

.urgency-box{background:var(--dark);color:#fff;border-radius:18px;padding:16px 18px;margin:14px 0;display:flex;align-items:center;gap:14px;animation:pulseBox 1.6s infinite}
@keyframes pulseBox{0%,100%{box-shadow:0 0 0 0 rgba(255,82,0,.5)}50%{box-shadow:0 0 0 10px rgba(255,82,0,0)}}
.urgency-box .uicon{font-size:30px;animation:swing 1s infinite}
@keyframes swing{0%,100%{transform:rotate(-8deg)}50%{transform:rotate(8deg)}}
.urgency-text{font-size:16px;font-weight:700;color:#ffcda3}
.urgency-timer{font-size:28px;font-weight:900;color:#fff;letter-spacing:1px}

.trust-badges{display:flex;flex-direction:column;gap:10px;margin:16px 0}
.trust-badge{position:relative;overflow:hidden;display:flex;align-items:center;gap:12px;background:#f0fff4;border:2px solid var(--green);border-radius:14px;padding:12px 16px;font-weight:800;font-size:17px;color:#006630;animation:swaySide 2.4s ease-in-out infinite}
.trust-badge.b2{background:#fff8f0;border-color:var(--orange);color:#a53c00;animation-delay:.5s}
.trust-badge::after{content:'';position:absolute;top:0;left:-60%;width:50%;height:100%;background:linear-gradient(120deg,transparent,rgba(255,255,255,.75),transparent);transform:skewX(-20deg);animation:shineMove 2.6s ease-in-out infinite}
.trust-badge.b2::after{animation-delay:1.3s}
@keyframes swaySide{
  0%,100%{transform:translateX(0)}
  25%{transform:translateX(-8px)}
  75%{transform:translateX(8px)}
}
@keyframes shineMove{
  0%{left:-60%}
  50%{left:120%}
  100%{left:120%}
}

.btn-buy{width:100%;background:var(--orange);color:#fff;border:none;padding:22px;border-radius:18px;font-weight:900;font-size:24px;margin-top:8px;box-shadow:0 8px 24px rgba(255,82,0,.35);transition:.2s}
.btn-buy:hover{background:#e04800}
@keyframes shakeBtn{
  0%{transform:translateX(0) rotate(0)}
  15%{transform:translateX(-6px) rotate(-1.5deg)}
  30%{transform:translateX(6px) rotate(1.5deg)}
  45%{transform:translateX(-5px) rotate(-1deg)}
  60%{transform:translateX(5px) rotate(1deg)}
  75%{transform:translateX(-2px)}
  90%{transform:translateX(2px)}
  100%{transform:translateX(0)}
}
.btn-buy.shaking{animation:shakeBtn .65s ease-in-out}
.sub-note{text-align:center;font-size:15px;color:var(--gray);margin-top:10px;font-weight:700}

/* PROBLEM/SOLUTION */
.section{max-width:1100px;margin:0 auto;padding:44px 16px}
.section-title{text-align:center;font-size:clamp(26px,4vw,34px);font-weight:900;margin-bottom:8px}
.section-title span{color:var(--orange)}
.section-sub{text-align:center;color:var(--gray);font-size:18px;margin-bottom:30px}

.problem-solution{display:grid;grid-template-columns:1fr 1fr;gap:24px}
@media(max-width:700px){.problem-solution{grid-template-columns:1fr}}
.ps-card{border-radius:20px;padding:26px;box-shadow:var(--shadow)}
.ps-card.problem{background:#fff0f0;border:2px solid #ffb3b3}
.ps-card.solution{background:#f0fff4;border:2px solid #b3e6c4}
.ps-card h3{font-size:22px;margin-bottom:12px}
.ps-card.problem h3{color:#c00}
.ps-card.solution h3{color:#00873e}
.ps-card ul{padding-left:22px}
.ps-card li{margin-bottom:10px;font-size:18px}

/* BENEFITS */
.benefits-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:20px}
.benefit-card{background:#fff;border-radius:18px;padding:24px;text-align:center;box-shadow:var(--shadow)}
.benefit-card .bicon{font-size:44px;margin-bottom:10px}
.benefit-card h4{font-size:19px;margin-bottom:6px}
.benefit-card p{font-size:16px;color:var(--gray)}

/* DELIVERY CALC */
.delivery-wrap{max-width:560px;margin:0 auto;background:#fff;border-radius:20px;padding:26px;box-shadow:var(--shadow);text-align:center}
.delivery-wrap h3{font-size:22px;margin-bottom:10px}
.delivery-wrap input{width:100%;padding:16px;border:2.5px solid var(--border);border-radius:14px;font-size:18px;font-family:'Nunito',sans-serif;margin-bottom:12px;outline:none}
.delivery-wrap input:focus{border-color:var(--orange)}
.delivery-wrap button{background:var(--orange);color:#fff;border:none;padding:14px 30px;border-radius:14px;font-weight:900;font-size:18px}
.delivery-result{background:#f0fff4;border:2px solid var(--green);border-radius:12px;padding:14px;font-size:17px;font-weight:700;color:#006630;margin-top:14px;display:none}

/* REVIEWS */
.review-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:18px}
.review-card{background:#fff;border-radius:18px;padding:20px;box-shadow:var(--shadow)}
.review-top{display:flex;align-items:center;gap:12px;margin-bottom:8px}
.review-avatar{width:46px;height:46px;border-radius:50%;background:var(--orange);color:#fff;display:flex;align-items:center;justify-content:center;font-weight:900;font-size:19px;flex-shrink:0}
.review-name{font-weight:800;font-size:17px}
.review-city{font-size:14px;color:var(--gray)}
.review-stars{color:#f5c518;font-size:16px}
.review-text{font-size:17px;color:#333;margin-top:8px}

/* FINAL CTA */
.final-cta{background:linear-gradient(135deg,var(--dark),#2d2d55);color:#fff;border-radius:26px;padding:40px 24px;text-align:center;max-width:900px;margin:0 auto}
.final-cta h2{font-size:clamp(24px,4vw,32px);margin-bottom:10px}
.final-cta p{font-size:18px;color:#ddd;margin-bottom:22px}

/* NOTIFICATION */
.notif{position:fixed;bottom:100px;left:16px;right:16px;max-width:340px;background:var(--dark);color:#fff;padding:14px 18px;border-radius:16px;font-size:16px;font-weight:700;z-index:1200;display:none;box-shadow:0 6px 24px rgba(0,0,0,.35);animation:slideUp .4s}
@keyframes slideUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
.notif .nn{color:var(--orange)}

/* ORDER FORM */
.order-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.65);z-index:1300;align-items:center;justify-content:center;padding:14px}
.order-overlay.active{display:flex}
.order-form-box{background:#fff;border-radius:24px;max-width:520px;width:100%;max-height:94vh;overflow-y:auto;padding:26px;position:relative}
.order-trust-img{width:160px;max-width:50%;border-radius:12px;margin:0 auto 16px;display:block}
.form-title{font-size:24px;font-weight:900;margin-bottom:6px}
.form-prod{font-size:16px;color:var(--gray);margin-bottom:14px}
.form-price-show{background:#fff8f0;border:2.5px solid var(--orange);border-radius:14px;padding:14px;margin-bottom:18px;display:flex;justify-content:space-between;align-items:center}
.form-price-show .fprice{font-size:26px;font-weight:900;color:var(--orange)}
.form-price-show .fold{font-size:14px;text-decoration:line-through;color:#aaa}
.form-group{margin-bottom:16px}
.form-group label{font-weight:800;font-size:17px;display:block;margin-bottom:6px}
.req{color:var(--red)}
.form-group input,.form-group textarea,.form-group select{width:100%;padding:14px;border:2.5px solid var(--border);border-radius:12px;font-size:17px;font-family:'Nunito',sans-serif;outline:none;background:#fafafa}
.form-group input:focus,.form-group textarea:focus,.form-group select:focus{border-color:var(--orange);background:#fff}
.form-group textarea{resize:vertical;min-height:70px}
.form-hint{font-size:14px;color:var(--gray);margin-top:5px}
.btn-confirm{width:100%;background:var(--green);color:#fff;border:none;padding:18px;border-radius:16px;font-weight:900;font-size:19px;margin-top:8px}
.btn-cancel-f{width:100%;background:#eee;color:var(--dark);border:none;padding:14px;border-radius:14px;font-weight:800;font-size:16px;cursor:pointer;margin-top:10px}
.modal-close{position:absolute;top:14px;right:14px;background:var(--dark);color:#fff;border:none;border-radius:50%;width:38px;height:38px;font-size:20px;cursor:pointer;display:flex;align-items:center;justify-content:center}

/* LIGHTBOX */
.lightbox-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.92);z-index:3000;align-items:center;justify-content:center;padding:20px;cursor:zoom-out}
.lightbox-overlay.active{display:flex}
.lightbox-overlay img{max-width:100%;max-height:100%;border-radius:12px}

/* ADMIN */
.admin-btns{position:fixed;bottom:16px;right:16px;z-index:1100}
.admin-btn{width:28px;height:28px;border-radius:50%;border:none;font-weight:900;font-size:12px;cursor:pointer;opacity:.3;background:var(--dark);color:#fff}
.admin-btn:hover{opacity:1}
.admin-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.65);z-index:2000;align-items:flex-start;justify-content:center;padding:16px;overflow-y:auto}
.admin-overlay.active{display:flex}
.admin-panel{background:#fff;border-radius:22px;max-width:800px;width:100%;margin:20px auto;padding:26px;position:relative;max-height:90vh;overflow-y:auto}
.admin-panel h2{font-size:22px;font-weight:900;color:var(--orange);margin-bottom:18px}
.admin-tabs{display:flex;gap:8px;margin-bottom:18px;flex-wrap:wrap}
.admin-tab-btn{background:#eee;border:none;padding:9px 16px;border-radius:10px;font-weight:800;font-size:13px;cursor:pointer}
.admin-tab-btn.active{background:var(--orange);color:#fff}
.admin-group{border:1.5px solid var(--border);border-radius:13px;padding:16px;margin-bottom:14px}
.admin-group label{font-weight:800;font-size:14px;display:block;margin-bottom:6px;margin-top:10px}
.admin-group input,.admin-group textarea,.admin-group select{width:100%;padding:9px 12px;border:1.5px solid var(--border);border-radius:9px;font-size:13px;font-family:'Nunito',sans-serif}
.admin-row2{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.btn-save-admin{background:var(--green);color:#fff;border:none;padding:10px 20px;border-radius:10px;font-weight:800;cursor:pointer;margin-top:10px}
.img-preview{width:70px;height:70px;object-fit:cover;border-radius:8px;border:2px solid var(--border);margin:4px}
.admin-review-item{border:1.5px solid var(--border);border-radius:11px;padding:12px;margin-bottom:10px;display:grid;gap:6px}

.wa-float{position:fixed;bottom:20px;right:20px;background:#25D366;color:#fff;width:64px;height:64px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:32px;box-shadow:0 4px 20px rgba(0,0,0,.3);z-index:1000;animation:pulseWa 1.8s infinite}
@keyframes pulseWa{0%,100%{transform:scale(1)}50%{transform:scale(1.08)}}

footer{background:var(--dark);color:#fff;padding:34px 16px;text-align:center;margin-top:30px}
footer .flogo{font-size:28px;font-weight:900;color:var(--orange);margin-bottom:8px}
footer p{font-size:15px;color:#bbb}
</style>
</head>
<body>

<div class="topbar"><span class="topbar-inner">🇨🇴 Envío <span>GRATIS</span> a toda Colombia &nbsp;|&nbsp; 💵 Pago Contra Entrega</span></div>

<header>
  <div class="header-inner">
    <div class="logo-text">TROGÜI</div>
    <div style="display:flex;gap:10px;flex-wrap:wrap">
      <a href="https://troguistore.github.io/web/" target="_blank" class="catalog-btn-header">🛍️ Ver Catálogo</a>
      <a href="https://wa.me/573206572598" target="_blank" class="wa-btn-header">💬 Escríbenos: 320 657 2598</a>
    </div>
  </div>
</header>

<!-- NOTIFICATION -->
<div class="notif" id="notif-box"></div>

<!-- HERO -->
<div class="hero">
  <div>
    <div class="gallery-main">
      <img id="main-img" src="" alt="Quita Callos Eléctrico" onclick="openLightbox(this.src)" decoding="async" fetchpriority="high">
      <div class="gallery-thumbs" id="gallery-thumbs"></div>
      <video id="main-video" class="media-video" style="display:none" autoplay muted loop playsinline controls></video>
    </div>
  </div>
  <div class="info-box">
    <h1 id="prod-name">Quita Callos Eléctrico</h1>
    <div class="stars-row">⭐⭐⭐⭐⭐ <span id="prod-sold">+340 personas ya lo compraron</span></div>

    <div class="price-box">
      <div><span class="price-old" id="price-old">$139.000</span><span class="price-off" id="price-off">-65% OFF</span></div>
      <div class="price-new" id="price-new">$49.000</div>
      <div style="font-size:15px;color:var(--gray);font-weight:700;margin-top:4px">Precio final · sin costos escondidos</div>
    </div>

    <div class="urgency-box">
      <div class="uicon">⏰</div>
      <div>
        <div class="urgency-text">¡La promoción termina en!</div>
        <div class="urgency-timer" id="urgency-timer">00:59:59</div>
      </div>
    </div>

    <div class="trust-badges">
      <div class="trust-badge">🚚 <span>Envío GRATIS a toda Colombia</span></div>
      <div class="trust-badge b2">💵 <span>Pagas cuando lo recibes en tu casa</span></div>
    </div>

    <button class="btn-buy" id="btn-buy-main" onclick="openOrderForm()">🔥 ¡QUIERO EL MÍO AHORA!</button>
    <div class="sub-note">✅ Compra 100% segura · Sin tarjeta · Solo pagas al recibir</div>
  </div>
</div>

<!-- PROBLEM / SOLUTION -->
<div class="section">
  <h2 class="section-title">¿Le duelen los <span>pies</span> al caminar?</h2>
  <p class="section-sub">Miles de personas mayores de 40 años ya encontraron la solución</p>
  <div class="problem-solution">
    <div class="ps-card problem">
      <h3>😣 El problema</h3>
      <ul>
        <li>Los callos y durezas duelen al caminar o estar de pie.</li>
        <li>Cortar los callos con cuchilla es peligroso, sobre todo si tiene diabetes.</li>
        <li>Ir a la podóloga cada mes sale caro y toca pedir cita.</li>
        <li>Las cremas y parches no eliminan el callo de raíz.</li>
      </ul>
    </div>
    <div class="ps-card solution">
      <h3>✅ La solución</h3>
      <ul id="solution-list">
        <li>Elimina callos y durezas sin dolor, sin cuchillas ni riesgo de cortes.</li>
        <li>Se usa desde la comodidad de su casa, cuando usted quiera.</li>
        <li>Funciona con USB, no necesita pilas ni cables complicados.</li>
        <li>Incluye repuestos: le dura mucho tiempo.</li>
      </ul>
    </div>
  </div>
</div>

<!-- BENEFITS -->
<div class="section" style="background:#fff">
  <h2 class="section-title">Beneficios que va a <span>sentir</span></h2>
  <p class="section-sub">Pies suaves y sin dolor, como cuando era joven</p>
  <div class="benefits-grid" id="benefits-grid">
    <div class="benefit-card"><div class="bicon">🦶</div><h4>Pies suaves</h4><p>Elimina durezas y callos desde la raíz en pocos usos.</p></div>
    <div class="benefit-card"><div class="bicon">🔌</div><h4>Fácil de usar</h4><p>Se carga por USB, sin pilas, listo para usar en segundos.</p></div>
    <div class="benefit-card"><div class="bicon">🛡️</div><h4>Sin dolor ni cortes</h4><p>A diferencia de la cuchilla, no corta la piel ni sangra.</p></div>
    <div class="benefit-card"><div class="bicon">💰</div><h4>Ahorra dinero</h4><p>Se acabaron las citas mensuales con la podóloga.</p></div>
  </div>
</div>

<!-- DELIVERY CALC -->
<div class="section">
  <div class="delivery-wrap">
    <h3>📍 ¿A dónde le llega su pedido?</h3>
    <p style="font-size:15px;color:var(--gray);margin-bottom:14px">Escriba su ciudad o pueblo y le decimos cuándo le llega:</p>
    <input type="text" id="delivery-place" placeholder="Ejemplo: Ibagué, Tolima">
    <button onclick="calcDelivery()">Calcular mi entrega</button>
    <div class="delivery-result" id="delivery-result"></div>
  </div>
</div>

<!-- REVIEWS -->
<div class="section" style="background:#fff">
  <h2 class="section-title">Lo que dicen nuestras <span>clientas</span></h2>
  <p class="section-sub">Personas reales, resultados reales</p>
  <div class="review-grid" id="review-grid"></div>
</div>

<!-- FINAL CTA -->
<div class="section">
  <div class="final-cta">
    <h2>No siga aguantando el dolor de sus pies</h2>
    <p>Pídalo hoy mismo, pague solo cuando lo reciba en la puerta de su casa.</p>
    <button class="btn-buy" style="max-width:420px;margin:0 auto" onclick="openOrderForm()">🔥 ¡PEDIR AHORA!</button>
  </div>
</div>

<!-- LIGHTBOX -->
<div class="lightbox-overlay" id="lightbox-overlay" onclick="closeLightbox()">
  <img id="lightbox-img" src="">
</div>

<!-- ORDER FORM -->
<div class="order-overlay" id="order-overlay">
  <div class="order-form-box">
    <button class="modal-close" onclick="closeOrderForm()">✕</button>
    <img id="order-trust-img" class="order-trust-img" src="" alt="Transportadoras confiables">
    <h2 class="form-title">📋 Confirmar su Pedido</h2>
    <p class="form-prod" id="form-prod-name"></p>
    <div class="form-price-show" id="form-price-show"></div>
    <div class="form-group"><label>Nombre <span class="req">*</span></label><input type="text" id="f-nombre" placeholder="Su nombre completo"></div>
    <div class="form-group"><label>Apellido <span class="req">*</span></label><input type="text" id="f-apellido" placeholder="Su apellido"></div>
    <div class="form-group">
      <label>Departamento <span class="req">*</span></label>
      <select id="f-departamento">
        <option value="">-- Selecciona --</option>
        <option>Amazonas</option><option>Antioquia</option><option>Arauca</option><option>Atlántico</option>
        <option>Bolívar</option><option>Boyacá</option><option>Caldas</option><option>Caquetá</option>
        <option>Casanare</option><option>Cauca</option><option>Cesar</option><option>Chocó</option>
        <option>Córdoba</option><option>Cundinamarca</option><option>Guainía</option><option>Guaviare</option>
        <option>Huila</option><option>La Guajira</option><option>Magdalena</option><option>Meta</option>
        <option>Nariño</option><option>Norte de Santander</option><option>Putumayo</option><option>Quindío</option>
        <option>Risaralda</option><option>San Andrés y Providencia</option><option>Santander</option>
        <option>Sucre</option><option>Tolima</option><option>Valle del Cauca</option><option>Vaupés</option>
        <option>Vichada</option><option>Bogotá D.C.</option>
      </select>
    </div>
    <div class="form-group"><label>Ciudad o Municipio <span class="req">*</span></label><input type="text" id="f-ciudad" placeholder="Ej: Ibagué"></div>
    <div class="form-group">
      <label>Dirección <span class="req">*</span></label>
      <input type="text" id="f-direccion" placeholder="Calle, carrera, barrio... o dejar en oficina Interrapidísimo">
      <div class="form-hint">📦 Si prefiere, puede recogerlo en la oficina de Interrapidísimo de su ciudad, solo escríbalo aquí.</div>
    </div>
    <div class="form-group"><label>Teléfono <span class="req">*</span></label><input type="tel" id="f-telefono" placeholder="Ej: 3001234567"></div>
    <div class="form-group"><label>Nota (opcional)</label><textarea id="f-nota" placeholder="Algún detalle adicional..."></textarea></div>
    <button class="btn-confirm" onclick="confirmOrder()">✅ Confirmar Pedido por WhatsApp</button>
    <button class="btn-cancel-f" onclick="closeOrderForm()">Cancelar</button>
  </div>
</div>

<!-- ADMIN R -->
<div class="admin-btns"><button class="admin-btn" onclick="adminAuth()">R</button></div>

<div class="admin-overlay" id="admin-r">
  <div class="admin-panel">
    <h2>✏️ Panel de Edición TROGÜI</h2>
    <div class="admin-tabs">
      <button class="admin-tab-btn active" onclick="showAdminTab('prod',this)">📦 Producto</button>
      <button class="admin-tab-btn" onclick="showAdminTab('media',this)">🖼️ Imágenes y Video</button>
      <button class="admin-tab-btn" onclick="showAdminTab('form',this)">📋 Formulario</button>
      <button class="admin-tab-btn" onclick="showAdminTab('page',this)">🎨 Página y Reseñas</button>
    </div>

    <div id="admin-tab-prod">
      <div class="admin-group">
        <label>Nombre del producto</label><input type="text" id="ap-name">
        <label>Descripción / Lista de "solución" (una línea por beneficio)</label><textarea id="ap-solution" rows="5"></textarea>
        <div class="admin-row2">
          <div><label>Precio real ($)</label><input type="number" id="ap-price"></div>
          <div><label>Precio anterior tachado ($)</label><input type="number" id="ap-oldprice"></div>
        </div>
        <div class="admin-row2">
          <div><label>Personas que lo compraron (texto)</label><input type="text" id="ap-sold"></div>
          <div><label>Minutos de la oferta (cronómetro)</label><input type="number" id="ap-timer-min"></div>
        </div>
        <button class="btn-save-admin" onclick="saveProductInfo()">💾 Guardar Producto</button>
      </div>
    </div>

    <div id="admin-tab-media" style="display:none">
      <div class="admin-group">
        <label>Imágenes (una URL por línea)</label>
        <textarea id="ap-images" rows="4"></textarea>
        <label>O suba fotos desde su galería</label>
        <input type="file" accept="image/*" multiple onchange="uploadProductImages(event)">
        <div id="ap-images-preview" style="margin-top:8px"></div>
      </div>
      <div class="admin-group">
        <label>Video o GIF (URL)</label>
        <input type="text" id="ap-video-url" placeholder="https://video.mp4 o .gif">
        <label>O suba un video/gif desde su galería</label>
        <input type="file" accept="video/*,image/gif" onchange="uploadProductVideo(event)">
        <div class="form-hint">El video se reproduce automáticamente en la página principal.</div>
        <button class="btn-save-admin" onclick="saveProductMedia()">💾 Guardar Imágenes y Video</button>
      </div>
    </div>

    <div id="admin-tab-form" style="display:none">
      <div class="admin-group">
        <label>Imagen de confianza (transportadoras) en el formulario</label>
        <input type="file" accept="image/*" onchange="uploadTrustImage(event)">
        <input type="text" id="trust-img-url" placeholder="https://imagen.jpg" style="margin-top:8px">
        <img id="trust-img-preview" class="img-preview" style="width:120px;height:auto;margin-top:8px" src="">
        <button class="btn-save-admin" onclick="saveTrustImage()">💾 Guardar imagen</button>
      </div>
    </div>

    <div id="admin-tab-page" style="display:none">
      <div class="admin-group">
        <label>Texto de la barra superior</label>
        <input type="text" id="edit-topbar">
        <button class="btn-save-admin" onclick="saveTopbar()">Guardar</button>
      </div>
      <div class="admin-group">
        <label>⭐ Editar Reseñas</label>
        <div id="admin-reviews-list"></div>
        <button class="btn-save-admin" onclick="saveReviews()">💾 Guardar Reseñas</button>
      </div>
    </div>

    <button onclick="closeAdmin()" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700;margin-top:16px">Cerrar</button>
  </div>
</div>

<a href="https://wa.me/573206572598" target="_blank" class="wa-float" title="WhatsApp">💬</a>

<footer>
  <div class="flogo">TROGÜI</div>
  <p>Tienda colombiana de confianza · Envíos a toda Colombia 🇨🇴</p>
  <p style="margin-top:8px">📞 320 657 2598 &nbsp;|&nbsp; 📦 Interrapidísimo · Coordinadora · Envia</p>
  <p style="margin-top:14px;color:#888;font-size:13px">© 2026 TROGÜI</p>
</footer>

<script>
const TRUST_IMG_DEFAULT = "data:image/jpeg;base64,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";

let product = JSON.parse(localStorage.getItem('trogui_callos_product') || 'null') || {
  name:'Quita Callos Eléctrico Recargable',
  price:49000,
  oldPrice:139000,
  sold:'+340 personas ya lo compraron',
  timerMinutes:60,
  images:[
    'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1707725/1773851515Callos.webp',
    'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1707725/1773851515callos%202.webp'
  ],
  video:'',
  solutionList:[
    'Elimina callos y durezas sin dolor, sin cuchillas ni riesgo de cortes.',
    'Se usa desde la comodidad de su casa, cuando usted quiera.',
    'Funciona con USB, no necesita pilas ni cables complicados.',
    'Incluye repuestos: le dura mucho tiempo.'
  ]
};

let reviews = JSON.parse(localStorage.getItem('trogui_callos_reviews') || 'null') || [
  {name:'Rosa Elena Gómez',city:'Ibagué',stars:5,text:'Ay que maravilla, me llego rapidito y de verdad si funciona, ya no me duelen los pies para caminar. Lo recomiendo mucho.'},
  {name:'María del Carmen Pérez',city:'Bogotá',stars:5,text:'Se lo compre a mi mama de 68 años y quedo encantada, dise que es facilisimo de usar. Gracias TROGUI.'},
  {name:'Gloria Inés Rodríguez',city:'Medellín',stars:5,text:'Excelente producto, muy buena calidad. Pague cuando me llego a la casa, todo perfecto.'},
  {name:'Aracely Muñoz',city:'Cali',stars:4,text:'Me gusto mucho, los callos que tenia hace años se me an ido quitando poco a poco. Muy contenta.'},
  {name:'Luz Marina Castañeda',city:'Bucaramanga',stars:5,text:'Sirve de verdad, ya se lo recomende a mis vecinas del barrio. Llegó bien empacadito.'},
  {name:'Consuelo Ramírez',city:'Pereira',stars:5,text:'Facilísimo de usar, no duele nada. Mis pies quedaron como de muchacha jaja gracias!'},
];

</script>
<script>
let timerInterval=null;

// ========== INIT ==========
document.addEventListener('DOMContentLoaded', ()=>{
  loadTopbar();
  renderProduct();
  renderReviews();
  startCountdown();
  startShakeLoop();
  startNotifications();
  document.getElementById('order-trust-img').src = localStorage.getItem('trogui_callos_trust_img') || TRUST_IMG_DEFAULT;
});

function fmt(n){ return Number(n).toLocaleString('es-CO'); }

function loadTopbar(){
  const tb=localStorage.getItem('trogui_callos_topbar');
  if(tb) document.querySelector('.topbar-inner').innerHTML=tb;
}

// ========== RENDER PRODUCT ==========
function renderProduct(){
  document.getElementById('prod-name').textContent=product.name;
  document.getElementById('prod-sold').textContent=product.sold;
  document.getElementById('price-old').textContent='$'+fmt(product.oldPrice);
  document.getElementById('price-new').textContent='$'+fmt(product.price);
  const disc=Math.round((1-product.price/product.oldPrice)*100);
  document.getElementById('price-off').textContent='-'+disc+'% OFF';

  document.getElementById('form-prod-name').textContent=product.name;
  document.getElementById('form-price-show').innerHTML=`
    <div><div style="font-size:13px;color:var(--gray);font-weight:700">Precio anterior:</div><div class="fold">$${fmt(product.oldPrice)}</div></div>
    <div style="text-align:right"><div style="font-size:13px;color:var(--gray);font-weight:700">Pagas al recibir:</div><div class="fprice">$${fmt(product.price)}</div></div>`;

  // solution list
  const solEl=document.getElementById('solution-list');
  solEl.innerHTML = product.solutionList.map(s=>`<li>${s}</li>`).join('');

  // gallery
  const imgs = product.images && product.images.length ? product.images : ['https://via.placeholder.com/500x400?text=TROGUI'];
  document.getElementById('main-img').src=imgs[0];
  const thumbs=document.getElementById('gallery-thumbs');
  thumbs.innerHTML=imgs.map((src,i)=>`<img src="${src}" loading="lazy" class="${i===0?'active':''}" onclick="setMainImg(this,'${src.replace(/'/g,"\\'")}')" onerror="this.style.display='none'">`).join('');

  // video
  const videoEl=document.getElementById('main-video');
  if(product.video){
    videoEl.src=product.video;
    videoEl.style.display='block';
  } else {
    videoEl.style.display='none';
  }
}
function setMainImg(el,src){
  document.querySelectorAll('.gallery-thumbs img').forEach(i=>i.classList.remove('active'));
  el.classList.add('active');
  document.getElementById('main-img').src=src;
}

// ========== LIGHTBOX ==========
function openLightbox(src){
  document.getElementById('lightbox-img').src=src;
  document.getElementById('lightbox-overlay').classList.add('active');
}
function closeLightbox(){
  document.getElementById('lightbox-overlay').classList.remove('active');
}

// ========== COUNTDOWN (con movimiento, oferta que "se acaba") ==========
function startCountdown(){
  if(timerInterval) clearInterval(timerInterval);
  let remaining = (product.timerMinutes||60)*60;
  function tick(){
    if(remaining<=0){ remaining=(product.timerMinutes||60)*60; }
    const h=Math.floor(remaining/3600);
    const m=Math.floor((remaining%3600)/60);
    const s=remaining%60;
    const pad=n=>String(n).padStart(2,'0');
    document.getElementById('urgency-timer').textContent=`${pad(h)}:${pad(m)}:${pad(s)}`;
    remaining--;
  }
  tick();
  timerInterval=setInterval(tick,1000);
}

// ========== SHAKE BUTTONS ==========
function startShakeLoop(){
  setInterval(()=>{
    const btns=document.querySelectorAll('.btn-buy');
    if(!btns.length) return;
    const btn=btns[Math.floor(Math.random()*btns.length)];
    btn.classList.remove('shaking');
    void btn.offsetWidth;
    btn.classList.add('shaking');
    setTimeout(()=>btn.classList.remove('shaking'),700);
  },2600);
}

// ========== DELIVERY CALC (texto libre) ==========
function calcDelivery(){
  const place=document.getElementById('delivery-place').value.trim();
  if(!place){ alert('Por favor escriba su ciudad o municipio'); return; }
  const date=new Date();
  date.setDate(date.getDate()+5);
  const dateStr=date.toLocaleDateString('es-CO',{weekday:'long',year:'numeric',month:'long',day:'numeric'});
  const el=document.getElementById('delivery-result');
  el.style.display='block';
  el.innerHTML=`📦 Su pedido a <strong>${place}</strong> llegaría aproximadamente el <strong>${dateStr}</strong> (entre 3 y 7 días hábiles).`;
}

// ========== REVIEWS ==========
function renderReviews(){
  const grid=document.getElementById('review-grid');
  grid.innerHTML = reviews.map(r=>`
    <div class="review-card">
      <div class="review-top">
        <div class="review-avatar">${r.name[0]}</div>
        <div><div class="review-name">${r.name}</div><div class="review-city">${r.city}</div></div>
      </div>
      <div class="review-stars">${'⭐'.repeat(r.stars)}</div>
      <div class="review-text">${r.text}</div>
    </div>`).join('');
}

// ========== ORDER FORM ==========
function openOrderForm(){
  document.getElementById('order-overlay').classList.add('active');
}
function closeOrderForm(){
  document.getElementById('order-overlay').classList.remove('active');
}
function confirmOrder(){
  const nombre=document.getElementById('f-nombre').value.trim();
  const apellido=document.getElementById('f-apellido').value.trim();
  const depto=document.getElementById('f-departamento').value.trim();
  const ciudad=document.getElementById('f-ciudad').value.trim();
  const direccion=document.getElementById('f-direccion').value.trim();
  const telefono=document.getElementById('f-telefono').value.trim();
  const nota=document.getElementById('f-nota').value.trim();
  if(!nombre||!apellido||!depto||!ciudad||!direccion||!telefono){
    alert('⚠️ Por favor complete todos los campos obligatorios.');return;
  }
  const disc=Math.round((1-product.price/product.oldPrice)*100);
  const msg=encodeURIComponent(
    `🛍️ *NUEVO PEDIDO - TROGÜI*\n\n📦 *Producto:* ${product.name}\n💰 *Precio:* $${fmt(product.price)} (-${disc}%)\n\n👤 *Cliente:* ${nombre} ${apellido}\n🗺️ *Departamento:* ${depto}\n🏙️ *Ciudad/Municipio:* ${ciudad}\n🏠 *Dirección:* ${direccion}\n📞 *Teléfono:* ${telefono}\n📝 *Nota:* ${nota||'Sin nota'}\n\n✅ Cliente confirma pago contra entrega`
  );
  closeOrderForm();
  window.open(`https://wa.me/573206572598?text=${msg}`,'_blank');
}

// ========== NOTIFICATIONS (cada 15 seg - 2 min, distintas ciudades) ==========
const notifPeople=[
  {name:'María Elena Suárez',city:'Ibagué'},{name:'Rosa Amparo Díaz',city:'Bogotá'},
  {name:'Gloria Inés Ramírez',city:'Medellín'},{name:'Consuelo Herrera',city:'Cali'},
  {name:'Luz Marina Gómez',city:'Barranquilla'},{name:'Aracely Torres',city:'Bucaramanga'},
  {name:'Blanca Cecilia Rojas',city:'Pereira'},{name:'Nubia Esperanza Peña',city:'Cartagena'},
  {name:'María del Carmen López',city:'Manizales'},{name:'Ofelia Castañeda',city:'Ibagué'},
  {name:'Fabiola Vargas',city:'Villavicencio'},{name:'Esperanza Moreno',city:'Neiva'},
  {name:'Alicia Fernández',city:'Armenia'},{name:'Marleny Ortiz',city:'Cúcuta'},
  {name:'Yolanda Salazar',city:'Popayán'},{name:'Doris Amaya',city:'Montería'},
  {name:'Teresa Reyes',city:'Tunja'},{name:'Miryam Guzmán',city:'Pasto'},
  {name:'Carlos Alberto Muñoz',city:'Santa Marta'},{name:'José Antonio Cárdenas',city:'Valledupar'},
];
let notifCount=0;
function startNotifications(){
  scheduleNextNotif();
}
function scheduleNextNotif(){
  let delay;
  if(notifCount===0) delay=7000;        // primera notificación a los 7 segundos
  else if(notifCount===1) delay=20000;  // segunda a los 20 segundos
  else delay = Math.random()*(120000-15000)+15000; // luego varía entre 15seg y 2min
  notifCount++;
  setTimeout(()=>{
    const person = notifPeople[Math.floor(Math.random()*notifPeople.length)];
    showNotif(`🛍️ <span class="nn">${person.name}</span> de ${person.city} acaba de comprar el <b>${product.name}</b>`);
    scheduleNextNotif();
  }, delay);
}
function showNotif(html){
  const nb=document.getElementById('notif-box');
  nb.innerHTML=html; nb.style.display='block';
  setTimeout(()=>nb.style.display='none',5500);
}

// ========== ADMIN (R) ==========
const ADMIN_PASS='43215';
function adminAuth(){
  const pass=prompt('🔐 Contraseña de administrador:');
  if(pass!==ADMIN_PASS){ if(pass!==null) alert('❌ Contraseña incorrecta'); return; }
  openAdminR();
}
function openAdminR(){
  document.getElementById('ap-name').value=product.name;
  document.getElementById('ap-solution').value=product.solutionList.join('\n');
  document.getElementById('ap-price').value=product.price;
  document.getElementById('ap-oldprice').value=product.oldPrice;
  document.getElementById('ap-sold').value=product.sold;
  document.getElementById('ap-timer-min').value=product.timerMinutes;
  document.getElementById('ap-images').value=product.images.join('\n');
  document.getElementById('ap-video-url').value=product.video||'';
  document.getElementById('ap-images-preview').innerHTML=product.images.map(src=>`<img src="${src}" class="img-preview" onerror="this.style.display='none'">`).join('');
  document.getElementById('edit-topbar').value=document.querySelector('.topbar-inner').innerHTML;
  document.getElementById('trust-img-preview').src=document.getElementById('order-trust-img').src;
  renderAdminReviews();
  document.getElementById('admin-r').classList.add('active');
}
function closeAdmin(){ document.getElementById('admin-r').classList.remove('active'); }
function showAdminTab(tab,btn){
  document.querySelectorAll('.admin-tab-btn').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  document.getElementById('admin-tab-prod').style.display = tab==='prod'?'block':'none';
  document.getElementById('admin-tab-media').style.display = tab==='media'?'block':'none';
  document.getElementById('admin-tab-form').style.display = tab==='form'?'block':'none';
  document.getElementById('admin-tab-page').style.display = tab==='page'?'block':'none';
}

function saveProductInfo(){
  product.name=document.getElementById('ap-name').value||product.name;
  product.solutionList=document.getElementById('ap-solution').value.split('\n').map(s=>s.trim()).filter(Boolean);
  product.price=parseInt(document.getElementById('ap-price').value)||product.price;
  product.oldPrice=parseInt(document.getElementById('ap-oldprice').value)||product.oldPrice;
  product.sold=document.getElementById('ap-sold').value||product.sold;
  product.timerMinutes=parseInt(document.getElementById('ap-timer-min').value)||product.timerMinutes;
  localStorage.setItem('trogui_callos_product',JSON.stringify(product));
  renderProduct();
  startCountdown();
  showFloatMsg('✅ Producto guardado');
}

function uploadProductImages(event){
  const files=event.target.files;
  if(!files.length) return;
  const ta=document.getElementById('ap-images');
  let pending=files.length;
  Array.from(files).forEach(file=>{
    const reader=new FileReader();
    reader.onload=e=>{
      ta.value = ta.value ? ta.value+'\n'+e.target.result : e.target.result;
      pending--;
      if(pending===0){
        const urls=ta.value.split('\n').map(u=>u.trim()).filter(Boolean);
        document.getElementById('ap-images-preview').innerHTML=urls.map(src=>`<img src="${src}" class="img-preview" onerror="this.style.display='none'">`).join('');
      }
    };
    reader.readAsDataURL(file);
  });
}
function uploadProductVideo(event){
  const file=event.target.files[0];
  if(!file) return;
  const reader=new FileReader();
  reader.onload=e=>{
    document.getElementById('ap-video-url').value=e.target.result;
    showFloatMsg('✅ Video/GIF cargado, recuerde guardar');
  };
  reader.readAsDataURL(file);
}
function saveProductMedia(){
  const urls=document.getElementById('ap-images').value.split('\n').map(u=>u.trim()).filter(Boolean);
  if(urls.length) product.images=urls;
  product.video=document.getElementById('ap-video-url').value.trim();
  localStorage.setItem('trogui_callos_product',JSON.stringify(product));
  renderProduct();
  showFloatMsg('✅ Imágenes y video guardados');
}

function uploadTrustImage(event){
  const file=event.target.files[0];
  if(!file) return;
  const reader=new FileReader();
  reader.onload=e=>{
    document.getElementById('trust-img-preview').src=e.target.result;
    document.getElementById('trust-img-preview').dataset.pending=e.target.result;
    document.getElementById('trust-img-url').value='';
  };
  reader.readAsDataURL(file);
}
function saveTrustImage(){
  const urlVal=document.getElementById('trust-img-url').value.trim();
  const pending=document.getElementById('trust-img-preview').dataset.pending;
  const finalSrc=urlVal||pending||document.getElementById('trust-img-preview').src;
  document.getElementById('order-trust-img').src=finalSrc;
  localStorage.setItem('trogui_callos_trust_img',finalSrc);
  showFloatMsg('✅ Imagen del formulario actualizada');
}

function saveTopbar(){
  const v=document.getElementById('edit-topbar').value;
  document.querySelector('.topbar-inner').innerHTML=v;
  localStorage.setItem('trogui_callos_topbar',v);
  showFloatMsg('✅ Guardado');
}

function renderAdminReviews(){
  document.getElementById('admin-reviews-list').innerHTML=reviews.map((r,i)=>`
    <div class="admin-review-item">
      <input type="text" id="rn-${i}" value="${r.name}" placeholder="Nombre">
      <input type="text" id="rc-${i}" value="${r.city}" placeholder="Ciudad">
      <select id="rs-${i}">${[1,2,3,4,5].map(s=>`<option value="${s}"${r.stars===s?' selected':''}>${s} ⭐</option>`).join('')}</select>
      <textarea id="rt-${i}" rows="2">${r.text}</textarea>
    </div>`).join('');
}
function saveReviews(){
  reviews=reviews.map((r,i)=>({
    name:document.getElementById('rn-'+i).value||r.name,
    city:document.getElementById('rc-'+i).value||r.city,
    stars:parseInt(document.getElementById('rs-'+i).value)||r.stars,
    text:document.getElementById('rt-'+i).value||r.text,
  }));
  localStorage.setItem('trogui_callos_reviews',JSON.stringify(reviews));
  renderReviews();
  showFloatMsg('✅ Reseñas guardadas');
}

function showFloatMsg(msg){
  const existing=document.querySelector('.float-msg-callos');
  if(existing) existing.remove();
  const div=document.createElement('div');
  div.className='float-msg-callos';
  div.style.cssText='position:fixed;bottom:100px;left:50%;transform:translateX(-50%);background:#1a1a2e;color:#fff;padding:12px 22px;border-radius:22px;font-weight:700;font-size:15px;z-index:9999;white-space:nowrap';
  div.textContent=msg;
  document.body.appendChild(div);
  setTimeout(()=>div.remove(),2800);
}

</script>
</body>
</html>
