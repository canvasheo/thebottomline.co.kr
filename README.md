<!--DOCTYPE html-->
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Bottom Line — 보이지 않는 곳까지, 당신의 건강을 끌어올리다</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;0,9..144,600;0,9..144,700;0,9..144,900;1,9..144,400;1,9..144,500;1,9..144,600&family=Bricolage+Grotesque:opsz,wght@12..96,300;12..96,400;12..96,500;12..96,600;12..96,700;12..96,800&family=Noto+Serif+KR:wght@300;400;500;600;700;900&family=Noto+Sans+KR:wght@200;300;400;500;600;700;900&family=Gowun+Batang:wght@400;700&display=swap" rel="stylesheet">
<style>
:root{
  --cream:#F8F4ED;
  --cream-warm:#F2EAD9;
  --cream-deep:#E8DCC4;
  --sage:#9DBE96;
  --sage-light:#C5DBC0;
  --sage-deep:#5A7F54;
  --sage-darkest:#2D4329;
  --terra:#D4906F;
  --terra-soft:#EDC0A6;
  --clay:#A86A4E;
  --ink:#1F1D1A;
  --ink-soft:#3D3A35;
  --stone:#7A746C;
  --stone-light:#A89F94;
  --mist:#E4DCD0;
  --gold:#D6B775;
  --pink-soft:#E5B5B0;
  --pink-deep:#C77B73;
  --blue-soft:#A5C2D6;
  --plum:#8B5A6A;

  --display:'Fraunces',serif;
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
}
::selection{background:var(--sage-deep);color:var(--cream);}

/* ═══ NAV ═══ */
.nav{
  position:fixed;top:0;left:0;right:0;z-index:100;
  padding:22px 48px;
  display:flex;justify-content:space-between;align-items:center;
  background:rgba(248,244,237,.6);
  backdrop-filter:blur(20px);
  -webkit-backdrop-filter:blur(20px);
  border-bottom:1px solid transparent;
  transition:all .4s ease;
}
.nav.scrolled{
  background:rgba(248,244,237,.92);
  border-bottom-color:rgba(31,29,26,.06);
  padding:16px 48px;
}
.nav-logo{
  font-family:var(--display);
  font-size:22px;font-weight:500;
  letter-spacing:-.4px;color:var(--ink);
  display:flex;align-items:center;gap:10px;
  text-decoration:none;
  font-variation-settings:"opsz" 144;
}
.nav-logo-mark{
  width:28px;height:28px;border-radius:50%;
  background:linear-gradient(135deg,var(--sage),var(--sage-deep));
  display:flex;align-items:center;justify-content:center;
  color:white;font-size:13px;
}
.nav-menu{display:flex;gap:36px;align-items:center;}
.nav-link{
  font-family:var(--grotesque);
  font-size:13px;letter-spacing:.5px;font-weight:500;
  color:var(--ink-soft);text-decoration:none;
  transition:color .2s ease;
}
.nav-link:hover{color:var(--sage-deep);}
.nav-cta{
  background:var(--ink);color:var(--cream);
  padding:10px 22px;border-radius:24px;
  font-family:var(--grotesque);
  font-size:12px;font-weight:600;letter-spacing:.5px;
  text-decoration:none;
  transition:all .3s ease;
}
.nav-cta:hover{background:var(--sage-deep);transform:translateY(-1px);}

