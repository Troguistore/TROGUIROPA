<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TROGÜI - Tienda Colombia 🇨🇴</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800;900&family=Nunito:wght@400;600;700;800;900&display=swap" rel="stylesheet">
<style>
:root{
  --orange:#FF5200;
  --orange-light:#FF7A3D;
  --dark:#1a1a2e;
  --white:#fff;
  --light:#f5f5f5;
  --green:#00b050;
  --red:#e00;
  --gray:#666;
  --border:#e8e8e8;
  --shadow:0 4px 24px rgba(0,0,0,.10);
  --shadow-hover:0 12px 40px rgba(255,82,0,.18);
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:'Nunito',sans-serif;background:#f2f2f2;color:var(--dark);overflow-x:hidden}
a{text-decoration:none;color:inherit}
img{max-width:100%}
button{font-family:'Nunito',sans-serif}

/* TOPBAR */
.topbar{background:var(--dark);color:#fff;text-align:center;padding:8px 12px;font-size:13px;font-weight:700;letter-spacing:.3px;position:relative;overflow:hidden}
.topbar span{color:var(--orange)}
.topbar-scroll{display:inline-block;white-space:nowrap;animation:marquee 30s linear infinite}
@keyframes marquee{0%{transform:translateX(100vw)}100%{transform:translateX(-100%)}}

/* HEADER */
header{background:#fff;box-shadow:0 2px 16px rgba(0,0,0,.1);position:sticky;top:0;z-index:900}
.header-inner{max-width:1320px;margin:0 auto;display:flex;align-items:center;gap:14px;padding:10px 16px;flex-wrap:wrap}
.logo-area{min-width:150px}
.logo-img{height:50px;width:auto;object-fit:contain}
.search-bar{flex:1;min-width:200px;position:relative}
.search-bar input{width:100%;padding:11px 48px 11px 18px;border:2.5px solid var(--border);border-radius:30px;font-size:15px;font-family:'Nunito',sans-serif;outline:none;transition:.25s;background:#fafafa}
.search-bar input:focus{border-color:var(--orange);background:#fff;box-shadow:0 0 0 4px rgba(255,82,0,.08)}
.search-bar button{position:absolute;right:6px;top:50%;transform:translateY(-50%);background:var(--orange);border:none;border-radius:50%;width:36px;height:36px;color:#fff;cursor:pointer;font-size:16px;display:flex;align-items:center;justify-content:center;transition:.2s}
.search-bar button:hover{background:#e04800;transform:translateY(-50%) scale(1.08)}
.header-actions{display:flex;align-items:center;gap:10px;flex-wrap:wrap}
.wa-btn{display:flex;align-items:center;gap:6px;background:#25D366;color:#fff;padding:9px 16px;border-radius:22px;font-weight:800;font-size:13px;transition:.2s;white-space:nowrap}
.wa-btn:hover{background:#128C7E;transform:scale(1.04)}
.cart-btn{position:relative;background:var(--orange);color:#fff;border:none;border-radius:22px;padding:9px 18px;font-weight:800;font-size:14px;cursor:pointer;display:flex;align-items:center;gap:7px;transition:.2s}
.cart-btn:hover{background:#e04800;transform:scale(1.04)}
.cart-count{background:#fff;color:var(--orange);border-radius:50%;min-width:22px;height:22px;font-size:12px;font-weight:900;display:flex;align-items:center;justify-content:center;padding:0 4px}
.socials{display:flex;gap:6px}
.socials a{width:36px;height:36px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:18px;transition:.2s}
.socials a:hover{transform:scale(1.15)}
.socials a.ig{background:linear-gradient(45deg,#f09433,#e6683c,#dc2743,#cc2366,#bc1888);color:#fff}
.socials a.tk{background:#010101;color:#fff}
.socials a.wa{background:#25D366;color:#fff}

/* NAV */
nav{background:var(--orange);position:sticky;top:70px;z-index:800}
.nav-inner{max-width:1320px;margin:0 auto;display:flex;gap:0;overflow-x:auto;scrollbar-width:none}
.nav-inner::-webkit-scrollbar{display:none}
.nav-inner a{color:#fff;padding:13px 20px;font-weight:800;font-size:13.5px;white-space:nowrap;border-bottom:3px solid transparent;transition:.2s;display:flex;align-items:center;gap:5px}
.nav-inner a:hover,.nav-inner a.active{border-bottom-color:#fff;background:rgba(255,255,255,.15)}

/* SLIDER */
.slider-section{background:#fff}
.slider-wrap{position:relative;overflow:hidden;height:280px}
.slider-track{display:flex;transition:transform .75s cubic-bezier(.65,0,.35,1);height:100%}
.slide{min-width:100%;height:100%;display:flex;align-items:center;position:relative;overflow:hidden;background-size:220% 220%;animation:gradientDrift 9s ease-in-out infinite}
@keyframes gradientDrift{0%{background-position:0% 30%}50%{background-position:100% 70%}100%{background-position:0% 30%}}
.slide-1{background-image:linear-gradient(135deg,#1a1a2e 45%,#FF5200 100%)}
.slide-2{background-image:linear-gradient(135deg,#0d3b2e 45%,#00b050 100%)}
.slide-3{background-image:linear-gradient(135deg,#16213e 45%,#e94560 100%)}
.slide-content{color:#fff;padding:40px;z-index:2;max-width:600px;opacity:0;transform:translateY(22px) scale(.97);animation:none}
.slide.slide-visible .slide-content{animation:slideContentIn .75s cubic-bezier(.2,.7,.3,1) forwards}
@keyframes slideContentIn{0%{opacity:0;transform:translateY(26px) scale(.96)}60%{opacity:1}100%{opacity:1;transform:translateY(0) scale(1)}}
.slide-content h2{font-size:clamp(22px,4vw,44px);font-weight:900;line-height:1.15;font-family:'Poppins',sans-serif}
.slide-content h2 span{color:var(--orange);position:relative}
.slide-content p{font-size:15px;margin:10px 0 20px;opacity:.9;line-height:1.5}
.slide-btn{background:var(--orange);color:#fff;padding:13px 30px;border-radius:30px;font-weight:900;font-size:15px;display:inline-block;transition:.25s;border:2px solid transparent;box-shadow:0 6px 18px rgba(255,82,0,.35);animation:btnPulse 2.4s ease-in-out infinite}
@keyframes btnPulse{0%,100%{box-shadow:0 6px 18px rgba(255,82,0,.35)}50%{box-shadow:0 6px 26px rgba(255,82,0,.6)}}
.slide-btn:hover{background:transparent;border-color:#fff;transform:scale(1.06);animation-play-state:paused}
.slide-deco{position:absolute;right:0;top:0;height:100%;width:45%;opacity:.1;background:radial-gradient(circle at center,#fff 0%,transparent 70%);animation:decoFloat 6s ease-in-out infinite}
@keyframes decoFloat{0%,100%{transform:translateX(0) scale(1)}50%{transform:translateX(-14px) scale(1.06)}}

/* SLIDER PRODUCT SHOWCASE (rotates every 7s) */
.slider-showcase{position:absolute;right:6%;top:50%;transform:translateY(-50%);width:170px;height:170px;z-index:3;display:flex;align-items:center;justify-content:center}
.slider-showcase img{width:100%;height:100%;object-fit:cover;border-radius:20px;border:4px solid rgba(255,255,255,.9);box-shadow:0 16px 40px rgba(0,0,0,.35);opacity:0;transform:translateY(10px) scale(.94);transition:opacity .6s ease,transform .6s ease}
.slider-showcase img.show{opacity:1;transform:translateY(0) scale(1)}
.showcase-tag{position:absolute;bottom:-10px;right:-6px;background:var(--orange);color:#fff;font-weight:900;font-size:13px;padding:6px 12px;border-radius:20px;box-shadow:0 4px 12px rgba(0,0,0,.25);opacity:0;transition:opacity .6s ease}
.showcase-tag.show{opacity:1}
@media(max-width:800px){.slider-showcase{display:none}}

/* WHATSAPP ICON (official style) */
.wa-icon{width:16px;height:16px;flex-shrink:0}
.wa-icon-lg{width:26px;height:26px}

/* SHIPPING / TRANSPORTADORAS */
.shipping-section{background:linear-gradient(180deg,#fff 0%,#fff8f3 100%);padding:26px 16px;border-top:1px solid var(--border);border-bottom:1px solid var(--border)}
.shipping-inner{max-width:1100px;margin:0 auto;display:grid;grid-template-columns:1.4fr .6fr;gap:26px;align-items:center}
.shipping-text h2{font-family:'Poppins',sans-serif;font-weight:900;font-size:clamp(18px,2.2vw,24px);color:var(--dark);margin-bottom:8px;line-height:1.25}
.shipping-text h2 span{color:var(--orange)}
.shipping-text p{color:var(--gray);font-size:13.5px;line-height:1.55;margin-bottom:14px}
.carrier-badges{display:flex;flex-wrap:wrap;gap:9px}
.carrier-chip{display:flex;align-items:center;gap:7px;background:#fff;border:2px solid var(--border);border-radius:13px;padding:8px 14px;font-weight:800;font-size:12.5px;color:var(--dark);box-shadow:0 3px 10px rgba(0,0,0,.05);transition:.25s;animation:chipFloat 3.2s ease-in-out infinite}
.carrier-chip:nth-child(2){animation-delay:.3s}
.carrier-chip:nth-child(3){animation-delay:.6s}
@keyframes chipFloat{0%,100%{transform:translateY(0)}50%{transform:translateY(-5px)}}
.carrier-chip:hover{border-color:var(--orange);box-shadow:var(--shadow-hover);transform:translateY(-3px)}
.carrier-chip .cc-dot{width:8px;height:8px;border-radius:50%;background:var(--green);animation:blink 1.3s infinite}
.shipping-trust{margin-top:12px;display:inline-flex;align-items:center;gap:7px;background:#f0fff4;border:1px solid var(--green);color:#006630;font-weight:800;font-size:12px;padding:8px 13px;border-radius:11px}
.shipping-img-wrap{position:relative;border-radius:16px;overflow:hidden;box-shadow:var(--shadow);max-width:150px;margin:0 auto}
.shipping-img-wrap img{width:100%;display:block;transition:.5s}
.shipping-img-wrap:hover img{transform:scale(1.05)}
@media(max-width:800px){.shipping-inner{grid-template-columns:1fr}.shipping-img-wrap{order:-1;max-width:110px}}
.slider-arrow{position:absolute;top:50%;transform:translateY(-50%);background:rgba(255,255,255,.15);backdrop-filter:blur(4px);color:#fff;border:none;font-size:24px;width:46px;height:46px;border-radius:50%;cursor:pointer;z-index:10;transition:.2s;border:1px solid rgba(255,255,255,.2)}
.slider-arrow:hover{background:rgba(255,255,255,.3)}
.slider-arrow.prev{left:14px}
.slider-arrow.next{right:14px}
.slider-dots{display:flex;justify-content:center;gap:8px;padding:12px;background:#fff}
.dot{width:10px;height:10px;border-radius:50%;background:#ddd;cursor:pointer;transition:.3s}
.dot.active{background:var(--orange);width:28px;border-radius:5px}

/* BADGES */
.badges-strip{background:#fff;border-top:1px solid var(--border);border-bottom:3px solid var(--orange)}
.badges-inner{max-width:1320px;margin:0 auto;display:flex;justify-content:center;flex-wrap:wrap}
.badge-item{display:flex;align-items:center;gap:8px;padding:14px 22px;font-weight:800;font-size:13px;border-right:1px solid var(--border);color:var(--dark)}
.badge-item:last-child{border-right:none}
.badge-item em{color:var(--orange);font-style:normal}

/* SECTION TITLES */
.section-title{text-align:center;padding:32px 16px 6px;font-size:clamp(22px,3vw,30px);font-weight:900;font-family:'Poppins',sans-serif;color:var(--dark)}
.section-title span{color:var(--orange)}
.section-sub{text-align:center;color:var(--gray);margin-bottom:22px;font-size:14px;padding:0 16px}

/* PRODUCTS */
.products-section{max-width:1320px;margin:0 auto;padding:0 14px 50px}
.products-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(210px,1fr));gap:18px}

/* PRODUCT CARD */
.product-card{background:#fff;border-radius:18px;overflow:hidden;box-shadow:var(--shadow);transition:.28s;position:relative;display:flex;flex-direction:column}
.product-card:hover{transform:translateY(-5px);box-shadow:var(--shadow-hover)}
.product-img-wrap{position:relative;background:#f8f8f8;height:210px;overflow:hidden;display:flex;align-items:center;justify-content:center;cursor:pointer}
.product-img-wrap img{height:100%;width:100%;object-fit:cover;transition:.4s}
.product-card:hover .product-img-wrap img{transform:scale(1.07)}
.badge-off{position:absolute;top:10px;left:10px;background:var(--orange);color:#fff;font-size:11px;font-weight:900;padding:4px 10px;border-radius:20px;z-index:2}
.badge-sold-c{position:absolute;top:10px;right:10px;background:rgba(26,26,46,.85);color:#fff;font-size:10px;font-weight:700;padding:3px 8px;border-radius:10px;z-index:2}
.badge-last{position:absolute;bottom:10px;left:10px;background:var(--red);color:#fff;font-size:10px;font-weight:900;padding:3px 9px;border-radius:10px;z-index:2;animation:pulse 1.3s infinite}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.55}}
.product-info{padding:13px 13px 0;flex:1;cursor:pointer}
.product-name{font-weight:800;font-size:14px;line-height:1.35;margin-bottom:6px;font-family:'Poppins',sans-serif;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}
.stars{color:#f5c518;font-size:14px;margin-bottom:5px}
.stars span{color:var(--gray);font-size:12px;margin-left:4px}
.price-wrap{display:flex;align-items:center;gap:8px;flex-wrap:wrap;margin-bottom:5px}
.price-old{color:#aaa;font-size:13px;text-decoration:line-through}
.price-new{color:var(--orange);font-size:22px;font-weight:900}
.timer-badge{background:#fff5ee;border:1px solid #ffccaa;border-radius:8px;padding:4px 9px;font-size:11px;font-weight:800;color:var(--orange);display:flex;align-items:center;gap:4px;margin-bottom:6px}
.free-ship{font-size:11.5px;color:var(--green);font-weight:800;display:flex;align-items:center;gap:3px;margin-bottom:3px}
.contra-e{font-size:11px;color:var(--gray);margin-bottom:10px}
.card-btns{display:grid;grid-template-columns:1fr 1fr;gap:8px;padding:0 13px 13px;margin-top:auto}
.btn-add{background:var(--dark);color:#fff;border:none;padding:10px 6px;border-radius:12px;font-weight:800;font-size:13px;cursor:pointer;transition:.2s;width:100%}
.btn-add:hover{background:#0f0f25}
.btn-pedir{background:var(--orange);color:#fff;border:none;padding:10px 6px;border-radius:12px;font-weight:900;font-size:13px;cursor:pointer;width:100%;position:relative;overflow:hidden;transition:.2s}
.btn-pedir:hover{background:#e04800}
@keyframes shake{
  0%{transform:translateX(0) rotate(0)}
  15%{transform:translateX(-5px) rotate(-1.5deg)}
  30%{transform:translateX(5px) rotate(1.5deg)}
  45%{transform:translateX(-4px) rotate(-1deg)}
  60%{transform:translateX(4px) rotate(1deg)}
  75%{transform:translateX(-2px)}
  90%{transform:translateX(2px)}
  100%{transform:translateX(0)}
}
.btn-pedir.shaking{animation:shake .65s ease-in-out}

/* PRODUCT PAGE (full immersive view) */
.modal-overlay{display:none;position:fixed;inset:0;background:#fff;z-index:1100;overflow-y:auto}
.modal-overlay.active{display:block}
.modal-box{background:#fff;width:100%;min-height:100%;position:relative}
.modal-close{position:fixed;top:14px;left:14px;background:#fff;color:var(--dark);border:none;border-radius:22px;padding:9px 16px;font-size:13px;font-weight:800;cursor:pointer;z-index:50;display:flex;align-items:center;gap:6px;box-shadow:0 4px 16px rgba(0,0,0,.18)}
.modal-close:hover{background:#f2f2f2}
.modal-content{padding:0}
.pp-topmarquee{background:var(--dark);color:#fff;font-size:12px;font-weight:700;padding:8px 12px;text-align:center;overflow:hidden;white-space:nowrap}
.pp-header{background:#fff;padding:12px 20px;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid var(--border);position:sticky;top:0;z-index:6}
.pp-header img{height:32px}
.pp-hero{max-width:1080px;margin:0 auto;display:grid;grid-template-columns:1fr 1fr;gap:36px;padding:34px 20px 12px}
.pp-gallery-main{border-radius:18px;overflow:hidden;background:#f8f8f8;aspect-ratio:1/1;display:flex;align-items:center;justify-content:center}
.pp-gallery-main img{width:100%;height:100%;object-fit:cover;cursor:pointer}
.pp-gallery-thumbs{display:flex;gap:8px;margin-top:10px;flex-wrap:wrap}
.pp-gallery-thumbs img{width:60px;height:60px;object-fit:cover;border-radius:10px;cursor:pointer;border:2px solid transparent}
.pp-gallery-thumbs img.active-img{border-color:var(--orange)}
.pp-badge{display:inline-flex;align-items:center;gap:6px;background:#f2f2f2;border-radius:20px;padding:7px 14px;font-weight:800;font-size:12.5px;color:var(--dark);margin-bottom:14px;width:fit-content}
.pp-title{font-family:'Poppins',sans-serif;font-weight:900;font-size:clamp(23px,3.2vw,32px);line-height:1.22;margin-bottom:14px;color:var(--dark)}
.pp-title span{color:var(--orange)}
.pp-price-row{display:flex;align-items:baseline;gap:14px;margin-bottom:16px}
.pp-price-old{font-size:17px;color:#aaa;text-decoration:line-through}
.pp-price-new{font-size:36px;font-weight:900;color:var(--orange);font-family:'Poppins',sans-serif}
.pp-cta{width:100%;background:var(--orange);color:#fff;border:none;padding:18px;border-radius:16px;font-weight:900;font-size:16.5px;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:10px;box-shadow:0 8px 24px rgba(255,82,0,.35);transition:.2s;animation:btnPulse 2.4s ease-in-out infinite}
.pp-cta:hover{background:#e04800;transform:scale(1.015);animation-play-state:paused}
.pp-note{font-size:12.5px;color:var(--gray);margin-top:10px;line-height:1.5}
.pp-trust-row{display:flex;gap:10px;flex-wrap:wrap;margin-top:16px}
.pp-trust-chip{display:flex;align-items:center;gap:6px;background:#fff;border:1.5px solid var(--border);border-radius:12px;padding:8px 13px;font-weight:800;font-size:12.5px;color:var(--dark)}
.pp-section{max-width:880px;margin:0 auto;padding:32px 20px}
.pp-eyebrow{color:var(--orange);font-weight:900;font-size:12px;letter-spacing:1px;text-transform:uppercase;margin-bottom:6px}
.pp-section h2{font-family:'Poppins',sans-serif;font-weight:900;font-size:clamp(19px,2.6vw,25px);color:var(--dark);margin-bottom:14px;line-height:1.32}
.pp-section p.pp-lead{color:var(--gray);font-size:14px;line-height:1.7;margin-bottom:8px}
.pp-features-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:14px;margin-top:8px}
.pp-feature-card{background:#fafafa;border:1px solid var(--border);border-radius:14px;padding:16px;transition:.2s}
.pp-feature-card:hover{border-color:var(--orange);box-shadow:var(--shadow);transform:translateY(-2px)}
.pp-feature-card .pf-icon{font-size:22px;margin-bottom:8px;display:block}
.pp-feature-card p{font-size:12.8px;color:#444;line-height:1.55}
.pp-steps{display:grid;grid-template-columns:repeat(auto-fit,minmax(170px,1fr));gap:18px;margin-top:8px}
.pp-step{text-align:center}
.pp-step .ps-num{width:36px;height:36px;border-radius:50%;background:var(--orange);color:#fff;font-weight:900;display:flex;align-items:center;justify-content:center;margin:0 auto 10px;font-size:15px}
.pp-step b{font-size:13.5px;display:block;margin-bottom:4px}
.pp-step p{font-size:12.5px;color:var(--gray)}
.pp-specs{background:#fafafa;border-radius:16px;padding:4px 18px;border:1px solid var(--border)}
.pp-spec-row{display:flex;justify-content:space-between;padding:12px 0;border-bottom:1px solid var(--border);font-size:13.5px}
.pp-spec-row:last-child{border-bottom:none}
.pp-spec-row b{color:var(--dark)}
.pp-spec-row span{color:var(--gray);font-weight:700}
.pp-shipping-mini{display:flex;align-items:center;gap:16px;background:#f0fff4;border:1px solid var(--green);border-radius:16px;padding:16px;flex-wrap:wrap}
.pp-shipping-mini img{width:60px;height:60px;object-fit:cover;border-radius:12px;flex-shrink:0}
.pp-shipping-mini .psm-text{flex:1;min-width:180px}
.pp-shipping-mini .psm-text b{display:block;font-size:13.5px;color:#006630;margin-bottom:4px}
.pp-shipping-mini .psm-text span{font-size:12px;color:var(--gray)}
.pp-faq details{border:1px solid var(--border);border-radius:12px;padding:14px 16px;margin-bottom:10px;background:#fff;cursor:pointer}
.pp-faq summary{font-weight:800;font-size:13.5px;list-style:none;display:flex;justify-content:space-between;align-items:center}
.pp-faq summary::-webkit-details-marker{display:none}
.pp-faq summary::after{content:'+';font-size:19px;color:var(--orange);font-weight:900}
.pp-faq details[open] summary::after{content:'−'}
.pp-faq p{font-size:12.8px;color:var(--gray);margin-top:10px;line-height:1.6}
.pp-sticky-bar{position:sticky;bottom:0;left:0;right:0;background:#fff;border-top:1px solid var(--border);box-shadow:0 -6px 20px rgba(0,0,0,.08);padding:12px 20px;display:flex;align-items:center;justify-content:space-between;gap:14px;z-index:20}
.pp-sticky-bar .psb-price{font-weight:900;color:var(--orange);font-size:18px;font-family:'Poppins',sans-serif}
.pp-sticky-bar button{background:var(--orange);color:#fff;border:none;padding:12px 20px;border-radius:14px;font-weight:900;font-size:13.5px;cursor:pointer;white-space:nowrap}
.pp-footer-mini{text-align:center;padding:26px 16px;color:var(--gray);font-size:12px;border-top:1px solid var(--border)}
@media(max-width:760px){.pp-hero{grid-template-columns:1fr;padding:24px 16px 8px}}
.review-list{margin-top:22px}
.review-item{border:1px solid var(--border);border-radius:13px;padding:14px;margin-bottom:11px;background:#fafafa}
.review-top{display:flex;align-items:center;gap:10px;margin-bottom:6px}
.review-avatar{width:38px;height:38px;border-radius:50%;background:var(--orange);color:#fff;display:flex;align-items:center;justify-content:center;font-weight:900;font-size:16px;flex-shrink:0}
.review-name{font-weight:800;font-size:14px}
.review-stars{color:#f5c518;font-size:13px}
.review-text{font-size:13px;color:#444;line-height:1.55}

/* ORDER FORM */
.order-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.65);z-index:1200;align-items:center;justify-content:center;padding:16px}
.order-overlay.active{display:flex}
.order-form-box{background:#fff;border-radius:22px;max-width:540px;width:100%;max-height:92vh;overflow-y:auto;padding:28px;position:relative}
.form-title{font-size:21px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:6px}
.form-prod{font-size:14px;color:var(--gray);margin-bottom:14px}
.form-price-show{background:#fff8f0;border:2.5px solid var(--orange);border-radius:13px;padding:14px;margin-bottom:18px;display:flex;justify-content:space-between;align-items:center}
.form-price-show .fprice{font-size:24px;font-weight:900;color:var(--orange)}
.form-price-show .fold{font-size:13px;text-decoration:line-through;color:#aaa}
.form-group{margin-bottom:14px}
.form-group label{font-weight:800;font-size:14px;display:block;margin-bottom:5px}
.req{color:var(--red)}
.form-group input,.form-group textarea,.form-group select{width:100%;padding:12px 14px;border:2px solid var(--border);border-radius:11px;font-size:14px;font-family:'Nunito',sans-serif;outline:none;transition:.2s;color:var(--dark);background:#fafafa}
.form-group input:focus,.form-group textarea:focus,.form-group select:focus{border-color:var(--orange);background:#fff}
.form-group textarea{resize:vertical;min-height:72px}
.btn-confirm{width:100%;background:var(--green);color:#fff;border:none;padding:15px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;margin-top:10px;transition:.2s}
.btn-confirm:hover{background:#009040}
.btn-cancel-f{width:100%;background:#eee;color:var(--dark);border:none;padding:12px;border-radius:14px;font-weight:700;font-size:14px;cursor:pointer;margin-top:8px}

/* CART DRAWER */
.cart-drawer{position:fixed;right:-420px;top:0;height:100vh;width:390px;background:#fff;box-shadow:-6px 0 40px rgba(0,0,0,.18);z-index:1300;transition:.35s cubic-bezier(.4,0,.2,1);overflow-y:auto;padding:22px}
.cart-drawer.open{right:0}
.cart-title{font-size:21px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:18px;display:flex;justify-content:space-between;align-items:center}
.cart-item{display:flex;gap:12px;border-bottom:1px solid var(--border);padding:13px 0;align-items:center}
.cart-item img{width:72px;height:72px;object-fit:cover;border-radius:10px;background:#f4f4f4;flex-shrink:0}
.cart-item-info{flex:1}
.cart-item-name{font-weight:800;font-size:14px;line-height:1.3;margin-bottom:3px}
.cart-item-price{color:var(--orange);font-weight:900;font-size:15px}
.cart-qty{display:flex;align-items:center;gap:8px;margin-top:5px}
.qty-btn{background:var(--border);border:none;border-radius:6px;width:26px;height:26px;font-weight:900;cursor:pointer;font-size:14px}
.qty-val{font-weight:800;font-size:14px;min-width:20px;text-align:center}
.cart-remove{color:var(--red);background:none;border:none;font-size:20px;cursor:pointer;flex-shrink:0;padding:0 4px}
.cart-total-row{font-size:18px;font-weight:900;color:var(--orange);text-align:right;margin:18px 0;padding-top:4px}
.btn-checkout{width:100%;background:var(--orange);color:#fff;border:none;padding:15px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;transition:.2s}
.btn-checkout:hover{background:#e04800}
.empty-cart{text-align:center;color:var(--gray);padding:48px 0;font-size:15px}

/* DELIVERY CALC */
.delivery-wrap{max-width:520px;margin:0 auto 36px;background:#fff;border-radius:18px;padding:22px;box-shadow:var(--shadow)}
.delivery-wrap h3{font-size:18px;font-weight:900;margin-bottom:12px;font-family:'Poppins',sans-serif}
.delivery-result{background:#f0fff4;border:1px solid var(--green);border-radius:11px;padding:13px;font-size:14px;font-weight:700;color:#006630;margin-top:12px;display:none}

/* NOTIFICATION */
.notif{position:fixed;bottom:90px;left:16px;background:var(--dark);color:#fff;padding:12px 18px;border-radius:14px;font-size:13px;font-weight:700;z-index:1200;display:none;max-width:300px;box-shadow:0 6px 24px rgba(0,0,0,.35);animation:slideUp .4s}
@keyframes slideUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
.notif .nn{color:var(--orange)}

/* ROULETTE MODAL */
.roulette-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.75);z-index:2000;align-items:center;justify-content:center;padding:16px}
.roulette-overlay.active{display:flex}
.roulette-box{background:#fff;border-radius:26px;max-width:500px;width:100%;padding:32px;text-align:center;position:relative;overflow:hidden}
.roulette-box::before{content:'';position:absolute;top:0;left:0;right:0;height:5px;background:linear-gradient(90deg,var(--orange),#ff9a5c,var(--orange))}
.roulette-title{font-size:26px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:6px;color:var(--dark)}
.roulette-title span{color:var(--orange)}
.roulette-sub{font-size:14px;color:var(--gray);margin-bottom:22px}
.roulette-canvas-wrap{position:relative;width:280px;height:280px;margin:0 auto 20px}
.roulette-canvas-wrap canvas{border-radius:50%;box-shadow:0 8px 32px rgba(255,82,0,.25)}
.roulette-pointer{position:absolute;top:-18px;left:50%;transform:translateX(-50%);font-size:36px;filter:drop-shadow(0 2px 4px rgba(0,0,0,.3))}
.roulette-btn{background:var(--orange);color:#fff;border:none;padding:14px 36px;border-radius:30px;font-weight:900;font-size:17px;cursor:pointer;transition:.2s;margin-top:8px}
.roulette-btn:hover{background:#e04800;transform:scale(1.05)}
.roulette-btn:disabled{background:#ccc;cursor:not-allowed;transform:none}
.roulette-result{margin-top:18px;font-size:18px;font-weight:900;color:var(--orange);display:none;animation:slideUp .4s}
.roulette-close{position:absolute;top:14px;right:14px;background:var(--dark);color:#fff;border:none;border-radius:50%;width:32px;height:32px;font-size:17px;cursor:pointer;display:flex;align-items:center;justify-content:center}
.roulette-close:hover{background:#333}

/* ADMIN */
.admin-btns{position:fixed;bottom:16px;right:16px;display:flex;gap:8px;z-index:1100}
.admin-btn{width:38px;height:38px;border-radius:50%;border:none;font-weight:900;font-size:13px;cursor:pointer;opacity:.55;transition:.2s;box-shadow:0 2px 10px rgba(0,0,0,.25)}
.admin-btn:hover{opacity:1;transform:scale(1.12)}
.admin-btn.r-btn{background:var(--orange);color:#fff}
.admin-btn.c-btn{background:var(--dark);color:#fff}
.admin-btn.e-btn{background:#0f3460;color:#fff}

.admin-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.65);z-index:2000;align-items:flex-start;justify-content:center;padding:16px;overflow-y:auto}
.admin-overlay.active{display:flex}
.admin-panel{background:#fff;border-radius:22px;max-width:980px;width:100%;margin:20px auto;padding:26px;position:relative;max-height:90vh;overflow-y:auto}
.admin-panel h2{font-size:22px;font-weight:900;font-family:'Poppins',sans-serif;color:var(--orange);margin-bottom:20px}
.admin-product-item{border:2px solid var(--border);border-radius:14px;padding:18px;margin-bottom:14px}
.admin-product-item label{font-weight:800;font-size:13px;display:block;margin-bottom:3px;margin-top:10px}
.admin-product-item input,.admin-product-item textarea,.admin-product-item select{width:100%;padding:8px 12px;border:1.5px solid var(--border);border-radius:9px;font-size:13px;font-family:'Nunito',sans-serif}
.admin-row2{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.btn-save-admin{background:var(--green);color:#fff;border:none;padding:10px 20px;border-radius:10px;font-weight:800;cursor:pointer;margin-top:10px}
.btn-del-admin{background:var(--red);color:#fff;border:none;padding:6px 12px;border-radius:8px;font-weight:700;cursor:pointer;font-size:12px}
.btn-add-prod{background:var(--orange);color:#fff;border:none;padding:12px 24px;border-radius:12px;font-weight:900;cursor:pointer;font-size:15px;margin-bottom:20px}
.img-preview{width:80px;height:80px;object-fit:cover;border-radius:10px;border:2px solid var(--border);margin-top:6px;cursor:pointer}

.orders-stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(120px,1fr));gap:10px;margin-bottom:18px}
.stat-card{background:#fff;border:2px solid var(--border);border-radius:13px;padding:14px;text-align:center}
.stat-card .sv{font-size:24px;font-weight:900;color:var(--orange)}
.stat-card .sl{font-size:12px;color:var(--gray);font-weight:700;margin-top:2px}
.orders-toolbar{display:flex;gap:10px;flex-wrap:wrap;margin-bottom:16px;padding:14px;background:#f8f8f8;border-radius:13px;align-items:center}
.orders-toolbar input{flex:1;min-width:160px;padding:9px 13px;border:1.5px solid var(--border);border-radius:9px;font-size:13px;font-family:'Nunito',sans-serif;outline:none}
.orders-toolbar input:focus{border-color:var(--orange)}
.order-card{border:2px solid var(--border);border-radius:15px;padding:16px;margin-bottom:12px;background:#fff;transition:.2s}
.order-card:hover{border-color:var(--orange);box-shadow:0 4px 18px rgba(255,82,0,.1)}
.order-product-name{font-size:15px;font-weight:900;color:var(--dark);font-family:'Poppins',sans-serif;margin-bottom:8px}
.order-grid{display:grid;grid-template-columns:1fr 1fr;gap:6px;font-size:13px}
.order-field .of-label{font-size:11px;font-weight:800;color:var(--gray);text-transform:uppercase;letter-spacing:.5px;display:block}
.order-field .of-value{font-weight:700;color:var(--dark)}
.order-price-row{display:flex;align-items:center;gap:10px;margin-top:10px;padding-top:10px;border-top:1px solid var(--border);flex-wrap:wrap}
.order-price-new{font-size:20px;font-weight:900;color:var(--orange)}
.order-price-old{font-size:13px;text-decoration:line-through;color:#aaa}
.order-wa-btn{margin-left:auto;background:#25D366;color:#fff;border:none;border-radius:10px;padding:8px 16px;font-weight:800;font-size:12px;cursor:pointer}
.order-nota{background:#fffbe6;border:1px solid #ffe082;border-radius:9px;padding:8px 12px;font-size:12px;color:#7a6000;margin-top:8px;font-weight:700}
.no-orders{text-align:center;padding:40px;color:var(--gray);font-size:15px}
.visitors-badge{background:var(--dark);color:#fff;border-radius:11px;padding:10px 16px;font-size:13px;font-weight:700;margin-bottom:16px;display:flex;align-items:center;gap:8px}
.visitors-dot{width:10px;height:10px;border-radius:50%;background:var(--green);animation:blink 1.1s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.15}}

/* SEARCH DROPDOWN */
.search-dropdown{position:absolute;top:108%;left:0;right:0;background:#fff;border-radius:14px;box-shadow:0 10px 32px rgba(0,0,0,.14);z-index:600;display:none;max-height:300px;overflow-y:auto}
.search-dropdown.open{display:block}
.search-dd-item{padding:11px 16px;cursor:pointer;font-size:14px;border-bottom:1px solid var(--border);display:flex;align-items:center;gap:10px;transition:.15s}
.search-dd-item:hover{background:#fff8f0}
.search-dd-item img{width:40px;height:40px;object-fit:cover;border-radius:8px}
.search-dd-item .sdi-name{font-weight:800;font-size:14px}
.search-dd-item .sdi-price{color:var(--orange);font-weight:900;font-size:13px}

/* WA FLOAT */
.wa-float{position:fixed;bottom:90px;right:20px;background:#25D366;color:#fff;width:58px;height:58px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:28px;box-shadow:0 4px 20px rgba(0,0,0,.3);z-index:1000;transition:.2s}
.wa-float:hover{transform:scale(1.12);background:#128C7E}

/* FLOAT MSG */
.float-msg{position:fixed;bottom:160px;left:50%;transform:translateX(-50%);background:var(--dark);color:#fff;padding:11px 22px;border-radius:22px;font-weight:700;font-size:14px;z-index:9999;animation:slideUp .4s;white-space:nowrap}

/* PAGE EDITOR */
.page-editor-group{border:1.5px solid var(--border);border-radius:13px;padding:16px;margin-bottom:14px}
.page-editor-group label{font-weight:800;font-size:14px;display:block;margin-bottom:6px;color:var(--dark)}
.page-editor-group input,.page-editor-group textarea{width:100%;padding:9px 13px;border:1.5px solid var(--border);border-radius:9px;font-size:13px;font-family:'Nunito',sans-serif}
.page-editor-group textarea{min-height:64px;resize:vertical}
.admin-review-item{border:1.5px solid var(--border);border-radius:11px;padding:13px;margin-bottom:10px;display:grid;gap:6px}
.admin-review-item input,.admin-review-item textarea,.admin-review-item select{width:100%;padding:8px 11px;border:1.5px solid var(--border);border-radius:8px;font-size:13px;font-family:'Nunito',sans-serif}

/* RESPONSIVE */
@media(max-width:700px){
  .products-grid{grid-template-columns:repeat(2,1fr);gap:12px}
  .modal-gallery{grid-template-columns:1fr 1fr}
  .cart-drawer{width:100%;right:-110%}
  .slide-content{padding:24px}
  .admin-row2{grid-template-columns:1fr}
  .order-grid{grid-template-columns:1fr}
  .orders-stats{grid-template-columns:1fr 1fr}
  .card-btns{grid-template-columns:1fr 1fr}
  .badge-item{padding:9px 12px;font-size:12px}
}
@media(max-width:380px){
  .products-grid{grid-template-columns:1fr}
}
/* GIF/VIDEO in modal */
.modal-media-item{border-radius:12px;overflow:hidden;height:190px;object-fit:cover;width:100%}
</style>
</head>
<body>

<!-- TOPBAR -->
<div class="topbar">
  <div class="topbar-scroll" id="topbar-text">
    🇨🇴 Envíos a TODA Colombia &nbsp;|&nbsp; 💵 PAGO CONTRA ENTREGA &nbsp;|&nbsp; 📦 Interrapidísimo · Coordinadora · Envia &nbsp;|&nbsp; ⭐ +500 clientes felices &nbsp;|&nbsp; 🔒 Compra 100% segura &nbsp;|&nbsp; 🚚 Envío GRATIS en todos los productos
  </div>
</div>

<!-- HEADER -->
<header>
  <div class="header-inner">
    <div class="logo-area">
      <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAQDAwMDAgQDAwMEBAQFBgoGBgUFBgwICQcKDgwPDg4MDQ0PERYTDxAVEQ0NExoTFRcYGRkZDxIbHRsYHRYYGRj/2wBDAQQEBAYFBgsGBgsYEA0QGBgYGBgYGBgYGBgYGBgYGBgYGBgYGBgYGBgYGBgYGBgYGBgYGBgYGBgYGBgYGBgYGBj/wAARCADZAv8DASIAAhEBAxEB/8QAHAABAAICAwEAAAAAAAAAAAAAAAEHAggDBQYE/8QASxAAAQIEBAIDDQUFBgUFAQAAAQACAwQFEQYHITESQVFxsRMiMjM0NmFyc4GRwdEUFReSoTU3QlTwFiNEUlPhJCZVYmMnQ0WC8aL/xAAcAQACAgMBAQAAAAAAAAAAAAAABwEGBAUIAgP/xAA5EQACAQMCAwYFAwQCAQUBAAAAAQIDBAYFERIhMRM0NUFRcQcUFiIzUlNhFRckMiORYiVCQ4GCsf/aAAwDAQACEQMRAD8A5ERFzedYBERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERABERAEghuqd0B3ssS3iCjuQHNSjycoddQ7dQDbZCb8kEpEDdTpdQpIsN16in5IkHVLJoAgPF7lG2/kR/DIRTYclChrYkKRZQBdLL0t0t9iG/IKdQEAHLdCF5226oNyERFBIREQAREQAREQAREQAREQAO6myi1j1qXC405L1ttzZD6rYHRQli4XWVivfZt80uR540YopIJUlHZv0ZPEjFFOqWJUdm/RhxIhFIGm6iyOzYcSCaJY9CAFRwP0J4kE0U2I3CWU8D9A3RHNFNuWiWPoUdmyOJepCWQDqWVx0I4PXkHEjFTYqTtcD9Fjc72RwbPZkcW/QKeG+ykaoeIjRTwJNA5GNtUWTbnRQW23KhU5PnsTxEXRSLAclOl16VJhxIxRZ2CxtZDpMOIhFN0ub7/AKLy4NdQ4iBqpsehLnpU3IO6OFeobkWKWU8RUXLioaXRcwT3FvSllJbw7KOSlqMerJXPzIRSBdQRZQ4tLmAREXkkIiIAIiIAIiIAe9FIB5oTY2Xrh2XMhvYW0UKdDsgI2so29eRG5CKT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" alt="TROGÜI" class="logo-img">
    </div>
    <div class="search-bar" style="position:relative">
      <input type="text" id="search-input" placeholder="🔍  Buscar productos..." autocomplete="off" oninput="searchProducts(this.value)" onfocus="searchProducts(this.value)">
      <button onclick="doSearch()">🔍</button>
      <div class="search-dropdown" id="search-dropdown"></div>
    </div>
    <div class="header-actions">
      <a href="https://wa.link/lhneng" target="_blank" class="wa-btn"><svg class="wa-icon" viewBox="0 0 32 32" fill="#fff" xmlns="http://www.w3.org/2000/svg"><path d="M16.001 3C9.373 3 4 8.373 4 15c0 2.386.7 4.607 1.902 6.472L4 29l7.72-1.868A11.94 11.94 0 0016.001 27C22.629 27 28 21.627 28 15S22.629 3 16.001 3zm6.965 17.06c-.29.816-1.434 1.5-2.353 1.695-.628.133-1.448.24-4.208-.903-3.532-1.462-5.805-5.045-5.983-5.278-.17-.233-1.435-1.91-1.435-3.643s.897-2.586 1.216-2.94c.318-.354.696-.442.928-.442.232 0 .464.002.667.012.213.01.5-.08.782.598.29.698.985 2.41 1.07 2.585.086.175.144.38.03.612-.116.233-.174.378-.343.58-.17.204-.357.455-.51.61-.17.174-.348.363-.15.71.198.348.88 1.454 1.89 2.354 1.3 1.158 2.396 1.517 2.744 1.687.348.17.552.145.756-.087.203-.233.87-1.014 1.103-1.362.232-.348.464-.29.782-.174.318.116 2.02.953 2.367 1.126.348.174.58.26.667.406.087.145.087.842-.203 1.658z"/></svg> 320 657 2598</a>
      <div class="socials">
        <a href="https://www.instagram.com/store_trog" target="_blank" class="ig" title="Instagram">📸</a>
        <a href="https://www.tiktok.com/@trogui_store" target="_blank" class="tk" title="TikTok">🎵</a>
        <a href="https://wa.link/lhneng" target="_blank" class="wa" title="WhatsApp"><svg class="wa-icon" viewBox="0 0 32 32" fill="#fff" xmlns="http://www.w3.org/2000/svg"><path d="M16.001 3C9.373 3 4 8.373 4 15c0 2.386.7 4.607 1.902 6.472L4 29l7.72-1.868A11.94 11.94 0 0016.001 27C22.629 27 28 21.627 28 15S22.629 3 16.001 3zm6.965 17.06c-.29.816-1.434 1.5-2.353 1.695-.628.133-1.448.24-4.208-.903-3.532-1.462-5.805-5.045-5.983-5.278-.17-.233-1.435-1.91-1.435-3.643s.897-2.586 1.216-2.94c.318-.354.696-.442.928-.442.232 0 .464.002.667.012.213.01.5-.08.782.598.29.698.985 2.41 1.07 2.585.086.175.144.38.03.612-.116.233-.174.378-.343.58-.17.204-.357.455-.51.61-.17.174-.348.363-.15.71.198.348.88 1.454 1.89 2.354 1.3 1.158 2.396 1.517 2.744 1.687.348.17.552.145.756-.087.203-.233.87-1.014 1.103-1.362.232-.348.464-.29.782-.174.318.116 2.02.953 2.367 1.126.348.174.58.26.667.406.087.145.087.842-.203 1.658z"/></svg></a>
      </div>
      <button class="cart-btn" onclick="toggleCart()">🛒 Carrito <span class="cart-count" id="cart-count">0</span></button>
    </div>
  </div>
</header>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <a href="#products" class="active" onclick="filterCat('all',this)">🏠 Todo</a>
    <a href="#products" onclick="filterCat('hogar',this)">🏡 Hogar</a>
    <a href="#products" onclick="filterCat('tecnologia',this)">📱 Tecnología</a>
    <a href="#products" onclick="filterCat('salud',this)">💊 Salud</a>
    <a href="#products" onclick="filterCat('belleza',this)">💄 Belleza</a>
    <a href="#products" onclick="filterCat('fitness',this)">🏋️ Fitness</a>
    <a href="#products" onclick="filterCat('accesorios',this)">👜 Accesorios</a>
    <a href="#products" onclick="filterCat('juguetes',this)">🧸 Juguetes</a>
    <a href="#products" onclick="filterCat('cocina',this)">🍳 Cocina</a>
  </div>
</nav>

<!-- SLIDER -->
<div class="slider-section">
  <div class="slider-wrap">
    <div class="slider-track" id="slider-track">
      <div class="slide slide-1">
        <div class="slide-deco"></div>
        <div class="slide-content">
          <h2>🇨🇴 Envío Gratis<br>a <span>Toda Colombia</span></h2>
          <p>Más de 35 productos increíbles · Pago contra entrega · Sin riesgo</p>
          <a href="#products" class="slide-btn">¡Ver Ofertas!</a>
        </div>
      </div>
      <div class="slide slide-2">
        <div class="slide-deco"></div>
        <div class="slide-content">
          <h2>💵 Pago<br><span>Contra Entrega</span></h2>
          <p>Pagas cuando recibes tu pedido. Sin tarjeta, sin riesgo, con confianza.</p>
          <a href="#products" class="slide-btn">Comprar Ahora</a>
        </div>
      </div>
      <div class="slide slide-3">
        <div class="slide-deco"></div>
        <div class="slide-content">
          <h2>📦 Recibe en<br><span>3 a 7 Días</span></h2>
          <p>Enviamos con Coordinadora, Interrapidísimo y Envia a todo el país.</p>
          <a href="#products" class="slide-btn">Ver Productos</a>
        </div>
      </div>
    </div>
    <button class="slider-arrow prev" onclick="moveSlider(-1)">‹</button>
    <button class="slider-arrow next" onclick="moveSlider(1)">›</button>
    <div class="slider-showcase" id="slider-showcase">
      <img id="showcase-img" src="" alt="Producto TROGÜI">
      <div class="showcase-tag" id="showcase-tag">$0</div>
    </div>
  </div>
  <div class="slider-dots" id="slider-dots">
    <div class="dot active" onclick="goSlide(0)"></div>
    <div class="dot" onclick="goSlide(1)"></div>
    <div class="dot" onclick="goSlide(2)"></div>
  </div>
</div>

<!-- BADGES -->
<div class="badges-strip">
  <div class="badges-inner">
    <div class="badge-item">✅ <em>Pago Contra Entrega</em></div>
    <div class="badge-item">🚚 <em>Envío GRATIS</em></div>
    <div class="badge-item">📦 <em>3 a 7 días hábiles</em></div>
    <div class="badge-item">🔒 <em>Compra Segura</em></div>
    <div class="badge-item">⭐ <em>+500 Clientes Felices</em></div>
  </div>
</div>

<!-- SHIPPING / TRANSPORTADORAS -->
<div class="shipping-section">
  <div class="shipping-inner">
    <div class="shipping-text">
      <h2>🚚 Hacemos envíos a través de <span>transportadoras autorizadas</span> a toda Colombia</h2>
      <p>Trabajamos con las empresas de mensajería más confiables del país para que tu pedido llegue seguro, rápido y en perfectas condiciones, sin importar en qué ciudad o municipio te encuentres.</p>
      <div class="carrier-badges">
        <div class="carrier-chip"><span class="cc-dot"></span> 📦 Interrapidísimo</div>
        <div class="carrier-chip"><span class="cc-dot"></span> 📦 Envía Mensajería</div>
        <div class="carrier-chip"><span class="cc-dot"></span> 📦 Coordinadora</div>
      </div>
      <div class="shipping-trust">✅ Envío seguro, confiable y autorizado</div>
    </div>
    <div class="shipping-img-wrap">
      <img id="shipping-carrier-photo" src="data:image/jpeg;base64,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" alt="Transportadoras autorizadas: Interrapidísimo, Envía y Coordinadora">
    </div>
  </div>
</div>

<!-- NOTIFICATION -->
<div class="notif" id="notif-box"></div>

<!-- PRODUCTS -->
<div id="products">
  <h2 class="section-title" id="products-title">🔥 Productos en <span>OFERTA</span></h2>
  <p class="section-sub">Envío gratis a toda Colombia · Pago contra entrega · ¡Precios increíbles!</p>
  <div class="products-section">
    <div class="products-grid" id="products-grid"></div>
  </div>
</div>

<!-- DELIVERY CALC -->
<div style="max-width:1320px;margin:0 auto;padding:0 14px 20px">
  <div class="delivery-wrap">
    <h3>📅 ¿Cuándo llega mi pedido?</h3>
    <p style="font-size:13px;color:var(--gray);margin-bottom:12px">Selecciona tu ciudad y te calculamos la fecha estimada:</p>
    <select id="delivery-city" style="width:100%;padding:11px;border:2px solid var(--border);border-radius:11px;font-size:14px;font-family:'Nunito',sans-serif;margin-bottom:10px;outline:none">
      <option value="">-- Selecciona tu ciudad --</option>
      <option value="3">Bogotá D.C.</option>
      <option value="4">Medellín</option>
      <option value="4">Cali</option>
      <option value="5">Barranquilla</option>
      <option value="5">Cartagena</option>
      <option value="5">Bucaramanga</option>
      <option value="6">Pereira</option>
      <option value="6">Manizales</option>
      <option value="7">Pasto</option>
      <option value="7">Montería</option>
      <option value="7">Leticia</option>
    </select>
    <button onclick="calcDelivery()" style="background:var(--orange);color:#fff;border:none;padding:11px 26px;border-radius:11px;font-weight:800;cursor:pointer;font-size:14px">Calcular Fecha</button>
    <div class="delivery-result" id="delivery-result"></div>
  </div>
</div>

<!-- PRODUCT PAGE -->
<div class="modal-overlay" id="product-modal">
  <div class="modal-box">
    <button class="modal-close" onclick="closeModal()">← Volver a la tienda</button>
    <div class="modal-content" id="modal-content"></div>
  </div>
</div>

<!-- ORDER FORM -->
<div class="order-overlay" id="order-overlay">
  <div class="order-form-box">
    <h2 class="form-title">📋 Confirmar Pedido</h2>
    <p class="form-prod" id="form-prod-name"></p>
    <div class="form-price-show" id="form-price-show"></div>
    <div class="form-group"><label>Nombre <span class="req">*</span></label><input type="text" id="f-nombre" placeholder="Tu nombre completo"></div>
    <div class="form-group"><label>Apellido <span class="req">*</span></label><input type="text" id="f-apellido" placeholder="Tu apellido"></div>
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
    <div class="form-group"><label>Ciudad <span class="req">*</span></label><input type="text" id="f-ciudad" placeholder="Ej: Bogotá, Medellín, Cali..."></div>
    <div class="form-group"><label>Dirección completa <span class="req">*</span></label><input type="text" id="f-direccion" placeholder="Calle, carrera, barrio, apto..."></div>
    <div class="form-group"><label>Teléfono <span class="req">*</span></label><input type="tel" id="f-telefono" placeholder="Ej: 3001234567"></div>
    <div class="form-group"><label>Nota (opcional)</label><textarea id="f-nota" placeholder="Color, talla, variante u otro detalle..."></textarea></div>
    <button class="btn-confirm" onclick="confirmOrder()">✅ Confirmar Pedido por WhatsApp</button>
    <button class="btn-cancel-f" onclick="closeOrderForm()">Cancelar</button>
  </div>
</div>

<!-- CART DRAWER -->
<div class="cart-drawer" id="cart-drawer">
  <div class="cart-title">🛒 Mi Carrito <button onclick="toggleCart()" style="background:none;border:none;font-size:24px;cursor:pointer">✕</button></div>
  <div id="cart-items-list"></div>
  <div class="cart-total-row" id="cart-total"></div>
  <button class="btn-checkout" id="btn-checkout" onclick="checkoutCart()" style="display:none">Pedir Todo por WhatsApp 💬</button>
</div>

<!-- ROULETTE MODAL -->
<div class="roulette-overlay" id="roulette-overlay">
  <div class="roulette-box">
    <button class="roulette-close" onclick="closeRoulette()">✕</button>
    <div class="roulette-title">🎡 ¡Gira y <span>Gana!</span></div>
    <p class="roulette-sub">¡Gira la ruleta y obtén un premio especial para tu pedido!</p>
    <div class="roulette-canvas-wrap">
      <div class="roulette-pointer">▼</div>
      <canvas id="roulette-canvas" width="280" height="280"></canvas>
    </div>
    <button class="roulette-btn" id="roulette-btn" onclick="spinRoulette()">¡Girar Ruleta! 🎉</button>
    <div class="roulette-result" id="roulette-result"></div>
  </div>
</div>

<!-- ADMIN -->
<div class="admin-btns">
  <button class="admin-btn r-btn" title="Editar Productos" onclick="adminAuth('r')">R</button>
  <button class="admin-btn c-btn" title="Ver Pedidos" onclick="adminAuth('c')">C</button>
  <button class="admin-btn e-btn" title="Editar Página" onclick="adminAuth('e')">E</button>
</div>

<!-- ADMIN R: PRODUCTS -->
<div class="admin-overlay" id="admin-r">
  <div class="admin-panel">
    <h2>✏️ Editor de Productos</h2>
    <div class="visitors-badge"><span class="visitors-dot"></span><span id="v1">0</span> personas en la página ahora</div>
    <button class="btn-add-prod" onclick="addNewProduct()">+ Agregar Producto</button>
    <div id="admin-product-list"></div>
    <div style="display:flex;gap:10px;margin-top:18px;flex-wrap:wrap">
      <button class="btn-save-admin" onclick="saveAllProducts()">💾 Guardar Todos</button>
      <button onclick="closeAdmin('admin-r')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700">Cerrar</button>
    </div>
  </div>
</div>

<!-- ADMIN C: ORDERS -->
<div class="admin-overlay" id="admin-c">
  <div class="admin-panel">
    <h2>📦 Pedidos Recibidos</h2>
    <div class="visitors-badge"><span class="visitors-dot"></span><span id="v2">0</span> personas en la página ahora</div>
    <div class="orders-stats" id="orders-stats"></div>
    <div class="orders-toolbar">
      <input type="text" id="order-search" placeholder="🔍 Buscar por nombre, ciudad, producto..." oninput="filterOrders(this.value)">
      <button onclick="exportCSV()" style="background:var(--green);color:#fff;border:none;padding:9px 16px;border-radius:9px;font-weight:800;cursor:pointer;white-space:nowrap">📥 Exportar CSV</button>
      <button onclick="clearOrders()" style="background:var(--red);color:#fff;border:none;padding:9px 14px;border-radius:9px;font-weight:700;cursor:pointer;white-space:nowrap">🗑️ Limpiar</button>
    </div>
    <div id="admin-orders-list"></div>
    <button onclick="closeAdmin('admin-c')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700;margin-top:16px">Cerrar</button>
  </div>
</div>

<!-- ADMIN E: PAGE EDITOR -->
<div class="admin-overlay" id="admin-e">
  <div class="admin-panel">
    <h2>🎨 Editor de Página</h2>
    <div class="page-editor-group">
      <label>🔊 URL de Audio/Música de Fondo (MP3)</label>
      <input type="text" id="audio-url" placeholder="https://... .mp3">
      <button class="btn-save-admin" onclick="setAudio()" style="margin-top:8px">Aplicar Audio</button>
    </div>
    <div class="page-editor-group">
      <label>📢 Texto del Marquee (Barra superior)</label>
      <input type="text" id="edit-topbar" placeholder="Texto scrolling del topbar">
      <button class="btn-save-admin" onclick="saveSetting('topbar')" style="margin-top:8px">Guardar</button>
    </div>
    <div class="page-editor-group">
      <label>🏷️ Título de Sección Productos</label>
      <input type="text" id="edit-prod-title" placeholder="Ej: 🔥 Productos en OFERTA">
      <button class="btn-save-admin" onclick="saveSetting('prod-title')" style="margin-top:8px">Guardar</button>
    </div>
    <div class="page-editor-group">
      <label>⭐ Editar Reseñas</label>
      <div id="admin-reviews-list"></div>
      <button class="btn-save-admin" onclick="saveReviews()">💾 Guardar Reseñas</button>
    </div>
    <button onclick="closeAdmin('admin-e')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700;margin-top:16px">Cerrar</button>
  </div>
</div>

<a href="https://wa.link/lhneng" target="_blank" class="wa-float" title="WhatsApp"><svg class="wa-icon-lg" viewBox="0 0 32 32" fill="#fff" xmlns="http://www.w3.org/2000/svg"><path d="M16.001 3C9.373 3 4 8.373 4 15c0 2.386.7 4.607 1.902 6.472L4 29l7.72-1.868A11.94 11.94 0 0016.001 27C22.629 27 28 21.627 28 15S22.629 3 16.001 3zm6.965 17.06c-.29.816-1.434 1.5-2.353 1.695-.628.133-1.448.24-4.208-.903-3.532-1.462-5.805-5.045-5.983-5.278-.17-.233-1.435-1.91-1.435-3.643s.897-2.586 1.216-2.94c.318-.354.696-.442.928-.442.232 0 .464.002.667.012.213.01.5-.08.782.598.29.698.985 2.41 1.07 2.585.086.175.144.38.03.612-.116.233-.174.378-.343.58-.17.204-.357.455-.51.61-.17.174-.348.363-.15.71.198.348.88 1.454 1.89 2.354 1.3 1.158 2.396 1.517 2.744 1.687.348.17.552.145.756-.087.203-.233.87-1.014 1.103-1.362.232-.348.464-.29.782-.174.318.116 2.02.953 2.367 1.126.348.174.58.26.667.406.087.145.087.842-.203 1.658z"/></svg></a>
<audio id="bg-audio" loop style="display:none"><source id="bg-audio-src" src="" type="audio/mpeg"></audio>

<footer style="background:var(--dark);color:#fff;padding:44px 16px 22px;margin-top:30px">
  <div style="max-width:1320px;margin:0 auto;display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:32px">
    <div>
      <div style="font-size:30px;font-weight:900;color:var(--orange);margin-bottom:12px;font-family:'Poppins',sans-serif">TROGÜI</div>
      <p style="font-size:13px;color:#bbb;line-height:1.8">Tienda colombiana de confianza. Enviamos a todo el país con las mejores transportadoras.</p>
      <div style="display:flex;gap:10px;margin-top:14px">
        <a href="https://wa.link/lhneng" target="_blank" style="color:#25D366;font-size:24px">💬</a>
        <a href="https://www.instagram.com/store_trog" target="_blank" style="font-size:24px">📸</a>
        <a href="https://www.tiktok.com/@trogui_store" target="_blank" style="color:#fff;font-size:24px">🎵</a>
      </div>
    </div>
    <div>
      <h4 style="font-weight:800;margin-bottom:12px;color:var(--orange)">Contacto</h4>
      <ul style="list-style:none;font-size:13px;color:#bbb;line-height:2">
        <li>📞 320 657 2598</li>
        <li>📧 trogui.store@gmail.com</li>
        <li>🇨🇴 Colombia - Nacional</li>
      </ul>
    </div>
    <div>
      <h4 style="font-weight:800;margin-bottom:12px;color:var(--orange)">Transportadoras</h4>
      <ul style="list-style:none;font-size:13px;color:#bbb;line-height:2">
        <li>📦 Interrapidísimo</li>
        <li>📦 Coordinadora</li>
        <li>📦 Envia</li>
      </ul>
    </div>
    <div>
      <h4 style="font-weight:800;margin-bottom:12px;color:var(--orange)">Pagos</h4>
      <ul style="list-style:none;font-size:13px;color:#bbb;line-height:2">
        <li>💵 Contra Entrega</li>
        <li>🏦 Transferencia</li>
        <li>💳 Nequi / Daviplata</li>
      </ul>
    </div>
  </div>
  <div style="text-align:center;margin-top:32px;padding-top:20px;border-top:1px solid #333;font-size:12px;color:#888">© 2025 TROGÜI · Tienda Colombiana de Confianza 🇨🇴</div>
</footer>

<script>
const ADMIN_PASS = '4325';
let products = JSON.parse(localStorage.getItem('trogui_v2_products') || 'null') || [
  {id:'T001',name:'Escurridor Loza Con Tapa 65cm 2 Niveles',cat:'cocina',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1916715/1756999631142.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1886527/1753723291WhatsApp%20Image%202025-07-27%20at%209.38.06%20PM%20(1).jpeg'],
   price:139000,oldPrice:220000,
   desc:'Escurreplatos con tapa innovadora que mantiene el polvo fuera. Gran capacidad para platos, cuencos, tazas y cubiertos. Fabricado en acero inoxidable con revestimiento negro resistente al óxido. 4 ventosas para mayor estabilidad. Diseño 2 niveles para máximo aprovechamiento del espacio.',
   sold:89,stars:5,lastUnits:false,timer:4*60*60},
  {id:'T002',name:'Maquina Quita Callos Eléctrica Removedor',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1635913/1737489352Screenshot_11.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1176532/1725899615Removedor%20de%20callos%20de%20pies%20el%C3%A9ctrico%208.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1635913/1737489352Screenshot_9.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1176555/1761839437Removedor%20de%20callos%20de%20pies%20el%C3%A9ctrico%2015.jpg'],
   price:49000,oldPrice:89000,
   desc:'Elimina callos, piel dura y talones agrietados de forma rápida y segura. Diseño ergonómico con mango cómodo. Cuerpo portátil giratorio 360° con rodillos de partículas microabrasivas impermeables y fáciles de reemplazar. ¡Resultados desde la primera aplicación!',
   sold:340,stars:5,lastUnits:true,timer:30*60},
  {id:'T003',name:'Armario 3 Cuerpos Tela No Tejida',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/640729/1707407078WhatsApp%20Image%202024-02-08%20at%2010.40.11%20AM.jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/431969/16968755751695661087Alpi88EsRuch6KZ4F4ep1M2qUqYsW5QfL9bm9PAu.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2151831/177886033588130.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/697347/1774473913armarion%203.jpg'],
   price:85000,oldPrice:149000,
   desc:'Armario portátil de gran capacidad con barra para colgar ropa y 9 estantes. Construcción robusta con tela no tejida impermeable y tubos de acero de alta calidad. Ideal para organizar tu ropa, calzado y accesorios. Disponible en negro, gris, vino tinto y café.',
   sold:210,stars:4,lastUnits:false,timer:6*60*60},
  {id:'T004',name:'Zapatero Organizador 9 Niveles',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2151325/1778790428Captura%20de%20pantalla%202026-05-14%20152040.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2151325/1778790428Captura%20de%20pantalla%202026-05-14%20152147.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2139088/1777304863WhatsApp%20Image%202026-04-27%20at%2010.44.43.jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1876905/17526759711723776108Screenshot_2024_0807_221349.jpg'],
   price:65000,oldPrice:110000,
   desc:'Zapatero de 9 niveles con gran capacidad de almacenamiento. Organiza hasta 27 pares de zapatos. Estructura resistente y fácil de armar. Ideal para habitaciones, entradas y closets. Ahorra espacio y mantiene tu calzado ordenado y protegido.',
   sold:175,stars:5,lastUnits:false,timer:2*60*60},
  {id:'T005',name:'Hidrolavadora 6 Chorros Potentes',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1872413/1752165098Hidrolavadora%206%20chorros%203.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1872413/1752165098Hidrolavadora%206%20chorros%2010.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1872413/1752165098Hidrolavadora%206%20chorros%209.jpg'],
   price:89900,oldPrice:160000,
   desc:'Boquilla 6 en 1 con ángulos ajustables (0°, 15°, 25°, 40°). Presión máxima 450 PSI. Caudal 135L/h. Alcance más de 4 metros de altura. Lata de espuma incluida para mayor efecto limpiador. Perfecta para carros, motos, jardín, muebles y superficies difíciles.',
   sold:95,stars:5,lastUnits:true,timer:3*60*60},
  {id:'T006',name:'Organizador de Baño Universal 3 Niveles',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1815317/1762527418%F0%9F%98%8DORGANIZA%20TU%20BA%C3%91O,%20AHORRA%20ESPACIO%20CON%20EL%20ESTANTE%20ORGANIZADOR%20DE%20BA%C3%91O.LLEVALO%20A%20UN%20SUPER%20PRECIO%20.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1127641/17248682961698332152estante%20ba%C3%B1o.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1934840/1758597600Organizador%20de%20ba%C3%B1o%204.png'],
   price:75000,oldPrice:130000,
   desc:'Estante organizador de baño con diseño elegante en blanco. 3 niveles prácticos para organizar tus productos de higiene personal. Estructura de acero resistente. Profundidad de 25cm para máximo aprovechamiento. Se adapta a cualquier estilo de decoración.',
   sold:142,stars:5,lastUnits:false,timer:45*60},
  {id:'T007',name:'Perchero 4 Niveles Con Zapatero',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/671801/1708726377percheroZapatero4Niveles.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/233273/17019840001701984000Z%20-%20Tendedero%20-%201.jpg'],
   price:59000,oldPrice:99000,
   desc:'Rack multifuncional 4 en 1: cuelga ropa en la parte superior, organiza zapatos en la inferior y usa el nivel medio como mesa para bolsos y accesorios. Da glamour y orden a tu habitación. Diseño práctico y elegante que aprovecha cada rincón.',
   sold:198,stars:4,lastUnits:false,timer:60*60},
  {id:'T008',name:'Nebulizador Respirador Portátil',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2155990/1779384719SEC%20RESPIRADOR_-2%20(1).jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2148270/17784646881764466495D_NQ_NP_2X_786151-MLU78819306019_082024-F.webp'],
   price:55000,oldPrice:95000,
   desc:'Nebulizador portátil silencioso ideal para tratamientos respiratorios en casa. Fácil de usar, perfecto para toda la familia incluyendo niños y adultos mayores. Convierte el líquido en micropartículas para una absorción efectiva. Compacto y recargable.',
   sold:67,stars:5,lastUnits:false,timer:2*60*60},
  {id:'T009',name:'Freidora de Aire 12L Extra Capacidad + Accesorios',cat:'cocina',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2152705/1778955350ChatGPT%20Image%2016%20may%202026,%2001_10_20%20p.m..png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2152705/1778955351ChatGPT%20Image%2016%20may%202026,%2001_05_39%20p.m..png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2152705/1778955351ChatGPT%20Image%2016%20may%202026,%2001_08_19%20p.m..png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2154464/1779231764AIRFRYER......jpg'],
   price:235000,oldPrice:420000,
   desc:'🍟 Freidora de aire X HOME con extra capacidad 12L. Cocina más fácil, rápido y saludable con hasta 80% menos aceite. Panel moderno e intuitivo. Cocción rápida y uniforme. Incluye accesorios. Ideal para familias. Perfecto para papas, alitas, empanadas, pizzas y mucho más.',
   sold:55,stars:5,lastUnits:true,timer:24*60*60},
  {id:'T010',name:'Fire TV Stick 4K Control de Voz',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1884233/1753385392Imagen%20de%20WhatsApp%202025-07-24%20a%20las%2011.15.27_97e32929.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2000277/1763589760fire%20tv%20magis..jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2000277/1767724666fire.jpg'],
   price:99000,oldPrice:179000,
   desc:'Convierte cualquier TV en un Smart TV. Control por voz Alexa. Acceso a Netflix, YouTube, Disney+, Prime Video, HBO Max y más. Resolución hasta 4K. Wi-Fi integrado. Fácil instalación en minutos. Sin mensualidad, pago único.',
   sold:280,stars:5,lastUnits:false,timer:3*60*60},
  {id:'T011',name:'Lonchera Eléctrica Portátil',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2132401/1776528877Captura%20de%20pantalla%202026-04-18%20111044.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2150102/1778686955photo_2026-05-12_16-25-56.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2150102/1778686955photo_2026-05-12_16-25-58.jpg'],
   price:75000,oldPrice:130000,
   desc:'Calienta tu comida en cualquier lugar. Conexión USB para auto, oficina o viajes. Mantiene los alimentos calientes por horas. Libre de BPA, material de alta calidad. Fácil de limpiar. Ideal para el trabajo, viajes y quienes cuidan su alimentación.',
   sold:130,stars:5,lastUnits:false,timer:60*60},
  {id:'T012',name:'Audífonos Bluetooth con Pantalla LED',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1966260/1760735613WhatsApp%20Image%202025-10-17%20at%204.11.38%20PM%20(1).jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1510875/173214620317298658215.jpg'],
   price:59900,oldPrice:110000,
   desc:'Audífonos inalámbricos con pantalla digital que muestra el nivel de batería. Sonido de alta calidad. Conexión Bluetooth estable. Batería de larga duración. Diseño cómodo y plegable. Compatible con todos los teléfonos Android e iPhone. Incluye cable de carga.',
   sold:215,stars:4,lastUnits:false,timer:2*60*60},
  {id:'T013',name:'Kit Buceo Snorkel Máscara',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/683907/1709323851IMG-20240301-WA0039.jpg'],
   price:59900,oldPrice:105000,
   desc:'Equipo de snorkel completo para explorar el mundo submarino. Máscara de silicona de alta calidad con amplio campo visual. Tubo de respiración cómodo y antivaho. Ideal para playas, ríos y piscinas. Para adultos y niños. Perfecto para vacaciones.',
   sold:88,stars:4,lastUnits:false,timer:45*60},
  {id:'T014',name:'Audífonos Ambie Sound Oreja Abierta',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/372272/171837588557.PNG'],
   price:55000,oldPrice:98000,
   desc:'Auriculares de diseño oreja abierta: escuchas música y también tu entorno con seguridad. Bluetooth 5.2. 6 horas de reproducción + 24h con estuche de carga. Peso ultra ligero (4.2g por oreja). Impermeables IPX5. Micrófono integrado para llamadas. Ideal para deporte, trabajo y conducción.',
   sold:310,stars:5,lastUnits:false,timer:30*60},
  {id:'T015',name:'Proyector Portátil HD',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2028712/1766853261image%20-%202025-12-27T113356.503.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1213390/1726624197WhatsApp%20Image%202024-09-17%20at%208.40.44%20PM.jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1007720/1721785503WhatsApp%20Image%202024-07-23%20at%208.38.21%20PM.jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2011451/1764368578Proyector%20Portatil%203.jpg'],
   price:165000,oldPrice:290000,
   desc:'Proyector portátil con imagen HD nítida. Pantalla hasta 120 pulgadas. Conecta tu celular, USB, HDMI. Batería recargable para uso sin cables. Perfecto para cine en casa, presentaciones o viajes. Altavoz integrado. Compacto y fácil de transportar.',
   sold:72,stars:4,lastUnits:true,timer:6*60*60},
  {id:'T016',name:'Careta y Snorkel Kit Completo de Buceo',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1776906/1746026425WhatsApp%20Image%202025-04-29%20at%202.21.01%20PM.jpeg'],
   price:69000,oldPrice:120000,
   desc:'Kit de buceo completo con máscara panorámica de cara completa y snorkel integrado. Campo de visión 180°. Anti-vaho avanzado. Válvula de purga. Fácil de ajustar para adultos. Ideal para vacaciones, esnórquel y exploración submarina. Incluye bolsa de transporte.',
   sold:64,stars:4,lastUnits:false,timer:90*60},
  {id:'T017',name:'Compresor de Aire Digital Portátil',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2128613/1776114630gl1.jpg'],
   price:89000,oldPrice:159000,
   desc:'Infla neumáticos de carros, motos y bicicletas. Pantalla LED que muestra la presión actual. Apagado automático al alcanzar la presión deseada. Batería recargable interna. Linterna LED integrada para uso nocturno. Compacto y fácil de llevar en el maletero.',
   sold:145,stars:5,lastUnits:false,timer:4*60*60},
  {id:'T018',name:'Afeitadora 3 en 1 Recargable',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/241636/17019755901701975590Screenshot_139.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2084758/1771097372202211292725100.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2084757/17710973659488ed82-c5b6-4498-986a-9d569175b40b.webp'],
   price:55000,oldPrice:98000,
   desc:'Afeitadora multifuncional 3 en 1: rasura, recorta y perfilador de precisión. Recargable USB. Cuchillas de acero inoxidable. Cabezal lavable. Apta para uso en seco y húmedo. Ideal para barba, bigote y cuello. Para hombres que quieren verse siempre impecables.',
   sold:189,stars:4,lastUnits:false,timer:60*60},
  {id:'T019',name:'Organizador de Condimentos Giratorio x18',cat:'cocina',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1908987/1769180297Organizador%20De%20Condimentos%20Giratorio%20X18_2.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1908987/1769180289Organizador%20De%20Condimentos%20Giratorio%20X18.png'],
   price:69000,oldPrice:120000,
   desc:'Organizador giratorio con 18 frascos incluidos. Base 360° para acceder fácilmente a todos tus condimentos. Añade elegancia y orden a tu cocina. Frascos herméticos de alta calidad. Etiquetas incluidas para identificar cada especia. Ahorra espacio y tiempo al cocinar.',
   sold:230,stars:5,lastUnits:false,timer:2*60*60},
  {id:'T020',name:'Tensiómetro Digital con Voz',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2109657/17738473851771888968tensiometro%203.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2130492/17763345271000000105.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2093052/17719638461720884377leman.webp'],
   price:55000,oldPrice:95000,
   desc:'Tensiómetro digital de brazo con voz en español. Mide presión arterial y pulso con alta precisión. Memoria para múltiples usuarios. Detecta irregularidades cardíacas. Pantalla grande y fácil de leer. Perfecto para adultos mayores y personas con hipertensión.',
   sold:198,stars:5,lastUnits:false,timer:3*60*60},
  {id:'T021',name:'Oxímetro Digital de Pulso',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2152741/1778960041WhatsApp%20Image%202026-04-09%20at%204.57.08%20PM.jpeg'],
   price:28000,oldPrice:55000,
   desc:'Oxímetro de pulso rápido y preciso. Mide la saturación de oxígeno en sangre (SpO2) y la frecuencia cardíaca en segundos. Pantalla OLED de fácil lectura. Ideal para control en casa. Funciona con 2 pilas AAA. Compacto y liviano. Esencial para el cuidado de la salud.',
   sold:415,stars:5,lastUnits:false,timer:30*60},
  {id:'T022',name:'Estuche Huevo Juego Cubiertos 24 Pzas',cat:'cocina',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2111127/1773974903cubiertos-forma-de-huevo.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2111127/1773974903WhatsApp%20Image%202026-03-19%20at%2019.31.35.jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2111127/1773974903public.jpeg'],
   price:89900,oldPrice:160000,
   desc:'Elegante juego de cubiertos 24 piezas presentado en estuche con forma de huevo. Acero inoxidable de alta calidad, resistente y duradero. Incluye tenedores, cucharas, cuchillos y cucharitas. Perfecto como regalo o para tu mesa del diario. Presentación lujosa.',
   sold:145,stars:5,lastUnits:true,timer:60*60},
  {id:'T023',name:'Iniciador de Batería Cargador 12V Inteligente',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2077325/1770401328cargador-bateria-para-carros-y-motos-12v-6-amp.webp'],
   price:69000,oldPrice:125000,
   desc:'¿Batería muerta? ¡Nunca más! Cargador inteligente 12V para carros y motos. Diagnostica, carga y repara baterías. Protección contra cortocircuito y sobrecarga. Pantalla indicadora de estado. Fácil conexión con pinzas tipo cocodrilo. Imprescindible para tu vehículo.',
   sold:110,stars:5,lastUnits:false,timer:4*60*60},
  {id:'T024',name:'Taladro Inalámbrico Profesional',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2043245/176901088317676296461761583467110.jpg'],
   price:125000,oldPrice:220000,
   desc:'Taladro inalámbrico de alto rendimiento. Batería recargable de larga duración. Modos perforación y destornillador. Incluye set de brocas. Diseño ergonómico anti-fatiga. Ideal para hogar, trabajos de mantenimiento, instalación de muebles y mucho más.',
   sold:78,stars:4,lastUnits:true,timer:8*60*60},
  {id:'T025',name:'Organizador de Ollas y Tapas',cat:'cocina',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2126689/1775838291ollas%201.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2126689/1775838291ollas.webp'],
   price:59000,oldPrice:99000,
   desc:'Organiza tus ollas y tapas de forma eficiente. Divisores ajustables. Estructura resistente de acero. Ahorra espacio en cajones y gabinetes. Fácil de instalar. Compatible con ollas de todos los tamaños. Mantén tu cocina limpia, ordenada y lista para cocinar.',
   sold:165,stars:5,lastUnits:false,timer:45*60},
  {id:'T026',name:'Consola Retro Portátil R36S 15000 Juegos',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2008339/1764092783video.png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2008339/1764092784video%20(3).png','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2008339/1764092783video%20(1).png'],
   price:179000,oldPrice:320000,
   desc:'Consola portátil retro con más de 15,000 juegos preinstalados. Pantalla IPS de 3.5". Batería 3500mAh. Soporte para PS1, GBA, SNES, NES, Sega y más. Controles cómodos tipo GameBoy. Salida HDMI para jugar en TV. ¡El regalo ideal para los amantes de los videojuegos!',
   sold:92,stars:5,lastUnits:true,timer:12*60*60},
  {id:'T027',name:'Juguete Perro Robot Interactivo',cat:'juguetes',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2001384/1763739468D_Q_NP_2X_957362-MLA96425148737_102025-T.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1995592/1763073811Lobo%20movimiento.JPG'],
   price:109000,oldPrice:190000,
   desc:'Adorable perro robot interactivo que camina, baila y hace trucos. Responde al tacto y voz. Múltiples modos de juego. Pilas incluidas. Seguro para niños desde 3 años. El compañero perfecto para los más pequeños. Les encantará su pelaje suave y sus movimientos reales.',
   sold:88,stars:5,lastUnits:false,timer:3*60*60},
  {id:'T028',name:'TV Stick Android HD Streaming',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1965814/1760720817sin%20(3).JPG','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1965814/1760720817sin%20(1).JPG'],
   price:89000,oldPrice:160000,
   desc:'Convierte tu TV en Smart TV al instante. Soporte Android con acceso a Play Store. Reproducción HD/4K. Wi-Fi integrado. Control remoto incluido. Accede a Netflix, YouTube, Prime Video y todas tus apps favoritas. Sin mensualidades. Plug & Play en minutos.',
   sold:195,stars:4,lastUnits:false,timer:2*60*60},
  {id:'T032',name:'Parlante JBL Boombox 3 Mini LED',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/827576/1714766066425321695_7609998525712221_4306800719508153007_n.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/827576/171476606615a438cb39617cc026517efb13949d88.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/827576/1714766066427540955_7456219337747742_1902590583006082060_n.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/827576/1714766066421837815_6940456066081576_2793123522810349384_n.jpg'
],
price:89000,oldPrice:169000,
desc:'Disfruta un sonido potente con bajos profundos y luces LED que siguen el ritmo de la música. Ideal para reuniones, fiestas, paseos y uso diario. Conexión Bluetooth rápida, diseño portátil y batería recargable para llevar la diversión a cualquier lugar.',
sold:184,stars:5,lastUnits:false,timer:3*60*60},

{id:'T033',name:'Parlante JBL Wind 3 Portátil',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1618784/1736435001WhatsApp%20Image%202025-01-09%20at%2010.00.48%20AM%20(1).jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1618784/1736435000WhatsApp%20Image%202025-01-09%20at%2010.00.51%20AM.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1618784/1736435000WhatsApp%20Image%202025-01-09%20at%2010.00.51%20AM%20(2).jpeg'
],
price:55000,oldPrice:119000,
desc:'Perfecto para bicicleta, moto o caminatas. Incluye Bluetooth, radio FM, entrada auxiliar y reproducción por microSD. Resistente a salpicaduras y fácil de instalar. Lleva tu música favorita a cualquier aventura.',
sold:223,stars:5,lastUnits:false,timer:2*60*60},

{id:'T034',name:'Parlante JBL Flip 6 Con Marquilla',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2133937/1776781569Captura%20de%20pantalla%202026-04-21%20092329.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2133937/1776781569Imagen%20de%20WhatsApp%202024-12-20%20a%20las%2015.00.38_6450639f%20(1).jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2133937/1776781569WhatsApp%20Image%202025-08-19%20at%2010.38.44%20AM%20(1).jpeg'
],
price:65000,oldPrice:139000,
desc:'Sonido potente y diseño moderno para disfrutar música en cualquier lugar. Conexión Bluetooth estable, batería recargable y excelente calidad de audio para reuniones, oficina o entretenimiento diario.',
sold:157,stars:5,lastUnits:false,timer:2*60*60},

{id:'T035',name:'Parlante JBL Charge 5',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/675632/1708974851photo_5089455367687089337_x%20(1).jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1616579/1736272346image%20(4).png',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/675632/1708974851photo_5089455367687089390_y.jpg'
],
price:63000,oldPrice:129000,
desc:'Potencia, portabilidad y autonomía en un solo equipo. Ideal para quienes buscan un parlante compacto con gran volumen y sonido envolvente para fiestas, viajes o uso diario.',
sold:245,stars:5,lastUnits:false,timer:4*60*60},

{id:'T036',name:'Consola Q9 Pro Retro',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1974861/17614359421.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1974861/17614359423.webp'
],
price:169000,oldPrice:289000,
desc:'Con miles de juegos clásicos incluidos, controles inalámbricos y salida HDMI, esta consola es perfecta para disfrutar en familia. Revive la nostalgia y diviértete durante horas sin necesidad de internet.',
sold:132,stars:5,lastUnits:false,timer:5*60*60},

{id:'T037',name:'Consola Retro 10000 Juegos 4K',cat:'tecnologia',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/355902/17018761741701876174da165ae2e8f6121968db11c04c1586f6-product.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1202261/1760218038Dise%C3%B1o%20sin%20t%C3%ADtulo%20-%202025-08-13T111659.315.png'
],
price:69000,oldPrice:149000,
desc:'Más de 10.000 juegos clásicos en una sola consola. Incluye dos controles inalámbricos para jugar con amigos o familiares. Compatible con televisores mediante HDMI y calidad de imagen 4K.',
sold:311,stars:5,lastUnits:false,timer:3*60*60},

{id:'T038',name:'Termo Premium 3 En 1',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1223914/1726847960termo3.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1223914/1726847960451034626_18030781265116909_6319577442867853304_n.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1223914/1726847960termo33.webp'
],
price:49000,oldPrice:99000,
desc:'Mantén tus bebidas frías o calientes por más tiempo. Diseño elegante, práctico y resistente para oficina, gimnasio, universidad o viajes. Ideal para quienes buscan comodidad todos los días.',
sold:287,stars:5,lastUnits:false,timer:2*60*60},

{id:'T039',name:'Depilador Recargable',cat:'salud',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1884098/1753379889depilador.JPG'
],
price:39000,oldPrice:79000,
desc:'Elimina el vello de forma rápida, cómoda y sin irritaciones. Diseño compacto y recargable para usar en casa o llevar de viaje. Ideal para mantener una apariencia impecable en minutos.',
sold:176,stars:5,lastUnits:false,timer:2*60*60},

{id:'T040',name:'Filtro Universal Para Ducha',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1876903/1752676012filtro%20de%20ducha%20universal.JPG'
],
price:55000,oldPrice:110000,
desc:'Ayuda a reducir cloro, impurezas y malos olores del agua. Protege tu piel y cabello mientras disfrutas de una ducha más saludable. Fácil instalación compatible con la mayoría de duchas estándar.',
sold:198,stars:5,lastUnits:false,timer:3*60*60},

{id:'T041',name:'Lámpara Solar 50W',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1209291/1740405054lampara%20sola%2050w%20gd.JPG'
],
price:59900,oldPrice:129900,
desc:'Ilumina patios, terrazas, fincas y exteriores sin aumentar el consumo de energía. Funciona con energía solar, brinda excelente iluminación nocturna y es resistente para uso exterior.',
sold:165,stars:5,lastUnits:false,timer:2*60*60},

{id:'T042',name:'Cámara Digital Para Niños',cat:'juguetes',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1584177/1734034325IMG_6987.JPG',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1584177/1734034325IMG_6988.JPG'
],
price:49000,oldPrice:99000,
desc:'Estimula la creatividad de los niños permitiéndoles tomar fotos y grabar videos fácilmente. Resistente, segura y divertida. Un regalo ideal para desarrollar imaginación y aprendizaje.',
sold:224,stars:5,lastUnits:false,timer:3*60*60},

{id:'T043',name:'Almohada Ortopédica Premium',cat:'salud',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/655374/1729089926ALMOHADA.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/655374/1729089926ALMOHADA%20ORTOPEDICA223.webp'
],
price:45000,oldPrice:95000,
desc:'Diseñada para brindar soporte cervical y mejorar la postura al dormir. Ayuda a disminuir molestias en cuello y espalda, proporcionando un descanso más cómodo y reparador.',
sold:354,stars:5,lastUnits:false,timer:2*60*60},

{id:'T044',name:'Ejercitador De Manos Ajustable',cat:'salud',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/323974/17018817971701881797D_NQ_NP_646020-MCO70479652653_072023-O.jpeg'
],
price:28000,oldPrice:59000,
desc:'Fortalece dedos, manos y antebrazos. Ideal para deportistas, músicos, rehabilitación física o personas que desean mejorar fuerza y resistencia de agarre.',
sold:173,stars:5,lastUnits:false,timer:60*60},

{id:'T045',name:'Rodillera De Compresión',cat:'salud',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/587016/1704688558rodillera.jpeg'
],
price:29000,oldPrice:59000,
desc:'Brinda soporte y estabilidad durante caminatas, ejercicio o actividades diarias. Ayuda a reducir molestias articulares y mejora la sensación de seguridad al moverte.',
sold:191,stars:5,lastUnits:false,timer:60*60},

{id:'T046',name:'Masajeador Facial Antiarrugas',cat:'belleza',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1243990/17272726811718573660MASAJEADOR%20FACIAL.jpeg'
],
price:49000,oldPrice:99000,
desc:'Ayuda a mejorar la apariencia de la piel mediante suaves vibraciones que favorecen la relajación facial. Ideal para complementar tu rutina de cuidado personal desde casa.',
sold:145,stars:5,lastUnits:false,timer:2*60*60},

{id:'T047',name:'Maletín Antirrobo Impermeable',cat:'accesorios',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/870258/1716052118maleta%20manos%20Libres.JPG',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/870258/1766246446Mochila%20Cruzada%20Impermeable%20Antirrobo%20-%20Carga%20USB%20ND.jpg'
],
price:55000,oldPrice:119000,
desc:'Protege tus pertenencias con un diseño moderno, impermeable y resistente. Cuenta con múltiples compartimentos para organizar celular, billetera, llaves y accesorios de forma segura.',
sold:278,stars:5,lastUnits:false,timer:3*60*60},

{id:'T048',name:'Reloj Despertador Con Proyector LED',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2160113/1779813291RELOJ%20PROYECTOR%20LED%208.JPG',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2160113/1779813291RELOJ%20PROYECTOR%20LED%2014.jpg'
],
price:55000,oldPrice:119000,
desc:'Visualiza la hora proyectada en techo o pared sin levantarte de la cama. Incluye temperatura, humedad y pantalla LED de fácil lectura. Perfecto para dormitorios modernos.',
sold:169,stars:5,lastUnits:false,timer:2*60*60},

{id:'T049',name:'Maleta Cabina De Viaje',cat:'viajes',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1358873/1741453295Maleta%20Amazon%20Con%20Zapatero%20Gris%20A.JPG',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1358873/1741453295Maleta%20Amazon%20Con%20Zapatero%20Lila%206.jpg'
],
price:89000,oldPrice:169000,
desc:'Ideal para viajes cortos, gimnasio o escapadas de fin de semana. Amplio espacio interior, compartimentos funcionales y diseño elegante para llevar todo organizado.',
sold:144,stars:5,lastUnits:false,timer:3*60*60},

{id:'T050',name:'Molino Eléctrico Multiusos',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1918942/1757248815IMG_0493.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2148755/1778530520Molinillo%20de%20caf%C3%A9%20el%C3%A9ctrico%20de%20cocina%20Grande%202.jpg'
],
price:49900,oldPrice:99900,
desc:'Muele café, especias, semillas y otros ingredientes en segundos. Potente, compacto y fácil de usar. Perfecto para quienes disfrutan preparar alimentos frescos en casa.',
sold:188,stars:5,lastUnits:false,timer:2*60*60},

{id:'T051',name:'Organizador Para Lavadora',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/337207/17018798431701879843WhatsApp%20Image%202023-07-31%20at%208.15.30%20PM.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/591719/1704992977ORGANIZADOR%20LAVADORA..jpg'
],
price:79000,oldPrice:149000,
desc:'Aprovecha el espacio sobre la lavadora y mantén detergentes, suavizantes y accesorios siempre organizados. Ideal para baños y zonas de lavado pequeñas.',
sold:152,stars:5,lastUnits:false,timer:3*60*60},
  {id:'T029',name:'Kit Máquina Afeitadora para Mascotas',cat:'accesorios',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1942148/17591538771992f34d9d2-electrohogarcyc-gneuklg0t7n-iest5inm75d.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1942148/17591538771992f34e3e7-electrohogarcyc-gneuklg0t7n-bteqsvyf7nu.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1942148/17591538771992f34d56e-electrohogarcyc-gneuklg0t7n-3nqhgzuzcf.jpg'],
   price:59000,oldPrice:105000,
   desc:'Kit completo para peluquería de mascotas en casa. Silencioso para no asustar a tu perro o gato. Cuchillas de acero inoxidable ajustables. Recargable USB. Incluye accesorios para diferentes longitudes de pelo. Ahorra en peluquería y cuida a tu mascota con amor.',
   sold:142,stars:5,lastUnits:false,timer:60*60},
  {id:'T052',name:'Estufa Eléctrica Doble Puesto',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2031440/1767718572Haac6d35fa02d468eb197d8b2a91bd799Y.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2002901/1763821917D_NQ_NP_2X_833686-MCO79108625469_092024-F.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1646802/1738172135estufas.webp'
],
price:65000,oldPrice:129000,
desc:'Cocina de forma rápida y práctica sin necesidad de gas. Cuenta con dos puestos para preparar varias recetas al mismo tiempo. Ideal para apartamentos, oficinas, fincas o estudiantes.',
sold:247,stars:5,lastUnits:false,timer:3*60*60},

{id:'T053',name:'Estufa Eléctrica Un Puesto',cat:'hogar',
imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2129027/1776178830estu.webp'],
price:49000,oldPrice:99000,
desc:'Solución práctica para cocinar en espacios reducidos. Compacta, fácil de transportar y perfecta para apartamentos, habitaciones, oficinas o viajes.',
sold:196,stars:5,lastUnits:false,timer:2*60*60},

{id:'T054',name:'Buzo Colombia Mundial Cuello Alto',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2160515/1779829600COOMBIA%20AMARILLO%20NUEVO.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2160515/1779829600COOMBIA%20NEGRO%20NUEVO.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2160515/1779829600COOMBIA%20azul%20oscuroNUEVO.jpg'
],
price:115000,oldPrice:199000,
desc:'Chaqueta premium inspirada en la Selección Colombia. Fabricada en tela de excelente calidad, cuello alto, cremallera completa y tallas para hombre y mujer. Ideal para lucir la pasión por Colombia con estilo.',
sold:312,stars:5,lastUnits:false,timer:4*60*60},

{id:'T055',name:'Buzo Junior FC',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2080820/17707696941000000157.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2080820/17707696941000000156.jpg'
],
price:95000,oldPrice:169000,
desc:'Diseño deportivo cómodo y moderno para los verdaderos hinchas del Junior. Perfecto para uso diario, eventos deportivos o regalar a un apasionado del fútbol.',
sold:154,stars:5,lastUnits:false,timer:2*60*60},

{id:'T056',name:'Buzo Deportivo Cali Bordado',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2044517/1769109981WhatsApp%20Image%202026-01-15%20at%202.57.16%20PM.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2044517/1769109984WhatsApp%20Image%202026-01-15%20at%202.57.15%20PM.jpeg'
],
price:115000,oldPrice:199000,
desc:'Buzo premium bordado para los seguidores del Deportivo Cali. Confección cómoda, excelente acabado y diseño elegante para demostrar tu pasión verdiblanca.',
sold:142,stars:5,lastUnits:false,timer:3*60*60},

{id:'T057',name:'Buzo Millonarios FC',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2080700/1770761411MILLONARIOS%201.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2080700/1770761411MILLONARIOS%203.jpg'
],
price:115000,oldPrice:199000,
desc:'Prenda deportiva diseñada para los aficionados embajadores. Tela cómoda, excelente calidad y acabados modernos para cualquier ocasión.',
sold:201,stars:5,lastUnits:false,timer:3*60*60},

{id:'T058',name:'Buzo América De Cali',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1836238/1748668187AMERICA.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1836238/1748668186ROJO.jpg'
],
price:115000,oldPrice:199000,
desc:'Lleva con orgullo los colores de La Mechita. Diseño moderno, cómodo y perfecto para acompañarte en cualquier momento del día.',
sold:263,stars:5,lastUnits:false,timer:4*60*60},

{id:'T059',name:'Saco América De Cali Premium',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1735937/1770477714AMERICA%20RAMON%20GARRA%204.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1735937/1770477714COLLAGE%20AMERICA.jpg'
],
price:95000,oldPrice:169000,
desc:'La pasión de un pueblo reflejada en una prenda cómoda y elegante. Ideal para hinchas que quieren representar al América dentro y fuera del estadio.',
sold:174,stars:5,lastUnits:false,timer:2*60*60},

{id:'T060',name:'Buzo Atlético Nacional',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1666448/1763070522NACIONAL%20RAMON%20VERTICAL%204.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1669284/1763069456collage%203.jpg'
],
price:95000,oldPrice:179000,
desc:'Diseñado para los verdaderos verdolagas. Cómodo, resistente y con acabados de alta calidad para acompañarte durante todo el año.',
sold:286,stars:5,lastUnits:false,timer:3*60*60},

{id:'T061',name:'Buzo Independiente Medellín',cat:'ropa',
imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1851963/1750177022WhatsApp%20Image%202025-06-17%20at%2010.41.38.jpeg'],
price:115000,oldPrice:199000,
desc:'Representa al Poderoso de la Montaña con una prenda deportiva cómoda, moderna y perfecta para cualquier ocasión.',
sold:135,stars:5,lastUnits:false,timer:2*60*60},

{id:'T062',name:'Buzo Once Caldas',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2077063/1775406122NEUMO%20ONCE%20CALDAS%201.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2077063/1775406123NEUMO%20ONCE%20CALDAS%203.jpg'
],
price:115000,oldPrice:199000,
desc:'Diseño exclusivo inspirado en uno de los equipos históricos del fútbol colombiano. Cómodo, elegante y de excelente calidad.',
sold:117,stars:5,lastUnits:false,timer:2*60*60},

{id:'T063',name:'Buzo Once Caldas Bordado',cat:'ropa',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1822990/1747409041ONCE-Photoroom.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1822990/1747409041WhatsApp%20Image%202025-05-15%20at%2018.11.49%20(1).jpeg'
],
price:95000,oldPrice:169000,
desc:'Acabados bordados premium y diseño elegante para quienes viven la pasión del Once Caldas todos los días.',
sold:121,stars:5,lastUnits:false,timer:2*60*60},

{id:'T064',name:'Buzo Colombia Petróleo',cat:'ropa',
imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2134937/1776822875WhatsApp%20Image%202026-04-21%20at%208.44.57%20PM.jpeg'],
price:115000,oldPrice:199000,
desc:'Edición especial con diseño moderno y colores llamativos. Ideal para fanáticos de la Selección Colombia que buscan destacar.',
sold:164,stars:5,lastUnits:false,timer:3*60*60},

{id:'T065',name:'Toldillo Plegable',cat:'bebes',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2147859/1778344866Toldillo-Plegable-BebeAzul3.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1593349/1734472536IMG-20241216-WA0045.jpg'
],
price:49000,oldPrice:99000,
desc:'Protege a tu bebé de mosquitos e insectos mientras duerme. Diseño plegable, liviano y fácil de transportar para usar en casa o viajes.',
sold:238,stars:5,lastUnits:false,timer:2*60*60},

{id:'T066',name:'Toldillo Para Bebés',cat:'bebes',
imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/921828/171900446117018815061701881506toldillo-mosquitero-bebes-cuna-plegable-cama-portatil-312012-importadora-blue-353152921_1200x1200.jpeg'],
price:59900,oldPrice:119900,
desc:'Brinda tranquilidad y protección mientras tu bebé descansa. Fácil de instalar y compatible con diferentes tipos de cunas.',
sold:207,stars:5,lastUnits:false,timer:2*60*60},

{id:'T067',name:'Silla Mecedora Para Bebé',cat:'bebes',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2015545/1764878056WhatsApp%20Image%202025-12-03%20at%2010.58.48%20AM.jpeg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2092041/1771882063mecedora%203.jpg'
],
price:119000,oldPrice:219000,
desc:'Ayuda a relajar y entretener al bebé gracias a su suave movimiento. Cómoda, segura y perfecta para los primeros meses de crecimiento.',
sold:148,stars:5,lastUnits:false,timer:3*60*60},

{id:'T068',name:'Juego De Ollas Premium',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2041825/1768875446w=1200,h=1200,fit=pad%20(12).webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1817856/1747071190Imagen%20de%20WhatsApp%202025-05-12%20a%20las%2012.31.21_2cd5bc55.jpg'
],
price:69900,oldPrice:149900,
desc:'Renueva tu cocina con un juego completo de ollas resistentes y elegantes. Distribuyen el calor uniformemente para cocinar de manera más eficiente.',
sold:293,stars:5,lastUnits:false,timer:3*60*60},

{id:'T069',name:'Sellador Y Cortador De Bolsas',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1960353/176014278933ea0d74-e47f-4d51-bcdf-9d1d818534f5.JPG',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2013355/1764696875bol.webp'
],
price:32000,oldPrice:69000,
desc:'Mantén tus alimentos frescos por más tiempo sellando bolsas en segundos. Fácil de usar, portátil y perfecto para la cocina diaria.',
sold:354,stars:5,lastUnits:false,timer:60*60},

{id:'T070',name:'Utensilio Multifuncional Cocina',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1515374/17485563742.jpg',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2126664/1775837217cocina.webp'
],
price:75000,oldPrice:139000,
desc:'Herramienta práctica que facilita múltiples tareas en la cocina. Ahorra tiempo y mejora la preparación de tus recetas favoritas.',
sold:138,stars:5,lastUnits:false,timer:2*60*60},
  {id:'T072',name:'Juego de Ollas Antiadherentes Premium',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2041825/1768875446w=1200,h=1200,fit=pad%20(12).webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1817856/1747071190Imagen%20de%20WhatsApp%202025-05-12%20a%20las%2012.31.21_2cd5bc55.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2041825/1768875445w=1200,h=1200,fit=pad%20(10).webp'],
 price:69900,oldPrice:139000,
 desc:'Renueva tu cocina con este completo juego de ollas antiadherentes. Distribuyen el calor de forma uniforme, reducen el consumo de aceite y facilitan la limpieza. Ideales para preparar tus recetas favoritas de manera rápida y práctica. Resistentes, elegantes y perfectas para el uso diario.',
 sold:201,stars:5,lastUnits:false,timer:3*60*60},

{id:'T073',name:'Sellador y Cortador de Bolsas Portátil',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1960353/176014278933ea0d74-e47f-4d51-bcdf-9d1d818534f5.JPG','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2013355/1764696875bol.webp'],
 price:32000,oldPrice:69000,
 desc:'Mantén tus alimentos frescos por más tiempo. Este práctico sellador y cortador portátil evita desperdicios, conserva snacks, arroz, café y mucho más. Funciona en segundos y ocupa muy poco espacio. Ideal para hogares organizados y ahorradores.',
 sold:263,stars:5,lastUnits:false,timer:2*60*60},

{id:'T074',name:'Utensilio Multifuncional de Cocina',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1515374/17485563742.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2126664/1775837217cocina.webp'],
 price:75000,oldPrice:129000,
 desc:'Herramienta versátil diseñada para facilitar múltiples tareas en la cocina. Ahorra tiempo en la preparación de alimentos y mejora la organización de tus espacios. Resistente, fácil de limpiar y perfecta para cualquier hogar moderno.',
 sold:116,stars:5,lastUnits:false,timer:2*60*60},

{id:'T075',name:'Organizador Metálico para Cocina',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2159999/1779807048ORGANIZADOR%20METALICO%20DE%20COCINA%201.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1085959/1723832912WhatsApp%20Image%202024-08-16%20at%2012.58.33%20PM.jpeg'],
 price:42000,oldPrice:79000,
 desc:'Aprovecha el espacio de tus paredes y mantén utensilios, cucharas y accesorios siempre organizados. Diseño resistente y elegante que ayuda a mantener la cocina ordenada y funcional. Fácil instalación y gran capacidad.',
 sold:171,stars:5,lastUnits:false,timer:60*60},

{id:'T076',name:'Set de Utensilios de Cocina 12 Piezas',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/377463/17018734491701873449Utensilio-de-cocina-12pz-Verde-1.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/377463/17018734491701873449Utensilio-de-cocina-12pz-Rojo-2.jpg'],
 price:49900,oldPrice:99000,
 desc:'Set completo de utensilios de silicona resistente al calor con elegantes mangos de madera. No raya ollas ni sartenes, es fácil de limpiar y aporta un toque moderno a tu cocina. Incluye soporte organizador para mantener todo en su lugar.',
 sold:312,stars:5,lastUnits:false,timer:3*60*60},

{id:'T077',name:'Gorro Terapéutico para Migraña y Dolor de Cabeza',cat:'salud',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/656487/1708057119WhatsApp%20Image%202023-08-29%20at%206.27.56%20PM%20(1).jpeg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/926788/171943595358b7d2b7-f548-4f85-9eaa-82dbfefe3d98.jpeg'],
 price:35000,oldPrice:69000,
 desc:'Alivio relajante para migrañas, estrés, cansancio visual y dolores de cabeza. Puede utilizarse frío o tibio para brindar una sensación inmediata de bienestar. Su diseño cómodo cubre completamente la zona afectada y ayuda a relajarte en minutos.',
 sold:289,stars:5,lastUnits:false,timer:60*60},

{id:'T078',name:'Radios Comunicadores Baofeng X2',cat:'tecnologia',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2034990/1768246197IMG_0355.jpeg'],
 price:75000,oldPrice:149000,
 desc:'Comunicación clara y estable para trabajo, seguridad, fincas, viajes y actividades al aire libre. Incluye dos radios, cargadores, auriculares y accesorios completos. Excelente alcance y batería de larga duración para mantenerte siempre conectado.',
 sold:152,stars:5,lastUnits:false,timer:3*60*60},

{id:'T079',name:'Sofá Inflable Portátil',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2130523/1776346965sofa%201.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2130523/1776346965SOFA%20AZUL.jpeg'],
 price:79000,oldPrice:149000,
 desc:'Descansa cómodamente en la playa, camping, parque o jardín. Se infla rápidamente y ofrece gran comodidad sin necesidad de muebles pesados. Ligero, resistente y fácil de transportar a cualquier lugar.',
 sold:136,stars:5,lastUnits:false,timer:2*60*60},

{id:'T080',name:'Destornillador Eléctrico Inalámbrico',cat:'herramientas',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1750036/1744224377DESTOR.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1750036/1768490298photo_2026-01-05_14-52-13.jpg'],
 price:49000,oldPrice:99000,
 desc:'Ideal para reparaciones en el hogar, muebles y proyectos de bricolaje. Facilita el trabajo, ahorra tiempo y reduce el esfuerzo. Diseño ergonómico, batería recargable y gran precisión para cualquier tarea.',
 sold:247,stars:5,lastUnits:false,timer:2*60*60},

{id:'T081',name:'Candado con Alarma para Moto',cat:'accesorios',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1882997/1753289533candado%20alarma.webp'],
 price:39000,oldPrice:79000,
 desc:'Protege tu motocicleta con este candado de alta resistencia equipado con alarma sonora. Detecta movimientos sospechosos y emite una potente alerta para disuadir robos. Seguridad adicional para tu tranquilidad.',
 sold:322,stars:5,lastUnits:false,timer:60*60},

{id:'T082',name:'Depiladora Trimmer Recargable 4 en 1',cat:'belleza',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2141242/1777486064gememy%20mujer%7D.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2141242/1777486062gemmey%20mujer.jpg'],
 price:49900,oldPrice:99000,
 desc:'Elimina vello facial y corporal de forma rápida, segura y sin irritaciones. Incluye diferentes cabezales para adaptarse a cada zona del cuerpo. Recargable, compacta y perfecta para mantener una apariencia impecable.',
 sold:183,stars:5,lastUnits:false,timer:2*60*60},

{id:'T083',name:'Aspiradora Inalámbrica 3 en 1',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1881968/1777060523ASPIRADORA%203%20EN%201.webp','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1881968/1777060523ASPIRAORA%203%20EN%201.webp'],
 price:65000,oldPrice:129000,
 desc:'Potente aspiradora portátil con gran capacidad de succión para hogar, oficina y automóvil. Elimina polvo, migas y suciedad en segundos. Ligera, recargable y fácil de usar, ideal para mantener cualquier espacio impecable.',
 sold:341,stars:5,lastUnits:false,timer:3*60*60},

{id:'T084',name:'Limpiador Eléctrico Multifuncional 9 en 1',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2102797/1776435194limpiadotr%209%20en%201.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2102797/1776435194CEPILLO%20LIM%20NPIADOR.webp'],
 price:65000,oldPrice:129000,
 desc:'Limpia baños, cocinas, juntas, vidrios y superficies difíciles sin esfuerzo. Incluye múltiples accesorios para diferentes usos. Ahorra tiempo y consigue resultados profesionales en cada limpieza.',
 sold:229,stars:5,lastUnits:false,timer:2*60*60},

{id:'T085',name:'Tapete Antideslizante para Baño',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1132537/1724951185TAPETE%20DE%20BA%C3%91O%202.webp'],
 price:32000,oldPrice:65000,
 desc:'Mayor seguridad y comodidad al salir de la ducha. Material absorbente, suave al tacto y con base antideslizante que ayuda a prevenir accidentes. Ideal para baños modernos y hogares con niños o adultos mayores.',
 sold:286,stars:5,lastUnits:false,timer:60*60},

{id:'T086',name:'Maleta Tocador para Niñas',cat:'infantil',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2010932/17643471924988295547701627829.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2010932/1768315742tocadr%202.jpg'],
 price:89000,oldPrice:159000,
 desc:'Divertido set de belleza infantil para estimular la imaginación y el juego creativo. Incluye accesorios organizados en una práctica maleta portátil. Ideal para regalar y disfrutar horas de entretenimiento.',
 sold:164,stars:5,lastUnits:false,timer:2*60*60},

{id:'T087',name:'Ducha Portátil Recargable',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2140982/1777474239ducha%203333.jpg'],
 price:55000,oldPrice:109000,
 desc:'Perfecta para camping, viajes, mascotas, jardines y emergencias. Funciona con batería recargable y proporciona un flujo constante de agua donde lo necesites. Compacta, práctica y fácil de transportar.',
 sold:198,stars:5,lastUnits:false,timer:2*60*60},

{id:'T088',name:'Máquina Eléctrica para Pintar',cat:'herramientas',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/422645/1741295923MAQUINA%20REAL.jpg'],
 price:135000,oldPrice:229000,
 desc:'Obtén acabados uniformes y profesionales en paredes, muebles y superficies. Reduce el tiempo de trabajo y evita marcas de brocha. Ideal para proyectos de remodelación, pintura doméstica y uso profesional.',
 sold:119,stars:5,lastUnits:false,timer:4*60*60},

{id:'T089',name:'Kit de Aseo para Bebé 9 Piezas',cat:'bebes',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1920100/1771462301BEBE%20REAL.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1920100/1757360432kit%20bebe%20N.webp'],
 price:49900,oldPrice:99000,
 desc:'Todo lo necesario para el cuidado diario de tu bebé en un práctico estuche portátil. Incluye accesorios seguros y diseñados especialmente para los más pequeños. Ideal para el hogar y para llevar de viaje.',
 sold:274,stars:5,lastUnits:false,timer:2*60*60},

{id:'T090',name:'Electroestimulador de Gimnasia Pasiva',cat:'salud',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/2086052/1771287122ELETRODO.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/2086052/1771287122ELECTP.jpg'],
 price:45000,oldPrice:89000,
 desc:'Ayuda a relajar músculos cansados, aliviar tensiones y complementar rutinas de bienestar. Cuenta con diferentes niveles de intensidad y programas de masaje para adaptarse a tus necesidades diarias.',
 sold:205,stars:5,lastUnits:false,timer:60*60},
{id:'T091',name:'Juego de Tapetes Antideslizantes',cat:'hogar',
 imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1951912/1759788205nuebo%20tap.jpg'],
 price:45000,oldPrice:89000,
 desc:'Protege tus pisos y añade confort a cualquier espacio del hogar. Material resistente, fácil de limpiar y diseño moderno que combina con cualquier decoración. Ideal para baños, habitaciones y salas.',
 sold:158,stars:5,lastUnits:false,timer:60*60},
{id:'T071',name:'Organizador Metálico De Cocina',cat:'hogar',
imgs:[
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/2159999/1779807048ORGANIZADOR%20METALICO%20DE%20COCINA%201.webp',
'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1085959/1723832912WhatsApp%20Image%202024-08-16%20at%2012.58.33%20PM.jpeg'
],
price:42000,oldPrice:89000,
desc:'Organiza utensilios, especias y accesorios aprovechando el espacio de las paredes. Diseño resistente y moderno para una cocina más ordenada.',
sold:225,stars:5,lastUnits:false,timer:2*60*60},
  {id:'T030',name:'Power Bank 10.000mAh Con Cables Incluidos',cat:'tecnologia',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1971753/176125897513ee3767-e1b3-4979-b91e-60045d161bc3.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1971753/176125897598402836-63d7-47d1-b973-db94c2fe68f0.jpg'],
   price:85000,oldPrice:149000,
   desc:'Power Bank 10,000mAh con carga rápida. Entradas: Tipo C y Micro USB. Salidas: USB, Tipo C, Lightning. Compatible con iPhone, Samsung, Xiaomi y todos los celulares. Cables incluidos. Diseño compacto y elegante. Perfecto para viajes, trabajo y emergencias.',
   sold:268,stars:5,lastUnits:false,timer:4*60*60},
  {id:'T031',name:'Báscula Inteligente Bluetooth Análisis Corporal',cat:'salud',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1930136/1758208266BASCULA%20BLUETOOTH%208.jpg','https://d39ru7awumhhs2.cloudfront.net/colombia/products/1930136/1758208266BASCULA%20BLUETOOTH%2010.jpg'],
   price:55000,oldPrice:99000,
   desc:'Báscula inteligente con análisis corporal completo: peso, grasa, músculo, agua y más. Sincronización Bluetooth con tu celular. Compatible con Apple Health y Samsung Health. Capacidad hasta 180kg. Vidrio templado resistente. Pantalla LCD clara. Multiusuario para toda la familia.',
   sold:188,stars:5,lastUnits:false,timer:3*60*60},
  {id:'T032',name:'Perchero con Cubierta Organizador',cat:'hogar',
   imgs:['https://d39ru7awumhhs2.cloudfront.net/colombia/products/1900120/1755196031WhatsApp%20Image%202025-08-14%20at%201.16.21%20PM.jpeg'],
   price:67000,oldPrice:119000,
   desc:'Perchero con cubierta protectora que mantiene tu ropa libre de polvo y humedad. Varios niveles de organización. Estructura robusta y estable. Ideal para dormitorios, entradas y cuartos pequeños. Fácil de armar, sin herramientas. Solución elegante para organizar tu ropa.',
   sold:99,stars:4,lastUnits:false,timer:90*60},
];

let reviews = JSON.parse(localStorage.getItem('trogui_reviews') || 'null') || [
  {name:'Valentina Torres',city:'Bogotá',stars:5,text:'Me llegó en 4 días!! El producto está 10/10, lo recomiendo mucho 😍'},
  {name:'Juan Camilo Restrepo',city:'Medellín',stars:5,text:'Pagué contra entrega y todo salió perfecto. La calidad es increíble, gracias TROGÜI!'},
  {name:'Luisa Fernanda Gómez',city:'Cali',stars:4,text:'Muy buen producto, llegó bien empacado. Lo recomiendo!'},
  {name:'Andrés Felipe Ospina',city:'Bucaramanga',stars:5,text:'Segunda vez que compro aquí y siempre quedo satisfecho. 100% confiable.'},
  {name:'Natalia Suárez',city:'Barranquilla',stars:5,text:'Excelente! El quita callos funcionó de maravilla desde el primer uso!'},
];

let cart = [];
let orders = JSON.parse(localStorage.getItem('trogui_orders') || '[]');
let currentOrderProduct = null;
let timers = {};
let sliderIdx = 0;
let visitors = Math.floor(Math.random()*38)+12;
let rouletteSpun = false;
let rouletteInactivityTimer = null;

// ========== INIT ==========
document.addEventListener('DOMContentLoaded', () => {
  loadSettings();
  renderProducts(products);
  startSlider();
  startShowcase();
  startNotifications();
  startShakeLoop();
  updateVisitors();
  startInactivityWatcher();
  drawRoulette();
  openProductFromHash();
});

function loadSettings(){
  const tb = localStorage.getItem('trogui_topbar');
  if(tb) document.getElementById('topbar-text').textContent = tb;
  const pt = localStorage.getItem('trogui_prod_title');
  if(pt) document.getElementById('products-title').innerHTML = pt;
  const au = localStorage.getItem('trogui_audio');
  if(au){ document.getElementById('bg-audio-src').src=au; document.getElementById('bg-audio').load(); document.getElementById('bg-audio').play().catch(()=>{}); }
}

// ========== SLIDER ==========
function moveSlider(d){ sliderIdx=(sliderIdx+d+3)%3; updateSlider(); }
function goSlide(i){ sliderIdx=i; updateSlider(); }
function updateSlider(){
  document.getElementById('slider-track').style.transform=`translateX(-${sliderIdx*100}%)`;
  document.querySelectorAll('.dot').forEach((d,i)=>d.classList.toggle('active',i===sliderIdx));
  document.querySelectorAll('.slide').forEach((s,i)=>{
    s.classList.remove('slide-visible');
    if(i===sliderIdx){ void s.offsetWidth; s.classList.add('slide-visible'); }
  });
}
function startSlider(){ updateSlider(); setInterval(()=>moveSlider(1), 6000); }

// ========== SLIDER PRODUCT SHOWCASE ==========
let showcaseIdx=0;
function startShowcase(){
  const pool = products.filter(p=>p.imgs&&p.imgs.length).slice(0,20);
  if(!pool.length) return;
  const img = document.getElementById('showcase-img');
  const tag = document.getElementById('showcase-tag');
  if(!img||!tag) return;
  function render(){
    const p = pool[showcaseIdx % pool.length];
    img.classList.remove('show'); tag.classList.remove('show');
    setTimeout(()=>{
      img.src = p.imgs[0];
      tag.textContent = '$'+fmt(p.price);
      img.classList.add('show'); tag.classList.add('show');
    }, 350);
    showcaseIdx++;
  }
  render();
  setInterval(render, 7000);
}

// ========== FORMAT ==========
function fmt(n){ return Number(n).toLocaleString('es-CO'); }

// ========== PRODUCTS ==========
function renderProducts(prods){
  const grid = document.getElementById('products-grid');
  grid.innerHTML = '';
  if(prods.length===0){ grid.innerHTML='<div style="grid-column:1/-1;text-align:center;padding:40px;color:var(--gray);font-size:16px">😕 No se encontraron productos</div>'; return; }
  prods.forEach(p => {
    const disc = Math.round((1-p.price/p.oldPrice)*100);
    const img = p.imgs && p.imgs[0] ? p.imgs[0] : 'https://via.placeholder.com/400x300?text=TROGUI';
    const el = document.createElement('div');
    el.className = 'product-card';
    el.id = 'card-'+p.id;
    el.innerHTML = `
      <div class="product-img-wrap" onclick="openModal('${p.id}')">
        <img src="${img}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/400x300?text=TROGUI'">
        <div class="badge-off">-${disc}% OFF</div>
        <div class="badge-sold-c">✅ ${p.sold}+ vendidos</div>
        ${p.lastUnits?'<div class="badge-last">⚠️ ¡Últimas!</div>':''}
      </div>
      <div class="product-info" onclick="openModal('${p.id}')">
        <div class="product-name">${p.name}</div>
        <div class="stars">${'⭐'.repeat(p.stars)}<span>(${p.stars}.0)</span></div>
        <div class="price-wrap">
          <span class="price-old">$${fmt(p.oldPrice)}</span>
          <span class="price-new">$${fmt(p.price)}</span>
        </div>
        <div class="timer-badge" id="timer-${p.id}">⏰ Cargando...</div>
        <div class="free-ship">🚚 Envío GRATIS toda Colombia</div>
        <div class="contra-e">💵 Pago Contra Entrega disponible</div>
      </div>
      <div class="card-btns">
        <button class="btn-add" onclick="event.stopPropagation();addToCart('${p.id}')">🛒 Al Carrito</button>
        <button class="btn-pedir" id="pedir-${p.id}" onclick="event.stopPropagation();openOrderDirect('${p.id}')">🔥 ¡Pedir Ya!</button>
      </div>`;
    grid.appendChild(el);
    startTimer(p.id, p.timer);
  });
}

function filterCat(cat, el){
  document.querySelectorAll('.nav-inner a').forEach(a=>a.classList.remove('active'));
  el.classList.add('active');
  const f = cat==='all' ? products : products.filter(p=>p.cat===cat);
  renderProducts(f);
}

// ========== TIMER ==========
function startTimer(id, seconds){
  if(timers[id]) clearInterval(timers[id]);
  let rem = seconds;
  function update(){
    const el = document.getElementById('timer-'+id);
    if(!el){ clearInterval(timers[id]); return; }
    if(rem<=0){ el.innerHTML='⚡ ¡Oferta vigente!'; return; }
    const h=Math.floor(rem/3600),m=Math.floor((rem%3600)/60),s=rem%60;
    const label=h>0?`${h}h ${m}m ${s}s`:m>0?`${m}m ${s}s`:`${s}s`;
    el.innerHTML=`⏰ Acaba en: <b>${label}</b>`;
    rem--;
  }
  update();
  timers[id]=setInterval(update,1000);
}

// ========== SHAKE ==========
function startShakeLoop(){
  setInterval(()=>{
    const btns=document.querySelectorAll('.btn-pedir');
    if(!btns.length) return;
    const btn=btns[Math.floor(Math.random()*btns.length)];
    btn.classList.remove('shaking');
    void btn.offsetWidth;
    btn.classList.add('shaking');
    setTimeout(()=>btn.classList.remove('shaking'),700);
  },2800);
}

// ========== MODAL ==========
const catEmoji={hogar:'🏡',tecnologia:'📱',salud:'💊',belleza:'💄',fitness:'🏋️',accesorios:'👜',juguetes:'🧸',cocina:'🍳',ropa:'👕',bebes:'🍼',herramientas:'🔧',viajes:'🧳',infantil:'🎈'};
const featureIcons=['🎯','⚡','✅','🚀','💪','🔒','📦','⭐','🛠️','🌟'];
const genericSteps=[
  {t:'Elige tu producto',d:'Selecciona el que más te guste y revisa fotos, precio y detalles.'},
  {t:'Confirma por WhatsApp',d:'Llena tus datos y un asesor confirma tu pedido contigo.'},
  {t:'Recíbelo y paga',d:'Te llega a la puerta y pagas en efectivo al mensajero.'}
];
const genericFAQ=[
  {q:'¿De verdad pago solo cuando lo recibo?',a:'Sí. No pagas nada por adelantado. Pagas en efectivo al mensajero cuando el producto llega a tu dirección.'},
  {q:'¿Cuánto tarda el envío?',a:'Entre 3 y 7 días hábiles dependiendo de tu ciudad, a través de Interrapidísimo, Envía o Coordinadora.'},
  {q:'¿El producto tiene garantía?',a:'Sí, todos nuestros productos son nuevos y cuentan con garantía directa con nosotros por cualquier inconveniente de fábrica.'},
  {q:'¿Cómo confirmo mi pedido?',a:'Al dar clic en "Pedir ahora" llenas un formulario corto y un asesor te escribe por WhatsApp para confirmar tu dirección antes de despachar.'}
];
function openModal(id){
  const p = products.find(x=>x.id===id);
  if(!p) return;
  const disc = Math.round((1-p.price/p.oldPrice)*100);
  const imgs = p.imgs && p.imgs.length ? p.imgs : ['https://via.placeholder.com/500x500?text=TROGUI'];
  const thumbsHtml = imgs.map((src,i)=>`<img src="${src}" alt="${p.name}" class="${i===0?'active-img':''}" onerror="this.style.display='none'" onclick="setMainImage('${src.replace(/'/g,"\\'")}',this)">`).join('');
  const emoji = catEmoji[p.cat] || '🛍️';
  const sentences = (p.desc||'').split(/(?<=[.!])\s+/).map(s=>s.trim()).filter(Boolean);
  const featuresHtml = sentences.slice(0,6).map((s,i)=>`<div class="pp-feature-card"><span class="pf-icon">${featureIcons[i%featureIcons.length]}</span><p>${s}</p></div>`).join('') ||
    `<div class="pp-feature-card"><span class="pf-icon">✅</span><p>Producto nuevo, de calidad y garantizado, listo para usar desde el primer día.</p></div>`;
  const stepsHtml = genericSteps.map((s,i)=>`<div class="pp-step"><div class="ps-num">${i+1}</div><b>${s.t}</b><p>${s.d}</p></div>`).join('');
  const shipImg = (document.getElementById('shipping-carrier-photo')||{}).src || '';
  const faqHtml = genericFAQ.map(f=>`<details><summary>${f.q}</summary><p>${f.a}</p></details>`).join('');
  const revHtml = reviews.map(r=>`
    <div class="review-item">
      <div class="review-top">
        <div class="review-avatar">${r.name[0]}</div>
        <div><div class="review-name">${r.name} — ${r.city}</div><div class="review-stars">${'⭐'.repeat(r.stars)}</div></div>
      </div>
      <div class="review-text">${r.text}</div>
    </div>`).join('');
  document.getElementById('modal-content').innerHTML=`
    <div class="pp-topmarquee">🚚 Envío gratis a toda Colombia &nbsp;·&nbsp; 💵 Pagas cuando lo recibes en tu casa</div>
    <div class="pp-header">
      <img src="${document.querySelector('.logo-img').src}" alt="TROGÜI">
      <a href="https://wa.link/lhneng" target="_blank" class="wa-btn"><svg class="wa-icon" viewBox="0 0 32 32" fill="#fff" xmlns="http://www.w3.org/2000/svg"><path d="M16.001 3C9.373 3 4 8.373 4 15c0 2.386.7 4.607 1.902 6.472L4 29l7.72-1.868A11.94 11.94 0 0016.001 27C22.629 27 28 21.627 28 15S22.629 3 16.001 3zm6.965 17.06c-.29.816-1.434 1.5-2.353 1.695-.628.133-1.448.24-4.208-.903-3.532-1.462-5.805-5.045-5.983-5.278-.17-.233-1.435-1.91-1.435-3.643s.897-2.586 1.216-2.94c.318-.354.696-.442.928-.442.232 0 .464.002.667.012.213.01.5-.08.782.598.29.698.985 2.41 1.07 2.585.086.175.144.38.03.612-.116.233-.174.378-.343.58-.17.204-.357.455-.51.61-.17.174-.348.363-.15.71.198.348.88 1.454 1.89 2.354 1.3 1.158 2.396 1.517 2.744 1.687.348.17.552.145.756-.087.203-.233.87-1.014 1.103-1.362.232-.348.464-.29.782-.174.318.116 2.02.953 2.367 1.126.348.174.58.26.667.406.087.145.087.842-.203 1.658z"/></svg> WhatsApp</a>
    </div>
    <div class="pp-hero">
      <div>
        <div class="pp-gallery-main"><img id="pp-main-img" src="${imgs[0]}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/500x500?text=TROGUI'"></div>
        <div class="pp-gallery-thumbs">${thumbsHtml}</div>
      </div>
      <div>
        <div class="pp-badge">${emoji} NUEVO · GARANTIZADO</div>
        <div class="pp-title">${p.name}</div>
        <div class="stars">${'⭐'.repeat(p.stars)}<span style="color:var(--gray);font-size:13px"> ${p.stars}.0 (${p.sold}+ vendidos)</span></div>
        <div class="pp-price-row">
          <span class="pp-price-old">$${fmt(p.oldPrice)}</span>
          <span class="pp-price-new">$${fmt(p.price)}</span>
          <span style="background:#ffe0cc;color:var(--orange);font-weight:900;padding:5px 12px;border-radius:20px;font-size:12.5px">-${disc}% OFF</span>
        </div>
        ${p.lastUnits?'<div style="background:#fff0f0;border:1px solid var(--red);border-radius:11px;padding:10px 12px;font-size:13px;font-weight:800;color:var(--red);margin-bottom:14px">⚠️ ¡ÚLTIMAS UNIDADES! Stock muy limitado</div>':''}
        <button class="pp-cta" onclick="openOrderForm('${p.id}')">🛒 Pedir ahora — Pago contra entrega</button>
        <div class="pp-note">No pagas nada ahora. Confirmamos tu pedido por WhatsApp y pagas al recibirlo.</div>
        <div class="pp-trust-row">
          <div class="pp-trust-chip">🚚 Envío gratis</div>
          <div class="pp-trust-chip">💵 Contraentrega</div>
          <div class="pp-trust-chip">🛡️ Garantía</div>
        </div>
        <button onclick="shareProduct('${p.id}')" style="margin-top:14px;background:#f2f2f2;border:none;color:var(--dark);font-weight:800;font-size:12px;padding:8px 14px;border-radius:20px;cursor:pointer;display:inline-flex;align-items:center;gap:5px">🔗 Compartir producto</button>
      </div>
    </div>

    <div class="pp-section" style="padding-top:10px">
      <div class="pp-eyebrow">Descripción</div>
      <h2>Todo lo que necesitas saber</h2>
      <p class="pp-lead">${p.desc}</p>
    </div>

    <div class="pp-section" style="background:#fafafa;border-top:1px solid var(--border);border-bottom:1px solid var(--border);max-width:100%">
      <div style="max-width:880px;margin:0 auto">
        <div class="pp-eyebrow">Lo que ganas</div>
        <h2>Beneficios de este producto</h2>
        <div class="pp-features-grid">${featuresHtml}</div>
      </div>
    </div>

    <div class="pp-section">
      <div class="pp-eyebrow">Así de fácil</div>
      <h2>¿Cómo funciona la compra?</h2>
      <div class="pp-steps">${stepsHtml}</div>
    </div>

    <div class="pp-section" style="background:#fafafa;border-top:1px solid var(--border);border-bottom:1px solid var(--border);max-width:100%">
      <div style="max-width:880px;margin:0 auto">
        <div class="pp-eyebrow">Ficha técnica</div>
        <h2>Detalles del producto</h2>
        <div class="pp-specs">
          <div class="pp-spec-row"><b>ID</b><span>${p.id}</span></div>
          <div class="pp-spec-row"><b>Categoría</b><span>${emoji} ${p.cat}</span></div>
          <div class="pp-spec-row"><b>Vendidos</b><span>${p.sold}+</span></div>
          <div class="pp-spec-row"><b>Calificación</b><span>${p.stars}.0 / 5</span></div>
          <div class="pp-spec-row"><b>Envío</b><span>Gratis · 3 a 7 días</span></div>
          <div class="pp-spec-row"><b>Garantía</b><span>Sí, incluida</span></div>
        </div>
      </div>
    </div>

    <div class="pp-section">
      <div class="pp-eyebrow">¿Por qué comprar en TROGÜI?</div>
      <h2>Compra fácil. Compra segura.</h2>
      <div class="pp-shipping-mini">
        ${shipImg?`<img src="${shipImg}" alt="Transportadoras">`:''}
        <div class="psm-text">
          <b>✅ Envío seguro, confiable y autorizado</b>
          <span>Trabajamos con Interrapidísimo, Envía y Coordinadora para que tu pedido llegue seguro a toda Colombia.</span>
        </div>
      </div>
    </div>

    <div class="pp-section" style="background:#fafafa;border-top:1px solid var(--border);border-bottom:1px solid var(--border);max-width:100%">
      <div style="max-width:880px;margin:0 auto">
        <div class="pp-eyebrow">Reseñas</div>
        <h2>⭐ Lo que dicen nuestros clientes</h2>
        <div class="review-list">${revHtml}</div>
      </div>
    </div>

    <div class="pp-section">
      <div class="pp-eyebrow">Preguntas frecuentes</div>
      <h2>Todo lo que quieres saber antes de pedir</h2>
      <div class="pp-faq">${faqHtml}</div>
    </div>

    <div class="pp-footer-mini">📞 WhatsApp: 320 657 2598 · Envíos a toda Colombia · © 2026 TROGÜI</div>

    <div class="pp-sticky-bar">
      <span class="psb-price">$${fmt(p.price)}</span>
      <button onclick="openOrderForm('${p.id}')">🔥 Pedir ahora</button>
    </div>`;
  document.getElementById('product-modal').classList.add('active');
  document.body.style.overflow='hidden';
  window.scrollTo(0,0);
  document.title = p.name + ' — TROGÜI';
  if(location.hash !== '#producto-'+p.id){
    history.pushState({productId:p.id}, '', '#producto-'+p.id);
  }
}
function setMainImage(src, thumbEl){
  document.getElementById('pp-main-img').src = src;
  document.querySelectorAll('.pp-gallery-thumbs img').forEach(i=>i.classList.remove('active-img'));
  if(thumbEl) thumbEl.classList.add('active-img');
}
function closeModal(){
  document.getElementById('product-modal').classList.remove('active');
  document.body.style.overflow='';
  document.title = 'TROGÜI - Tienda Colombia 🇨🇴';
  if(location.hash.startsWith('#producto-')){
    history.pushState({}, '', location.pathname + location.search);
  }
}
function shareProduct(id){
  const url = location.origin + location.pathname + '#producto-' + id;
  if(navigator.share){
    navigator.share({title:'TROGÜI', url}).catch(()=>{});
  } else if(navigator.clipboard){
    navigator.clipboard.writeText(url).then(()=>showFloatMsg('🔗 Enlace copiado al portapapeles'));
  } else {
    prompt('Copia este enlace:', url);
  }
}
function openProductFromHash(){
  const h = location.hash;
  if(h && h.startsWith('#producto-')){
    const id = h.replace('#producto-','');
    if(products.find(x=>x.id===id)) openModal(id);
  }
}
window.addEventListener('popstate', () => {
  if(location.hash.startsWith('#producto-')) openProductFromHash();
  else closeModal();
});

// ========== ORDER FORM ==========
function openOrderForm(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  currentOrderProduct=p;
  closeModal();
  _showOrderForm(p);
}
function openOrderDirect(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  currentOrderProduct=p;
  _showOrderForm(p);
}
function _showOrderForm(p){
  document.getElementById('form-prod-name').textContent=p.name+' (ID: '+p.id+')';
  document.getElementById('form-price-show').innerHTML=`
    <div><div style="font-size:13px;color:var(--gray);font-weight:700">Precio anterior:</div><div class="fold">$${fmt(p.oldPrice)}</div></div>
    <div style="text-align:right"><div style="font-size:13px;color:var(--gray);font-weight:700">Pagas al recibir:</div><div class="fprice">$${fmt(p.price)}</div></div>`;
  document.getElementById('order-overlay').classList.add('active');
}
function closeOrderForm(){ document.getElementById('order-overlay').classList.remove('active'); }

function confirmOrder(){
  const nombre=document.getElementById('f-nombre').value.trim();
  const apellido=document.getElementById('f-apellido').value.trim();
  const depto=document.getElementById('f-departamento').value.trim();
  const ciudad=document.getElementById('f-ciudad').value.trim();
  const direccion=document.getElementById('f-direccion').value.trim();
  const telefono=document.getElementById('f-telefono').value.trim();
  const nota=document.getElementById('f-nota').value.trim();
  if(!nombre||!apellido||!depto||!ciudad||!direccion||!telefono){
    alert('⚠️ Por favor completa todos los campos obligatorios.');return;
  }
  const p=currentOrderProduct;
  const disc=Math.round((1-p.price/p.oldPrice)*100);
  const order={id:'ORD'+Date.now(),product:p.name,productId:p.id,price:p.price,oldPrice:p.oldPrice,discount:disc,nombre,apellido,departamento:depto,ciudad,direccion,telefono,nota,fecha:new Date().toLocaleString('es-CO'),fechaISO:new Date().toISOString()};
  orders.push(order);
  localStorage.setItem('trogui_orders',JSON.stringify(orders));
  const msg=encodeURIComponent(
    `🛍️ *NUEVO PEDIDO - TROGÜI*\n\n📦 *Producto:* ${p.name}\n🆔 *ID:* ${p.id}\n💰 *Precio:* $${fmt(p.price)} (-${disc}%)\n\n👤 *Cliente:* ${nombre} ${apellido}\n🗺️ *Departamento:* ${depto}\n🏙️ *Ciudad:* ${ciudad}\n🏠 *Dirección:* ${direccion}\n📞 *Teléfono:* ${telefono}\n📝 *Nota:* ${nota||'Sin nota'}\n\n✅ Pago contra entrega`
  );
  closeOrderForm();
  window.open(`https://wa.me/573206572598?text=${msg}`,'_blank');
}

// ========== CART ==========
function addToCart(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  const ex=cart.find(x=>x.id===id);
  if(ex) ex.qty++;
  else cart.push({...p,qty:1});
  updateCartUI();
  showFloatMsg('✅ '+p.name.substring(0,28)+'... al carrito');
}
function removeFromCart(id){ cart=cart.filter(x=>x.id!==id); updateCartUI(); }
function changeQty(id,delta){
  const item=cart.find(x=>x.id===id);
  if(!item) return;
  item.qty=Math.max(1,item.qty+delta);
  updateCartUI();
}
function updateCartUI(){
  const count=cart.reduce((a,b)=>a+b.qty,0);
  document.getElementById('cart-count').textContent=count;
  const list=document.getElementById('cart-items-list');
  if(!cart.length){
    list.innerHTML='<div class="empty-cart">🛒<br>Tu carrito está vacío<br><small style="font-size:13px;color:#aaa">Agrega productos para comenzar</small></div>';
    document.getElementById('cart-total').textContent='';
    document.getElementById('btn-checkout').style.display='none';
    return;
  }
  list.innerHTML=cart.map(item=>`
    <div class="cart-item">
      <img src="${item.imgs&&item.imgs[0]||''}" alt="${item.name}" onerror="this.src='https://via.placeholder.com/72?text=T'">
      <div class="cart-item-info">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-price">$${fmt(item.price)}</div>
        <div class="cart-qty">
          <button class="qty-btn" onclick="changeQty('${item.id}',-1)">−</button>
          <span class="qty-val">${item.qty}</span>
          <button class="qty-btn" onclick="changeQty('${item.id}',1)">+</button>
        </div>
      </div>
      <button class="cart-remove" onclick="removeFromCart('${item.id}')">✕</button>
    </div>`).join('');
  const total=cart.reduce((a,b)=>a+b.price*b.qty,0);
  document.getElementById('cart-total').innerHTML=`Total: <span>$${fmt(total)}</span>`;
  document.getElementById('btn-checkout').style.display='block';
}
function toggleCart(){ document.getElementById('cart-drawer').classList.toggle('open'); }
function checkoutCart(){
  if(!cart.length) return;
  const lines=cart.map(i=>`• ${i.name} x${i.qty} = $${fmt(i.price*i.qty)}`).join('\n');
  const total=cart.reduce((a,b)=>a+b.price*b.qty,0);
  const msg=encodeURIComponent(`🛍️ *PEDIDO CARRITO - TROGÜI*\n\n${lines}\n\n💰 *Total: $${fmt(total)}*\n\nDeseo pagar contra entrega 🙏`);
  window.open(`https://wa.me/573206572598?text=${msg}`,'_blank');
}

// ========== SEARCH ==========
function levenshtein(a,b){
  const m=a.length,n=b.length;
  if(m===0) return n;
  if(n===0) return m;
  const dp=[];
  for(let i=0;i<=m;i++){dp[i]=[i];for(let j=1;j<=n;j++) dp[i][j]=0;}
  for(let j=0;j<=n;j++) dp[0][j]=j;
  for(let i=1;i<=m;i++) for(let j=1;j<=n;j++){
    if(a[i-1]===b[j-1]) dp[i][j]=dp[i-1][j-1];
    else dp[i][j]=1+Math.min(dp[i-1][j],dp[i][j-1],dp[i-1][j-1]);
  }
  return dp[m][n];
}
function searchProducts(q){
  const dd=document.getElementById('search-dropdown');
  if(!q||q.length<2){ dd.classList.remove('open'); renderProducts(products); return; }
  const ql=q.toLowerCase().replace(/[áàä]/g,'a').replace(/[éèë]/g,'e').replace(/[íìï]/g,'i').replace(/[óòö]/g,'o').replace(/[úùü]/g,'u');
  const scored=products.map(p=>{
    const nl=p.name.toLowerCase().replace(/[áàä]/g,'a').replace(/[éèë]/g,'e').replace(/[íìï]/g,'i').replace(/[óòö]/g,'o').replace(/[úùü]/g,'u');
    const dl=p.desc.toLowerCase().replace(/[áàä]/g,'a').replace(/[éèë]/g,'e').replace(/[íìï]/g,'i').replace(/[óòö]/g,'o').replace(/[úùü]/g,'u');
    const exact=nl.includes(ql)||dl.includes(ql)?0:1;
    const words=nl.split(' ');
    const lev=Math.min(...words.map(w=>levenshtein(ql,w)));
    return{p,score:exact*8+lev};
  }).filter(x=>x.score<7).sort((a,b)=>a.score-b.score).slice(0,8);
  if(!scored.length){
    dd.innerHTML='<div style="padding:14px 16px;color:var(--gray);font-size:14px">😕 No encontramos ese producto</div>';
    dd.classList.add('open');
    renderProducts([]);
    return;
  }
  dd.innerHTML=scored.map(({p})=>`
    <div class="search-dd-item" onclick="openModal('${p.id}');document.getElementById('search-dropdown').classList.remove('open')">
      <img src="${p.imgs&&p.imgs[0]||''}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/40?text=T'">
      <div><div class="sdi-name">${p.name}</div><div class="sdi-price">$${fmt(p.price)}</div></div>
    </div>`).join('');
  dd.classList.add('open');
  renderProducts(scored.map(x=>x.p));
}
function doSearch(){ searchProducts(document.getElementById('search-input').value); }
document.addEventListener('click',e=>{ if(!e.target.closest('.search-bar')) document.getElementById('search-dropdown').classList.remove('open'); });

// ========== DELIVERY ==========
function calcDelivery(){
  const sel=document.getElementById('delivery-city');
  const days=parseInt(sel.value)||0;
  if(!days){ alert('Selecciona una ciudad'); return; }
  const date=new Date();
  date.setDate(date.getDate()+days);
  const dateStr=date.toLocaleDateString('es-CO',{weekday:'long',year:'numeric',month:'long',day:'numeric'});
  const el=document.getElementById('delivery-result');
  el.style.display='block';
  el.innerHTML=`📦 Tu pedido llegaría aproximadamente el <strong>${dateStr}</strong> (entre ${days} y ${days+2} días hábiles).`;
}

// ========== NOTIFICATIONS ==========
const notifPeople=[
  {name:'Ana María Roa',city:'Bogotá'},{name:'Camilo Vargas',city:'Medellín'},
  {name:'Sofía López',city:'Cali'},{name:'Jorge Herrera',city:'Barranquilla'},
  {name:'Daniela Ruiz',city:'Bucaramanga'},{name:'Mauricio Torres',city:'Pereira'},
  {name:'Valentina Soto',city:'Cartagena'},{name:'Felipe Molina',city:'Manizales'},
  {name:'Gloria Jiménez',city:'Ibagué'},{name:'Ernesto Díaz',city:'Santa Marta'},
];
let notifIdx=0;
function startNotifications(){
  setInterval(()=>{
    const {name,city}=notifPeople[notifIdx%notifPeople.length];
    const p=products[Math.floor(Math.random()*products.length)];
    showNotif(`🛍️ <span class="nn">${name}</span> de ${city} acaba de pedir <b>${p.name.substring(0,30)}</b>`);
    notifIdx++;
  },9000);
}
function showNotif(html){
  const nb=document.getElementById('notif-box');
  nb.innerHTML=html; nb.style.display='block';
  setTimeout(()=>nb.style.display='none',5000);
}
function showFloatMsg(msg){
  const existing=document.querySelector('.float-msg');
  if(existing) existing.remove();
  const div=document.createElement('div');
  div.className='float-msg'; div.textContent=msg;
  document.body.appendChild(div);
  setTimeout(()=>div.remove(),2800);
}
function updateVisitors(){
  setInterval(()=>{
    visitors=Math.max(8,visitors+Math.floor(Math.random()*7)-3);
    document.querySelectorAll('#v1,#v2').forEach(el=>el.textContent=visitors);
  },5000);
  document.querySelectorAll('#v1,#v2').forEach(el=>el.textContent=visitors);
}

// ========== ROULETTE ==========
const rouletteSegments=[
  {label:'🚚 Envío GRATIS',color:'#FF5200',prize:'¡Envío GRATIS en tu pedido!',win:true},
  {label:'5% Descuento',color:'#00b050',prize:'¡5% de descuento adicional en tu pedido!',win:true},
  {label:'💵 Contra Entrega',color:'#1a1a2e',prize:'¡Tienes Pago Contra Entrega disponible!',win:true},
  {label:'🎁 Regalo Sorpresa',color:'#e94560',prize:'¡Recibirás un pequeño regalo con tu pedido!',win:true},
  {label:'😅 Mejor Suerte',color:'#888',prize:'¡No ganaste esta vez! Pero tenemos envío gratis de todos modos 😊',win:false},
  {label:'10% Extra OFF',color:'#FF5200',prize:'¡10% de descuento adicional! Cuéntale al vendedor.',win:true},
  {label:'😅 Casi!',color:'#aaa',prize:'¡Casi! Pero igual tienes precios increíbles 🎉',win:false},
  {label:'🌟 Cliente VIP',color:'#f5c518',prize:'¡Eres Cliente VIP! Prioridad en atención.',win:true},
];
let rouletteAngle=0;
let rouletteSpinning=false;

function drawRoulette(angle=0){
  const canvas=document.getElementById('roulette-canvas');
  if(!canvas) return;
  const ctx=canvas.getContext('2d');
  const cx=140,cy=140,radius=135;
  const n=rouletteSegments.length;
  const arc=2*Math.PI/n;
  ctx.clearRect(0,0,280,280);
  rouletteSegments.forEach((seg,i)=>{
    const start=angle+i*arc-Math.PI/2;
    const end=start+arc;
    ctx.beginPath();
    ctx.moveTo(cx,cy);
    ctx.arc(cx,cy,radius,start,end);
    ctx.closePath();
    ctx.fillStyle=seg.color;
    ctx.fill();
    ctx.strokeStyle='rgba(255,255,255,.3)';
    ctx.lineWidth=2;
    ctx.stroke();
    ctx.save();
    ctx.translate(cx,cy);
    ctx.rotate(start+arc/2);
    ctx.textAlign='right';
    ctx.fillStyle='#fff';
    ctx.font='bold 11px Nunito,sans-serif';
    ctx.fillText(seg.label,radius-8,4);
    ctx.restore();
  });
  // Center circle
  ctx.beginPath();
  ctx.arc(cx,cy,22,0,2*Math.PI);
  ctx.fillStyle='#fff';
  ctx.fill();
  ctx.fillStyle='#FF5200';
  ctx.font='bold 13px Nunito,sans-serif';
  ctx.textAlign='center';
  ctx.fillText('TROGÜI',cx,cy+4);
}

function spinRoulette(){
  if(rouletteSpinning) return;
  rouletteSpinning=true;
  document.getElementById('roulette-btn').disabled=true;
  document.getElementById('roulette-result').style.display='none';
  // Bias: win 80% of time
  const winSegs=rouletteSegments.map((s,i)=>({...s,i})).filter(s=>s.win);
  const loseSegs=rouletteSegments.map((s,i)=>({...s,i})).filter(s=>!s.win);
  const chosen=Math.random()<0.8 ? winSegs[Math.floor(Math.random()*winSegs.length)] : loseSegs[Math.floor(Math.random()*loseSegs.length)];
  const n=rouletteSegments.length;
  const arc=2*Math.PI/n;
  const targetIdx=chosen.i;
  const totalSpins=5+Math.random()*3;
  const totalAngle=totalSpins*2*Math.PI - targetIdx*arc - arc/2 + Math.random()*arc*0.6;
  const duration=5000;
  let start=null;
  const baseAngle=rouletteAngle;
  function animate(ts){
    if(!start) start=ts;
    const elapsed=ts-start;
    const progress=Math.min(elapsed/duration,1);
    const ease=1-Math.pow(1-progress,4);
    rouletteAngle=baseAngle+totalAngle*ease;
    drawRoulette(rouletteAngle);
    if(progress<1){ requestAnimationFrame(animate); }
    else {
      rouletteSpinning=false;
      const res=document.getElementById('roulette-result');
      res.style.display='block';
      res.innerHTML=chosen.win
        ? `🎉 <b>¡Felicidades!</b><br>${chosen.prize}<br><small style="color:var(--gray)">Muestra esta pantalla al hacer tu pedido.</small>`
        : `😅 <b>¡Suerte la próxima!</b><br>${chosen.prize}`;
      res.style.color=chosen.win?'var(--orange)':'var(--gray)';
    }
  }
  requestAnimationFrame(animate);
}

function openRoulette(){ document.getElementById('roulette-overlay').classList.add('active'); }
function closeRoulette(){ document.getElementById('roulette-overlay').classList.remove('active'); }

// Inactivity watcher (1 min)
function startInactivityWatcher(){
  let lastActivity=Date.now();
  const events=['mousemove','keydown','scroll','click','touchstart'];
  events.forEach(e=>document.addEventListener(e,()=>{ lastActivity=Date.now(); }));
  setInterval(()=>{
    if(Date.now()-lastActivity > 60000 && !rouletteSpun){
      rouletteSpun=true;
      openRoulette();
    }
  },5000);
}

// ========== ADMIN AUTH ==========
function adminAuth(panel){
  const pass=prompt('🔐 Contraseña de administrador:');
  if(pass!==ADMIN_PASS){ alert('❌ Contraseña incorrecta'); return; }
  if(panel==='r') openAdminR();
  else if(panel==='c') openAdminC();
  else openAdminE();
}
function closeAdmin(id){ document.getElementById(id).classList.remove('active'); }

// ========== ADMIN R: PRODUCTS ==========
function openAdminR(){ renderAdminProducts(); document.getElementById('admin-r').classList.add('active'); }

function renderAdminProducts(){
  const list=document.getElementById('admin-product-list');
  list.innerHTML='';
  products.forEach(p=>{
    const div=document.createElement('div');
    div.className='admin-product-item';
    div.id='aitem-'+p.id;
    const imgsJson=JSON.stringify(p.imgs||[]).replace(/"/g,'&quot;');
    div.innerHTML=`
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:8px">
        <b style="color:var(--orange);font-size:13px">${p.id} — ${p.name}</b>
        <button class="btn-del-admin" onclick="deleteProduct('${p.id}')">🗑️ Eliminar</button>
      </div>
      <label>Nombre</label><input type="text" id="an-${p.id}" value="${p.name.replace(/"/g,'&quot;')}">
      <label>Descripción</label><textarea id="ad-${p.id}" rows="3">${p.desc}</textarea>
      <div class="admin-row2">
        <div><label>Precio ($)</label><input type="number" id="ap-${p.id}" value="${p.price}"></div>
        <div><label>Precio Anterior ($)</label><input type="number" id="ao-${p.id}" value="${p.oldPrice}"></div>
      </div>
      <div class="admin-row2">
        <div><label>Vendidos</label><input type="number" id="av-${p.id}" value="${p.sold}"></div>
        <div><label>Estrellas (1-5)</label><input type="number" id="as-${p.id}" value="${p.stars}" min="1" max="5"></div>
      </div>
      <label>Categoría</label>
      <select id="ac-${p.id}">
        ${['hogar','tecnologia','salud','belleza','fitness','accesorios','juguetes','cocina'].map(c=>`<option value="${c}"${p.cat===c?' selected':''}>${c}</option>`).join('')}
      </select>
      <label>URLs de Imágenes/GIFs (una por línea)</label>
      <textarea id="ai-${p.id}" rows="4" placeholder="https://imagen1.jpg&#10;https://imagen2.jpg&#10;https://gif.gif">${(p.imgs||[]).join('\n')}</textarea>
      <div style="display:flex;gap:8px;flex-wrap:wrap;margin-top:8px" id="preview-${p.id}">
        ${(p.imgs||[]).map(src=>`<img src="${src}" class="img-preview" onerror="this.style.display='none'">`).join('')}
      </div>
      <div class="admin-row2" style="margin-top:8px">
        <div><label>Últimas unidades</label><select id="alu-${p.id}"><option value="false"${!p.lastUnits?' selected':''}>No</option><option value="true"${p.lastUnits?' selected':''}>Sí</option></select></div>
        <div><label>Timer (segundos)</label><input type="number" id="at-${p.id}" value="${p.timer}"></div>
      </div>
      <button class="btn-save-admin" style="width:100%;margin-top:12px;font-size:14px" onclick="saveOneProduct('${p.id}')">💾 Guardar este producto</button>`;
    list.appendChild(div);
    // live preview update
    const ta=div.querySelector(`#ai-${p.id}`);
    const prev=div.querySelector(`#preview-${p.id}`);
    ta.addEventListener('input',()=>{
      const urls=ta.value.split('\n').map(u=>u.trim()).filter(Boolean);
      prev.innerHTML=urls.map(src=>`<img src="${src}" class="img-preview" onerror="this.style.display='none'">`).join('');
    });
  });
}

function saveOneProduct(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  p.name=document.getElementById('an-'+id).value||p.name;
  p.desc=document.getElementById('ad-'+id).value;
  p.price=parseInt(document.getElementById('ap-'+id).value)||p.price;
  p.oldPrice=parseInt(document.getElementById('ao-'+id).value)||p.oldPrice;
  p.sold=parseInt(document.getElementById('av-'+id).value)||p.sold;
  p.stars=parseInt(document.getElementById('as-'+id).value)||p.stars;
  p.cat=document.getElementById('ac-'+id).value;
  const imgsRaw=document.getElementById('ai-'+id).value.split('\n').map(u=>u.trim()).filter(Boolean);
  if(imgsRaw.length) p.imgs=imgsRaw;
  p.lastUnits=document.getElementById('alu-'+id).value==='true';
  p.timer=parseInt(document.getElementById('at-'+id).value)||p.timer;
  localStorage.setItem('trogui_v2_products',JSON.stringify(products));
  renderProducts(products);
  showFloatMsg('✅ "'+p.name.substring(0,24)+'" guardado!');
}

function saveAllProducts(){
  products.forEach(p=>saveOneProduct(p.id));
  showFloatMsg('✅ Todos los productos guardados!');
}

function addNewProduct(){
  const newId='T'+String(Date.now()).slice(-4);
  products.push({id:newId,name:'Nuevo Producto',cat:'hogar',imgs:['https://via.placeholder.com/400x300?text=TROGUI'],price:49000,oldPrice:89000,desc:'Descripción del producto.',sold:10,stars:5,lastUnits:false,timer:3600});
  localStorage.setItem('trogui_v2_products',JSON.stringify(products));
  renderAdminProducts();
  renderProducts(products);
  setTimeout(()=>document.getElementById('admin-product-list').lastElementChild?.scrollIntoView({behavior:'smooth'}),150);
}

function deleteProduct(id){
  if(!confirm('¿Eliminar este producto?')) return;
  products=products.filter(p=>p.id!==id);
  localStorage.setItem('trogui_v2_products',JSON.stringify(products));
  renderAdminProducts();
  renderProducts(products);
}

// ========== ADMIN C: ORDERS ==========
let filteredOrders=[];
function openAdminC(){
  filteredOrders=[...orders].reverse();
  renderOrderStats();
  renderOrdersList(filteredOrders);
  document.getElementById('order-search').value='';
  document.getElementById('admin-c').classList.add('active');
}
function renderOrderStats(){
  const total=orders.length;
  const totalRev=orders.reduce((s,o)=>s+(o.price||0),0);
  const today=new Date().toLocaleDateString('es-CO');
  const todayCount=orders.filter(o=>o.fecha&&o.fecha.startsWith(today)).length;
  const ciudades=[...new Set(orders.map(o=>o.ciudad).filter(Boolean))].length;
  document.getElementById('orders-stats').innerHTML=`
    <div class="stat-card"><div class="sv">${total}</div><div class="sl">Total Pedidos</div></div>
    <div class="stat-card"><div class="sv">$${fmt(totalRev)}</div><div class="sl">Ingresos</div></div>
    <div class="stat-card"><div class="sv">${todayCount}</div><div class="sl">Pedidos Hoy</div></div>
    <div class="stat-card"><div class="sv">${ciudades}</div><div class="sl">Ciudades</div></div>`;
}
function renderOrdersList(list){
  const cont=document.getElementById('admin-orders-list');
  if(!list.length){ cont.innerHTML='<div class="no-orders">📭 No hay pedidos aún</div>'; return; }
  cont.innerHTML=list.map(o=>{
    const waMsg=encodeURIComponent(`Hola ${o.nombre}, tu pedido de *${o.product}* por $${fmt(o.price)} está confirmado. ¡Gracias por comprar en TROGÜI! 🛍️`);
    return `<div class="order-card">
      <div class="order-product-name">${o.product}</div>
      <div style="font-size:11px;color:var(--gray);margin-bottom:8px">#${o.id} · ${o.fecha}</div>
      <div class="order-grid">
        <div class="order-field"><span class="of-label">👤 Nombre</span><span class="of-value">${o.nombre} ${o.apellido||''}</span></div>
        <div class="order-field"><span class="of-label">📞 Teléfono</span><span class="of-value">${o.telefono}</span></div>
        <div class="order-field"><span class="of-label">🗺️ Departamento</span><span class="of-value">${o.departamento||'—'}</span></div>
        <div class="order-field"><span class="of-label">🏙️ Ciudad</span><span class="of-value">${o.ciudad}</span></div>
        <div class="order-field" style="grid-column:1/-1"><span class="of-label">🏠 Dirección</span><span class="of-value">${o.direccion}</span></div>
      </div>
      <div class="order-price-row">
        <div><div class="order-price-new">$${fmt(o.price)}</div><div class="order-price-old">Antes $${fmt(o.oldPrice)}</div></div>
        <button class="order-wa-btn" onclick="window.open('https://wa.me/57${(o.telefono||'').replace(/\D/g,'')}?text=${waMsg}','_blank')">💬 Contactar</button>
      </div>
      ${o.nota?`<div class="order-nota">📝 ${o.nota}</div>`:''}
    </div>`;
  }).join('');
}
function filterOrders(q){
  if(!q){ filteredOrders=[...orders].reverse(); renderOrdersList(filteredOrders); return; }
  const ql=q.toLowerCase();
  filteredOrders=[...orders].reverse().filter(o=>
    (o.nombre||'').toLowerCase().includes(ql)||(o.apellido||'').toLowerCase().includes(ql)||
    (o.ciudad||'').toLowerCase().includes(ql)||(o.product||'').toLowerCase().includes(ql)||
    (o.telefono||'').includes(q)||(o.id||'').toLowerCase().includes(ql)
  );
  renderOrdersList(filteredOrders);
}
function exportCSV(){
  if(!orders.length){ alert('No hay pedidos para exportar.'); return; }
  const h=['ID','Producto','Precio','Descuento%','Nombre','Apellido','Departamento','Ciudad','Dirección','Teléfono','Nota','Fecha'];
  const rows=orders.map(o=>[o.id,o.product,o.price,o.discount||'',o.nombre,o.apellido||'',o.departamento||'',o.ciudad,o.direccion,o.telefono,o.nota||'',o.fecha].map(v=>`"${String(v||'').replace(/"/g,'""')}"`).join(','));
  const csv='\uFEFF'+[h.join(','),...rows].join('\n');
  const blob=new Blob([csv],{type:'text/csv;charset=utf-8;'});
  const url=URL.createObjectURL(blob);
  const a=document.createElement('a');
  a.href=url; a.download='pedidos_trogui_'+new Date().toISOString().slice(0,10)+'.csv'; a.click();
  URL.revokeObjectURL(url);
  showFloatMsg('✅ CSV exportado!');
}
function clearOrders(){
  if(!confirm('¿Eliminar TODOS los pedidos? Esto no se puede deshacer.')) return;
  orders=[];
  localStorage.removeItem('trogui_orders');
  openAdminC();
}

// ========== ADMIN E: PAGE EDITOR ==========
function openAdminE(){
  document.getElementById('edit-topbar').value=document.getElementById('topbar-text').textContent;
  document.getElementById('edit-prod-title').value=document.getElementById('products-title').textContent;
  document.getElementById('audio-url').value=localStorage.getItem('trogui_audio')||'';
  renderAdminReviews();
  document.getElementById('admin-e').classList.add('active');
}
function saveSetting(key){
  if(key==='topbar'){
    const v=document.getElementById('edit-topbar').value;
    document.getElementById('topbar-text').textContent=v;
    localStorage.setItem('trogui_topbar',v);
  } else if(key==='prod-title'){
    const v=document.getElementById('edit-prod-title').value;
    document.getElementById('products-title').innerHTML=v;
    localStorage.setItem('trogui_prod_title',v);
  }
  showFloatMsg('✅ Guardado!');
}
function setAudio(){
  const url=document.getElementById('audio-url').value.trim();
  if(!url){ alert('Ingresa una URL de audio'); return; }
  document.getElementById('bg-audio-src').src=url;
  document.getElementById('bg-audio').load();
  document.getElementById('bg-audio').play().catch(()=>{});
  localStorage.setItem('trogui_audio',url);
  showFloatMsg('✅ Audio establecido');
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
  localStorage.setItem('trogui_reviews',JSON.stringify(reviews));
  showFloatMsg('✅ Reseñas guardadas!');
}
</script>
<script>
document.addEventListener("DOMContentLoaded", function () {

    // MEZCLA LOS PRODUCTOS CADA VEZ QUE ALGUIEN ABRE LA PÁGINA
    const grid = document.querySelector(".products-grid");

    if (grid) {
        const productos = Array.from(grid.children);

        for (let i = productos.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [productos[i], productos[j]] = [productos[j], productos[i]];
        }

        productos.forEach(producto => {
            grid.appendChild(producto);
        });
    }

});
</script>
</body>
</html>
