<!--DOCTYPE html-->
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Bottom Line — 보이지 않는 곳까지, 당신의 건강을 끌어올리다</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;0,9..144,600;0,9..144,700;0,9..144,800;0,9..144,900;1,9..144,300;1,9..144,400;1,9..144,500;1,9..144,600;1,9..144,700&family=Instrument+Serif:ital@0;1&family=Bricolage+Grotesque:opsz,wght@12..96,300;12..96,400;12..96,500;12..96,600;12..96,700;12..96,800&family=Noto+Serif+KR:wght@300;400;500;600;700;900&family=Noto+Sans+KR:wght@200;300;400;500;600;700;900&family=Gowun+Batang:wght@400;700&display=swap" rel="stylesheet">
<style>
:root{
  /* Natural light palette — cream → sage → gold */
  --cream:#F8F4ED;
  --cream-warm:#F2EAD9;
  --cream-deep:#E8DCC4;
  --paper:#FBF8F2;
  --sage:#9DBE96;
  --sage-mid:#7BA075;
  --sage-light:#C5DBC0;
  --sage-deep:#5A7F54;
  --sage-darkest:#2D4329;
  --terra:#D4906F;
  --terra-soft:#EDC0A6;
  --terra-deep:#B36D4D;
  --clay:#A86A4E;
  --ink:#1A1A18;
  --ink-soft:#3D3A35;
  --stone:#7A746C;
  --stone-light:#A89F94;
  --mist:#E4DCD0;
  --gold:#D6B775;
  --gold-deep:#B89248;
  --pink-soft:#E5B5B0;
  --pink-deep:#C77B73;
  --plum:#8B5A6A;
  --honey:#E8C988;
  --moss:#6B8064;

  --display:'Fraunces',serif;
  --display-italic:'Instrument Serif',serif;
  --grotesque:'Bricolage Grotesque',sans-serif;
  --serif-kr:'Noto Serif KR',serif;
  --sans-kr:'Noto Sans KR',sans-serif;
  --batang:'Gowun Batang',serif;
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{
  background:var(--cream);
  color:var(--ink);
  font-family:var(--sans-kr);
  font-weight:300;
  line-height:1.65;
  overflow-x:hidden;
  -webkit-font-smoothing:antialiased;
  text-rendering:optimizeLegibility;
}
::selection{background:var(--sage-deep);color:var(--cream);}

/* ═══════════════ FILM GRAIN OVERLAY ═══════════════ */
body::before{
  content:'';
  position:fixed;inset:0;
  background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' stitchTiles='stitch'/%3E%3CfeColorMatrix values='0 0 0 0 0.95 0 0 0 0 0.92 0 0 0 0 0.85 0 0 0 0.45 0'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)' opacity='0.6'/%3E%3C/svg%3E");
  opacity:.18;
  mix-blend-mode:multiply;
  pointer-events:none;
  z-index:200;
}

/* ═══════════════ NAV ═══════════════ */
.nav{
  position:fixed;top:0;left:0;right:0;z-index:100;
  padding:24px 56px;
  display:flex;justify-content:space-between;align-items:center;
  background:rgba(248,244,237,.55);
  backdrop-filter:blur(24px) saturate(1.4);
  -webkit-backdrop-filter:blur(24px) saturate(1.4);
  border-bottom:1px solid transparent;
  transition:all .5s cubic-bezier(.2,.8,.2,1);
}
.nav.scrolled{
  background:rgba(248,244,237,.95);
  border-bottom-color:rgba(31,29,26,.06);
  padding:16px 56px;
}
.nav-logo{
  font-family:var(--display);
  font-size:23px;font-weight:500;
  letter-spacing:-.5px;color:var(--ink);
  display:flex;align-items:center;gap:11px;
  text-decoration:none;
  font-variation-settings:"opsz" 144;
}
.nav-logo em{
  font-family:var(--display-italic);
  font-style:italic;
  color:var(--sage-deep);
  font-weight:400;
}
.nav-logo-mark{
  width:30px;height:30px;border-radius:50%;
  background:linear-gradient(135deg,var(--sage),var(--sage-deep));
  display:flex;align-items:center;justify-content:center;
  color:white;font-size:14px;
  box-shadow:0 4px 12px rgba(90,127,84,.25);
}
.nav-menu{display:flex;gap:40px;align-items:center;}
.nav-link{
  font-family:var(--grotesque);
  font-size:13px;letter-spacing:.5px;font-weight:500;
  color:var(--ink-soft);text-decoration:none;
  transition:color .25s ease;
  position:relative;
}
.nav-link::after{
  content:'';
  position:absolute;
  left:0;right:0;bottom:-6px;
  height:1px;
  background:var(--sage-deep);
  transform:scaleX(0);
  transform-origin:left;
  transition:transform .35s cubic-bezier(.2,.8,.2,1);
}
.nav-link:hover{color:var(--sage-deep);}
.nav-link:hover::after{transform:scaleX(1);}
.nav-cta{
  background:var(--ink);color:var(--cream);
  padding:11px 24px;border-radius:28px;
  font-family:var(--grotesque);
  font-size:12px;font-weight:600;letter-spacing:.5px;
  text-decoration:none;
  transition:all .35s cubic-bezier(.2,.8,.2,1);
  display:inline-flex;align-items:center;gap:8px;
}
.nav-cta:hover{
  background:var(--sage-deep);
  transform:translateY(-1px);
  box-shadow:0 12px 28px rgba(90,127,84,.3);
}
.nav-cta-arrow{
  transition:transform .3s ease;
  display:inline-block;
}
.nav-cta:hover .nav-cta-arrow{transform:translateX(3px);}

/* ═══════════════ HERO — natural light cinematic ═══════════════ */
.hero{
  min-height:100vh;
  position:relative;
  display:flex;align-items:center;
  padding:140px 56px 80px;
  overflow:hidden;
  background:
    radial-gradient(ellipse 80% 60% at 75% 20%,rgba(232,201,136,.45),transparent 70%),
    radial-gradient(ellipse 70% 50% at 20% 80%,rgba(157,190,150,.35),transparent 70%),
    linear-gradient(160deg,#FAF6EC 0%,#F2EAD9 50%,#E8DCC4 100%);
}

/* sun-light shaft */
.hero::before{
  content:'';
  position:absolute;
  top:-20%;right:10%;
  width:60vw;height:140vh;
  background:linear-gradient(195deg,
    rgba(255,247,225,.6) 0%,
    rgba(232,201,136,.25) 30%,
    transparent 70%);
  filter:blur(40px);
  pointer-events:none;
  transform:rotate(15deg);
  animation:lightShift 20s ease-in-out infinite;
}
@keyframes lightShift{
  0%,100%{opacity:.7;transform:rotate(15deg) translateY(0);}
  50%{opacity:1;transform:rotate(13deg) translateY(-20px);}
}

.hero-orb{
  position:absolute;border-radius:50%;
  filter:blur(80px);
  pointer-events:none;
  opacity:.55;
  animation:floatOrb 18s ease-in-out infinite;
  mix-blend-mode:multiply;
}
.hero-orb-1{
  width:560px;height:560px;
  top:-120px;right:-100px;
  background:radial-gradient(circle,rgba(157,190,150,.5),transparent 65%);
}
.hero-orb-2{
  width:420px;height:420px;
  bottom:-80px;left:5%;
  background:radial-gradient(circle,rgba(214,144,111,.4),transparent 65%);
  animation-delay:-6s;animation-duration:22s;
}
.hero-orb-3{
  width:300px;height:300px;
  top:35%;left:38%;
  background:radial-gradient(circle,rgba(232,201,136,.5),transparent 65%);
  animation-delay:-10s;animation-duration:16s;
}
@keyframes floatOrb{
  0%,100%{transform:translate(0,0) scale(1);}
  33%{transform:translate(30px,-30px) scale(1.08);}
  66%{transform:translate(-20px,20px) scale(.95);}
}

.hero-grid{
  max-width:1380px;margin:0 auto;width:100%;
  display:grid;grid-template-columns:1.05fr .95fr;gap:80px;
  align-items:center;
  position:relative;z-index:2;
}

.hero-eyebrow{
  display:inline-flex;align-items:center;gap:12px;
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:3.5px;font-weight:600;
  color:var(--sage-deep);text-transform:uppercase;
  margin-bottom:36px;
  padding:8px 18px 8px 14px;
  background:rgba(255,255,255,.6);
  border:1px solid rgba(157,190,150,.35);
  border-radius:24px;
  backdrop-filter:blur(10px);
  animation:fadeUp 1s cubic-bezier(.2,.8,.2,1) both;
  box-shadow:0 4px 16px rgba(90,127,84,.08);
}
.hero-eyebrow-dot{
  width:7px;height:7px;border-radius:50%;
  background:var(--sage-deep);
  animation:pulse 2.5s ease-in-out infinite;
  box-shadow:0 0 8px rgba(90,127,84,.5);
}
@keyframes pulse{0%,100%{opacity:.4;}50%{opacity:1;box-shadow:0 0 16px rgba(90,127,84,.7);}}

/* HERO TITLE — refined editorial */
.hero-title{
  font-family:var(--display);
  font-size:clamp(56px,7.6vw,114px);
  font-weight:300;
  line-height:.92;letter-spacing:-3.5px;
  color:var(--ink);
  margin-bottom:36px;
  animation:fadeUp 1.1s cubic-bezier(.2,.8,.2,1) .15s both;
  font-variation-settings:"opsz" 144;
}
.hero-title-row1{font-weight:300;}
.hero-title-row2{
  display:block;
  font-style:italic;
  font-weight:400;
  color:var(--sage-deep);
  font-variation-settings:"opsz" 144;
}
.hero-title-mark{
  font-family:var(--display);
  font-style:italic;
  color:var(--terra-deep);
  font-weight:500;
  position:relative;
  display:inline-block;
  font-variation-settings:"opsz" 144;
}
.hero-title-mark::after{
  content:'';
  position:absolute;
  bottom:14px;left:-4px;right:-4px;
  height:18px;
  background:linear-gradient(90deg,
    rgba(157,190,150,.5),
    rgba(232,201,136,.5));
  z-index:-1;
  border-radius:4px;
  animation:highlightDraw 1.5s cubic-bezier(.2,.8,.2,1) 1s both;
  transform-origin:left;
}
@keyframes highlightDraw{
  from{transform:scaleX(0);}
  to{transform:scaleX(1);}
}

.hero-subtitle{
  font-family:var(--serif-kr);
  font-size:18px;line-height:1.85;font-weight:300;
  color:var(--ink-soft);
  max-width:520px;
  margin-bottom:48px;
  animation:fadeUp 1.1s cubic-bezier(.2,.8,.2,1) .25s both;
}
.hero-subtitle strong{
  color:var(--ink);
  font-weight:600;
  background:linear-gradient(180deg,transparent 65%,rgba(157,190,150,.3) 65%);
  padding:0 2px;
}

.hero-actions{
  display:flex;gap:18px;align-items:center;
  animation:fadeUp 1.1s cubic-bezier(.2,.8,.2,1) .35s both;
  flex-wrap:wrap;
}
.btn-primary{
  background:var(--ink);color:var(--cream);
  padding:18px 36px;border-radius:36px;
  font-family:var(--grotesque);
  font-size:13px;font-weight:600;letter-spacing:.5px;
  text-decoration:none;
  display:inline-flex;align-items:center;gap:12px;
  transition:all .4s cubic-bezier(.2,.8,.2,1);
  position:relative;overflow:hidden;
}
.btn-primary::before{
  content:'';
  position:absolute;inset:0;
  background:linear-gradient(135deg,var(--sage-deep),var(--sage-darkest));
  opacity:0;
  transition:opacity .4s ease;
}
.btn-primary:hover::before{opacity:1;}
.btn-primary > *{position:relative;z-index:1;}
.btn-primary:hover{
  transform:translateY(-2px);
  box-shadow:0 16px 36px rgba(90,127,84,.3);
}
.btn-arrow{
  width:20px;height:20px;border-radius:50%;
  background:var(--cream);color:var(--ink);
  display:flex;align-items:center;justify-content:center;
  font-size:11px;
  transition:transform .35s cubic-bezier(.2,.8,.2,1);
}
.btn-primary:hover .btn-arrow{transform:translateX(4px);}

.btn-text{
  font-family:var(--grotesque);
  font-size:13px;letter-spacing:.5px;font-weight:500;
  color:var(--ink-soft);text-decoration:none;
  border-bottom:1px solid var(--ink-soft);
  padding-bottom:3px;
  transition:all .25s ease;
}
.btn-text:hover{color:var(--sage-deep);border-color:var(--sage-deep);}

/* HERO TAGS — refined */
.hero-tags{
  display:flex;gap:8px;margin-top:54px;flex-wrap:wrap;
  animation:fadeUp 1.1s cubic-bezier(.2,.8,.2,1) .45s both;
}
.hero-tag{
  font-family:var(--grotesque);
  font-size:12px;font-weight:500;letter-spacing:.3px;
  background:rgba(255,255,255,.7);
  border:1px solid rgba(31,29,26,.08);
  color:var(--ink-soft);
  padding:7px 15px;
  border-radius:16px;
  backdrop-filter:blur(8px);
  transition:all .3s ease;
  cursor:default;
}
.hero-tag:hover{
  background:white;
  border-color:rgba(157,190,150,.4);
  transform:translateY(-2px);
  box-shadow:0 6px 16px rgba(31,29,26,.06);
}
.hero-tag span{color:var(--sage-deep);font-weight:600;}

/* ═══════════════ HERO PHONE ═══════════════ */
.hero-visual{
  position:relative;
  display:flex;justify-content:center;
  animation:fadeUp 1.3s cubic-bezier(.2,.8,.2,1) .5s both;
}
.phone-shell{
  width:316px;height:632px;
  background:#1a1814;
  border-radius:48px;
  padding:9px;
  box-shadow:
    0 80px 140px rgba(31,29,26,.22),
    0 40px 80px rgba(31,29,26,.14),
    inset 0 0 0 2px rgba(255,255,255,.05);
  position:relative;
  transform:rotate(-2.5deg);
  transition:transform 1s cubic-bezier(.2,.8,.2,1);
}
.phone-shell:hover{transform:rotate(0deg) scale(1.025);}
.phone-screen{
  width:100%;height:100%;
  background:var(--paper);
  border-radius:40px;
  overflow:hidden;
  position:relative;
}
.phone-notch{
  position:absolute;top:8px;left:50%;
  transform:translateX(-50%);
  width:96px;height:26px;
  background:#1a1814;border-radius:14px;z-index:5;
}
.phone-content{
  height:100%;width:100%;
  padding:48px 16px 16px;
  overflow:hidden;
  display:flex;flex-direction:column;
}

/* Tree tabs — exactly match new app images */
.tree-tabs{
  display:flex;justify-content:space-around;align-items:center;
  padding:8px 4px 14px;
}
.tree-tab{
  display:flex;flex-direction:column;align-items:center;gap:4px;
  padding:6px 12px;border-radius:16px;
  transition:background .3s ease;
}
.tree-tab.active{background:rgba(157,190,150,.28);}
.tree-tab-icon{font-size:20px;}
.tree-tab-name{
  font-family:var(--sans-kr);
  font-size:9.5px;font-weight:600;color:var(--ink);
}
.tree-tab.active .tree-tab-name{color:var(--sage-deep);font-weight:700;}

.routine-title{
  font-family:var(--sans-kr);
  font-size:11.5px;font-weight:700;
  color:var(--ink);margin-bottom:10px;
  letter-spacing:-.2px;padding-left:5px;
}
.routine-card{
  background:rgba(157,190,150,.18);
  border-radius:14px;padding:11px 12px;
  display:flex;align-items:center;gap:11px;
  margin-bottom:7px;
  transition:transform .3s ease;
}
.routine-card:hover{transform:translateX(2px);}
.routine-icon{
  width:34px;height:34px;border-radius:10px;
  background:white;
  display:flex;align-items:center;justify-content:center;
  font-size:17px;flex-shrink:0;
  box-shadow:0 2px 6px rgba(31,29,26,.06);
}
.routine-info{flex:1;min-width:0;}
.routine-time{
  font-family:var(--grotesque);
  font-size:8px;letter-spacing:.5px;
  color:var(--sage-deep);font-weight:700;
  text-transform:uppercase;
}
.routine-name{
  font-family:var(--sans-kr);
  font-size:11.5px;font-weight:700;
  color:var(--ink);line-height:1.25;margin-top:2px;
}
.routine-desc{
  font-family:var(--sans-kr);
  font-size:9px;color:var(--stone);margin-top:2px;
}
.routine-check{
  width:20px;height:20px;border-radius:50%;
  background:var(--sage-deep);color:white;
  display:flex;align-items:center;justify-content:center;
  font-size:10px;flex-shrink:0;
  box-shadow:0 2px 6px rgba(90,127,84,.3);
}

/* Forest growth status mini */
.phone-forest-status{
  background:linear-gradient(135deg,rgba(157,190,150,.12),rgba(214,183,117,.08));
  border-radius:14px;padding:11px 12px;
  margin-top:9px;
  border:1px solid rgba(157,190,150,.2);
}
.phone-forest-h{
  font-family:var(--sans-kr);
  font-size:9.5px;font-weight:700;
  color:var(--sage-deep);
  margin-bottom:8px;display:flex;align-items:center;gap:5px;
}
.phone-forest-row{
  display:flex;align-items:center;gap:7px;
  margin-bottom:4px;
}
.phone-forest-row:last-child{margin-bottom:0;}
.phone-forest-icon{font-size:14px;width:18px;text-align:center;}
.phone-forest-label{
  flex:1;font-family:var(--sans-kr);
  font-size:8.5px;color:var(--ink);font-weight:500;
}
.phone-forest-bar{
  width:42px;height:3px;border-radius:2px;
  background:var(--mist);overflow:hidden;
}
.phone-forest-bar-fill{height:100%;border-radius:2px;}

/* Floating tags — Updated content */
.phone-floating-tag{
  position:absolute;
  background:white;
  border-radius:16px;
  padding:13px 16px;
  box-shadow:
    0 16px 40px rgba(31,29,26,.14),
    0 4px 12px rgba(31,29,26,.06);
  display:flex;align-items:center;gap:10px;
  white-space:nowrap;
  border:1px solid rgba(31,29,26,.05);
  z-index:10;
  backdrop-filter:blur(20px);
}
.phone-floating-tag-icon{
  width:28px;height:28px;border-radius:9px;
  display:flex;align-items:center;justify-content:center;
  font-size:14px;flex-shrink:0;
}
.phone-floating-tag-info{display:flex;flex-direction:column;gap:1px;}
.phone-floating-tag-info strong{
  font-family:var(--grotesque);
  font-size:11.5px;color:var(--ink);font-weight:700;
}
.phone-floating-tag-info span{
  font-family:var(--grotesque);
  font-size:9.5px;color:var(--stone);
}

.tag-1{top:60px;left:-70px;animation:floatTag 5s ease-in-out infinite;}
.tag-2{top:280px;right:-58px;animation:floatTag 6s ease-in-out infinite -2s;}
.tag-3{bottom:90px;left:-50px;animation:floatTag 5.5s ease-in-out infinite -3s;}
@keyframes floatTag{
  0%,100%{transform:translateY(0);}
  50%{transform:translateY(-10px);}
}
@keyframes fadeUp{from{opacity:0;transform:translateY(28px);}to{opacity:1;transform:translateY(0);}}

/* ═══════════════ TICKER ═══════════════ */
.ticker-section{
  background:linear-gradient(90deg,#1A1A18 0%,#2A2A26 50%,#1A1A18 100%);
  padding:28px 0;
  overflow:hidden;
  border-top:1px solid rgba(255,255,255,.06);
  border-bottom:1px solid rgba(255,255,255,.06);
  position:relative;
}
.ticker-section::before,.ticker-section::after{
  content:'';
  position:absolute;top:0;bottom:0;width:120px;z-index:2;
  pointer-events:none;
}
.ticker-section::before{
  left:0;
  background:linear-gradient(90deg,#1A1A18,transparent);
}
.ticker-section::after{
  right:0;
  background:linear-gradient(-90deg,#1A1A18,transparent);
}
.ticker{display:flex;animation:ticker 45s linear infinite;width:max-content;}
.ticker-item{
  font-family:var(--display);
  font-size:42px;font-style:italic;font-weight:300;
  color:rgba(255,255,255,.4);
  padding:0 38px;
  display:flex;align-items:center;
  font-variation-settings:"opsz" 144;
  white-space:nowrap;
}
.ticker-item em{
  color:rgba(157,190,150,.85);
  font-style:italic;
  font-weight:400;
}
.ticker-dot{
  width:6px;height:6px;border-radius:50%;
  background:var(--sage);margin:0 38px;
  flex-shrink:0;
}
@keyframes ticker{to{transform:translateX(-50%);}}

/* ═══════════════ SECTION COMMON ═══════════════ */
.section{padding:160px 56px;position:relative;}
.section-inner{max-width:1280px;margin:0 auto;}
.section-eyebrow{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:3.5px;font-weight:600;
  color:var(--sage-deep);text-transform:uppercase;
  margin-bottom:20px;display:flex;align-items:center;gap:14px;
}
.section-eyebrow::before{
  content:'';width:32px;height:1px;background:var(--sage-deep);
}

.section-title{
  font-family:var(--display);
  font-size:clamp(44px,5.6vw,80px);
  font-weight:300;line-height:1.02;
  letter-spacing:-2.5px;color:var(--ink);
  margin-bottom:24px;
  font-variation-settings:"opsz" 144;
}
.section-title-italic{
  font-style:italic;font-weight:400;color:var(--sage-deep);
}
.section-desc{
  font-family:var(--serif-kr);
  font-size:17px;line-height:1.9;font-weight:300;
  color:var(--ink-soft);max-width:680px;
  margin-bottom:64px;
}
.reveal{
  opacity:0;
  transform:translateY(36px);
  transition:opacity 1.1s cubic-bezier(.2,.8,.2,1),
             transform 1.1s cubic-bezier(.2,.8,.2,1);
}
.reveal.in{opacity:1;transform:none;}

/* ═══════════════ MARKET / PROBLEM ═══════════════ */
.market-section{
  background:
    radial-gradient(ellipse 60% 40% at 80% 30%,rgba(232,201,136,.18),transparent 70%),
    linear-gradient(180deg,var(--cream) 0%,var(--cream-warm) 100%);
  position:relative;
}

.market-headline{
  font-family:var(--display);
  font-size:clamp(38px,4.8vw,68px);
  font-weight:400;font-style:italic;
  line-height:1.18;letter-spacing:-1.8px;
  color:var(--ink);
  max-width:1020px;
  margin-bottom:80px;
  font-variation-settings:"opsz" 144;
}
.market-headline em{color:var(--clay);font-style:italic;font-weight:500;}
.market-headline strong{
  color:var(--sage-deep);font-weight:500;font-style:italic;
  position:relative;
}

.stats-grid{
  display:grid;grid-template-columns:repeat(4,1fr);
  gap:0;
  background:white;
  border-radius:32px;
  overflow:hidden;
  box-shadow:0 30px 80px rgba(31,29,26,.08),
             0 8px 24px rgba(31,29,26,.04);
}
.stat-block{
  padding:52px 36px;
  border-right:1px solid var(--mist);
  position:relative;
  overflow:hidden;
  transition:background .4s ease;
}
.stat-block:hover{background:rgba(248,244,237,.5);}
.stat-block:last-child{border-right:none;}
.stat-block::before{
  content:'';
  position:absolute;
  top:0;left:0;right:0;
  height:3px;
  opacity:.7;
}
.stat-block:nth-child(1)::before{background:var(--clay);}
.stat-block:nth-child(2)::before{background:var(--terra);}
.stat-block:nth-child(3)::before{background:var(--gold-deep);}
.stat-block:nth-child(4)::before{background:var(--sage-deep);}

.stat-tag{
  font-family:var(--grotesque);
  font-size:10.5px;letter-spacing:2px;font-weight:600;
  text-transform:uppercase;
  margin-bottom:28px;
  color:var(--stone);
  display:flex;align-items:center;gap:8px;
}
.stat-tag-dot{
  width:6px;height:6px;border-radius:50%;
}
.stat-block:nth-child(1) .stat-tag-dot{background:var(--clay);}
.stat-block:nth-child(2) .stat-tag-dot{background:var(--terra);}
.stat-block:nth-child(3) .stat-tag-dot{background:var(--gold-deep);}
.stat-block:nth-child(4) .stat-tag-dot{background:var(--sage-deep);}

.stat-num{
  font-family:var(--display);
  font-size:68px;font-weight:400;
  line-height:.9;letter-spacing:-2.5px;
  color:var(--ink);
  margin-bottom:16px;
  font-variation-settings:"opsz" 144;
}
.stat-num small{
  font-size:.4em;
  color:var(--stone);
  font-weight:300;
  letter-spacing:0;
}
.stat-block:nth-child(1) .stat-num{color:var(--clay);}
.stat-block:nth-child(2) .stat-num{color:var(--terra);}
.stat-block:nth-child(3) .stat-num{color:var(--gold-deep);}
.stat-block:nth-child(4) .stat-num{color:var(--sage-deep);}

.stat-label{
  font-family:var(--serif-kr);
  font-size:14.5px;font-weight:600;color:var(--ink);
  margin-bottom:10px;letter-spacing:-.3px;
}
.stat-source{
  font-family:var(--grotesque);
  font-size:10.5px;color:var(--stone-light);
  font-weight:400;line-height:1.6;
}

.problem-trio{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:22px;
  margin-top:56px;
}
.problem-card{
  background:rgba(255,255,255,.7);
  backdrop-filter:blur(10px);
  border-radius:24px;
  padding:36px 32px;
  border:1px solid rgba(31,29,26,.05);
  position:relative;overflow:hidden;
  transition:all .5s cubic-bezier(.2,.8,.2,1);
}
.problem-card:hover{
  background:white;
  transform:translateY(-6px);
  box-shadow:0 24px 60px rgba(31,29,26,.08);
  border-color:rgba(157,190,150,.3);
}
.problem-card-num{
  font-family:var(--display);
  font-size:11.5px;font-weight:600;font-style:italic;
  color:var(--terra);letter-spacing:1.5px;
  margin-bottom:14px;
  font-variation-settings:"opsz" 14;
}
.problem-card-icon{
  font-size:32px;margin-bottom:18px;
  display:inline-block;
  filter:drop-shadow(0 4px 8px rgba(31,29,26,.08));
}
.problem-card-title{
  font-family:var(--serif-kr);
  font-size:20px;font-weight:600;
  color:var(--ink);
  line-height:1.4;margin-bottom:14px;letter-spacing:-.4px;
}
.problem-card-desc{
  font-family:var(--sans-kr);
  font-size:13.5px;color:var(--stone);
  line-height:1.75;font-weight:300;
}

/* ═══════════════ 4 GAPS — diagonal storytelling ═══════════════ */
.gaps-section{
  background:
    radial-gradient(ellipse 50% 40% at 30% 70%,rgba(157,190,150,.18),transparent 70%),
    linear-gradient(180deg,var(--cream-warm) 0%,#EDDFC4 100%);
}
.gaps-grid{
  display:grid;grid-template-columns:repeat(4,1fr);
  gap:20px;margin-top:56px;
}
.gap-card{
  background:rgba(255,255,255,.78);
  backdrop-filter:blur(12px);
  border:1px solid rgba(31,29,26,.05);
  border-radius:24px;
  padding:36px 28px;
  transition:all .5s cubic-bezier(.2,.8,.2,1);
  position:relative;overflow:hidden;
}
.gap-card:hover{
  background:white;
  border-color:rgba(157,190,150,.4);
  transform:translateY(-6px);
  box-shadow:0 24px 60px rgba(31,29,26,.1);
}
.gap-card::before{
  content:'';
  position:absolute;
  bottom:0;left:0;
  width:0;height:2px;
  background:var(--sage-deep);
  transition:width .5s cubic-bezier(.2,.8,.2,1);
}
.gap-card:hover::before{width:100%;}

.gap-num{
  font-family:var(--display-italic);
  font-size:60px;font-style:italic;
  color:var(--sage);letter-spacing:-2px;
  line-height:.85;margin-bottom:18px;
  opacity:.5;
  transition:opacity .4s ease;
}
.gap-card:hover .gap-num{opacity:.85;}
.gap-title{
  font-family:var(--serif-kr);
  font-size:17.5px;font-weight:600;
  color:var(--ink);
  line-height:1.4;margin-bottom:14px;letter-spacing:-.3px;
}
.gap-desc{
  font-size:13px;color:var(--stone);line-height:1.75;font-weight:300;
}

/* ═══════════════ JOURNEY ═══════════════ */
.journey-section{
  background:
    radial-gradient(ellipse 60% 50% at 80% 30%,rgba(157,190,150,.12),transparent 70%),
    radial-gradient(ellipse 50% 40% at 20% 70%,rgba(214,144,111,.1),transparent 70%),
    var(--ink);
  color:var(--cream);
  padding:160px 0;
  position:relative;
  /* overflow:hidden 제거 → 카드 잘림 방지 */
}
.journey-section .section-inner{position:relative;z-index:2;}
.journey-section .section-eyebrow{color:var(--sage-light);}
.journey-section .section-eyebrow::before{background:var(--sage-light);}
.journey-section .section-title{color:var(--cream);}
.journey-section .section-title-italic{color:var(--sage-light);}
.journey-section .section-desc{color:rgba(248,244,237,.55);}

.journey-track{position:relative;}
.journey-scenes{
  display:flex;gap:24px;
  overflow-x:auto;
  padding:24px 56px 36px;
  scroll-snap-type:x mandatory;
  scrollbar-width:none;
  /* 첫 카드가 잘리지 않도록 음수 마진 제거 */
}
.journey-scenes::-webkit-scrollbar{display:none;}
.scene-card{
  min-width:340px;width:340px;
  background:linear-gradient(165deg,rgba(255,255,255,.04),rgba(255,255,255,.01));
  border:1px solid rgba(255,255,255,.08);
  border-radius:24px;
  padding:36px 32px;
  scroll-snap-align:start;
  position:relative;
  transition:all .5s cubic-bezier(.2,.8,.2,1);
  flex-shrink:0;
}
.scene-card:hover{
  border-color:rgba(157,190,150,.4);
  transform:translateY(-6px);
  background:linear-gradient(165deg,rgba(157,190,150,.08),rgba(255,255,255,.02));
}
.scene-num-row{display:flex;align-items:center;gap:14px;margin-bottom:24px;}
.scene-num{
  font-family:var(--display);
  font-size:14px;font-weight:600;font-style:italic;
  color:var(--sage-light);letter-spacing:1.5px;
  font-variation-settings:"opsz" 14;
}
.scene-line{flex:1;height:1px;background:rgba(255,255,255,.1);}
.scene-emo{font-size:18px;}
.scene-illust{
  width:100%;height:200px;
  border-radius:18px;
  margin-bottom:24px;
  display:flex;align-items:center;justify-content:center;
  position:relative;overflow:hidden;
}
.scene-illust-1{background:linear-gradient(135deg,#3a2a20,#5a3e2c);}
.scene-illust-2{background:linear-gradient(135deg,#3a2e20,#5a4830);}
.scene-illust-3{background:linear-gradient(135deg,#2a3a26,#3e5a32);}
.scene-illust-4{background:linear-gradient(135deg,#2c4028,#3e6238);}
.scene-illust-5{background:linear-gradient(135deg,#3a4a30,#5a7240);}
.scene-illust-6{background:linear-gradient(135deg,#5a6a3a,#8aa055);}
.scene-illust-7{background:linear-gradient(135deg,#7a8a4a,#aac270);}
.scene-illust-8{background:linear-gradient(135deg,#9aae5a,#c8dc88);}

.scene-phase{
  font-family:var(--grotesque);
  font-size:10px;letter-spacing:2.5px;font-weight:600;
  color:var(--sage-light);text-transform:uppercase;
  margin-bottom:10px;
}
.scene-title{
  font-family:var(--serif-kr);
  font-size:21px;font-weight:600;
  color:var(--cream);line-height:1.3;
  margin-bottom:14px;letter-spacing:-.3px;
}
.scene-text{
  font-size:13.5px;color:rgba(248,244,237,.6);
  line-height:1.75;font-weight:300;margin-bottom:18px;
}
.scene-quote{
  border-left:2px solid var(--sage-light);
  padding-left:14px;
  font-family:var(--batang);
  font-style:italic;font-size:13px;font-weight:400;
  color:var(--sage-light);
  line-height:1.65;
}
.journey-controls{
  display:flex;justify-content:space-between;align-items:center;
  margin-top:36px;padding:0 8px;
}
.journey-progress-bar{
  flex:1;height:2px;background:rgba(255,255,255,.08);
  border-radius:2px;margin:0 32px;position:relative;overflow:hidden;
}
.journey-progress-fill{
  position:absolute;left:0;top:0;height:100%;
  background:var(--sage);width:12.5%;
  transition:width .5s ease;
  box-shadow:0 0 12px rgba(157,190,150,.5);
}
.journey-arrow{
  width:52px;height:52px;border-radius:50%;
  background:rgba(255,255,255,.06);
  border:1px solid rgba(255,255,255,.12);
  color:var(--cream);
  display:flex;align-items:center;justify-content:center;
  cursor:pointer;font-size:15px;
  transition:all .35s cubic-bezier(.2,.8,.2,1);
}
.journey-arrow:hover{
  background:var(--sage-deep);
  border-color:var(--sage-deep);
  transform:scale(1.05);
}
.journey-arrow:disabled{opacity:.3;cursor:not-allowed;}

/* ═══════════════ FLOW (INPUT → CORE → OUTPUT) ═══════════════ */
.flow-section{
  background:
    radial-gradient(ellipse 50% 40% at 80% 30%,rgba(232,201,136,.18),transparent 70%),
    linear-gradient(180deg,var(--cream-warm) 0%,var(--cream) 100%);
  position:relative;overflow:hidden;
}

.flow-track{
  display:grid;
  grid-template-columns:1fr 60px 1.2fr 60px 1fr;
  gap:0;align-items:stretch;
  margin-top:56px;
}
.flow-step{
  background:white;
  border-radius:28px;padding:40px 36px;
  border:1px solid rgba(31,29,26,.05);
  transition:all .5s cubic-bezier(.2,.8,.2,1);
  position:relative;overflow:hidden;
}
.flow-step:hover{
  transform:translateY(-8px);
  box-shadow:0 30px 70px rgba(31,29,26,.08);
}
.flow-step.center{
  background:
    radial-gradient(ellipse 80% 60% at 30% 30%,rgba(157,190,150,.18),transparent 70%),
    linear-gradient(165deg,#2D4329 0%,#1F3018 100%);
  color:var(--cream);
  border-color:var(--sage-deep);
  transform:scale(1.04);
  box-shadow:0 24px 60px rgba(45,67,41,.3);
}
.flow-step.center:hover{
  transform:scale(1.04) translateY(-8px);
  box-shadow:0 36px 80px rgba(45,67,41,.4);
}

.flow-num{
  font-family:var(--display-italic);
  font-size:54px;font-style:italic;
  letter-spacing:-1.5px;line-height:.85;
  margin-bottom:16px;
  opacity:.4;
}
.flow-step:nth-child(1) .flow-num{color:var(--terra);}
.flow-step.center .flow-num{color:var(--sage-light);opacity:.85;}
.flow-step:nth-child(5) .flow-num{color:var(--sage-deep);}

.flow-label{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:3.5px;font-weight:700;
  text-transform:uppercase;
  margin-bottom:16px;
  display:inline-block;
  padding:5px 12px;border-radius:12px;
}
.flow-step:nth-child(1) .flow-label{
  color:var(--terra-deep);
  background:rgba(214,144,111,.12);
}
.flow-step.center .flow-label{
  color:var(--sage-light);
  background:rgba(255,255,255,.08);
}
.flow-step:nth-child(5) .flow-label{
  color:var(--sage-deep);
  background:rgba(157,190,150,.15);
}

.flow-title{
  font-family:var(--serif-kr);
  font-size:23px;font-weight:700;
  letter-spacing:-.5px;
  margin-bottom:24px;
  line-height:1.3;
}
.flow-step .flow-title{color:var(--ink);}
.flow-step.center .flow-title{color:var(--cream);}

.flow-list{
  list-style:none;
  display:flex;flex-direction:column;gap:11px;
}
.flow-list li{
  font-size:13.5px;line-height:1.6;font-weight:300;
  padding-left:18px;position:relative;
}
.flow-step .flow-list li{color:var(--ink-soft);}
.flow-step.center .flow-list li{color:rgba(255,255,255,.78);}
.flow-list li::before{
  content:'';
  position:absolute;left:0;top:8px;
  width:6px;height:6px;border-radius:50%;
}
.flow-step:nth-child(1) .flow-list li::before{background:var(--terra);}
.flow-step.center .flow-list li::before{background:var(--sage-light);}
.flow-step:nth-child(5) .flow-list li::before{background:var(--sage-deep);}

.flow-arrow{
  font-family:var(--display);
  font-size:36px;font-weight:300;font-style:italic;
  color:var(--stone-light);
  display:flex;align-items:center;justify-content:center;
  padding:0 12px;
  font-variation-settings:"opsz" 144;
}

.flow-quote{
  margin-top:80px;padding:56px 64px;
  background:
    radial-gradient(ellipse 80% 60% at 30% 50%,rgba(157,190,150,.15),transparent 70%),
    linear-gradient(135deg,rgba(255,255,255,.6),rgba(248,244,237,.4));
  backdrop-filter:blur(10px);
  border:1px solid rgba(157,190,150,.2);
  border-radius:32px;
  text-align:center;
  position:relative;
  overflow:hidden;
}
.flow-quote::before{
  content:'❝';
  position:absolute;top:20px;left:36px;
  font-family:var(--display);
  font-size:80px;line-height:1;
  color:var(--sage);opacity:.25;
  font-style:italic;
}
.flow-quote p{
  font-family:var(--display);
  font-size:clamp(22px,2.8vw,36px);
  font-weight:300;line-height:1.4;
  letter-spacing:-.6px;
  color:var(--ink);
  font-variation-settings:"opsz" 144;
  position:relative;z-index:1;
}
.flow-quote em{
  font-style:italic;
  color:var(--sage-deep);
  font-weight:500;
}

/* ═══════════════ FOREST GROWTH ═══════════════ */
.forest-section{
  background:
    radial-gradient(ellipse 70% 50% at 80% 30%,rgba(232,201,136,.2),transparent 70%),
    radial-gradient(ellipse 60% 40% at 20% 70%,rgba(157,190,150,.18),transparent 70%),
    linear-gradient(180deg,var(--cream) 0%,#EDDFC4 100%);
  position:relative;
  overflow:hidden;
}

.forest-headline{
  font-family:var(--display);
  font-size:clamp(38px,4.6vw,64px);
  font-weight:300;
  line-height:1.05;letter-spacing:-1.8px;
  color:var(--ink);
  margin-bottom:28px;
  font-variation-settings:"opsz" 144;
}
.forest-headline em{
  font-style:italic;color:var(--sage-deep);font-weight:500;
}
.forest-headline .marker{
  background:linear-gradient(180deg,transparent 60%,rgba(214,144,111,.4) 60%);
  padding:0 6px;
}

/* 7-stage timeline */
.forest-stages{
  display:grid;
  grid-template-columns:repeat(7,1fr);
  gap:0;
  margin-top:72px;
  padding:56px 0 36px;
  position:relative;
}
.forest-stages::before{
  content:'';
  position:absolute;
  top:92px;left:6%;right:6%;
  height:2px;
  background:linear-gradient(90deg,
    rgba(157,190,150,.2) 0%,
    var(--sage) 30%,
    var(--gold) 60%,
    var(--sage-deep) 100%);
  z-index:0;
}
.stage{
  text-align:center;
  position:relative;z-index:1;
  cursor:pointer;
  transition:transform .4s cubic-bezier(.2,.8,.2,1);
}
.stage:hover{transform:translateY(-6px);}
.stage-icon-wrap{
  width:96px;height:96px;
  margin:0 auto 18px;
  border-radius:50%;
  background:white;
  border:2px solid var(--sage-light);
  display:flex;align-items:center;justify-content:center;
  font-size:38px;
  position:relative;
  box-shadow:0 10px 28px rgba(31,29,26,.06);
  transition:all .5s cubic-bezier(.2,.8,.2,1);
}
.stage:hover .stage-icon-wrap{
  transform:scale(1.12);
  box-shadow:0 20px 50px rgba(157,190,150,.35);
  border-color:var(--sage-deep);
}
.stage-icon-wrap::after{
  content:attr(data-count);
  position:absolute;
  bottom:-7px;right:-7px;
  background:var(--sage-deep);color:white;
  font-family:var(--grotesque);
  font-size:9.5px;font-weight:700;
  padding:4px 10px;border-radius:11px;
  letter-spacing:.5px;
  box-shadow:0 4px 12px rgba(90,127,84,.3);
}
.stage-name{
  font-family:var(--serif-kr);
  font-size:14.5px;font-weight:600;
  color:var(--ink);
  margin-bottom:4px;letter-spacing:-.3px;
}
.stage-en{
  font-family:var(--grotesque);
  font-size:9px;letter-spacing:1.5px;font-weight:500;
  color:var(--sage-deep);text-transform:uppercase;
}

/* 3 trees with their dedicated routines from new app images */
.trees-section-title{
  font-family:var(--display);
  font-size:clamp(30px,3.6vw,48px);
  font-weight:300;font-style:italic;
  line-height:1.18;letter-spacing:-1.2px;
  color:var(--ink);
  margin-top:104px;margin-bottom:18px;
  font-variation-settings:"opsz" 144;
}
.trees-section-title strong{
  color:var(--sage-deep);font-style:italic;font-weight:500;
}
.trees-section-desc{
  font-family:var(--serif-kr);
  font-size:15px;line-height:1.85;font-weight:300;
  color:var(--ink-soft);max-width:680px;
  margin-bottom:56px;
}

.trees-trio{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:24px;
}
.tree-card{
  background:white;
  border-radius:28px;
  padding:40px 36px;
  position:relative;overflow:hidden;
  border:1px solid rgba(31,29,26,.05);
  transition:all .5s cubic-bezier(.2,.8,.2,1);
}
.tree-card:hover{
  transform:translateY(-8px);
  box-shadow:0 30px 70px rgba(31,29,26,.1);
}
/* Tree gradient backdrops */
.tree-card.pine{
  background:
    radial-gradient(ellipse 80% 60% at 70% 0%,rgba(157,190,150,.25),transparent 70%),
    linear-gradient(165deg,#fff,#E9F0E5);
}
.tree-card.bamboo{
  background:
    radial-gradient(ellipse 80% 60% at 70% 0%,rgba(168,106,78,.18),transparent 70%),
    linear-gradient(165deg,#fff,#F5EBE5);
}
.tree-card.cherry{
  background:
    radial-gradient(ellipse 80% 60% at 70% 0%,rgba(199,123,115,.2),transparent 70%),
    linear-gradient(165deg,#fff,#FDEEF1);
}

.tree-icon-big{
  font-size:64px;
  margin-bottom:24px;
  display:inline-block;
  filter:drop-shadow(0 10px 20px rgba(31,29,26,.12));
  transition:transform .5s cubic-bezier(.2,.8,.2,1);
}
.tree-card:hover .tree-icon-big{
  transform:rotate(-6deg) scale(1.05);
}
.tree-card h3{
  font-family:var(--serif-kr);
  font-size:26px;font-weight:700;
  color:var(--ink);
  margin-bottom:8px;letter-spacing:-.5px;
}
.tree-purpose{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:2.5px;font-weight:600;
  text-transform:uppercase;
  margin-bottom:24px;
  display:inline-block;
  padding:6px 14px;border-radius:12px;
}
.tree-card.pine .tree-purpose{
  color:var(--sage-deep);background:rgba(157,190,150,.18);
}
.tree-card.bamboo .tree-purpose{
  color:var(--clay);background:rgba(168,106,78,.1);
}
.tree-card.cherry .tree-purpose{
  color:var(--pink-deep);background:rgba(199,123,115,.1);
}

/* Routines per tree — matches uploaded app images */
.tree-routines{
  display:flex;flex-direction:column;gap:10px;
  margin-bottom:28px;
}
.tree-routine{
  display:flex;align-items:center;gap:12px;
  padding:14px 16px;
  border-radius:14px;
}
.tree-card.pine .tree-routine{background:rgba(157,190,150,.12);}
.tree-card.bamboo .tree-routine{background:rgba(168,106,78,.07);}
.tree-card.cherry .tree-routine{background:rgba(199,123,115,.07);}

.tree-routine-icon{
  width:38px;height:38px;border-radius:10px;
  background:white;
  display:flex;align-items:center;justify-content:center;
  font-size:19px;flex-shrink:0;
  box-shadow:0 2px 6px rgba(31,29,26,.04);
}
.tree-routine-info{flex:1;}
.tree-routine-time{
  font-family:var(--grotesque);
  font-size:9.5px;letter-spacing:.5px;font-weight:700;
  text-transform:uppercase;
  margin-bottom:3px;
}
.tree-card.pine .tree-routine-time{color:var(--sage-deep);}
.tree-card.bamboo .tree-routine-time{color:var(--clay);}
.tree-card.cherry .tree-routine-time{color:var(--pink-deep);}
.tree-routine-name{
  font-family:var(--sans-kr);
  font-size:13.5px;font-weight:700;color:var(--ink);line-height:1.3;
}
.tree-routine-desc{
  font-family:var(--sans-kr);
  font-size:11px;color:var(--stone);margin-top:2px;
}

.tree-progress-row{
  display:flex;align-items:center;gap:12px;
  padding-top:18px;border-top:1px solid var(--mist);
}
.tree-progress-bar{
  flex:1;height:6px;background:var(--mist);
  border-radius:3px;overflow:hidden;
}
.tree-progress-fill{height:100%;border-radius:3px;}
.tree-card.pine .tree-progress-fill{background:var(--sage-deep);width:67%;}
.tree-card.bamboo .tree-progress-fill{background:var(--clay);width:30%;}
.tree-card.cherry .tree-progress-fill{background:var(--pink-deep);width:67%;}
.tree-progress-text{
  font-family:var(--grotesque);
  font-size:11.5px;font-weight:600;
  color:var(--ink);letter-spacing:.5px;
}

/* ═══════════════ EXPERT COLUMN ═══════════════ */
.column-section{
  background:
    radial-gradient(ellipse 60% 40% at 30% 80%,rgba(157,190,150,.15),transparent 70%),
    linear-gradient(180deg,#EDDFC4 0%,var(--cream) 100%);
  position:relative;overflow:hidden;
}
.column-grid{
  display:grid;
  grid-template-columns:1fr 1.15fr;
  gap:96px;
  align-items:start;
}
.column-left{position:sticky;top:140px;}

.column-headline{
  font-family:var(--display);
  font-size:clamp(38px,4.6vw,64px);
  font-weight:300;
  line-height:1.05;letter-spacing:-1.8px;
  color:var(--ink);
  margin-bottom:28px;
  font-variation-settings:"opsz" 144;
}
.column-headline em{
  font-style:italic;color:var(--sage-deep);font-weight:500;
}
.column-desc{
  font-family:var(--serif-kr);
  font-size:15.5px;line-height:1.9;font-weight:300;
  color:var(--ink-soft);
  margin-bottom:32px;
}

.column-credibility{
  background:linear-gradient(135deg,rgba(157,190,150,.12),rgba(214,144,111,.08));
  border-left:3px solid var(--sage-deep);
  border-radius:0 14px 14px 0;
  padding:20px 24px;
}
.column-credibility-label{
  font-family:var(--grotesque);
  font-size:10.5px;letter-spacing:2.5px;font-weight:600;
  color:var(--sage-deep);text-transform:uppercase;
  margin-bottom:8px;
}
.column-credibility-text{
  font-family:var(--serif-kr);
  font-size:13.5px;line-height:1.75;color:var(--ink);
  font-weight:500;
}

.column-list{
  display:flex;flex-direction:column;gap:18px;
}
.article-card{
  background:white;
  border-radius:22px;
  padding:28px 32px;
  display:flex;align-items:flex-start;gap:22px;
  border:1px solid rgba(31,29,26,.05);
  cursor:pointer;
  transition:all .5s cubic-bezier(.2,.8,.2,1);
  position:relative;
  overflow:hidden;
}
.article-card:hover{
  transform:translateX(6px);
  box-shadow:0 20px 50px rgba(31,29,26,.08);
  border-color:rgba(157,190,150,.4);
}
.article-card::before{
  content:'';
  position:absolute;
  top:0;left:0;
  width:0;height:100%;
  transition:width .5s cubic-bezier(.2,.8,.2,1);
}
.article-card.kidney::before{
  background:linear-gradient(180deg,var(--sage),var(--sage-deep));
}
.article-card.anal::before{
  background:linear-gradient(180deg,var(--pink-soft),var(--plum));
}
.article-card.diet::before{
  background:linear-gradient(180deg,var(--terra-soft),var(--clay));
}
.article-card:hover::before{width:3px;}

.article-icon-wrap{
  width:56px;height:56px;border-radius:14px;
  display:flex;align-items:center;justify-content:center;
  flex-shrink:0;font-size:26px;
  transition:transform .4s ease;
}
.article-card:hover .article-icon-wrap{
  transform:scale(1.08) rotate(-3deg);
}
.article-card.kidney .article-icon-wrap{
  background:linear-gradient(135deg,#E0EFDE,#C5DBC0);
}
.article-card.anal .article-icon-wrap{
  background:linear-gradient(135deg,#FBE0EE,#F2C8DD);
}
.article-card.diet .article-icon-wrap{
  background:linear-gradient(135deg,#FCE5E2,#F2C0BB);
}

.article-content{flex:1;min-width:0;}
.article-tag{
  font-family:var(--grotesque);
  font-size:10.5px;letter-spacing:1.5px;font-weight:600;
  text-transform:uppercase;
  padding:4px 11px;border-radius:11px;
  display:inline-block;
  margin-bottom:12px;
}
.article-card.kidney .article-tag{
  color:var(--sage-deep);background:rgba(157,190,150,.18);
}
.article-card.anal .article-tag{
  color:#B85786;background:rgba(184,87,134,.1);
}
.article-card.diet .article-tag{
  color:var(--clay);background:rgba(168,106,78,.1);
}

.article-title{
  font-family:var(--serif-kr);
  font-size:18px;font-weight:700;
  color:var(--ink);
  line-height:1.4;letter-spacing:-.3px;
  margin-bottom:10px;
}
.article-meta{
  font-family:var(--grotesque);
  font-size:12px;color:var(--stone);
  font-weight:400;
}
.article-meta span{color:var(--ink);font-weight:600;}
.article-arrow{
  align-self:center;
  width:36px;height:36px;border-radius:50%;
  background:rgba(31,29,26,.04);
  color:var(--ink-soft);
  display:flex;align-items:center;justify-content:center;
  font-size:14px;flex-shrink:0;
  transition:all .4s cubic-bezier(.2,.8,.2,1);
}
.article-card:hover .article-arrow{
  background:var(--sage-deep);color:white;
  transform:translateX(6px) rotate(-45deg);
}

/* ═══════════════ APP TABS — 5 ═══════════════ */
.tabs-section{
  background:
    radial-gradient(ellipse 70% 50% at 80% 30%,rgba(157,190,150,.12),transparent 70%),
    var(--ink);
  color:var(--cream);
  position:relative;overflow:hidden;
}
.tabs-section .section-inner{position:relative;z-index:2;}
.tabs-section .section-eyebrow{color:var(--sage-light);}
.tabs-section .section-eyebrow::before{background:var(--sage-light);}
.tabs-section .section-title{color:var(--cream);}
.tabs-section .section-title-italic{color:var(--sage-light);}
.tabs-section .section-desc{color:rgba(248,244,237,.55);}

.tabs-grid{
  display:grid;grid-template-columns:repeat(5,1fr);
  gap:18px;margin-top:40px;
}
.tab-card{
  background:linear-gradient(165deg,rgba(255,255,255,.04),rgba(255,255,255,.01));
  border:1px solid rgba(255,255,255,.08);
  border-radius:22px;
  padding:36px 28px;
  transition:all .5s cubic-bezier(.2,.8,.2,1);
  position:relative;
}
.tab-card:hover{
  border-color:rgba(157,190,150,.4);
  background:linear-gradient(165deg,rgba(157,190,150,.08),rgba(255,255,255,.02));
  transform:translateY(-6px);
}
.tab-num{
  font-family:var(--display);
  font-size:11.5px;font-weight:600;font-style:italic;
  color:var(--sage-light);letter-spacing:1.5px;
  margin-bottom:14px;
  font-variation-settings:"opsz" 14;
}
.tab-emoji{
  font-size:38px;margin-bottom:20px;display:block;
  filter:saturate(1.1) drop-shadow(0 4px 12px rgba(0,0,0,.3));
}
.tab-name{
  font-family:var(--serif-kr);
  font-size:19px;font-weight:700;
  color:var(--cream);
  margin-bottom:6px;letter-spacing:-.3px;
}
.tab-role{
  font-family:var(--grotesque);
  font-size:10px;letter-spacing:2px;font-weight:600;
  color:var(--sage-light);text-transform:uppercase;
  margin-bottom:20px;
}
.tab-features{
  list-style:none;display:flex;flex-direction:column;gap:9px;
}
.tab-features li{
  font-size:12.5px;color:rgba(248,244,237,.65);
  font-weight:300;line-height:1.65;
  padding-left:14px;position:relative;
}
.tab-features li::before{
  content:'·';
  position:absolute;left:0;top:0;
  color:var(--sage);font-weight:700;font-size:18px;line-height:.8;
}

/* ═══════════════ SOLUTIONS — 5 care ═══════════════ */
.solutions-section{
  background:
    radial-gradient(ellipse 60% 40% at 20% 30%,rgba(232,201,136,.18),transparent 70%),
    linear-gradient(180deg,var(--cream) 0%,var(--cream-warm) 100%);
}
.solutions-grid{
  display:grid;grid-template-columns:1.2fr 1fr;
  gap:80px;align-items:center;
}
.solutions-tagline{
  font-family:var(--display);
  font-size:clamp(40px,4.8vw,68px);
  font-weight:300;font-style:italic;
  line-height:1.1;letter-spacing:-1.8px;
  color:var(--ink);
  margin-bottom:52px;
  font-variation-settings:"opsz" 144;
}
.solutions-tagline strong{
  color:var(--sage-deep);font-style:italic;font-weight:500;
}
.solutions-tagline .num{
  font-family:var(--display-italic);
  font-style:italic;
  color:var(--terra-deep);
  font-weight:600;
  font-size:1.2em;
}

.solution-list{display:flex;flex-direction:column;gap:4px;}
.solution-item{
  display:flex;align-items:flex-start;gap:28px;
  padding:28px 0;
  border-bottom:1px solid rgba(31,29,26,.08);
  transition:all .35s cubic-bezier(.2,.8,.2,1);
  cursor:pointer;
}
.solution-item:last-child{border-bottom:none;}
.solution-item:hover{padding-left:10px;}
.solution-num{
  font-family:var(--display-italic);
  font-size:24px;font-weight:500;font-style:italic;
  color:var(--sage-deep);
  letter-spacing:0;
  flex-shrink:0;width:42px;
  padding-top:4px;
}
.solution-content{flex:1;}
.solution-name{
  font-family:var(--serif-kr);
  font-size:20px;font-weight:600;
  color:var(--ink);
  margin-bottom:10px;letter-spacing:-.3px;
}
.solution-desc{
  font-size:13.5px;color:var(--stone);
  line-height:1.75;font-weight:300;
}
.solution-arrow{
  flex-shrink:0;
  width:36px;height:36px;border-radius:50%;
  background:rgba(157,190,150,.15);
  display:flex;align-items:center;justify-content:center;
  color:var(--sage-deep);font-size:12px;
  transition:all .4s cubic-bezier(.2,.8,.2,1);
}
.solution-item:hover .solution-arrow{
  background:var(--sage-deep);color:white;
  transform:translateX(6px) rotate(-45deg);
}

.showcase-right{position:relative;display:flex;justify-content:center;}
.showcase-phone{
  width:316px;height:632px;
  background:#1a1814;
  border-radius:48px;padding:9px;
  box-shadow:0 60px 120px rgba(0,0,0,.2);
  position:relative;z-index:2;
}
.showcase-screen{
  width:100%;height:100%;
  background:white;
  border-radius:40px;
  overflow:hidden;
  position:relative;
}
.showcase-notch{
  position:absolute;top:8px;left:50%;
  transform:translateX(-50%);
  width:96px;height:26px;
  background:#1a1814;border-radius:14px;z-index:5;
}
.showcase-content{
  padding:48px 14px 14px;
  height:100%;overflow:hidden;
}
.showcase-tabs{
  display:flex;justify-content:space-around;align-items:center;
  padding:8px 4px 14px;
}
.showcase-tab{
  display:flex;flex-direction:column;align-items:center;gap:3px;
  padding:6px 12px;border-radius:16px;
}
.showcase-tab.active{background:rgba(199,123,115,.22);}
.showcase-tab-icon{font-size:20px;}
.showcase-tab-name{font-size:9.5px;font-weight:600;color:var(--ink);}
.showcase-tab.active .showcase-tab-name{color:var(--pink-deep);font-weight:700;}

.showcase-h{
  font-size:11.5px;color:var(--ink);font-weight:700;
  margin-bottom:10px;
  padding-left:5px;
}
.showcase-routine{
  background:rgba(199,123,115,.14);
  border-radius:14px;padding:12px 13px;
  display:flex;align-items:center;gap:11px;
  margin-bottom:7px;
}
.showcase-routine-icon{
  width:32px;height:32px;border-radius:9px;
  background:white;
  display:flex;align-items:center;justify-content:center;
  font-size:16px;flex-shrink:0;
}
.showcase-routine-info{flex:1;}
.showcase-routine-time{
  font-family:var(--grotesque);
  font-size:8px;letter-spacing:.5px;
  color:var(--pink-deep);font-weight:700;text-transform:uppercase;
}
.showcase-routine-name{font-size:11px;font-weight:700;color:var(--ink);line-height:1.25;}
.showcase-routine-desc{font-size:8.5px;color:var(--stone);}
.showcase-routine-check{
  width:18px;height:18px;border-radius:50%;
  background:var(--pink-deep);color:white;
  display:flex;align-items:center;justify-content:center;
  font-size:9px;
}

.showcase-deco{
  position:absolute;
  background:white;
  border-radius:16px;padding:13px 16px;
  box-shadow:0 24px 60px rgba(0,0,0,.14);
  display:flex;align-items:center;gap:10px;
  border:1px solid rgba(31,29,26,.05);
  z-index:3;
}
.showcase-deco-1{
  top:80px;right:-30px;
  animation:floatTag 5s ease-in-out infinite;
}
.showcase-deco-2{
  bottom:140px;left:-40px;
  animation:floatTag 6s ease-in-out infinite -2s;
}
.deco-icon{
  width:34px;height:34px;border-radius:9px;
  display:flex;align-items:center;justify-content:center;font-size:17px;
}
.deco-text strong{
  font-family:var(--grotesque);
  font-size:12.5px;color:var(--ink);font-weight:700;display:block;
}
.deco-text span{
  font-family:var(--grotesque);
  font-size:10px;color:var(--stone);
}

/* ═══════════════ AI TECH ═══════════════ */
.tech-section{
  background:
    radial-gradient(ellipse 60% 40% at 80% 30%,rgba(214,144,111,.16),transparent 70%),
    linear-gradient(165deg,#1a1814 0%,#2c241c 100%);
  color:var(--cream);
  position:relative;overflow:hidden;
}
.tech-section .section-inner{position:relative;z-index:2;}
.tech-section .section-eyebrow{color:var(--terra-soft);}
.tech-section .section-eyebrow::before{background:var(--terra-soft);}
.tech-section .section-title{color:var(--cream);}
.tech-section .section-title-italic{color:var(--terra-soft);}
.tech-section .section-desc{color:rgba(248,244,237,.55);}

.tech-grid{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:22px;margin-top:40px;
}
.tech-card{
  background:linear-gradient(165deg,rgba(255,255,255,.04),rgba(255,255,255,.01));
  border:1px solid rgba(255,255,255,.08);
  border-radius:22px;
  padding:36px 32px;
  transition:all .5s cubic-bezier(.2,.8,.2,1);
}
.tech-card:hover{
  border-color:rgba(214,144,111,.4);
  transform:translateY(-6px);
}
.tech-icon{
  width:52px;height:52px;border-radius:14px;
  background:rgba(214,144,111,.16);
  border:1px solid rgba(214,144,111,.28);
  display:flex;align-items:center;justify-content:center;
  font-size:24px;
  margin-bottom:22px;
}
.tech-num{
  font-family:var(--display);
  font-size:13px;font-weight:600;font-style:italic;
  color:var(--terra-soft);letter-spacing:1px;
  margin-bottom:12px;
  font-variation-settings:"opsz" 14;
}
.tech-name{
  font-family:var(--serif-kr);
  font-size:19px;font-weight:700;
  color:var(--cream);
  margin-bottom:14px;letter-spacing:-.3px;line-height:1.3;
}
.tech-desc{
  font-size:13.5px;color:rgba(248,244,237,.6);
  line-height:1.75;font-weight:300;margin-bottom:16px;
}
.tech-paper{
  background:rgba(214,144,111,.08);
  border-left:2px solid var(--terra);
  padding:11px 16px;border-radius:0 8px 8px 0;
}
.tech-paper-label{
  font-family:var(--grotesque);
  font-size:9.5px;letter-spacing:1.5px;font-weight:600;
  color:var(--terra-soft);text-transform:uppercase;
  margin-bottom:5px;
}
.tech-paper-cite{
  font-family:var(--batang);
  font-size:11.5px;color:rgba(248,244,237,.7);
  font-style:italic;line-height:1.55;
}

/* ═══════════════ PRICING ═══════════════ */
.pricing-section{
  background:
    radial-gradient(ellipse 50% 40% at 80% 70%,rgba(157,190,150,.15),transparent 70%),
    var(--cream);
}
.pricing-grid{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:22px;margin-top:56px;
}
.price-card{
  background:white;
  border-radius:28px;
  padding:44px 36px;
  border:1px solid rgba(31,29,26,.06);
  position:relative;
  transition:all .5s cubic-bezier(.2,.8,.2,1);
}
.price-card:hover{
  transform:translateY(-8px);
  box-shadow:0 30px 70px rgba(31,29,26,.08);
}
.price-card.featured{
  background:
    radial-gradient(ellipse 80% 60% at 30% 30%,rgba(157,190,150,.18),transparent 70%),
    linear-gradient(165deg,var(--sage-darkest),#1F3018);
  color:var(--cream);
  border-color:var(--sage-deep);
  box-shadow:0 24px 60px rgba(45,67,41,.25);
}
.price-tag{
  font-family:var(--grotesque);
  font-size:10.5px;letter-spacing:2px;font-weight:600;
  text-transform:uppercase;
  padding:6px 13px;border-radius:13px;
  display:inline-block;
  margin-bottom:18px;
}
.price-card .price-tag{background:rgba(157,190,150,.15);color:var(--sage-deep);}
.price-card.featured .price-tag{background:rgba(255,255,255,.12);color:var(--sage-light);}

.price-target{
  font-family:var(--serif-kr);
  font-size:13px;color:var(--stone);
  margin-bottom:18px;font-weight:300;
}
.price-card.featured .price-target{color:rgba(255,255,255,.55);}

.price-name{
  font-family:var(--display);
  font-size:34px;font-weight:300;
  color:var(--ink);
  margin-bottom:36px;letter-spacing:-1.2px;line-height:1.1;
  font-variation-settings:"opsz" 144;
}
.price-card.featured .price-name{color:var(--cream);}
.price-name em{
  font-style:italic;color:var(--sage-deep);font-weight:500;
  font-family:var(--display-italic);
}
.price-card.featured .price-name em{color:var(--sage-light);}

.price-tier{
  display:flex;justify-content:space-between;align-items:baseline;
  padding:18px 0;
  border-bottom:1px solid var(--mist);
}
.price-card.featured .price-tier{border-bottom-color:rgba(255,255,255,.1);}
.price-tier:last-of-type{border-bottom:none;}
.price-tier-label{
  font-family:var(--serif-kr);
  font-size:14.5px;font-weight:600;
  color:var(--ink);letter-spacing:-.2px;
}
.price-card.featured .price-tier-label{color:var(--cream);}
.price-tier-amount{
  font-family:var(--display);
  font-size:25px;font-weight:600;
  color:var(--ink);letter-spacing:-1px;line-height:1;
  font-variation-settings:"opsz" 14;
}
.price-card.featured .price-tier-amount{color:var(--sage-light);}
.price-tier-amount small{
  font-family:var(--grotesque);
  font-size:11px;color:var(--stone);font-weight:500;letter-spacing:.5px;
}
.price-card.featured .price-tier-amount small{color:rgba(255,255,255,.45);}

.price-features{
  list-style:none;
  margin-top:26px;display:flex;flex-direction:column;gap:9px;
}
.price-features li{
  font-size:12.5px;color:var(--ink-soft);
  font-weight:300;line-height:1.65;
  padding-left:18px;position:relative;
}
.price-card.featured .price-features li{color:rgba(255,255,255,.65);}
.price-features li::before{
  content:'✓';
  position:absolute;left:0;top:0;
  color:var(--sage-deep);font-weight:700;font-size:11px;
}
.price-card.featured .price-features li::before{color:var(--sage-light);}

/* ═══════════════ ROADMAP ═══════════════ */
.roadmap-section{
  background:
    radial-gradient(ellipse 60% 40% at 30% 30%,rgba(157,190,150,.15),transparent 70%),
    linear-gradient(180deg,var(--cream) 0%,var(--cream-warm) 100%);
}
.roadmap-track{
  margin-top:56px;
  position:relative;
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:0;
}
.roadmap-track::before{
  content:'';
  position:absolute;
  top:60px;left:8%;right:8%;
  height:2px;
  background:linear-gradient(90deg,
    var(--sage) 0%,
    var(--gold) 50%,
    var(--terra) 100%);
}
.phase{
  text-align:center;
  padding:0 28px;
  position:relative;
}
.phase-dot{
  width:30px;height:30px;border-radius:50%;
  background:white;
  border:3px solid var(--sage);
  margin:42px auto 26px;
  position:relative;z-index:1;
  transition:all .35s cubic-bezier(.2,.8,.2,1);
  box-shadow:0 4px 12px rgba(31,29,26,.08);
}
.phase:nth-child(2) .phase-dot{border-color:var(--gold);}
.phase:nth-child(3) .phase-dot{border-color:var(--terra);}
.phase:hover .phase-dot{transform:scale(1.25);}

.phase-tag{
  font-family:var(--grotesque);
  font-size:10.5px;letter-spacing:2.5px;font-weight:600;
  text-transform:uppercase;
  margin-bottom:8px;
}
.phase:nth-child(1) .phase-tag{color:var(--sage-deep);}
.phase:nth-child(2) .phase-tag{color:var(--gold-deep);}
.phase:nth-child(3) .phase-tag{color:var(--clay);}

.phase-title{
  font-family:var(--display-italic);
  font-size:36px;font-weight:400;font-style:italic;
  color:var(--ink);
  margin-bottom:6px;letter-spacing:-1px;
}
.phase-period{
  font-family:var(--grotesque);
  font-size:12px;color:var(--stone);
  font-weight:500;letter-spacing:.5px;
  margin-bottom:26px;
}
.phase-features{
  background:white;
  border-radius:20px;
  padding:26px 24px;
  border:1px solid rgba(31,29,26,.06);
  text-align:left;
  transition:transform .4s ease,box-shadow .4s ease;
}
.phase:hover .phase-features{
  transform:translateY(-4px);
  box-shadow:0 16px 40px rgba(31,29,26,.06);
}
.phase-features li{
  list-style:none;
  font-size:12.5px;color:var(--ink-soft);
  font-weight:300;line-height:1.7;
  padding:7px 0 7px 18px;
  position:relative;
  border-bottom:1px solid rgba(31,29,26,.05);
}
.phase-features li:last-child{border-bottom:none;}
.phase-features li::before{
  content:'';
  position:absolute;left:0;top:14px;
  width:6px;height:6px;border-radius:50%;
}
.phase:nth-child(1) .phase-features li::before{background:var(--sage);}
.phase:nth-child(2) .phase-features li::before{background:var(--gold);}
.phase:nth-child(3) .phase-features li::before{background:var(--terra);}

.roadmap-closing{
  text-align:center;
  margin-top:88px;padding:56px 36px;
  background:
    radial-gradient(ellipse 80% 60% at 50% 30%,rgba(232,201,136,.2),transparent 70%),
    linear-gradient(135deg,rgba(157,190,150,.1),rgba(214,144,111,.08));
  border-radius:28px;
  border:1px solid rgba(157,190,150,.2);
  position:relative;
  overflow:hidden;
}
.roadmap-closing-mark{
  font-size:42px;
  margin-bottom:24px;
  letter-spacing:10px;
  filter:drop-shadow(0 4px 8px rgba(31,29,26,.08));
}
.roadmap-closing-text{
  font-family:var(--display);
  font-size:clamp(30px,3.8vw,52px);
  font-weight:300;line-height:1.2;
  letter-spacing:-1.4px;
  color:var(--ink);
  margin-bottom:16px;
  font-variation-settings:"opsz" 144;
}
.roadmap-closing-text em{
  font-style:italic;
  color:var(--sage-deep);
  font-weight:500;
  font-family:var(--display-italic);
}
.roadmap-closing-sub{
  font-family:var(--serif-kr);
  font-size:14.5px;
  color:var(--stone);
  font-weight:300;
  letter-spacing:-.2px;
}

/* ═══════════════ IMPACT (8 outcomes) ═══════════════ */
.impact-section{
  background:linear-gradient(180deg,var(--cream-warm) 0%,var(--cream) 100%);
}
.impact-tracks{
  display:flex;flex-direction:column;gap:56px;
  margin-top:40px;
}
.impact-track-header{margin-bottom:36px;}
.impact-track-tag{
  display:inline-block;
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:2.5px;font-weight:600;
  text-transform:uppercase;
  padding:7px 16px;border-radius:14px;
  margin-bottom:16px;
}
.impact-track-tag.short{
  background:rgba(157,190,150,.18);
  color:var(--sage-deep);
  border:1px solid rgba(157,190,150,.3);
}
.impact-track-tag.long{
  background:rgba(214,144,111,.15);
  color:var(--clay);
  border:1px solid rgba(214,144,111,.3);
}
.impact-track-title{
  font-family:var(--display);
  font-size:clamp(30px,3.6vw,48px);
  font-weight:300;font-style:italic;
  line-height:1.2;letter-spacing:-1.2px;
  color:var(--ink);
  font-variation-settings:"opsz" 144;
}
.impact-grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:20px;
}
.impact-card{
  background:white;
  border-radius:20px;
  padding:30px 26px;
  border:1px solid rgba(31,29,26,.05);
  transition:all .5s cubic-bezier(.2,.8,.2,1);
  position:relative;
  overflow:hidden;
}
.impact-card:hover{
  transform:translateY(-6px);
  box-shadow:0 24px 60px rgba(31,29,26,.08);
  border-color:rgba(157,190,150,.4);
}
.impact-card::before{
  content:'';position:absolute;
  top:0;left:0;width:0;height:3px;
  transition:width .5s cubic-bezier(.2,.8,.2,1);
}
.impact-track:nth-child(1) .impact-card::before{background:var(--sage-deep);}
.impact-track:nth-child(2) .impact-card::before{background:var(--terra);}
.impact-card:hover::before{width:100%;}
.impact-num{
  font-family:var(--display-italic);
  font-size:18px;font-weight:500;font-style:italic;
  letter-spacing:1px;
  margin-bottom:14px;
}
.impact-track:nth-child(1) .impact-num{color:var(--sage-deep);}
.impact-track:nth-child(2) .impact-num{color:var(--clay);}
.impact-card h4{
  font-family:var(--serif-kr);
  font-size:17px;font-weight:700;
  color:var(--ink);
  line-height:1.4;letter-spacing:-.3px;
  margin-bottom:12px;
}
.impact-card p{
  font-size:12.5px;color:var(--stone);
  line-height:1.75;font-weight:300;
}

/* ═══════════════ MANIFESTO ═══════════════ */
.manifesto-section{
  background:
    radial-gradient(ellipse 60% 40% at 30% 30%,rgba(157,190,150,.15),transparent 70%),
    radial-gradient(ellipse 50% 40% at 70% 70%,rgba(214,144,111,.12),transparent 70%),
    linear-gradient(165deg,var(--sage-darkest) 0%,#1A2914 100%);
  color:var(--cream);
  padding:180px 56px;
  text-align:center;
  position:relative;overflow:hidden;
}
.manifesto-inner{position:relative;z-index:2;max-width:1100px;margin:0 auto;}

.manifesto-mark{
  font-family:var(--display-italic);
  font-size:96px;line-height:1;
  color:var(--sage-light);opacity:.35;
  margin-bottom:28px;
  font-style:italic;
}
.manifesto-text{
  font-family:var(--display);
  font-size:clamp(38px,4.8vw,72px);
  font-weight:300;
  line-height:1.2;letter-spacing:-1.8px;
  color:var(--cream);
  margin:0 auto 56px;
  font-variation-settings:"opsz" 144;
}
.manifesto-text em{
  font-style:italic;color:var(--sage-light);font-weight:500;
  font-family:var(--display-italic);
}
.manifesto-text .highlight{position:relative;display:inline-block;}
.manifesto-text .highlight::after{
  content:'';
  position:absolute;
  bottom:10px;left:-6px;right:-6px;
  height:16px;
  background:rgba(214,144,111,.45);
  z-index:-1;
  border-radius:4px;
}

.manifesto-pillars{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:24px;
  margin-top:88px;
}
.pillar{
  padding:36px 28px;
  border:1px solid rgba(255,255,255,.1);
  border-radius:20px;
  background:rgba(255,255,255,.03);
  text-align:center;
  transition:all .5s cubic-bezier(.2,.8,.2,1);
  position:relative;overflow:hidden;
}
.pillar:hover{
  border-color:rgba(157,190,150,.4);
  transform:translateY(-6px);
  background:rgba(255,255,255,.05);
}
.pillar-en{
  font-family:var(--display);
  font-size:20px;font-style:italic;font-weight:400;
  color:var(--sage-light);
  margin-bottom:16px;letter-spacing:-.5px;
  font-variation-settings:"opsz" 14;
}
.pillar-kr{
  font-family:var(--serif-kr);
  font-size:14px;font-weight:300;
  color:rgba(255,255,255,.7);
  line-height:1.75;
}

.manifesto-author{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:3.5px;font-weight:600;
  color:rgba(255,255,255,.4);text-transform:uppercase;
  margin-top:72px;
}

/* ═══════════════ CTA ═══════════════ */
.cta-section{
  background:
    radial-gradient(ellipse 70% 50% at 80% 20%,rgba(232,201,136,.4),transparent 70%),
    radial-gradient(ellipse 60% 40% at 20% 80%,rgba(157,190,150,.35),transparent 70%),
    var(--cream);
  padding:180px 56px;
  position:relative;overflow:hidden;
}
.cta-inner{
  max-width:920px;margin:0 auto;
  text-align:center;position:relative;z-index:2;
}
.cta-eyebrow{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:4px;font-weight:600;
  color:var(--sage-deep);text-transform:uppercase;
  margin-bottom:28px;
}
.cta-title{
  font-family:var(--display);
  font-size:clamp(50px,6.8vw,116px);
  font-weight:300;line-height:1.02;
  letter-spacing:-3px;
  color:var(--ink);
  margin-bottom:36px;
  font-variation-settings:"opsz" 144;
}
.cta-title-italic{
  font-style:italic;color:var(--sage-deep);font-weight:500;
}
.cta-desc{
  font-family:var(--serif-kr);
  font-size:17.5px;line-height:1.9;font-weight:300;
  color:var(--ink-soft);
  max-width:580px;margin:0 auto 52px;
}
.cta-buttons{display:flex;gap:18px;justify-content:center;flex-wrap:wrap;}
.btn-cta-primary{
  background:var(--ink);color:var(--cream);
  padding:20px 40px;border-radius:36px;
  font-family:var(--grotesque);
  font-size:14px;font-weight:600;letter-spacing:.5px;
  text-decoration:none;
  display:inline-flex;align-items:center;gap:14px;
  transition:all .4s cubic-bezier(.2,.8,.2,1);
}
.btn-cta-primary:hover{
  background:var(--sage-deep);
  transform:translateY(-3px);
  box-shadow:0 20px 50px rgba(90,127,84,.35);
}
.btn-cta-secondary{
  background:transparent;color:var(--ink);
  border:1px solid rgba(31,29,26,.2);
  padding:20px 40px;border-radius:36px;
  font-family:var(--grotesque);
  font-size:14px;font-weight:500;letter-spacing:.5px;
  text-decoration:none;
  display:inline-flex;align-items:center;gap:14px;
  transition:all .4s cubic-bezier(.2,.8,.2,1);
}
.btn-cta-secondary:hover{
  background:white;border-color:var(--sage-deep);
  transform:translateY(-3px);
}

/* ═══════════════ FOOTER ═══════════════ */
footer{
  background:var(--ink);
  color:var(--stone-light);
  padding:88px 56px 44px;
}
.footer-inner{max-width:1280px;margin:0 auto;}
.footer-grid{
  display:grid;grid-template-columns:2fr 1fr 1fr 1fr;
  gap:64px;
  padding-bottom:52px;
  border-bottom:1px solid rgba(255,255,255,.08);
  margin-bottom:36px;
}
.footer-logo{
  font-family:var(--display);
  font-size:30px;font-weight:400;
  color:var(--cream);
  letter-spacing:-.6px;
  margin-bottom:18px;
  font-variation-settings:"opsz" 144;
}
.footer-logo em{
  font-family:var(--display-italic);
  font-style:italic;
  color:var(--sage-light);
}
.footer-tagline{
  font-family:var(--serif-kr);
  font-size:14px;line-height:1.85;font-weight:300;
  color:rgba(248,244,237,.55);
  max-width:340px;
}
.footer-col-title{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:2.5px;font-weight:600;
  color:var(--sage-light);text-transform:uppercase;
  margin-bottom:20px;
}
.footer-col ul{list-style:none;display:flex;flex-direction:column;gap:11px;}
.footer-col a{
  font-family:var(--sans-kr);
  font-size:13px;color:rgba(248,244,237,.55);
  text-decoration:none;
  transition:color .25s ease;
  font-weight:300;
}
.footer-col a:hover{color:var(--cream);}
.footer-bottom{
  display:flex;justify-content:space-between;align-items:center;
  padding-top:26px;
  font-family:var(--grotesque);
  font-size:11px;color:rgba(248,244,237,.35);
  letter-spacing:.5px;flex-wrap:wrap;gap:18px;
}
.footer-disclaimer{
  font-family:var(--batang);
  font-size:11.5px;color:rgba(248,244,237,.4);
  font-weight:400;
  background:rgba(255,255,255,.03);
  padding:16px 20px;border-radius:10px;
  margin-top:26px;line-height:1.7;
  font-style:italic;
  border-left:2px solid rgba(157,190,150,.3);
}

/* ═══════════════ RESPONSIVE ═══════════════ */
@media (max-width:1100px){
  .stats-grid{grid-template-columns:1fr 1fr;}
  .stat-block{border-right:none;border-bottom:1px solid var(--mist);}
  .stat-block:nth-child(2){border-right:none;}
  .stat-block:nth-child(2n){border-right:none;}
  .stat-block:nth-last-child(-n+2){border-bottom:none;}
  .gaps-grid{grid-template-columns:1fr 1fr;}
  .tabs-grid{grid-template-columns:repeat(3,1fr);}
  .pricing-grid{grid-template-columns:1fr;}
  .forest-stages{grid-template-columns:repeat(4,1fr);gap:32px;padding:24px 0;}
  .forest-stages::before{display:none;}
  .impact-grid{grid-template-columns:repeat(2,1fr);}
  .column-grid{grid-template-columns:1fr;gap:56px;}
  .column-left{position:relative;top:0;}
}
@media (max-width:980px){
  .nav{padding:18px 24px;}
  .nav.scrolled{padding:14px 24px;}
  .nav-menu{display:none;}
  .hero{padding:120px 24px 60px;}
  .hero-grid{grid-template-columns:1fr;gap:60px;}
  .section{padding:80px 24px;}
  .problem-trio{grid-template-columns:1fr;}
  .trees-trio{grid-template-columns:1fr;}
  .roadmap-track{grid-template-columns:1fr;gap:36px;}
  .roadmap-track::before{display:none;}
  .solutions-grid{grid-template-columns:1fr;gap:56px;}
  .tech-grid{grid-template-columns:1fr;}
  .manifesto-pillars{grid-template-columns:1fr;}
  .footer-grid{grid-template-columns:1fr 1fr;gap:36px;}
  .flow-track{grid-template-columns:1fr;gap:24px;}
  .flow-step.center{transform:scale(1);}
  .flow-step.center:hover{transform:translateY(-6px);}
  .flow-arrow{transform:rotate(90deg);padding:0;}
  .manifesto-section{padding:120px 24px;}
}
@media (max-width:640px){
  .stats-grid{grid-template-columns:1fr;}
  .stat-block{border-right:none;border-bottom:1px solid var(--mist);}
  .stat-block:last-child{border-bottom:none;}
  .gaps-grid{grid-template-columns:1fr;}
  .tabs-grid{grid-template-columns:1fr;}
  .forest-stages{grid-template-columns:repeat(2,1fr);}
  .footer-grid{grid-template-columns:1fr;}
  .impact-grid{grid-template-columns:1fr;}
  .phone-floating-tag{display:none;}
}
</style>
</head>
<body>

<!-- ═══════════════ NAV ═══════════════ -->
<nav class="nav" id="nav">
  <a href="#top" class="nav-logo">
    <span class="nav-logo-mark">🌿</span>
    The <em>Bottom</em> Line
  </a>
  <div class="nav-menu">
    <a href="#problem" class="nav-link">문제 인식</a>
    <a href="#service" class="nav-link">서비스</a>
    <a href="#column" class="nav-link">전문가 칼럼</a>
    <a href="#tech" class="nav-link">기술</a>
    <a href="#pricing" class="nav-link">요금제</a>
    <a href="#cta" class="nav-cta">
      앱 다운로드
      <span class="nav-cta-arrow">→</span>
    </a>
  </div>
</nav>

<!-- ═══════════════ HERO ═══════════════ -->
<section class="hero" id="top">
  <div class="hero-orb hero-orb-1"></div>
  <div class="hero-orb hero-orb-2"></div>
  <div class="hero-orb hero-orb-3"></div>

  <div class="hero-grid">
    <div class="hero-text">
      <div class="hero-eyebrow">
        <span class="hero-eyebrow-dot"></span>
        하부 이너뷰티 예방 웰니스
      </div>
      <h1 class="hero-title">
        <span class="hero-title-row1">보이지 않는 곳까지,</span>
        <span class="hero-title-row2">당신의 건강을<br><span class="hero-title-mark">끌어올리다.</span></span>
      </h1>
      <p class="hero-subtitle">
        병원 가기엔 애매하고, 그냥 두기엔 불안한 그 중간.<br>
        <strong>하루 3초의 기록</strong>으로 시작되는, 부끄럽지 않은 자기 관리.
      </p>
      <div class="hero-actions">
        <a href="#cta" class="btn-primary">
          <span>시작하기</span>
          <span class="btn-arrow">→</span>
        </a>
        <a href="#service" class="btn-text">서비스 둘러보기</a>
      </div>
      <div class="hero-tags">
        <span class="hero-tag"><span>#</span>하부이너뷰티</span>
        <span class="hero-tag"><span>#</span>단백뇨관리</span>
        <span class="hero-tag"><span>#</span>치질예방</span>
        <span class="hero-tag"><span>#</span>나노루틴</span>
        <span class="hero-tag"><span>#</span>나의숲</span>
        <span class="hero-tag"><span>#</span>AI거품분석</span>
      </div>
    </div>

    <div class="hero-visual">
      <!-- Floating tags showing tree-specific routines -->
      <div class="phone-floating-tag tag-1">
        <div class="phone-floating-tag-icon" style="background:linear-gradient(135deg,#E0EFDE,#C5DBC0);">🪵</div>
        <div class="phone-floating-tag-info">
          <strong>소나무 · 단백뇨</strong>
          <span>물 2컵 · 신장 세척</span>
        </div>
      </div>
      <div class="phone-floating-tag tag-2">
        <div class="phone-floating-tag-icon" style="background:linear-gradient(135deg,#FCE5E2,#F2C0BB);">🫘</div>
        <div class="phone-floating-tag-info">
          <strong>대나무 · 치질 예방</strong>
          <span>좌욕 5분 · 혈류 개선</span>
        </div>
      </div>
      <div class="phone-floating-tag tag-3">
        <div class="phone-floating-tag-icon" style="background:linear-gradient(135deg,#FBE0EE,#F2C8DD);">🌸</div>
        <div class="phone-floating-tag-info">
          <strong>벚꽃나무 · 식이</strong>
          <span>식물성 단백질 · 장 건강</span>
        </div>
      </div>

      <div class="phone-shell">
        <div class="phone-screen">
          <div class="phone-notch"></div>
          <div class="phone-content">
            <!-- Tree tabs — 벚꽃나무 / 소나무 / 대나무 (matches uploaded images) -->
            <div class="tree-tabs">
              <div class="tree-tab">
                <div class="tree-tab-icon">🌸</div>
                <div class="tree-tab-name">벚꽃나무</div>
              </div>
              <div class="tree-tab active">
                <div class="tree-tab-icon">🪵</div>
                <div class="tree-tab-name">소나무</div>
              </div>
              <div class="tree-tab">
                <div class="tree-tab-icon">🫘</div>
                <div class="tree-tab-name">대나무</div>
              </div>
            </div>

            <div class="routine-title">오늘의 나노 루틴</div>
            <!-- 소나무 = 단백뇨 관리 루틴 (매칭) -->
            <div class="routine-card">
              <div class="routine-icon">💧</div>
              <div class="routine-info">
                <div class="routine-time">아침 루틴</div>
                <div class="routine-name">물 2컵 마시기</div>
                <div class="routine-desc">신장 세척 · 400ml 권장</div>
              </div>
              <div class="routine-check">✓</div>
            </div>
            <div class="routine-card">
              <div class="routine-icon">🥗</div>
              <div class="routine-info">
                <div class="routine-time">점심 루틴</div>
                <div class="routine-name">저염 식단 체크</div>
                <div class="routine-desc">나트륨 제한 · 단백뇨 예방</div>
              </div>
              <div class="routine-check">✓</div>
            </div>
            <div class="routine-card">
              <div class="routine-icon">📊</div>
              <div class="routine-info">
                <div class="routine-time">저녁 루틴</div>
                <div class="routine-name">단백뇨 수치 기록</div>
                <div class="routine-desc">소변 검사 스트립 확인</div>
              </div>
              <div class="routine-check">✓</div>
            </div>

            <!-- 나만의 숲 미니 -->
            <div class="phone-forest-status">
              <div class="phone-forest-h">🌿 나만의 숲 성장 현황</div>
              <div class="phone-forest-row">
                <span class="phone-forest-icon">🌸</span>
                <span class="phone-forest-label">벚꽃나무 · 새잎</span>
                <div class="phone-forest-bar"><div class="phone-forest-bar-fill" style="background:var(--pink-deep);width:67%;"></div></div>
              </div>
              <div class="phone-forest-row">
                <span class="phone-forest-icon">🪵</span>
                <span class="phone-forest-label">소나무 · 새순</span>
                <div class="phone-forest-bar"><div class="phone-forest-bar-fill" style="background:var(--sage-deep);width:67%;"></div></div>
              </div>
              <div class="phone-forest-row">
                <span class="phone-forest-icon">🫘</span>
                <span class="phone-forest-label">대나무 · 씨앗</span>
                <div class="phone-forest-bar"><div class="phone-forest-bar-fill" style="background:var(--clay);width:30%;"></div></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ TICKER ═══════════════ -->
<section class="ticker-section">
  <div class="ticker">
    <span class="ticker-item"><em>3초의 기록</em></span>
    <span class="ticker-dot"></span>
    <span class="ticker-item">나의 숲을 키우다</span>
    <span class="ticker-dot"></span>
    <span class="ticker-item"><em>피부 관리하듯</em></span>
    <span class="ticker-dot"></span>
    <span class="ticker-item">하부 건강 관리</span>
    <span class="ticker-dot"></span>
    <span class="ticker-item"><em>병원 가기 전 단계</em></span>
    <span class="ticker-dot"></span>
    <span class="ticker-item">예방형 웰니스</span>
    <span class="ticker-dot"></span>
    <span class="ticker-item"><em>3초의 기록</em></span>
    <span class="ticker-dot"></span>
    <span class="ticker-item">나의 숲을 키우다</span>
    <span class="ticker-dot"></span>
    <span class="ticker-item"><em>피부 관리하듯</em></span>
    <span class="ticker-dot"></span>
    <span class="ticker-item">하부 건강 관리</span>
    <span class="ticker-dot"></span>
    <span class="ticker-item"><em>병원 가기 전 단계</em></span>
    <span class="ticker-dot"></span>
    <span class="ticker-item">예방형 웰니스</span>
    <span class="ticker-dot"></span>
  </div>
</section>

<!-- ═══════════════ MARKET — 무리한 다이어트 메시지로 변경 ═══════════════ -->
<section class="section market-section" id="problem">
  <div class="section-inner">
    <div class="section-eyebrow reveal">시장 현황 · 문제 인식</div>
    <!-- UPDATED HEADLINE per user request -->
    <h2 class="market-headline reveal">
      무리한 다이어트·<em>안 좋은 생활습관</em>으로 인한<br>
      <strong>하부 건강 질환</strong>이 가파르게 증가하고 있습니다.
    </h2>

    <div class="stats-grid reveal">
      <div class="stat-block">
        <div class="stat-tag"><span class="stat-tag-dot"></span>만성콩팥병</div>
        <div class="stat-num">90<small>%↑</small></div>
        <div class="stat-label">말기콩팥병 유병 인구</div>
        <div class="stat-source">2012 → 2022 · 10년간 증가율<br>대한신장학회 팩트시트 2024</div>
      </div>
      <div class="stat-block">
        <div class="stat-tag"><span class="stat-tag-dot"></span>치질·치핵</div>
        <div class="stat-num">632<small>K+</small></div>
        <div class="stat-label">연간 치질 환자 수</div>
        <div class="stat-source">2021년 국내 기준<br>건강보험심사평가원</div>
      </div>
      <div class="stat-block">
        <div class="stat-tag"><span class="stat-tag-dot"></span>의료 비용</div>
        <div class="stat-num">2,508<small>억</small></div>
        <div class="stat-label">연간 치질 진료비</div>
        <div class="stat-source">2022년 기준<br>최근 5년간 지속 상승</div>
      </div>
      <div class="stat-block">
        <div class="stat-tag"><span class="stat-tag-dot"></span>20~40대 위험군</div>
        <div class="stat-num">50<small>%↑</small></div>
        <div class="stat-label">30~50대 환자 비중</div>
        <div class="stat-source">젊은층 관련 질환<br>경험 증가 추세</div>
      </div>
    </div>

    <div class="problem-trio">
      <div class="problem-card reveal">
        <div class="problem-card-num">PROBLEM / 01</div>
        <div class="problem-card-icon">🥗</div>
        <h3 class="problem-card-title">영양성 문제</h3>
        <p class="problem-card-desc">
          섬유질 부족 → 변비 유발. 신장 부담 증가, 반복적 체중 감량 사이클이 누적됩니다.
        </p>
      </div>
      <div class="problem-card reveal">
        <div class="problem-card-num">PROBLEM / 02</div>
        <div class="problem-card-icon">🪑</div>
        <h3 class="problem-card-title">신체성 문제</h3>
        <p class="problem-card-desc">
          하루 평균 8~10시간 좌식 생활. 항문·골반 혈류 저하, 소화기 기능 저하로 직장인 위험군 급증.
        </p>
      </div>
      <div class="problem-card reveal">
        <div class="problem-card-num">PROBLEM / 03</div>
        <div class="problem-card-icon">🤐</div>
        <h3 class="problem-card-title">정보성 문제</h3>
        <p class="problem-card-desc">
          '민감한 부위'라는 인식으로 병원 방문이 지연되고, 그 사이 조기 인지에 실패합니다.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ 4 GAPS ═══════════════ -->
<section class="section gaps-section">
  <div class="section-inner">
    <div class="section-eyebrow reveal">기존 의료서비스의 한계</div>
    <h2 class="section-title reveal">
      병원과 일상 사이,<br>
      <span class="section-title-italic">예방의 공백.</span>
    </h2>
    <p class="section-desc reveal">
      The Bottom Line은 기존 의료서비스를 대체하지 않습니다.
      그 사이의 빈 자리에서 시작합니다.
    </p>

    <div class="gaps-grid">
      <div class="gap-card reveal">
        <div class="gap-num">01</div>
        <h3 class="gap-title">무증상·경계 단계의<br>포착 어려움</h3>
        <p class="gap-desc">증상이 없으면 사용자가 스스로 인지하기 어렵습니다.</p>
      </div>
      <div class="gap-card reveal">
        <div class="gap-num">02</div>
        <h3 class="gap-title">검진 이후의<br>지속 관리 단절</h3>
        <p class="gap-desc">검진 결과 유소견이 있어도 관리 행동으로 이어지지 않습니다.</p>
      </div>
      <div class="gap-card reveal">
        <div class="gap-num">03</div>
        <h3 class="gap-title">진료실 밖 생활습관<br>실행의 어려움</h3>
        <p class="gap-desc">섬유질·수분·배변 습관 교정 등 일상에서 장기간 수행이 필요합니다.</p>
      </div>
      <div class="gap-card reveal">
        <div class="gap-num">04</div>
        <h3 class="gap-title">민감한 증상의<br>의료 이용 지연</h3>
        <p class="gap-desc">낙인 우려·당혹감으로 병원 방문이 늦어지고 관리 공백이 길어집니다.</p>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ JOURNEY ═══════════════ -->
<section class="journey-section" id="journey">
  <div class="section-inner" style="padding:0 56px;">
    <div class="section-eyebrow reveal">고객의 이야기 · 8개 장면</div>
    <h2 class="section-title reveal">
      이지은이<br>
      <span class="section-title-italic">되찾은 것들.</span>
    </h2>
    <p class="section-desc reveal">
      33세 마케터, 2년간 15kg 감량. 성공의 이면에서 발견된 거품뇨에서 시작해<br>
      <em style="color:var(--sage-light);font-style:italic;">자기 몸의 언어를 다시 이해하기까지</em>의 8개 장면.
    </p>
  </div>

  <div class="journey-track">
    <div class="journey-scenes" id="journeyScenes">
      <div class="scene-card">
        <div class="scene-num-row"><span class="scene-num">SCENE / 01</span><div class="scene-line"></div><span class="scene-emo">😟</span></div>
        <div class="scene-illust scene-illust-1">
          <svg viewBox="0 0 300 180" width="260" height="160" xmlns="http://www.w3.org/2000/svg">
            <!-- toilet bowl shape -->
            <ellipse cx="150" cy="110" rx="90" ry="22" fill="rgba(157,190,150,.18)" stroke="rgba(157,190,150,.4)" stroke-width="1.5"/>
            <path d="M70 112 Q68 160 100 175 L200 175 Q232 160 230 112" fill="none" stroke="rgba(255,255,255,.15)" stroke-width="1.5"/>
            <!-- water surface shimmer -->
            <ellipse cx="150" cy="110" rx="82" ry="16" fill="rgba(100,170,200,.18)"/>
            <!-- bubbles large -->
            <circle cx="118" cy="103" r="8" fill="rgba(255,255,255,.65)"><animate attributeName="cy" values="103;94;103" dur="2.4s" repeatCount="indefinite"/><animate attributeName="r" values="8;9.5;8" dur="2.4s" repeatCount="indefinite"/></circle>
            <circle cx="148" cy="108" r="11" fill="rgba(255,255,255,.75)"><animate attributeName="cy" values="108;97;108" dur="2.8s" repeatCount="indefinite"/><animate attributeName="r" values="11;13;11" dur="2.8s" repeatCount="indefinite"/></circle>
            <circle cx="178" cy="104" r="8" fill="rgba(255,255,255,.6)"><animate attributeName="cy" values="104;95;104" dur="2.2s" repeatCount="indefinite"/><animate attributeName="r" values="8;9;8" dur="2.2s" repeatCount="indefinite"/></circle>
            <circle cx="135" cy="114" r="6" fill="rgba(255,255,255,.55)"><animate attributeName="cy" values="114;108;114" dur="2s" repeatCount="indefinite"/></circle>
            <circle cx="163" cy="116" r="5" fill="rgba(255,255,255,.5)"><animate attributeName="cy" values="116;110;116" dur="1.8s" repeatCount="indefinite"/></circle>
            <!-- question mark -->
            <text x="150" y="58" font-size="44" fill="rgba(212,144,111,.85)" text-anchor="middle" font-style="italic" font-family="Georgia,serif">?</text>
            <!-- label -->
            <text x="150" y="148" font-size="11" fill="rgba(255,255,255,.45)" text-anchor="middle" font-family="sans-serif" letter-spacing="2">FOAM DETECTED</text>
          </svg>
        </div>
        <div class="scene-phase">균열의 시작</div>
        <h3 class="scene-title">15kg을 빼고 나서,<br>거품이 보였다</h3>
        <p class="scene-text">2년간의 고단백 식단과 필라테스. 어느 날 아침, 화장실에서 거품이 보이기 시작했다.</p>
        <div class="scene-quote">"이게 뭐지... 원래 이런 거였나?"</div>
      </div>
      <div class="scene-card">
        <div class="scene-num-row"><span class="scene-num">SCENE / 02</span><div class="scene-line"></div><span class="scene-emo">😔</span></div>
        <div class="scene-illust scene-illust-2">
          <svg viewBox="0 0 300 180" width="260" height="160" xmlns="http://www.w3.org/2000/svg">
            <!-- phone frame -->
            <rect x="70" y="14" width="160" height="155" rx="14" fill="rgba(255,255,255,.97)" stroke="rgba(0,0,0,.08)" stroke-width="1"/>
            <!-- search bar -->
            <rect x="82" y="26" width="136" height="18" rx="9" fill="#f0f0f0"/>
            <text x="92" y="39" font-size="9" fill="#888" font-family="sans-serif">🔍  거품뇨 원인</text>
            <!-- result 1 — warning -->
            <rect x="82" y="52" width="136" height="32" rx="5" fill="rgba(255,220,220,.6)"/>
            <text x="89" y="64" font-size="9" fill="#1a0dab" font-family="sans-serif" font-weight="600">거품뇨, 정말 위험한가요?</text>
            <text x="89" y="76" font-size="8" fill="#cc3333" font-family="sans-serif">단백뇨 의심, 만성콩팥병 초기...</text>
            <!-- result 2 -->
            <rect x="82" y="90" width="136" height="28" rx="5" fill="rgba(255,255,255,.8)"/>
            <text x="89" y="102" font-size="9" fill="#1a0dab" font-family="sans-serif">고단백 식단의 위험성</text>
            <text x="89" y="113" font-size="8" fill="#555" font-family="sans-serif">신장 부담을 키울 수 있어...</text>
            <!-- result 3 -->
            <rect x="82" y="124" width="136" height="28" rx="5" fill="rgba(255,255,255,.8)"/>
            <text x="89" y="136" font-size="9" fill="#1a0dab" font-family="sans-serif">병원 가야 할까요?</text>
            <text x="89" y="147" font-size="8" fill="#555" font-family="sans-serif">검사 시기를 놓치면...</text>
            <!-- sad face overlay top right -->
            <text x="215" y="50" font-size="28" text-anchor="middle">😟</text>
          </svg>
        </div>
        <div class="scene-phase">불안의 증폭</div>
        <h3 class="scene-title">검색은 답이 아니라<br>불안이었다</h3>
        <p class="scene-text">첫 줄: "단백뇨 의심, 만성콩팥병 초기 증상일 수 있습니다." 내과 예약 창을 열었다 닫았다.</p>
        <div class="scene-quote">"카톡을 쓰다 지웠다. 너무 오버하는 것 같아서."</div>
      </div>
      <div class="scene-card">
        <div class="scene-num-row"><span class="scene-num">SCENE / 03</span><div class="scene-line"></div><span class="scene-emo">🤔</span></div>
        <div class="scene-illust scene-illust-3">
          <svg viewBox="0 0 300 180" width="260" height="160" xmlns="http://www.w3.org/2000/svg">
            <!-- phone frame -->
            <rect x="90" y="8" width="120" height="166" rx="14" fill="#111"/>
            <rect x="93" y="12" width="114" height="158" rx="11" fill="url(#reelGrad)"/>
            <defs>
              <linearGradient id="reelGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" style="stop-color:#3a6e34"/>
                <stop offset="100%" style="stop-color:#1a3a16"/>
              </linearGradient>
            </defs>
            <!-- reel content -->
            <text x="150" y="58" font-size="22" text-anchor="middle">🌿</text>
            <text x="150" y="88" font-size="9" fill="white" text-anchor="middle" font-weight="700" font-family="sans-serif">"다이어트 중</text>
            <text x="150" y="101" font-size="9" fill="white" text-anchor="middle" font-weight="700" font-family="sans-serif">몸이 보내는 신호,</text>
            <text x="150" y="114" font-size="9" fill="white" text-anchor="middle" font-weight="700" font-family="sans-serif">무시하고 있나요?"</text>
            <!-- handle -->
            <text x="150" y="136" font-size="8" fill="rgba(255,255,255,.7)" text-anchor="middle" font-family="sans-serif">@wellness_pilates</text>
            <!-- like / comment icons -->
            <text x="191" y="85" font-size="13" text-anchor="middle">❤️</text>
            <text x="191" y="105" font-size="13" text-anchor="middle">💬</text>
            <!-- glow hint on left -->
            <circle cx="40" cy="90" r="28" fill="rgba(157,190,150,.18)" filter="blur(10px)"/>
            <text x="40" y="96" font-size="26" text-anchor="middle">✨</text>
          </svg>
        </div>
        <div class="scene-phase">우연한 발견</div>
        <h3 class="scene-title">SNS에서 우연히,<br>나만 그런 게 아니었다</h3>
        <p class="scene-text">주말 인스타그램 릴스. 필라테스 강사가 자기 경험을 말한다. 병원 가기 전에 시작한 기록 이야기.</p>
        <div class="scene-quote">"바로 병원이 아닌 선택지가 있다는 걸 처음 알았다."</div>
      </div>
      <div class="scene-card">
        <div class="scene-num-row"><span class="scene-num">SCENE / 04</span><div class="scene-line"></div><span class="scene-emo">😊</span></div>
        <div class="scene-illust scene-illust-4">
          <svg viewBox="0 0 300 180" width="260" height="160" xmlns="http://www.w3.org/2000/svg">
            <!-- card bg -->
            <rect x="50" y="10" width="200" height="162" rx="16" fill="rgba(255,255,255,.97)"/>
            <!-- title -->
            <text x="150" y="34" font-size="11" fill="#2C2A26" text-anchor="middle" font-weight="700" font-family="sans-serif">자가 체크 7문항</text>
            <text x="150" y="48" font-size="8.5" fill="#7A746C" text-anchor="middle" font-family="sans-serif">위험군 여부를 확인해보세요</text>
            <!-- checked rows -->
            <rect x="62" y="56" width="176" height="24" rx="6" fill="rgba(157,190,150,.55)"/>
            <text x="74" y="72" font-size="9.5" fill="white" font-family="sans-serif">고단백 식단 6개월 이상</text>
            <text x="226" y="72" font-size="13" fill="white" text-anchor="middle">✓</text>
            <rect x="62" y="84" width="176" height="24" rx="6" fill="rgba(157,190,150,.55)"/>
            <text x="74" y="100" font-size="9.5" fill="white" font-family="sans-serif">거품뇨를 경험한 적 있다</text>
            <text x="226" y="100" font-size="13" fill="white" text-anchor="middle">✓</text>
            <rect x="62" y="112" width="176" height="24" rx="6" fill="rgba(157,190,150,.55)"/>
            <text x="74" y="128" font-size="9.5" fill="white" font-family="sans-serif">하루 8시간 이상 좌식</text>
            <text x="226" y="128" font-size="13" fill="white" text-anchor="middle">✓</text>
            <!-- result banner -->
            <rect x="62" y="144" width="176" height="22" rx="7" fill="rgba(90,127,84,.15)" stroke="rgba(90,127,84,.35)" stroke-width="1"/>
            <text x="150" y="158" font-size="9" fill="#5A7F54" text-anchor="middle" font-family="sans-serif" font-style="italic">기록을 시작할 적절한 타이밍이에요 ✦</text>
          </svg>
        </div>
        <div class="scene-phase">첫 만남</div>
        <h3 class="scene-title">7개 문항,<br>전부 '예'였다</h3>
        <p class="scene-text">앱이 말했다. 병원을 권유하는 대신, "지금은 생활기록을 시작할 적절한 타이밍이에요."</p>
        <div class="scene-quote">"의사가 아닌, 옆에서 말해주는 것 같았다."</div>
      </div>
      <div class="scene-card">
        <div class="scene-num-row"><span class="scene-num">SCENE / 05</span><div class="scene-line"></div><span class="scene-emo">🌱</span></div>
        <div class="scene-illust scene-illust-5">
          <svg viewBox="0 0 300 180" width="260" height="160" xmlns="http://www.w3.org/2000/svg">
            <rect x="40" y="10" width="220" height="162" rx="16" fill="rgba(255,255,255,.97)"/>
            <text x="55" y="32" font-size="11" fill="#2C2A26" font-weight="700" font-family="sans-serif">오늘의 나노 루틴</text>
            <!-- routine 1 -->
            <rect x="52" y="40" width="196" height="26" rx="8" fill="rgba(157,190,150,.2)"/>
            <text x="62" y="49" font-size="11">🚶</text>
            <text x="80" y="48" font-size="9" fill="#3D3A35" font-family="sans-serif" font-weight="600">기상 후 스트레칭</text>
            <text x="80" y="59" font-size="7.5" fill="#7A746C" font-family="sans-serif">항문 혈류 개선 5분</text>
            <circle cx="234" cy="53" r="9" fill="#5A7F54"/>
            <text x="234" y="57" font-size="9" fill="white" text-anchor="middle">✓</text>
            <!-- routine 2 -->
            <rect x="52" y="72" width="196" height="26" rx="8" fill="rgba(157,190,150,.2)"/>
            <text x="62" y="81" font-size="11">🌿</text>
            <text x="80" y="80" font-size="9" fill="#3D3A35" font-family="sans-serif" font-weight="600">식이섬유 섭취</text>
            <text x="80" y="91" font-size="7.5" fill="#7A746C" font-family="sans-serif">채소·과일 목표량 절반</text>
            <circle cx="234" cy="85" r="9" fill="#5A7F54"/>
            <text x="234" y="89" font-size="9" fill="white" text-anchor="middle">✓</text>
            <!-- routine 3 -->
            <rect x="52" y="104" width="196" height="26" rx="8" fill="rgba(157,190,150,.2)"/>
            <text x="62" y="113" font-size="11">🪑</text>
            <text x="80" y="112" font-size="9" fill="#3D3A35" font-family="sans-serif" font-weight="600">좌욕 5분</text>
            <text x="80" y="123" font-size="7.5" fill="#7A746C" font-family="sans-serif">하부 케어 루틴 유지</text>
            <circle cx="234" cy="117" r="9" fill="#5A7F54"/>
            <text x="234" y="121" font-size="9" fill="white" text-anchor="middle">✓</text>
            <!-- forest mini -->
            <rect x="52" y="138" width="196" height="26" rx="8" fill="rgba(157,190,150,.1)" stroke="rgba(157,190,150,.3)" stroke-width="1"/>
            <text x="62" y="153" font-size="11">🌱</text>
            <text x="78" y="153" font-size="9" fill="#5A7F54" font-family="sans-serif" font-weight="600">벚꽃나무 · 씨앗 → 새잎 성장 중!</text>
          </svg>
        </div>
        <div class="scene-phase">루틴의 시작</div>
        <h3 class="scene-title">하루 3초,<br>식물이 자랐다</h3>
        <p class="scene-text">출근길 지하철에서 엄지 세 번. 14일째, 처음으로 빠짐없이 기록을 마쳤다.</p>
        <div class="scene-quote">"기록이 귀찮다고 생각했는데, 진짜 3초였다."</div>
      </div>
      <div class="scene-card">
        <div class="scene-num-row"><span class="scene-num">SCENE / 06</span><div class="scene-line"></div><span class="scene-emo">💚</span></div>
        <div class="scene-illust scene-illust-6">
          <svg viewBox="0 0 300 180" width="260" height="160" xmlns="http://www.w3.org/2000/svg">
            <rect x="30" y="8" width="240" height="166" rx="16" fill="rgba(255,255,255,.97)"/>
            <text x="45" y="28" font-size="10.5" fill="#5A7F54" font-weight="700" font-family="sans-serif">📊  핵심 건강 지표 요약</text>
            <!-- 3 metric cards -->
            <rect x="40" y="36" width="64" height="42" rx="8" fill="rgba(214,183,117,.2)"/>
            <text x="72" y="52" text-anchor="middle" font-size="16" fill="#2C2A26" font-weight="700" font-family="sans-serif">1.8</text>
            <text x="72" y="62" text-anchor="middle" font-size="8" fill="#9A746C" font-family="sans-serif">L · 수분</text>
            <rect x="40" y="41" width="40" height="3" rx="1.5" fill="#D6B775"/>
            <rect x="118" y="36" width="64" height="42" rx="8" fill="rgba(229,181,176,.3)"/>
            <text x="150" y="52" text-anchor="middle" font-size="16" fill="#2C2A26" font-weight="700" font-family="sans-serif">7.2</text>
            <text x="150" y="62" text-anchor="middle" font-size="8" fill="#CC4848" font-family="sans-serif">거품 관리 필요</text>
            <rect x="118" y="41" width="52" height="3" rx="1.5" fill="#D44"/>
            <rect x="196" y="36" width="64" height="42" rx="8" fill="rgba(157,190,150,.25)"/>
            <text x="228" y="52" text-anchor="middle" font-size="16" fill="#2C2A26" font-weight="700" font-family="sans-serif">3회</text>
            <text x="228" y="62" text-anchor="middle" font-size="8" fill="#5A7F54" font-family="sans-serif">감소 추세 ↓</text>
            <rect x="196" y="41" width="28" height="3" rx="1.5" fill="#5A7F54"/>
            <!-- bar chart -->
            <text x="45" y="94" font-size="9" fill="#2C2A26" font-weight="700" font-family="sans-serif">소변 거품 7일 추이</text>
            <rect x="43" y="100" width="214" height="46" rx="8" fill="rgba(157,190,150,.08)"/>
            <!-- bars with varying heights -->
            <rect x="54"  y="124" width="20" height="16" rx="2" fill="#9DBE96"/>
            <rect x="82"  y="118" width="20" height="22" rx="2" fill="#D6B775"/>
            <rect x="110" y="126" width="20" height="14" rx="2" fill="#9DBE96"/>
            <rect x="138" y="110" width="20" height="30" rx="2" fill="#D44"/>
            <rect x="166" y="114" width="20" height="26" rx="2" fill="#D44"/>
            <rect x="194" y="116" width="20" height="24" rx="2" fill="#D44"/>
            <rect x="222" y="117" width="20" height="23" rx="2" fill="#D44"/>
            <!-- insight -->
            <rect x="40" y="154" width="220" height="16" rx="6" fill="rgba(157,190,150,.15)"/>
            <text x="150" y="165" font-size="8.5" fill="#5A7F54" text-anchor="middle" font-style="italic" font-family="sans-serif">"수분 루틴이 오르면서 흐름이 좋아지고 있어요"</text>
          </svg>
        </div>
        <div class="scene-phase">빛의 순간</div>
        <h3 class="scene-title">숫자 대신,<br>이야기를 받았다</h3>
        <p class="scene-text">"최근 3일의 거품 수준은 첫 주보다 낮아지는 흐름이에요." 처음으로 내 몸이 나에게 말을 걸었다.</p>
        <div class="scene-quote">"의학 용어가 아니라, 나의 언어였다."</div>
      </div>
      <div class="scene-card">
        <div class="scene-num-row"><span class="scene-num">SCENE / 07</span><div class="scene-line"></div><span class="scene-emo">⭐</span></div>
        <div class="scene-illust scene-illust-7">
          <svg viewBox="0 0 300 180" width="260" height="160" xmlns="http://www.w3.org/2000/svg">
            <rect x="50" y="10" width="200" height="162" rx="18" fill="rgba(255,255,255,.97)"/>
            <!-- premium badge -->
            <rect x="106" y="22" width="88" height="18" rx="9" fill="rgba(157,190,150,.25)"/>
            <text x="150" y="34" font-size="9" fill="#5A7F54" text-anchor="middle" font-weight="700" font-family="sans-serif" letter-spacing="2">PREMIUM</text>
            <!-- price big -->
            <text x="150" y="78" font-size="38" fill="#2C2A26" text-anchor="middle" font-weight="700" font-family="Georgia,serif">2,900</text>
            <text x="150" y="94" font-size="10" fill="#7A746C" text-anchor="middle" font-family="sans-serif">원 / 월</text>
            <!-- divider -->
            <line x1="70" y1="104" x2="230" y2="104" stroke="#E4DCD0" stroke-width="1"/>
            <!-- feature list -->
            <text x="76" y="121" font-size="9" fill="#5A7F54" font-family="sans-serif">✓</text>
            <text x="90" y="121" font-size="9" fill="#3D3A35" font-family="sans-serif">광고 제거 + 프리미엄 콘텐츠</text>
            <text x="76" y="136" font-size="9" fill="#5A7F54" font-family="sans-serif">✓</text>
            <text x="90" y="136" font-size="9" fill="#3D3A35" font-family="sans-serif">장·단기 통합 맞춤 리포트</text>
            <!-- CTA button -->
            <rect x="62" y="148" width="176" height="18" rx="9" fill="#5A7F54"/>
            <text x="150" y="160" font-size="9" fill="white" text-anchor="middle" font-weight="700" font-family="sans-serif">계속 기록할게요 →</text>
          </svg>
        </div>
        <div class="scene-phase">약속의 순간</div>
        <h3 class="scene-title">2,900원,<br>나와의 약속이었다</h3>
        <p class="scene-text">기본형 무료에서 확장형으로. 망설임 없이 결제 버튼을 눌렀다. 광고 제거, 프리미엄 콘텐츠.</p>
        <div class="scene-quote">"돈을 낸 게 아니라, 나와의 약속을 한 것 같았다."</div>
      </div>
      <div class="scene-card">
        <div class="scene-num-row"><span class="scene-num">SCENE / 08</span><div class="scene-line"></div><span class="scene-emo">💜</span></div>
        <div class="scene-illust scene-illust-8">
          <svg viewBox="0 0 300 180" width="260" height="160" xmlns="http://www.w3.org/2000/svg">
            <!-- chat bg -->
            <rect x="20" y="8" width="260" height="166" rx="16" fill="rgba(255,255,255,.2)"/>
            <!-- message 1 (left) -->
            <rect x="32" y="20" width="156" height="26" rx="13" fill="white"/>
            <text x="44" y="34" font-size="9.5" fill="#2C2A26" font-family="sans-serif">나 요즘 이 앱 쓰는데... 🌱</text>
            <!-- message 2 (right) -->
            <rect x="114" y="52" width="154" height="26" rx="13" fill="rgba(157,190,150,.75)"/>
            <text x="126" y="66" font-size="9.5" fill="white" font-family="sans-serif">헐 그런 것도 있어? 뭐야?</text>
            <!-- message 3 (left) -->
            <rect x="32" y="84" width="170" height="26" rx="13" fill="white"/>
            <text x="44" y="98" font-size="9.5" fill="#2C2A26" font-family="sans-serif">The Bottom Line! 진짜 간단해</text>
            <!-- message 4 (right) -->
            <rect x="110" y="116" width="158" height="26" rx="13" fill="rgba(157,190,150,.75)"/>
            <text x="122" y="130" font-size="9.5" fill="white" font-family="sans-serif">오늘 바로 다운받아볼래 ✨</text>
            <!-- bottom caption -->
            <rect x="60" y="150" width="180" height="18" rx="9" fill="rgba(255,255,255,.45)"/>
            <text x="150" y="162" text-anchor="middle" font-size="8.5" fill="#2D4329" font-style="italic" font-family="sans-serif">피부 관리하듯, 당연하게.</text>
          </svg>
        </div>
        <div class="scene-phase">확산의 순간</div>
        <h3 class="scene-title">피부 관리 이야기처럼,<br>당연하게</h3>
        <p class="scene-text">6개월 뒤. 회사 점심에서 자연스럽게 말했다. "나 요즘 이 앱 쓰는데, 진짜 간단해."</p>
        <div class="scene-quote">"부끄러운 이야기가 당연한 자기 관리가 됐다."</div>
      </div>
    </div>

    <div class="journey-controls" style="padding:0 56px 0 56px;">
      <div class="journey-progress-bar">
        <div class="journey-progress-fill" id="journeyProgress"></div>
      </div>
      <button class="journey-arrow" id="journeyPrev" disabled>←</button>
      <button class="journey-arrow" id="journeyNext">→</button>
    </div>
  </div>
</section>

<!-- ═══════════════ FLOW ═══════════════ -->
<section class="section flow-section">
  <div class="section-inner">
    <div class="section-eyebrow reveal">서비스 흐름 · INPUT → CORE → OUTPUT</div>
    <h2 class="section-title reveal">
      기록부터 가치 전달까지,<br>
      <span class="section-title-italic">한 흐름.</span>
    </h2>
    <p class="section-desc reveal">
      병원 가기 전 단계의 예방형 웰니스 서비스. 사용자의 입력이 어떻게 가치로 전환되는지를 보여드립니다.
    </p>

    <div class="flow-track">
      <div class="flow-step reveal">
        <div class="flow-num">01</div>
        <div class="flow-label">INPUT</div>
        <h3 class="flow-title">사용자 입력</h3>
        <ul class="flow-list">
          <li>거품뇨 · 배변 상태</li>
          <li>수분 · 식단 섭취</li>
          <li>수면 · 스트레스 · 활동량</li>
        </ul>
      </div>
      <div class="flow-arrow reveal">→</div>
      <div class="flow-step center reveal">
        <div class="flow-num">02</div>
        <div class="flow-label">CORE</div>
        <h3 class="flow-title">맞춤형 생활기록</h3>
        <ul class="flow-list">
          <li>나노 타임라인 루틴 미션</li>
          <li>데일리 거품뇨·배변상태 기록</li>
          <li>게이미피케이션 (나의 숲)</li>
        </ul>
      </div>
      <div class="flow-arrow reveal">→</div>
      <div class="flow-step reveal">
        <div class="flow-num">03</div>
        <div class="flow-label">OUTPUT</div>
        <h3 class="flow-title">AI 기반 가치 전달</h3>
        <ul class="flow-list">
          <li>AI 거품 분석 · 추이</li>
          <li>주간·월간 웰니스 리포트</li>
          <li>맞춤 큐레이션 · 추천</li>
          <li>예방 콘텐츠 · 자가 체크</li>
          <li>B2B 센터 연계 프로그램</li>
        </ul>
      </div>
    </div>

    <div class="flow-quote reveal">
      <p>
        피부 관리하듯, <em>하부 건강도 매일 가볍게.</em><br>
        보이지 않는 곳까지, 당신의 건강을 끌어올리다.
      </p>
    </div>
  </div>
</section>

<!-- ═══════════════ FOREST ═══════════════ -->
<section class="section forest-section" id="service">
  <div class="section-inner">
    <div class="section-eyebrow reveal">나의 숲 · 게이미피케이션</div>
    <h2 class="forest-headline reveal">
      오늘의 <span class="marker">3초</span>가,<br>
      <em>한 그루의 나무</em>가 됩니다.
    </h2>
    <p class="section-desc reveal">
      루틴 종류별로 다른 식물이 자라며, 달성률에 따라 숲 전체의 상태가 달라집니다.
      <strong style="color:var(--ink);font-weight:500;">씨앗에서 거목까지.</strong>
    </p>

    <!-- 7-stage timeline -->
    <div class="forest-stages reveal">
      <div class="stage">
        <div class="stage-icon-wrap" data-count="0회">🟫</div>
        <div class="stage-name">씨앗</div>
        <div class="stage-en">Seed</div>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="3회">🌱</div>
        <div class="stage-name">새순</div>
        <div class="stage-en">Sprout</div>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="6회">🌿</div>
        <div class="stage-name">새잎</div>
        <div class="stage-en">Leaf</div>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="9회">🪴</div>
        <div class="stage-name">묘목</div>
        <div class="stage-en">Sapling</div>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="12회">🌷</div>
        <div class="stage-name">꽃봉오리</div>
        <div class="stage-en">Bud</div>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="18회">🌸</div>
        <div class="stage-name">만개</div>
        <div class="stage-en">Bloom</div>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="30회">🌳</div>
        <div class="stage-name">거목</div>
        <div class="stage-en">Forest</div>
      </div>
    </div>

    <h3 class="trees-section-title reveal">
      세 그루의 나무, <strong>세 가지 케어.</strong>
    </h3>
    <p class="trees-section-desc reveal">
      각 식물은 고유한 성장 과정과 루틴을 가집니다. 본인의 관심 케어를 선택해 자신만의 숲을 만들어보세요.
    </p>

    <!-- 3 trees with their unique routines -->
    <div class="trees-trio">
      <!-- 소나무 — 단백뇨 관리 (uploaded image 6.png) -->
      <div class="tree-card pine reveal">
        <span class="tree-icon-big">🪵</span>
        <h3>소나무</h3>
        <div class="tree-purpose">단백뇨 관리 · Renal</div>

        <div class="tree-routines">
          <div class="tree-routine">
            <div class="tree-routine-icon">💧</div>
            <div class="tree-routine-info">
              <div class="tree-routine-time">아침 루틴</div>
              <div class="tree-routine-name">물 2컵 마시기</div>
              <div class="tree-routine-desc">신장 세척 · 400ml 권장</div>
            </div>
          </div>
          <div class="tree-routine">
            <div class="tree-routine-icon">🥗</div>
            <div class="tree-routine-info">
              <div class="tree-routine-time">점심 루틴</div>
              <div class="tree-routine-name">저염 식단 체크</div>
              <div class="tree-routine-desc">나트륨 제한 · 단백뇨 예방</div>
            </div>
          </div>
          <div class="tree-routine">
            <div class="tree-routine-icon">📊</div>
            <div class="tree-routine-info">
              <div class="tree-routine-time">저녁 루틴</div>
              <div class="tree-routine-name">단백뇨 수치 기록</div>
              <div class="tree-routine-desc">소변 검사 스트립 확인</div>
            </div>
          </div>
        </div>

        <div class="tree-progress-row">
          <div class="tree-progress-bar"><div class="tree-progress-fill"></div></div>
          <span class="tree-progress-text">새순 · 6/9회</span>
        </div>
      </div>

      <!-- 대나무 — 치질 예방 (uploaded image 5.png) -->
      <div class="tree-card bamboo reveal">
        <span class="tree-icon-big">🫘</span>
        <h3>대나무</h3>
        <div class="tree-purpose">치질 예방 · Anal Care</div>

        <div class="tree-routines">
          <div class="tree-routine">
            <div class="tree-routine-icon">🚶</div>
            <div class="tree-routine-info">
              <div class="tree-routine-time">아침 루틴</div>
              <div class="tree-routine-name">기상 후 스트레칭</div>
              <div class="tree-routine-desc">항문 혈류 개선 5분</div>
            </div>
          </div>
          <div class="tree-routine">
            <div class="tree-routine-icon">🌿</div>
            <div class="tree-routine-info">
              <div class="tree-routine-time">점심 루틴</div>
              <div class="tree-routine-name">식이섬유 섭취</div>
              <div class="tree-routine-desc">채소·과일 목표량 절반</div>
            </div>
          </div>
          <div class="tree-routine">
            <div class="tree-routine-icon">🪑</div>
            <div class="tree-routine-info">
              <div class="tree-routine-time">저녁 루틴</div>
              <div class="tree-routine-name">좌욕 5분</div>
              <div class="tree-routine-desc">하부 케어 루틴 유지</div>
            </div>
          </div>
        </div>

        <div class="tree-progress-row">
          <div class="tree-progress-bar"><div class="tree-progress-fill"></div></div>
          <span class="tree-progress-text">씨앗 · 2/3회</span>
        </div>
      </div>

      <!-- 벚꽃나무 — 식이 관리 (uploaded image 4.png) -->
      <div class="tree-card cherry reveal">
        <span class="tree-icon-big">🌸</span>
        <h3>벚꽃나무</h3>
        <div class="tree-purpose">식이 관리 · Nutrition</div>

        <div class="tree-routines">
          <div class="tree-routine">
            <div class="tree-routine-icon">🫘</div>
            <div class="tree-routine-info">
              <div class="tree-routine-time">아침 루틴</div>
              <div class="tree-routine-name">소이조이 또는 두유 섭취</div>
              <div class="tree-routine-desc">식물성 단백질 · 장 건강</div>
            </div>
          </div>
          <div class="tree-routine">
            <div class="tree-routine-icon">💧</div>
            <div class="tree-routine-info">
              <div class="tree-routine-time">점심 루틴</div>
              <div class="tree-routine-name">수분 목표 절반</div>
              <div class="tree-routine-desc">1L 이상 · 신장 부담 완화</div>
            </div>
          </div>
          <div class="tree-routine">
            <div class="tree-routine-icon">🥬</div>
            <div class="tree-routine-info">
              <div class="tree-routine-time">저녁 루틴</div>
              <div class="tree-routine-name">채소 위주 저녁 식단</div>
              <div class="tree-routine-desc">가공식품 줄이기 · 하부 건강</div>
            </div>
          </div>
        </div>

        <div class="tree-progress-row">
          <div class="tree-progress-bar"><div class="tree-progress-fill"></div></div>
          <span class="tree-progress-text">새잎 · 6/9회</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ EXPERT COLUMN — NEW ═══════════════ -->
<section class="section column-section" id="column">
  <div class="section-inner">
    <div class="column-grid">
      <div class="column-left">
        <div class="section-eyebrow reveal">전문가 칼럼 · 근거 있는 가이드</div>
        <h2 class="column-headline reveal">
          학회 지침을<br>
          <em>일상의 언어</em>로<br>
          전합니다.
        </h2>
        <p class="column-desc reveal">
          신장·항문·식이 분야 전문 학회와 영양사의 공인된 콘텐츠를 큐레이션해
          매주 새로운 칼럼을 제공합니다. 정보를 가공하지 않고, 근거를 명확히 합니다.
        </p>
        <div class="column-credibility reveal">
          <div class="column-credibility-label">CREDIBILITY · 근거</div>
          <div class="column-credibility-text">
            대한신장학회 · 대한대장항문학회 · 영양사 협회 등 공인 기관의 공식 가이드라인 기반
          </div>
        </div>
      </div>

      <div class="column-right">
        <div class="column-list">
          <article class="article-card kidney reveal">
            <div class="article-icon-wrap">📋</div>
            <div class="article-content">
              <span class="article-tag">신장 · Kidney</span>
              <h3 class="article-title">단백뇨 경계 수치, 이렇게 관리하세요</h3>
              <p class="article-meta"><span>대한신장학회</span> · 2025.04.10 · 5분 읽기</p>
            </div>
            <div class="article-arrow">→</div>
          </article>

          <article class="article-card anal reveal">
            <div class="article-icon-wrap">🩺</div>
            <div class="article-content">
              <span class="article-tag">항문 · Anal Care</span>
              <h3 class="article-title">치질 예방에 좌욕이 효과 있는 이유</h3>
              <p class="article-meta"><span>항문외과 전문의</span> · 2025.04.08 · 4분 읽기</p>
            </div>
            <div class="article-arrow">→</div>
          </article>

          <article class="article-card diet reveal">
            <div class="article-icon-wrap">🌸</div>
            <div class="article-content">
              <span class="article-tag">식이 · Nutrition</span>
              <h3 class="article-title">식물성 단백질로 하부 건강 지키는 법</h3>
              <p class="article-meta"><span>영양사 칼럼</span> · 2025.04.05 · 6분 읽기</p>
            </div>
            <div class="article-arrow">→</div>
          </article>

          <article class="article-card kidney reveal">
            <div class="article-icon-wrap">💧</div>
            <div class="article-content">
              <span class="article-tag">신장 · Kidney</span>
              <h3 class="article-title">아침 첫 컵, 신장 세척이 시작됩니다</h3>
              <p class="article-meta"><span>대한신장학회</span> · 2025.04.02 · 3분 읽기</p>
            </div>
            <div class="article-arrow">→</div>
          </article>

          <article class="article-card diet reveal">
            <div class="article-icon-wrap">🥗</div>
            <div class="article-content">
              <span class="article-tag">식이 · Nutrition</span>
              <h3 class="article-title">고단백 다이어트, 신장에 미치는 영향</h3>
              <p class="article-meta"><span>임상영양학회</span> · 2025.03.28 · 7분 읽기</p>
            </div>
            <div class="article-arrow">→</div>
          </article>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ APP TABS — 5 ═══════════════ -->
<section class="section tabs-section">
  <div class="section-inner">
    <div class="section-eyebrow reveal">앱 구성 · 5개 탭</div>
    <h2 class="section-title reveal">
      한 흐름에<br>
      <span class="section-title-italic">모든 케어.</span>
    </h2>
    <p class="section-desc reveal">
      홈에서 시작해 마이까지 — 기록·분석·쇼핑·관리가 하나의 일상 흐름으로 이어집니다.
    </p>

    <div class="tabs-grid">
      <div class="tab-card reveal">
        <div class="tab-num">TAB / 01</div>
        <span class="tab-emoji">🏠</span>
        <h3 class="tab-name">홈</h3>
        <div class="tab-role">관리</div>
        <ul class="tab-features">
          <li>식물 성장 트래커 (나의 숲)</li>
          <li>원터치 나노 루틴 관리</li>
          <li>전문 칼럼 공유</li>
        </ul>
      </div>
      <div class="tab-card reveal">
        <div class="tab-num">TAB / 02</div>
        <span class="tab-emoji">📊</span>
        <h3 class="tab-name">단백뇨 관리</h3>
        <div class="tab-role">기록</div>
        <ul class="tab-features">
          <li>소변 거품 밀도 변화 촬영</li>
          <li>Before & After 비교</li>
          <li>10초 영상 AI 분석</li>
        </ul>
      </div>
      <div class="tab-card reveal">
        <div class="tab-num">TAB / 03</div>
        <span class="tab-emoji">🚦</span>
        <h3 class="tab-name">항문 체크</h3>
        <div class="tab-role">기록</div>
        <ul class="tab-features">
          <li>신호등 상태 체크</li>
          <li>브리스톨 7단계 활용</li>
          <li>일일 컨디션 트래킹</li>
        </ul>
      </div>
      <div class="tab-card reveal">
        <div class="tab-num">TAB / 04</div>
        <span class="tab-emoji">🛍️</span>
        <h3 class="tab-name">스토어</h3>
        <div class="tab-role">쇼핑</div>
        <ul class="tab-features">
          <li>포인트 교환소</li>
          <li>맞춤 큐레이션 추천</li>
          <li>식물성 단백질 간식</li>
        </ul>
      </div>
      <div class="tab-card reveal">
        <div class="tab-num">TAB / 05</div>
        <span class="tab-emoji">👤</span>
        <h3 class="tab-name">마이</h3>
        <div class="tab-role">설정</div>
        <ul class="tab-features">
          <li>맞춤형 PDF 리포트</li>
          <li>알림·프라이버시 설정</li>
          <li>개인 건강 프로필</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ SOLUTIONS ═══════════════ -->
<section class="section solutions-section">
  <div class="section-inner">
    <div class="solutions-grid">
      <div class="solutions-left">
        <div class="section-eyebrow reveal">서비스 특장점</div>
        <h2 class="solutions-tagline reveal">
          데이터 가시화와<br>
          습관 형성을 돕는<br>
          <strong><span class="num">5</span>대 케어 솔루션.</strong>
        </h2>

        <div class="solution-list">
          <div class="solution-item reveal">
            <span class="solution-num">i.</span>
            <div class="solution-content">
              <h3 class="solution-name">나노 타임라인 루틴</h3>
              <p class="solution-desc">아침/점심/저녁 시간대별 맞춤 미션. 실천 가능한 소행동 중심의 게이미피케이션.</p>
            </div>
            <div class="solution-arrow">→</div>
          </div>
          <div class="solution-item reveal">
            <span class="solution-num">ii.</span>
            <div class="solution-content">
              <h3 class="solution-name">3초 원터치 기록</h3>
              <p class="solution-desc">아이콘 터치만으로 현재 상태 즉시 기록. 기록의 심리적 비용을 최소화.</p>
            </div>
            <div class="solution-arrow">→</div>
          </div>
          <div class="solution-item reveal">
            <span class="solution-num">iii.</span>
            <div class="solution-content">
              <h3 class="solution-name">AI 이미지 분석</h3>
              <p class="solution-desc">소변 거품 촬영 시 AI가 거품 밀도를 분석. 시각적 효과를 통한 자가 관리 방향 제시.</p>
            </div>
            <div class="solution-arrow">→</div>
          </div>
          <div class="solution-item reveal">
            <span class="solution-num">iv.</span>
            <div class="solution-content">
              <h3 class="solution-name">개인 맞춤형 PDF 리포트</h3>
              <p class="solution-desc">축적 데이터를 바탕으로 개인 맞춤형 리포트 자동 생성.</p>
            </div>
            <div class="solution-arrow">→</div>
          </div>
          <div class="solution-item reveal">
            <span class="solution-num">v.</span>
            <div class="solution-content">
              <h3 class="solution-name">공인 지침 교육 콘텐츠</h3>
              <p class="solution-desc">대한신장학회·대한대장항문학회 지침 기반의 신뢰도 높은 근거 기반 가이드.</p>
            </div>
            <div class="solution-arrow">→</div>
          </div>
        </div>
      </div>

      <div class="showcase-right">
        <div class="showcase-deco showcase-deco-1">
          <div class="deco-icon" style="background:linear-gradient(135deg,#FBE0EE,#F2C8DD);">🌸</div>
          <div class="deco-text">
            <strong>벚꽃나무 +1</strong>
            <span>새잎 → 꽃봉오리</span>
          </div>
        </div>
        <div class="showcase-deco showcase-deco-2">
          <div class="deco-icon" style="background:linear-gradient(135deg,#FFE5D6,#F2C0BB);">📋</div>
          <div class="deco-text">
            <strong>맞춤 리포트</strong>
            <span>축적 데이터 자동 생성</span>
          </div>
        </div>

        <div class="showcase-phone">
          <div class="showcase-screen">
            <div class="showcase-notch"></div>
            <div class="showcase-content">
              <!-- 벚꽃나무 active — matches uploaded image 4.png -->
              <div class="showcase-tabs">
                <div class="showcase-tab active">
                  <div class="showcase-tab-icon">🌸</div>
                  <div class="showcase-tab-name">벚꽃나무</div>
                </div>
                <div class="showcase-tab">
                  <div class="showcase-tab-icon">🪵</div>
                  <div class="showcase-tab-name">소나무</div>
                </div>
                <div class="showcase-tab">
                  <div class="showcase-tab-icon">🫘</div>
                  <div class="showcase-tab-name">대나무</div>
                </div>
              </div>

              <div class="showcase-h">오늘의 나노 루틴</div>
              <div class="showcase-routine">
                <div class="showcase-routine-icon">🫘</div>
                <div class="showcase-routine-info">
                  <div class="showcase-routine-time">아침 루틴</div>
                  <div class="showcase-routine-name">소이조이 또는 두유 섭취</div>
                  <div class="showcase-routine-desc">식물성 단백질 · 장 건강</div>
                </div>
                <div class="showcase-routine-check">✓</div>
              </div>
              <div class="showcase-routine">
                <div class="showcase-routine-icon">💧</div>
                <div class="showcase-routine-info">
                  <div class="showcase-routine-time">점심 루틴</div>
                  <div class="showcase-routine-name">수분 목표 절반</div>
                  <div class="showcase-routine-desc">1L 이상 · 신장 부담 완화</div>
                </div>
                <div class="showcase-routine-check">✓</div>
              </div>
              <div class="showcase-routine">
                <div class="showcase-routine-icon">🥬</div>
                <div class="showcase-routine-info">
                  <div class="showcase-routine-time">저녁 루틴</div>
                  <div class="showcase-routine-name">채소 위주 저녁 식단</div>
                  <div class="showcase-routine-desc">가공식품 줄이기 · 하부 건강</div>
                </div>
                <div class="showcase-routine-check">✓</div>
              </div>

              <div class="showcase-h" style="margin-top:14px;">📋 전문가 칼럼</div>
              <div style="background:rgba(199,123,115,.08);border-radius:10px;padding:9px 11px;margin-bottom:5px;display:flex;align-items:center;gap:9px;">
                <div style="width:24px;height:24px;border-radius:6px;background:linear-gradient(135deg,#E0EFDE,#C5DBC0);display:flex;align-items:center;justify-content:center;font-size:11px;flex-shrink:0;">📋</div>
                <div style="flex:1;">
                  <div style="font-size:8.5px;font-weight:700;color:var(--ink);line-height:1.2;">단백뇨 경계 수치, 이렇게 관리하세요</div>
                  <div style="font-size:7px;color:var(--stone);">대한신장학회 · 04.10</div>
                </div>
              </div>
              <div style="background:rgba(199,123,115,.08);border-radius:10px;padding:9px 11px;display:flex;align-items:center;gap:9px;">
                <div style="width:24px;height:24px;border-radius:6px;background:linear-gradient(135deg,#FCE5E2,#F2C0BB);display:flex;align-items:center;justify-content:center;font-size:11px;flex-shrink:0;">🌸</div>
                <div style="flex:1;">
                  <div style="font-size:8.5px;font-weight:700;color:var(--ink);line-height:1.2;">식물성 단백질로 하부 건강 지키는 법</div>
                  <div style="font-size:7px;color:var(--stone);">영양사 칼럼 · 04.05</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ AI TECH ═══════════════ -->
<section class="section tech-section" id="tech">
  <div class="section-inner">
    <div class="section-eyebrow reveal">기술 차별점 · AI Foam Analysis</div>
    <h2 class="section-title reveal">
      논문 기반의<br>
      <span class="section-title-italic">거품 분석 AI.</span>
    </h2>
    <p class="section-desc reveal">
      소변 거품은 질병 판단 근거가 아닌 <strong style="color:var(--terra-soft);font-weight:500;">개인 기준선 대비 변화 추이</strong>를 비교하는 기록 기능.
      국제 논문 기반의 컴퓨터 비전 기술로 신뢰도를 확보합니다.
    </p>

    <div class="tech-grid">
      <div class="tech-card reveal">
        <div class="tech-icon">🎥</div>
        <div class="tech-num">TECH / 01</div>
        <h3 class="tech-name">10초 영상 촬영 권장</h3>
        <p class="tech-desc">
          정확한 단백뇨 측정을 위해 10초 이상의 소변 영상 촬영을 권장합니다.
          영상 분석 시 거품 밀도 측정 정확도가 유의미하게 향상됩니다.
        </p>
        <div class="tech-paper">
          <div class="tech-paper-label">논문 근거</div>
          <div class="tech-paper-cite">Jahedsaravani et al. (2023) — CNN 기반 거품 size·velocity 측정</div>
        </div>
      </div>
      <div class="tech-card reveal">
        <div class="tech-icon">📅</div>
        <div class="tech-num">TECH / 02</div>
        <h3 class="tech-name">하루 2회 권장 빈도</h3>
        <p class="tech-desc">
          아침·저녁 2회 촬영이 권장됩니다. 반복 측정 데이터의 추이 예측 가능성이
          ANN 기반 연구로 입증되었습니다.
        </p>
        <div class="tech-paper">
          <div class="tech-paper-label">논문 근거</div>
          <div class="tech-paper-cite">Morelle et al. (2021) — ANN 기반 거품 변화 예측</div>
        </div>
      </div>
      <div class="tech-card reveal">
        <div class="tech-icon">🤖</div>
        <div class="tech-num">TECH / 03</div>
        <h3 class="tech-name">자동 검출·정량화</h3>
        <p class="tech-desc">
          타임스탬프로 날짜·시간 자동 저장. U-Net과 Mask R-CNN으로
          거품 검출·정량화·개별 분할까지 자동화.
        </p>
        <div class="tech-paper">
          <div class="tech-paper-label">논문 근거</div>
          <div class="tech-paper-cite">Hoseini (U-Net) · Cui (Mask R-CNN) — 거품 검출·shape reconstruction</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ PRICING — Final PPT pricing ═══════════════ -->
<section class="section pricing-section" id="pricing">
  <div class="section-inner">
    <div class="section-eyebrow reveal">비즈니스 모델 · 요금제</div>
    <h2 class="section-title reveal">
      <span class="section-title-italic">단계적</span> 도입,<br>
      가벼운 시작.
    </h2>
    <p class="section-desc reveal">
      B2C와 B2B를 이원화한 모델. 기본형으로 가볍게 시작하고, 확장형으로 더 깊은 가치로.
    </p>

    <div class="pricing-grid">
      <!-- B2C -->
      <div class="price-card reveal">
        <span class="price-tag">B2C · 개인 사용자</span>
        <p class="price-target">20~40대 직장인 · 다이어터 · MZ세대</p>
        <h3 class="price-name"><em>Premium</em><br>구독</h3>
        <div class="price-tier">
          <span class="price-tier-label">기본형</span>
          <span class="price-tier-amount">무료<small> · 광고</small></span>
        </div>
        <div class="price-tier">
          <span class="price-tier-label">확장형</span>
          <span class="price-tier-amount">₩2,900<small>/월</small></span>
        </div>
        <ul class="price-features">
          <li>AI 거품 분석 · 단기 맞춤 리포트</li>
          <li>광고 제거 + 프리미엄 콘텐츠</li>
          <li>포인트 추가 적립</li>
          <li>장·단기 통합 맞춤 리포트</li>
        </ul>
      </div>

      <!-- B2B 센터 (FEATURED) -->
      <div class="price-card featured reveal">
        <span class="price-tag">B2B · 웰니스 센터</span>
        <p class="price-target">피트니스 · 필라테스 · 요가 센터</p>
        <h3 class="price-name"><em>Wellness</em><br>라이선스</h3>
        <div class="price-tier">
          <span class="price-tier-label">기본형</span>
          <span class="price-tier-amount">₩12.9<small>만/월</small></span>
        </div>
        <div class="price-tier">
          <span class="price-tier-label">확장형</span>
          <span class="price-tier-amount">₩19.9<small>만/월</small></span>
        </div>
        <ul class="price-features">
          <li>QR 유입 · 체험 쿠폰 제공</li>
          <li>PT 회원 대상 부가 서비스</li>
          <li>주기적 챌린지 + 스토어 입점 상품</li>
          <li>전체 회원 + 공식 파트너십 권한</li>
        </ul>
      </div>

      <!-- B2B 기업 -->
      <div class="price-card reveal">
        <span class="price-tag">B2B · 기업 HR · 후속</span>
        <p class="price-target">좌식근무 직군 비중이 큰 조직</p>
        <h3 class="price-name"><em>HR</em> 프로그램</h3>
        <div class="price-tier">
          <span class="price-tier-label">기본형</span>
          <span class="price-tier-amount">₩1,500<small>/인·월</small></span>
        </div>
        <div class="price-tier">
          <span class="price-tier-label">확장형</span>
          <span class="price-tier-amount">₩1,900<small>/인·월</small></span>
        </div>
        <ul class="price-features">
          <li>성별·연령별 건강상태 리포트</li>
          <li>이너뷰티 스토어 입점권 제공</li>
          <li>맞춤형 인식 개선 캠페인</li>
          <li>기업별 나노 루틴 미션 개설</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ ROADMAP ═══════════════ -->
<section class="section roadmap-section">
  <div class="section-inner">
    <div class="section-eyebrow reveal">향후 로드맵</div>
    <h2 class="section-title reveal">
      MVP에서 IoT 생태계까지,<br>
      <span class="section-title-italic">3단계 성장 전략.</span>
    </h2>
    <p class="section-desc reveal">
      하부 건강 관리의 표준을 향한 단계적 확장 — 출시부터 글로벌까지.
    </p>

    <div class="roadmap-track">
      <div class="phase reveal">
        <div class="phase-dot"></div>
        <div class="phase-tag">PHASE 01 · MVP 출시</div>
        <div class="phase-title">Launch</div>
        <div class="phase-period">~ 12 개월</div>
        <ul class="phase-features">
          <li>나노 타임라인 루틴 + 원터치 기록</li>
          <li>iOS / Android 동시 론칭</li>
          <li>초기 사용자 UX 피드백 수집</li>
          <li>AI 소변 이미지 분석 도입</li>
          <li>맞춤형 PDF 리포트 생성</li>
          <li>웰니스 센터 · 이너뷰티 상품 판매사 제휴</li>
        </ul>
      </div>
      <div class="phase reveal">
        <div class="phase-dot"></div>
        <div class="phase-tag">PHASE 02 · 기능 고도화</div>
        <div class="phase-title">Scale</div>
        <div class="phase-period">12 ~ 24 개월</div>
        <ul class="phase-features">
          <li>나노 타임라인 루틴 목록 다양화</li>
          <li>일정 앱과의 자동 연동 기능 개발</li>
          <li>ISO 27001/27701 인증 취득</li>
          <li>데이터 기반 스토어 큐레이션 서비스</li>
        </ul>
      </div>
      <div class="phase reveal">
        <div class="phase-dot"></div>
        <div class="phase-tag">PHASE 03 · 생태계 확장</div>
        <div class="phase-title">Expand</div>
        <div class="phase-period">24 개월 ~</div>
        <ul class="phase-features">
          <li>의료서비스 연계 검토</li>
          <li>자동 측정 IoT 시스템과 연계</li>
          <li>글로벌 시장 진출 검토</li>
          <li>비식별 데이터 기반 공동연구</li>
        </ul>
      </div>
    </div>

    <div class="roadmap-closing reveal">
      <div class="roadmap-closing-mark">🌱 → 🌳</div>
      <p class="roadmap-closing-text">
        한 그루의 나무가 자라듯,<br>
        <em>씨앗에서 숲까지.</em>
      </p>
      <p class="roadmap-closing-sub">
        개인의 작은 기록이 쌓여 사회 전체의 예방 문화로
      </p>
    </div>
  </div>
</section>

<!-- ═══════════════ IMPACT ═══════════════ -->
<section class="section impact-section">
  <div class="section-inner">
    <div class="section-eyebrow reveal">기대 효과</div>
    <h2 class="section-title reveal">
      개인의 <span class="section-title-italic">건강 리터러시</span>에서<br>
      예방 중심 문화 확산까지.
    </h2>
    <p class="section-desc reveal">
      The Bottom Line이 만드는 변화는 한 사람의 자기 관리에서 시작해 사회의 예방 문화로 확장됩니다.
    </p>

    <div class="impact-tracks">
      <div class="impact-track reveal">
        <div class="impact-track-header">
          <span class="impact-track-tag short">🌱 SHORT-TERM · 단기적 가치</span>
          <h3 class="impact-track-title">개인의 변화에서 시작합니다.</h3>
        </div>
        <div class="impact-grid">
          <div class="impact-card">
            <div class="impact-num">01.</div>
            <h4>건강 리터러시 향상</h4>
            <p>스스로 몸의 신호를 읽고 해석하는 능력을 키웁니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">02.</div>
            <h4>민감 질환 낙인 효과 완화</h4>
            <p>부끄러운 질환이라는 사회적 인식을 해체합니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">03.</div>
            <h4>다이어트 부작용 예방</h4>
            <p>고단백 식단·수분 부족으로 인한 위험을 사전에 차단합니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">04.</div>
            <h4>프라이버시 보호 복지</h4>
            <p>개인정보를 노출하지 않는 안전한 자기관리 환경을 제공합니다.</p>
          </div>
        </div>
      </div>

      <div class="impact-track reveal">
        <div class="impact-track-header">
          <span class="impact-track-tag long">🌳 LONG-TERM · 장기적 가치</span>
          <h3 class="impact-track-title">사회의 예방 문화로 확산됩니다.</h3>
        </div>
        <div class="impact-grid">
          <div class="impact-card">
            <div class="impact-num">05.</div>
            <h4>예방 중심 문화 확산</h4>
            <p>치료에서 예방으로, 한국 헬스케어의 패러다임 전환에 기여합니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">06.</div>
            <h4>건강 정보 격차 완화</h4>
            <p>학회 지침을 일상언어로 변환해 누구나 접근 가능하게 합니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">07.</div>
            <h4>건강 형평성 기여</h4>
            <p>지리·경제적 의료 접근성 차이를 디지털로 보완합니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">08.</div>
            <h4>지속 가능한 행동 변화</h4>
            <p>일회성 캠페인이 아닌, 매일 3초로 이어지는 라이프스타일을 만듭니다.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ MANIFESTO ═══════════════ -->
<section class="manifesto-section">
  <div class="manifesto-inner">
    <div class="manifesto-mark reveal">"</div>
    <p class="manifesto-text reveal">
      방치되던 위험군을 위한<br>
      데이터 기반의 <span class="highlight"><em>확신.</em></span><br>
      The Bottom Line이 함께합니다.
    </p>

    <div class="manifesto-pillars">
      <div class="pillar reveal">
        <div class="pillar-en">Evidence-based</div>
        <div class="pillar-kr">질병관리청 및 학회 지침 기반의<br>공신력 있는 예방 가이드</div>
      </div>
      <div class="pillar reveal">
        <div class="pillar-en">Data-driven</div>
        <div class="pillar-kr">AI 분석과 시각화 리포트로<br>증명하는 관리의 효과</div>
      </div>
      <div class="pillar reveal">
        <div class="pillar-en">Inner Beauty</div>
        <div class="pillar-kr">부끄러운 질환에서 당당한<br>자기 관리 문화로의 전환</div>
      </div>
    </div>

    <div class="manifesto-author reveal">— TEAM Bottoms Up</div>
  </div>
</section>

<!-- ═══════════════ CTA ═══════════════ -->
<section class="cta-section" id="cta">
  <div class="cta-inner">
    <div class="cta-eyebrow reveal">DOWNLOAD · 지금 시작하기</div>
    <h2 class="cta-title reveal">
      당신의 <span class="cta-title-italic">3초</span>가<br>
      <span class="cta-title-italic">한 그루의 나무</span>가 됩니다.
    </h2>
    <p class="cta-desc reveal">
      이지은처럼, 작은 기록이 큰 이해가 되는 여정.<br>
      나만의 숲을 함께 키워보세요.
    </p>
    <div class="cta-buttons reveal">
      <a href="#" class="btn-cta-primary">
        앱 다운로드
        <span class="btn-arrow" style="background:var(--cream);color:var(--ink);">→</span>
      </a>
      <a href="#" class="btn-cta-secondary">
        센터 파트너십 문의
      </a>
    </div>
  </div>
</section>

<!-- ═══════════════ FOOTER ═══════════════ -->
<footer>
  <div class="footer-inner">
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="footer-logo">The <em>Bottom</em> Line</div>
        <p class="footer-tagline">
          하부 이너뷰티 예방 웰니스 서비스.<br>
          무리한 다이어트와 좌식 생활로 하부 건강 부담이 늘어가는 현대인을 위한 예방형 생활습관 관리.
        </p>
      </div>
      <div class="footer-col">
        <div class="footer-col-title">서비스</div>
        <ul>
          <li><a href="#service">앱 다운로드</a></li>
          <li><a href="#pricing">프리미엄</a></li>
          <li><a href="#service">웰니스 리포트</a></li>
          <li><a href="#pricing">파트너 센터</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <div class="footer-col-title">알아보기</div>
        <ul>
          <li><a href="#problem">문제 인식</a></li>
          <li><a href="#journey">고객 여정</a></li>
          <li><a href="#column">전문가 칼럼</a></li>
          <li><a href="#tech">기술 차별점</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <div class="footer-col-title">팀</div>
        <ul>
          <li><a href="#">TEAM Bottoms Up</a></li>
          <li><a href="#">파트너 문의</a></li>
          <li><a href="#">언론 문의</a></li>
          <li><a href="#">개인정보처리방침</a></li>
        </ul>
      </div>
    </div>

    <div class="footer-disclaimer">
      본 서비스는 의료기기가 아니며, 질병의 진단·치료를 목적으로 하지 않습니다.
      웰니스 리포트는 생활기록 기반 코칭 자료이며, 의료적 판단이 필요한 경우 의료기관 상담을 권장합니다.
    </div>

    <div class="footer-bottom">
      <div>© 2026 TEAM Bottoms Up · 오성경 · 유현지 · 정예진 · 허윤지</div>
      <div>Made with care for your inner beauty.</div>
    </div>
  </div>
</footer>

<script>
const nav = document.getElementById('nav');
window.addEventListener('scroll', () => {
  if (window.scrollY > 60) nav.classList.add('scrolled');
  else nav.classList.remove('scrolled');
});

const io = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) e.target.classList.add('in');
  });
}, { threshold: 0.12 });

document.querySelectorAll('.reveal').forEach((el, i) => {
  el.style.transitionDelay = (i % 4) * 0.08 + 's';
  io.observe(el);
});

// Journey horizontal scroll
const scenes = document.getElementById('journeyScenes');
const prevBtn = document.getElementById('journeyPrev');
const nextBtn = document.getElementById('journeyNext');
const progressFill = document.getElementById('journeyProgress');

function updateJourneyState() {
  const sl = scenes.scrollLeft;
  const max = scenes.scrollWidth - scenes.clientWidth;
  const ratio = max > 0 ? sl / max : 0;
  const pct = (1 + ratio * 7) / 8 * 100;
  progressFill.style.width = pct + '%';
  prevBtn.disabled = sl <= 5;
  nextBtn.disabled = sl >= max - 5;
}
scenes.addEventListener('scroll', updateJourneyState);
window.addEventListener('resize', updateJourneyState);
prevBtn.addEventListener('click', () => scenes.scrollBy({ left: -364, behavior: 'smooth' }));
nextBtn.addEventListener('click', () => scenes.scrollBy({ left: 364, behavior: 'smooth' }));
setTimeout(updateJourneyState, 100);

// Stats counter
document.querySelectorAll('.stat-num').forEach(el => {
  const text = el.innerHTML;
  if (!/\d/.test(text)) return;
  el.dataset.text = text;
});

const statIo = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting && !e.target.dataset.animated && e.target.dataset.text) {
      e.target.dataset.animated = 'true';
      const text = e.target.dataset.text;
      const m = text.match(/^([\d,]+)(.*)$/);
      if (!m) return;
      const target = parseInt(m[1].replace(/,/g, ''));
      const suffix = m[2];
      const duration = 1600;
      const step = target / (duration / 16);
      let cur = 0;
      const it = setInterval(() => {
        cur += step;
        if (cur >= target) {
          cur = target;
          clearInterval(it);
        }
        e.target.innerHTML = Math.floor(cur).toLocaleString() + suffix;
      }, 16);
    }
  });
}, { threshold: 0.5 });
document.querySelectorAll('.stat-num').forEach(b => statIo.observe(b));
</script>

</body>
</html>