/* ═══ HERO ═══ */
.hero{
  min-height:100vh;
  position:relative;
  display:flex;align-items:center;
  padding:140px 48px 80px;
  overflow:hidden;
  background:linear-gradient(170deg,var(--cream) 0%,var(--cream-warm) 60%,#EDDFC4 100%);
}
.hero-orb{
  position:absolute;border-radius:50%;
  filter:blur(60px);
  pointer-events:none;
  opacity:.55;
  animation:floatOrb 14s ease-in-out infinite;
}
.hero-orb-1{
  width:520px;height:520px;
  top:-100px;right:-80px;
  background:radial-gradient(circle,rgba(157,190,150,.5),transparent 70%);
}
.hero-orb-2{
  width:380px;height:380px;
  bottom:-50px;left:10%;
  background:radial-gradient(circle,rgba(214,144,111,.35),transparent 70%);
  animation-delay:-4s;animation-duration:18s;
}
.hero-orb-3{
  width:280px;height:280px;
  top:30%;left:35%;
  background:radial-gradient(circle,rgba(214,183,117,.3),transparent 70%);
  animation-delay:-8s;animation-duration:16s;
}
@keyframes floatOrb{
  0%,100%{transform:translate(0,0) scale(1);}
  50%{transform:translate(30px,-30px) scale(1.08);}
}

.hero-grid{
  max-width:1380px;margin:0 auto;width:100%;
  display:grid;grid-template-columns:1.1fr .9fr;gap:80px;
  align-items:center;
  position:relative;z-index:2;
}
.hero-eyebrow{
  display:inline-flex;align-items:center;gap:10px;
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:3px;font-weight:600;
  color:var(--sage-deep);text-transform:uppercase;
  margin-bottom:32px;
  padding:7px 16px 7px 12px;
  background:rgba(157,190,150,.18);
  border:1px solid rgba(157,190,150,.3);
  border-radius:20px;
  animation:fadeUp .9s cubic-bezier(.2,.8,.2,1) both;
}
.hero-eyebrow-dot{
  width:6px;height:6px;border-radius:50%;
  background:var(--sage-deep);
  animation:pulse 2.5s ease-in-out infinite;
}
@keyframes pulse{0%,100%{opacity:.4;}50%{opacity:1;}}

.hero-title{
  font-family:var(--display);
  font-size:clamp(54px,7.4vw,108px);
  font-weight:400;
  line-height:.96;letter-spacing:-3px;
  color:var(--ink);
  margin-bottom:32px;
  animation:fadeUp .9s cubic-bezier(.2,.8,.2,1) .1s both;
  font-variation-settings:"opsz" 144;
}
.hero-title-line2{
  font-style:italic;
  color:var(--sage-deep);
  font-weight:500;
}
.hero-title-mark{
  font-family:var(--display);
  font-style:italic;
  color:var(--terra);
  font-weight:500;
  position:relative;
}
.hero-title-mark::after{
  content:'';
  position:absolute;
  bottom:8px;left:-2px;right:-2px;
  height:18px;
  background:rgba(157,190,150,.35);
  z-index:-1;
  border-radius:4px;
}

.hero-subtitle{
  font-family:var(--serif-kr);
  font-size:17px;line-height:1.85;font-weight:300;
  color:var(--ink-soft);
  max-width:520px;
  margin-bottom:44px;
  animation:fadeUp .9s cubic-bezier(.2,.8,.2,1) .2s both;
}
.hero-subtitle strong{color:var(--ink);font-weight:500;}

.hero-actions{
  display:flex;gap:16px;align-items:center;
  animation:fadeUp .9s cubic-bezier(.2,.8,.2,1) .3s both;
  flex-wrap:wrap;
}
.btn-primary{
  background:var(--ink);color:var(--cream);
  padding:16px 32px;border-radius:32px;
  font-family:var(--grotesque);
  font-size:13px;font-weight:600;letter-spacing:.5px;
  text-decoration:none;
  display:inline-flex;align-items:center;gap:10px;
  transition:all .3s ease;
}
.btn-primary:hover{
  background:var(--sage-deep);
  transform:translateY(-2px);
  box-shadow:0 12px 32px rgba(90,127,84,.28);
}
.btn-arrow{
  width:18px;height:18px;border-radius:50%;
  background:var(--cream);color:var(--ink);
  display:flex;align-items:center;justify-content:center;
  font-size:10px;
  transition:transform .3s ease;
}
.btn-primary:hover .btn-arrow{transform:translateX(3px);}

.btn-text{
  font-family:var(--grotesque);
  font-size:13px;letter-spacing:.5px;font-weight:500;
  color:var(--ink-soft);text-decoration:none;
  border-bottom:1px solid var(--ink-soft);
  padding-bottom:2px;
  transition:all .2s ease;
}
.btn-text:hover{color:var(--sage-deep);border-color:var(--sage-deep);}

.hero-tags{
  display:flex;gap:8px;margin-top:48px;flex-wrap:wrap;
  animation:fadeUp .9s cubic-bezier(.2,.8,.2,1) .4s both;
}
.hero-tag{
  font-family:var(--grotesque);
  font-size:12px;font-weight:500;letter-spacing:.5px;
  background:white;
  border:1px solid rgba(31,29,26,.08);
  color:var(--ink-soft);
  padding:6px 14px;
  border-radius:14px;
}
.hero-tag span{color:var(--sage-deep);font-weight:600;}

/* Hero phone */
.hero-visual{
  position:relative;
  display:flex;justify-content:center;
  animation:fadeUp 1.1s cubic-bezier(.2,.8,.2,1) .5s both;
}
.phone-shell{
  width:300px;height:600px;
  background:#1a1814;
  border-radius:44px;
  padding:8px;
  box-shadow:
    0 60px 120px rgba(0,0,0,.18),
    0 30px 60px rgba(0,0,0,.12),
    inset 0 0 0 2px rgba(255,255,255,.04);
  position:relative;
  transform:rotate(-2deg);
  transition:transform .8s cubic-bezier(.2,.8,.2,1);
}
.phone-shell:hover{transform:rotate(0deg) scale(1.02);}
.phone-screen{
  width:100%;height:100%;
  background:var(--cream);
  border-radius:36px;
  overflow:hidden;
  position:relative;
}
.phone-notch{
  position:absolute;top:8px;left:50%;
  transform:translateX(-50%);
  width:90px;height:24px;
  background:#1a1814;border-radius:14px;z-index:5;
}
.phone-content{
  height:100%;width:100%;
  padding:42px 18px 18px;
  overflow:hidden;
  display:flex;flex-direction:column;
}
.phone-header{
  background:var(--sage-darkest);
  border-radius:18px;padding:18px 14px;
  margin-bottom:14px;
}
.forest-row{display:flex;justify-content:space-around;align-items:flex-end;margin-bottom:10px;}
.forest-tree{display:flex;flex-direction:column;align-items:center;gap:4px;}
.forest-tree-icon{font-size:24px;}
.forest-tree-name{font-size:8px;color:rgba(255,255,255,.7);}
.forest-tree.active .forest-tree-name{color:var(--sage-light);font-weight:600;}
.forest-streak{
  background:rgba(255,255,255,.08);
  border-radius:10px;padding:7px 10px;
  display:flex;justify-content:space-between;
  font-size:9px;
}
.forest-streak-fire{color:#FFB668;}
.forest-streak-text{color:rgba(255,255,255,.85);}

.routine-title{
  font-size:11px;font-weight:700;
  color:var(--ink);margin-bottom:8px;letter-spacing:-.2px;
}
.routine-card{
  background:rgba(157,190,150,.16);
  border-radius:12px;padding:9px 11px;
  display:flex;align-items:center;gap:9px;
  margin-bottom:5px;
}
.routine-icon{
  width:26px;height:26px;border-radius:7px;
  background:white;display:flex;align-items:center;justify-content:center;
  font-size:13px;flex-shrink:0;
}
.routine-info{flex:1;min-width:0;}
.routine-time{font-size:7px;letter-spacing:.5px;color:var(--sage-deep);font-weight:700;text-transform:uppercase;}
.routine-name{font-size:10px;font-weight:600;color:var(--ink);line-height:1.2;}
.routine-desc{font-size:7.5px;color:var(--stone);}
.routine-check{
  width:18px;height:18px;border-radius:50%;
  background:var(--sage-deep);color:white;
  display:flex;align-items:center;justify-content:center;
  font-size:9px;flex-shrink:0;
}

.phone-floating-tag{
  position:absolute;
  background:white;
  border-radius:14px;
  padding:11px 14px;
  box-shadow:0 12px 36px rgba(0,0,0,.12);
  font-size:11px;
  display:flex;align-items:center;gap:8px;
  white-space:nowrap;
  border:1px solid rgba(31,29,26,.05);
  z-index:10;
}
.phone-floating-tag-icon{
  width:24px;height:24px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  font-size:13px;
}
.phone-floating-tag-info strong{
  font-family:var(--grotesque);
  font-size:11px;color:var(--ink);font-weight:600;display:block;
}
.phone-floating-tag-info span{
  font-family:var(--grotesque);
  font-size:9px;color:var(--stone);
}
.tag-1{top:80px;left:-50px;animation:floatTag 5s ease-in-out infinite;}
.tag-2{bottom:140px;right:-60px;animation:floatTag 6s ease-in-out infinite -2s;}
.tag-3{top:300px;right:-40px;animation:floatTag 5.5s ease-in-out infinite -3s;}
@keyframes floatTag{0%,100%{transform:translateY(0);}50%{transform:translateY(-8px);}}
@keyframes fadeUp{from{opacity:0;transform:translateY(24px);}to{opacity:1;transform:translateY(0);}}

/* ═══ TICKER ═══ */
.ticker-section{
  background:var(--ink);
  padding:24px 0;
  overflow:hidden;
  border-top:1px solid rgba(255,255,255,.06);
  border-bottom:1px solid rgba(255,255,255,.06);
}
.ticker{display:flex;animation:ticker 40s linear infinite;width:max-content;}
.ticker-item{
  font-family:var(--display);
  font-size:38px;font-style:italic;font-weight:400;
  color:rgba(255,255,255,.5);
  padding:0 36px;
  display:flex;align-items:center;
  font-variation-settings:"opsz" 144;
  white-space:nowrap;
}
.ticker-item em{color:rgba(157,190,150,.85);font-style:italic;}
.ticker-dot{
  width:8px;height:8px;border-radius:50%;
  background:var(--sage);margin:0 36px;
  flex-shrink:0;
}
@keyframes ticker{to{transform:translateX(-50%);}}

/* ═══ SECTION COMMON ═══ */
.section{padding:140px 48px;position:relative;}
.section-inner{max-width:1280px;margin:0 auto;}
.section-eyebrow{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:3px;font-weight:600;
  color:var(--sage-deep);text-transform:uppercase;
  margin-bottom:18px;display:flex;align-items:center;gap:14px;
}
.section-eyebrow::before{content:'';width:32px;height:1px;background:var(--sage-deep);}
.section-title{
  font-family:var(--display);
  font-size:clamp(42px,5.4vw,76px);
  font-weight:400;line-height:1.05;
  letter-spacing:-2px;color:var(--ink);
  margin-bottom:20px;
  font-variation-settings:"opsz" 144;
}
.section-title-italic{font-style:italic;font-weight:500;color:var(--sage-deep);}
.section-desc{
  font-family:var(--serif-kr);
  font-size:17px;line-height:1.85;font-weight:300;
  color:var(--ink-soft);max-width:680px;
  margin-bottom:64px;
}
.reveal{opacity:0;transform:translateY(32px);transition:opacity .9s ease,transform .9s cubic-bezier(.2,.8,.2,1);}
.reveal.in{opacity:1;transform:none;}

/* ═══ MARKET STATS (PPT 핵심 지표) ═══ */
.market-section{
  background:linear-gradient(180deg,var(--cream) 0%,var(--cream-warm) 100%);
  position:relative;
}
.market-headline{
  font-family:var(--display);
  font-size:clamp(36px,4.5vw,62px);
  font-weight:400;font-style:italic;
  line-height:1.2;letter-spacing:-1.5px;
  color:var(--ink);
  max-width:980px;
  margin-bottom:80px;
  font-variation-settings:"opsz" 144;
}
.market-headline em{color:var(--clay);font-style:italic;}
.market-headline strong{color:var(--sage-deep);font-weight:500;font-style:italic;}

.stats-grid{
  display:grid;grid-template-columns:repeat(4,1fr);
  gap:0;
  background:white;
  border-radius:28px;
  overflow:hidden;
  box-shadow:0 20px 60px rgba(31,29,26,.06);
}
.stat-block{
  padding:48px 32px;
  border-right:1px solid var(--mist);
  position:relative;
  overflow:hidden;
}
.stat-block:last-child{border-right:none;}
.stat-block::before{
  content:'';
  position:absolute;
  top:0;left:0;right:0;
  height:3px;
  opacity:.6;
}
.stat-block:nth-child(1)::before{background:var(--clay);}
.stat-block:nth-child(2)::before{background:var(--terra);}
.stat-block:nth-child(3)::before{background:var(--gold);}
.stat-block:nth-child(4)::before{background:var(--sage-deep);}

.stat-tag{
  font-family:var(--grotesque);
  font-size:10px;letter-spacing:2px;font-weight:600;
  text-transform:uppercase;
  margin-bottom:24px;
  color:var(--stone);
  display:flex;align-items:center;gap:8px;
}
.stat-tag-dot{
  width:6px;height:6px;border-radius:50%;
}
.stat-block:nth-child(1) .stat-tag-dot{background:var(--clay);}
.stat-block:nth-child(2) .stat-tag-dot{background:var(--terra);}
.stat-block:nth-child(3) .stat-tag-dot{background:var(--gold);}
.stat-block:nth-child(4) .stat-tag-dot{background:var(--sage-deep);}

.stat-num{
  font-family:var(--display);
  font-size:64px;font-weight:500;
  line-height:.9;letter-spacing:-2px;
  color:var(--ink);
  margin-bottom:14px;
  font-variation-settings:"opsz" 144;
}
.stat-num small{font-size:.4em;color:var(--stone);font-weight:400;}
.stat-block:nth-child(1) .stat-num{color:var(--clay);}
.stat-block:nth-child(2) .stat-num{color:var(--terra);}
.stat-block:nth-child(3) .stat-num{color:#9C7E40;}
.stat-block:nth-child(4) .stat-num{color:var(--sage-deep);}

.stat-label{
  font-family:var(--serif-kr);
  font-size:14px;font-weight:600;color:var(--ink);
  margin-bottom:8px;letter-spacing:-.3px;
}
.stat-source{
  font-family:var(--grotesque);
  font-size:10px;color:var(--stone-light);
  font-weight:400;line-height:1.5;
}

.problem-trio{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:20px;
  margin-top:48px;
}
.problem-card{
  background:white;
  border-radius:20px;
  padding:32px 28px;
  border:1px solid rgba(31,29,26,.05);
  position:relative;overflow:hidden;
  transition:all .4s ease;
}
.problem-card:hover{
  transform:translateY(-4px);
  box-shadow:0 20px 50px rgba(31,29,26,.08);
}
.problem-card-num{
  font-family:var(--display);
  font-size:11px;font-weight:600;
  color:var(--terra);letter-spacing:1.5px;
  margin-bottom:12px;
  font-variation-settings:"opsz" 14;
}
.problem-card-title{
  font-family:var(--serif-kr);
  font-size:18px;font-weight:600;
  color:var(--ink);
  line-height:1.4;margin-bottom:12px;letter-spacing:-.3px;
}
.problem-card-desc{
  font-family:var(--sans-kr);
  font-size:13px;color:var(--stone);line-height:1.7;font-weight:300;
}

/* ═══ INTERVENTION (4 GAPS) ═══ */
.gaps-section{
  background:var(--cream-warm);
}
.gaps-grid{
  display:grid;grid-template-columns:repeat(4,1fr);
  gap:20px;margin-top:48px;
}
.gap-card{
  background:rgba(255,255,255,.7);
  backdrop-filter:blur(10px);
  border:1px solid rgba(31,29,26,.05);
  border-radius:20px;
  padding:32px 24px;
  transition:all .4s ease;
}
.gap-card:hover{
  background:white;
  border-color:rgba(157,190,150,.4);
  transform:translateY(-4px);
  box-shadow:0 24px 60px rgba(31,29,26,.08);
}
.gap-num{
  font-family:var(--display);
  font-size:48px;font-weight:400;font-style:italic;
  color:var(--sage);letter-spacing:-1.5px;
  line-height:.9;margin-bottom:16px;
  font-variation-settings:"opsz" 144;
  opacity:.6;
}
.gap-title{
  font-family:var(--serif-kr);
  font-size:17px;font-weight:600;
  color:var(--ink);
  line-height:1.4;margin-bottom:14px;letter-spacing:-.3px;
}
.gap-desc{
  font-size:13px;color:var(--stone);line-height:1.7;font-weight:300;
}

/* ═══ JOURNEY ═══ */
.journey-section{
  background:var(--ink);
  color:var(--cream);
  padding:140px 0;
  position:relative;overflow:hidden;
}
.journey-section::before{
  content:'';position:absolute;
  top:-200px;right:-200px;
  width:600px;height:600px;border-radius:50%;
  background:radial-gradient(circle,rgba(157,190,150,.15),transparent 70%);
  filter:blur(40px);
}
.journey-section::after{
  content:'';position:absolute;
  bottom:-150px;left:-150px;
  width:500px;height:500px;border-radius:50%;
  background:radial-gradient(circle,rgba(214,144,111,.12),transparent 70%);
  filter:blur(40px);
}
.journey-section .section-inner{position:relative;z-index:2;}
.journey-section .section-eyebrow{color:var(--sage-light);}
.journey-section .section-eyebrow::before{background:var(--sage-light);}
.journey-section .section-title{color:var(--cream);}
.journey-section .section-title-italic{color:var(--sage-light);}
.journey-section .section-desc{color:rgba(248,244,237,.55);}

.journey-track{position:relative;margin:0 -48px;padding:0 48px;}
.journey-scenes{
  display:flex;gap:24px;
  overflow-x:auto;
  padding:20px 48px 32px;
  margin:-20px -48px 0;
  scroll-snap-type:x mandatory;
  scrollbar-width:none;
}
.journey-scenes::-webkit-scrollbar{display:none;}
.scene-card{
  min-width:340px;width:340px;
  background:linear-gradient(160deg,rgba(255,255,255,.04),rgba(255,255,255,.01));
  border:1px solid rgba(255,255,255,.08);
  border-radius:24px;
  padding:32px 28px;
  scroll-snap-align:start;
  position:relative;
  transition:all .4s ease;
  flex-shrink:0;
}
.scene-card:hover{
  border-color:rgba(157,190,150,.4);
  transform:translateY(-4px);
  background:linear-gradient(160deg,rgba(157,190,150,.06),rgba(255,255,255,.02));
}
.scene-num-row{display:flex;align-items:center;gap:14px;margin-bottom:24px;}
.scene-num{
  font-family:var(--display);
  font-size:14px;font-weight:600;
  color:var(--sage-light);letter-spacing:1.5px;
  font-variation-settings:"opsz" 14;
}
.scene-line{flex:1;height:1px;background:rgba(255,255,255,.1);}
.scene-emo{font-size:18px;}
.scene-illust{
  width:100%;height:140px;
  border-radius:14px;
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
  font-size:20px;font-weight:600;
  color:var(--cream);line-height:1.3;
  margin-bottom:14px;letter-spacing:-.3px;
}
.scene-text{
  font-size:13px;color:rgba(248,244,237,.6);
  line-height:1.7;font-weight:300;margin-bottom:18px;
}
.scene-quote{
  border-left:2px solid var(--sage-light);
  padding-left:14px;
  font-family:var(--batang);
  font-style:italic;font-size:13px;font-weight:400;
  color:var(--sage-light);
  line-height:1.6;
}
.journey-controls{
  display:flex;justify-content:space-between;align-items:center;
  margin-top:32px;padding:0 8px;
}
.journey-progress-bar{
  flex:1;height:2px;background:rgba(255,255,255,.08);
  border-radius:2px;margin:0 32px;position:relative;overflow:hidden;
}
.journey-progress-fill{
  position:absolute;left:0;top:0;height:100%;
  background:var(--sage);width:12.5%;
  transition:width .4s ease;
}
.journey-arrow{
  width:48px;height:48px;border-radius:50%;
  background:rgba(255,255,255,.08);
  border:1px solid rgba(255,255,255,.12);
  color:var(--cream);
  display:flex;align-items:center;justify-content:center;
  cursor:pointer;font-size:14px;
  transition:all .3s ease;
}
.journey-arrow:hover{background:var(--sage-deep);border-color:var(--sage-deep);}
.journey-arrow:disabled{opacity:.3;cursor:not-allowed;}

/* ═══ FOREST GROWTH (NEW) ═══ */
.forest-section{
  background:linear-gradient(180deg,var(--cream-warm) 0%,#E8DFC8 100%);
  position:relative;
  overflow:hidden;
}
.forest-section::before{
  content:'';
  position:absolute;
  top:50%;right:-200px;
  width:600px;height:600px;border-radius:50%;
  background:radial-gradient(circle,rgba(157,190,150,.2),transparent 70%);
  filter:blur(40px);
  pointer-events:none;
}
.forest-headline{
  font-family:var(--display);
  font-size:clamp(36px,4.4vw,60px);
  font-weight:400;
  line-height:1.1;letter-spacing:-1.5px;
  color:var(--ink);
  margin-bottom:24px;
  font-variation-settings:"opsz" 144;
}
.forest-headline em{font-style:italic;color:var(--sage-deep);}
.forest-headline .marker{
  background:linear-gradient(180deg,transparent 60%,rgba(214,144,111,.35) 60%);
  padding:0 4px;
}

.forest-stages{
  display:grid;
  grid-template-columns:repeat(7,1fr);
  gap:0;
  margin-top:64px;
  padding:48px 0 32px;
  position:relative;
}
.forest-stages::before{
  content:'';
  position:absolute;
  top:84px;left:6%;right:6%;
  height:2px;
  background:linear-gradient(90deg,
    rgba(157,190,150,.2) 0%,
    var(--sage) 50%,
    var(--sage-deep) 100%);
  z-index:0;
}
.stage{
  text-align:center;
  position:relative;z-index:1;
  cursor:pointer;
  transition:transform .3s ease;
}
.stage:hover{transform:translateY(-4px);}
.stage-icon-wrap{
  width:88px;height:88px;
  margin:0 auto 16px;
  border-radius:50%;
  background:white;
  border:2px solid var(--sage-light);
  display:flex;align-items:center;justify-content:center;
  font-size:34px;
  position:relative;
  box-shadow:0 8px 24px rgba(31,29,26,.06);
  transition:all .4s ease;
}
.stage:hover .stage-icon-wrap{
  transform:scale(1.1);
  box-shadow:0 16px 40px rgba(157,190,150,.3);
  border-color:var(--sage-deep);
}
.stage-icon-wrap::after{
  content:attr(data-count);
  position:absolute;
  bottom:-6px;right:-6px;
  background:var(--sage-deep);color:white;
  font-family:var(--grotesque);
  font-size:9px;font-weight:600;
  padding:3px 8px;border-radius:10px;
  letter-spacing:.5px;
}
.stage-name{
  font-family:var(--serif-kr);
  font-size:14px;font-weight:600;
  color:var(--ink);
  margin-bottom:4px;letter-spacing:-.3px;
}
.stage-en{
  font-family:var(--grotesque);
  font-size:9px;letter-spacing:1.5px;font-weight:500;
  color:var(--sage-deep);text-transform:uppercase;
}
.stage-arrow{
  position:absolute;
  top:38px;right:-12px;
  font-size:14px;color:var(--sage);
  font-family:var(--display);
}
.stage:last-child .stage-arrow{display:none;}

/* Tree showcase trio */
.trees-trio{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:24px;margin-top:96px;
}
.tree-card{
  background:white;
  border-radius:24px;
  padding:36px 32px;
  position:relative;overflow:hidden;
  border:1px solid rgba(31,29,26,.05);
  transition:all .4s ease;
}
.tree-card:hover{
  transform:translateY(-6px);
  box-shadow:0 24px 60px rgba(31,29,26,.08);
}
.tree-card.cherry{background:linear-gradient(160deg,#fff,#FDEEF1);}
.tree-card.pine{background:linear-gradient(160deg,#fff,#E9F0E5);}
.tree-card.bamboo{background:linear-gradient(160deg,#fff,#F5EBE5);}

.tree-icon-big{
  font-size:64px;
  margin-bottom:24px;
  display:inline-block;
  filter:drop-shadow(0 8px 16px rgba(31,29,26,.1));
}
.tree-card h3{
  font-family:var(--serif-kr);
  font-size:24px;font-weight:700;
  color:var(--ink);
  margin-bottom:6px;letter-spacing:-.5px;
}
.tree-purpose{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:2px;font-weight:600;
  text-transform:uppercase;
  margin-bottom:18px;
}
.tree-card.cherry .tree-purpose{color:var(--pink-deep);}
.tree-card.pine .tree-purpose{color:var(--sage-deep);}
.tree-card.bamboo .tree-purpose{color:var(--clay);}

.tree-desc{
  font-family:var(--serif-kr);
  font-size:14px;line-height:1.85;font-weight:300;
  color:var(--ink-soft);
  margin-bottom:24px;
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
.tree-card.cherry .tree-progress-fill{background:var(--pink-deep);width:70%;}
.tree-card.pine .tree-progress-fill{background:var(--sage-deep);width:55%;}
.tree-card.bamboo .tree-progress-fill{background:var(--clay);width:30%;}
.tree-progress-text{
  font-family:var(--grotesque);
  font-size:11px;font-weight:600;
  color:var(--ink);letter-spacing:.5px;
}

/* ═══ APP TABS (5개 탭) ═══ */
.tabs-section{background:var(--ink);color:var(--cream);position:relative;overflow:hidden;}
.tabs-section::before{
  content:'';position:absolute;
  top:-200px;left:-100px;
  width:500px;height:500px;border-radius:50%;
  background:radial-gradient(circle,rgba(157,190,150,.12),transparent 70%);
  filter:blur(40px);
}
.tabs-section .section-inner{position:relative;z-index:2;}
.tabs-section .section-eyebrow{color:var(--sage-light);}
.tabs-section .section-eyebrow::before{background:var(--sage-light);}
.tabs-section .section-title{color:var(--cream);}
.tabs-section .section-title-italic{color:var(--sage-light);}
.tabs-section .section-desc{color:rgba(248,244,237,.55);}

.tabs-grid{
  display:grid;grid-template-columns:repeat(5,1fr);
  gap:16px;margin-top:32px;
}
.tab-card{
  background:linear-gradient(165deg,rgba(255,255,255,.04),rgba(255,255,255,.01));
  border:1px solid rgba(255,255,255,.08);
  border-radius:20px;
  padding:32px 24px;
  transition:all .4s ease;
  position:relative;
  cursor:default;
}
.tab-card:hover{
  border-color:rgba(157,190,150,.4);
  background:linear-gradient(165deg,rgba(157,190,150,.06),rgba(255,255,255,.02));
  transform:translateY(-4px);
}
.tab-num{
  font-family:var(--display);
  font-size:11px;font-weight:600;
  color:var(--sage-light);letter-spacing:1.5px;
  margin-bottom:12px;
  font-variation-settings:"opsz" 14;
}
.tab-emoji{font-size:36px;margin-bottom:18px;display:block;filter:saturate(1.1);}
.tab-name{
  font-family:var(--serif-kr);
  font-size:18px;font-weight:700;
  color:var(--cream);
  margin-bottom:4px;letter-spacing:-.3px;
}
.tab-role{
  font-family:var(--grotesque);
  font-size:10px;letter-spacing:2px;font-weight:600;
  color:var(--sage-light);text-transform:uppercase;
  margin-bottom:18px;
}
.tab-features{
  list-style:none;display:flex;flex-direction:column;gap:8px;
}
.tab-features li{
  font-size:12px;color:rgba(248,244,237,.65);
  font-weight:300;line-height:1.6;
  padding-left:14px;position:relative;
}
.tab-features li::before{
  content:'·';
  position:absolute;left:0;top:0;
  color:var(--sage);font-weight:700;font-size:18px;line-height:.8;
}

/* ═══ FLOW SECTION (INPUT → CORE → OUTPUT) ═══ */
.flow-section{
  background:var(--cream);
  position:relative;overflow:hidden;
}
.flow-section::before{
  content:'';position:absolute;
  top:30%;left:-100px;
  width:400px;height:400px;border-radius:50%;
  background:radial-gradient(circle,rgba(157,190,150,.12),transparent 70%);
  filter:blur(40px);
  pointer-events:none;
}
.flow-track{
  display:grid;
  grid-template-columns:1fr auto 1.15fr auto 1fr;
  gap:0;align-items:stretch;
  margin-top:48px;
}
.flow-step{
  background:white;
  border-radius:24px;padding:36px 32px;
  border:1px solid rgba(31,29,26,.05);
  transition:all .4s ease;
  position:relative;overflow:hidden;
}
.flow-step:hover{
  transform:translateY(-6px);
  box-shadow:0 24px 60px rgba(31,29,26,.08);
}
.flow-step.center{
  background:linear-gradient(165deg,var(--sage-darkest),#1F3018);
  color:var(--cream);
  border-color:var(--sage-deep);
  transform:scale(1.04);
}
.flow-step.center:hover{transform:scale(1.04) translateY(-6px);}
.flow-num{
  font-family:var(--display);
  font-size:48px;font-weight:400;font-style:italic;
  letter-spacing:-1.5px;line-height:1;
  margin-bottom:14px;
  font-variation-settings:"opsz" 144;
  opacity:.5;
}
.flow-step:nth-child(1) .flow-num{color:var(--terra);}
.flow-step.center .flow-num{color:var(--sage-light);opacity:.8;}
.flow-step:nth-child(5) .flow-num{color:var(--sage-deep);}

.flow-label{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:3px;font-weight:700;
  text-transform:uppercase;
  margin-bottom:14px;
}
.flow-step:nth-child(1) .flow-label{color:var(--terra);}
.flow-step.center .flow-label{color:var(--sage-light);}
.flow-step:nth-child(5) .flow-label{color:var(--sage-deep);}

.flow-title{
  font-family:var(--serif-kr);
  font-size:22px;font-weight:700;
  letter-spacing:-.5px;
  margin-bottom:24px;
  line-height:1.3;
}
.flow-step .flow-title{color:var(--ink);}
.flow-step.center .flow-title{color:var(--cream);}

.flow-list{
  list-style:none;
  display:flex;flex-direction:column;gap:10px;
}
.flow-list li{
  font-size:13px;line-height:1.6;font-weight:300;
  padding-left:16px;position:relative;
}
.flow-step .flow-list li{color:var(--ink-soft);}
.flow-step.center .flow-list li{color:rgba(255,255,255,.75);}
.flow-list li::before{
  content:'·';
  position:absolute;left:0;top:0;
  font-weight:700;font-size:18px;line-height:.8;
}
.flow-step:nth-child(1) .flow-list li::before{color:var(--terra);}
.flow-step.center .flow-list li::before{color:var(--sage-light);}
.flow-step:nth-child(5) .flow-list li::before{color:var(--sage-deep);}

.flow-arrow{
  font-family:var(--display);
  font-size:32px;font-weight:300;
  color:var(--stone-light);
  display:flex;align-items:center;justify-content:center;
  padding:0 12px;
}

.flow-quote{
  margin-top:64px;padding:40px 48px;
  background:linear-gradient(135deg,rgba(157,190,150,.08),rgba(214,144,111,.06));
  border-radius:24px;
  text-align:center;
  border-left:3px solid var(--sage-deep);
}
.flow-quote p{
  font-family:var(--display);
  font-size:clamp(20px,2.6vw,32px);
  font-weight:400;line-height:1.5;
  letter-spacing:-.6px;
  color:var(--ink);
  font-variation-settings:"opsz" 144;
}
.flow-quote em{
  font-style:italic;
  color:var(--sage-deep);
  font-weight:500;
}

/* ═══ FEATURES — 5대 케어 솔루션 ═══ */
.solutions-section{
  background:linear-gradient(180deg,var(--cream) 0%,var(--cream-warm) 100%);
}
.solutions-grid{
  display:grid;grid-template-columns:1.2fr 1fr;
  gap:64px;align-items:center;
}
.solutions-tagline{
  font-family:var(--display);
  font-size:clamp(38px,4.6vw,62px);
  font-weight:400;font-style:italic;
  line-height:1.1;letter-spacing:-1.5px;
  color:var(--ink);
  margin-bottom:48px;
  font-variation-settings:"opsz" 144;
}
.solutions-tagline strong{color:var(--sage-deep);font-style:italic;font-weight:500;}
.solutions-tagline .num{
  font-family:var(--display);
  font-style:italic;
  color:var(--terra);
  font-weight:600;
  font-size:1.2em;
}

.solution-list{display:flex;flex-direction:column;gap:4px;}
.solution-item{
  display:flex;align-items:flex-start;gap:24px;
  padding:24px 0;
  border-bottom:1px solid rgba(31,29,26,.08);
  transition:all .3s ease;
}
.solution-item:last-child{border-bottom:none;}
.solution-item:hover{padding-left:8px;}
.solution-num{
  font-family:var(--display);
  font-size:18px;font-weight:600;font-style:italic;
  color:var(--sage-deep);
  letter-spacing:0;
  flex-shrink:0;width:36px;
  padding-top:2px;
  font-variation-settings:"opsz" 14;
}
.solution-content{flex:1;}
.solution-name{
  font-family:var(--serif-kr);
  font-size:19px;font-weight:600;
  color:var(--ink);
  margin-bottom:8px;letter-spacing:-.3px;
}
.solution-desc{
  font-size:13px;color:var(--stone);line-height:1.7;font-weight:300;
}
.solution-arrow{
  flex-shrink:0;
  width:32px;height:32px;border-radius:50%;
  background:rgba(157,190,150,.15);
  display:flex;align-items:center;justify-content:center;
  color:var(--sage-deep);font-size:11px;
  transition:all .3s ease;
}
.solution-item:hover .solution-arrow{
  background:var(--sage-deep);color:white;transform:translateX(4px);
}

.showcase-right{position:relative;display:flex;justify-content:center;}
.showcase-phone{
  width:300px;height:600px;
  background:#1a1814;
  border-radius:44px;padding:8px;
  box-shadow:0 50px 100px rgba(0,0,0,.18);
  position:relative;z-index:2;
}
.showcase-screen{
  width:100%;height:100%;
  background:white;
  border-radius:36px;
  overflow:hidden;
  position:relative;
}
.showcase-notch{
  position:absolute;top:8px;left:50%;
  transform:translateX(-50%);
  width:90px;height:24px;
  background:#1a1814;border-radius:14px;z-index:5;
}
.showcase-content{
  padding:42px 16px 16px;
  height:100%;overflow:hidden;
}
.showcase-h{
  font-size:11px;color:var(--ink);font-weight:700;
  margin-bottom:10px;
}

/* mini routine items reflecting new ppt content */
.routine-mini{
  background:rgba(157,190,150,.18);
  border:1px solid rgba(157,190,150,.3);
  border-radius:12px;padding:10px 12px;
  display:flex;align-items:center;gap:10px;
  margin-bottom:6px;
}
.routine-mini-icon{
  width:24px;height:24px;border-radius:6px;
  background:white;
  display:flex;align-items:center;justify-content:center;
  font-size:13px;flex-shrink:0;
}
.routine-mini-info{flex:1;}
.routine-mini-time{
  font-family:var(--grotesque);
  font-size:7px;letter-spacing:.5px;
  color:var(--sage-deep);font-weight:700;text-transform:uppercase;
}
.routine-mini-name{
  font-size:11px;font-weight:700;color:var(--ink);line-height:1.2;
}
.routine-mini-desc{font-size:8px;color:var(--stone);}
.routine-mini-check{
  width:16px;height:16px;border-radius:50%;
  background:var(--sage-deep);color:white;
  display:flex;align-items:center;justify-content:center;
  font-size:8px;
}

/* forest growth status in phone */
.forest-status{
  background:rgba(157,190,150,.1);
  border-radius:12px;padding:10px 12px;
  margin-top:10px;
}
.forest-status-h{
  font-size:9px;font-weight:700;color:var(--sage-deep);
  letter-spacing:.5px;margin-bottom:8px;
  display:flex;align-items:center;gap:5px;
}
.forest-status-row{
  display:flex;align-items:center;gap:8px;
  margin-bottom:5px;
  font-size:8px;
}
.forest-status-icon{font-size:14px;width:18px;text-align:center;}
.forest-status-info{flex:1;}
.forest-status-name{font-size:9px;font-weight:700;color:var(--ink);}
.forest-status-sub{font-size:7px;color:var(--stone);}
.forest-status-bar{
  width:50px;height:3px;border-radius:2px;background:var(--mist);
}
.forest-status-bar div{height:100%;border-radius:2px;}
.forest-status-count{
  font-family:var(--grotesque);
  font-size:8px;font-weight:700;color:var(--ink);
}

.showcase-deco{
  position:absolute;
  background:white;
  border-radius:14px;padding:12px 14px;
  box-shadow:0 20px 50px rgba(0,0,0,.12);
  font-size:11px;
  display:flex;align-items:center;gap:10px;
  border:1px solid rgba(31,29,26,.05);
  z-index:3;
}
.showcase-deco-1{top:80px;right:-30px;animation:floatTag 5s ease-in-out infinite;}
.showcase-deco-2{bottom:160px;left:-40px;animation:floatTag 6s ease-in-out infinite -2s;}
.deco-icon{
  width:32px;height:32px;border-radius:8px;
  display:flex;align-items:center;justify-content:center;font-size:16px;
}
.deco-text strong{
  font-family:var(--grotesque);
  font-size:12px;color:var(--ink);font-weight:700;display:block;
}
.deco-text span{
  font-family:var(--grotesque);
  font-size:10px;color:var(--stone);
}

/* ═══ AI TECH SECTION ═══ */
.tech-section{
  background:linear-gradient(165deg,#1a1814 0%,#2c241c 100%);
  color:var(--cream);
  position:relative;overflow:hidden;
}
.tech-section::before{
  content:'';position:absolute;
  top:-200px;right:-100px;
  width:500px;height:500px;border-radius:50%;
  background:radial-gradient(circle,rgba(214,144,111,.15),transparent 70%);
  filter:blur(40px);
}
.tech-section .section-inner{position:relative;z-index:2;}
.tech-section .section-eyebrow{color:var(--terra-soft);}
.tech-section .section-eyebrow::before{background:var(--terra-soft);}
.tech-section .section-title{color:var(--cream);}
.tech-section .section-title-italic{color:var(--terra-soft);}
.tech-section .section-desc{color:rgba(248,244,237,.55);}

.tech-grid{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:20px;margin-top:32px;
}
.tech-card{
  background:linear-gradient(165deg,rgba(255,255,255,.04),rgba(255,255,255,.01));
  border:1px solid rgba(255,255,255,.08);
  border-radius:20px;
  padding:32px 28px;
  transition:all .4s ease;
}
.tech-card:hover{
  border-color:rgba(214,144,111,.4);
  transform:translateY(-4px);
}
.tech-icon{
  width:48px;height:48px;border-radius:12px;
  background:rgba(214,144,111,.15);
  border:1px solid rgba(214,144,111,.25);
  display:flex;align-items:center;justify-content:center;
  font-size:22px;
  margin-bottom:20px;
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
  font-size:18px;font-weight:700;
  color:var(--cream);
  margin-bottom:14px;letter-spacing:-.3px;line-height:1.3;
}
.tech-desc{
  font-size:13px;color:rgba(248,244,237,.6);
  line-height:1.7;font-weight:300;
  margin-bottom:14px;
}
.tech-paper{
  background:rgba(214,144,111,.08);
  border-left:2px solid var(--terra);
  padding:10px 14px;border-radius:0 8px 8px 0;
}
.tech-paper-label{
  font-family:var(--grotesque);
  font-size:9px;letter-spacing:1.5px;font-weight:600;
  color:var(--terra-soft);text-transform:uppercase;
  margin-bottom:4px;
}
.tech-paper-cite{
  font-family:var(--batang);
  font-size:11px;color:rgba(248,244,237,.7);
  font-style:italic;line-height:1.5;
}

/* ═══ EMOTION CURVE ═══ */
.emotion-section{background:linear-gradient(180deg,var(--cream-warm) 0%,var(--cream) 100%);}
.emotion-chart{
  background:white;
  border-radius:32px;
  padding:56px 48px 40px;
  border:1px solid rgba(31,29,26,.04);
  box-shadow:0 30px 80px rgba(31,29,26,.05);
  margin-top:32px;
  position:relative;
}
.emo-zones{display:flex;justify-content:space-between;margin-bottom:24px;}
.emo-zone-tag{
  font-family:var(--grotesque);
  font-size:10px;letter-spacing:2px;font-weight:600;
  text-transform:uppercase;
  padding:5px 12px;border-radius:8px;
}
.emo-zone-tag.danger{color:var(--clay);background:rgba(168,106,78,.08);border:1px solid rgba(168,106,78,.2);}
.emo-zone-tag.growth{color:var(--sage-deep);background:rgba(90,127,84,.08);border:1px solid rgba(90,127,84,.2);}
.emo-zone-tag.thrive{color:#5A8DAA;background:rgba(90,141,170,.08);border:1px solid rgba(90,141,170,.2);}

.emo-svg-container{
  width:100%;height:280px;
  margin-bottom:16px;
  position:relative;
}
.emo-svg-container svg{width:100%;height:100%;overflow:visible;}
.emo-labels{display:flex;}
.emo-label{flex:1;text-align:center;}
.emo-label-step{
  font-family:var(--grotesque);
  font-size:9px;letter-spacing:1.5px;color:var(--stone-light);
  font-weight:600;margin-bottom:4px;
}
.emo-label-text{
  font-size:11px;color:var(--ink-soft);font-weight:500;line-height:1.3;
}
.emo-legend{
  display:flex;justify-content:center;gap:32px;
  margin-top:36px;padding-top:32px;
  border-top:1px solid var(--mist);flex-wrap:wrap;
}
.legend-item{
  display:flex;align-items:center;gap:10px;
  font-family:var(--grotesque);
  font-size:12px;color:var(--ink-soft);
}
.legend-dot{width:10px;height:10px;border-radius:50%;}

/* ═══ PRICING ═══ */
.pricing-section{background:var(--cream);}
.pricing-grid{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:20px;margin-top:48px;
}
.price-card{
  background:white;
  border-radius:24px;
  padding:40px 32px;
  border:1px solid rgba(31,29,26,.06);
  position:relative;
  transition:all .4s ease;
}
.price-card:hover{
  transform:translateY(-6px);
  box-shadow:0 24px 60px rgba(31,29,26,.08);
}
.price-card.featured{
  background:linear-gradient(165deg,var(--sage-darkest),#1F3018);
  color:var(--cream);
  border-color:var(--sage-deep);
}
.price-tag{
  font-family:var(--grotesque);
  font-size:10px;letter-spacing:2px;font-weight:600;
  text-transform:uppercase;
  padding:5px 12px;border-radius:12px;
  display:inline-block;
  margin-bottom:18px;
}
.price-card .price-tag{background:rgba(157,190,150,.15);color:var(--sage-deep);}
.price-card.featured .price-tag{background:rgba(255,255,255,.12);color:var(--sage-light);}

.price-target{
  font-family:var(--serif-kr);
  font-size:13px;color:var(--stone);
  margin-bottom:16px;font-weight:300;
}
.price-card.featured .price-target{color:rgba(255,255,255,.55);}

.price-name{
  font-family:var(--display);
  font-size:32px;font-weight:500;
  color:var(--ink);
  margin-bottom:32px;letter-spacing:-1px;line-height:1.1;
  font-variation-settings:"opsz" 144;
}
.price-card.featured .price-name{color:var(--cream);}
.price-name em{font-style:italic;color:var(--sage-deep);font-weight:500;}
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
  font-size:14px;font-weight:600;
  color:var(--ink);letter-spacing:-.2px;
}
.price-card.featured .price-tier-label{color:var(--cream);}
.price-tier-amount{
  font-family:var(--display);
  font-size:24px;font-weight:600;
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
  margin-top:24px;display:flex;flex-direction:column;gap:8px;
}
.price-features li{
  font-size:12px;color:var(--ink-soft);
  font-weight:300;line-height:1.6;
  padding-left:16px;position:relative;
}
.price-card.featured .price-features li{color:rgba(255,255,255,.65);}
.price-features li::before{
  content:'✓';
  position:absolute;left:0;top:0;
  color:var(--sage-deep);font-weight:700;font-size:11px;
}
.price-card.featured .price-features li::before{color:var(--sage-light);}

/* ═══ ROADMAP ═══ */
.roadmap-section{
  background:linear-gradient(180deg,var(--cream) 0%,var(--cream-warm) 100%);
}
.roadmap-track{
  margin-top:48px;
  position:relative;
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:0;
}
.roadmap-track::before{
  content:'';
  position:absolute;
  top:54px;left:8%;right:8%;
  height:2px;
  background:linear-gradient(90deg,
    var(--sage) 0%,
    var(--gold) 50%,
    var(--terra) 100%);
}
.phase{
  text-align:center;
  padding:0 24px;
  position:relative;
}
.phase-dot{
  width:28px;height:28px;border-radius:50%;
  background:white;
  border:3px solid var(--sage);
  margin:38px auto 24px;
  position:relative;z-index:1;
  transition:all .3s ease;
}
.phase:nth-child(2) .phase-dot{border-color:var(--gold);}
.phase:nth-child(3) .phase-dot{border-color:var(--terra);}
.phase:hover .phase-dot{transform:scale(1.2);}

.phase-tag{
  font-family:var(--grotesque);
  font-size:10px;letter-spacing:2px;font-weight:600;
  text-transform:uppercase;
  margin-bottom:8px;
}
.phase:nth-child(1) .phase-tag{color:var(--sage-deep);}
.phase:nth-child(2) .phase-tag{color:#9C7E40;}
.phase:nth-child(3) .phase-tag{color:var(--clay);}

.phase-title{
  font-family:var(--display);
  font-size:32px;font-weight:500;
  color:var(--ink);
  margin-bottom:6px;letter-spacing:-1px;
  font-variation-settings:"opsz" 144;
}
.phase-period{
  font-family:var(--grotesque);
  font-size:12px;color:var(--stone);
  font-weight:500;letter-spacing:.5px;
  margin-bottom:24px;
}
.phase-features{
  background:white;
  border-radius:18px;
  padding:24px 22px;
  border:1px solid rgba(31,29,26,.06);
  text-align:left;
}
.phase-features li{
  list-style:none;
  font-size:12px;color:var(--ink-soft);
  font-weight:300;line-height:1.7;
  padding:6px 0 6px 18px;
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

/* Roadmap closing tagline */
.roadmap-closing{
  text-align:center;
  margin-top:80px;padding:48px 32px;
  background:linear-gradient(135deg,rgba(157,190,150,.08),rgba(214,144,111,.06));
  border-radius:24px;
  border:1px solid rgba(157,190,150,.2);
}
.roadmap-closing-mark{
  font-size:36px;
  margin-bottom:20px;
  letter-spacing:8px;
}
.roadmap-closing-text{
  font-family:var(--display);
  font-size:clamp(28px,3.6vw,48px);
  font-weight:400;line-height:1.2;
  letter-spacing:-1.2px;
  color:var(--ink);
  margin-bottom:14px;
  font-variation-settings:"opsz" 144;
}
.roadmap-closing-text em{
  font-style:italic;
  color:var(--sage-deep);
  font-weight:500;
}
.roadmap-closing-sub{
  font-family:var(--serif-kr);
  font-size:14px;
  color:var(--stone);
  font-weight:300;
  letter-spacing:-.2px;
}

/* ═══ IMPACT SECTION (8 outcomes) ═══ */
.impact-section{
  background:linear-gradient(180deg,var(--cream-warm) 0%,var(--cream) 100%);
}
.impact-tracks{
  display:flex;flex-direction:column;gap:48px;
  margin-top:32px;
}
.impact-track{
  position:relative;
}
.impact-track-header{
  margin-bottom:32px;
}
.impact-track-tag{
  display:inline-block;
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:2px;font-weight:600;
  text-transform:uppercase;
  padding:6px 14px;border-radius:14px;
  margin-bottom:14px;
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
  font-size:clamp(28px,3.4vw,42px);
  font-weight:400;font-style:italic;
  line-height:1.2;letter-spacing:-1px;
  color:var(--ink);
  font-variation-settings:"opsz" 144;
}
.impact-grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:18px;
}
.impact-card{
  background:white;
  border-radius:18px;
  padding:28px 24px;
  border:1px solid rgba(31,29,26,.05);
  transition:all .4s ease;
  position:relative;
  overflow:hidden;
}
.impact-card:hover{
  transform:translateY(-4px);
  box-shadow:0 20px 50px rgba(31,29,26,.06);
  border-color:rgba(157,190,150,.4);
}
.impact-track:nth-child(1) .impact-card::before{
  content:'';position:absolute;
  top:0;left:0;width:3px;height:0;
  background:var(--sage-deep);
  transition:height .4s ease;
}
.impact-track:nth-child(2) .impact-card::before{
  content:'';position:absolute;
  top:0;left:0;width:3px;height:0;
  background:var(--terra);
  transition:height .4s ease;
}
.impact-card:hover::before{height:100%;}
.impact-num{
  font-family:var(--display);
  font-size:14px;font-weight:600;font-style:italic;
  letter-spacing:1px;
  margin-bottom:14px;
  font-variation-settings:"opsz" 14;
}
.impact-track:nth-child(1) .impact-num{color:var(--sage-deep);}
.impact-track:nth-child(2) .impact-num{color:var(--clay);}
.impact-card h4{
  font-family:var(--serif-kr);
  font-size:16px;font-weight:700;
  color:var(--ink);
  line-height:1.4;letter-spacing:-.3px;
  margin-bottom:10px;
}
.impact-card p{
  font-size:12px;color:var(--stone);
  line-height:1.7;font-weight:300;
}

/* ═══ MANIFESTO ═══ */
.manifesto-section{
  background:linear-gradient(165deg,var(--sage-darkest) 0%,#1A2914 100%);
  color:var(--cream);
  padding:160px 48px;
  text-align:center;
  position:relative;overflow:hidden;
}
.manifesto-section::before{
  content:'';position:absolute;
  top:-200px;right:-200px;
  width:600px;height:600px;border-radius:50%;
  background:radial-gradient(circle,rgba(157,190,150,.15),transparent 70%);
  filter:blur(40px);
}
.manifesto-section::after{
  content:'';position:absolute;
  bottom:-150px;left:-150px;
  width:500px;height:500px;border-radius:50%;
  background:radial-gradient(circle,rgba(214,144,111,.12),transparent 70%);
  filter:blur(40px);
}
.manifesto-inner{position:relative;z-index:2;max-width:1100px;margin:0 auto;}

.manifesto-mark{
  font-family:var(--display);
  font-size:80px;line-height:1;
  color:var(--sage-light);opacity:.4;
  margin-bottom:24px;
  font-style:italic;
  font-variation-settings:"opsz" 144;
}
.manifesto-text{
  font-family:var(--display);
  font-size:clamp(36px,4.5vw,68px);
  font-weight:400;
  line-height:1.2;letter-spacing:-1.5px;
  color:var(--cream);
  margin:0 auto 48px;
  font-variation-settings:"opsz" 144;
}
.manifesto-text em{
  font-style:italic;
  color:var(--sage-light);
  font-weight:500;
}
.manifesto-text .highlight{
  position:relative;
  display:inline-block;
}
.manifesto-text .highlight::after{
  content:'';
  position:absolute;
  bottom:8px;left:-4px;right:-4px;
  height:14px;
  background:rgba(214,144,111,.4);
  z-index:-1;
  border-radius:4px;
}

.manifesto-pillars{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:24px;
  margin-top:80px;
}
.pillar{
  padding:32px 24px;
  border:1px solid rgba(255,255,255,.1);
  border-radius:18px;
  background:rgba(255,255,255,.03);
  text-align:center;
  transition:all .4s ease;
}
.pillar:hover{
  border-color:rgba(157,190,150,.4);
  transform:translateY(-4px);
}
.pillar-en{
  font-family:var(--display);
  font-size:18px;font-style:italic;font-weight:500;
  color:var(--sage-light);
  margin-bottom:14px;letter-spacing:-.5px;
  font-variation-settings:"opsz" 14;
}
.pillar-kr{
  font-family:var(--serif-kr);
  font-size:14px;font-weight:300;
  color:rgba(255,255,255,.7);
  line-height:1.7;
}

.manifesto-author{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:3px;font-weight:600;
  color:rgba(255,255,255,.4);text-transform:uppercase;
  margin-top:64px;
}

/* ═══ CTA ═══ */
.cta-section{
  background:var(--cream);
  padding:160px 48px;
  position:relative;overflow:hidden;
}
.cta-orb{
  position:absolute;border-radius:50%;
  filter:blur(60px);
  pointer-events:none;
  opacity:.5;
}
.cta-orb-1{
  width:500px;height:500px;
  top:-100px;right:-100px;
  background:radial-gradient(circle,rgba(157,190,150,.4),transparent 70%);
}
.cta-orb-2{
  width:400px;height:400px;
  bottom:-80px;left:-80px;
  background:radial-gradient(circle,rgba(214,144,111,.3),transparent 70%);
}
.cta-inner{
  max-width:900px;margin:0 auto;
  text-align:center;position:relative;z-index:2;
}
.cta-eyebrow{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:4px;font-weight:600;
  color:var(--sage-deep);text-transform:uppercase;
  margin-bottom:24px;
}
.cta-title{
  font-family:var(--display);
  font-size:clamp(48px,6.4vw,108px);
  font-weight:400;line-height:1.05;
  letter-spacing:-2.5px;
  color:var(--ink);
  margin-bottom:32px;
  font-variation-settings:"opsz" 144;
}
.cta-title-italic{font-style:italic;color:var(--sage-deep);font-weight:500;}
.cta-desc{
  font-family:var(--serif-kr);
  font-size:17px;line-height:1.85;font-weight:300;
  color:var(--ink-soft);
  max-width:560px;margin:0 auto 48px;
}
.cta-buttons{display:flex;gap:16px;justify-content:center;flex-wrap:wrap;}
.btn-cta-primary{
  background:var(--ink);color:var(--cream);
  padding:18px 36px;border-radius:32px;
  font-family:var(--grotesque);
  font-size:14px;font-weight:600;letter-spacing:.5px;
  text-decoration:none;
  display:inline-flex;align-items:center;gap:12px;
  transition:all .3s ease;
}
.btn-cta-primary:hover{
  background:var(--sage-deep);
  transform:translateY(-2px);
  box-shadow:0 16px 40px rgba(90,127,84,.3);
}
.btn-cta-secondary{
  background:transparent;color:var(--ink);
  border:1px solid rgba(31,29,26,.2);
  padding:18px 36px;border-radius:32px;
  font-family:var(--grotesque);
  font-size:14px;font-weight:500;letter-spacing:.5px;
  text-decoration:none;
  display:inline-flex;align-items:center;gap:12px;
  transition:all .3s ease;
}
.btn-cta-secondary:hover{
  background:white;border-color:var(--sage-deep);
}

/* ═══ FOOTER ═══ */
footer{
  background:var(--ink);
  color:var(--stone-light);
  padding:80px 48px 40px;
}
.footer-inner{max-width:1280px;margin:0 auto;}
.footer-grid{
  display:grid;grid-template-columns:2fr 1fr 1fr 1fr;
  gap:64px;
  padding-bottom:48px;
  border-bottom:1px solid rgba(255,255,255,.08);
  margin-bottom:32px;
}
.footer-logo{
  font-family:var(--display);
  font-size:28px;font-weight:500;
  color:var(--cream);
  letter-spacing:-.5px;
  margin-bottom:16px;
  font-variation-settings:"opsz" 144;
}
.footer-tagline{
  font-family:var(--serif-kr);
  font-size:14px;line-height:1.8;font-weight:300;
  color:rgba(248,244,237,.55);
  max-width:340px;
}
.footer-col-title{
  font-family:var(--grotesque);
  font-size:11px;letter-spacing:2px;font-weight:600;
  color:var(--sage-light);text-transform:uppercase;
  margin-bottom:18px;
}
.footer-col ul{list-style:none;display:flex;flex-direction:column;gap:10px;}
.footer-col a{
  font-family:var(--sans-kr);
  font-size:13px;color:rgba(248,244,237,.55);
  text-decoration:none;
  transition:color .2s ease;
  font-weight:300;
}
.footer-col a:hover{color:var(--cream);}
.footer-bottom{
  display:flex;justify-content:space-between;align-items:center;
  padding-top:24px;
  font-family:var(--grotesque);
  font-size:11px;color:rgba(248,244,237,.35);
  letter-spacing:.5px;flex-wrap:wrap;gap:16px;
}
.footer-disclaimer{
  font-family:var(--batang);
  font-size:11px;color:rgba(248,244,237,.4);
  font-weight:400;
  background:rgba(255,255,255,.03);
  padding:14px 18px;border-radius:8px;
  margin-top:24px;line-height:1.6;
  font-style:italic;
  border-left:2px solid rgba(157,190,150,.3);
}

/* ═══ RESPONSIVE ═══ */
@media (max-width:1100px){
  .stats-grid{grid-template-columns:1fr 1fr;}
  .stat-block{border-right:none;border-bottom:1px solid var(--mist);}
  .stat-block:nth-child(2){border-right:none;}
  .stat-block:nth-child(2n){border-right:none;}
  .stat-block:nth-last-child(-n+2){border-bottom:none;}
  .gaps-grid{grid-template-columns:1fr 1fr;}
  .tabs-grid{grid-template-columns:repeat(3,1fr);}
  .tabs-grid .tab-card:last-child{grid-column:span 1;}
  .pricing-grid{grid-template-columns:1fr;}
  .forest-stages{grid-template-columns:repeat(4,1fr);gap:24px;padding:24px 0;}
  .forest-stages::before{display:none;}
  .impact-grid{grid-template-columns:repeat(2,1fr);}
}
@media (max-width:980px){
  .nav{padding:18px 24px;}
  .nav-menu{display:none;}
  .hero{padding:120px 24px 60px;}
  .hero-grid{grid-template-columns:1fr;gap:60px;}
  .section{padding:80px 24px;}
  .problem-trio{grid-template-columns:1fr;}
  .trees-trio{grid-template-columns:1fr;}
  .roadmap-track{grid-template-columns:1fr;gap:32px;}
  .roadmap-track::before{display:none;}
  .solutions-grid{grid-template-columns:1fr;gap:48px;}
  .tech-grid{grid-template-columns:1fr;}
  .manifesto-pillars{grid-template-columns:1fr;}
  .footer-grid{grid-template-columns:1fr 1fr;gap:32px;}
  .flow-track{grid-template-columns:1fr;gap:24px;}
  .flow-step.center{transform:scale(1);}
  .flow-step.center:hover{transform:translateY(-6px);}
  .flow-arrow{transform:rotate(90deg);padding:0;}
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
}
</style>
</head>
<body>

<!-- ═══════════════ NAV ═══════════════ -->
<nav class="nav" id="nav">
  <a href="#top" class="nav-logo">
    <span class="nav-logo-mark">🌿</span>
    The Bottom Line
  </a>
  <div class="nav-menu">
    <a href="#problem" class="nav-link">문제 인식</a>
    <a href="#service" class="nav-link">서비스</a>
    <a href="#tech" class="nav-link">기술</a>
    <a href="#pricing" class="nav-link">요금제</a>
    <a href="#cta" class="nav-cta">앱 다운로드 →</a>
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
        보이지 않는 곳까지,<br>
        <span class="hero-title-line2">당신의 건강을<br><span class="hero-title-mark">끌어올리다.</span></span>
      </h1>
      <p class="hero-subtitle">
        병원 가기엔 애매하고, 그냥 두기엔 불안한 그 중간.<br>
        <strong>3초 원터치 기록</strong>으로 시작되는, 부끄럽지 않은 자기 관리.
      </p>
      <div class="hero-actions">
        <a href="#cta" class="btn-primary">
          시작하기
          <span class="btn-arrow">→</span>
        </a>
        <a href="#service" class="btn-text">서비스 둘러보기</a>
      </div>
      <div class="hero-tags">
        <span class="hero-tag"><span>#</span>하부이너뷰티</span>
        <span class="hero-tag"><span>#</span>단백뇨관리</span>
        <span class="hero-tag"><span>#</span>치질예방</span>
        <span class="hero-tag"><span>#</span>나노루틴</span>
        <span class="hero-tag"><span>#</span>게이미피케이션</span>
      </div>
    </div>

    <div class="hero-visual">
      <div class="phone-floating-tag tag-1">
        <div class="phone-floating-tag-icon" style="background:rgba(157,190,150,.18);">🚶</div>
        <div class="phone-floating-tag-info">
          <strong>기상 후 스트레칭</strong>
          <span>오전 7:30 · 5분 완료</span>
        </div>
      </div>
      <div class="phone-floating-tag tag-2">
        <div class="phone-floating-tag-icon" style="background:rgba(214,183,117,.2);">🌸</div>
        <div class="phone-floating-tag-info">
          <strong>벚꽃나무 +1 성장</strong>
          <span>새잎 → 꽃봉오리 (6/9)</span>
        </div>
      </div>
      <div class="phone-floating-tag tag-3">
        <div class="phone-floating-tag-icon" style="background:rgba(229,181,176,.25);">🔥</div>
        <div class="phone-floating-tag-info">
          <strong>연속 12일째</strong>
          <span>숲 67% 달성</span>
        </div>
      </div>

      <div class="phone-shell">
        <div class="phone-screen">
          <div class="phone-notch"></div>
          <div class="phone-content">
            <div class="phone-header">
              <div class="forest-row">
                <div class="forest-tree active">
                  <div class="forest-tree-icon">🌿</div>
                  <div class="forest-tree-name">벚꽃나무</div>
                </div>
                <div class="forest-tree">
                  <div class="forest-tree-icon">🪵</div>
                  <div class="forest-tree-name">소나무</div>
                </div>
                <div class="forest-tree">
                  <div class="forest-tree-icon">🫘</div>
                  <div class="forest-tree-name">대나무</div>
                </div>
              </div>
              <div class="forest-streak">
                <span class="forest-streak-fire">🔥 연속 12일째</span>
                <span class="forest-streak-text">숲 67% 달성</span>
              </div>
            </div>

            <div class="routine-title">오늘의 나노 루틴</div>
            <div class="routine-card">
              <div class="routine-icon">🚶</div>
              <div class="routine-info">
                <div class="routine-time">아침 루틴</div>
                <div class="routine-name">기상 후 스트레칭</div>
                <div class="routine-desc">항문 혈류 개선 5분</div>
              </div>
              <div class="routine-check">✓</div>
            </div>
            <div class="routine-card">
              <div class="routine-icon">🌿</div>
              <div class="routine-info">
                <div class="routine-time">점심 루틴</div>
                <div class="routine-name">식이섬유 섭취</div>
                <div class="routine-desc">채소·과일 목표량 절반</div>
              </div>
              <div class="routine-check">✓</div>
            </div>
            <div class="routine-card">
              <div class="routine-icon">🪑</div>
              <div class="routine-info">
                <div class="routine-time">저녁 루틴</div>
                <div class="routine-name">좌욕 5분</div>
                <div class="routine-desc">하부 케어 루틴 유지</div>
              </div>
              <div class="routine-check">✓</div>
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
    <span class="ticker-item"><em>3초 원터치</em></span>
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
    <span class="ticker-item"><em>3초 원터치</em></span>
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

<!-- ═══════════════ MARKET (NEW: PPT 핵심 통계) ═══════════════ -->
<section class="section market-section" id="problem">
  <div class="section-inner">
    <div class="section-eyebrow reveal">시장 현황 · 문제 인식</div>
    <h2 class="market-headline reveal">
      살을 빼려고 시작한 다이어트가,<br>
      <em>젊은 콩팥과 항문</em>을 위협합니다.<br>
      <strong>그 사이의 시간</strong>이 가장 위험합니다.
    </h2>

    <div class="stats-grid reveal">
      <div class="stat-block">
        <div class="stat-tag"><span class="stat-tag-dot"></span>만성콩팥병</div>
        <div class="stat-num">90<small>%↑</small></div>
        <div class="stat-label">말기콩팥병 유병 인구</div>
        <div class="stat-source">2012 → 2022 / 10년간 증가율<br>대한신장학회 팩트시트 2024</div>
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
        <h3 class="problem-card-title">영양성 문제</h3>
        <p class="problem-card-desc">
          섬유질 부족 → 변비 유발. 신장 부담 증가, 반복적 체중 감량 사이클이 누적됩니다.
        </p>
      </div>
      <div class="problem-card reveal">
        <div class="problem-card-num">PROBLEM / 02</div>
        <h3 class="problem-card-title">신체성 문제</h3>
        <p class="problem-card-desc">
          하루 평균 8~10시간 좌식 생활. 항문·골반 혈류 저하, 소화기 기능 저하로 직장인 위험군 급증.
        </p>
      </div>
      <div class="problem-card reveal">
        <div class="problem-card-num">PROBLEM / 03</div>
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
        <p class="gap-desc">
          증상이 없으면 사용자가 스스로 인지하기 어렵습니다.
        </p>
      </div>
      <div class="gap-card reveal">
        <div class="gap-num">02</div>
        <h3 class="gap-title">검진 이후의<br>지속 관리 단절</h3>
        <p class="gap-desc">
          검진 결과 유소견이 있어도 관리 행동으로 이어지지 않습니다.
        </p>
      </div>
      <div class="gap-card reveal">
        <div class="gap-num">03</div>
        <h3 class="gap-title">진료실 밖 생활습관<br>실행의 어려움</h3>
        <p class="gap-desc">
          섬유질·수분·배변 습관 교정 등 일상에서 장기간 수행이 필요합니다.
        </p>
      </div>
      <div class="gap-card reveal">
        <div class="gap-num">04</div>
        <h3 class="gap-title">민감한 증상의<br>의료 이용 지연</h3>
        <p class="gap-desc">
          낙인 우려·당혹감으로 병원 방문이 늦어지고 관리 공백이 길어집니다.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ JOURNEY ═══════════════ -->
<section class="journey-section" id="journey">
  <div class="section-inner" style="padding:0 48px;">
    <div class="section-eyebrow reveal">고객의 이야기 · 8개 장면</div>
    <h2 class="section-title reveal">
      이지은이<br>
      <span class="section-title-italic">되찾은 것들.</span>
    </h2>
    <p class="section-desc reveal">
      33세 마케터, 2년간 15kg 감량. 성공의 이면에서 발견된 거품뇨에서 시작해<br>
      <em style="color:var(--sage-light);">자기 몸의 언어를 다시 이해하기까지</em>의 8개 장면.
    </p>
  </div>

  <div class="journey-track">
    <div class="journey-scenes" id="journeyScenes">

      <div class="scene-card">
        <div class="scene-num-row">
          <span class="scene-num">SCENE / 01</span>
          <div class="scene-line"></div>
          <span class="scene-emo">😟</span>
        </div>
        <div class="scene-illust scene-illust-1">
          <svg viewBox="0 0 200 100" width="160" height="80">
            <ellipse cx="100" cy="55" rx="62" ry="14" fill="rgba(157,190,150,.15)" stroke="rgba(157,190,150,.3)" stroke-width="1"/>
            <circle cx="80" cy="50" r="4" fill="rgba(255,255,255,.6)"><animate attributeName="cy" values="50;46;50" dur="2.5s" repeatCount="indefinite"/></circle>
            <circle cx="100" cy="55" r="6" fill="rgba(255,255,255,.7)"><animate attributeName="cy" values="55;49;55" dur="2.8s" repeatCount="indefinite"/></circle>
            <circle cx="118" cy="52" r="4" fill="rgba(255,255,255,.55)"><animate attributeName="cy" values="52;47;52" dur="2.3s" repeatCount="indefinite"/></circle>
            <circle cx="92" cy="58" r="3" fill="rgba(255,255,255,.5)"><animate attributeName="cy" values="58;54;58" dur="2.1s" repeatCount="indefinite"/></circle>
            <text x="100" y="28" text-anchor="middle" font-size="22" fill="rgba(212,144,111,.8)" font-family="serif" font-style="italic">?</text>
          </svg>
        </div>
        <div class="scene-phase">균열의 시작</div>
        <h3 class="scene-title">15kg을 빼고 나서,<br>거품이 보였다</h3>
        <p class="scene-text">
          2년간의 고단백 식단과 필라테스. 주변 반응도 좋았다.
          그런데 어느 날 아침, 화장실에서 거품이 보이기 시작했다.
        </p>
        <div class="scene-quote">"이게 뭐지... 원래 이런 거였나?"</div>
      </div>

      <div class="scene-card">
        <div class="scene-num-row">
          <span class="scene-num">SCENE / 02</span>
          <div class="scene-line"></div>
          <span class="scene-emo">😔</span>
        </div>
        <div class="scene-illust scene-illust-2">
          <svg viewBox="0 0 200 100" width="160" height="80">
            <rect x="50" y="20" width="100" height="60" rx="8" fill="rgba(255,255,255,.95)"/>
            <rect x="56" y="28" width="88" height="6" rx="3" fill="#ccc"/>
            <text x="60" y="48" font-size="6" fill="#1a0dab" font-family="sans-serif">거품뇨, 정말 위험한가요?</text>
            <text x="60" y="58" font-size="5" fill="#D44" font-family="sans-serif">단백뇨 의심...</text>
            <text x="60" y="66" font-size="5" fill="#666" font-family="sans-serif">만성콩팥병 초기 증상...</text>
            <text x="60" y="76" font-size="5" fill="#666" font-family="sans-serif">병원 가야 할까?</text>
          </svg>
        </div>
        <div class="scene-phase">불안의 증폭</div>
        <h3 class="scene-title">검색은 답이 아니라<br>불안이었다</h3>
        <p class="scene-text">
          첫 줄: "단백뇨 의심, 만성콩팥병 초기 증상일 수 있습니다."
          내과 예약 창을 열었다 닫았다.
        </p>
        <div class="scene-quote">"카톡을 쓰다 지웠다. 너무 오버하는 것 같아서."</div>
      </div>

      <div class="scene-card">
        <div class="scene-num-row">
          <span class="scene-num">SCENE / 03</span>
          <div class="scene-line"></div>
          <span class="scene-emo">🤔</span>
        </div>
        <div class="scene-illust scene-illust-3">
          <svg viewBox="0 0 200 100" width="160" height="80">
            <rect x="60" y="15" width="80" height="70" rx="10" fill="rgba(157,190,150,.4)"/>
            <text x="100" y="40" text-anchor="middle" font-size="7" fill="white" font-family="serif" font-weight="bold">"다이어트 중</text>
            <text x="100" y="50" text-anchor="middle" font-size="7" fill="white" font-family="serif" font-weight="bold">몸이 보내는 신호,</text>
            <text x="100" y="60" text-anchor="middle" font-size="7" fill="white" font-family="serif" font-weight="bold">무시하고 있나요?"</text>
            <text x="100" y="76" text-anchor="middle" font-size="5" fill="rgba(255,255,255,.7)">@wellness_pilates</text>
          </svg>
        </div>
        <div class="scene-phase">우연한 발견</div>
        <h3 class="scene-title">SNS에서 우연히,<br>나만 그런 게 아니었다</h3>
        <p class="scene-text">
          주말 인스타그램 릴스. 필라테스 강사가 자기 경험을 말한다. 병원 가기 전에 시작한 기록 이야기.
        </p>
        <div class="scene-quote">"바로 병원이 아닌 선택지가 있다는 걸 처음 알았다."</div>
      </div>

      <div class="scene-card">
        <div class="scene-num-row">
          <span class="scene-num">SCENE / 04</span>
          <div class="scene-line"></div>
          <span class="scene-emo">😊</span>
        </div>
        <div class="scene-illust scene-illust-4">
          <svg viewBox="0 0 200 100" width="160" height="80">
            <rect x="50" y="15" width="100" height="70" rx="10" fill="rgba(255,255,255,.95)"/>
            <text x="100" y="32" text-anchor="middle" font-size="7" fill="#2C2A26" font-weight="bold">자가 체크 7문항</text>
            <rect x="58" y="40" width="84" height="10" rx="3" fill="rgba(157,190,150,.6)"/>
            <text x="100" y="48" text-anchor="middle" font-size="6" fill="white" font-weight="600">고단백 식단 6개월+ ✓</text>
            <rect x="58" y="54" width="84" height="10" rx="3" fill="rgba(157,190,150,.6)"/>
            <text x="100" y="62" text-anchor="middle" font-size="6" fill="white" font-weight="600">거품뇨 경험 ✓</text>
            <rect x="58" y="68" width="84" height="10" rx="3" fill="rgba(157,190,150,.6)"/>
            <text x="100" y="76" text-anchor="middle" font-size="6" fill="white" font-weight="600">하루 8시간 좌식 ✓</text>
          </svg>
        </div>
        <div class="scene-phase">첫 만남</div>
        <h3 class="scene-title">7개 문항,<br>전부 '예'였다</h3>
        <p class="scene-text">
          앱이 말했다. 병원을 권유하는 대신, "지금은 생활기록을 시작할 적절한 타이밍이에요."
        </p>
        <div class="scene-quote">"의사가 아닌, 옆에서 말해주는 것 같았다."</div>
      </div>

      <div class="scene-card">
        <div class="scene-num-row">
          <span class="scene-num">SCENE / 05</span>
          <div class="scene-line"></div>
          <span class="scene-emo">🌱</span>
        </div>
        <div class="scene-illust scene-illust-5">
          <svg viewBox="0 0 200 100" width="160" height="80">
            <rect x="50" y="20" width="100" height="60" rx="10" fill="rgba(255,255,255,.95)"/>
            <text x="60" y="32" font-size="6" fill="#2C2A26" font-weight="bold">오늘의 나노 루틴</text>
            <rect x="58" y="36" width="84" height="11" rx="3" fill="rgba(157,190,150,.2)"/>
            <text x="62" y="44" font-size="5" fill="#2C2A26">🚶 기상 후 스트레칭</text>
            <text x="138" y="44" font-size="6" fill="#5A7F54">✓</text>
            <rect x="58" y="49" width="84" height="11" rx="3" fill="rgba(157,190,150,.2)"/>
            <text x="62" y="57" font-size="5" fill="#2C2A26">🌿 식이섬유 섭취</text>
            <text x="138" y="57" font-size="6" fill="#5A7F54">✓</text>
            <rect x="58" y="62" width="84" height="11" rx="3" fill="rgba(157,190,150,.2)"/>
            <text x="62" y="70" font-size="5" fill="#2C2A26">🪑 좌욕 5분</text>
            <text x="138" y="70" font-size="6" fill="#5A7F54">✓</text>
          </svg>
        </div>
        <div class="scene-phase">루틴의 시작</div>
        <h3 class="scene-title">하루 3초,<br>식물이 자랐다</h3>
        <p class="scene-text">
          출근길 지하철에서 엄지 세 번. 14일째, 처음으로 빠짐없이 기록을 마쳤다.
        </p>
        <div class="scene-quote">"기록이 귀찮다고 생각했는데, 진짜 3초였다."</div>
      </div>

      <div class="scene-card">
        <div class="scene-num-row">
          <span class="scene-num">SCENE / 06</span>
          <div class="scene-line"></div>
          <span class="scene-emo">💚</span>
        </div>
        <div class="scene-illust scene-illust-6">
          <svg viewBox="0 0 200 100" width="160" height="80">
            <rect x="40" y="15" width="120" height="70" rx="10" fill="rgba(255,255,255,.95)"/>
            <text x="50" y="28" font-size="7" fill="#5A7F54" font-weight="bold">📊 핵심 건강 지표</text>
            <rect x="50" y="34" width="32" height="22" rx="3" fill="rgba(214,183,117,.2)"/>
            <text x="66" y="44" text-anchor="middle" font-size="9" fill="#2C2A26" font-weight="bold">1.8L</text>
            <text x="66" y="53" text-anchor="middle" font-size="5" fill="#9C7E40">목표 미달</text>
            <rect x="84" y="34" width="32" height="22" rx="3" fill="rgba(229,181,176,.3)"/>
            <text x="100" y="44" text-anchor="middle" font-size="9" fill="#2C2A26" font-weight="bold">7.2/10</text>
            <text x="100" y="53" text-anchor="middle" font-size="5" fill="#C44848">관리 필요</text>
            <rect x="118" y="34" width="32" height="22" rx="3" fill="rgba(157,190,150,.25)"/>
            <text x="134" y="44" text-anchor="middle" font-size="9" fill="#2C2A26" font-weight="bold">3회</text>
            <text x="134" y="53" text-anchor="middle" font-size="5" fill="#5A7F54">감소 추세</text>
            <rect x="50" y="60" width="100" height="20" rx="3" fill="rgba(157,190,150,.1)"/>
            <text x="100" y="74" text-anchor="middle" font-size="5" fill="#5A7F54" font-style="italic">"흐름이 좋아지고 있어요"</text>
          </svg>
        </div>
        <div class="scene-phase">빛의 순간</div>
        <h3 class="scene-title">숫자 대신,<br>이야기를 받았다</h3>
        <p class="scene-text">
          "최근 3일의 거품 수준은 첫 주보다 낮아지는 흐름이에요." 처음으로 내 몸이 나에게 말을 걸었다.
        </p>
        <div class="scene-quote">"의학 용어가 아니라, 나의 언어였다."</div>
      </div>

      <div class="scene-card">
        <div class="scene-num-row">
          <span class="scene-num">SCENE / 07</span>
          <div class="scene-line"></div>
          <span class="scene-emo">⭐</span>
        </div>
        <div class="scene-illust scene-illust-7">
          <svg viewBox="0 0 200 100" width="160" height="80">
            <rect x="50" y="15" width="100" height="70" rx="10" fill="rgba(255,255,255,.95)"/>
            <rect x="76" y="22" width="48" height="11" rx="5" fill="rgba(157,190,150,.25)"/>
            <text x="100" y="30" text-anchor="middle" font-size="5" fill="#5A7F54" font-weight="bold">PREMIUM</text>
            <text x="100" y="50" text-anchor="middle" font-size="20" fill="#2C2A26" font-weight="bold" font-family="serif">2,900</text>
            <text x="100" y="60" text-anchor="middle" font-size="5" fill="#7A746C">원/월 · 광고 제거 + 프리미엄</text>
            <rect x="60" y="68" width="80" height="13" rx="6" fill="#5A7F54"/>
            <text x="100" y="77" text-anchor="middle" font-size="6" fill="white" font-weight="bold">계속 기록할게요 →</text>
          </svg>
        </div>
        <div class="scene-phase">약속의 순간</div>
        <h3 class="scene-title">2,900원,<br>나와의 약속이었다</h3>
        <p class="scene-text">
          기본형 무료에서 확장형으로. 망설임 없이 결제 버튼을 눌렀다. 광고 제거, 프리미엄 콘텐츠.
        </p>
        <div class="scene-quote">"돈을 낸 게 아니라, 나와의 약속을 한 것 같았다."</div>
      </div>

      <div class="scene-card">
        <div class="scene-num-row">
          <span class="scene-num">SCENE / 08</span>
          <div class="scene-line"></div>
          <span class="scene-emo">💜</span>
        </div>
        <div class="scene-illust scene-illust-8">
          <svg viewBox="0 0 200 100" width="160" height="80">
            <rect x="20" y="20" width="100" height="14" rx="6" fill="white"/>
            <text x="28" y="30" font-size="6" fill="#2C2A26">나 요즘 이 앱 쓰는데... 🌱</text>
            <rect x="80" y="38" width="100" height="14" rx="6" fill="rgba(157,190,150,.7)"/>
            <text x="88" y="48" font-size="6" fill="white">헐 그런 것도 있어?</text>
            <rect x="20" y="56" width="100" height="14" rx="6" fill="white"/>
            <text x="28" y="66" font-size="6" fill="#2C2A26">The Bottom Line!</text>
            <rect x="80" y="74" width="80" height="12" rx="5" fill="rgba(157,190,150,.7)"/>
            <text x="88" y="83" font-size="6" fill="white">나도 써볼래 ✨</text>
          </svg>
        </div>
        <div class="scene-phase">확산의 순간</div>
        <h3 class="scene-title">피부 관리 이야기처럼,<br>당연하게</h3>
        <p class="scene-text">
          6개월 뒤. 회사 점심에서 자연스럽게 말했다. "나 요즘 이 앱 쓰는데, 진짜 간단해."
        </p>
        <div class="scene-quote">"부끄러운 이야기가 당연한 자기 관리가 됐다."</div>
      </div>

    </div>

    <div class="journey-controls" style="padding:0 56px;">
      <div class="journey-progress-bar">
        <div class="journey-progress-fill" id="journeyProgress"></div>
      </div>
      <button class="journey-arrow" id="journeyPrev" disabled>←</button>
      <button class="journey-arrow" id="journeyNext">→</button>
    </div>
  </div>
</section>

<!-- ═══════════════ EMOTION CURVE ═══════════════ -->
<section class="section emotion-section">
  <div class="section-inner">
    <div class="section-eyebrow reveal">감정 곡선</div>
    <h2 class="section-title reveal">
      불안에서 확신까지,<br>
      <span class="section-title-italic">감정의 궤적.</span>
    </h2>
    <p class="section-desc reveal">
      8개 장면마다 이지은의 마음이 어디에 있었는지. The Bottom Line이 개입하는 정확한 지점.
    </p>

    <div class="emotion-chart reveal">
      <div class="emo-zones">
        <span class="emo-zone-tag danger">😨 위기 구간</span>
        <span class="emo-zone-tag growth">🌱 성장 구간</span>
        <span class="emo-zone-tag thrive">💜 확신 구간</span>
      </div>

      <div class="emo-svg-container">
        <svg viewBox="0 0 800 220" preserveAspectRatio="none">
          <defs>
            <linearGradient id="curveGrad" x1="0%" y1="0%" x2="100%" y2="0%">
              <stop offset="0%" style="stop-color:#A86A4E"/>
              <stop offset="22%" style="stop-color:#D6B775"/>
              <stop offset="48%" style="stop-color:#9DBE96"/>
              <stop offset="72%" style="stop-color:#5A7F54"/>
              <stop offset="100%" style="stop-color:#B8A0C8"/>
            </linearGradient>
            <linearGradient id="fillGrad" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" style="stop-color:#9DBE96;stop-opacity:.18"/>
              <stop offset="100%" style="stop-color:#9DBE96;stop-opacity:0"/>
            </linearGradient>
            <filter id="curveGlow">
              <feGaussianBlur stdDeviation="3" result="blur"/>
              <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
            </filter>
          </defs>

          <line x1="0" y1="55" x2="800" y2="55" stroke="#E4DCD0" stroke-width="1" stroke-dasharray="4,6"/>
          <line x1="0" y1="110" x2="800" y2="110" stroke="#E4DCD0" stroke-width="1" stroke-dasharray="4,6"/>
          <line x1="0" y1="165" x2="800" y2="165" stroke="#E4DCD0" stroke-width="1" stroke-dasharray="4,6"/>

          <path d="M 50 185 C 100 185 130 175 150 170
                   C 200 165 220 145 270 130
                   C 320 115 360 90 410 75
                   C 470 60 530 45 590 35
                   C 650 25 720 20 770 18 L 770 220 L 50 220 Z"
                fill="url(#fillGrad)"/>

          <path d="M 50 185 C 100 185 130 175 150 170
                   C 200 165 220 145 270 130
                   C 320 115 360 90 410 75
                   C 470 60 530 45 590 35
                   C 650 25 720 20 770 18"
                fill="none" stroke="url(#curveGrad)" stroke-width="3"
                stroke-linecap="round" filter="url(#curveGlow)"/>

          <line x1="270" y1="0" x2="270" y2="220" stroke="#5A7F54" stroke-width="1" stroke-dasharray="5,4" opacity=".5"/>
          <rect x="195" y="0" width="150" height="22" rx="4" fill="rgba(90,127,84,.1)" stroke="rgba(90,127,84,.3)"/>
          <text x="270" y="14" font-size="9.5" fill="#5A7F54" font-family="Noto Sans KR" text-anchor="middle" font-weight="700">↑ The Bottom Line 진입</text>

          <circle cx="50" cy="185" r="7" fill="#A86A4E" stroke="white" stroke-width="2.5"/>
          <circle cx="150" cy="170" r="7" fill="#C47B5A" stroke="white" stroke-width="2.5"/>
          <circle cx="270" cy="130" r="7" fill="#D6B775" stroke="white" stroke-width="2.5"/>
          <circle cx="380" cy="95" r="7" fill="#B8C46A" stroke="white" stroke-width="2.5"/>
          <circle cx="490" cy="65" r="7" fill="#9DBE96" stroke="white" stroke-width="2.5"/>
          <circle cx="590" cy="35" r="8" fill="#5A7F54" stroke="white" stroke-width="3"/>
          <circle cx="680" cy="22" r="7" fill="#85AFCC" stroke="white" stroke-width="2.5"/>
          <circle cx="770" cy="18" r="9" fill="#B8A0C8" stroke="white" stroke-width="3"/>

          <text x="50" y="208" font-size="18" text-anchor="middle">😟</text>
          <text x="150" y="195" font-size="16" text-anchor="middle">😔</text>
          <text x="270" y="155" font-size="16" text-anchor="middle">🤔</text>
          <text x="380" y="115" font-size="16" text-anchor="middle">😊</text>
          <text x="490" y="85" font-size="16" text-anchor="middle">🌱</text>
          <text x="590" y="52" font-size="18" text-anchor="middle">💚</text>
          <text x="680" y="40" font-size="16" text-anchor="middle">⭐</text>
          <text x="770" y="36" font-size="20" text-anchor="middle">💜</text>
        </svg>
      </div>

      <div class="emo-labels">
        <div class="emo-label"><div class="emo-label-step">SCENE 1</div><div class="emo-label-text">이상 발견</div></div>
        <div class="emo-label"><div class="emo-label-step">SCENE 2</div><div class="emo-label-text">검색·방치</div></div>
        <div class="emo-label"><div class="emo-label-step">SCENE 3</div><div class="emo-label-text">SNS 발견</div></div>
        <div class="emo-label"><div class="emo-label-step">SCENE 4</div><div class="emo-label-text">앱 만남</div></div>
        <div class="emo-label"><div class="emo-label-step">SCENE 5</div><div class="emo-label-text">루틴 시작</div></div>
        <div class="emo-label"><div class="emo-label-step">SCENE 6</div><div class="emo-label-text">첫 리포트</div></div>
        <div class="emo-label"><div class="emo-label-step">SCENE 7</div><div class="emo-label-text">구독 전환</div></div>
        <div class="emo-label"><div class="emo-label-step">SCENE 8</div><div class="emo-label-text">친구 추천</div></div>
      </div>

      <div class="emo-legend">
        <div class="legend-item"><div class="legend-dot" style="background:#C47B5A;"></div>위기 구간</div>
        <div class="legend-item"><div class="legend-dot" style="background:#9DBE96;"></div>성장 구간</div>
        <div class="legend-item"><div class="legend-dot" style="background:#B8A0C8;"></div>확신 구간</div>
        <div class="legend-item"><div style="width:20px;height:1px;border-top:1px dashed #5A7F54;"></div>The Bottom Line 진입</div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ FOREST GROWTH (NEW) ═══════════════ -->
<section class="section forest-section" id="service">
  <div class="section-inner">
    <div class="section-eyebrow reveal">나의 숲 · 게이미피케이션</div>
    <h2 class="forest-headline reveal">
      오늘의 <span class="marker">3초</span>가,<br>
      <em>한 그루의 나무</em>가 됩니다.
    </h2>
    <p class="section-desc reveal">
      루틴 종류별로 다른 식물이 자라며, 달성률에 따라 숲 전체의 상태가 달라집니다.
      <strong style="color:var(--ink);font-weight:500;">씨앗에서 거목까지 7단계.</strong>
    </p>

    <!-- 7단계 성장 시각화 -->
    <div class="forest-stages reveal">
      <div class="stage">
        <div class="stage-icon-wrap" data-count="0회">🟫</div>
        <div class="stage-name">씨앗</div>
        <div class="stage-en">Seed</div>
        <span class="stage-arrow">›</span>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="3회">🌱</div>
        <div class="stage-name">새순</div>
        <div class="stage-en">Sprout</div>
        <span class="stage-arrow">›</span>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="6회">🌿</div>
        <div class="stage-name">새잎</div>
        <div class="stage-en">Leaf</div>
        <span class="stage-arrow">›</span>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="9회">🪴</div>
        <div class="stage-name">묘목</div>
        <div class="stage-en">Sapling</div>
        <span class="stage-arrow">›</span>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="12회">🌷</div>
        <div class="stage-name">꽃봉오리</div>
        <div class="stage-en">Bud</div>
        <span class="stage-arrow">›</span>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="18회">🌸</div>
        <div class="stage-name">만개</div>
        <div class="stage-en">Bloom</div>
        <span class="stage-arrow">›</span>
      </div>
      <div class="stage">
        <div class="stage-icon-wrap" data-count="30회">🌳</div>
        <div class="stage-name">거목</div>
        <div class="stage-en">Forest</div>
      </div>
    </div>

    <!-- 3종 나무 카드 -->
    <div class="trees-trio">
      <div class="tree-card cherry reveal">
        <span class="tree-icon-big">🌸</span>
        <h3>벚꽃나무</h3>
        <div class="tree-purpose">식이 관리 · Nutrition</div>
        <p class="tree-desc">
          식이섬유·수분·저염 식단 루틴을 기록할수록 자랍니다.
          새잎에서 꽃봉오리, 만개까지 — 체크 기록이 쌓일수록 분홍빛이 짙어져요.
        </p>
        <div class="tree-progress-row">
          <div class="tree-progress-bar"><div class="tree-progress-fill"></div></div>
          <span class="tree-progress-text">새잎 · 6/9회</span>
        </div>
      </div>

      <div class="tree-card pine reveal">
        <span class="tree-icon-big">🌲</span>
        <h3>소나무</h3>
        <div class="tree-purpose">단백뇨 관리 · Renal</div>
        <p class="tree-desc">
          소변 거품 기록·수분 섭취·저염 루틴을 챙길수록 자랍니다.
          새순부터 거목까지 — 신장 케어 루틴의 꾸준함이 곧 나무의 굵기예요.
        </p>
        <div class="tree-progress-row">
          <div class="tree-progress-bar"><div class="tree-progress-fill"></div></div>
          <span class="tree-progress-text">묘목 · 6/9회</span>
        </div>
      </div>

      <div class="tree-card bamboo reveal">
        <span class="tree-icon-big">🫘</span>
        <h3>대나무</h3>
        <div class="tree-purpose">치질 예방 · Anal Care</div>
        <p class="tree-desc">
          좌욕·스트레칭·배변 기록(브리스톨 7단계)을 챙길수록 자랍니다.
          씨앗에서 출발해 빠르게 자라는 대나무처럼, 작은 습관이 큰 변화를 만들어요.
        </p>
        <div class="tree-progress-row">
          <div class="tree-progress-bar"><div class="tree-progress-fill"></div></div>
          <span class="tree-progress-text">씨앗 · 2/3회</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ APP TABS (5개 탭) ═══════════════ -->
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

<!-- ═══════════════ FLOW (INPUT → CORE → OUTPUT) ═══════════════ -->
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
        "피부 관리하듯, <em>하부 건강도 매일 가볍게.</em><br>
        보이지 않는 곳까지, 당신의 건강을 끌어올리다."
      </p>
    </div>
  </div>
</section>

<!-- ═══════════════ 5대 케어 솔루션 ═══════════════ -->
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
          <div class="deco-icon" style="background:rgba(214,144,111,.18);">📋</div>
          <div class="deco-text">
            <strong>맞춤형 리포트</strong>
            <span>축적 데이터 자동 생성</span>
          </div>
        </div>
        <div class="showcase-deco showcase-deco-2">
          <div class="deco-icon" style="background:rgba(157,190,150,.2);">🌸</div>
          <div class="deco-text">
            <strong>벚꽃나무 +1</strong>
            <span>새잎 → 꽃봉오리 (6회)</span>
          </div>
        </div>

        <div class="showcase-phone">
          <div class="showcase-screen">
            <div class="showcase-notch"></div>
            <div class="showcase-content">
              <div class="showcase-h">오늘의 나노 루틴</div>

              <div class="routine-mini">
                <div class="routine-mini-icon">🚶</div>
                <div class="routine-mini-info">
                  <div class="routine-mini-time">아침 루틴</div>
                  <div class="routine-mini-name">기상 후 스트레칭</div>
                  <div class="routine-mini-desc">항문 혈류 개선 5분</div>
                </div>
                <div class="routine-mini-check">✓</div>
              </div>
              <div class="routine-mini" style="background:rgba(165,194,214,.18);border-color:rgba(165,194,214,.3);">
                <div class="routine-mini-icon">🌿</div>
                <div class="routine-mini-info">
                  <div class="routine-mini-time" style="color:#5A8DAA;">점심 루틴</div>
                  <div class="routine-mini-name">식이섬유 섭취</div>
                  <div class="routine-mini-desc">채소·과일 목표량 절반</div>
                </div>
                <div class="routine-mini-check" style="background:#5A8DAA;">✓</div>
              </div>
              <div class="routine-mini" style="background:rgba(200,176,212,.2);border-color:rgba(200,176,212,.35);">
                <div class="routine-mini-icon">🪑</div>
                <div class="routine-mini-info">
                  <div class="routine-mini-time" style="color:#8B5A6A;">저녁 루틴</div>
                  <div class="routine-mini-name">좌욕 5분</div>
                  <div class="routine-mini-desc">하부 케어 루틴 유지</div>
                </div>
                <div class="routine-mini-check" style="background:#8B5A6A;">✓</div>
              </div>

              <div class="forest-status">
                <div class="forest-status-h">🌿 나만의 숲 성장 현황</div>
                <div class="forest-status-row">
                  <span class="forest-status-icon">🌿</span>
                  <div class="forest-status-info">
                    <div class="forest-status-name">벚꽃나무</div>
                    <div class="forest-status-sub">새잎 · 다음: 꽃봉오리</div>
                  </div>
                  <div class="forest-status-bar"><div style="background:var(--pink-deep);width:67%;"></div></div>
                  <span class="forest-status-count">6회</span>
                </div>
                <div class="forest-status-row">
                  <span class="forest-status-icon">🪵</span>
                  <div class="forest-status-info">
                    <div class="forest-status-name">소나무</div>
                    <div class="forest-status-sub">새순 · 다음: 묘목</div>
                  </div>
                  <div class="forest-status-bar"><div style="background:var(--sage-deep);width:67%;"></div></div>
                  <span class="forest-status-count">6회</span>
                </div>
                <div class="forest-status-row">
                  <span class="forest-status-icon">🫘</span>
                  <div class="forest-status-info">
                    <div class="forest-status-name">대나무</div>
                    <div class="forest-status-sub">씨앗 · 다음: 새싹</div>
                  </div>
                  <div class="forest-status-bar"><div style="background:var(--clay);width:30%;"></div></div>
                  <span class="forest-status-count">2회</span>
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
      소변 거품은 질병 판단 근거가 아닌 <strong style="color:var(--terra-soft);">개인 기준선 대비 변화 추이</strong>를 비교하는 기록 기능.
      국제 논문 기반의 컴퓨터 비전 기술로 신뢰도를 확보합니다.
    </p>

    <div class="tech-grid">
      <div class="tech-card reveal">
        <div class="tech-icon">🎥</div>
        <div class="tech-num">TECH / 01</div>
        <h3 class="tech-name">10초 영상 촬영 권장</h3>
        <p class="tech-desc">
          정확한 단백뇨 측정을 위해 10초 이상의 소변 영상 촬영을 권장합니다. 영상 분석 시 거품 밀도 측정 정확도가 유의미하게 향상됩니다.
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
          아침·저녁 2회 촬영이 권장됩니다. 반복 측정 데이터의 추이 예측 가능성이 ANN 기반 연구로 입증되었습니다.
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
          타임스탬프로 날짜·시간 자동 저장. U-Net과 Mask R-CNN으로 거품 검출·정량화·개별 분할까지 자동화.
        </p>
        <div class="tech-paper">
          <div class="tech-paper-label">논문 근거</div>
          <div class="tech-paper-cite">Hoseini (U-Net) · Cui (Mask R-CNN) — 거품 검출·shape reconstruction</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════ PRICING (B2C/B2B 이원화) ═══════════════ -->
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

    <!-- Closing tagline from final PPT -->
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

<!-- ═══════════════ IMPACT (8 outcomes from final PPT) ═══════════════ -->
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
      <!-- 단기 -->
      <div class="impact-track reveal">
        <div class="impact-track-header">
          <span class="impact-track-tag short">🌱 SHORT-TERM · 단기적 가치</span>
          <h3 class="impact-track-title">개인의 변화에서 시작합니다.</h3>
        </div>
        <div class="impact-grid">
          <div class="impact-card">
            <div class="impact-num">01</div>
            <h4>건강 리터러시 향상</h4>
            <p>스스로 몸의 신호를 읽고 해석하는 능력을 키웁니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">02</div>
            <h4>민감 질환 낙인 효과 완화</h4>
            <p>부끄러운 질환이라는 사회적 인식을 해체합니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">03</div>
            <h4>다이어트 부작용 예방</h4>
            <p>고단백 식단·수분 부족으로 인한 위험을 사전에 차단합니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">04</div>
            <h4>프라이버시 보호 복지</h4>
            <p>개인정보를 노출하지 않는 안전한 자기관리 환경을 제공합니다.</p>
          </div>
        </div>
      </div>

      <!-- 장기 -->
      <div class="impact-track reveal">
        <div class="impact-track-header">
          <span class="impact-track-tag long">🌳 LONG-TERM · 장기적 가치</span>
          <h3 class="impact-track-title">사회의 예방 문화로 확산됩니다.</h3>
        </div>
        <div class="impact-grid">
          <div class="impact-card">
            <div class="impact-num">05</div>
            <h4>예방 중심 문화 확산</h4>
            <p>치료에서 예방으로, 한국 헬스케어의 패러다임 전환에 기여합니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">06</div>
            <h4>건강 정보 격차 완화</h4>
            <p>학회 지침을 일상언어로 변환해 누구나 접근 가능하게 합니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">07</div>
            <h4>건강 형평성 기여</h4>
            <p>지리·경제적 의료 접근성 차이를 디지털로 보완합니다.</p>
          </div>
          <div class="impact-card">
            <div class="impact-num">08</div>
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
  <div class="cta-orb cta-orb-1"></div>
  <div class="cta-orb cta-orb-2"></div>
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
        <div class="footer-logo">The Bottom Line</div>
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
          <li><a href="#tech">기술 차별점</a></li>
          <li><a href="#">사업계획서</a></li>
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

// Emotion curve animation
const emoSvg = document.querySelector('.emo-svg-container svg');
if (emoSvg) {
  const svgIo = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        const path = emoSvg.querySelectorAll('path[stroke]')[0];
        if (path) {
          const len = path.getTotalLength();
          path.style.strokeDasharray = len;
          path.style.strokeDashoffset = len;
          path.style.transition = 'stroke-dashoffset 2.4s cubic-bezier(.2,.8,.2,1)';
          setTimeout(() => { path.style.strokeDashoffset = 0; }, 200);
        }
        emoSvg.querySelectorAll('circle').forEach((c, i) => {
          c.style.opacity = 0;
          c.style.transition = 'opacity .5s ease';
          setTimeout(() => { c.style.opacity = 1; }, 600 + i * 180);
        });
      }
    });
  }, { threshold: 0.3 });
  svgIo.observe(emoSvg);
}

// Stats counter (with K, % suffix support)
document.querySelectorAll('.stat-num').forEach(el => {
  const text = el.innerHTML;
  // Skip if no number
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
      const duration = 1500;
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
