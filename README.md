
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>Phòng Thí Nghiệm — Ghép Chất</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  .home-origin-btn{
    position:relative;
    display:flex;
    align-items:center;
    gap:12px;

    padding:10px 18px;
    margin-left:14px;

    border:none;
    border-radius:999px;

    background:
        linear-gradient(135deg,#b02b27,#8d221f);

    color:#f7eed7;
    cursor:pointer;

    font-family:'Be Vietnam Pro',sans-serif;

    box-shadow:
        0 10px 24px rgba(156,42,37,.28),
        inset 0 1px 0 rgba(255,255,255,.15);

    transition:
        transform .28s,
        box-shadow .28s,
        background .28s;
}

.home-origin-btn::before{
    content:"";
    position:absolute;
    inset:2px;
    border-radius:999px;
    border:1px solid rgba(255,215,120,.45);
    pointer-events:none;
}

.home-origin-btn:hover{
    transform:translateY(-3px);
    background:linear-gradient(135deg,#c53a35,#a42a25);
    box-shadow:
        0 16px 32px rgba(156,42,37,.4),
        inset 0 1px 0 rgba(255,255,255,.2);
}

.home-origin-btn:active{
    transform:scale(.96);
}

.btn-icon{
    width:42px;
    height:42px;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;

    background:
        radial-gradient(circle,#e8c574,#e5c88c);

    color:#2d2118;
    font-size:22px;

    box-shadow:
        inset 0 2px 5px rgba(255,255,255,.3),
        0 5px 10px rgba(0,0,0,.18);
}

.btn-text{
    display:flex;
    flex-direction:column;
    line-height:1.1;
    text-align:left;
}

.btn-text small{
    font-size:9px;
    letter-spacing:.35em;
    opacity:.75;
    font-weight:700;
}

.btn-text strong{
    font-size:15px;
    font-weight:700;
    font-family:'Cormorant Garamond',serif;
    letter-spacing:.05em;
}

@media(max-width:768px){

    .home-origin-btn{
        padding:10px;
        border-radius:50%;
        width:52px;
        height:52px;
        justify-content:center;
        margin-left:8px;
    }

    .btn-text{
        display:none;
    }

    .btn-icon{
        width:36px;
        height:36px;
        font-size:20px;
    }
}
:root{
  /* Màu nền */
  --bg:#f6efe2;          /* nền be */
  --panel:#fffaf2;       /* panel sáng */
  --panel2:#f4ead8;      /* panel phụ */
  --line:#d9c6a6;        /* đường viền */

  /* Chữ */
  --ink:#3a2418;         /* nâu đậm */
  --dim:#8b6b56;         /* nâu nhạt */

  /* Màu chủ đạo */
  --phos:#b02b27;        /* đỏ KOIFISH */
  --phos-dim:#f6efe6;    /* đỏ đậm */

  /* Các màu phụ */
  --amber:#d19b45;       /* vàng be */
  --red:#cf3c38;
  --violet:#8d4d79;
  --cyan:#8f5b46;
  --slate:#8b7566;
  --sand:#d7b987;
}
*{box-sizing:border-box;}
html,body{margin:0;padding:0;}
body{
  background:
      radial-gradient(circle at top left,
      rgba(176,43,39,.12), transparent 45%),
      radial-gradient(circle at bottom right,
      rgba(209,155,69,.12), transparent 40%),
      var(--bg);

  color:var(--ink);
  font-family:'Space Grotesk',sans-serif;
}
::selection{background:var(--phos-dim);}
.wrap{max-width:1400px;margin:0 auto;padding:20px 22px 60px;}

/* header */
header{display:flex;align-items:flex-end;justify-content:space-between;flex-wrap:wrap;gap:14px;padding-bottom:18px;border-bottom:1px solid var(--line);margin-bottom:18px;}
.brand{display:flex;align-items:center;gap:14px;}
.flaskmark{width:44px;height:44px;flex-shrink:0;}
h1{font-size:1.5rem;margin:0;font-weight:700;letter-spacing:.2px;}
h1 span{color:var(--phos);}
.sub{color:var(--dim);font-size:.82rem;margin-top:2px;}
.stats{display:flex;gap:22px;font-family:'JetBrains Mono',monospace;font-size:.78rem;color:var(--dim);}
.stats b{color:var(--phos);font-size:1.05rem;display:block;font-family:'Space Grotesk',sans-serif;font-weight:700;}

/* layout */
.grid{display:grid;grid-template-columns:1.3fr 1fr;gap:20px;}
@media(max-width:980px){.grid{grid-template-columns:1fr;}}

.panel{background:linear-gradient(180deg,var(--panel),var(--panel2));border:1px solid var(--line);border-radius:14px;padding:16px;}
.panel h2{font-size:.72rem;text-transform:uppercase;letter-spacing:1.5px;color:var(--dim);margin:0 0 12px;font-weight:600;}

/* tabs */
.tabs{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:12px;}
.tab{background:transparent;border:1px solid var(--line);color:var(--dim);font-family:'JetBrains Mono',monospace;font-size:.7rem;padding:5px 10px;border-radius:20px;cursor:pointer;transition:.15s;}
.tab.active{background:var(--phos-dim);border-color:var(--phos);color:var(--ink);}
.tab:hover{border-color:var(--phos);}

.searchbox{width:100%;background:var(--bg);border:1px solid var(--line);border-radius:8px;color:var(--ink);padding:8px 10px;font-family:'JetBrains Mono',monospace;font-size:.8rem;margin-bottom:12px;}
.searchbox:focus{outline:none;border-color:var(--phos);}

.tiles{display:grid;grid-template-columns:repeat(auto-fill,minmax(84px,1fr));gap:8px;max-height:520px;overflow-y:auto;padding-right:4px;}
.tiles::-webkit-scrollbar{width:6px;}
.tiles::-webkit-scrollbar-thumb{background:var(--line);border-radius:3px;}

.tile{background:var(--bg);border:1px solid var(--line);border-radius:10px;padding:8px 6px;text-align:center;cursor:pointer;transition:.12s;position:relative;overflow:hidden;}
.tile:hover{transform:translateY(-2px);  border-color:#b02b27;
    box-shadow:0 6px 18px rgba(176,43,39,.18)}
.tile .f{font-family:'JetBrains Mono',monospace;font-size:.86rem;font-weight:700;display:block;}
.tile .n{font-size:.6rem;color:var(--dim);display:block;margin-top:2px;line-height:1.15;}
.tile .catbar{position:absolute;top:0;left:0;right:0;height:3px;}

.locked{opacity:.16;filter:grayscale(1);cursor:not-allowed;}
.locked:hover{transform:none;box-shadow:none;border-color:var(--line);}

/* category colors */
.c-element .catbar{background:#a65c39;}
.c-element .f{color:#a65c39;}
.c-oxide .catbar{background:var(--amber);} .c-oxide .f{color:var(--amber);}
.c-base .catbar{background:#b02b27;}
.c-base .f{color:#b02b27;}
.c-acid .catbar{background:var(--red);} .c-acid .f{color:var(--red);}
.c-salt .catbar{background:var(--sand);} .c-salt .f{color:var(--sand);}
.c-organic .catbar{background:var(--violet);} .c-organic .f{color:var(--violet);}
.c-other .catbar{background:var(--slate);} .c-other .f{color:var(--slate);}

/* flask panel */
.flaskzone{min-height:110px;      background:#fffaf5;  border:2px dashed #c8aa86;;border-radius:10px;padding:12px;display:flex;flex-wrap:wrap;gap:8px;align-content:flex-start;margin-bottom:12px;}
.flaskzone.empty::before{content:"Chọn chất ở bên trái để thêm vào bình phản ứng…";color:var(--dim);font-size:.78rem;font-style:italic;}
.chip{background:var(--panel2);border:1px solid var(--phos-dim);border-radius:20px;padding:6px 12px 6px 12px;font-family:'JetBrains Mono',monospace;font-size:.82rem;display:flex;align-items:center;gap:8px;cursor:pointer;}
.chip:hover{border-color:var(--red);}
.chip .x{color:var(--dim);font-size:.7rem;}

.actions{display:flex;gap:10px;margin-bottom:16px;}
.btn{flex:1;    background:#b02b27;
    color:#fffaf2;;border:none;border-radius:8px;padding:12px;font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:.88rem;cursor:pointer;letter-spacing:.3px;transition:.15s;}
.btn:hover{   background:#c53a35;}
.btn:disabled{background:var(--line);color:var(--dim);cursor:not-allowed;}
.btn.ghost{background:transparent;border:1px solid var(--line);color:var(--dim);flex:0 0 auto;padding:12px 16px;}
.btn.ghost:hover{border-color:var(--red);color:var(--red);}

/* result / log */
.result{border-radius:10px;padding:14px;margin-bottom:12px;font-family:'JetBrains Mono',monospace;}
.result.ok{
    background:#fff4ef;
    border:1px solid #c53a35;
}

.result.ok .eqline{
    color:#b02b27;
}

.result.no{
    background:#f9ece6;
    border:1px solid #cf3c38;
}

.result.no .eqline{
    color:#cf3c38;
}
.result .eqline{font-size:1.05rem;font-weight:700;color:var(--phos);margin-bottom:4px;word-break:break-word;}
.result.no .eqline{color:var(--red);font-weight:400;font-style:italic;font-size:.85rem;}
.result .cond{color:var(--amber);font-size:.72rem;}
.result .unlockline{color:var(--sand);font-size:.75rem;margin-top:6px;}

.log{max-height:300px;overflow-y:auto;display:flex;flex-direction:column-reverse;gap:8px;}
.logitem{border-left:2px solid var(--phos-dim);padding:6px 0 6px 10px;font-family:'JetBrains Mono',monospace;font-size:.76rem;color:var(--dim);}
.logitem b{color:var(--ink);display:block;font-size:.82rem;margin-bottom:2px;}
.logitem .lcond{color:var(--amber);}

footer{margin-top:26px;color:var(--dim);font-size:.72rem;text-align:center;line-height:1.7;}
footer b{color:var(--phos);}

/* =========================================================
   KOI LAB — VISUAL REDESIGN LAYER
   Chỉnh màu nhanh tại :root; không thay đổi logic JavaScript.
   ========================================================= */
:root{
  --bg:#f4eee3;
  --panel:#fffdf8;
  --panel2:#f8f1e6;
  --line:#dfd1bd;
  --ink:#211c19;
  --dim:#827466;
  --phos:#b52a32;
  --phos-dim:#f8e6df;
  --amber:#c58a37;
  --red:#d34a40;
  --violet:#87618c;
  --cyan:#497f7b;
  --slate:#8b8176;
  --sand:#d7b987;
  --radius-xl:26px;
  --radius-lg:19px;
  --radius-md:13px;
  --shadow-soft:0 18px 50px rgba(66,43,28,.08);
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  min-height:100vh;
  color:var(--ink);
  font-family:'Space Grotesk',sans-serif;
  background:
    radial-gradient(ellipse at 8% 2%,rgba(181,42,50,.11),transparent 30rem),
    radial-gradient(ellipse at 95% 42%,rgba(197,138,55,.13),transparent 28rem),
    linear-gradient(135deg,#f7f1e7 0%,#efe5d5 100%);
}
body::before{
  content:"";position:fixed;inset:0;pointer-events:none;z-index:-1;opacity:.24;
  background-image:radial-gradient(#8b715a .65px,transparent .65px);
  background-size:15px 15px;
}
.wrap{max-width:1480px;padding:22px 28px 64px;margin:0 auto}
.topbar{
  max-width:1480px;margin:0 auto;padding:22px 28px 0;
  display:flex;align-items:center;justify-content:flex-start;
}
.home-origin-btn{
  margin:0;padding:8px 17px 8px 9px;gap:11px;
  border:1px solid rgba(255,255,255,.14);border-radius:999px;
  background:#211c19;color:#fff8ec;box-shadow:0 8px 24px rgba(33,28,25,.15);
  transition:transform .22s ease,box-shadow .22s ease;
}
.home-origin-btn:hover{transform:translateY(-2px);background:#332622;box-shadow:0 13px 30px rgba(33,28,25,.2)}
.home-origin-btn::before{border-color:rgba(232,192,115,.48)}
.btn-icon{width:36px;height:36px;background:linear-gradient(145deg,#e8c879,#c78c3c);font-size:18px}
.btn-icon::before{content:"⌂";font-weight:700}
.btn-text small{font-family:'JetBrains Mono',monospace;font-size:8px;letter-spacing:.22em}
.btn-text strong{font-size:16px}
header:not(.topbar){
  position:relative;overflow:hidden;align-items:center;gap:24px;
  padding:30px 32px;margin:0 0 24px;
  border:1px solid rgba(255,255,255,.12);border-radius:var(--radius-xl);
  background:#211c19;color:#fff7eb;
  box-shadow:0 20px 48px rgba(48,32,22,.16);
}
header:not(.topbar)::after{
  content:"";position:absolute;width:300px;height:300px;right:14%;top:-190px;
  border:1px solid rgba(229,190,115,.28);border-radius:50%;
  box-shadow:0 0 0 26px rgba(229,190,115,.035),0 0 0 55px rgba(229,190,115,.025);
  pointer-events:none;
}
.brand{position:relative;z-index:1;gap:18px}
.flaskmark{width:58px;height:58px;padding:8px;border-radius:17px;background:#f5e8d5}
h1{font-size:clamp(1.45rem,2.5vw,2.15rem);line-height:1.1;letter-spacing:-.045em}
h1 span{color:#e8b75f}
.sub{max-width:650px;color:#c8b9a7;font-size:.88rem;line-height:1.65;margin-top:9px}
.stats{position:relative;z-index:1;gap:12px;color:#c8b9a7}
.stats>div{min-width:126px;padding:13px 16px;border:1px solid rgba(255,255,255,.14);border-radius:15px;background:rgba(255,255,255,.045)}
.stats b{font-size:1.45rem;color:#efbd66;margin-top:5px}
.grid{grid-template-columns:minmax(0,1.12fr) minmax(360px,.88fr);gap:22px;align-items:start}
.panel{
  padding:22px;border:1px solid rgba(137,105,72,.18);border-radius:var(--radius-xl);
  background:rgba(255,253,248,.88);box-shadow:var(--shadow-soft);
  backdrop-filter:blur(8px);
}
.panel h2{display:flex;align-items:center;gap:10px;margin:0 0 17px;color:#6f5c4c;font-size:.72rem;letter-spacing:.16em}
.panel h2::before{content:"";width:7px;height:7px;border-radius:2px;background:var(--phos);transform:rotate(45deg)}
.searchbox{
  padding:14px 16px;border:1px solid #e0d2bf;border-radius:13px;background:#f8f2e8;
  font-family:'Space Grotesk',sans-serif;font-size:.88rem;transition:border-color .2s,box-shadow .2s;
}
.searchbox:focus{border-color:var(--phos);box-shadow:0 0 0 4px rgba(181,42,50,.09)}
.tabs{gap:7px;margin-bottom:16px}
.tab{
  padding:8px 12px;border:1px solid #e3d6c4;border-radius:999px;background:#fffaf2;
  color:#796b5d;font-family:'Space Grotesk',sans-serif;font-size:.74rem;font-weight:600;
  transition:all .18s ease;
}
.tab:hover{transform:translateY(-1px);border-color:var(--phos)}
.tab.active{background:#29211d;color:#fff7eb;border-color:#29211d;box-shadow:0 5px 12px #29211d1c}
.tiles{grid-template-columns:repeat(auto-fill,minmax(94px,1fr));gap:10px;max-height:600px;padding:2px 5px 5px 0}
.tiles::-webkit-scrollbar{width:7px}
.tiles::-webkit-scrollbar-thumb{background:#d8c5ac;border-radius:10px}
.tile{
  min-height:88px;display:flex;flex-direction:column;align-items:center;justify-content:center;
  padding:13px 7px 10px;border:1px solid #e8dccb;border-radius:15px;background:#fffdf8;
  box-shadow:0 3px 0 rgba(88,59,37,.025);transition:transform .2s ease,border-color .2s,box-shadow .2s;
}
.tile:hover{transform:translateY(-4px);border-color:#c75a4d;box-shadow:0 12px 22px rgba(142,58,43,.12)}
.tile .catbar{height:4px}
.tile .f{font-size:.96rem;color:var(--ink);margin-bottom:4px}
.tile .n{font-size:.64rem;color:#897969;line-height:1.3}
.c-element .catbar{background:#b67844}.c-element .f{color:#a96836}
.c-oxide .catbar{background:#d2a24e}.c-oxide .f{color:#b17b24}
.c-base .catbar{background:#b52a32}.c-base .f{color:#b52a32}
.c-acid .catbar{background:#d34a40}.c-acid .f{color:#c13e35}
.c-salt .catbar{background:#8e9a78}.c-salt .f{color:#64754f}
.c-organic .catbar{background:#87618c}.c-organic .f{color:#805786}
.c-polymer .catbar{background:#497f7b}.c-polymer .f{color:#39716d}
.c-other .catbar{background:#8b8176}.c-other .f{color:#766b60}
.locked{opacity:.25;filter:grayscale(.7)}
.flaskzone{
  min-height:150px;padding:16px;border:1px dashed #c9b49a;border-radius:17px;
  background:linear-gradient(135deg,#faf4e9,#fffdf8);
  gap:9px;align-content:flex-start;position:relative;
}
.flaskzone.empty::before{content:"Thả các chất vào bình để bắt đầu khám phá…";font-size:.82rem;color:#a08c77;font-style:normal}
.chip{
  padding:9px 13px;border:1px solid #e8d3c1;border-radius:999px;background:#fff;
  box-shadow:0 4px 10px rgba(72,48,31,.05);font-size:.83rem;transition:all .16s;
}
.chip:hover{transform:translateY(-1px);border-color:var(--phos);background:#fff7f2}
.chip .x{font-size:.8rem;color:#b52a32}
.actions{gap:10px;margin:15px 0 18px}
.btn{
  min-height:48px;border-radius:13px;background:linear-gradient(135deg,#bd3438,#98242c);
  box-shadow:0 8px 18px rgba(181,42,50,.18);font-size:.86rem;transition:transform .18s,box-shadow .18s,filter .18s;
}
.btn:hover{background:linear-gradient(135deg,#ce4547,#a52a32);transform:translateY(-2px);box-shadow:0 12px 22px rgba(181,42,50,.23)}
.btn:active{transform:translateY(0)}
.btn:disabled{box-shadow:none}
.btn.ghost{border:1px solid #dfd0bd;background:#fffaf2;color:#786757;box-shadow:none}
.btn.ghost:hover{border-color:#b52a32;color:#b52a32;background:#fff3ed}
.result{padding:17px;border-radius:16px;font-family:'Space Grotesk',sans-serif;animation:resultIn .25s ease both}
.result.ok{background:linear-gradient(135deg,#fff3e8,#fffaf2);border:1px solid #e7c6a6}
.result.no{background:#fff0eb;border:1px solid #e9c4ba}
.result .eqline{font-size:1.02rem;line-height:1.65;color:#a72b32}
.result.no .eqline{font-size:.88rem;color:#b8473f}
.result .cond{margin-top:7px;color:#8b6a3f;font-size:.78rem}
.result .unlockline{margin-top:10px;color:#54754f;font-size:.77rem;line-height:1.6}
.log{max-height:330px;gap:9px}
.logitem{padding:11px 12px;border-left:3px solid #d8aa66;border-radius:0 12px 12px 0;background:#faf4e9;font-size:.76rem;line-height:1.55}
.logitem b{font-size:.81rem;line-height:1.55;color:#332720}
.logitem .lcond{display:inline-block;margin-top:4px;color:#9b7748}
footer{margin-top:30px;padding:20px 24px;border:1px solid #e1d1bd;border-radius:18px;background:rgba(255,250,242,.72);color:#897866;font-size:.76rem}
footer b{color:#b52a32}
@keyframes resultIn{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:translateY(0)}}
@media(max-width:980px){
  .wrap{padding:18px 18px 44px}
  .topbar{padding:18px 18px 0}
  .grid{grid-template-columns:1fr}
  header:not(.topbar){padding:25px}
}
@media(max-width:600px){
  .wrap{padding:13px 12px 32px}
  .topbar{padding:13px 12px 0}
  header:not(.topbar){padding:21px 17px;border-radius:21px;align-items:flex-start}
  .brand{align-items:flex-start;gap:12px}
  .flaskmark{width:45px;height:45px;padding:5px;border-radius:13px}
  h1{font-size:1.35rem}
  .sub{font-size:.78rem}
  .stats{width:100%;gap:8px}
  .stats>div{flex:1;min-width:0;padding:10px 11px;font-size:.65rem}
  .stats b{font-size:1.15rem}
  .panel{padding:16px;border-radius:20px}
  .tiles{grid-template-columns:repeat(auto-fill,minmax(78px,1fr));gap:8px;max-height:470px}
  .tile{min-height:79px;border-radius:12px}
  .tile .f{font-size:.88rem}
  .tile .n{font-size:.59rem}
  .actions{flex-wrap:wrap}
  .actions .btn{flex:1 1 100%}
  .actions .btn.ghost{flex:1 1 100%}
  .home-origin-btn{width:48px;height:48px;padding:6px;justify-content:center}
  .btn-icon{width:34px;height:34px}
}
@media(prefers-reduced-motion:reduce){
  *,*::before,*::after{scroll-behavior:auto!important;animation-duration:.01ms!important;transition-duration:.01ms!important}
}


/* ===== VISUAL SYSTEM 2.0 — editorial science journal ===== */
:root{
  --paper:#f4ead8; --paper-light:#fffaf0; --red-950:#3a1718; --red-800:#702126;
  --red-700:#9e2630; --red-500:#c64843; --gold:#d5aa62; --olive:#777e60;
  --shadow-lift:0 18px 46px rgba(57,31,21,.09);
}
body{background:linear-gradient(135deg,#f8f1e6 0%,#f0e3d0 58%,#f7eee1 100%)}
body::before{opacity:.16;background-size:18px 18px;background-image:radial-gradient(#9b7c60 .7px,transparent .7px)}
.wrap{max-width:1520px}
header:not(.topbar){isolation:isolate;background:linear-gradient(112deg,#241b18 0%,#3c2020 66%,#6e292b 100%);border:1px solid rgba(238,205,151,.2);box-shadow:0 24px 65px rgba(66,29,24,.19);min-height:204px}
header:not(.topbar)::before{content:"";position:absolute;z-index:-1;right:8%;top:50%;width:245px;height:245px;transform:translateY(-50%);border:1px solid rgba(231,195,128,.35);border-radius:50%;box-shadow:0 0 0 22px rgba(231,195,128,.035),0 0 0 48px rgba(231,195,128,.035),0 0 0 78px rgba(231,195,128,.025)}
header:not(.topbar)::after{right:calc(8% + 71px);top:calc(50% - 75px);width:95px;height:95px;border-color:rgba(231,195,128,.5);box-shadow:0 0 0 19px rgba(231,195,128,.05),0 0 0 43px rgba(231,195,128,.035)}
header:not(.topbar) .brand{max-width:760px}
header:not(.topbar) .brand::after{content:"KOI LAB  /  CHEMISTRY × NUCLEAR STUDIES";display:block;position:absolute;left:76px;bottom:-28px;color:#c7a879;font:600 .61rem 'JetBrains Mono',monospace;letter-spacing:.18em;opacity:.85}
.flaskmark{box-shadow:0 9px 24px rgba(0,0,0,.12)}
h1{letter-spacing:-.055em}
h1 span{color:#edc67f}
.stats>div{backdrop-filter:blur(4px);border-color:rgba(240,210,166,.15)}
.mode-strip{display:flex;justify-content:space-between;align-items:center;gap:18px;padding:18px 20px;margin:0 0 9px;border:1px solid #decbb1;border-radius:22px;background:rgba(255,250,241,.84);box-shadow:0 10px 30px rgba(57,31,21,.04)}
.mode-copy{display:flex;flex-direction:column;gap:4px;min-width:0}
.eyebrow{font:700 .62rem 'JetBrains Mono',monospace;letter-spacing:.16em;color:#a16f4c}
.mode-copy strong{font-size:1.05rem;letter-spacing:-.03em;color:#30241e}
.mode-copy>span:last-child{font-size:.78rem;color:#857464;line-height:1.5}
.mode-switch{display:flex;gap:7px;padding:5px;background:#f0e5d4;border:1px solid #e3d0b7;border-radius:16px;flex-shrink:0}
.mode-button{display:flex;align-items:center;gap:9px;border:1px solid transparent;background:transparent;color:#776756;border-radius:12px;padding:11px 15px;font:700 .78rem 'Space Grotesk',sans-serif;cursor:pointer;transition:all .2s ease}
.mode-button:hover{color:#9e2630;background:#fffaf1}
.mode-button.active{background:#a92b32;color:#fff8ed;box-shadow:0 6px 15px rgba(158,38,48,.2)}
.mode-button .mode-icon{font-size:1.05rem;line-height:1}
.mode-disclaimer{display:flex;align-items:center;gap:9px;margin:0 0 20px;padding:8px 13px;color:#907d67;font:500 .68rem 'JetBrains Mono',monospace;letter-spacing:.01em}
.disclaimer-dot{width:7px;height:7px;border-radius:50%;background:#c39b55;box-shadow:0 0 0 4px rgba(195,155,85,.13);flex-shrink:0}
.grid{gap:20px}
.panel{box-shadow:0 14px 40px rgba(57,31,21,.06);border-color:#e6d7c3}
.panel h2{letter-spacing:.13em}
.inventory-meta{display:flex;align-items:center;justify-content:space-between;gap:10px;margin:-7px 0 13px;color:#9a8772;font-size:.68rem}
.inventory-help{display:inline-flex;align-items:center;gap:5px;color:#ad3a3c;font-weight:700}
.inventory-help::before{content:"＋";font-size:.85rem}
.searchbox{margin-bottom:14px}
.tiles{max-height:620px;scrollbar-gutter:stable}
.tile{position:relative}
.tile::after{content:"↗";position:absolute;right:7px;bottom:5px;font:600 .63rem 'JetBrains Mono',monospace;color:#cdbca5;opacity:0;transform:translate(-2px,2px);transition:all .18s}
.tile:hover::after{opacity:1;transform:translate(0,0)}
.tile.locked::after{content:"·";opacity:.6}
.c-nuclear .catbar{background:linear-gradient(90deg,#9f2630,#e2ae58)}
.c-nuclear .f{color:#9f2630}
.c-nuclear .tile{background:linear-gradient(155deg,#fff9ee,#f8eadb)}
.locked{opacity:.24}
.bench-label{display:flex;align-items:center;gap:8px;margin:-4px 0 12px;padding:8px 10px;border-radius:10px;background:#f4ead9;color:#8b7661;font:600 .62rem 'JetBrains Mono',monospace;letter-spacing:.08em}
.bench-led{width:7px;height:7px;border-radius:50%;background:#7f9b6b;box-shadow:0 0 0 4px rgba(127,155,107,.14)}
.bench-status{margin-left:auto;padding:4px 7px;border-radius:5px;background:#fffaf1;color:#8c7354;font-size:.56rem}
.flaskzone{background:radial-gradient(ellipse at 50% 0%,#fffdf8,#f7eddd);border-style:dashed;border-width:1.5px}
.flaskzone:not(.empty){border-color:#ca9b86;box-shadow:inset 0 0 0 4px rgba(190,135,94,.035)}
.chip{font-weight:600}
.chip .f{font-size:.88rem}
.chip-nuclear{border-color:#d7a6a0;background:#fff4ee}
.result.ok{background:linear-gradient(145deg,#fff6ed,#fffaf4);border-color:#e8c5a3}
.result.ok .eqline{color:#9d252e}
.result.nuclear-result{background:radial-gradient(circle at 100% 0%,rgba(214,170,98,.14),transparent 13rem),linear-gradient(135deg,#fff2e7,#fffaf1);border-color:#d7a35e}
.result.nuclear-result::before{content:"NUCLEAR EVENT / MÔ PHỎNG";display:block;margin-bottom:10px;color:#9f2630;font:700 .6rem 'JetBrains Mono',monospace;letter-spacing:.16em}
.result .nuclear-note{margin-top:10px;color:#7c6b58;font-size:.78rem;line-height:1.6}
.logitem.nuclear-entry{border-left-color:#a72b32;background:linear-gradient(90deg,#fff1e4,#faf4e9)}
footer{box-shadow:0 10px 26px rgba(57,31,21,.035)}
body[data-mode="nuclear"] .bench-led{background:#c94c43;box-shadow:0 0 0 4px rgba(201,76,67,.15)}
body[data-mode="nuclear"] .mode-disclaimer{color:#9e5550}
body[data-mode="nuclear"] .disclaimer-dot{background:#b52a32;box-shadow:0 0 0 4px rgba(181,42,50,.12)}
@media(max-width:700px){
 .mode-strip{align-items:stretch;flex-direction:column;padding:16px;border-radius:18px}
 .mode-switch{width:100%}
 .mode-button{flex:1;justify-content:center;padding:11px 8px}
 .mode-copy strong{font-size:1rem}
 .mode-disclaimer{align-items:flex-start;line-height:1.55}
 header:not(.topbar)::before{right:-95px;opacity:.6}
 header:not(.topbar)::after{right:-24px;opacity:.55}
 header:not(.topbar) .brand::after{left:58px;bottom:-25px;font-size:.48rem;letter-spacing:.08em}
}


/* ===== BẢNG TUẦN HOÀN TƯƠNG TÁC ===== */
.tiles.periodic-grid{
  display:grid;grid-template-columns:repeat(18,minmax(31px,1fr));grid-auto-rows:76px;
  grid-auto-flow:row;gap:4px;min-width:700px;max-height:620px;overflow:auto;
  align-content:start;padding:5px 5px 10px 2px;scrollbar-gutter:stable;
}
.periodic-cell{min-width:0;min-height:0;height:76px;padding:7px 2px 4px;border-radius:9px;overflow:hidden;justify-content:flex-end;position:relative}
.periodic-cell .atomic-number{position:absolute;top:4px;left:5px;font:500 .52rem 'JetBrains Mono',monospace;color:#9f8a70;display:block}
.periodic-cell .f{font-size:.82rem;margin:0 0 3px;line-height:1.15}
.periodic-cell .n{display:block;font-size:.46rem;line-height:1.08;max-height:20px;overflow:hidden;overflow-wrap:anywhere}
.periodic-cell .catbar{display:none}
.periodic-cell::after{display:none}
.pt-alkali{background:#f8e3d9;border-color:#e8beb0}.pt-alkali .f{color:#a73b31}
.pt-alkaline{background:#f8ecd4;border-color:#e5cf9c}.pt-alkaline .f{color:#a47b29}
.pt-transition{background:#f7e6e3;border-color:#e6c4be}.pt-transition .f{color:#a23a3d}
.pt-post{background:#e9ece0;border-color:#cdd6b7}.pt-post .f{color:#5c704b}
.pt-metalloid{background:#e9e3ef;border-color:#cec0df}.pt-metalloid .f{color:#785890}
.pt-nonmetal{background:#e2eee9;border-color:#bedbd0}.pt-nonmetal .f{color:#357766}
.pt-halogen{background:#f1e1ec;border-color:#dfc2d8}.pt-halogen .f{color:#99558d}
.pt-noble{background:#e4e9f3;border-color:#c4d0e6}.pt-noble .f{color:#526a9b}
.pt-lanthanoid{background:#f8e8d2;border-color:#e4c9a0}.pt-lanthanoid .f{color:#a56d31}
.pt-actinoid{background:#f3dfdb;border-color:#dfb9b3}.pt-actinoid .f{color:#9f3437}
@media(max-width:700px){.tiles.periodic-grid{min-width:690px;grid-auto-rows:68px}.periodic-cell{height:68px}.periodic-cell .f{font-size:.75rem}}


/* KOI LAB · APP SHELL — bố cục ngang cố định, không cuộn trang */


/* =========================================================
   KOI LAB · APP SHELL
   Bố cục ngang cố định, không cuộn trang; chỉ vùng dữ liệu tự cuộn.
   ========================================================= */
:root{
  --lab-bg:#f3ecdf;
  --lab-paper:#fffaf2;
  --lab-ink:#2b211c;
  --lab-muted:#877565;
  --lab-red:#ad2932;
  --lab-red-dark:#79202a;
  --lab-gold:#c69a58;
  --lab-line:#dfcfb8;
  --lab-topbar:52px;
}
html,body{
  width:100%;
  height:100%;
  min-width:0;
  min-height:0;
  margin:0;
  overflow:hidden !important;
}
html{scroll-behavior:auto}
body{
  display:flex;
  flex-direction:column;
  overscroll-behavior:none;
  background:
    radial-gradient(ellipse at 8% 0%,rgba(173,41,50,.10),transparent 32%),
    radial-gradient(ellipse at 96% 92%,rgba(198,154,88,.13),transparent 28%),
    linear-gradient(135deg,#f8f2e8 0%,#eee2d0 100%);
}
.topbar{
  width:100%;
  max-width:none;
  height:var(--lab-topbar);
  min-height:var(--lab-topbar);
  flex:0 0 var(--lab-topbar);
  margin:0;
  padding:6px 18px;
  display:flex;
  align-items:center;
  justify-content:flex-start;
  box-sizing:border-box;
}
.home-origin-btn{
  min-height:40px;
  margin:0;
  padding:4px 15px 4px 6px;
  gap:9px;
  border:1px solid rgba(255,255,255,.12);
  border-radius:999px;
  background:linear-gradient(135deg,#30241f,#1f1917);
  color:#fff8ed;
  box-shadow:0 5px 16px rgba(51,30,22,.12);
}
.home-origin-btn:hover{transform:translateY(-1px);background:#3b2823}
.home-origin-btn .btn-icon{
  width:31px;height:31px;
  display:grid;place-items:center;
  border-radius:50%;
  background:linear-gradient(145deg,#efd69c,#c48d43);
  color:#38251c;
}
.home-origin-btn .btn-icon::before{content:"⌂";font-size:18px;font-weight:700}
.home-origin-btn .btn-text{display:flex}
.home-origin-btn .btn-text small{font-size:8px;letter-spacing:.16em}
.home-origin-btn .btn-text strong{font-size:14px}
.wrap{
  width:100%;
  max-width:none;
  height:calc(100dvh - var(--lab-topbar));
  min-height:0;
  flex:1 1 auto;
  margin:0;
  padding:8px 18px 12px;
  display:grid;
  grid-template-rows:minmax(86px,auto) auto auto minmax(0,1fr);
  gap:8px;
  overflow:hidden;
}
.wrap>header:not(.topbar){
  min-height:86px;
  margin:0;
  padding:15px 24px;
  border-radius:20px;
  align-items:center;
  gap:18px;
  overflow:hidden;
}
.wrap>header:not(.topbar)::before{
  right:8%;
  width:205px;
  height:205px;
}
.wrap>header:not(.topbar)::after{
  right:calc(8% + 57px);
  top:calc(50% - 48px);
  width:82px;height:82px;
}
.brand{gap:13px;min-width:0}
.flaskmark{width:48px;height:48px;padding:6px;border-radius:13px}
h1{font-size:clamp(1.2rem,2vw,1.8rem);letter-spacing:-.04em}
.sub{margin-top:5px;font-size:.76rem;line-height:1.35}
.wrap>header:not(.topbar) .brand::after{
  left:61px;bottom:-19px;font-size:.48rem;letter-spacing:.13em;
}
.stats{gap:8px}
.stats>div{
  min-width:104px;
  padding:9px 12px;
  border-radius:12px;
  font-size:.64rem;
}
.stats b{font-size:1.15rem;margin-top:2px}
.mode-strip{
  min-height:58px;
  padding:9px 14px;
  margin:0;
  border-radius:15px;
  gap:14px;
}
.mode-copy{gap:2px}
.eyebrow{font-size:.55rem}
.mode-copy strong{font-size:.92rem}
.mode-copy>span:last-child{font-size:.68rem;line-height:1.3}
.mode-switch{padding:3px;gap:4px;border-radius:12px}
.mode-button{padding:8px 12px;border-radius:9px;font-size:.7rem;gap:7px}
.mode-button .mode-icon{font-size:.9rem}
.mode-disclaimer{
  min-height:14px;
  margin:0;
  padding:0 5px;
  font-size:.58rem;
  line-height:1.25;
}
.disclaimer-dot{width:6px;height:6px}
.grid{
  height:100%;
  min-height:0;
  grid-template-columns:minmax(0,1.02fr) minmax(0,.98fr);
  gap:14px;
  align-items:stretch;
  overflow:hidden;
}
.grid>.panel,.grid>div:last-child{
  min-width:0;
  min-height:0;
}
.grid>.panel{
  display:flex;
  flex-direction:column;
  overflow:hidden;
  padding:12px;
  border-radius:16px;
}
.grid>div:last-child{
  display:grid;
  grid-template-rows:minmax(0,1.13fr) minmax(0,.87fr);
  gap:12px;
}
.grid>div:last-child>.panel{
  display:flex;
  flex-direction:column;
  min-height:0;
  min-width:0;
  margin:0 !important;
  padding:12px;
  border-radius:16px;
  overflow:hidden;
}
.panel h2{
  flex:0 0 auto;
  margin:0 0 10px;
  font-size:.63rem;
  letter-spacing:.12em;
}
.panel h2::before{width:6px;height:6px}
.inventory-meta{
  flex:0 0 auto;
  margin:-3px 0 7px;
  font-size:.6rem;
}
.searchbox{
  min-height:34px;
  height:34px;
  flex:0 0 34px;
  padding:7px 10px;
  margin:0 0 8px;
  border-radius:9px;
  font-size:.7rem;
}
.tabs{
  flex:0 0 auto;
  display:flex;
  flex-wrap:nowrap;
  gap:5px;
  margin:0 0 8px;
  padding:1px 1px 4px;
  overflow-x:auto;
  overflow-y:hidden;
  scrollbar-width:thin;
}
.tab{
  flex:0 0 auto;
  padding:5px 9px;
  font-size:.61rem;
  white-space:nowrap;
}
.tiles{
  flex:1 1 0;
  min-height:0;
  min-width:0;
  width:100%;
  max-height:none;
  padding:2px 4px 5px 1px;
  grid-template-columns:repeat(auto-fill,minmax(76px,1fr));
  grid-auto-rows:min-content;
  align-content:start;
  gap:7px;
  overflow:auto;
  overscroll-behavior:contain;
  scrollbar-width:thin;
  scrollbar-color:#d1bca1 transparent;
}
.tiles::-webkit-scrollbar,.log::-webkit-scrollbar,#resultArea::-webkit-scrollbar{width:5px;height:5px}
.tiles::-webkit-scrollbar-thumb,.log::-webkit-scrollbar-thumb,#resultArea::-webkit-scrollbar-thumb{background:#d1bca1;border-radius:9px}
.tile{
  min-height:58px;
  padding:9px 5px 7px;
  border-radius:10px;
  background:rgba(255,250,242,.85);
}
.tile .catbar{height:3px}
.tile .f{font-size:.83rem;margin-bottom:3px}
.tile .n{font-size:.58rem;line-height:1.2}
.tile:hover{transform:translateY(-2px);box-shadow:0 7px 15px rgba(142,58,43,.10)}
.tile.locked{
  opacity:.68;
  filter:grayscale(.35);
  background:#f0e6d8;
  border-style:dashed;
  cursor:not-allowed;
}
.tile.locked::before{
  content:"🔒";
  position:absolute;
  top:5px;right:7px;
  z-index:2;
  color:#8c7560;
  font:700 .8rem 'JetBrains Mono',monospace;
  opacity:.9;
}
.tile.locked .catbar{opacity:.4}
.tile.locked:hover{transform:none;box-shadow:none}
.tiles.periodic-grid{
  min-width:0;
  grid-template-columns:repeat(18,minmax(0,1fr));
  grid-auto-rows:minmax(40px,1fr);
  gap:3px;
  padding:2px;
  overflow:auto;
  align-content:start;
}
.periodic-cell{
  width:auto;
  height:auto;
  min-width:0;
  min-height:40px;
  padding:7px 1px 3px;
  border-radius:6px;
  justify-content:flex-end;
}
.periodic-cell .atomic-number{top:3px;left:3px;font-size:.43rem}
.periodic-cell .f{font-size:clamp(.55rem,.9vw,.76rem);margin-bottom:2px}
.periodic-cell .n{font-size:clamp(.34rem,.52vw,.46rem);line-height:1.05;max-height:18px}
.periodic-cell::before{display:none}
.flaskzone{
  min-height:60px;
  max-height:112px;
  flex:0 0 auto;
  margin-bottom:8px;
  padding:9px;
  gap:6px;
  border-radius:11px;
}
.flaskzone.empty::before{font-size:.72rem;line-height:1.35}
.chip{padding:5px 9px;font-size:.72rem;gap:6px}
.chip .f{font-size:.78rem}
.actions{flex:0 0 auto;gap:7px;margin:5px 0 9px}
.btn{padding:9px 10px;border-radius:9px;font-size:.72rem}
.btn.ghost{padding:9px 12px}
#resultArea{
  flex:1 1 0;
  min-height:0;
  overflow:auto;
  overscroll-behavior:contain;
}
.result{padding:11px;border-radius:12px;margin:0 0 7px}
.result .eqline{font-size:.86rem;line-height:1.45}
.result .cond,.result .nuclear-note,.result .unlockline{font-size:.66rem;line-height:1.45}
.log{
  flex:1 1 0;
  min-height:0;
  max-height:none;
  gap:6px;
  overflow:auto;
  overscroll-behavior:contain;
}
.logitem{
  flex:0 0 auto;
  padding:7px 9px;
  border-radius:0 9px 9px 0;
  font-size:.64rem;
  line-height:1.35;
}
.logitem b{font-size:.69rem;line-height:1.35}
.logitem .lcond{font-size:.57rem}
footer{display:none !important}
@media (max-height:700px) and (orientation:landscape){
  :root{--lab-topbar:42px}
  .topbar{padding:4px 12px}
  .wrap{padding:6px 12px 8px;gap:5px;grid-template-rows:minmax(68px,auto) 52px auto minmax(0,1fr)}
  .wrap>header:not(.topbar){min-height:68px;padding:9px 16px;border-radius:15px}
  .flaskmark{width:40px;height:40px}
  .sub{font-size:.67rem}
  .stats>div{min-width:94px;padding:7px 9px}
  .stats b{font-size:1rem}
  .mode-strip{min-height:48px;padding:7px 11px;border-radius:12px}
  .mode-copy strong{font-size:.82rem}
  .mode-copy>span:last-child{font-size:.61rem}
  .mode-button{padding:6px 9px;font-size:.64rem}
  .mode-disclaimer{font-size:.53rem}
  .grid{gap:9px}
  .grid>.panel,.grid>div:last-child>.panel{padding:8px;border-radius:12px}
  .grid>div:last-child{gap:8px;grid-template-rows:minmax(0,1.1fr) minmax(0,.9fr)}
  .panel h2{font-size:.58rem;margin-bottom:7px}
  .inventory-meta{margin-bottom:5px;font-size:.54rem}
  .searchbox{height:29px;min-height:29px;flex-basis:29px;font-size:.64rem;margin-bottom:5px}
  .tabs{margin-bottom:5px}
  .tab{padding:4px 7px;font-size:.55rem}
  .tiles{grid-template-columns:repeat(auto-fill,minmax(64px,1fr));gap:5px}
  .tile{min-height:48px;padding:7px 4px 5px}
  .tile .f{font-size:.73rem}
  .tile .n{font-size:.52rem}
  .flaskzone{min-height:42px;max-height:66px;padding:6px;margin-bottom:5px}
  .actions{margin:4px 0 6px}
  .btn,.btn.ghost{padding:7px 8px;font-size:.64rem}
  .result{padding:8px}
  .result .eqline{font-size:.75rem}
  .logitem{padding:5px 7px;font-size:.59rem}
}
@media (orientation:portrait) and (max-width:900px){
  /* Khi máy dọc, xoay khung giao diện thành ngang để tránh xếp các panel theo cột.
     Trình duyệt không cho mọi trang web ép khóa hướng màn hình ở cấp thiết bị. */
  body{
    position:fixed;
    top:0;left:0;
    width:100dvh;
    height:100vw;
    min-height:0;
    transform:rotate(90deg) translateY(-100%);
    transform-origin:top left;
  }
  .topbar{height:40px;min-height:40px;flex-basis:40px;padding:3px 10px}
  .wrap{
    height:calc(100% - 40px);
    padding:5px 10px 7px;
    gap:4px;
    grid-template-rows:60px 48px auto minmax(0,1fr);
  }
  .wrap>header:not(.topbar){
    min-height:60px;
    padding:7px 11px;
    border-radius:12px;
    gap:8px;
  }
  .wrap>header:not(.topbar)::before{width:130px;height:130px;right:4%}
  .wrap>header:not(.topbar)::after{width:54px;height:54px;right:calc(4% + 36px);top:calc(50% - 32px)}
  .brand{gap:8px;align-items:center}
  .flaskmark{width:34px;height:34px;padding:4px;border-radius:9px}
  h1{font-size:1rem;letter-spacing:-.03em}
  .sub{font-size:.57rem;line-height:1.25;margin-top:3px;max-width:440px}
  .wrap>header:not(.topbar) .brand::after{left:42px;bottom:-13px;font-size:.34rem;letter-spacing:.08em}
  .stats{width:auto;gap:5px}
  .stats>div{min-width:72px;padding:5px 7px;font-size:.47rem;border-radius:8px}
  .stats b{font-size:.82rem;margin-top:1px}
  .mode-strip{
    min-height:48px;
    display:flex;
    flex-direction:row;
    align-items:center;
    justify-content:space-between;
    gap:7px;
    padding:6px 9px;
    border-radius:11px;
  }
  .mode-copy{gap:1px}
  .eyebrow{font-size:.42rem;letter-spacing:.08em}
  .mode-copy strong{font-size:.7rem}
  .mode-copy>span:last-child{font-size:.49rem;line-height:1.12;max-width:285px}
  .mode-switch{width:auto;flex:0 0 auto;padding:2px;gap:2px;border-radius:8px}
  .mode-button{flex:0 0 auto;justify-content:center;gap:4px;padding:6px 8px;border-radius:6px;font-size:.54rem}
  .mode-button .mode-icon{font-size:.68rem}
  .mode-disclaimer{font-size:.43rem;line-height:1.05;padding:0 3px}
  .disclaimer-dot{width:4px;height:4px;box-shadow:none}
  .grid{
    grid-template-columns:minmax(0,1fr) minmax(0,1fr);
    gap:7px;
  }
  .grid>.panel,.grid>div:last-child>.panel{padding:7px;border-radius:10px}
  .grid>div:last-child{grid-template-rows:minmax(0,1.13fr) minmax(0,.87fr);gap:7px}
  .panel h2{font-size:.48rem;letter-spacing:.08em;margin-bottom:5px}
  .panel h2::before{width:4px;height:4px}
  .inventory-meta{font-size:.43rem;gap:4px;margin:0 0 4px}
  .inventory-help::before{font-size:.6rem}
  .searchbox{height:25px;min-height:25px;flex-basis:25px;font-size:.51rem;padding:4px 7px;margin-bottom:4px;border-radius:6px}
  .tabs{gap:3px;margin-bottom:4px;padding-bottom:2px}
  .tab{font-size:.45rem;padding:3px 5px;border-radius:10px}
  .tiles{grid-template-columns:repeat(auto-fill,minmax(49px,1fr));gap:3px;padding:1px 2px 3px 0}
  .tile{min-height:37px;padding:6px 2px 4px;border-radius:6px}
  .tile .catbar{height:2px}
  .tile .f{font-size:.58rem;margin-bottom:1px}
  .tile .n{font-size:.4rem;line-height:1.08}
  .tile.locked::before{top:2px;right:3px;font-size:.5rem}
  .tiles.periodic-grid{grid-template-columns:repeat(18,minmax(0,1fr));grid-auto-rows:minmax(26px,1fr);gap:1px}
  .periodic-cell{min-height:26px;padding:5px 0 2px;border-radius:3px}
  .periodic-cell .atomic-number{top:1px;left:1px;font-size:.28rem}
  .periodic-cell .f{font-size:.43rem;margin-bottom:1px}
  .periodic-cell .n{font-size:.25rem;max-height:9px}
  .flaskzone{min-height:29px;max-height:48px;padding:4px;gap:3px;margin-bottom:4px;border-radius:6px}
  .flaskzone.empty::before{font-size:.49rem}
  .chip{padding:3px 5px;font-size:.5rem;gap:3px}
  .chip .f{font-size:.54rem}
  .chip .x{font-size:.49rem}
  .actions{gap:4px;margin:2px 0 4px}
  .btn,.btn.ghost{padding:5px 6px;font-size:.48rem;border-radius:6px}
  .result{padding:6px;border-radius:7px;margin-bottom:3px}
  .result .eqline{font-size:.58rem;line-height:1.25}
  .result .cond,.result .nuclear-note,.result .unlockline{font-size:.45rem;line-height:1.25;margin-top:3px}
  .log{gap:3px}
  .logitem{padding:4px 5px;font-size:.43rem;line-height:1.2}
  .logitem b{font-size:.47rem;line-height:1.2}
  .logitem .lcond{font-size:.39rem;margin-top:2px}
}
@media (prefers-reduced-motion:reduce){
  *,*::before,*::after{animation-duration:.01ms!important;transition-duration:.01ms!important}
}



/* =========================================================
   GITHUB PAGES · FULL-VIEWPORT / ANTI-SHRINK PATCH
   Giữ nguyên logic ứng dụng; loại khoảng trống thừa quanh khung.
   ========================================================= */
*, *::before, *::after { box-sizing: border-box; }
html, body {
  width: 100%;
  height: 100%;
  min-width: 0;
  min-height: 0;
  margin: 0 !important;
  padding: 0 !important;
  overflow: hidden !important;
}
body { max-width: none !important; }
.topbar {
  width: 100%;
  max-width: none !important;
  padding-left: clamp(6px, .9vw, 14px) !important;
  padding-right: clamp(6px, .9vw, 14px) !important;
}
.wrap {
  width: 100%;
  max-width: none !important;
  min-width: 0;
  margin: 0 !important;
  padding: clamp(4px, .55vw, 9px) clamp(5px, .75vw, 12px) clamp(4px, .55vw, 8px) !important;
  gap: clamp(4px, .55vw, 8px) !important;
  grid-template-rows: minmax(74px, auto) minmax(50px, auto) minmax(12px, auto) minmax(0, 1fr);
}
.wrap > header:not(.topbar) {
  min-width: 0;
  padding: clamp(9px, 1vw, 16px) clamp(12px, 1.5vw, 22px);
  margin: 0 !important;
}
.grid {
  min-width: 0;
  min-height: 0;
  width: 100%;
  gap: clamp(6px, .7vw, 11px) !important;
}
.grid > .panel,
.grid > div:last-child > .panel {
  min-width: 0;
  min-height: 0;
}

/* Chế độ ngang ở máy tính / điện thoại đã xoay */
@media (max-height: 700px) and (orientation: landscape) {
  .wrap {
    padding: 4px 7px 5px !important;
    gap: 4px !important;
    grid-template-rows: minmax(62px, auto) minmax(43px, auto) minmax(10px, auto) minmax(0, 1fr);
  }
  .wrap > header:not(.topbar) { padding: 7px 12px; }
  .grid { gap: 6px !important; }
}

/* Điện thoại đang cầm dọc: xoay khung ứng dụng, nhưng không thu nhỏ chữ quá mức */
@media (orientation: portrait) and (max-width: 900px) {
  body {
    position: fixed;
    inset: auto;
    top: 0;
    left: 0;
    width: 100dvh;
    height: 100vw;
    min-width: 0;
    min-height: 0;
    margin: 0 !important;
    padding: 0 !important;
    overflow: hidden !important;
    transform: rotate(90deg) translateY(-100%);
    transform-origin: top left;
  }
  .topbar {
    width: 100%;
    height: 38px;
    min-height: 38px;
    flex: 0 0 38px;
    padding: 3px 7px !important;
  }
  .home-origin-btn { min-height: 31px; padding: 3px 10px 3px 4px; gap: 6px; }
  .home-origin-btn .btn-icon { width: 25px; height: 25px; }
  .home-origin-btn .btn-text small { font-size: 7px; }
  .home-origin-btn .btn-text strong { font-size: 12px; }
  .wrap {
    width: 100%;
    height: calc(100% - 38px);
    min-height: 0;
    flex: 1 1 auto;
    padding: 4px 6px 5px !important;
    gap: 4px !important;
    grid-template-rows: minmax(54px, auto) minmax(43px, auto) minmax(10px, auto) minmax(0, 1fr);
  }
  .wrap > header:not(.topbar) {
    min-height: 54px;
    padding: 6px 10px;
    gap: 7px;
    border-radius: 10px;
  }
  .brand { gap: 7px; }
  .flaskmark { width: 32px; height: 32px; padding: 3px; }
  h1 { font-size: 1rem; line-height: 1.08; }
  .sub { font-size: .62rem; line-height: 1.2; margin-top: 3px; }
  .wrap > header:not(.topbar) .brand::after { display: none; }
  .stats { gap: 4px; }
  .stats > div { min-width: 68px; padding: 4px 6px; font-size: .48rem; border-radius: 7px; }
  .stats b { font-size: .78rem; margin-top: 1px; }
  .mode-strip { min-height: 43px; padding: 5px 8px; gap: 6px; border-radius: 9px; }
  .eyebrow { font-size: .48rem; letter-spacing: .06em; }
  .mode-copy strong { font-size: .72rem; line-height: 1.15; }
  .mode-copy > span:last-child { max-width: 310px; font-size: .54rem; line-height: 1.15; }
  .mode-switch { flex: 0 0 auto; padding: 2px; gap: 2px; border-radius: 7px; }
  .mode-button { padding: 6px 8px; gap: 4px; border-radius: 6px; font-size: .58rem; }
  .mode-button .mode-icon { font-size: .7rem; }
  .mode-disclaimer { min-height: 10px; padding: 0 3px; font-size: .48rem; line-height: 1.1; }
  .disclaimer-dot { width: 4px; height: 4px; }
  .grid { grid-template-columns: minmax(0, 1fr) minmax(0, 1fr); gap: 6px !important; }
  .grid > .panel,
  .grid > div:last-child > .panel { padding: 6px; border-radius: 9px; }
  .grid > div:last-child { grid-template-rows: minmax(0, 1.13fr) minmax(0, .87fr); gap: 6px; }
  .panel h2 { font-size: .57rem; letter-spacing: .06em; margin-bottom: 5px; }
  .panel h2::before { width: 4px; height: 4px; }
  .inventory-meta { margin: 0 0 4px; gap: 4px; font-size: .48rem; }
  .searchbox { height: 27px; min-height: 27px; flex-basis: 27px; padding: 4px 7px; margin-bottom: 4px; font-size: .58rem; border-radius: 6px; }
  .tabs { gap: 3px; margin-bottom: 4px; padding-bottom: 2px; }
  .tab { padding: 4px 6px; font-size: .5rem; border-radius: 9px; }
  .tiles { grid-template-columns: repeat(auto-fill, minmax(56px, 1fr)); gap: 4px; padding: 1px 2px 3px 0; }
  .tile { min-height: 42px; padding: 6px 3px 4px; border-radius: 6px; }
  .tile .catbar { height: 2px; }
  .tile .f { font-size: .68rem; margin-bottom: 2px; }
  .tile .n { font-size: .48rem; line-height: 1.08; }
  .tile.locked::before { top: 2px; right: 3px; font-size: .52rem; }
  .tiles.periodic-grid { grid-template-columns: repeat(18, minmax(0, 1fr)); grid-auto-rows: minmax(29px, 1fr); gap: 1px; }
  .periodic-cell { min-height: 29px; padding: 5px 0 2px; }
  .periodic-cell .atomic-number { top: 1px; left: 1px; font-size: .3rem; }
  .periodic-cell .f { font-size: .46rem; margin-bottom: 1px; }
  .periodic-cell .n { font-size: .29rem; max-height: 10px; }
  .flaskzone { min-height: 32px; max-height: 49px; padding: 4px; gap: 3px; margin-bottom: 4px; border-radius: 6px; }
  .flaskzone.empty::before { font-size: .54rem; }
  .chip { padding: 3px 5px; font-size: .54rem; gap: 3px; }
  .chip .f { font-size: .58rem; }
  .chip .x { font-size: .52rem; }
  .actions { gap: 4px; margin: 3px 0 4px; }
  .btn, .btn.ghost { padding: 6px 7px; font-size: .55rem; border-radius: 6px; }
  .result { padding: 6px; border-radius: 7px; margin-bottom: 3px; }
  .result .eqline { font-size: .66rem; line-height: 1.25; }
  .result .cond, .result .nuclear-note, .result .unlockline { font-size: .51rem; line-height: 1.25; margin-top: 3px; }
  .log { gap: 3px; }
  .logitem { padding: 4px 5px; font-size: .49rem; line-height: 1.2; }
  .logitem b { font-size: .52rem; line-height: 1.2; }
  .logitem .lcond { font-size: .44rem; margin-top: 2px; }
}

</style>
</head>
<body>
  <header class="topbar"> 
    <button class="home-origin-btn" onclick="window.location.href='https://2410phongnguyen-eng.github.io/Koi/'">
    <span class="btn-icon"></span>
    <span class="btn-text">
        <small>TRANG CHỦ</small>
        <strong>Nishiki Hub</strong>
    </span>
</button>
  </header>
<div class="wrap">

<header>
  <div class="brand">
    <svg class="flaskmark" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
      <path d="M40 10 L60 10 L60 38 L82 78 Q86 86 76 86 L24 86 Q14 86 18 78 L40 38 Z" fill="none" stroke="#2b1a15" stroke-width="4"/>
      <path d="M27 66 L73 66 L76 78 Q78 82 74 82 L26 82 Q22 82 24 78 Z" fill="#b02b27" opacity="0.35"/>
      <circle cx="50" cy="52" r="3" fill="#b02b27"/>
      <circle cx="42" cy="60" r="2" fill="#b02b27"/>
      <circle cx="58" cy="58" r="2.2" fill="#b02b27"/>
    </svg>
    <div>
      <h1>Phòng Thí Nghiệm <span>Ghép Chất</span></h1>
      <div class="sub">Một bàn thí nghiệm tương tác cho hóa học, đồng vị và các biến đổi hạt nhân.</div>
    </div>
  </div>
  <div class="stats">
    <div>Đã mở khoá<b id="statUnlocked">0/0</b></div>
    <div>Phản ứng đã xảy ra<b id="statReactions">0</b></div>
  </div>
</header>

<section class="mode-strip" aria-label="Chọn chế độ mô phỏng">
  <div class="mode-copy">
    <span class="eyebrow">BÀN ĐIỀU KHIỂN / 01</span>
    <strong id="modeTitle">Phản ứng hóa học</strong>
    <span id="modeDescription">Kết hợp chất, khám phá sản phẩm và mở khóa kho chất.</span>
  </div>
  <div class="mode-switch">
    <button class="mode-button active" id="chemModeBtn" type="button" aria-pressed="true"><span class="mode-icon">✳</span><span>Hóa học</span></button>
    <button class="mode-button" id="nuclearModeBtn" type="button" aria-pressed="false"><span class="mode-icon">⚛</span><span>Hạt nhân</span></button>
  </div>
</section>
<div class="mode-disclaimer" id="modeDisclaimer"><span class="disclaimer-dot"></span><span>Chế độ học tập · Phương trình hóa học phụ thuộc điều kiện ghi kèm.</span></div>

<div class="grid">

  <!-- LEFT: substances -->
  <div class="panel">
    <h2 id="inventoryTitle">Kho chất — bấm để thêm vào bình</h2>
    <div class="inventory-meta"><span id="inventoryCount">Đang hiển thị kho hóa học</span><span class="inventory-help">Chạm thẻ để thêm</span></div>
    <input class="searchbox" id="search" placeholder="Tìm tên, ký hiệu, số nguyên tử, công thức hoặc đồng vị…">
    <div class="tabs" id="tabs"></div>
    <div class="tiles" id="tiles"></div>
  </div>

  <!-- RIGHT: flask + result -->
  <div>
    <div class="panel" style="margin-bottom:16px;">
      <h2 id="flaskTitle">Bình phản ứng</h2>
      <div class="bench-label"><span class="bench-led"></span><span id="benchLabel">REACTION CHAMBER / HÓA HỌC</span><span class="bench-status">READY</span></div>
      <div class="flaskzone empty" id="flask"></div>
      <div class="actions">
        <button class="btn" id="reactBtn" disabled> Thực hiện phản ứng</button>
        <button class="btn ghost" id="clearBtn">Đổ bỏ</button>
      </div>
      <div id="resultArea"></div>
    </div>

    <div class="panel">
      <h2>Nhật ký phản ứng</h2>
      <div class="log" id="log"><div class="logitem" style="border:none;color:var(--dim);font-style:italic;">Chưa có phản ứng nào được thực hiện.</div></div>
    </div>
  </div>

</div>

<footer>
  Kho hóa học: <b id="fCount">0</b> chất · Kho hạt nhân: <b id="nCount">0</b> hạt / đồng vị · <b id="fReact">0</b> phương trình mô phỏng. Hãy xem điều kiện phản ứng như một phần của phương trình, không chỉ là dòng ghi chú.<br>
  Chế độ hạt nhân là mô hình học tập về đồng vị, hạt bắn phá và bảo toàn số khối / điện tích; không phải hướng dẫn thí nghiệm.
</footer>

</div>

<script>
/* =========================================================
   DATABASE — substances
   c: category -> element | oxide | base | acid | salt | organic | other
   ========================================================= */
const S = {


Na:{f:"Na",n:"Natri",c:"element"}, K:{f:"K",n:"Kali",c:"element"}, Ca:{f:"Ca",n:"Canxi",c:"element"},
Ba:{f:"Ba",n:"Bari",c:"element"}, Mg:{f:"Mg",n:"Magie",c:"element"}, Al:{f:"Al",n:"Nhôm",c:"element"},
Zn:{f:"Zn",n:"Kẽm",c:"element"}, Fe:{f:"Fe",n:"Sắt",c:"element"}, Ni:{f:"Ni",n:"Niken",c:"element"},
Sn:{f:"Sn",n:"Thiếc",c:"element"}, Pb:{f:"Pb",n:"Chì",c:"element"}, Cu:{f:"Cu",n:"Đồng",c:"element"},
Ag:{f:"Ag",n:"Bạc",c:"element"}, Hg:{f:"Hg",n:"Thủy ngân",c:"element"}, Au:{f:"Au",n:"Vàng",c:"element"},
H2:{f:"H<sub>2</sub>",n:"Hiđro",c:"element"},O3:{f:"O₃",n:"Ozon",c:"element"}, O2:{f:"O<sub>2</sub>",n:"Oxi",c:"element"}, N2:{f:"N<sub>2</sub>",n:"Nitơ",c:"element"},
Cl2:{f:"Cl<sub>2</sub>",n:"Clo",c:"element"}, Br2:{f:"Br<sub>2</sub>",n:"Brom",c:"element"}, I2:{f:"I<sub>2</sub>",n:"Iot",c:"element"},
F2:{f:"F<sub>2</sub>",n:"Flo",c:"element"}, S:{f:"S",n:"Lưu huỳnh",c:"element"}, C:{f:"C",n:"Cacbon",c:"element"},
P:{f:"P",n:"Photpho",c:"element"},
 Si:{f:"Si",n:"Silic",c:"element"},
Mn:{f:"Mn",n:"Mangan",c:"element"},
Cr:{f:"Cr",n:"Crôm",c:"element"},
  Li:{f:"Li",n:"Liti",c:"element"},
Be:{f:"Be",n:"Berili",c:"element"},
Sr:{f:"Sr",n:"Stronti",c:"element"},
Cd:{f:"Cd",n:"Cadimi",c:"element"},
Co:{f:"Co",n:"Coban",c:"element"},
Li2O:{f:"Li₂O",n:"Liti oxit",c:"oxide"},
BeO:{f:"BeO",n:"Berili oxit",c:"oxide"},
SrO:{f:"SrO",n:"Stronti oxit",c:"oxide"},
CdO:{f:"CdO",n:"Cadimi oxit",c:"oxide"},
CoO:{f:"CoO",n:"Coban(II) oxit",c:"oxide"},
Co2O3:{f:"Co₂O₃",n:"Coban(III) oxit",c:"oxide"},

LiOH:{f:"LiOH",n:"Liti hiđroxit",c:"base"},
BeOH2:{f:"Be(OH)₂",n:"Berili hiđroxit",c:"base"},
SrOH2:{f:"Sr(OH)₂",n:"Stronti hiđroxit",c:"base"},
CdOH2:{f:"Cd(OH)₂",n:"Cadimi hiđroxit",c:"base"},
CoOH2:{f:"Co(OH)₂",n:"Coban(II) hiđroxit",c:"base"},

LiCl:{f:"LiCl",n:"Liti clorua",c:"salt"},
LiBr:{f:"LiBr",n:"Liti bromua",c:"salt"},
LiI:{f:"LiI",n:"Liti iodua",c:"salt"},
LiF:{f:"LiF",n:"Liti florua",c:"salt"},

BeCl2:{f:"BeCl₂",n:"Berili clorua",c:"salt"},
SrCl2:{f:"SrCl₂",n:"Stronti clorua",c:"salt"},
CdCl2:{f:"CdCl₂",n:"Cadimi clorua",c:"salt"},
CoCl2:{f:"CoCl₂",n:"Coban(II) clorua",c:"salt"},

Li2CO3:{f:"Li₂CO₃",n:"Liti cacbonat",c:"salt"},
Li2SO4:{f:"Li₂SO₄",n:"Liti sunfat",c:"salt"},
LiNO3:{f:"LiNO₃",n:"Liti nitrat",c:"salt"},
Li3PO4:{f:"Li₃PO₄",n:"Liti photphat",c:"salt"},
Li2S:{f:"Li₂S",n:"Liti sunfua",c:"salt"},

BeSO4:{f:"BeSO₄",n:"Berili sunfat",c:"salt"},
SrSO4:{f:"SrSO₄",n:"Stronti sunfat",c:"salt"},
CdSO4:{f:"CdSO₄",n:"Cadimi sunfat",c:"salt"},
CoSO4:{f:"CoSO₄",n:"Coban(II) sunfat",c:"salt"},

Na2O2:{f:"Na<sub>2</sub>O<sub>2</sub>",n:"Natri peroxit",c:"oxide"},
K2O2:{f:"K<sub>2</sub>O<sub>2</sub>",n:"Kali peroxit",c:"oxide"},
CaO2:{f:"CaO<sub>2</sub>",n:"Canxi peroxit",c:"oxide"},
BaO2:{f:"BaO<sub>2</sub>",n:"Bari peroxit",c:"oxide"},
MnO2:{f:"MnO<sub>2</sub>",n:"Mangan(IV) oxit",c:"oxide"},
Na2O:{f:"Na<sub>2</sub>O",n:"Natri oxit",c:"oxide"}, K2O:{f:"K<sub>2</sub>O",n:"Kali oxit",c:"oxide"},
CaO:{f:"CaO",n:"Canxi oxit (vôi sống)",c:"oxide"}, BaO:{f:"BaO",n:"Bari oxit",c:"oxide"},
MgO:{f:"MgO",n:"Magie oxit",c:"oxide"}, Al2O3:{f:"Al<sub>2</sub>O<sub>3</sub>",n:"Nhôm oxit",c:"oxide"},
ZnO:{f:"ZnO",n:"Kẽm oxit",c:"oxide"}, FeO:{f:"FeO",n:"Sắt(II) oxit",c:"oxide"},
Fe2O3:{f:"Fe<sub>2</sub>O<sub>3</sub>",n:"Sắt(III) oxit",c:"oxide"},
FeO:{f:"FeO",n:"Sắt(II) oxit",c:"oxide"},
 Fe3O4:{f:"Fe<sub>3</sub>O<sub>4</sub>",n:"Oxit sắt từ",c:"oxide"},
CuO:{f:"CuO",n:"Đồng(II) oxit",c:"oxide"}, Cu2O:{f:"Cu<sub>2</sub>O",n:"Đồng(I) oxit",c:"oxide"},
CO2:{f:"CO<sub>2</sub>",n:"Cacbon đioxit",c:"oxide"}, CO:{f:"CO",n:"Cacbon monoxit",c:"oxide"},
SO2:{f:"SO<sub>2</sub>",n:"Lưu huỳnh đioxit",c:"oxide"}, SO3:{f:"SO<sub>3</sub>",n:"Lưu huỳnh trioxit",c:"oxide"},
NO:{f:"NO",n:"Nitơ monoxit",c:"oxide"}, NO2:{f:"NO<sub>2</sub>",n:"Nitơ đioxit",c:"oxide"},
N2O5:{f:"N<sub>2</sub>O<sub>5</sub>",n:"Đinitơ pentaoxit",c:"oxide"}, P2O5:{f:"P<sub>2</sub>O<sub>5</sub>",n:"Điphotpho pentaoxit",c:"oxide"},
SiO2:{f:"SiO<sub>2</sub>",n:"Silic đioxit",c:"oxide"}, H2O:{f:"H<sub>2</sub>O",n:"Nước",c:"oxide"},
H2O2:{f:"H<sub>2</sub>O<sub>2</sub>",n:"Oxi già",c:"oxide"},
Cr2O3:{f:"Cr<sub>2</sub>O<sub>3</sub>",n:"Crôm(III) oxit",c:"oxide"},
Ag2O:{f:"Ag<sub>2</sub>O",n:"Bạc oxit",c:"oxide"},



NaOH:{f:"NaOH",n:"Natri hiđroxit",c:"base"}, KOH:{f:"KOH",n:"Kali hiđroxit",c:"base"},
CaOH2:{f:"Ca(OH)<sub>2</sub>",n:"Canxi hiđroxit",c:"base"}, BaOH2:{f:"Ba(OH)<sub>2</sub>",n:"Bari hiđroxit",c:"base"},
MgOH2:{f:"Mg(OH)<sub>2</sub>",n:"Magie hiđroxit",c:"base"}, AlOH3:{f:"Al(OH)<sub>3</sub>",n:"Nhôm hiđroxit",c:"base"},
ZnOH2:{f:"Zn(OH)<sub>2</sub>",n:"Kẽm hiđroxit",c:"base"}, FeOH2:{f:"Fe(OH)<sub>2</sub>",n:"Sắt(II) hiđroxit",c:"base"},
FeOH3:{f:"Fe(OH)<sub>3</sub>",n:"Sắt(III) hiđroxit",c:"base"}, CuOH2:{f:"Cu(OH)<sub>2</sub>",n:"Đồng(II) hiđroxit",c:"base"},
NH3H2O:{f:"NH<sub>3</sub>·H<sub>2</sub>O",n:"Amoniac (dd)",c:"base"},

HCl:{f:"HCl",n:"Axit clohiđric",c:"acid"},
"H2SO4 loãng":{f:"H<sub>2</sub>SO<sub>4</sub> loãng",n:"Axit sunfuric loãng",c:"acid"},
"H2SO4 đặc":{f:"H<sub>2</sub>SO<sub>4</sub> đặc",n:"Axit sunfuric đặc",c:"acid"},
"H2SO4.nSO3":{f:"H<sub>2</sub>SO<sub>4</sub>.nSO<sub>3</sub>",n:"Oleum",c:"other"},
H2S2O8:{f:"H<sub>2</sub>S<sub>2</sub>O<sub>8</sub>",n:"Axit peroxydisulfuric",c:"acid"},

H2SO3:{f:"H<sub>2</sub>SO<sub>3</sub>",n:"Axit sunfurơ",c:"acid"}, HNO3:{f:"HNO<sub>3</sub>",n:"Axit nitric",c:"acid"},
H2CO3:{f:"H<sub>2</sub>CO<sub>3</sub>",n:"Axit cacbonic",c:"acid"}, H3PO4:{f:"H<sub>3</sub>PO<sub>4</sub>",n:"Axit photphoric",c:"acid"},
H2S:{f:"H<sub>2</sub>S",n:"Axit sunfuhiđric",c:"acid"}, HF:{f:"HF",n:"Axit flohiđric",c:"acid"},
HBr:{f:"HBr",n:"Axit bromhiđric",c:"acid"}, HI:{f:"HI",n:"Axit iothiđric",c:"acid"},
HIO:{f:"HIO",n:"Axit iot",c:"acid"},HClO:{f:"HClO",n:"Axit hipoclorit",c:"acid"},HBrO:{f:"HBrO",n:"Axit bromit",c:"acid"},
K2MnO4:{f:"K₂MnO₄",n:"Kali manganat",c:"salt"},
KMnO4:{f:"KMnO₄",n:"Kali pemanganat",c:"salt"},
K2CrO7:{f:"K₂CrO₇",n:"Kali cromat",c:"salt"},
NaCl:{f:"NaCl",n:"Natri clorua",c:"salt"}, KCl:{f:"KCl",n:"Kali clorua",c:"salt"},
CaCl2:{f:"CaCl<sub>2</sub>",n:"Canxi clorua",c:"salt"}, BaCl2:{f:"BaCl<sub>2</sub>",n:"Bari clorua",c:"salt"},
MgCl2:{f:"MgCl<sub>2</sub>",n:"Magie clorua",c:"salt"},
 AlCl3:{f:"AlCl<sub>3</sub>",n:"Nhôm clorua",c:"salt"},
  AlBr3:{f:"AlBr<sub>3</sub>",n:"Nhôm bromua",c:"salt"},
   AlI3:{f:"AlI<sub>3</sub>",n:"Nhôm iodide",c:"salt"},
    AlF3:{f:"AlF<sub>3</sub>",n:"Nhôm fluorua",c:"salt"},
ZnCl2:{f:"ZnCl<sub>2</sub>",n:"Kẽm clorua",c:"salt"}, FeCl2:{f:"FeCl<sub>2</sub>",n:"Sắt(II) clorua",c:"salt"},
FeCl3:{f:"FeCl<sub>3</sub>",n:"Sắt(III) clorua",c:"salt"},
 FeBr3:{f:"FeBr<sub>3</sub>",n:"Sắt(III) bromua",c:"salt"}, 
 FeI3:{f:"FeI<sub>3</sub>",n:"Sắt(III) iodide",c:"salt"}, 
 FeF3:{f:"FeF<sub>3</sub>",n:"Sắt(III) fluorua",c:"salt"},

CuCl2:{f:"CuCl<sub>2</sub>",n:"Đồng(II) clorua",c:"salt"},
CuBr2:{f:"CuBr<sub>2</sub>",n:"Đồng(II) bromua",c:"salt"},
CuI2:{f:"CuI<sub>2</sub>",n:"Đồng(II) iodide",c:"salt"},
CuF2:{f:"CuF<sub>2</sub>",n:"Đồng(II) fluorua",c:"salt"},
AgCl:{f:"AgCl",n:"Bạc clorua (↓trắng)",c:"salt"}, 
HgCl2:{f:"HgCl<sub>2</sub>",n:"Thuỷ ngân(II) clorua",c:"salt"},
NH4Cl:{f:"NH<sub>4</sub>Cl",n:"Amoni clorua",c:"salt"},
 NiCl2:{f:"NiCl<sub>2</sub>",n:"Niken clorua",c:"salt"},
SnCl2:{f:"SnCl<sub>2</sub>",n:"Thiếc(II) clorua",c:"salt"}, 
PbCl2:{f:"PbCl<sub>2</sub>",n:"Chì(II) clorua",c:"salt"},


 NaClO:{f:"NaClO",n:"Natri hipoclorit",c:"salt"},
KClO3:{f:"KClO₃",n:"Kali clorat",c:"salt"},
CaOCl2:{f:"CaOCl₂",n:"Canxi hipoclorit",c:"salt"},
BaOCl2:{f:"BaOCl₂",n:"Bari hipoclorit",c:"salt"},
Na2SO4:{f:"Na<sub>2</sub>SO<sub>4</sub>",n:"Natri sunfat",c:"salt"}, 
K2SO4:{f:"K<sub>2</sub>SO<sub>4</sub>",n:"Kali sunfat",c:"salt"},
CaSO4:{f:"CaSO<sub>4</sub>",n:"Canxi sunfat",c:"salt"}, 
BaSO4:{f:"BaSO<sub>4</sub>",n:"Bari sunfat (↓trắng)",c:"salt"},
MgSO4:{f:"MgSO<sub>4</sub>",n:"Magie sunfat",c:"salt"},
 Al2SO43:{f:"Al<sub>2</sub>(SO<sub>4</sub>)<sub>3</sub>",n:"Nhôm sunfat",c:"salt"},
ZnSO4:{f:"ZnSO<sub>4</sub>",n:"Kẽm sunfat",c:"salt"},
 FeSO4:{f:"FeSO<sub>4</sub>",n:"Sắt(II) sunfat",c:"salt"},
Fe2SO43:{f:"Fe<sub>2</sub>(SO<sub>4</sub>)<sub>3</sub>",n:"Sắt(III) sunfat",c:"salt"},
 CuSO4:{f:"CuSO<sub>4</sub>",n:"Đồng(II) sunfat",c:"salt"},
Ag2SO4:{f:"Ag<sub>2</sub>SO<sub>4</sub>",n:"Bạc sunfat (↓)",c:"salt"}, 
NH42SO4:{f:"(NH<sub>4</sub>)<sub>2</sub>SO<sub>4</sub>",n:"Amoni sunfat",c:"salt"},

Na2SO3:{f:"Na<sub>2</sub>SO<sub>3</sub>",n:"Natri sunfit",c:"salt"},

Na2CO3:{f:"Na<sub>2</sub>CO<sub>3</sub>",n:"Natri cacbonat",c:"salt"}, 
K2CO3:{f:"K<sub>2</sub>CO<sub>3</sub>",n:"Kali cacbonat",c:"salt"},
CaCO3:{f:"CaCO<sub>3</sub>",n:"Canxi cacbonat (đá vôi)",c:"salt"},
 BaCO3:{f:"BaCO<sub>3</sub>",n:"Bari cacbonat",c:"salt"},
MgCO3:{f:"MgCO<sub>3</sub>",n:"Magie cacbonat",c:"salt"},
 NaHCO3:{f:"NaHCO<sub>3</sub>",n:"Natri hiđrocacbonat",c:"salt"},
KHCO3:{f:"KHCO<sub>3</sub>",n:"Kali hiđrocacbonat",c:"salt"}, 
CaHCO32:{f:"Ca(HCO<sub>3</sub>)<sub>2</sub>",n:"Canxi hiđrocacbonat",c:"salt"},
NH4HCO3:{f:"NH<sub>4</sub>HCO<sub>3</sub>",n:"Amoni hiđrocacbonat",c:"salt"},
K2SO3:{f:"K<sub>2</sub>SO<sub>3</sub>",n:"Kali sunfit",c:"salt"},
CaSO3:{f:"CaSO<sub>3</sub>",n:"Canxi sunfit",c:"salt"},
 BaSO3:{f:"BaSO<sub>3</sub>",n:"Bari sunfit",c:"salt"},
 NaHSO3:{f:"NaHSO<sub>3</sub>",n:"Natri hiđrosunfit",c:"salt"},
KHSO3:{f:"KHSO<sub>3</sub>",n:"Kali hiđrosunfit",c:"salt"}, 
CaHSO32:{f:"Ca(HSO<sub>3</sub>)<sub>2</sub>",n:"Canxi hiđrosunfit",c:"salt"},
NH4HSO3:{f:"NH<sub>4</sub>HSO<sub>3</sub>",n:"Amoni hiđrosunfit",c:"salt"},


NaNO3:{f:"NaNO<sub>3</sub>",n:"Natri nitrat",c:"salt"}, 
KNO3:{f:"KNO<sub>3</sub>",n:"Kali nitrat",c:"salt"},
CaNO32:{f:"Ca(NO<sub>3</sub>)<sub>2</sub>",n:"Canxi nitrat",c:"salt"}, 
AgNO3:{f:"AgNO<sub>3</sub>",n:"Bạc nitrat",c:"salt"},
CuNO32:{f:"Cu(NO<sub>3</sub>)<sub>2</sub>",n:"Đồng(II) nitrat",c:"salt"}, 
FeNO32:{f:"Fe(NO<sub>3</sub>)<sub>2</sub>",n:"Sắt(II) nitrat",c:"salt"},
FeNO33:{f:"Fe(NO<sub>3</sub>)<sub>3</sub>",n:"Sắt(III) nitrat",c:"salt"},
 ZnNO32:{f:"Zn(NO<sub>3</sub>)<sub>2</sub>",n:"Kẽm nitrat",c:"salt"},
AlNO33:{f:"Al(NO<sub>3</sub>)<sub>3</sub>",n:"Nhôm nitrat",c:"salt"}, 
NH4NO3:{f:"NH<sub>4</sub>NO<sub>3</sub>",n:"Amoni nitrat",c:"salt"},

Na3PO4:{f:"Na<sub>3</sub>PO<sub>4</sub>",n:"Natri photphat",c:"salt"},
 Ca3PO42:{f:"Ca<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Canxi photphat",c:"salt"},
Ag3PO4:{f:"Ag<sub>3</sub>PO<sub>4</sub>",n:"Bạc photphat (↓vàng)",c:"salt"},
 Ba3PO42:{f:"Ba<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Bari photphat",c:"salt"},
 Na3PO4:{f:"Na<sub>3</sub>PO<sub>4</sub>",n:"Natri photphat",c:"salt"},
 K3PO4:{f:"K<sub>3</sub>PO<sub>4</sub>",n:"Kali photphat",c:"salt"},
 Cu3PO42:{f:"Cu<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Đồng(II) photphat",c:"salt"},
 Fe3PO42:{f:"Fe<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Sắt(II) photphat",c:"salt"},
 FePO4:{f:"FePO₄",n:"Sắt(III) photphat",c:"salt"},
 Mg3PO42:{f:"Mg<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Magie photphat",c:"salt"},
 Zn3PO42:{f:"Zn<sub>3</sub>(PO<sub>4</sub>)<sub>2</sub>",n:"Kẽm photphat",c:"salt"},
 AlPO4:{f:"AlPO<sub>4</sub>",n:"Nhôm photphat",c:"salt"},


Na2S:{f:"Na<sub>2</sub>S",n:"Natri sunfua",c:"salt"}, FeS:{f:"FeS",n:"Sắt(II) sunfua",c:"salt"},
CuS:{f:"CuS",n:"Đồng(II) sunfua (↓đen)",c:"salt"}, ZnS:{f:"ZnS",n:"Kẽm sunfua",c:"salt"},
Ag2S:{f:"Ag<sub>2</sub>S",n:"Bạc sunfua (↓đen)",c:"salt"}, PbS:{f:"PbS",n:"Chì(II) sunfua",c:"salt"},

NaBr:{f:"NaBr",n:"Natri bromua",c:"salt"}, NaI:{f:"NaI",n:"Natri iotua",c:"salt"},
KI:{f:"KI",n:"Kali iotua",c:"salt"}, KBr:{f:"KBr",n:"Kali bromua",c:"salt"},
NaClO:{f:"NaClO",n:"Natri hipoclorit (nước Gia-ven)",c:"salt"},
NaAlO2:{f:"NaAlO₂",n:"Natri aluminat",c:"salt"},
KAlO2:{f:"KAlO₂",n:"Kali aluminat",c:"salt"},
CaAlO22:{f:"Ca(AlO₂)₂",n:"Canxi aluminat",c:"salt"},
BaAlO22:{f:"Ba(AlO₂)₂",n:"Barium aluminat",c:"salt"},
Na2ZnO2:{f:"Na2ZnO2",n:"Natri zincat",c:"salt"},
K2ZnO2:{f:"K2ZnO2",n:"Kali zincat",c:"salt"},
CaZnO2:{f:"CaZnO2",n:"Canxi zincat",c:"salt"},
BaZnO2:{f:"BaZnO2",n:"Barium zincat",c:"salt"},

CH4:{f:"CH<sub>4</sub>",n:"Metan",c:"organic"}, C2H2:{f:"C<sub>2</sub>H<sub>2</sub>",n:"Axetilen",c:"organic"},
C2H4:{f:"C<sub>2</sub>H<sub>4</sub>",n:"Etilen",c:"organic"}, C2H6:{f:"C<sub>2</sub>H<sub>6</sub>",n:"Etan",c:"organic"},
C6H6:{f:"C<sub>6</sub>H<sub>6</sub>",n:"Benzen",c:"organic"}, C2H5OH:{f:"C<sub>2</sub>H<sub>5</sub>OH",n:"Ancol etylic",c:"organic"},
CH3OH:{f:"CH<sub>3</sub>OH",n:"Ancol metylic",c:"organic"}, HCHO:{f:"HCHO",n:"Fomanđehit",c:"organic"},
CH3CHO:{f:"CH<sub>3</sub>CHO",n:"Axetanđehit",c:"organic"}, CH3COOH:{f:"CH<sub>3</sub>COOH",n:"Axit axetic",c:"organic"},
CH3COONa:{f:"CH<sub>3</sub>COONa",n:"Natri axetat",c:"organic"}, CH3COOC2H5:{f:"CH<sub>3</sub>COOC<sub>2</sub>H<sub>5</sub>",n:"Etyl axetat",c:"organic"},
C6H12O6:{f:"C<sub>6</sub>H<sub>12</sub>O<sub>6</sub>",n:"Glucozơ",c:"organic"}, CaC2:{f:"CaC<sub>2</sub>",n:"Canxi cacbua",c:"organic"},
Al4C3:{f:"Al<sub>4</sub>C<sub>3</sub>",n:"Nhôm cacbua",c:"organic"}, CH3Cl:{f:"CH<sub>3</sub>Cl",n:"Clometan",c:"organic"},
C2H5Cl:{f:"C<sub>2</sub>H<sub>5</sub>Cl",n:"Cloetan",c:"organic"}, C2H5ONa:{f:"C<sub>2</sub>H<sub>5</sub>ONa",n:"Natri etylat",c:"organic"},
CH4:{f:"CH₄",n:"Metan",c:"organic"},
CH3OH:{f:"CH₃OH",n:"Metanol",c:"organic"},
CH2O:{f:"CH₂O",n:"Fomanđehit",c:"organic"},
HCOOH:{f:"HCOOH",n:"Axit fomic",c:"organic"},
HCOONa:{f:"HCOONa",n:"Natri fomat",c:"salt"},
CH3Cl:{f:"CH₃Cl",n:"Clometan",c:"organic"},
C2H5Cl:{f:"C₂H₅Cl",n:"Cloetan",c:"organic"},
C2H5OC2H5:{f:"C₂H₅OC₂H₅",n:"Đietyl ete",c:"organic"},
CH3COOCH3:{f:"CH₃COOCH₃",n:"Metyl axetat",c:"organic"},
HCOOC2H5:{f:"HCOOC₂H₅",n:"Etyl fomat",c:"organic"},
C3H8:{f:"C₃H₈",n:"Propan",c:"organic"},
C3H8O:{f:"C₃H₈O",n:"Propanol",c:"organic"},
CH3COCH3:{f:"CH₃COCH₃",n:"Axeton",c:"organic"},
C3H8O3:{f:"C₃H₈O₃",n:"Glixerol",c:"organic"},
C3H5N3O9:{f:"C₃H₅N₃O₉",n:"Nitroglixerin",c:"organic"},
C12H22O11:{f:"C₁₂H₂₂O₁₁",n:"Saccarozơ",c:"organic"},
NH2CONH2:{f:"NH₂CONH₂",n:"Urê",c:"organic"},
CH2CHCl:{f:"CH₂=CHCl",n:"Vinyl clorua",c:"organic"},
PP:{f:"PP",n:"Polipropilen",c:"polymer"},
CH3CHO:{f:"CH₃CHO",n:"Anđehit axetic",c:"organic"},
CH3COOH:{f:"CH₃COOH",n:"Axit axetic",c:"organic"},
CH3COONa:{f:"CH₃COONa",n:"Natri axetat",c:"salt"},
C2F4:{f:"CF₂=CF₂",n:"Tetrafloetylen",c:"organic"},
PTFE:{f:"PTFE",n:"Politetrafluoroetylen (Teflon)",c:"polymer"},

MMA:{f:"MMA",n:"Metyl metacrylat",c:"organic"},
PMMA:{f:"PMMA",n:"Polymetyl metacrylat",c:"polymer"},

VAc:{f:"VAc",n:"Vinyl axetat",c:"organic"},
PVAc:{f:"PVAc",n:"Polyvinyl axetat",c:"polymer"},
PVA:{f:"PVA",n:"Polyvinyl ancol",c:"polymer"},

AN:{f:"CH₂=CHCN",n:"Acrylonitril",c:"organic"},
PAN:{f:"PAN",n:"Polyacrylonitril",c:"polymer"},

Butadien:{f:"CH₂=CHCH=CH₂",n:"Buta-1,3-đien",c:"organic"},
PB:{f:"PB",n:"Polybutadien",c:"polymer"},

Isopren:{f:"C₅H₈",n:"Isopren",c:"organic"},
PI:{f:"PI",n:"Polyisopren",c:"polymer"},

Styren:{f:"C₈H₈",n:"Stiren",c:"organic"},
SBR:{f:"SBR",n:"Cao su Buna-S",c:"polymer"},
NBR:{f:"NBR",n:"Cao su Buna-N",c:"polymer"},

EG:{f:"HOCH₂CH₂OH",n:"Etylen glicol",c:"organic"},
TPA:{f:"HOOC-C₆H₄-COOH",n:"Axit terephtalic",c:"organic"},
PET:{f:"PET",n:"Polietilen terephtalat",c:"polymer"},

Caprolactam:{f:"Caprolactam",n:"Caprolactam",c:"organic"},
Nylon6:{f:"Nylon-6",n:"Nylon-6",c:"polymer"},

HMDA:{f:"H₂N(CH₂)₆NH₂",n:"Hexametylenđiamin",c:"organic"},
AdipicAcid:{f:"HOOC(CH₂)₄COOH",n:"Axit adipic",c:"organic"},
Nylon66:{f:"Nylon-6,6",n:"Nylon-6,6",c:"polymer"},

Phenol:{f:"C₆H₅OH",n:"Phenol",c:"organic"},
Bakelite:{f:"Bakelite",n:"Nhựa Bakelit",c:"polymer"},

BisphenolA:{f:"Bisphenol A",n:"Bisphenol A",c:"organic"},
Phosgene:{f:"COCl₂",n:"Photgen",c:"organic"},
PC:{f:"PC",n:"Polycarbonate",c:"polymer"},

POM:{f:"POM",n:"Polyoxymetylen",c:"polymer"},

LacticAcid:{f:"CH₃CH(OH)COOH",n:"Axit lactic",c:"organic"},
PLA:{f:"PLA",n:"Polylactic acid",c:"polymer"},

Diisocyanate:{f:"Diisocyanate",n:"Điisoxianat",c:"organic"},
Polyol:{f:"Polyol",n:"Polyol",c:"organic"},
PU:{f:"PU",n:"Polyurethane",c:"polymer"},

Epichlorohydrin:{f:"Epichlorohydrin",n:"Epiclohiđrin",c:"organic"},
Epoxy:{f:"Epoxy",n:"Nhựa epoxy",c:"polymer"},

Dimethyldichlorosilane:{f:"(CH₃)₂SiCl₂",n:"Đimetyl điclo silan",c:"organic"},
Silicone:{f:"Silicone",n:"Silicone",c:"polymer"},

PPD:{f:"PPD",n:"p-Phenylenediamine",c:"organic"},
TPC:{f:"TPC",n:"Terephthaloyl chloride",c:"organic"},
Kevlar:{f:"Kevlar",n:"Kevlar",c:"polymer"},
CH3COOC2H5:{f:"CH₃COOC₂H₅",n:"Etyl axetat",c:"organic"},

C6H12O6:{f:"C₆H₁₂O₆",n:"Glucozơ",c:"organic"},

C6H12:{f:"C₆H₁₂",n:"Xiclohexan",c:"organic"},
C6H5Cl:{f:"C₆H₅Cl",n:"Clobenzen",c:"organic"},

PE:{f:"PE",n:"Polietilen",c:"polymer"},
PVC:{f:"PVC",n:"Polivinyl clorua",c:"polymer"},
PS:{f:"PS",n:"Polistiren",c:"polymer"},

BeBr2:{f:"BeBr₂",n:"Berili bromua",c:"salt"},
SrBr2:{f:"SrBr₂",n:"Stronti bromua",c:"salt"},
CdBr2:{f:"CdBr₂",n:"Cadimi bromua",c:"salt"},
CoBr2:{f:"CoBr₂",n:"Coban(II) bromua",c:"salt"},

BeI2:{f:"BeI₂",n:"Berili iodua",c:"salt"},
SrI2:{f:"SrI₂",n:"Stronti iodua",c:"salt"},
CdI2:{f:"CdI₂",n:"Cadimi iodua",c:"salt"},
CoI2:{f:"CoI₂",n:"Coban(II) iodua",c:"salt"},

BeF2:{f:"BeF₂",n:"Berili florua",c:"salt"},
SrF2:{f:"SrF₂",n:"Stronti florua",c:"salt"},
CdF2:{f:"CdF₂",n:"Cadimi florua",c:"salt"},
CoF2:{f:"CoF₂",n:"Coban(II) florua",c:"salt"},

BeS:{f:"BeS",n:"Berili sunfua",c:"salt"},
SrS:{f:"SrS",n:"Stronti sunfua",c:"salt"},
CdS:{f:"CdS",n:"Cadimi sunfua",c:"salt"},
CoS:{f:"CoS",n:"Coban(II) sunfua",c:"salt"},

SrNO32:{f:"Sr(NO₃)₂",n:"Stronti nitrat",c:"salt"},
CdNO32:{f:"Cd(NO₃)₂",n:"Cadimi nitrat",c:"salt"},
CoNO32:{f:"Co(NO₃)₂",n:"Coban(II) nitrat",c:"salt"},

Sr3PO42:{f:"Sr₃(PO₄)₂",n:"Stronti photphat",c:"salt"},
Cd3PO42:{f:"Cd₃(PO₄)₂",n:"Cadimi photphat",c:"salt"},
Co3PO42:{f:"Co₃(PO₄)₂",n:"Coban(II) photphat",c:"salt"},
//==================== KHÍ ĐẶC BIỆT ====================


ClO2:{f:"ClO₂",n:"Clo đioxit",c:"other"},

NH2OH:{f:"NH₂OH",n:"Hiđroxylamin",c:"other"},
PH3:{f:"PH₃",n:"Photphin",c:"other"},
SiH4:{f:"SiH₄",n:"Silan",c:"other"},
B2H6:{f:"B₂H₆",n:"Điboran",c:"other"},

//==================== PEROXIT ====================

ZnO2:{f:"ZnO₂",n:"Kẽm peoxit",c:"oxide"},
MgO2:{f:"MgO₂",n:"Magie peoxit",c:"oxide"},
SrO2:{f:"SrO₂",n:"Stronti peoxit",c:"oxide"},

//==================== MUỐI KHÁC ====================

Na2S2O3:{f:"Na₂S₂O₃",n:"Natri thiosunfat",c:"salt"},
K2S2O3:{f:"K₂S₂O₃",n:"Kali thiosunfat",c:"salt"},
Na2Cr2O7:{f:"Na₂Cr₂O₇",n:"Natri đicromat",c:"salt"},
K2Cr2O7:{f:"K₂Cr₂O₇",n:"Kali đicromat",c:"salt"},
Na2B4O7:{f:"Na₂B₄O₇",n:"Hàn the",c:"salt"},
NH4ClO4:{f:"NH₄ClO₄",n:"Amoni peclorat",c:"salt"},
KClO4:{f:"KClO₄",n:"Kali peclorat",c:"salt"},
NaClO4:{f:"NaClO₄",n:"Natri peclorat",c:"salt"},
CuCN:{f:"CuCN",n:"Đồng(I) xyanua",c:"salt"},
AgCN:{f:"AgCN",n:"Bạc xyanua",c:"salt"},
KCN:{f:"KCN",n:"Kali xyanua",c:"salt"},
NaCN:{f:"NaCN",n:"Natri xyanua",c:"salt"},

//==================== SILICAT ====================

Na2SiO3:{f:"Na₂SiO₃",n:"Natri silicat",c:"salt"},
K2SiO3:{f:"K₂SiO₃",n:"Kali silicat",c:"salt"},
CaSiO3:{f:"CaSiO₃",n:"Canxi silicat",c:"salt"},
MgSiO3:{f:"MgSiO₃",n:"Magie silicat",c:"salt"},

//==================== BORAT ====================

H3BO3:{f:"H₃BO₃",n:"Axit boric",c:"acid"},
NaBO2:{f:"NaBO₂",n:"Natri metaborat",c:"salt"},
B2O3:{f:"B₂O₃",n:"Bo oxit",c:"oxide"},

//==================== HỢP CHẤT SILIC ====================

SiC:{f:"SiC",n:"Silic cacbua",c:"salt"},
Si3N4:{f:"Si₃N₄",n:"Silic nitrua",c:"salt"},
SiCl4:{f:"SiCl₄",n:"Silic tetraclorua",c:"salt"},

//==================== CACBUA ====================

TiC:{f:"TiC",n:"Titan cacbua",c:"salt"},

//==================== NITRUA ====================

BN:{f:"BN",n:"Bo nitrua",c:"salt"},
AlN:{f:"AlN",n:"Nhôm nitrua",c:"salt"},
Mg3N2:{f:"Mg₃N₂",n:"Magie nitrua",c:"salt"},

//==================== SUNFUA MỚI ====================

MoS2:{f:"MoS₂",n:"Molypden đisunfua",c:"compound"},
CS2:{f:"CS₂",n:"Cacbon đisunfua",c:"organic"},
NH3:{f:"NH<sub>3</sub>",n:"Amoniac",c:"other"},
NaH:{f:"NaH",n:"Natri hydrua",c:"other"},
KH:{f:"KH",n:"Kali hydrua",c:"other"},
BaH2:{f:"BaH₂",n:"Barium hydrua",c:"other"},
CaH2:{f:"CaH₂",n:"Canxi hydrua",c:"other"},

// ===== CHẤT BỔ SUNG & KHO HẠT NHÂN =====
B:{f:"B",n:"Bo",c:"element"},

HNO2:{f:"HNO₂",n:"Axit nitrơ",c:"acid"},

N2O4:{f:"N₂O₄",n:"Đinitơ tetroxit",c:"oxide"},

H2C2O4:{f:"H₂C₂O₄",n:"Axit oxalic",c:"acid"},

Na2C2O4:{f:"Na₂C₂O₄",n:"Natri oxalat",c:"salt"},

CaC2O4:{f:"CaC₂O₄",n:"Canxi oxalat",c:"salt"},

KAlSO42:{f:"KAl(SO₄)₂",n:"Kali nhôm sunfat",c:"salt"},

K2CrO4:{f:"K₂CrO₄",n:"Kali cromat",c:"salt"},

Na2CrO4:{f:"Na₂CrO₄",n:"Natri cromat",c:"salt"},

Cu2S:{f:"Cu₂S",n:"Đồng(I) sunfua",c:"salt"},

FeS2:{f:"FeS₂",n:"Sắt(II) đisunfua (pyrit)",c:"salt"},

Al2S3:{f:"Al₂S₃",n:"Nhôm sunfua",c:"salt"},

PCl3:{f:"PCl₃",n:"Photpho triclorua",c:"other"},

PCl5:{f:"PCl₅",n:"Photpho pentaclorua",c:"other"},

NaH2PO4:{f:"NaH₂PO₄",n:"Natri đihiđrophotphat",c:"salt"},

Na2HPO4:{f:"Na₂HPO₄",n:"Natri hiđrophotphat",c:"salt"},

KH2PO4:{f:"KH₂PO₄",n:"Kali đihiđrophotphat",c:"salt"},

K2HPO4:{f:"K₂HPO₄",n:"Kali hiđrophotphat",c:"salt"},

neutron:{f:"¹₀n",n:"Nơtron — hạt bắn phá",c:"nuclear",kind:"particle"},

proton:{f:"¹₁p",n:"Prôtôn — hạt bắn phá",c:"nuclear",kind:"particle"},

alpha:{f:"⁴₂He (α)",n:"Hạt alpha",c:"nuclear",kind:"particle"},

deuteron:{f:"²₁H (d)",n:"Đơteri / deutron",c:"nuclear",kind:"particle"},

gamma:{f:"⁰₀γ",n:"Photon gamma",c:"nuclear",kind:"particle"},

electron:{f:"⁰₋₁e",n:"Electron beta trừ",c:"nuclear",kind:"particle"},

positron:{f:"⁰₊₁e",n:"Positron beta cộng",c:"nuclear",kind:"particle"},

antinu:{f:"⁰₀ν̅ₑ",n:"Phản nơtrinô electron",c:"nuclear",kind:"particle"},

H1n:{f:"¹₁H",n:"Hiđro-1",c:"nuclear",kind:"isotope"},

H2n:{f:"²₁H",n:"Hiđro-2 (đơteri)",c:"nuclear",kind:"isotope"},

H3n:{f:"³₁H",n:"Hiđro-3 (triti)",c:"nuclear",kind:"isotope"},

He3n:{f:"³₂He",n:"Heli-3",c:"nuclear",kind:"isotope"},

He4n:{f:"⁴₂He",n:"Heli-4",c:"nuclear",kind:"isotope"},

Li6n:{f:"⁶₃Li",n:"Liti-6",c:"nuclear",kind:"isotope"},

Li7n:{f:"⁷₃Li",n:"Liti-7",c:"nuclear",kind:"isotope"},

Be9n:{f:"⁹₄Be",n:"Berili-9",c:"nuclear",kind:"isotope"},

B10n:{f:"¹⁰₅B",n:"Bo-10",c:"nuclear",kind:"isotope"},

B11n:{f:"¹¹₅B",n:"Bo-11",c:"nuclear",kind:"isotope"},

C11n:{f:"¹¹₆C",n:"Cacbon-11",c:"nuclear",kind:"isotope"},

C12n:{f:"¹²₆C",n:"Cacbon-12",c:"nuclear",kind:"isotope"},

C13n:{f:"¹³₆C",n:"Cacbon-13",c:"nuclear",kind:"isotope"},

C14n:{f:"¹⁴₆C",n:"Cacbon-14",c:"nuclear",kind:"isotope"},

N14n:{f:"¹⁴₇N",n:"Nitơ-14",c:"nuclear",kind:"isotope"},

O16n:{f:"¹⁶₈O",n:"Oxi-16",c:"nuclear",kind:"isotope"},

O17n:{f:"¹⁷₈O",n:"Oxi-17",c:"nuclear",kind:"isotope"},

F19n:{f:"¹⁹₉F",n:"Flo-19",c:"nuclear",kind:"isotope"},

Na22n:{f:"²²₁₁Na",n:"Natri-22",c:"nuclear",kind:"isotope"},

Na23n:{f:"²³₁₁Na",n:"Natri-23",c:"nuclear",kind:"isotope"},

Na24n:{f:"²⁴₁₁Na",n:"Natri-24",c:"nuclear",kind:"isotope"},

Al27n:{f:"²⁷₁₃Al",n:"Nhôm-27",c:"nuclear",kind:"isotope"},

P30n:{f:"³⁰₁₅P",n:"Photpho-30",c:"nuclear",kind:"isotope"},

S32n:{f:"³²₁₆S",n:"Lưu huỳnh-32",c:"nuclear",kind:"isotope"},

S33n:{f:"³³₁₆S",n:"Lưu huỳnh-33",c:"nuclear",kind:"isotope"},

U235n:{f:"²³⁵₉₂U",n:"Urani-235",c:"nuclear",kind:"isotope"},

U238n:{f:"²³⁸₉₂U",n:"Urani-238",c:"nuclear",kind:"isotope"},

U239n:{f:"²³⁹₉₂U",n:"Urani-239",c:"nuclear",kind:"isotope"},

Np239n:{f:"²³⁹₉₃Np",n:"Neptuni-239",c:"nuclear",kind:"isotope"},

Pu239n:{f:"²³⁹₉₄Pu",n:"Plutoni-239",c:"nuclear",kind:"isotope"},

Ba141n:{f:"¹⁴¹₅₆Ba",n:"Bari-141",c:"nuclear",kind:"isotope"},

Kr92n:{f:"⁹²₃₆Kr",n:"Krypton-92",c:"nuclear",kind:"isotope"},

Xe140n:{f:"¹⁴⁰₅₄Xe",n:"Xenon-140",c:"nuclear",kind:"isotope"},

Sr94n:{f:"⁹⁴₃₈Sr",n:"Stronti-94",c:"nuclear",kind:"isotope"},

// ===== CÁC MUỐI BỔ SUNG ĐƯỢC THAM CHIẾU TRONG PHẢN ỨNG =====
BaHCO32:{f:"Ba(HCO₃)₂",n:"Bari hiđrocacbonat",c:"salt"},
BaHSO32:{f:"Ba(HSO₃)₂",n:"Bari hiđrosunfit",c:"salt"},
BaHSO42:{f:"Ba(HSO₄)₂",n:"Bari hiđrosunfat",c:"salt"},
CaHSO42:{f:"Ca(HSO₄)₂",n:"Canxi hiđrosunfat",c:"salt"},
NaHSO4:{f:"NaHSO₄",n:"Natri hiđrosunfat",c:"salt"},
KHSO4:{f:"KHSO₄",n:"Kali hiđrosunfat",c:"salt"},
MgBr2:{f:"MgBr₂",n:"Magie bromua",c:"salt"},
MgF2:{f:"MgF₂",n:"Magie florua",c:"salt"},
MgI2:{f:"MgI₂",n:"Magie iodua",c:"salt"},
MgNO32:{f:"Mg(NO₃)₂",n:"Magie nitrat",c:"salt"},
NiSO4:{f:"NiSO₄",n:"Niken(II) sunfat",c:"salt"},
PbSO4:{f:"PbSO₄",n:"Chì(II) sunfat",c:"salt"},
SnSO4:{f:"SnSO₄",n:"Thiếc(II) sunfat",c:"salt"},
Ni3PO42:{f:"Ni₃(PO₄)₂",n:"Niken(II) photphat",c:"salt"},
Pb3PO42:{f:"Pb₃(PO₄)₂",n:"Chì(II) photphat",c:"salt"},
Sn3PO42:{f:"Sn₃(PO₄)₂",n:"Thiếc(II) photphat",c:"salt"},
NaO2:{f:"NaO₂",n:"Natri superoxit",c:"oxide"}
};

/* =========================================================
   BẢNG TUẦN HOÀN ĐẦY ĐỦ — 118 NGUYÊN TỐ (dữ liệu biên tập)
   z, ký hiệu, tên Việt, nhóm, hàng hiển thị, họ nguyên tố.
   ========================================================= */
const PERIODIC_ELEMENTS = [
  [1, "H", "Hiđro", 1, 1, "nonmetal"],
  [2, "He", "Heli", 18, 1, "noble"],
  [3, "Li", "Liti", 1, 2, "alkali"],
  [4, "Be", "Berili", 2, 2, "alkaline"],
  [5, "B", "Bo", 13, 2, "metalloid"],
  [6, "C", "Cacbon", 14, 2, "nonmetal"],
  [7, "N", "Nitơ", 15, 2, "nonmetal"],
  [8, "O", "Oxi", 16, 2, "nonmetal"],
  [9, "F", "Flo", 17, 2, "halogen"],
  [10, "Ne", "Neon", 18, 2, "noble"],
  [11, "Na", "Natri", 1, 3, "alkali"],
  [12, "Mg", "Magie", 2, 3, "alkaline"],
  [13, "Al", "Nhôm", 13, 3, "post"],
  [14, "Si", "Silic", 14, 3, "metalloid"],
  [15, "P", "Photpho", 15, 3, "nonmetal"],
  [16, "S", "Lưu huỳnh", 16, 3, "nonmetal"],
  [17, "Cl", "Clo", 17, 3, "halogen"],
  [18, "Ar", "Argon", 18, 3, "noble"],
  [19, "K", "Kali", 1, 4, "alkali"],
  [20, "Ca", "Canxi", 2, 4, "alkaline"],
  [21, "Sc", "Scandi", 3, 4, "transition"],
  [22, "Ti", "Titan", 4, 4, "transition"],
  [23, "V", "Vanadi", 5, 4, "transition"],
  [24, "Cr", "Crôm", 6, 4, "transition"],
  [25, "Mn", "Mangan", 7, 4, "transition"],
  [26, "Fe", "Sắt", 8, 4, "transition"],
  [27, "Co", "Coban", 9, 4, "transition"],
  [28, "Ni", "Niken", 10, 4, "transition"],
  [29, "Cu", "Đồng", 11, 4, "transition"],
  [30, "Zn", "Kẽm", 12, 4, "transition"],
  [31, "Ga", "Gali", 13, 4, "post"],
  [32, "Ge", "Gecmani", 14, 4, "metalloid"],
  [33, "As", "Asen", 15, 4, "metalloid"],
  [34, "Se", "Selen", 16, 4, "nonmetal"],
  [35, "Br", "Brom", 17, 4, "halogen"],
  [36, "Kr", "Krypton", 18, 4, "noble"],
  [37, "Rb", "Rubidi", 1, 5, "alkali"],
  [38, "Sr", "Stronti", 2, 5, "alkaline"],
  [39, "Y", "Ytri", 3, 5, "transition"],
  [40, "Zr", "Zirconi", 4, 5, "transition"],
  [41, "Nb", "Niobi", 5, 5, "transition"],
  [42, "Mo", "Molypden", 6, 5, "transition"],
  [43, "Tc", "Tecneti", 7, 5, "transition"],
  [44, "Ru", "Rutheni", 8, 5, "transition"],
  [45, "Rh", "Rhodi", 9, 5, "transition"],
  [46, "Pd", "Paladi", 10, 5, "transition"],
  [47, "Ag", "Bạc", 11, 5, "transition"],
  [48, "Cd", "Cadimi", 12, 5, "transition"],
  [49, "In", "Indi", 13, 5, "post"],
  [50, "Sn", "Thiếc", 14, 5, "post"],
  [51, "Sb", "Antimon", 15, 5, "metalloid"],
  [52, "Te", "Telu", 16, 5, "metalloid"],
  [53, "I", "Iot", 17, 5, "halogen"],
  [54, "Xe", "Xenon", 18, 5, "noble"],
  [55, "Cs", "Xesi", 1, 6, "alkali"],
  [56, "Ba", "Bari", 2, 6, "alkaline"],
  [57, "La", "Lantan", 3, 6, "lanthanoid"],
  [72, "Hf", "Hafni", 4, 6, "transition"],
  [73, "Ta", "Tantan", 5, 6, "transition"],
  [74, "W", "Wolfram", 6, 6, "transition"],
  [75, "Re", "Rheni", 7, 6, "transition"],
  [76, "Os", "Osmi", 8, 6, "transition"],
  [77, "Ir", "Iridi", 9, 6, "transition"],
  [78, "Pt", "Platin", 10, 6, "transition"],
  [79, "Au", "Vàng", 11, 6, "transition"],
  [80, "Hg", "Thủy ngân", 12, 6, "transition"],
  [81, "Tl", "Tali", 13, 6, "post"],
  [82, "Pb", "Chì", 14, 6, "post"],
  [83, "Bi", "Bitmut", 15, 6, "post"],
  [84, "Po", "Poloni", 16, 6, "post"],
  [85, "At", "Astatin", 17, 6, "halogen"],
  [86, "Rn", "Radon", 18, 6, "noble"],
  [87, "Fr", "Franxi", 1, 7, "alkali"],
  [88, "Ra", "Radi", 2, 7, "alkaline"],
  [89, "Ac", "Actini", 3, 7, "actinoid"],
  [104, "Rf", "Rutherfordi", 4, 7, "transition"],
  [105, "Db", "Dubni", 5, 7, "transition"],
  [106, "Sg", "Seaborgi", 6, 7, "transition"],
  [107, "Bh", "Bohri", 7, 7, "transition"],
  [108, "Hs", "Hassi", 8, 7, "transition"],
  [109, "Mt", "Meitneri", 9, 7, "transition"],
  [110, "Ds", "Darmstadti", 10, 7, "transition"],
  [111, "Rg", "Roentgeni", 11, 7, "transition"],
  [112, "Cn", "Copernici", 12, 7, "transition"],
  [113, "Nh", "Nihoni", 13, 7, "post"],
  [114, "Fl", "Flerovi", 14, 7, "post"],
  [115, "Mc", "Moscovi", 15, 7, "post"],
  [116, "Lv", "Livermori", 16, 7, "post"],
  [117, "Ts", "Tennessin", 17, 7, "halogen"],
  [118, "Og", "Oganesson", 18, 7, "noble"],
  [58, "Ce", "Xeri", 4, 8, "lanthanoid"],
  [59, "Pr", "Prazeodim", 5, 8, "lanthanoid"],
  [60, "Nd", "Neodim", 6, 8, "lanthanoid"],
  [61, "Pm", "Prometi", 7, 8, "lanthanoid"],
  [62, "Sm", "Samari", 8, 8, "lanthanoid"],
  [63, "Eu", "Europi", 9, 8, "lanthanoid"],
  [64, "Gd", "Gadolini", 10, 8, "lanthanoid"],
  [65, "Tb", "Terbi", 11, 8, "lanthanoid"],
  [66, "Dy", "Dysprosi", 12, 8, "lanthanoid"],
  [67, "Ho", "Holmi", 13, 8, "lanthanoid"],
  [68, "Er", "Erbi", 14, 8, "lanthanoid"],
  [69, "Tm", "Tuli", 15, 8, "lanthanoid"],
  [70, "Yb", "Ytterbi", 16, 8, "lanthanoid"],
  [71, "Lu", "Luteti", 17, 8, "lanthanoid"],
  [90, "Th", "Thori", 4, 9, "actinoid"],
  [91, "Pa", "Protactini", 5, 9, "actinoid"],
  [92, "U", "Urani", 6, 9, "actinoid"],
  [93, "Np", "Neptuni", 7, 9, "actinoid"],
  [94, "Pu", "Plutoni", 8, 9, "actinoid"],
  [95, "Am", "Americi", 9, 9, "actinoid"],
  [96, "Cm", "Curi", 10, 9, "actinoid"],
  [97, "Bk", "Berkeli", 11, 9, "actinoid"],
  [98, "Cf", "Californi", 12, 9, "actinoid"],
  [99, "Es", "Einsteini", 13, 9, "actinoid"],
  [100, "Fm", "Fermi", 14, 9, "actinoid"],
  [101, "Md", "Mendelevi", 15, 9, "actinoid"],
  [102, "No", "Nobeli", 16, 9, "actinoid"],
  [103, "Lr", "Lawrenci", 17, 9, "actinoid"]
].map(([z, symbol, name, group, period, family]) => ({z, symbol, name, group, period, family}));
for (const el of PERIODIC_ELEMENTS) {
  if (!S[el.symbol]) S[el.symbol] = { f: el.symbol, n: el.name, c: "element" };
  Object.assign(S[el.symbol], { z: el.z, group: el.group, period: el.period, family: el.family });
}

/* =========================================================
   MỞ RỘNG HÓA CHẤT & ĐỒNG PHÂN CẤU TẠO
   Các chất cùng công thức nhưng khác cấu trúc có ID riêng.
   ========================================================= */
Object.assign(S, {
  // Oxide, acids and inorganic salts
  SnO:{f:"SnO",n:"Thiếc(II) oxit",c:"oxide"},
  SnO2:{f:"SnO₂",n:"Thiếc(IV) oxit",c:"oxide"},
  PbO:{f:"PbO",n:"Chì(II) oxit",c:"oxide"},
  PbO2:{f:"PbO₂",n:"Chì(IV) oxit",c:"oxide"},
  NiO:{f:"NiO",n:"Niken(II) oxit",c:"oxide"},
  Co3O4:{f:"Co₃O₄",n:"Oxit coban từ",c:"oxide"},
  Mn2O3:{f:"Mn₂O₃",n:"Mangan(III) oxit",c:"oxide"},
  Mn3O4:{f:"Mn₃O₄",n:"Oxit mangan từ",c:"oxide"},
  CrO3:{f:"CrO₃",n:"Crôm(VI) oxit",c:"oxide"},
  TiO2:{f:"TiO₂",n:"Titan(IV) oxit",c:"oxide"},
  ZrO2:{f:"ZrO₂",n:"Zirconi đioxit",c:"oxide"},
  V2O5:{f:"V₂O₅",n:"Vanadi(V) oxit",c:"oxide"},
  MoO3:{f:"MoO₃",n:"Molypden(VI) oxit",c:"oxide"},
  WO3:{f:"WO₃",n:"Vonfram(VI) oxit",c:"oxide"},
  HgO:{f:"HgO",n:"Thủy ngân(II) oxit",c:"oxide"},
  HClO3:{f:"HClO₃",n:"Axit cloric",c:"acid"},
  HClO4:{f:"HClO₄",n:"Axit pecloric",c:"acid"},
  H2CrO4:{f:"H₂CrO₄",n:"Axit cromic",c:"acid"},
  NH4NO2:{f:"NH₄NO₂",n:"Amoni nitrit",c:"salt"},
  NaBrO3:{f:"NaBrO₃",n:"Natri bromat",c:"salt"},
  NaClO3:{f:"NaClO₃",n:"Natri clorat",c:"salt"},
  KBrO3:{f:"KBrO₃",n:"Kali bromat",c:"salt"},
  NaIO3:{f:"NaIO₃",n:"Natri iodat",c:"salt"},
  KIO3:{f:"KIO₃",n:"Kali iodat",c:"salt"},
  K2S2O8:{f:"K₂S₂O₈",n:"Kali persunfat",c:"salt"},
  AgBr:{f:"AgBr",n:"Bạc bromua (kết tủa vàng nhạt)",c:"salt"},
  AgI:{f:"AgI",n:"Bạc iodua (kết tủa vàng)",c:"salt"},
  PbI2:{f:"PbI₂",n:"Chì(II) iodua",c:"salt"},
  BaCrO4:{f:"BaCrO₄",n:"Bari cromat",c:"salt"},
  PbNO32:{f:"Pb(NO₃)₂",n:"Chì(II) nitrat",c:"salt"},
  BaNO32:{f:"Ba(NO₃)₂",n:"Bari nitrat",c:"salt"},
  NaNO2:{f:"NaNO₂",n:"Natri nitrit",c:"salt"},
  // Structural / functional isomers
  Butane:{f:"CH₃–CH₂–CH₂–CH₃",n:"Butan mạch thẳng · C₄H₁₀",c:"organic",isomerGroup:"C4H10"},
  Isobutane:{f:"(CH₃)₃CH",n:"2-metylpropan (isobutan) · C₄H₁₀",c:"organic",isomerGroup:"C4H10"},
  Pentane:{f:"CH₃–(CH₂)₃–CH₃",n:"Pentan mạch thẳng · C₅H₁₂",c:"organic",isomerGroup:"C5H12"},
  Isopentane:{f:"(CH₃)₂CH–CH₂–CH₃",n:"2-metylbutan · C₅H₁₂",c:"organic",isomerGroup:"C5H12"},
  Neopentane:{f:"C(CH₃)₄",n:"2,2-đimetylpropan · C₅H₁₂",c:"organic",isomerGroup:"C5H12"},
  Butene1:{f:"CH₂=CH–CH₂–CH₃",n:"But-1-en · C₄H₈",c:"organic",isomerGroup:"C4H8"},
  cisButene2:{f:"cis-CH₃–CH=CH–CH₃",n:"cis-but-2-en · C₄H₈",c:"organic",isomerGroup:"C4H8"},
  transButene2:{f:"trans-CH₃–CH=CH–CH₃",n:"trans-but-2-en · C₄H₈",c:"organic",isomerGroup:"C4H8"},
  Isobutene:{f:"CH₂=C(CH₃)₂",n:"2-metylpropen (isobutilen) · C₄H₈",c:"organic",isomerGroup:"C4H8"},
  Cyclopropane:{f:"(CH₂)₃ vòng",n:"Xiclopropan · C₃H₆",c:"organic",isomerGroup:"C3H6"},
  Propene:{f:"CH₂=CH–CH₃",n:"Propen · C₃H₆",c:"organic",isomerGroup:"C3H6"},
  DimethylEther:{f:"CH₃–O–CH₃",n:"Đimetyl ete · C₂H₆O",c:"organic",isomerGroup:"C2H6O"},
  Propan1ol:{f:"CH₃–CH₂–CH₂OH",n:"Propan-1-ol · C₃H₈O",c:"organic",isomerGroup:"C3H8O"},
  Propan2ol:{f:"CH₃–CHOH–CH₃",n:"Propan-2-ol (isopropanol) · C₃H₈O",c:"organic",isomerGroup:"C3H8O"},
  MethylEthylEther:{f:"CH₃–O–CH₂–CH₃",n:"Metoxyetan · C₃H₈O",c:"organic",isomerGroup:"C3H8O"},
  Propanal:{f:"CH₃–CH₂–CHO",n:"Propanal · C₃H₆O",c:"organic",isomerGroup:"C3H6O"},
  Butanal:{f:"CH₃–CH₂–CH₂–CHO",n:"Butanal · C₄H₈O",c:"organic",isomerGroup:"C4H8O"},
  Butanone:{f:"CH₃–CO–CH₂–CH₃",n:"Butan-2-on · C₄H₈O",c:"organic",isomerGroup:"C4H8O"},
  PropanoicAcid:{f:"CH₃CH₂COOH",n:"Axit propionic · C₃H₆O₂",c:"organic"},
  MethylPropanoate:{f:"CH₃CH₂COOCH₃",n:"Metyl propionat · C₄H₈O₂",c:"organic",isomerGroup:"C4H8O2"},
  EthylPropanoate:{f:"CH₃CH₂COOC₂H₅",n:"Etyl propionat · C₅H₁₀O₂",c:"organic"},
  Fructose:{f:"C₆H₁₂O₆",n:"Fructozơ · đồng phân của glucozơ",c:"organic",isomerGroup:"C6H12O6"},
  Galactose:{f:"C₆H₁₂O₆",n:"Galactozơ · đồng phân của glucozơ",c:"organic",isomerGroup:"C6H12O6"},
  MaleicAcid:{f:"cis-HOOC–CH=CH–COOH",n:"Axit maleic · C₄H₄O₄",c:"organic",isomerGroup:"C4H4O4"},
  FumaricAcid:{f:"trans-HOOC–CH=CH–COOH",n:"Axit fumaric · C₄H₄O₄",c:"organic",isomerGroup:"C4H4O4"},
  OrthoXylene:{f:"o-C₆H₄(CH₃)₂",n:"o-Xylen (1,2-đimetylbenzen) · C₈H₁₀",c:"organic",isomerGroup:"C8H10"},
  MetaXylene:{f:"m-C₆H₄(CH₃)₂",n:"m-Xylen (1,3-đimetylbenzen) · C₈H₁₀",c:"organic",isomerGroup:"C8H10"},
  ParaXylene:{f:"p-C₆H₄(CH₃)₂",n:"p-Xylen (1,4-đimetylbenzen) · C₈H₁₀",c:"organic",isomerGroup:"C8H10"},
  nButanol:{f:"CH₃CH₂CH₂CH₂OH",n:"Butan-1-ol · C₄H₁₀O",c:"organic",isomerGroup:"C4H10O"},
  secButanol:{f:"CH₃CH(OH)CH₂CH₃",n:"Butan-2-ol · C₄H₁₀O",c:"organic",isomerGroup:"C4H10O"},
  isoButanol:{f:"(CH₃)₂CHCH₂OH",n:"2-metylpropan-1-ol · C₄H₁₀O",c:"organic",isomerGroup:"C4H10O"},
  tertButanol:{f:"(CH₃)₃COH",n:"2-metylpropan-2-ol · C₄H₁₀O",c:"organic",isomerGroup:"C4H10O"}
});

/* =========================================================
   REACTIONS
   r: reactant ids, p: product ids, cond: condition text ("" = không cần điều kiện)
   eq: full display equation
   ========================================================= */
const R = [

{r:["Na2SO3","S"],p:["Na2S2O3"],cond:"",eq:"Na₂SO₃ + S → Na₂S₂O₃"},

{r:["SiO2","NaOH"],p:["Na2SiO3","H2O"],cond:"t°",eq:"SiO₂ + 2NaOH → Na₂SiO₃ + H₂O"},

{r:["SiO2","KOH"],p:["K2SiO3","H2O"],cond:"t°",eq:"SiO₂ + 2KOH → K₂SiO₃ + H₂O"},

{r:["CaO","SiO2"],p:["CaSiO3"],cond:"t°",eq:"CaO + SiO₂ → CaSiO₃"},

{r:["MgO","SiO2"],p:["MgSiO3"],cond:"t°",eq:"MgO + SiO₂ → MgSiO₃"},

{r:["B","O2"],p:["B2O3"],cond:"t°",eq:"4B + 3O₂ → 2B₂O₃"},

{r:["B2O3","H2O"],p:["H3BO3"],cond:"",eq:"B₂O₃ + 3H₂O → 2H₃BO₃"},

{r:["Si","C"],p:["SiC"],cond:"2000°C",eq:"Si + C → SiC"},

{r:["Si","Cl2"],p:["SiCl4"],cond:"t°",eq:"Si + 2Cl₂ → SiCl₄"},

{r:["Si","N2"],p:["Si3N4"],cond:"t°",eq:"3Si + 2N₂ → Si₃N₄"},


{r:["Mg","N2"],p:["Mg3N2"],cond:"t°",eq:"3Mg + N₂ → Mg₃N₂"},

{r:["Al","N2"],p:["AlN"],cond:"t°",eq:"2Al + N₂ → 2AlN"},

{r:["B","N2"],p:["BN"],cond:"t°",eq:"2B + N₂ → 2BN"},

{r:["C","S"],p:["CS2"],cond:"t°",eq:"C + 2S → CS₂"},
  // --- kim loại + oxi ---
{r:["Li","O2"],p:["Li2O"],cond:"t°",eq:"4Li + O₂ → 2Li₂O"},
{r:["Be","O2"],p:["BeO"],cond:"t°",eq:"2Be + O₂ → 2BeO"},
{r:["Sr","O2"],p:["SrO"],cond:"t°",eq:"2Sr + O₂ → 2SrO"},
{r:["Cd","O2"],p:["CdO"],cond:"t°",eq:"2Cd + O₂ → 2CdO"},
{r:["Co","O2"],p:["CoO"],cond:"t°",eq:"2Co + O₂ → 2CoO"},
{r:["CoO","O2"],p:["Co2O3"],cond:"t°",eq:"4CoO + O₂ → 2Co₂O₃"},

// --- oxit + nước ---
{r:["Li2O","H2O"],p:["LiOH"],cond:"",eq:"Li₂O + H₂O → 2LiOH"},
{r:["SrO","H2O"],p:["SrOH2"],cond:"",eq:"SrO + H₂O → Sr(OH)₂"},

// --- kim loại + nước ---
{r:["Li","H2O"],p:["LiOH","H2"],cond:"",eq:"2Li + 2H₂O → 2LiOH + H₂↑"},
{r:["Sr","H2O"],p:["SrOH2","H2"],cond:"",eq:"Sr + 2H₂O → Sr(OH)₂ + H₂↑"},

// --- kim loại + clo ---
{r:["Li","Cl2"],p:["LiCl"],cond:"t°",eq:"2Li + Cl₂ → 2LiCl"},
{r:["Be","Cl2"],p:["BeCl2"],cond:"t°",eq:"Be + Cl₂ → BeCl₂"},
{r:["Sr","Cl2"],p:["SrCl2"],cond:"t°",eq:"Sr + Cl₂ → SrCl₂"},
{r:["Cd","Cl2"],p:["CdCl2"],cond:"t°",eq:"Cd + Cl₂ → CdCl₂"},
{r:["Co","Cl2"],p:["CoCl2"],cond:"t°",eq:"Co + Cl₂ → CoCl₂"},

// --- liti + halogen ---
{r:["Li","Br2"],p:["LiBr"],cond:"t°",eq:"2Li + Br₂ → 2LiBr"},
{r:["Li","I2"],p:["LiI"],cond:"t°",eq:"2Li + I₂ → 2LiI"},
{r:["Li","F2"],p:["LiF"],cond:"",eq:"2Li + F₂ → 2LiF"},

// --- axit + kim loại ---
{r:["HCl","Li"],p:["LiCl","H2"],cond:"",eq:"2Li + 2HCl → 2LiCl + H₂↑"},
{r:["HCl","Be"],p:["BeCl2","H2"],cond:"",eq:"Be + 2HCl → BeCl₂ + H₂↑"},
{r:["HCl","Cd"],p:["CdCl2","H2"],cond:"",eq:"Cd + 2HCl → CdCl₂ + H₂↑"},
{r:["HCl","Co"],p:["CoCl2","H2"],cond:"",eq:"Co + 2HCl → CoCl₂ + H₂↑"},

{r:["Li","H2SO4 loãng"],p:["Li2SO4","H2"],cond:"",eq:"2Li + H₂SO₄ loãng → Li₂SO₄ + H₂↑"},
{r:["Be","H2SO4 loãng"],p:["BeSO4","H2"],cond:"",eq:"Be + H₂SO₄ loãng → BeSO₄ + H₂↑"},
{r:["Cd","H2SO4 loãng"],p:["CdSO4","H2"],cond:"",eq:"Cd + H₂SO₄ loãng → CdSO₄ + H₂↑"},
{r:["Co","H2SO4 loãng"],p:["CoSO4","H2"],cond:"",eq:"Co + H₂SO₄ loãng → CoSO₄ + H₂↑"},

// --- bazơ + axit ---
{r:["LiOH","HCl"],p:["LiCl","H2O"],cond:"",eq:"LiOH + HCl → LiCl + H₂O"},
{r:["SrOH2","HCl"],p:["SrCl2","H2O"],cond:"",eq:"Sr(OH)₂ + 2HCl → SrCl₂ + 2H₂O"},
{r:["CdOH2","HCl"],p:["CdCl2","H2O"],cond:"",eq:"Cd(OH)₂ + 2HCl → CdCl₂ + 2H₂O"},
{r:["CoOH2","HCl"],p:["CoCl2","H2O"],cond:"",eq:"Co(OH)₂ + 2HCl → CoCl₂ + 2H₂O"},

// --- oxit + axit ---
{r:["Li2O","HCl"],p:["LiCl","H2O"],cond:"",eq:"Li₂O + 2HCl → 2LiCl + H₂O"},
{r:["BeO","HCl"],p:["BeCl2","H2O"],cond:"",eq:"BeO + 2HCl → BeCl₂ + H₂O"},
{r:["SrO","HCl"],p:["SrCl2","H2O"],cond:"",eq:"SrO + 2HCl → SrCl₂ + H₂O"},
{r:["CdO","HCl"],p:["CdCl2","H2O"],cond:"",eq:"CdO + 2HCl → CdCl₂ + H₂O"},
{r:["CoO","HCl"],p:["CoCl2","H2O"],cond:"",eq:"CoO + 2HCl → CoCl₂ + H₂O"},
// --- kim loại + brom ---
{r:["Be","Br2"],p:["BeBr2"],cond:"t°",eq:"Be + Br₂ → BeBr₂"},
{r:["Sr","Br2"],p:["SrBr2"],cond:"t°",eq:"Sr + Br₂ → SrBr₂"},
{r:["Cd","Br2"],p:["CdBr2"],cond:"t°",eq:"Cd + Br₂ → CdBr₂"},
{r:["Co","Br2"],p:["CoBr2"],cond:"t°",eq:"Co + Br₂ → CoBr₂"},

// --- kim loại + iot ---
{r:["Be","I2"],p:["BeI2"],cond:"t°",eq:"Be + I₂ → BeI₂"},
{r:["Sr","I2"],p:["SrI2"],cond:"t°",eq:"Sr + I₂ → SrI₂"},
{r:["Cd","I2"],p:["CdI2"],cond:"t°",eq:"Cd + I₂ → CdI₂"},
{r:["Co","I2"],p:["CoI2"],cond:"t°",eq:"Co + I₂ → CoI₂"},

// --- kim loại + flo ---
{r:["Be","F2"],p:["BeF2"],cond:"",eq:"Be + F₂ → BeF₂"},
{r:["Sr","F2"],p:["SrF2"],cond:"",eq:"Sr + F₂ → SrF₂"},
{r:["Cd","F2"],p:["CdF2"],cond:"",eq:"Cd + F₂ → CdF₂"},
{r:["Co","F2"],p:["CoF2"],cond:"",eq:"Co + F₂ → CoF₂"},

// --- kim loại + lưu huỳnh ---
{r:["Li","S"],p:["Li2S"],cond:"t°",eq:"2Li + S → Li₂S"},
{r:["Be","S"],p:["BeS"],cond:"t°",eq:"Be + S → BeS"},
{r:["Sr","S"],p:["SrS"],cond:"t°",eq:"Sr + S → SrS"},
{r:["Cd","S"],p:["CdS"],cond:"t°",eq:"Cd + S → CdS"},
{r:["Co","S"],p:["CoS"],cond:"t°",eq:"Co + S → CoS"},

// --- oxit + H2SO4 loãng ---
{r:["Li2O","H2SO4 loãng"],p:["Li2SO4","H2O"],cond:"",eq:"Li₂O + H₂SO₄ → Li₂SO₄ + H₂O"},
{r:["BeO","H2SO4 loãng"],p:["BeSO4","H2O"],cond:"",eq:"BeO + H₂SO₄ → BeSO₄ + H₂O"},
{r:["SrO","H2SO4 loãng"],p:["SrSO4","H2O"],cond:"",eq:"SrO + H₂SO₄ → SrSO₄ + H₂O"},
{r:["CdO","H2SO4 loãng"],p:["CdSO4","H2O"],cond:"",eq:"CdO + H₂SO₄ → CdSO₄ + H₂O"},
{r:["CoO","H2SO4 loãng"],p:["CoSO4","H2O"],cond:"",eq:"CoO + H₂SO₄ → CoSO₄ + H₂O"},

// --- bazơ + H2SO4 ---
{r:["LiOH","H2SO4 loãng"],p:["Li2SO4","H2O"],cond:"",eq:"2LiOH + H₂SO₄ → Li₂SO₄ + 2H₂O"},
{r:["SrOH2","H2SO4 loãng"],p:["SrSO4","H2O"],cond:"",eq:"Sr(OH)₂ + H₂SO₄ → SrSO₄ + 2H₂O"},
{r:["CdOH2","H2SO4 loãng"],p:["CdSO4","H2O"],cond:"",eq:"Cd(OH)₂ + H₂SO₄ → CdSO₄ + 2H₂O"},
{r:["CoOH2","H2SO4 loãng"],p:["CoSO4","H2O"],cond:"",eq:"Co(OH)₂ + H₂SO₄ → CoSO₄ + 2H₂O"},

// --- bazơ + HNO3 ---
{r:["LiOH","HNO3"],p:["LiNO3","H2O"],cond:"",eq:"LiOH + HNO₃ → LiNO₃ + H₂O"},
{r:["SrOH2","HNO3"],p:["SrNO32","H2O"],cond:"",eq:"Sr(OH)₂ + 2HNO₃ → Sr(NO₃)₂ + 2H₂O"},
{r:["CdOH2","HNO3"],p:["CdNO32","H2O"],cond:"",eq:"Cd(OH)₂ + 2HNO₃ → Cd(NO₃)₂ + 2H₂O"},
{r:["CoOH2","HNO3"],p:["CoNO32","H2O"],cond:"",eq:"Co(OH)₂ + 2HNO₃ → Co(NO₃)₂ + 2H₂O"},

// --- bazơ + H3PO4 ---
{r:["LiOH","H3PO4"],p:["Li3PO4","H2O"],cond:"",eq:"3LiOH + H₃PO₄ → Li₃PO₄ + 3H₂O"},
{r:["SrOH2","H3PO4"],p:["Sr3PO42","H2O"],cond:"",eq:"3Sr(OH)₂ + 2H₃PO₄ → Sr₃(PO₄)₂ + 6H₂O"},
{r:["CdOH2","H3PO4"],p:["Cd3PO42","H2O"],cond:"",eq:"3Cd(OH)₂ + 2H₃PO₄ → Cd₃(PO₄)₂ + 6H₂O"},
{r:["CoOH2","H3PO4"],p:["Co3PO42","H2O"],cond:"",eq:"3Co(OH)₂ + 2H₃PO₄ → Co₃(PO₄)₂ + 6H₂O"},

//==================== DẪN XUẤT HALOGEN ====================

{r:["CH4","Cl2"],p:["CH3Cl","HCl"],cond:"ánh sáng",eq:"CH₄ + Cl₂ → CH₃Cl + HCl"},
{r:["CH3Cl","NaOH"],p:["CH3OH","NaCl"],cond:"dd,t°",eq:"CH₃Cl + NaOH → CH₃OH + NaCl"},
{r:["C2H6","Cl2"],p:["C2H5Cl","HCl"],cond:"ánh sáng",eq:"C₂H₆ + Cl₂ → C₂H₅Cl + HCl"},
{r:["C2H5Cl","NaOH"],p:["C2H5OH","NaCl"],cond:"dd,t°",eq:"C₂H₅Cl + NaOH → C₂H₅OH + NaCl"},

//==================== ETE ====================

{r:["C2H5OH"],p:["C2H5OC2H5","H2O"],cond:"H₂SO₄ đặc,140°C",eq:"2C₂H₅OH → C₂H₅OC₂H₅ + H₂O"},
{r:["C2H5OC2H5","H2O"],p:["C2H5OH"],cond:"H⁺",eq:"C₂H₅OC₂H₅ + H₂O → 2C₂H₅OH"},

//==================== AXIT HỮU CƠ ====================

{r:["CH3COOH","CH3OH"],p:["CH3COOCH3","H2O"],cond:"H₂SO₄ đặc",eq:"CH₃COOH + CH₃OH ⇌ CH₃COOCH₃ + H₂O"},
{r:["HCOOH","C2H5OH"],p:["HCOOC2H5","H2O"],cond:"H₂SO₄ đặc",eq:"HCOOH + C₂H₅OH ⇌ HCOOC₂H₅ + H₂O"},

//==================== GLIXEROL ====================

{r:["C3H8","O2"],p:["C3H8O3"],cond:"xt",eq:"2C₃H₈ + 3O₂ → 2C₃H₈O₃"},
{r:["C3H8O3","HNO3"],p:["C3H5N3O9","H2O"],cond:"H₂SO₄ đặc",eq:"C₃H₈O₃ + 3HNO₃ → C₃H₅N₃O₉ + 3H₂O"},

//==================== ĐƯỜNG ====================

{r:["C6H12O6"],p:["C12H22O11","H2O"],cond:"xt",eq:"2C₆H₁₂O₆ → C₁₂H₂₂O₁₁ + H₂O"},
{r:["C12H22O11","H2O"],p:["C6H12O6"],cond:"H⁺",eq:"C₁₂H₂₂O₁₁ + H₂O → 2C₆H₁₂O₆"},

//==================== AXETON ====================

{r:["C3H8O"],p:["CH3COCH3","H2"],cond:"Cu,t°",eq:"C₃H₈O → CH₃COCH₃ + H₂"},
{r:["CH3COCH3","H2"],p:["C3H8O"],cond:"Ni",eq:"CH₃COCH₃ + H₂ → C₃H₈O"},

//==================== URE ====================

{r:["NH3","CO2"],p:["NH2CONH2","H2O"],cond:"t°,p",eq:"2NH₃ + CO₂ → NH₂CONH₂ + H₂O"},



//==================== POLYME ====================

// Politetrafluoroetylen (Teflon)
{r:["C2F4"],p:["PTFE"],cond:"xt,p",eq:"nCF₂=CF₂ → PTFE"},

// Polymetyl metacrylat (Mica hữu cơ)
{r:["MMA"],p:["PMMA"],cond:"xt",eq:"nCH₂=C(CH₃)COOCH₃ → PMMA"},

// Polyvinyl axetat
{r:["VAc"],p:["PVAc"],cond:"xt",eq:"nCH₂=CHOCOCH₃ → PVAc"},

// Polyvinyl ancol
{r:["PVAc","NaOH"],p:["PVA","CH3COONa"],cond:"dd",eq:"PVAc + NaOH → PVA + CH₃COONa"},

// Polyacrylonitril
{r:["AN"],p:["PAN"],cond:"xt",eq:"nCH₂=CHCN → PAN"},

// Polybutadien
{r:["Butadien"],p:["PB"],cond:"xt",eq:"nCH₂=CH−CH=CH₂ → PB"},

// Polyisopren (cao su thiên nhiên)
{r:["Isopren"],p:["PI"],cond:"xt",eq:"nC₅H₈ → PI"},

// Cao su Buna-S
{r:["Butadien","Styren"],p:["SBR"],cond:"xt",eq:"Butadien + Styren → SBR"},

// Cao su Buna-N
{r:["Butadien","AN"],p:["NBR"],cond:"xt",eq:"Butadien + Acrylonitril → NBR"},

// PET
{r:["EG","TPA"],p:["PET","H2O"],cond:"t°",eq:"nHOCH₂CH₂OH + nHOOCC₆H₄COOH → PET + 2nH₂O"},

// Nylon-6
{r:["Caprolactam"],p:["Nylon6"],cond:"t°",eq:"nCaprolactam → Nylon-6"},

// Nylon-6,6
{r:["HMDA","AdipicAcid"],p:["Nylon66","H2O"],cond:"t°",eq:"nHMDA + nAdipic Acid → Nylon-6,6 + H₂O"},

// Bakelit
{r:["Phenol","CH2O"],p:["Bakelite","H2O"],cond:"xt",eq:"Phenol + Formaldehyde → Bakelite"},

// Polycarbonate
{r:["BisphenolA","Phosgene"],p:["PC"],cond:"xt",eq:"Bisphenol A + COCl₂ → PC"},

// Polyoxymetylen
{r:["CH2O"],p:["POM"],cond:"xt",eq:"nCH₂O → POM"},

// Polylactic acid
{r:["LacticAcid"],p:["PLA","H2O"],cond:"xt",eq:"nLactic Acid → PLA + H₂O"},

// Polyurethane
{r:["Diisocyanate","Polyol"],p:["PU"],cond:"xt",eq:"Diisocyanate + Polyol → PU"},

// Nhựa epoxy
{r:["Epichlorohydrin","BisphenolA"],p:["Epoxy"],cond:"xt",eq:"Epichlorohydrin + Bisphenol A → Epoxy"},

// Silicone
{r:["Dimethyldichlorosilane","H2O"],p:["Silicone","HCl"],cond:"",eq:"(CH₃)₂SiCl₂ + H₂O → Silicone + HCl"},

// Kevlar
{r:["PPD","TPC"],p:["Kevlar","HCl"],cond:"",eq:"PPD + TPC → Kevlar + HCl"},
{r:["C2H4"],p:["PP"],cond:"xt",eq:"nC₃H₆ → PP"},
{r:["C2H4","Cl2"],p:["CH2CHCl"],cond:"xt",eq:"C₂H₄ + Cl₂ → CH₂CHCl + HCl"},
{r:["CH2CHCl"],p:["PVC"],cond:"xt",eq:"nCH₂CHCl → PVC"},
// --- đốt cháy với O2 ---

{r:["Ag","O2"],p:["Ag2O"],cond:"t°",eq:"4Ag + O₂ → 2Ag₂O"},
{r:["Mn","O2"],p:["MnO2"],cond:"t°",eq:"Mn + O₂ → MnO₂"},
{r:["Cr","O2"],p:["Cr2O3"],cond:"t°",eq:"4Cr + 3O₂ → 2Cr₂O₃"},
{r:["Na","O2"],p:["Na2O"],cond:"t°",eq:"4Na + O₂ → 2Na₂O"},
{r:["K","O2"],p:["K2O"],cond:"t°",eq:"4K + O₂ → 2K₂O"},
{r:["Ca","O2"],p:["CaO"],cond:"t°",eq:"2Ca + O₂ → 2CaO"},
{r:["Ba","O2"],p:["BaO"],cond:"t°",eq:"2Ba + O₂ → 2BaO"},
{r:["Mg","O2"],p:["MgO"],cond:"t°",eq:"2Mg + O₂ → 2MgO"},
{r:["Al","O2"],p:["Al2O3"],cond:"t°",eq:"4Al + 3O₂ → 2Al₂O₃"},
{r:["Zn","O2"],p:["ZnO"],cond:"t°",eq:"2Zn + O₂ → 2ZnO"},
{r:["FeO","O2"],p:["Fe2O3"],cond:"t°",eq:"4FeO + O₂ → 2Fe₂O₃"},
{r:["Fe","O2"],p:["FeO"],cond:"t°",eq:"2Fe + O₂ → 2FeO"},
{r:["FeO","Fe2O3"],p:["Fe3O4"],cond:"t°",eq:"FeO + Fe₂O₃ → Fe₃O₄"},
{r:["Cu","O2"],p:["CuO"],cond:"t°",eq:"2Cu + O₂ → 2CuO"},
{r:["S","O2"],p:["SO2"],cond:"t°",eq:"S + O₂ → SO₂"},
{r:["SO2","O2"],p:["SO3"],cond:"V₂O₅/t°",eq:"2SO₂ + O₂ → 2SO₃"},
{r:["C","O2"],p:["CO2"],cond:"t°",eq:"C + O₂ → CO₂"},
{r:["P","O2"],p:["P2O5"],cond:"t°",eq:"4P + 5O₂ → 2P₂O₅"},
{r:["Si","O2"],p:["SiO2"],cond:"t°",eq:"Si + O₂ → SiO₂"},
{r:["H2","O2"],p:["H2O"],cond:"tia lửa",eq:"2H₂ + O₂ → 2H₂O"},
{r:["CO","O2"],p:["CO2"],cond:"t°",eq:"2CO + O₂ → 2CO₂"},
{r:["CH4","O2"],p:["CO2","H2O"],cond:"t°",eq:"CH₄ + 2O₂ → CO₂ + 2H₂O"},
{r:["C2H2","O2"],p:["CO2","H2O"],cond:"t°",eq:"2C₂H₂ + 5O₂ → 4CO₂ + 2H₂O"},
{r:["C2H4","O2"],p:["CO2","H2O"],cond:"t°",eq:"C₂H₄ + 3O₂ → 2CO₂ + 2H₂O"},
{r:["C2H6","O2"],p:["CO2","H2O"],cond:"t°",eq:"2C₂H₆ + 7O₂ → 4CO₂ + 6H₂O"},
{r:["C2H5OH","O2"],p:["CO2","H2O"],cond:"t°",eq:"C₂H₅OH + 3O₂ → 2CO₂ + 3H₂O"},
{r:["C6H6","O2"],p:["CO2","H2O"],cond:"t°",eq:"2C₆H₆ + 15O₂ → 12CO₂ + 6H₂O"},
{r:["CaO","O2"],p:["CaO2"],cond:"t°",eq:"2CaO + O₂ → 2CaO₂"},
{r:["BaO","O2"],p:["BaO2"],cond:"t°",eq:"2BaO + O₂ → 2BaO₂"},
{r:["K2O","O2"],p:["K2O2"],cond:"t°",eq:"2K₂O + O₂ → 2K₂O₂"},
{r:["Na2O","O2"],p:["Na2O2"],cond:"t°",eq:"2NaO + O₂ → 2Na₂O₂"},


// --- muối acid ---
{r:["Na2CO3","H2O","CO2"],p:["NaHCO3"],cond:"",eq:"Na₂CO₃ + H₂O + CO₂ → 2NaHCO₃"},
{r:["CaCO3","H2O","CO2"],p:["CaHCO32"],cond:"",eq:"CaCO₃ + H₂O + CO₂ → Ca(HCO₃)₂"},
{r:["K2CO3","H2O","CO2"],p:["KHCO3"],cond:"",eq:"K₂CO₃ + H₂O + CO₂ → 2KHCO₃"},
{r:["BaCO3","H2O","CO2"],p:["BaHCO32"],cond:"",eq:"BaCO₃ + H₂O + CO₂ → Ba(HCO₃)₂"},
{r:["Na2SO3","H2O","SO2"],p:["NaHSO3"],cond:"",eq:"Na₂SO₃ + H₂O + SO₂ → 2NaHSO₃"},
{r:["CaSO3","H2O","SO2"],p:["CaHSO32"],cond:"",eq:"CaSO₃ + H₂O + SO₂ → Ca(HSO₃)₂"},
{r:["BaSO3","H2O","SO2"],p:["BaHSO32"],cond:"",eq:"BaSO₃ + H₂O + SO₂ → Ba(HSO₃)₂"},
{r:["K2SO3","H2O","SO2"],p:["KHSO3"],cond:"",eq:"K₂SO₃ + H₂O + SO₂ → 2KHSO₃"},
{r:["Na2SO4","H2SO4 loãng"],p:["NaHSO4"],cond:"",eq:"Na₂SO₄ + H₂SO₄ loãng → 2NaHSO₄"},
{r:["CaSO4","H2SO4 loãng"],p:["CaHSO42"],cond:"",eq:"CaSO₄ + H₂SO₄ loãng → Ca(HSO₄)₂"},
{r:["BaSO4","H2SO4 loãng"],p:["BaHSO42"],cond:"",eq:"BaSO₄ + H₂SO₄ loãng → Ba(HSO₄)₂"},
{r:["K2SO4","H2SO4 loãng"],p:["KHSO4"],cond:"",eq:"K₂SO₄ + H₂SO₄ loãng → 2KHSO₄"},
{r:["Na2SO4","H2SO4 đặc"],p:["NaHSO4"],cond:"",eq:"Na₂SO₄ + H₂SO₄ đặc → 2NaHSO₄"},
{r:["CaSO4","H2SO4 đặc"],p:["CaHSO42"],cond:"",eq:"CaSO₄ + H₂SO₄ đặc → Ca(HSO₄)₂"},
{r:["BaSO4","H2SO4 đặc"],p:["BaHSO42"],cond:"",eq:"BaSO₄ + H₂SO₄ đặc → Ba(HSO₄)₂"},
{r:["K2SO4","H2SO4 đặc"],p:["KHSO4"],cond:"",eq:"K₂SO₄ + H₂SO₄ đặc → 2KHSO₄"},


// --- base + halogen ---
{r:["NaOH","Cl2"],p:["NaCl","NaClO"],cond:"t°",eq:"2NaOH + Cl₂ → NaCl + NaClO + H₂O"},
{r:["KOH","Cl2"],p:["KCl","KClO3"],cond:"t°",eq:"6KOH + 3Cl₂ → 5KCl + KClO₃+ 3H₂O"},
{r:["CaOH2","Cl2"],p:["CaCl2","CaOCl2"],cond:"",eq:"2Ca(OH)₂ + 2Cl₂ → CaCl₂ + CaOCl₂ + 2H₂O"},
{r:["BaOH2","Cl2"],p:["BaCl2","BaOCl2"],cond:"",eq:"2Ba(OH)₂ + 2Cl₂ → BaCl₂ + BaOCl₂ + 2H₂O"},
// --- kim loại + halogen ---
{r:["Na","Cl2"],p:["NaCl"],cond:"t°",eq:"2Na + Cl₂ → 2NaCl"},
{r:["K","Cl2"],p:["KCl"],cond:"t°",eq:"2K + Cl₂ → 2KCl"},
{r:["Ca","Cl2"],p:["CaCl2"],cond:"t°",eq:"Ca + Cl₂ → CaCl₂"},
{r:["Mg","Cl2"],p:["MgCl2"],cond:"t°",eq:"Mg + Cl₂ → MgCl₂"},
{r:["Mg","I2"],p:["MgI2"],cond:"t°",eq:"Mg + I₂ → MgI₂"},
{r:["Mg","Br2"],p:["MgBr2"],cond:"t°",eq:"Mg + Br₂ → MgBr₂"},
{r:["Mg","F2"],p:["MgF2"],cond:"t°",eq:"Mg + F₂ → MgF₂"},
{r:["Al","I2"],p:["AlI3"],cond:"t°",eq:"2Al + 3I₂ → 2AlI₃"},
{r:["Al","F2"],p:["AlF3"],cond:"t°",eq:"2Al + 3F₂ → 2AlF₃"},
{r:["Al","Br2"],p:["AlBr3"],cond:"t°",eq:"2Al + 3Br₂ → 2AlBr₃"},
{r:["Al","Cl2"],p:["AlCl3"],cond:"t°",eq:"2Al + 3Cl₂ → 2AlCl₃"},
{r:["Fe","Cl2"],p:["FeCl3"],cond:"t°",eq:"2Fe + 3Cl₂ → 2FeCl₃"},
{r:["Fe","I2"],p:["FeI3"],cond:"t°",eq:"2Fe + 3I₂ → 2FeI₃"},
{r:["Fe","F2"],p:["FeF3"],cond:"t°",eq:"2Fe + 3F₂ → 2FeF₃"},
{r:["Fe","Br2"],p:["FeBr3"],cond:"t°",eq:"2Fe + 3Br₂ → 2FeBr₃"},
{r:["Cu","Cl2"],p:["CuCl2"],cond:"t°",eq:"Cu + Cl₂ → CuCl₂"},
{r:["Cu","I2"],p:["CuI2"],cond:"t°",eq:"Cu + I₂ → CuI₂"},
{r:["Cu","Br2"],p:["CuBr2"],cond:"t°",eq:"Cu + Br₂ → CuBr₂"},
{r:["Cu","F2"],p:["CuF2"],cond:"t°",eq:"Cu + F₂ → CuF₂"},
{r:["Zn","Cl2"],p:["ZnCl2"],cond:"t°",eq:"Zn + Cl₂ → ZnCl₂"},
{r:["Hg","Cl2"],p:["HgCl2"],cond:"t°",eq:"Hg + Cl₂ → HgCl₂"},
{r:["H2","Cl2"],p:["HCl"],cond:"ánh sáng",eq:"H₂ + Cl₂ → 2HCl"},
{r:["Na","Br2"],p:["NaBr"],cond:"t°",eq:"2Na + Br₂ → 2NaBr"},
{r:["Na","I2"],p:["NaI"],cond:"t°",eq:"2Na + I₂ → 2NaI"},
{r:["K","Br2"],p:["KBr"],cond:"t°",eq:"2K + Br₂ → 2KBr"},
{r:["K","I2"],p:["KI"],cond:"t°",eq:"2K + I₂ → 2KI"},

{r:["H2","I2"],p:["HI"],cond:"t°",eq:"H₂ + I₂ ⇌ 2HI"},
{r:["H2","F2"],p:["HF"],cond:"",eq:"H₂ + F₂ → 2HF"},
{r:["H2","Br2"],p:["HBr"],cond:"t°",eq:"H₂ + Br₂ → 2HBr"},
// --- kim loại + lưu huỳnh ---
{r:["Fe","S"],p:["FeS"],cond:"t°",eq:"Fe + S → FeS"},
{r:["Cu","S"],p:["CuS"],cond:"t°",eq:"Cu + S → CuS"},
{r:["Zn","S"],p:["ZnS"],cond:"t°",eq:"Zn + S → ZnS"},
{r:["Ag","S"],p:["Ag2S"],cond:"t°",eq:"2Ag + S → Ag₂S"},
{r:["Pb","S"],p:["PbS"],cond:"t°",eq:"Pb + S → PbS"},
{r:["H2","S"],p:["H2S"],cond:"t°",eq:"H₂ + S → H₂S"},

// --- kim loại + nước ---
{r:["Na","H2O"],p:["NaOH","H2"],cond:"",eq:"2Na + 2H₂O → 2NaOH + H₂↑"},
{r:["K","H2O"],p:["KOH","H2"],cond:"",eq:"2K + 2H₂O → 2KOH + H₂↑"},
{r:["Ca","H2O"],p:["CaOH2","H2"],cond:"",eq:"Ca + 2H₂O → Ca(OH)₂ + H₂↑"},
{r:["Ba","H2O"],p:["BaOH2","H2"],cond:"",eq:"Ba + 2H₂O → Ba(OH)₂ + H₂↑"},

// ---  nước ---
{r:["Na2O","H2O"],p:["NaOH"],cond:"",eq:"Na₂O + H₂O → 2NaOH"},
{r:["K2O","H2O"],p:["KOH"],cond:"",eq:"K₂O + H₂O → 2KOH"},
{r:["CaO","H2O"],p:["CaOH2"],cond:"",eq:"CaO + H₂O → Ca(OH)₂"},
{r:["BaO","H2O"],p:["BaOH2"],cond:"",eq:"BaO + H₂O → Ba(OH)₂"},
{r:["CO2","H2O"],p:["H2CO3"],cond:"",eq:"CO₂ + H₂O ⇌ H₂CO₃"},
{r:["SO2","H2O"],p:["H2SO3"],cond:"",eq:"SO₂ + H₂O ⇌ H₂SO₃"},
{r:["SO3","H2O"],p:["H2SO4 đặc"],cond:"",eq:"SO₃ + H₂O → H₂SO₄ đặc"},
{r:["H2SO4 đặc","H2O"],p:["H2SO4 loãng"],cond:"",eq:"H₂SO₄ đặc + H₂O → H₂SO₄ loãng"},
{r:["H2SO4 đặc","SO3"],p:["H2SO4.nSO3"],cond:"",eq:"H₂SO₄ đặc + SO₃ → H2SO4.nSO3"},
{r:["H2SO4.nSO3","H2O"],p:["H2SO4 đặc"],cond:"",eq:"H2SO4.nSO3 + nH₂O → (n+1)H₂SO₄ đặc "},
{r:["N2O5","H2O"],p:["HNO3"],cond:"",eq:"N₂O₅ + H₂O → 2HNO₃"},
{r:["P2O5","H2O"],p:["H3PO4"],cond:"",eq:"P₂O₅ + 3H₂O → 2H₃PO₄"},
{r:["NO2","H2O"],p:["HNO3","NO"],cond:"",eq:"3NO₂ + H₂O → 2HNO₃ + NO"},
{r:["NO2","O2","H2O"],p:["HNO3"],cond:"",eq:"4NO₂ + O₂ + 2H₂O → 4HNO₃"},

{r:["Br2","SO2","H2O"],p:["HBr","H2SO4 loãng"],cond:"",eq:"Br₂ + SO₂ + 2H₂O → 2HBr + H₂SO₄"},
{r:["F2","H2O"],p:["HF","O2"],cond:"",eq:"2F₂ + 2H₂O → 4HF + O₂"},
{r:["I2","H2O"],p:["HI","HIO"],cond:"",eq:"I₂ + H₂O ⇌ HI + HIO"},
{r:["Cl2","H2O"],p:["HCl","HClO"],cond:"",eq:"Cl₂ + H₂O ⇌ HCl + HClO"},
{r:["Br2","H2O"],p:["HBr","HBrO"],cond:"",eq:"Br₂ + H₂O ⇌ HBr + HBrO"},

{r:["CaO2","H2O"],p:["CaOH2","H2O2"],cond:"0°C",eq:"CaO₂ + H₂O → Ca(OH)₂ + H₂O₂"},
{r:["BaO2","H2O"],p:["BaOH2","H2O2"],cond:"0°C",eq:"BaO₂ a+ H₂O → Ba(OH)₂ + H₂O₂"},
{r:["K2O2","H2O"],p:["KOH","H2O2"],cond:"0°C",eq:"K₂O₂ + H₂O → 2KOH + H₂O₂"},
{r:["NaO2","H2O"],p:["NaOH","H2O2"],cond:"0°C",eq:"NaO₂ + H₂O → NaOH + H₂O₂"},

  {r:["NaH","H2O"],p:["NaOH","H2O"],cond:"0°C",eq:"NaH + H₂O → NaOH + H₂"},
  {r:["KH","H2O"],p:["KOH","H2O"],cond:"0°C",eq:"KH + H₂O → KOH + H₂"},
  {r:["CaH2","H2O"],p:["CaOH2","H2O"],cond:"0°C",eq:"CaH₂ + H₂O → CaOH + H₂"},
   {r:["BaH2","H2O"],p:["BaOH2","H2O"],cond:"0°C",eq:"BaH₂ + H₂O → BaOH + H₂"},
// --- nitơ / amoniac ---
{r:["N2","H2"],p:["NH3"],cond:"t°, p, xt Fe",eq:"N₂ + 3H₂ ⇌ 2NH₃"},
{r:["N2","O2"],p:["NO"],cond:"tia lửa điện / 3000°C",eq:"N₂ + O₂ → 2NO"},
{r:["NO","O2"],p:["NO2"],cond:"",eq:"2NO + O₂ → 2NO₂"},
{r:["NH3","O2"],p:["NO","H2O"],cond:"xt, t°",eq:"4NH₃ + 5O₂ → 4NO + 6H₂O"},
{r:["NH3","H2O"],p:["NH3H2O"],cond:"",eq:"NH₃ + H₂O ⇌ NH₃·H₂O"},
{r:["NH3","HCl"],p:["NH4Cl"],cond:"",eq:"NH₃ + HCl → NH₄Cl"},
{r:["NH3","HNO3"],p:["NH4NO3"],cond:"",eq:"NH₃ + HNO₃ → NH₄NO₃"},
{r:["NH3","H2SO4 đặc"],p:["NH42SO4"],cond:"",eq:"2NH₃ + H₂SO₄ đặc → (NH₄)₂SO₄"},
{r:["NH3","H2SO4 loãng"],p:["NH42SO4"],cond:"",eq:"2NH₃ + H₂SO₄ loãng → (NH₄)₂SO₄"},
{r:["NH3","H2O","SO2"],p:["NH4HSO3"],cond:"",eq:"NH₃ + H₂O + SO₂ → NH₄HSO₃"},
{r:["NH3","H2O","CO2"],p:["NH4HCO3"],cond:"",eq:"NH₃ + H₂O + CO₂ → NH₄HCO₃"},

// --- axit + bazơ (trung hoà) ---
{r:["HCl","NaOH"],p:["NaCl","H2O"],cond:"",eq:"HCl + NaOH → NaCl + H₂O"},
{r:["HCl","KOH"],p:["KCl","H2O"],cond:"",eq:"HCl + KOH → KCl + H₂O"},
{r:["HCl","CaOH2"],p:["CaCl2","H2O"],cond:"",eq:"2HCl + Ca(OH)₂ → CaCl₂ + 2H₂O"},
{r:["HCl","BaOH2"],p:["BaCl2","H2O"],cond:"",eq:"2HCl + Ba(OH)₂ → BaCl₂ + 2H₂O"},
{r:["HCl","MgOH2"],p:["MgCl2","H2O"],cond:"",eq:"2HCl + Mg(OH)₂ → MgCl₂ + 2H₂O"},
{r:["HCl","AlOH3"],p:["AlCl3","H2O"],cond:"",eq:"3HCl + Al(OH)₃ → AlCl₃ + 3H₂O"},
{r:["HCl","ZnOH2"],p:["ZnCl2","H2O"],cond:"",eq:"2HCl + Zn(OH)₂ → ZnCl₂ + 2H₂O"},
{r:["HCl","FeOH2"],p:["FeCl2","H2O"],cond:"",eq:"2HCl + Fe(OH)₂ → FeCl₂ + 2H₂O"},
{r:["HCl","FeOH3"],p:["FeCl3","H2O"],cond:"",eq:"3HCl + Fe(OH)₃ → FeCl₃ + 3H₂O"},
{r:["HCl","CuOH2"],p:["CuCl2","H2O"],cond:"",eq:"2HCl + Cu(OH)₂ → CuCl₂ + 2H₂O"},
{r:["H2SO4 loãng","NaOH"],p:["Na2SO4","H2O"],cond:"",eq:"H₂SO₄ + 2NaOH → Na₂SO₄ + 2H₂O"},
{r:["H2SO4 loãng","KOH"],p:["K2SO4","H2O"],cond:"",eq:"H₂SO₄ + 2KOH → K₂SO₄ + 2H₂O"},
{r:["H2SO4 loãng","CaOH2"],p:["CaSO4","H2O"],cond:"",eq:"H₂SO₄ + Ca(OH)₂ → CaSO₄ + 2H₂O"},
{r:["H2SO4 loãng","BaOH2"],p:["BaSO4","H2O"],cond:"",eq:"H₂SO₄ + Ba(OH)₂ → BaSO₄↓ + 2H₂O"},
{r:["H2SO4 loãng","MgOH2"],p:["MgSO4","H2O"],cond:"",eq:"H₂SO₄ + Mg(OH)₂ → MgSO₄ + 2H₂O"},
{r:["H2SO4 loãng","AlOH3"],p:["Al2SO43","H2O"],cond:"",eq:"3H₂SO₄ + 2Al(OH)₃ → Al₂(SO₄)₃ + 6H₂O"},
{r:["H2SO4 loãng","ZnOH2"],p:["ZnSO4","H2O"],cond:"",eq:"H₂SO₄ + Zn(OH)₂ → ZnSO₄ + 2H₂O"},
{r:["H2SO4 loãng","FeOH2"],p:["FeSO4","H2O"],cond:"",eq:"H₂SO₄ + Fe(OH)₂ → FeSO₄ + 2H₂O"},
{r:["H2SO4 loãng","FeOH3"],p:["Fe2SO43","H2O"],cond:"",eq:"3H₂SO₄ + 2Fe(OH)₃ → Fe₂(SO₄)₃ + 6H₂O"},
{r:["H2SO4 loãng","CuOH2"],p:["CuSO4","H2O"],cond:"",eq:"H₂SO₄ + Cu(OH)₂ → CuSO₄ + 2H₂O"},

{r:["H2SO4 đặc","NaOH"],p:["Na2SO4","H2O"],cond:"",eq:"H₂SO₄ + 2NaOH → Na₂SO₄ + 2H₂O"},
{r:["H2SO4 đặc","KOH"],p:["K2SO4","H2O"],cond:"",eq:"H₂SO₄ + 2KOH → K₂SO₄ + 2H₂O"},
{r:["H2SO4 đặc","CaOH2"],p:["CaSO4","H2O"],cond:"",eq:"H₂SO₄ + Ca(OH)₂ → CaSO₄ + 2H₂O"},
{r:["H2SO4 đặc","BaOH2"],p:["BaSO4","H2O"],cond:"",eq:"H₂SO₄ + Ba(OH)₂ → BaSO₄↓ + 2H₂O"},
{r:["H2SO4 đặc","MgOH2"],p:["MgSO4","H2O"],cond:"",eq:"H₂SO₄ + Mg(OH)₂ → MgSO₄ + 2H₂O"},
{r:["H2SO4 đặc","AlOH3"],p:["Al2SO43","H2O"],cond:"",eq:"3H₂SO₄ + 2Al(OH)₃ → Al₂(SO₄)₃ + 6H₂O"},
{r:["H2SO4 đặc","ZnOH2"],p:["ZnSO4","H2O"],cond:"",eq:"H₂SO₄ + Zn(OH)₂ → ZnSO₄ + 2H₂O"},
{r:["H2SO4 đặc","FeOH2"],p:["FeSO4","H2O"],cond:"",eq:"H₂SO₄ + Fe(OH)₂ → FeSO₄ + 2H₂O"},
{r:["H2SO4 đặc","FeOH3"],p:["Fe2SO43","H2O"],cond:"",eq:"3H₂SO₄ + 2Fe(OH)₃ → Fe₂(SO₄)₃ + 6H₂O"},
{r:["H2SO4 đặc","CuOH2"],p:["CuSO4","H2O"],cond:"",eq:"H₂SO₄ + Cu(OH)₂ → CuSO₄ + 2H₂O"},

{r:["HNO3","NaOH"],p:["NaNO3","H2O"],cond:"",eq:"HNO₃ + NaOH → NaNO₃ + H₂O"},
{r:["HNO3","KOH"],p:["KNO3","H2O"],cond:"",eq:"HNO₃ + KOH → KNO₃ + H₂O"},
{r:["HNO3","CaOH2"],p:["CaNO32","H2O"],cond:"",eq:"2HNO₃ + Ca(OH)₂ → Ca(NO₃)₂ + 2H₂O"},
{r:["HNO3","CuOH2"],p:["CuNO32","H2O"],cond:"",eq:"2HNO₃ + Cu(OH)₂ → Cu(NO₃)₂ + 2H₂O"},
{r:["H3PO4","NaOH"],p:["Na3PO4","H2O"],cond:"",eq:"H₃PO₄ + 3NaOH → Na₃PO₄ + 3H₂O"},
{r:["H3PO4","CaOH2"],p:["Ca3PO42","H2O"],cond:"",eq:"2H₃PO₄ + 3Ca(OH)₂ → Ca₃(PO₄)₂↓ + 6H₂O"},
{r:["CH3COOH","NaOH"],p:["CH3COONa","H2O"],cond:"",eq:"CH₃COOH + NaOH → CH₃COONa + H₂O"},

// --- axit + kim loại đứng trước H ---
{r:["HCl","K"],p:["KCl","H2"],cond:"",eq:"2K + 2HCl → 2KCl + H₂↑"},
{r:["HCl","Na"],p:["NaCl","H2"],cond:"",eq:"2Na + 2HCl → 2NaCl + H₂↑"},
{r:["HCl","Ca"],p:["CaCl2","H2"],cond:"",eq:"Ca + 2HCl → CaCl₂ + H₂↑"},
{r:["HCl","Ba"],p:["BaCl2","H2"],cond:"",eq:"Ba + 2HCl → BaCl₂ + H₂↑"},
{r:["HCl","Mg"],p:["MgCl2","H2"],cond:"",eq:"Mg + 2HCl → MgCl₂ + H₂↑"},
{r:["HCl","Al"],p:["AlCl3","H2"],cond:"",eq:"2Al + 6HCl → 2AlCl₃ + 3H₂↑"},
{r:["HCl","Zn"],p:["ZnCl2","H2"],cond:"",eq:"Zn + 2HCl → ZnCl₂ + H₂↑"},
{r:["HCl","Fe"],p:["FeCl2","H2"],cond:"",eq:"Fe + 2HCl → FeCl₂ + H₂↑"},
{r:["HCl","Ni"],p:["NiCl2","H2"],cond:"",eq:"Ni + 2HCl → NiCl₂ + H₂↑"},
{r:["HCl","Sn"],p:["SnCl2","H2"],cond:"",eq:"Sn + 2HCl → SnCl₂ + H₂↑"},
{r:["HCl","Pb"],p:["PbCl2","H2"],cond:"",eq:"Pb + 2HCl → PbCl₂ + H₂↑"},

{r:["K","H2SO4 loãng"],p:["K2SO4","H2"],cond:"",eq:"2K + H₂SO₄ loãng → K₂SO₄ + H₂↑"},
{r:["Ca","H2SO4 loãng"],p:["CaSO4","H2"],cond:"",eq:"Ca + H₂SO₄ loãng → CaSO₄ + H₂↑"},
{r:["Na","H2SO4 loãng"],p:["Na2SO4","H2"],cond:"",eq:"2Na + H₂SO₄ loãng → Na₂SO₄ + H₂↑"},
{r:["Ba","H2SO4 loãng"],p:["BaSO4","H2"],cond:"",eq:"Ba + H₂SO₄ loãng → BaSO₄↓ + H₂↑"},
{r:["Al","H2SO4 loãng"],p:["Al2SO43","H2"],cond:"",eq:"2Al + 3H₂SO₄ loãng → Al₂(SO₄)₃ + 3H₂↑"},
{r:["Fe","H2SO4 loãng"],p:["FeSO4","H2"],cond:"",eq:"Fe + H₂SO₄ loãng → FeSO₄ + H₂↑"},
{r:["Zn","H2SO4 loãng"],p:["ZnSO4","H2"],cond:"",eq:"Zn + H₂SO₄ loãng → ZnSO₄ + H₂↑"},
{r:["Mg","H2SO4 loãng"],p:["MgSO4","H2"],cond:"",eq:"Mg + H₂SO₄ loãng → MgSO₄ + H₂↑"},
{r:["H2SO4 loãng","Ni"],p:["NiSO4","H2"],cond:"",eq:"Ni + H₂SO₄ loãng → NiSO₄ + H₂↑"},
{r:["H2SO4 loãng","Sn"],p:["SnSO4","H2"],cond:"",eq:"Sn + H₂SO₄ loãng → SnSO₄ + H₂↑"},
{r:["H2SO4 loãng","Pb"],p:["PbSO4","H2"],cond:"",eq:"Pb + H₂SO₄ loãng → PbSO₄↓ + H₂↑"},

{r:["K","H2SO4 đặc"],p:["K2SO4","SO2","H2O"],cond:"nóng",eq:"2K + 2H₂SO₄ đặc → K₂SO₄ + SO₂↑ + 2H₂O"},
{r:["Ca","H2SO4 đặc"],p:["CaSO4","SO2","H2O"],cond:"nóng",eq:"Ca + 2H₂SO₄ đặc → CaSO₄ + SO₂↑ + 2H₂O"},
{r:["Na","H2SO4 đặc"],p:["Na2SO4","SO2","H2O"],cond:"nóng",eq:"2Na + 2H₂SO₄ đặc → Na₂SO₄ + SO₂↑ + 2H₂O"},
{r:["Ba","H2SO4 đặc"],p:["BaSO4","SO2","H2O"],cond:"nóng",eq:"Ba + 2H₂SO₄ đặc → BaSO₄ + SO₂↑ + 2H₂O"},
{r:["Al","H2SO4 đặc"],p:["Al2SO43","SO2","H2O"],cond:"nóng",eq:"2Al + 6H₂SO₄ đặc → Al₂(SO₄)₃ + 3SO₂↑ + 6H₂O"},
{r:["Cu","H2SO4 đặc"],p:["CuSO4","SO2","H2O"],cond:"nóng",eq:"Cu + 2H₂SO₄ đặc → CuSO₄ + SO₂↑ + 2H₂O"},
{r:["Ag","H2SO4 đặc"],p:["Ag2SO4","SO2","H2O"],cond:"nóng",eq:"2Ag + 2H₂SO₄ đặc → Ag₂SO₄ + SO₂↑ + 2H₂O"},
{r:["Fe","H2SO4 đặc"],p:["Fe2SO43","SO2","H2O"],cond:"nóng",eq:"2Fe + 6H₂SO₄ đặc → Fe₂(SO₄)₃ + 3SO₂↑ + 6H₂O"},
{r:["Zn","H2SO4 đặc"],p:["ZnSO4","SO2","H2O"],cond:"nóng",eq:"Zn + 2H₂SO₄ đặc → ZnSO₄ + SO₂↑ + 2H₂O"},
{r:["Mg","H2SO4 đặc"],p:["MgSO4","SO2","H2O"],cond:"nóng",eq:"Mg + 2H₂SO₄ đặc → MgSO₄ + SO₂↑ + 2H₂O"},


{r:["K","H3PO4"],p:["K3PO4","H2"],cond:"",eq:"6K + 2H₃PO₄ → 2K₃PO₄ + 3H₂↑"},
{r:["Ca","H3PO4"],p:["Ca3PO42","H2"],cond:"",eq:"3Ca + 2H₃PO₄ → Ca₃(PO₄)₂↓ + 3H₂↑"},
{r:["Na","H3PO4"],p:["Na3PO4","H2"],cond:"",eq:"6Na + 2H₃PO₄ → 2Na₃PO₄ + 3H₂↑"},
{r:["Ba","H3PO4"],p:["Ba3PO42","H2"],cond:"",eq:"3Ba + 2H₃PO₄ → Ba₃(PO₄)₂↓ + 3H₂↑"},
{r:["Al","H3PO4"],p:["AlPO4","H2"],cond:"",eq:"2Al + 2H₃PO₄ → 2AlPO₄↓ + 3H₂↑"},
{r:["Fe","H3PO4"],p:["Fe3PO42","H2"],cond:"",eq:"3Fe + 2H₃PO₄ → Fe₃(PO₄)₂↓ + 3H₂↑"},
{r:["Zn","H3PO4"],p:["Zn3PO42","H2"],cond:"",eq:"3Zn + 2H₃PO₄ → Zn₃(PO₄)₂↓ + 3H₂↑"},
{r:["Mg","H3PO4"],p:["Mg3PO42","H2"],cond:"",eq:"3Mg + 2H₃PO₄ → Mg₃(PO₄)₂↓ + 3H₂↑"},
{r:["H3PO4","Ni"],p:["Ni3PO42","H2"],cond:"",eq:"3Ni + 2H₃PO₄ → Ni₃(PO₄)₂↓ + 3H₂↑"},
{r:["H3PO4","Sn"],p:["Sn3PO42","H2"],cond:"",eq:"3Sn + 2H₃PO₄ → Sn₃(PO₄)₂↓ + 3H₂↑"},
{r:["H3PO4","Pb"],p:["Pb3PO42","H2"],cond:"",eq:"3Pb + 2H₃PO₄ → Pb₃(PO₄)₂↓ + 3H₂↑"},

{r:["K","HNO3"],p:["KNO3","NO2","H2O"],cond:"",eq:"K + 2HNO₃ → KNO₃ + NO₂↑ + H₂O"},
{r:["Ca","HNO3"],p:["CaNO32","NO2","H2O"],cond:"",eq:"Ca + 2HNO₃ → Ca(NO₃)₂ + NO₂↑ + H₂O"},
{r:["Na","HNO3"],p:["NaNO3","NO2","H2O"],cond:"",eq:"Na + 2HNO₃ → NaNO₃ + NO₂↑ + H₂O"},
{r:["Ba","HNO3"],p:["BaNO32","NO2","H2O"],cond:"",eq:"Ba + 2HNO₃ → Ba(NO₃)₂ + NO₂↑ + H₂O"},
{r:["Al","HNO3"],p:["AlNO33","NO2","H2O"],cond:"",eq:"Al + 6HNO₃ → Al(NO₃)₃ + 3NO₂↑ + 3H₂O"},
{r:["Cu","HNO3"],p:["CuNO32","NO2","H2O"],cond:"",eq:"Cu + 4HNO₃ → Cu(NO₃)₂ + 2NO₂↑ + 2H₂O"},
{r:["Ag","HNO3"],p:["AgNO3","NO2","H2O"],cond:"",eq:"Ag + 2HNO₃ → AgNO₃ + NO₂↑ + H₂O"},
{r:["Fe","HNO3"],p:["FeNO33","NO2","H2O"],cond:"",eq:"Fe + 6HNO₃ → Fe(NO₃)₃ + 3NO₂↑ + 3H₂O"},
{r:["Zn","HNO3"],p:["ZnNO32","NO2","H2O"],cond:"",eq:"Zn + 4HNO₃ → Zn(NO₃)₂ + 2NO₂↑ + 2H₂O"},
{r:["Mg","HNO3"],p:["MgNO32","NO2","H2O"],cond:"",eq:"Mg + 4HNO₃ → Mg(NO₃)₂ + 2NO₂↑ + 2H₂O"},
// ---  bazơ  ---
{r:["NaOH","AlOH3"],p:["NaAlO2","H2O"],cond:"",eq:"NaOH + Al(OH)₃ → NaAlO₂ + 2H₂O"},
{r:["KOH","AlOH3"],p:["KAlO2","H2O"],cond:"",eq:"KOH + Al(OH)₃ → KAlO₂ + 2H₂O"},
{r:["NaOH","Al2O3"],p:["NaAlO2","H2O"],cond:"",eq:"NaOH + Al₂O₃ → NaAlO₂ + 3H₂O"},
{r:["NaOH","Al","H2O"],p:["NaAlO2","H2"],cond:"",eq:"2NaOH + 2Al + 2H₂O → 2NaAlO₂ + 3H₂"},
{r:["CaOH2","AlOH3"],p:["CaAlO22","H2O"],cond:"",eq:"Ca(OH)₂ + 2Al(OH)₃ → Ca(AlO₂)₂ + 4H₂O"},
{r:["BaOH2","AlOH3"],p:["BaAlO22","H2O"],cond:"",eq:"Ba(OH)₂ + 2Al(OH)₃ → Ba(AlO₂)₂ + 4H₂O"},
{r:["KOH","Al2O3"],p:["KAlO2","H2O"],cond:"",eq:"KOH + Al₂O₃ → KAlO₂ + 3H₂O"},
{r:["CaOH2","Al2O3"],p:["CaAlO22","H2O"],cond:"",eq:"Ca(OH)₂ + Al₂O₃ → Ca(AlO₂)₂ + 3H₂O"},
{r:["BaOH2","Al2O3"],p:["BaAlO22","H2O"],cond:"",eq:"Ba(OH)₂ + Al₂O₃ → Ba(AlO₂)₂ + 3H₂O"},
{r:["KOH","Al","H2O"],p:["KAlO2","H2"],cond:"",eq:"2KOH + 2Al + 2H₂O → 2KAlO₂ + 3H₂"},
{r:["CaOH2","Al","H2O"],p:["CaAlO22","H2"],cond:"",eq:"Ca(OH)₂ + 2Al + 2H₂O → Ca(AlO₂)₂ + 3H₂"},
{r:["BaOH2","Al","H2O"],p:["BaAlO22","H2"],cond:"",eq:"Ba(OH)₂ + 2Al + 2H₂O → Ba(AlO₂)₂ + 3H₂"},

{r:["NaOH","ZnOH2"],p:["Na2ZnO2","H2O"],cond:"",eq:"2NaOH + Zn(OH)₂ → Na₂ZnO₂ + 2H₂O"},
{r:["KOH","ZnOH2"],p:["K2ZnO2","H2O"],cond:"",eq:"2KOH + Zn(OH)₂ → K₂ZnO₂ + 2H₂O"},
{r:["NaOH","ZnO"],p:["Na2ZnO2","H2O"],cond:"",eq:"2NaOH + ZnO → Na₂ZnO₂ + H₂O"},
{r:["NaOH","Zn"],p:["Na2ZnO2","H2"],cond:"",eq:"2NaOH + Zn → Na₂ZnO₂ + H₂"},
{r:["CaOH2","ZnOH2"],p:["CaZnO2","H2O"],cond:"",eq:"Ca(OH)₂ + Zn(OH)₂ → CaZnO₂ + 2H₂O"},
{r:["BaOH2","ZnOH2"],p:["BaZnO2","H2O"],cond:"",eq:"Ba(OH)₂ + Zn(OH)₂ → BaZnO₂ + 2H₂O"},
{r:["KOH","ZnO"],p:["K2ZnO2","H2O"],cond:"",eq:"2KOH + ZnO → K₂ZnO₂ + H₂O"},
{r:["KOH","Zn"],p:["K2ZnO2","H2"],cond:"",eq:"2KOH + Zn → K₂ZnO₂ + H₂"},
{r:["BaOH2","ZnO"],p:["BaZnO2","H2O"],cond:"",eq:"Ba(OH)₂ + ZnO → BaZnO₂ + H₂O"},
{r:["CaOH2","ZnO"],p:["CaZnO2","H2O"],cond:"",eq:"Ca(OH)₂ + ZnO → CaZnO₂ + H₂O"},
{r:["CaOH2","Zn"],p:["CaZnO2","H2"],cond:"",eq:"Ca(OH)₂ + Zn  → CaZnO₂ + H₂"},
{r:["BaOH2","Zn"],p:["BaZnO2","H2"],cond:"",eq:"Ba(OH)₂ + Zn  → BaZnO₂ + H₂"},

// --- oxit bazơ + axit ---
{r:["BaO2","HCl"],p:["BaCl2","H2O2"],cond:"",eq:"BaO₂ + 2HCl → BaCl₂ + H₂O₂"},
{r:["CaO2","HCl"],p:["CaCl2","H2O2"],cond:"",eq:"CaO₂ + 2HCl → CaCl₂ + H₂O₂"},
{r:["Na2O2","HCl"],p:["NaCl","H2O2"],cond:"",eq:"Na₂O₂ + 2HCl → 2NaCl + H₂O₂"},
{r:["K2O2","HCl"],p:["KCl","H2O2"],cond:"",eq:"K₂O₂ + 2HCl → 2KCl + H₂O₂"},
{r:["BaO","HCl"],p:["BaCl2","H2O"],cond:"",eq:"BaO + 2HCl → BaCl₂ + H₂O"},
{r:["CaO","HCl"],p:["CaCl2","H2O"],cond:"",eq:"CaO + 2HCl → CaCl₂ + H₂O"},
{r:["Na2O","HCl"],p:["NaCl","H2O"],cond:"",eq:"Na₂O + 2HCl → 2NaCl + H₂O"},
{r:["K2O","HCl"],p:["KCl","H2O"],cond:"",eq:"K₂O + 2HCl → 2KCl + H₂O"},
{r:["MgO","HCl"],p:["MgCl2","H2O"],cond:"",eq:"MgO + 2HCl → MgCl₂ + H₂O"},
{r:["CuO","HCl"],p:["CuCl2","H2O"],cond:"",eq:"CuO + 2HCl → CuCl₂ + H₂O"},
{r:["Fe3O4","HCl"],p:["FeCl3","FeCl2","H2O"],cond:"",eq:"Fe₃O₄ + 8HCl → 2FeCl₃ + FeCl₂ + 4H₂O"},
{r:["FeO","HCl"],p:["FeCl2","H2O"],cond:"",eq:"FeO + 2HCl → FeCl₂ + H₂O"},
{r:["Fe2O3","HCl"],p:["FeCl3","H2O"],cond:"",eq:"Fe₂O₃ + 6HCl → 2FeCl₃ + 3H₂O"},
{r:["Ag2O","HCl"],p:["AgCl","H2O"],cond:"",eq:"Ag₂O + 2HCl → 2AgCl + H₂O"},
{r:["ZnO","HCl"],p:["ZnCl2","H2O"],cond:"",eq:"ZnO + 2HCl → ZnCl₂ + H₂O"},
{r:["Al2O3","HCl"],p:["AlCl3","H2O"],cond:"",eq:"Al₂O₃ + 6HCl → 2AlCl₃ + 3H₂O"},

{r:["BaO2","H2SO4 loãng"],p:["BaSO4","H2O2"],cond:"",eq:"BaO₂ + H₂SO₄ loãng → BaSO₄ + H₂O₂"},
{r:["CaO2","H2SO4 loãng"],p:["CaSO4","H2O2"],cond:"",eq:"CaO₂ + H₂SO₄ loãng → CaSO₄ + H₂O₂"},
{r:["Na2O2","H2SO4 loãng"],p:["Na2SO4","H2O2"],cond:"",eq:"Na₂O₂ + H₂SO₄ loãng → Na₂SO₄ + H₂O₂"},
{r:["K2O2","H2SO4 loãng"],p:["K2SO4","H2O2"],cond:"",eq:"K₂O₂ + H₂SO₄ loãng → K₂SO₄ + H₂O₂"},
{r:["BaO","H2SO4 loãng"],p:["BaSO4","H2O"],cond:"",eq:"BaO + H₂SO₄ loãng → BaSO₄ + H₂O"},
{r:["CaO","H2SO4 loãng"],p:["CaSO4","H2O"],cond:"",eq:"CaO + H₂SO₄ loãng → CaSO₄ + H₂O"},
{r:["Na2O","H2SO4 loãng"],p:["Na2SO4","H2O"],cond:"",eq:"Na₂O + H₂SO₄ loãng → Na₂SO₄ + H₂O"},
{r:["K2O","H2SO4 loãng"],p:["K2SO4","H2O"],cond:"",eq:"K₂O + H₂SO₄ loãng → K₂SO₄ + H₂O"},
{r:["Fe3O4","H2SO4 loãng"],p:["Fe2SO43","H2O","SO2"],cond:"",eq:"Fe3O4 + 4H2SO4 loãng → Fe2(SO4)3 + FeSO4 + 4H2O"},
{r:["CuO","H2SO4 loãng"],p:["CuSO4","H2O"],cond:"",eq:"CuO + H₂SO₄ loãng → CuSO₄ + H₂O"},
{r:["MgO","H2SO4 loãng"],p:["MgSO4","H2O"],cond:"",eq:"MgO + H₂SO₄ loãng → MgSO₄ + H₂O"},
{r:["Fe2O3","H2SO4 loãng"],p:["Fe2SO43","H2O"],cond:"",eq:"Fe₂O₃ + 3H₂SO₄ loãng → Fe₂(SO₄)₃ + 3H₂O"},
{r:["FeO","H2SO4 loãng"],p:["FeSO4","H2O"],cond:"",eq:"FeO + H₂SO₄ loãng → FeSO₄ + 4H₂O"},
{r:["Ag2O","H2SO4 loãng"],p:["Ag2SO4","H2O"],cond:"",eq:"Ag₂O + H₂SO₄ loãng → Ag₂SO₄ + H₂O"},
{r:["ZnO","H2SO4 loãng"],p:["ZnSO4","H2O"],cond:"",eq:"ZnO + H₂SO₄ loãng → ZnSO₄ + H₂O"},
{r:["Al2O3","H2SO4 loãng"],p:["Al2SO43","H2O"],cond:"",eq:"Al₂O₃ + 3H₂SO₄ loãng → Al₂(SO₄)₃ + 3H₂O"},

{r:["BaO","H2SO4 đặc"],p:["BaSO4","H2O"],cond:"",eq:"BaO + H₂SO₄ đặc → BaSO₄ + H₂O"},
{r:["CaO","H2SO4 đặc"],p:["CaSO4","H2O"],cond:"",eq:"CaO + H₂SO₄ đặc → CaSO₄ + H₂O"},
{r:["Na2O","H2SO4 đặc"],p:["Na2SO4","H2O"],cond:"",eq:"Na₂O + H₂SO₄ đặc → Na₂SO₄ + H₂O"},
{r:["K2O","H2SO4 đặc"],p:["K2SO4","H2O"],cond:"",eq:"K₂O + H₂SO₄ đặc → K₂SO₄ + H₂O"},
{r:["Fe3O4","H2SO4 đặc"],p:["Fe2SO43","H2O","SO2"],cond:"",eq:"Fe₃O₄ + 10H₂SO₄ đặc → 3Fe(SO₄)₃ + SO₂↑ + 10H₂O"},
{r:["CuO","H2SO4 đặc"],p:["CuSO4","H2O"],cond:"",eq:"CuO + H₂SO₄ đặc → CuSO₄ + H₂O"},
{r:["MgO","H2SO4 đặc"],p:["MgSO4","H2O"],cond:"",eq:"MgO + H₂SO₄ đặc → MgSO₄ + H₂O"},
{r:["Fe2O3","H2SO4 đặc"],p:["Fe2SO43","H2O"],cond:"",eq:"Fe₂O₃ + 3H₂SO₄ đặc → Fe₂(SO₄)₃ + 3H₂O"},
{r:["FeO","H2SO4 đặc"],p:["Fe2SO43","H2O","SO2"],cond:"",eq:"3FeO + 4H₂SO₄ đặc → Fe₂(SO₄)₃ + SO₂↑ + 4H₂O"},
{r:["Ag2O","H2SO4 đặc"],p:["Ag2SO4","H2O"],cond:"",eq:"Ag₂O + H₂SO₄ đặc → Ag₂SO₄ + H₂O"},
{r:["ZnO","H2SO4 đặc"],p:["ZnSO4","H2O"],cond:"",eq:"ZnO + H₂SO₄ đặc → ZnSO₄ + H₂O"},
{r:["Al2O3","H2SO4 đặc"],p:["Al2SO43","H2O"],cond:"",eq:"Al₂O₃ + 3H₂SO₄ đặc → Al₂(SO₄)₃ + 3H₂O"},

{r:["BaO2","HNO3"],p:["BaNO32","H2O2"],cond:"",eq:"BaO₂ + 2HNO₃ → Ba(NO₃)₂ + H₂O₂"},
{r:["CaO2","HNO3"],p:["CaNO32","H2O2"],cond:"",eq:"CaO₂ + 2HNO₃ → Ca(NO₃)₂ + H₂O₂"},
{r:["Na2O2","HNO3"],p:["NaNO3","H2O2"],cond:"",eq:"Na₂O₂ + 2HNO₃ → 2NaNO₃ + H₂O₂"},
{r:["K2O2","HNO3"],p:["KNO3","H2O2"],cond:"",eq:"K₂O₂ + 2HNO₃ → 2KNO₃ + H₂O₂"},
{r:["BaO","HNO3"],p:["BaNO32","H2O"],cond:"",eq:"BaO + 2HNO₃ → Ba(NO₃)₂ + H₂O"},
{r:["CaO","HNO3"],p:["CaNO32","H2O"],cond:"",eq:"CaO + 2HNO₃ → Ca(NO₃)₂ + H₂O"},
{r:["Na2O","HNO3"],p:["NaNO3","H2O"],cond:"",eq:"Na₂O + 2HNO₃ → 2NaNO₃ + H₂O"},
{r:["K2O","HNO3"],p:["KNO3","H2O"],cond:"",eq:"K₂O + 2HNO₃ → 2KNO₃ + H₂O"},
{r:["Fe3O4","HNO3"],p:["FeNO33","H2O","NO2"],cond:"",eq:"Fe₃O₄ + 10HNO₃ → 3Fe(NO₃)₃ + NO₂↑ + 5H₂O"},
{r:["CuO","HNO3"],p:["CuNO32","H2O"],cond:"",eq:"CuO + 2HNO₃ → Cu(NO₃)₂ + H₂O"},
{r:["MgO","HNO3"],p:["MgNO32","H2O"],cond:"",eq:"MgO + 2HNO₃ → Mg(NO₃)₂ + H₂O"},
{r:["Fe2O3","HNO3"],p:["FeNO33","H2O"],cond:"",eq:"Fe₂O₃ + 6HNO₃ → 2Fe(NO₃)₃ + 3H₂O"},
{r:["FeO","HNO3"],p:["FeNO33","H2O","NO2"],cond:"",eq:"3FeO + 4HNO₃ → Fe(NO₃)₃ +NO₂↑ + 2H₂O"},
{r:["Ag2O","HNO3"],p:["AgNO3","H2O"],cond:"",eq:"Ag₂O + 2HNO₃ → 2AgNO₃ + H₂O"},
{r:["ZnO","HNO3"],p:["ZnNO32","H2O"],cond:"",eq:"ZnO + 2HNO₃ → Zn(NO₃)₂ + H₂O"},
{r:["Al2O3","HNO3"],p:["AlNO33","H2O"],cond:"",eq:"Al₂O₃ + 6HNO₃ → 2Al(NO₃)₃ + 3H₂O"},

{r:["BaO2","H3PO4"],p:["Ba3PO42","H2O2"],cond:"",eq:"3BaO₂ + 2H₃PO₄ → Ba₃(PO₄)₂ + 3H₂O₂"},
{r:["CaO2","H3PO4"],p:["Ca3PO42","H2O2"],cond:"",eq:"3CaO₂ + 2H₃PO₄ → Ca₃(PO₄)₂ + 3H₂O₂"},
{r:["Na2O2","H3PO4"],p:["Na3PO4","H2O2"],cond:"",eq:"3Na₂O₂ + 2H₃PO₄ → 2Na₃PO₄ + 3H₂O₂"},
{r:["K2O2","H3PO4"],p:["K3PO4","H2O2"],cond:"",eq:"3K₂O₂ + 2H₃PO₄ → 2K₃PO₄ + 3H₂O₂"},
{r:["Na2O","H3PO4"],p:["Na3PO4","H2O"],cond:"",eq:"3Na₂O + 2H₃PO₄ → 2Na₃PO₄ + 3H₂O"},
{r:["K2O","H3PO4"],p:["K3PO4","H2O"],cond:"",eq:"3K₂O + 2H₃PO₄ → 2K₃PO₄ + 3H₂O"},
{r:["CaO","H3PO4"],p:["Ca3PO42","H2O"],cond:"",eq:"3CaO + 2H₃PO₄ → Ca₃(PO₄)₂ + 3H₂O"},
{r:["BaO","H3PO4"],p:["Ba3PO42","H2O"],cond:"",eq:"3BaO + 2H₃PO₄ → Ba₃(PO₄)₂ + 3H₂O"},
{r:["FeO","H3PO4"],p:["Fe3PO42","H2O","NO2"],cond:"",eq:"3FeO + 2H₃PO₄ → Fe₃(PO₄)₂ + 3H₂O"},
{r:["Fe2O3","H3PO4"],p:["FePO4","H2O"],cond:"",eq:"Fe₂O₃ + 2H₃PO₄ → 2FePO₄ + 3H₂O"},
{r:["Ag2O","H3PO4"],p:["Ag3PO4","H2O"],cond:"",eq:"3Ag₂O + 2H₃PO₄ → 2Ag₃PO₄ + 3H₂O"},
{r:["ZnO","H3PO4"],p:["Zn3PO42","H2O"],cond:"",eq:"3ZnO + 2H₃PO₄ → Zn₃(PO₄)₂ + 3H₂O"},
{r:["Al2O3","H3PO4"],p:["AlPO4","H2O"],cond:"",eq:"Al₂O₃ + 2H₃PO₄ → 2AlPO₄ + 3H₂O"},
{r:["MgO","H3PO4"],p:["Mg3PO42","H2O"],cond:"",eq:"3MgO + 2H₃PO₄ → Mg₃(PO₄)₂ + 3H₂O"},
{r:["CuO","H3PO4"],p:["Cu3PO42","H2O"],cond:"",eq:"3CuO + 2H₃PO₄ → Cu₃(PO₄)₂ + 3H₂O"},

// --- axit + muối cacbonat ---
{r:["HCl","CaCO3"],p:["CaCl2","CO2","H2O"],cond:"",eq:"CaCO₃ + 2HCl → CaCl₂ + CO₂↑ + H₂O"},
{r:["HCl","Na2CO3"],p:["NaCl","CO2","H2O"],cond:"",eq:"Na₂CO₃ + 2HCl → 2NaCl + CO₂↑ + H₂O"},
{r:["HCl","NaHCO3"],p:["NaCl","CO2","H2O"],cond:"",eq:"NaHCO₃ + HCl → NaCl + CO₂↑ + H₂O"},
{r:["H2SO4 loãng","Na2CO3"],p:["Na2SO4","CO2","H2O"],cond:"",eq:"Na₂CO₃ + H₂SO₄ → Na₂SO₄ + CO₂↑ + H₂O"},
{r:["H2SO4 loãng","BaCO3"],p:["BaSO4","CO2","H2O"],cond:"",eq:"BaCO₃ + H₂SO₄ → BaSO₄↓ + CO₂↑ + H₂O"},

// --- kim loại đẩy kim loại khỏi muối ---
{r:["Fe","CuSO4"],p:["FeSO4","Cu"],cond:"",eq:"Fe + CuSO₄ → FeSO₄ + Cu"},
{r:["Cu","AgNO3"],p:["CuNO32","Ag"],cond:"",eq:"Cu + 2AgNO₃ → Cu(NO₃)₂ + 2Ag"},
{r:["Zn","CuSO4"],p:["ZnSO4","Cu"],cond:"",eq:"Zn + CuSO₄ → ZnSO₄ + Cu"},
{r:["Fe","AgNO3"],p:["FeNO32","Ag"],cond:"",eq:"Fe + 2AgNO₃ → Fe(NO₃)₂ + 2Ag"},
{r:["Al","CuSO4"],p:["Al2SO43","Cu"],cond:"",eq:"2Al + 3CuSO₄ → Al₂(SO₄)₃ + 3Cu"},
{r:["Mg","CuSO4"],p:["MgSO4","Cu"],cond:"",eq:"Mg + CuSO₄ → MgSO₄ + Cu"},




// --- bazơ + muối (kết tủa hiđroxit) ---
{r:["NaOH","FeCl3"],p:["FeOH3","NaCl"],cond:"",eq:"3NaOH + FeCl₃ → Fe(OH)₃↓ + 3NaCl"},
{r:["NaOH","FeCl2"],p:["FeOH2","NaCl"],cond:"",eq:"2NaOH + FeCl₂ → Fe(OH)₂↓ + 2NaCl"},
{r:["NaOH","CuSO4"],p:["CuOH2","Na2SO4"],cond:"",eq:"2NaOH + CuSO₄ → Cu(OH)₂↓ + Na₂SO₄"},
{r:["NaOH","MgCl2"],p:["MgOH2","NaCl"],cond:"",eq:"2NaOH + MgCl₂ → Mg(OH)₂↓ + 2NaCl"},
{r:["NaOH","AlCl3"],p:["AlOH3","NaCl"],cond:"",eq:"3NaOH + AlCl₃ → Al(OH)₃↓ + 3NaCl"},
{r:["NaOH","ZnCl2"],p:["ZnOH2","NaCl"],cond:"",eq:"2NaOH + ZnCl₂ → Zn(OH)₂↓ + 2NaCl"},
{r:["NaOH","NH4Cl"],p:["NaCl","NH3","H2O"],cond:"t°",eq:"NaOH + NH₄Cl → NaCl + NH₃↑ + H₂O"},
{r:["CaOH2","FeCl3"],p:["FeOH3","CaCl2"],cond:"",eq:"3Ca(OH)2 + 2FeCl3 → 2Fe(OH)3↓ + 3CaCl2"},
{r:["CaOH2","FeCl2"],p:["FeOH2","CaCl2"],cond:"",eq:"Ca(OH)2 + FeCl2 → Fe(OH)2↓ + CaCl2"},
{r:["CaOH2","CuSO4"],p:["CuOH2","CaSO4"],cond:"",eq:"Ca(OH)2 + CuSO4 → Cu(OH)2↓ + CaSO4"},
{r:["CaOH2","MgCl2"],p:["MgOH2","CaCl2"],cond:"",eq:"Ca(OH)2 + MgCl2 → Mg(OH)2↓ + CaCl2"},
{r:["CaOH2","AlCl3"],p:["AlOH3","CaCl2"],cond:"",eq:"3Ca(OH)2 + 2AlCl3 → 2Al(OH)3↓ + 3CaCl₂"},
{r:["CaOH2","ZnCl2"],p:["ZnOH2","CaCl2"],cond:"",eq:"Ca(OH)2 + ZnCl2 → Zn(OH)2↓ + CaCl2"},
{r:["CaOH2","NH4Cl"],p:["CaCl2","NH3","H2O"],cond:"t°",eq:"Ca(OH)2 + 2NH4Cl → CaCl2 + 2NH3↑ + 2H2O"},
{r:["BaOH2","FeCl3"],p:["FeOH3","BaCl2"],cond:"",eq:"3Ba(OH)2 + 2FeCl3 → 2Fe(OH)3↓ + 3BaCl2"},
{r:["BaOH2","FeCl2"],p:["FeOH2","BaCl2"],cond:"",eq:"Ba(OH)2 + FeCl2 → Fe(OH)2↓ + BaCl2"},
{r:["BaOH2","CuSO4"],p:["CuOH2","BaSO4"],cond:"",eq:"Ba(OH)2 + CuSO4 → Cu(OH)2↓ + BaSO4"},
{r:["BaOH2","MgCl2"],p:["MgOH2","BaCl2"],cond:"",eq:"Ba(OH)2 + MgCl2 → Mg(OH)2↓ + BaCl2"},
{r:["BaOH2","AlCl3"],p:["AlOH3","BaCl2"],cond:"",eq:"3Ba(OH)2 + 2AlCl3 → 2Al(OH)3↓ + 3BaCl₂"},
{r:["BaOH2","ZnCl2"],p:["ZnOH2","BaCl2"],cond:"",eq:"Ba(OH)2 + ZnCl2 → Zn(OH)2↓ + BaCl2"},
{r:["BaOH2","NH4Cl"],p:["BaCl2","NH3","H2O"],cond:"t°",eq:"Ba(OH)2 + 2NH4Cl → BaCl2 + 2NH3↑ + 2H2O"},
{r:["KOH","FeCl3"],p:["FeOH3","KCl"],cond:"",eq:"3KOH + FeCl₃ → Fe(OH)₃↓ + 3KCl"},
{r:["KOH","FeCl2"],p:["FeOH2","KCl"],cond:"",eq:"2KOH + FeCl₂ → Fe(OH)₂↓ + 2KCl"},
{r:["KOH","CuSO4"],p:["CuOH2","K2SO4"],cond:"",eq:"2KOH + CuSO₄ → Cu(OH)₂↓ + K₂SO₄"},
{r:["KOH","MgCl2"],p:["MgOH2","KCl"],cond:"",eq:"2KOH + MgCl₂ → Mg(OH)₂↓ + 2KCl"},
{r:["KOH","AlCl3"],p:["AlOH3","KCl"],cond:"",eq:"3KOH + AlCl₃ → Al(OH)₃↓ + 3KCl"},
{r:["KOH","ZnCl2"],p:["ZnOH2","KCl"],cond:"",eq:"2KOH + ZnCl₂ → Zn(OH)₂↓ + 2KCl"},
{r:["KOH","NH4Cl"],p:["KCl","NH3","H2O"],cond:"t°",eq:"KOH + NH₄Cl → KCl + NH₃↑ + H₂O"},







// --- muối + muối (kết tủa) ---
{r:["AgNO3","NaCl"],p:["AgCl","NaNO3"],cond:"",eq:"AgNO₃ + NaCl → AgCl↓ + NaNO₃"},
{r:["AgNO3","KCl"],p:["AgCl","KNO3"],cond:"",eq:"AgNO₃ + KCl → AgCl↓ + KNO₃"},
{r:["AgNO3","CaCl2"],p:["AgCl","CaNO32"],cond:"",eq:"2AgNO₃ + CaCl₂ → 2AgCl↓ + Ca(NO₃)₂"},
{r:["AgNO3","Na2SO4"],p:["Ag2SO4","NaNO3"],cond:"",eq:"2AgNO₃ + Na₂SO₄ → Ag₂SO₄↓ + 2NaNO₃"},
{r:["BaCl2","Na2SO4"],p:["BaSO4","NaCl"],cond:"",eq:"BaCl₂ + Na₂SO₄ → BaSO₄↓ + 2NaCl"},
{r:["BaCl2","K2SO4"],p:["BaSO4","KCl"],cond:"",eq:"BaCl₂ + K₂SO₄ → BaSO₄↓ + 2KCl"},
{r:["AgNO3","Na2S"],p:["Ag2S","NaNO3"],cond:"",eq:"2AgNO₃ + Na₂S → Ag₂S↓ + 2NaNO₃"},
{r:["AgNO3","Na3PO4"],p:["Ag3PO4","NaNO3"],cond:"",eq:"3AgNO₃ + Na₃PO₄ → Ag₃PO₄↓ + 3NaNO₃"},
{r:["Na2CO3","CaCl2"],p:["CaCO3","NaCl"],cond:"",eq:"Na₂CO₃ + CaCl₂ → CaCO₃↓ + 2NaCl"},
{r:["Na2CO3","BaCl2"],p:["BaCO3","NaCl"],cond:"",eq:"Na₂CO₃ + BaCl₂ → BaCO₃↓ + 2NaCl"},
{r:["Na2S","CuSO4"],p:["CuS","Na2SO4"],cond:"",eq:"Na₂S + CuSO₄ → CuS↓ + Na₂SO₄"},
{r:["Na2S","ZnSO4"],p:["ZnS","Na2SO4"],cond:"",eq:"Na₂S + ZnSO₄ → ZnS↓ + Na₂SO₄"},

// --- halogen đẩy nhau ---
{r:["Cl2","NaBr"],p:["NaCl","Br2"],cond:"",eq:"Cl₂ + 2NaBr → 2NaCl + Br₂"},
{r:["Cl2","KI"],p:["KCl","I2"],cond:"",eq:"Cl₂ + 2KI → 2KCl + I₂"},
{r:["Br2","NaI"],p:["NaBr","I2"],cond:"",eq:"Br₂ + 2NaI → 2NaBr + I₂"},


// --- phân huỷ nhiệt ---
{r:["CaCO3"],p:["CaO","CO2"],cond:"t° cao",eq:"CaCO₃ → CaO + CO₂↑"},
{r:["NaHCO3"],p:["Na2CO3","CO2","H2O"],cond:"t°",eq:"2NaHCO₃ → Na₂CO₃ + CO₂↑ + H₂O"},
{r:["CaHCO32"],p:["CaCO3","CO2","H2O"],cond:"t°",eq:"Ca(HCO₃)₂ → CaCO₃↓ + CO₂↑ + H₂O"},
{r:["CuOH2"],p:["CuO","H2O"],cond:"t°",eq:"Cu(OH)₂ → CuO + H₂O"},
{r:["FeOH3"],p:["Fe2O3","H2O"],cond:"t°",eq:"2Fe(OH)₃ → Fe₂O₃ + 3H₂O"},
{r:["NH4Cl"],p:["NH3","HCl"],cond:"t°",eq:"NH₄Cl → NH₃↑ + HCl↑"},
{r:["KMnO4"],p:["K2MnO4","O2"],cond:"t°",eq:"2KMnO₄ → K₂MnO₄ + O₂↑"},

// --- điện phân ---
{r:["H2O"],p:["H2","O2"],cond:"điện phân",eq:"2H₂O → 2H₂↑ + O₂↑"},
{r:["NaCl","H2O"],p:["NaOH","Cl2","H2"],cond:"điện phân dd, màng ngăn",eq:"2NaCl + 2H₂O → 2NaOH + Cl₂↑ + H₂↑"},
{r:["Al2O3"],p:["Al","O2"],cond:"điện phân nóng chảy, criolit",eq:"2Al₂O₃ → 4Al + 3O₂↑"},
{r:["CuCl2"],p:["Cu","Cl2"],cond:"điện phân",eq:"CuCl₂ → Cu + Cl₂↑"},
{r:["H2SO4 loãng"],p:["H2S2O8","H2"],cond:"điện phân dung dịch",eq:"2H₂SO₄ loãng → H₂S₂O₈ + H₂↑"},

// --- khử oxit kim loại ---
{r:["H2","CuO"],p:["Cu","H2O"],cond:"t°",eq:"H₂ + CuO → Cu + H₂O"},
{r:["H2","Fe2O3"],p:["Fe","H2O"],cond:"t°",eq:"3H₂ + Fe₂O₃ → 2Fe + 3H₂O"},
{r:["CO","CuO"],p:["Cu","CO2"],cond:"t°",eq:"CO + CuO → Cu + CO₂"},
{r:["CO","Fe2O3"],p:["Fe","CO2"],cond:"t°",eq:"3CO + Fe₂O₃ → 2Fe + 3CO₂"},
{r:["CO","Fe3O4"],p:["Fe","CO2"],cond:"t°",eq:"4CO + Fe₃O₄ → 3Fe + 4CO₂"},
{r:["C","CO2"],p:["CO"],cond:"t° cao",eq:"C + CO₂ → 2CO"},
{r:["C","Fe2O3"],p:["Fe","CO2"],cond:"t° cao",eq:"3C + 2Fe₂O₃ → 4Fe + 3CO₂"},
{r:["C","CuO"],p:["Cu","CO2"],cond:"t°",eq:"2CuO + C → 2Cu + CO₂"},
{r:["C","SiO2"],p:["Si","CO"],cond:"t° cao",eq:"SiO₂ + 2C → Si + 2CO"},

// --- điều chế cacbua & hoá hữu cơ ---
{r:["CaO","C"],p:["CaC2","CO"],cond:"lò điện, ~2000°C",eq:"CaO + 3C → CaC₂ + CO"},
{r:["Al","C"],p:["Al4C3"],cond:"t° cao",eq:"4Al + 3C → Al₄C₃"},
{r:["CaC2","H2O"],p:["C2H2","CaOH2"],cond:"",eq:"CaC₂ + 2H₂O → C₂H₂↑ + Ca(OH)₂"},
{r:["Al4C3","H2O"],p:["CH4","AlOH3"],cond:"",eq:"Al₄C₃ + 12H₂O → 3CH₄↑ + 4Al(OH)₃"},
{r:["C2H2","H2"],p:["C2H4"],cond:"xt Pd, t°",eq:"C₂H₂ + H₂ → C₂H₄"},
{r:["C2H4","H2"],p:["C2H6"],cond:"xt Ni, t°",eq:"C₂H₄ + H₂ → C₂H₆"},
{r:["C2H4","H2O"],p:["C2H5OH"],cond:"xt axit, t°",eq:"C₂H₄ + H₂O → C₂H₅OH"},
{r:["C2H2","H2O"],p:["CH3CHO"],cond:"xt HgSO₄, t°",eq:"C₂H₂ + H₂O → CH₃CHO"},
{r:["CH3CHO","H2"],p:["C2H5OH"],cond:"xt Ni, t°",eq:"CH₃CHO + H₂ → C₂H₅OH"},
{r:["CH3CHO","O2"],p:["CH3COOH"],cond:"xt Mn²⁺",eq:"2CH₃CHO + O₂ → 2CH₃COOH"},
{r:["C2H5OH","O2"],p:["CH3COOH","H2O"],cond:"men giấm",eq:"C₂H₅OH + O₂ → CH₃COOH + H₂O"},
{r:["C2H5OH","Na"],p:["C2H5ONa","H2"],cond:"",eq:"2C₂H₅OH + 2Na → 2C₂H₅ONa + H₂↑"},
{r:["CH3COOH","Na"],p:["CH3COONa","H2"],cond:"",eq:"2CH₃COOH + 2Na → 2CH₃COONa + H₂↑"},
{r:["CH3COOH","C2H5OH"],p:["CH3COOC2H5","H2O"],cond:"H₂SO₄ đặc, t°",eq:"CH₃COOH + C₂H₅OH ⇌ CH₃COOC₂H₅ + H₂O"},
{r:["CH3COONa","NaOH"],p:["CH4","Na2CO3"],cond:"CaO, t°",eq:"CH₃COONa + NaOH → CH₄↑ + Na₂CO₃"},
{r:["CH4","Cl2"],p:["CH3Cl","HCl"],cond:"ánh sáng",eq:"CH₄ + Cl₂ → CH₃Cl + HCl"},
{r:["C2H6","Cl2"],p:["C2H5Cl","HCl"],cond:"ánh sáng",eq:"C₂H₆ + Cl₂ → C₂H₅Cl + HCl"},
{r:["C6H12O6"],p:["C2H5OH","CO2"],cond:"men rượu, 30-35°C",eq:"C₆H₁₂O₆ → 2C₂H₅OH + 2CO₂↑"},
{r:["C2H2"],p:["C6H6"],cond:"xt, t° cao",eq:"3C₂H₂ → C₆H₆"},
{r:["C2H5OH"],p:["C2H4","H2O"],cond:"H₂SO₄ đặc, 170°C",eq:"C₂H₅OH → C₂H₄↑ + H₂O"},
{r:["CO","H2"],p:["CH3OH"],cond:"xt, t°, p",eq:"CO + 2H₂ → CH₃OH"},
{r:["CH3OH","O2"],p:["HCHO","H2O"],cond:"xt Cu, t°",eq:"2CH₃OH + O₂ → 2HCHO + 2H₂O"},

//==================== HỮU CƠ CƠ BẢN ====================

{r:["C","H2"],p:["CH4"],cond:"xt Ni,t°",eq:"C + 2H₂ → CH₄"},
{r:["CH4","O2"],p:["CH3OH"],cond:"xt",eq:"2CH₄ + O₂ → 2CH₃OH"},
{r:["CH3OH"],p:["CH2O","H2"],cond:"Cu,t°",eq:"CH₃OH → CH₂O + H₂"},
{r:["CH2O","H2"],p:["CH3OH"],cond:"Ni",eq:"CH₂O + H₂ → CH₃OH"},
{r:["CH2O","O2"],p:["HCOOH"],cond:"",eq:"2CH₂O + O₂ → 2HCOOH"},
{r:["HCOOH","NaOH"],p:["HCOONa","H2O"],cond:"",eq:"HCOOH + NaOH → HCOONa + H₂O"},

//==================== ETAN ====================

{r:["CH4"],p:["C2H6","H2"],cond:"t°",eq:"2CH₄ → C₂H₆ + H₂"},
{r:["C2H6"],p:["C2H4","H2"],cond:"xt,t°",eq:"C₂H₆ → C₂H₄ + H₂"},
{r:["C2H4"],p:["C2H2","H2"],cond:"xt,t°",eq:"C₂H₄ → C₂H₂ + H₂"},
{r:["C2H4","H2O"],p:["C2H5OH"],cond:"H₃PO₄",eq:"C₂H₄ + H₂O → C₂H₅OH"},
{r:["C2H5OH"],p:["CH3CHO","H2"],cond:"Cu,t°",eq:"C₂H₅OH → CH₃CHO + H₂"},
{r:["CH3CHO","O2"],p:["CH3COOH"],cond:"",eq:"2CH₃CHO + O₂ → 2CH₃COOH"},
{r:["CH3COOH","NaOH"],p:["CH3COONa","H2O"],cond:"",eq:"CH₃COOH + NaOH → CH₃COONa + H₂O"},

//==================== ESTE ====================

{r:["CH3COOH","C2H5OH"],p:["CH3COOC2H5","H2O"],cond:"H₂SO₄ đặc",eq:"CH₃COOH + C₂H₅OH ⇌ CH₃COOC₂H₅ + H₂O"},
{r:["CH3COOC2H5","H2O"],p:["CH3COOH","C2H5OH"],cond:"H⁺",eq:"CH₃COOC₂H₅ + H₂O ⇌ CH₃COOH + C₂H₅OH"},

//==================== GLUCO ====================

{r:["CO2","H2O"],p:["C6H12O6","O2"],cond:"ánh sáng",eq:"6CO₂ + 6H₂O → C₆H₁₂O₆ + 6O₂"},
{r:["C6H12O6"],p:["C2H5OH","CO2"],cond:"men",eq:"C₆H₁₂O₆ → 2C₂H₅OH + 2CO₂"},
{r:["C6H12O6","O2"],p:["CO2","H2O"],cond:"",eq:"C₆H₁₂O₆ + 6O₂ → 6CO₂ + 6H₂O"},

//==================== BENZEN ====================

{r:["C2H2"],p:["C6H6"],cond:"xt,t°",eq:"3C₂H₂ → C₆H₆"},
{r:["C6H6","H2"],p:["C6H12"],cond:"Ni",eq:"C₆H₆ + 3H₂ → C₆H₁₂"},
{r:["C6H6","Cl2"],p:["C6H5Cl","HCl"],cond:"FeCl₃",eq:"C₆H₆ + Cl₂ → C₆H₅Cl + HCl"},

//==================== POLIME ====================

{r:["C2H4"],p:["PE"],cond:"xt,p",eq:"nC₂H₄ → (–CH₂–CH₂–)ₙ"},
{r:["C2H2"],p:["PVC"],cond:"xt",eq:"nCH₂=CHCl → PVC"},
{r:["C6H5Cl"],p:["PS"],cond:"xt",eq:"nC₈H₈ → PS"},
// --- điều chế khác ---
{r:["MnO2","KClO3","KOH"],p:["K2MnO4","KCl","H2O"],cond:"t° cao",eq:" 3MnO₂ + KClO₃ + 6KOH → 3K₂MnO₄ + KCl + 3H₂O"},
{r:["K2MnO4","Cl2"],p:["KMnO4","KCl"],cond:"t° cao",eq:" 2K₂MnO₄ + Cl₂ → 2KMnO₄ + 2KCl"},
{r:["H2S2O8","H2O"],p:["H2SO4 loãng","H2O2"],cond:"t° cao",eq:" H2S2O8 + H2O → H2SO4 + H2O2"},
{r:["Na","H2"],p:["NaH"],cond:"t° cao",eq:" 2Na + H₂ → 2NaH"},
{r:["K","H2"],p:["KH"],cond:"t° cao",eq:" 2K + H₂ → 2KH"},
{r:["Ba","H2"],p:["BaH2"],cond:"t° cao",eq:" 2Ba + H₂ → 2BaH₂"},
{r:["Ca","H2"],p:["CaH2"],cond:"t° cao",eq:" 2Ca + H₂ → 2CaH₂"},



// ===== PHẢN ỨNG BỔ SUNG: CÂN BẰNG, AXIT–BAZƠ VÀ PHÂN HỦY =====
{r:["NO2","NO2"],p:["N2O4"],cond:"nhiệt độ thấp / cân bằng",eq:"2NO₂ ⇌ N₂O₄"},
{r:["N2O4","H2O"],p:["HNO2","HNO3"],cond:"",eq:"N₂O₄ + H₂O → HNO₂ + HNO₃"},
{r:["H2O2","H2O2"],p:["H2O","H2O","O2"],cond:"xúc tác phù hợp",eq:"2H₂O₂ → 2H₂O + O₂↑"},
{r:["H2C2O4","NaOH"],p:["Na2C2O4","H2O","H2O"],cond:"trung hòa",eq:"H₂C₂O₄ + 2NaOH → Na₂C₂O₄ + 2H₂O"},
{r:["Na2C2O4","CaCl2"],p:["CaC2O4","NaCl","NaCl"],cond:"dung dịch",eq:"Na₂C₂O₄ + CaCl₂ → CaC₂O₄↓ + 2NaCl"},
{r:["H3PO4","NaOH"],p:["NaH2PO4","H2O"],cond:"tỉ lệ mol 1:1",eq:"H₃PO₄ + NaOH → NaH₂PO₄ + H₂O"},
{r:["H3PO4","NaOH"],p:["Na2HPO4","H2O","H2O"],cond:"tỉ lệ mol 1:2",eq:"H₃PO₄ + 2NaOH → Na₂HPO₄ + 2H₂O"},
{r:["H3PO4","KOH"],p:["K2HPO4","H2O","H2O"],cond:"tỉ lệ mol 1:2",eq:"H₃PO₄ + 2KOH → K₂HPO₄ + 2H₂O"},
{r:["CaOH2","CO2"],p:["CaCO3","H2O"],cond:"sục CO₂ vừa đủ",eq:"Ca(OH)₂ + CO₂ → CaCO₃↓ + H₂O"},
{r:["FeS2","O2"],p:["Fe2O3","Fe2O3","SO2","SO2","SO2","SO2","SO2","SO2","SO2","SO2"],cond:"nhiệt độ cao (phương trình minh họa)",eq:"4FeS₂ + 11O₂ → 2Fe₂O₃ + 8SO₂↑"},
// ===== MỞ RỘNG: ĐỒNG PHÂN, PHÂN HỦY, AXIT–BAZƠ VÀ PHẢN ỨNG VÔ CƠ =====
{r:["H2O2","H2O2"],p:["H2O","H2O","O2"],cond:"xúc tác phù hợp",eq:"2H₂O₂ → 2H₂O + O₂↑"},
{r:["KClO3","KClO3"],p:["KCl","KCl","O2","O2","O2"],cond:"phân hủy nhiệt — phương trình học tập",eq:"2KClO₃ → 2KCl + 3O₂↑"},
{r:["NaNO3","NaNO3"],p:["NaNO2","NaNO2","O2"],cond:"phân hủy nhiệt",eq:"2NaNO₃ → 2NaNO₂ + O₂↑"},
{r:["NH4NO2"],p:["N2","H2O","H2O"],cond:"phân hủy",eq:"NH₄NO₂ → N₂↑ + 2H₂O"},
{r:["NH3","HNO2"],p:["NH4NO2"],cond:"axit–bazơ",eq:"NH₃ + HNO₂ → NH₄NO₂"},
{r:["SO3","NaOH","NaOH"],p:["Na2SO4","H2O"],cond:"trung hòa",eq:"SO₃ + 2NaOH → Na₂SO₄ + H₂O"},
{r:["SO2","NaOH","NaOH"],p:["Na2SO3","H2O"],cond:"trung hòa",eq:"SO₂ + 2NaOH → Na₂SO₃ + H₂O"},
{r:["CO2","NaOH","NaOH"],p:["Na2CO3","H2O"],cond:"NaOH dư",eq:"CO₂ + 2NaOH → Na₂CO₃ + H₂O"},
{r:["CO2","NaOH"],p:["NaHCO3"],cond:"NaOH tỉ lệ 1:1",eq:"CO₂ + NaOH → NaHCO₃"},
{r:["AgNO3","NaBr"],p:["AgBr","NaNO3"],cond:"dung dịch",eq:"AgNO₃ + NaBr → AgBr↓ + NaNO₃"},
{r:["AgNO3","NaI"],p:["AgI","NaNO3"],cond:"dung dịch",eq:"AgNO₃ + NaI → AgI↓ + NaNO₃"},
{r:["PbNO32","KI","KI"],p:["PbI2","KNO3","KNO3"],cond:"dung dịch",eq:"Pb(NO₃)₂ + 2KI → PbI₂↓ + 2KNO₃"},
{r:["BaCl2","K2CrO4"],p:["BaCrO4","KCl","KCl"],cond:"dung dịch",eq:"BaCl₂ + K₂CrO₄ → BaCrO₄↓ + 2KCl"},
{r:["Zn","AgNO3","AgNO3"],p:["ZnNO32","Ag","Ag"],cond:"phản ứng thế",eq:"Zn + 2AgNO₃ → Zn(NO₃)₂ + 2Ag"},
{r:["FeCl2","FeCl2","Cl2"],p:["FeCl3","FeCl3"],cond:"oxi hóa",eq:"2FeCl₂ + Cl₂ → 2FeCl₃"},
{r:["Fe","FeCl3","FeCl3"],p:["FeCl2","FeCl2","FeCl2"],cond:"oxi hóa–khử",eq:"Fe + 2FeCl₃ → 3FeCl₂"},
{r:["Al","Al","CuCl2","CuCl2","CuCl2"],p:["AlCl3","AlCl3","Cu","Cu","Cu"],cond:"phản ứng thế — mô hình phương trình",eq:"2Al + 3CuCl₂ → 2AlCl₃ + 3Cu"},
{r:["Na2S2O3","HCl","HCl"],p:["NaCl","NaCl","SO2","S","H2O"],cond:"axit hóa dung dịch",eq:"Na₂S₂O₃ + 2HCl → 2NaCl + SO₂↑ + S↓ + H₂O"},
{r:["Na2SO3","HCl","HCl"],p:["NaCl","NaCl","SO2","H2O"],cond:"axit hóa",eq:"Na₂SO₃ + 2HCl → 2NaCl + SO₂↑ + H₂O"},
{r:["KMnO4","KMnO4"],p:["K2MnO4","MnO2","O2"],cond:"phân hủy nhiệt",eq:"2KMnO₄ → K₂MnO₄ + MnO₂ + O₂↑"},
{r:["PbNO32","PbNO32"],p:["PbO","PbO","NO2","NO2","NO2","NO2","O2"],cond:"phân hủy nhiệt — phương trình học tập",eq:"2Pb(NO₃)₂ → 2PbO + 4NO₂↑ + O₂↑"},
{r:["CuNO32","CuNO32"],p:["CuO","CuO","NO2","NO2","NO2","NO2","O2"],cond:"phân hủy nhiệt",eq:"2Cu(NO₃)₂ → 2CuO + 4NO₂↑ + O₂↑"},
{r:["HgO","HgO"],p:["Hg","Hg","O2"],cond:"phân hủy nhiệt",eq:"2HgO → 2Hg + O₂↑"},
{r:["NaHCO3","NaHCO3"],p:["Na2CO3","CO2","H2O"],cond:"đun nóng",eq:"2NaHCO₃ → Na₂CO₃ + CO₂↑ + H₂O"},
{r:["HCl","NaHCO3"],p:["NaCl","CO2","H2O"],cond:"axit + hiđrocacbonat",eq:"HCl + NaHCO₃ → NaCl + CO₂↑ + H₂O"},
{r:["HCl","HCl","Na2CO3"],p:["NaCl","NaCl","CO2","H2O"],cond:"axit + cacbonat",eq:"2HCl + Na₂CO₃ → 2NaCl + CO₂↑ + H₂O"},
{r:["Na2S","HCl","HCl"],p:["NaCl","NaCl","H2S"],cond:"axit + sunfua",eq:"Na₂S + 2HCl → 2NaCl + H₂S↑"},
{r:["CaCO3","CO2","H2O"],p:["CaHCO32"],cond:"CO₂ dư trong nước",eq:"CaCO₃ + CO₂ + H₂O → Ca(HCO₃)₂"},
{r:["Propene","H2"],p:["C3H8"],cond:"xúc tác Ni",eq:"CH₂=CH–CH₃ + H₂ → CH₃–CH₂–CH₃"},
{r:["Cyclopropane","H2"],p:["C3H8"],cond:"hiđro hóa vòng — mô hình",eq:"C₃H₆ + H₂ → C₃H₈"},
{r:["Butene1","H2"],p:["Butane"],cond:"xúc tác Ni",eq:"CH₂=CHCH₂CH₃ + H₂ → CH₃CH₂CH₂CH₃"},
{r:["Isobutene","H2"],p:["Isobutane"],cond:"xúc tác Ni",eq:"CH₂=C(CH₃)₂ + H₂ → (CH₃)₃CH"},
{r:["Butene1"],p:["cisButene2"],cond:"đồng phân hóa (mô hình)",eq:"But-1-en ⇌ cis-but-2-en"},
{r:["cisButene2"],p:["transButene2"],cond:"đồng phân hóa hình học (mô hình) ",eq:"cis-but-2-en ⇌ trans-but-2-en"},
{r:["Butane"],p:["Isobutane"],cond:"đồng phân hóa mạch carbon",eq:"n-C₄H₁₀ ⇌ iso-C₄H₁₀"},
{r:["Pentane"],p:["Isopentane"],cond:"đồng phân hóa mạch carbon",eq:"n-C₅H₁₂ ⇌ iso-C₅H₁₂"},
{r:["Isopentane"],p:["Neopentane"],cond:"đồng phân hóa mạch carbon (mô hình)",eq:"2-metylbutan ⇌ 2,2-đimetylpropan"},
{r:["Propan1ol"],p:["Propene","H2O"],cond:"tách nước, xúc tác axit (phương trình tổng quát)",eq:"CH₃CH₂CH₂OH → CH₂=CHCH₃ + H₂O"},
{r:["Propan2ol"],p:["Propene","H2O"],cond:"tách nước, xúc tác axit (phương trình tổng quát)",eq:"(CH₃)₂CHOH → CH₂=CHCH₃ + H₂O"},
{r:["Propanal","H2"],p:["Propan1ol"],cond:"hiđro hóa nhóm carbonyl",eq:"CH₃CH₂CHO + H₂ → CH₃CH₂CH₂OH"},
{r:["Propanal","O2"],p:["PropanoicAcid"],cond:"oxi hóa",eq:"2CH₃CH₂CHO + O₂ → 2CH₃CH₂COOH"},
{r:["CH3COCH3","H2"],p:["Propan2ol"],cond:"hiđro hóa nhóm carbonyl",eq:"CH₃COCH₃ + H₂ → CH₃CHOHCH₃"},
{r:["PropanoicAcid","C2H5OH"],p:["EthylPropanoate","H2O"],cond:"este hóa thuận nghịch, xúc tác axit",eq:"CH₃CH₂COOH + C₂H₅OH ⇌ CH₃CH₂COOC₂H₅ + H₂O"},
{r:["PropanoicAcid","CH3OH"],p:["MethylPropanoate","H2O"],cond:"este hóa thuận nghịch, xúc tác axit",eq:"CH₃CH₂COOH + CH₃OH ⇌ CH₃CH₂COOCH₃ + H₂O"},
{r:["EthylPropanoate","H2O"],p:["PropanoicAcid","C2H5OH"],cond:"thủy phân este, xúc tác axit",eq:"CH₃CH₂COOC₂H₅ + H₂O ⇌ CH₃CH₂COOH + C₂H₅OH"},
{r:["Fructose"],p:["C2H5OH","C2H5OH","CO2","CO2"],cond:"lên men — phương trình tổng quát",eq:"C₆H₁₂O₆ → 2C₂H₅OH + 2CO₂↑"},
{r:["Galactose"],p:["C2H5OH","C2H5OH","CO2","CO2"],cond:"lên men — mô hình tổng quát",eq:"C₆H₁₂O₆ → 2C₂H₅OH + 2CO₂↑"},
{r:["Butane","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2"],p:["CO2","CO2","CO2","CO2","CO2","CO2","CO2","CO2","H2O","H2O","H2O","H2O","H2O"],cond:"cháy hoàn toàn — phương trình cân bằng",eq:"2C₄H₁₀ + 13O₂ → 8CO₂ + 10H₂O"},
{r:["Isobutane","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2"],p:["CO2","CO2","CO2","CO2","CO2","CO2","CO2","CO2","H2O","H2O","H2O","H2O","H2O"],cond:"cháy hoàn toàn — phương trình cân bằng",eq:"2(CH₃)₃CH + 13O₂ → 8CO₂ + 10H₂O"},
{r:["Pentane","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2"],p:["CO2","CO2","CO2","CO2","CO2","CO2","CO2","CO2","CO2","CO2","H2O","H2O","H2O","H2O","H2O","H2O"],cond:"cháy hoàn toàn — phương trình cân bằng",eq:"C₅H₁₂ + 8O₂ → 5CO₂ + 6H₂O"},
{r:["Neopentane","O2","O2","O2","O2","O2","O2","O2"],p:["CO2","CO2","CO2","CO2","CO2","H2O","H2O","H2O","H2O","H2O","H2O"],cond:"cháy hoàn toàn — phương trình cân bằng",eq:"C₅H₁₂ + 8O₂ → 5CO₂ + 6H₂O"},
{r:["MethylPropanoate","H2O"],p:["PropanoicAcid","CH3OH"],cond:"thủy phân este, xúc tác axit",eq:"CH₃CH₂COOCH₃ + H₂O ⇌ CH₃CH₂COOH + CH₃OH"},
{r:["MaleicAcid"],p:["FumaricAcid"],cond:"đồng phân hóa hình học (mô hình)",eq:"Axit maleic ⇌ axit fumaric"},
{r:["OrthoXylene","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2","O2"],p:["CO2","CO2","CO2","CO2","CO2","CO2","CO2","CO2","H2O","H2O","H2O","H2O","H2O"],cond:"cháy hoàn toàn — phương trình cân bằng",eq:"2C₈H₁₀ + 21O₂ → 16CO₂ + 10H₂O"},
{r:["ParaXylene"],p:["MetaXylene"],cond:"đồng phân hóa vị trí — mô hình khái niệm",eq:"p-xylen ⇌ m-xylen"},
{r:["HClO3","NaOH"],p:["NaClO3","H2O"],cond:"trung hòa",eq:"HClO₃ + NaOH → NaClO₃ + H₂O"},
{r:["HClO4","KOH"],p:["KClO4","H2O"],cond:"trung hòa",eq:"HClO₄ + KOH → KClO₄ + H₂O"},
{r:["CrO3","H2O"],p:["H2CrO4"],cond:"hình thành axit trong mô hình dung dịch",eq:"CrO₃ + H₂O → H₂CrO₄"},
{r:["SnO2","H2","H2"],p:["Sn","H2O","H2O"],cond:"khử oxit — phương trình tổng quát",eq:"SnO₂ + 2H₂ → Sn + 2H₂O"},
{r:["PbO","H2"],p:["Pb","H2O"],cond:"khử oxit — phương trình tổng quát",eq:"PbO + H₂ → Pb + H₂O"},
{r:["NiO","H2"],p:["Ni","H2O"],cond:"khử oxit — phương trình tổng quát",eq:"NiO + H₂ → Ni + H₂O"},
{r:["Mn2O3","H2","H2","H2"],p:["Mn","Mn","Mn","H2O","H2O","H2O"],cond:"khử oxit — phương trình tổng quát",eq:"Mn₂O₃ + 3H₂ → 2Mn + 3H₂O"},
{r:["TiO2","C","C"],p:["Ti","CO","CO"],cond:"phương trình khử tổng quát; điều kiện thực tế phức tạp",eq:"TiO₂ + 2C → Ti + 2CO"},
{r:["V2O5","H2","H2","H2","H2","H2"],p:["V","V","V","V","V","H2O","H2O","H2O","H2O","H2O"],cond:"khử oxit — phương trình tổng quát",eq:"V₂O₅ + 5H₂ → 2V + 5H₂O"},
{r:["MoO3","H2","H2","H2"],p:["Mo","H2O","H2O","H2O"],cond:"khử oxit — phương trình tổng quát",eq:"MoO₃ + 3H₂ → Mo + 3H₂O"},
{r:["WO3","H2","H2","H2"],p:["W","H2O","H2O","H2O"],cond:"khử oxit — phương trình tổng quát",eq:"WO₃ + 3H₂ → W + 3H₂O"},
{r:["ZnO","H2"],p:["Zn","H2O"],cond:"khử oxit — mô hình tổng quát",eq:"ZnO + H₂ → Zn + H₂O"},
{r:["CuO","CO"],p:["Cu","CO2"],cond:"khử oxit",eq:"CuO + CO → Cu + CO₂"},
{r:["PbO2","H2","H2"],p:["Pb","H2O","H2O"],cond:"khử oxit — phương trình tổng quát",eq:"PbO₂ + 2H₂ → Pb + 2H₂O"},
{r:["H2CrO4","NaOH","NaOH"],p:["Na2CrO4","H2O","H2O"],cond:"trung hòa — phương trình tổng quát",eq:"H₂CrO₄ + 2NaOH → Na₂CrO₄ + 2H₂O"},
{r:["NaBrO3"],p:["NaBr","O2","O2","O2"],cond:"phân hủy nhiệt — phương trình tổng quát",eq:"2NaBrO₃ → 2NaBr + 3O₂↑"},
{r:["NaIO3","NaIO3"],p:["NaI","NaI","O2","O2","O2"],cond:"phân hủy nhiệt — phương trình tổng quát",eq:"2NaIO₃ → 2NaI + 3O₂↑"},
{r:["MethylEthylEther","H2"],p:["Propan1ol"],cond:"không gắn trực tiếp thành phản ứng thực nghiệm; dùng thẻ đồng phân để so sánh",eq:"Metoxyetan và propan-1-ol cùng công thức C₃H₈O nhưng khác nhóm chức"}
];

/* =========================================================
   KHO CHẤT MỞ RỘNG — các hợp chất mới đều bắt đầu ở trạng thái khóa.
   Chúng chỉ được mở khóa khi được tạo ra bởi một phản ứng bên dưới.
   ========================================================= */
Object.assign(S, {
  // Nitơ, nitrua và hợp chất vô cơ bổ sung
  N2O3:{f:"N₂O₃",n:"Đinitơ trioxit",c:"oxide"},
  Li3N:{f:"Li₃N",n:"Liti nitrua",c:"salt"},
  Ca3N2:{f:"Ca₃N₂",n:"Canxi nitrua",c:"salt"},
  Sr3N2:{f:"Sr₃N₂",n:"Stronti nitrua",c:"salt"},
  K2S:{f:"K₂S",n:"Kali sunfua",c:"salt"},
  SnS:{f:"SnS",n:"Thiếc(II) sunfua",c:"salt"},
  HgS:{f:"HgS",n:"Thủy ngân(II) sunfua",c:"salt"},
  Zn3P2:{f:"Zn₃P₂",n:"Kẽm photphua",c:"salt"},
  Ca3P2:{f:"Ca₃P₂",n:"Canxi photphua",c:"salt"},
  Mg3P2:{f:"Mg₃P₂",n:"Magie photphua",c:"salt"},
  FeSi:{f:"FeSi",n:"Sắt silixua",c:"other"},
  CaSi2:{f:"CaSi₂",n:"Canxi đisilixua",c:"other"},
  TiSi2:{f:"TiSi₂",n:"Titan đisilixua",c:"other"},
  BF3:{f:"BF₃",n:"Bo triflorua",c:"other"},
  CF4:{f:"CF₄",n:"Cacbon tetraflorua",c:"other"},
  SF6:{f:"SF₆",n:"Lưu huỳnh hexaflorua",c:"other"},
  SiF4:{f:"SiF₄",n:"Silic tetraflorua",c:"other"},
  ZnF2:{f:"ZnF₂",n:"Kẽm florua",c:"salt"},
  NaF:{f:"NaF",n:"Natri florua",c:"salt"},
  KF:{f:"KF",n:"Kali florua",c:"salt"},
  CaF2:{f:"CaF₂",n:"Canxi florua",c:"salt"},
  PF5:{f:"PF₅",n:"Photpho pentaflorua",c:"other"},
  PBr3:{f:"PBr₃",n:"Photpho tribromua",c:"other"},
  H2Se:{f:"H₂Se",n:"Hiđro selenua",c:"acid"},
  H2Te:{f:"H₂Te",n:"Hiđro telurua",c:"acid"},
  HBrO3:{f:"HBrO₃",n:"Axit bromic",c:"acid"},
  HIO3:{f:"HIO₃",n:"Axit iodic",c:"acid"},
  H2SeO4:{f:"H₂SeO₄",n:"Axit selenic",c:"acid"},
  H3PO3:{f:"H₃PO₃",n:"Axit photphorơ",c:"acid"},
  HMnO4:{f:"HMnO₄",n:"Axit pemanganic",c:"acid"},
  Na3AlF6:{f:"Na₃AlF₆",n:"Natri hexafloroaluminat (criolit)",c:"salt"},
  Na2WO4:{f:"Na₂WO₄",n:"Natri vonframat",c:"salt"},
  K2WO4:{f:"K₂WO₄",n:"Kali vonframat",c:"salt"},
  Na2MoO4:{f:"Na₂MoO₄",n:"Natri molypđat",c:"salt"},
  K2MoO4:{f:"K₂MoO₄",n:"Kali molypđat",c:"salt"},
  BaTiO3:{f:"BaTiO₃",n:"Bari titanat",c:"salt"},
  PbCrO4:{f:"PbCrO₄",n:"Chì(II) cromat",c:"salt"},
  B4C:{f:"B₄C",n:"Bo cacbua",c:"other"},
  TiB2:{f:"TiB₂",n:"Titan điborua",c:"other"},
  TiN:{f:"TiN",n:"Titan nitrua",c:"salt"},
  ZrN:{f:"ZrN",n:"Zirconi nitrua",c:"salt"},
  ZnSe:{f:"ZnSe",n:"Kẽm selenua",c:"salt"},
  CdSe:{f:"CdSe",n:"Cadimi selenua",c:"salt"},
  PbSe:{f:"PbSe",n:"Chì(II) selenua",c:"salt"},
  Na2Se:{f:"Na₂Se",n:"Natri selenua",c:"salt"},
  K2Se:{f:"K₂Se",n:"Kali selenua",c:"salt"},
  MnO:{f:"MnO",n:"Mangan(II) oxit",c:"oxide"},
  V2O3:{f:"V₂O₃",n:"Vanadi(III) oxit",c:"oxide"},
  VO2:{f:"VO₂",n:"Vanadi(IV) oxit",c:"oxide"},
  TiO:{f:"TiO",n:"Titan(II) oxit",c:"oxide"},
  EthyleneOxide:{f:"C₂H₄O",n:"Etylen oxit (oxiran)",c:"organic"},
  Toluene:{f:"C₆H₅CH₃",n:"Toluen",c:"organic"},
  Ethylbenzene:{f:"C₆H₅C₂H₅",n:"Etylbenzen",c:"organic"},
  Nitrobenzene:{f:"C₆H₅NO₂",n:"Nitrobenzen",c:"organic"},
  Aniline:{f:"C₆H₅NH₂",n:"Anilin",c:"organic"},
  Benzaldehyde:{f:"C₆H₅CHO",n:"Benzanđehit",c:"organic"},
  BenzylAlcohol:{f:"C₆H₅CH₂OH",n:"Ancol benzylic",c:"organic"},
  BenzoicAcid:{f:"C₆H₅COOH",n:"Axit benzoic",c:"organic"},
  SodiumSalicylate:{f:"C₇H₅NaO₃",n:"Natri salicylat",c:"salt"},
  SalicylicAcid:{f:"HO–C₆H₄–COOH",n:"Axit salicylic",c:"organic"},
  Acetamide:{f:"CH₃CONH₂",n:"Axetamid",c:"organic"},
  AceticAnhydride:{f:"(CH₃CO)₂O",n:"Anhiđrit axetic",c:"organic"},
  Aspirin:{f:"C₉H₈O₄",n:"Axit axetylsalicylic (aspirin)",c:"organic"},
  MethylBenzoate:{f:"C₆H₅COOCH₃",n:"Metyl benzoat",c:"organic"}
});

/* Các phản ứng bổ sung. Chúng tuân theo cùng engine và cơ chế mở khóa gốc. */
R.push(
  {r:["NO","NO2"],p:["N2O3"],cond:"nhiệt độ thấp / cân bằng",eq:"NO + NO₂ ⇌ N₂O₃"},
  {r:["Li","N2"],p:["Li3N"],cond:"t°",eq:"6Li + N₂ → 2Li₃N"},
  {r:["Ca","N2"],p:["Ca3N2"],cond:"t°",eq:"3Ca + N₂ → Ca₃N₂"},
  {r:["Sr","N2"],p:["Sr3N2"],cond:"t°",eq:"3Sr + N₂ → Sr₃N₂"},
  {r:["K","S"],p:["K2S"],cond:"t°",eq:"2K + S → K₂S"},
  {r:["Sn","S"],p:["SnS"],cond:"t°",eq:"Sn + S → SnS"},
  {r:["Hg","S"],p:["HgS"],cond:"mô phỏng phản ứng kết hợp",eq:"Hg + S → HgS"},
  {r:["Zn","P"],p:["Zn3P2"],cond:"t°",eq:"3Zn + 2P → Zn₃P₂"},
  {r:["Ca","P"],p:["Ca3P2"],cond:"t°",eq:"3Ca + 2P → Ca₃P₂"},
  {r:["Mg","P"],p:["Mg3P2"],cond:"t°",eq:"3Mg + 2P → Mg₃P₂"},
  {r:["Fe","Si"],p:["FeSi"],cond:"nhiệt độ cao",eq:"Fe + Si → FeSi"},
  {r:["Ca","Si"],p:["CaSi2"],cond:"nhiệt độ cao",eq:"Ca + 2Si → CaSi₂"},
  {r:["Ti","Si"],p:["TiSi2"],cond:"nhiệt độ cao",eq:"Ti + 2Si → TiSi₂"},
  {r:["B","F2"],p:["BF3"],cond:"phương trình mô hình",eq:"2B + 3F₂ → 2BF₃"},
  {r:["C","F2"],p:["CF4"],cond:"phương trình mô hình",eq:"C + 2F₂ → CF₄"},
  {r:["S","F2"],p:["SF6"],cond:"phương trình mô hình",eq:"S + 3F₂ → SF₆"},
  {r:["Si","F2"],p:["SiF4"],cond:"phương trình mô hình",eq:"Si + 2F₂ → SiF₄"},
  {r:["Zn","F2"],p:["ZnF2"],cond:"t°",eq:"Zn + F₂ → ZnF₂"},
  {r:["Na","F2"],p:["NaF"],cond:"phương trình kết hợp",eq:"2Na + F₂ → 2NaF"},
  {r:["K","F2"],p:["KF"],cond:"phương trình kết hợp",eq:"2K + F₂ → 2KF"},
  {r:["Ca","F2"],p:["CaF2"],cond:"phương trình kết hợp",eq:"Ca + F₂ → CaF₂"},
  {r:["P","F2"],p:["PF5"],cond:"phương trình mô hình",eq:"2P + 5F₂ → 2PF₅"},
  {r:["P","Br2"],p:["PBr3"],cond:"t°",eq:"2P + 3Br₂ → 2PBr₃"},
  {r:["H2","Se"],p:["H2Se"],cond:"phương trình kết hợp mô hình",eq:"H₂ + Se → H₂Se"},
  {r:["H2","Te"],p:["H2Te"],cond:"phương trình kết hợp mô hình",eq:"H₂ + Te → H₂Te"},
  {r:["Br2","O3","H2O"],p:["HBrO3"],cond:"oxi hóa — mô hình khái niệm",eq:"3Br₂ + 5O₃ + 3H₂O → 6HBrO₃"},
  {r:["I2","O3","H2O"],p:["HIO3"],cond:"oxi hóa — mô hình khái niệm",eq:"3I₂ + 5O₃ + 3H₂O → 6HIO₃"},
  {r:["H2Se","O2"],p:["H2SeO4"],cond:"oxi hóa",eq:"H₂Se + 2O₂ → H₂SeO₄"},
  {r:["P","O2","H2O"],p:["H3PO3"],cond:"oxi hóa có kiểm soát — mô hình",eq:"4P + 3O₂ + 6H₂O → 4H₃PO₃"},
  {r:["MnO2","KOH","O2"],p:["K2MnO4","H2O"],cond:"oxi hóa trong môi trường kiềm — mô hình",eq:"2MnO₂ + 4KOH + O₂ → 2K₂MnO₄ + 2H₂O"},
  {r:["KMnO4","H2SO4 loãng"],p:["HMnO4","KHSO4"],cond:"axit hóa — mô hình khái niệm",eq:"KMnO₄ + H₂SO₄ → HMnO₄ + KHSO₄"},
  {r:["NaF","AlF3"],p:["Na3AlF6"],cond:"nhiệt độ cao",eq:"3NaF + AlF₃ → Na₃AlF₆"},
  {r:["W","O2"],p:["WO3"],cond:"t°",eq:"2W + 3O₂ → 2WO₃"},
  {r:["Mo","O2"],p:["MoO3"],cond:"t°",eq:"2Mo + 3O₂ → 2MoO₃"},
  {r:["WO3","NaOH"],p:["Na2WO4","H2O"],cond:"nóng chảy",eq:"WO₃ + 2NaOH → Na₂WO₄ + H₂O"},
  {r:["WO3","KOH"],p:["K2WO4","H2O"],cond:"nóng chảy",eq:"WO₃ + 2KOH → K₂WO₄ + H₂O"},
  {r:["MoO3","NaOH"],p:["Na2MoO4","H2O"],cond:"nóng chảy",eq:"MoO₃ + 2NaOH → Na₂MoO₄ + H₂O"},
  {r:["MoO3","KOH"],p:["K2MoO4","H2O"],cond:"nóng chảy",eq:"MoO₃ + 2KOH → K₂MoO₄ + H₂O"},
  {r:["Ti","O2"],p:["TiO2"],cond:"t°",eq:"Ti + O₂ → TiO₂"},
  {r:["BaO","TiO2"],p:["BaTiO3"],cond:"nung gốm — mô hình",eq:"BaO + TiO₂ → BaTiO₃"},
  {r:["Cr2O3","KOH","O2"],p:["K2CrO4","H2O"],cond:"oxi hóa trong kiềm — mô hình",eq:"2Cr₂O₃ + 8KOH + 3O₂ → 4K₂CrO₄ + 4H₂O"},
  {r:["Pb","O2"],p:["PbO"],cond:"t° — mô hình",eq:"2Pb + O₂ → 2PbO"},
  {r:["PbO","HNO3"],p:["PbNO32","H2O"],cond:"axit hóa",eq:"PbO + 2HNO₃ → Pb(NO₃)₂ + H₂O"},
  {r:["PbNO32","K2CrO4"],p:["PbCrO4","KNO3"],cond:"trao đổi trong dung dịch",eq:"Pb(NO₃)₂ + K₂CrO₄ → PbCrO₄↓ + 2KNO₃"},
  {r:["B","C"],p:["B4C"],cond:"nhiệt độ cao",eq:"4B + C → B₄C"},
  {r:["Ti","B"],p:["TiB2"],cond:"nhiệt độ cao",eq:"Ti + 2B → TiB₂"},
  {r:["Ti","N2"],p:["TiN"],cond:"nhiệt độ cao",eq:"2Ti + N₂ → 2TiN"},
  {r:["Zr","N2"],p:["ZrN"],cond:"nhiệt độ cao",eq:"2Zr + N₂ → 2ZrN"},
  {r:["Zn","Se"],p:["ZnSe"],cond:"phương trình kết hợp mô hình",eq:"Zn + Se → ZnSe"},
  {r:["Cd","Se"],p:["CdSe"],cond:"phương trình kết hợp mô hình",eq:"Cd + Se → CdSe"},
  {r:["Pb","Se"],p:["PbSe"],cond:"phương trình kết hợp mô hình",eq:"Pb + Se → PbSe"},
  {r:["Na","Se"],p:["Na2Se"],cond:"phương trình kết hợp mô hình",eq:"2Na + Se → Na₂Se"},
  {r:["K","Se"],p:["K2Se"],cond:"phương trình kết hợp mô hình",eq:"2K + Se → K₂Se"},
  {r:["MnO2","H2"],p:["MnO","H2O"],cond:"khử một phần — mô hình tổng quát",eq:"MnO₂ + H₂ → MnO + H₂O"},
  {r:["V","O2"],p:["V2O3"],cond:"oxi hóa hạn chế — mô hình",eq:"4V + 3O₂ → 2V₂O₃"},
  {r:["V2O3","O2"],p:["VO2"],cond:"oxi hóa tiếp",eq:"2V₂O₃ + O₂ → 4VO₂"},
  {r:["TiO2","Ti"],p:["TiO"],cond:"khử oxit — mô hình",eq:"TiO₂ + Ti → 2TiO"},
  {r:["C2H4","H2O2"],p:["EthyleneOxide","H2O"],cond:"oxi hóa — mô hình hữu cơ",eq:"C₂H₄ + H₂O₂ → C₂H₄O + H₂O"},
  {r:["C6H6","CH3Cl"],p:["Toluene","HCl"],cond:"ankyl hóa thơm — mô hình, xúc tác",eq:"C₆H₆ + CH₃Cl → C₆H₅CH₃ + HCl"},
  {r:["C6H6","C2H4"],p:["Ethylbenzene"],cond:"ankyl hóa thơm — mô hình, xúc tác",eq:"C₆H₆ + C₂H₄ → C₆H₅C₂H₅"},
  {r:["C6H6","HNO3"],p:["Nitrobenzene","H2O"],cond:"nitro hóa — mô hình, xúc tác axit",eq:"C₆H₆ + HNO₃ → C₆H₅NO₂ + H₂O"},
  {r:["Nitrobenzene","H2"],p:["Aniline","H2O"],cond:"khử — mô hình, xúc tác",eq:"C₆H₅NO₂ + 3H₂ → C₆H₅NH₂ + 2H₂O"},
  {r:["C6H6","CO"],p:["Benzaldehyde"],cond:"formyl hóa thơm — mô hình, xúc tác HCl/CuCl",eq:"C₆H₆ + CO → C₆H₅CHO"},
  {r:["Benzaldehyde","H2"],p:["BenzylAlcohol"],cond:"hiđro hóa — mô hình",eq:"C₆H₅CHO + H₂ → C₆H₅CH₂OH"},
  {r:["Benzaldehyde","O2"],p:["BenzoicAcid"],cond:"oxi hóa",eq:"2C₆H₅CHO + O₂ → 2C₆H₅COOH"},
  {r:["Phenol","CO2","NaOH"],p:["SodiumSalicylate","H2O"],cond:"Kolbe–Schmitt — mô hình khái niệm",eq:"C₆H₅OH + CO₂ + NaOH → C₇H₅NaO₃ + H₂O"},
  {r:["SodiumSalicylate","HCl"],p:["SalicylicAcid","NaCl"],cond:"axit hóa",eq:"C₇H₅NaO₃ + HCl → C₇H₆O₃ + NaCl"},
  {r:["CH3COOH","NH3"],p:["Acetamide","H2O"],cond:"tách nước — mô hình hữu cơ",eq:"CH₃COOH + NH₃ → CH₃CONH₂ + H₂O"},
  {r:["CH3COOH"],p:["AceticAnhydride","H2O"],cond:"tách nước — mô hình khái niệm",eq:"2CH₃COOH → (CH₃CO)₂O + H₂O"},
  {r:["SalicylicAcid","AceticAnhydride"],p:["Aspirin","CH3COOH"],cond:"axetyl hóa — mô hình hữu cơ",eq:"C₇H₆O₃ + (CH₃CO)₂O → C₉H₈O₄ + CH₃COOH"},
  {r:["BenzoicAcid","CH3OH"],p:["MethylBenzoate","H2O"],cond:"este hóa — mô hình hữu cơ",eq:"C₆H₅COOH + CH₃OH ⇌ C₆H₅COOCH₃ + H₂O"},
  {r:["C6H5Cl","NaOH"],p:["Phenol","NaCl"],cond:"thế nucleophile — mô hình học tập",eq:"C₆H₅Cl + NaOH → C₆H₅OH + NaCl"}
);

/* =========================================================
   PHẢN ỨNG HẠT NHÂN — mô phỏng giáo dục
   r = chất/hạt đầu vào; p = sản phẩm. ID lặp lại là số lượng hạt.
   ========================================================= */
const NX = [
  {r:["H2n","neutron"],p:["H3n","gamma"],cond:"Bắt nơtron",eq:"²₁H + ¹₀n → ³₁H + ⁰₀γ",note:"Bắt nơtron tạo triti và phát photon gamma."},
  {r:["H2n","H2n"],p:["H3n","proton"],cond:"Bắn phá deuteri",eq:"²₁H + ²₁H → ³₁H + ¹₁p",note:"Một nhánh phản ứng deuteri–deuteri."},
  {r:["H2n","H2n"],p:["He3n","neutron"],cond:"Bắn phá deuteri",eq:"²₁H + ²₁H → ³₂He + ¹₀n",note:"Nhánh khác của phản ứng deuteri–deuteri."},
  {r:["H2n","H3n"],p:["He4n","neutron"],cond:"Nhiệt hạch (mô phỏng lý thuyết)",eq:"²₁H + ³₁H → ⁴₂He + ¹₀n",note:"Phản ứng nhiệt hạch deuteri–triti."},
  {r:["He3n","neutron"],p:["H3n","proton"],cond:"Bắt nơtron",eq:"³₂He + ¹₀n → ³₁H + ¹₁p",note:"Bảo toàn số khối và điện tích hạt nhân."},
  {r:["Li6n","neutron"],p:["H3n","He4n"],cond:"Bắt nơtron",eq:"⁶₃Li + ¹₀n → ³₁H + ⁴₂He",note:"Phản ứng hạt nhân của liti-6."},
  {r:["Li7n","proton"],p:["He4n","He4n"],cond:"Bắn phá bằng proton",eq:"⁷₃Li + ¹₁p → ⁴₂He + ⁴₂He",note:"Tạo hai hạt alpha; tổng số khối và điện tích được bảo toàn."},
  {r:["Be9n","alpha"],p:["C12n","neutron"],cond:"Bắn phá bằng hạt alpha",eq:"⁹₄Be + ⁴₂He → ¹²₆C + ¹₀n",note:"Phản ứng tạo cacbon-12 và nơtron."},
  {r:["N14n","alpha"],p:["O17n","proton"],cond:"Bắn phá bằng hạt alpha",eq:"¹⁴₇N + ⁴₂He → ¹⁷₈O + ¹₁p",note:"Phản ứng chuyển hạt nhân nitơ thành oxi-17."},
  {r:["B10n","neutron"],p:["Li7n","He4n"],cond:"Bắt nơtron",eq:"¹⁰₅B + ¹₀n → ⁷₃Li + ⁴₂He",note:"Ví dụ bắt nơtron của bo-10."},
  {r:["C12n","neutron"],p:["C13n","gamma"],cond:"Bắt nơtron",eq:"¹²₆C + ¹₀n → ¹³₆C + ⁰₀γ",note:"Tạo đồng vị cacbon-13."},
  {r:["Na23n","neutron"],p:["Na24n","gamma"],cond:"Bắt nơtron",eq:"²³₁₁Na + ¹₀n → ²⁴₁₁Na + ⁰₀γ",note:"Tạo đồng vị natri-24."},
  {r:["Al27n","alpha"],p:["P30n","neutron"],cond:"Bắn phá bằng hạt alpha",eq:"²⁷₁₃Al + ⁴₂He → ³⁰₁₅P + ¹₀n",note:"Phản ứng tạo photpho-30."},
  {r:["S32n","neutron"],p:["S33n","gamma"],cond:"Bắt nơtron",eq:"³²₁₆S + ¹₀n → ³³₁₆S + ⁰₀γ",note:"Tạo đồng vị lưu huỳnh-33."},
  {r:["F19n","alpha"],p:["Na22n","neutron"],cond:"Bắn phá bằng hạt alpha",eq:"¹⁹₉F + ⁴₂He → ²²₁₁Na + ¹₀n",note:"Phản ứng tạo natri-22."},
  {r:["C12n","alpha"],p:["O16n","gamma"],cond:"Bắt hạt alpha",eq:"¹²₆C + ⁴₂He → ¹⁶₈O + ⁰₀γ",note:"Phản ứng tạo oxi-16."},
  {r:["He3n","He3n"],p:["He4n","proton","proton"],cond:"Nhiệt hạch (mô phỏng lý thuyết)",eq:"³₂He + ³₂He → ⁴₂He + ¹₁p + ¹₁p",note:"Phản ứng giữa hai hạt nhân heli-3."},
  {r:["U235n","neutron"],p:["Ba141n","Kr92n","neutron","neutron","neutron"],cond:"Phân hạch — ví dụ khái niệm",eq:"²³⁵₉₂U + ¹₀n → ¹⁴¹₅₆Ba + ⁹²₃₆Kr + 3¹₀n",note:"Phương trình minh họa bảo toàn số khối và điện tích; sản phẩm phân hạch thực tế có thể khác."},
  {r:["U235n","neutron"],p:["Xe140n","Sr94n","neutron","neutron"],cond:"Phân hạch — ví dụ khái niệm",eq:"²³⁵₉₂U + ¹₀n → ¹⁴⁰₅₄Xe + ⁹⁴₃₈Sr + 2¹₀n",note:"Một phương án sản phẩm phân hạch minh họa khác."},
  {r:["U238n","neutron"],p:["U239n","gamma"],cond:"Bắt nơtron",eq:"²³⁸₉₂U + ¹₀n → ²³⁹₉₂U + ⁰₀γ",note:"Bắt nơtron làm tăng số khối của hạt nhân."},
  {r:["U239n"],p:["Np239n","electron","antinu"],cond:"Phân rã beta trừ",eq:"²³⁹₉₂U → ²³⁹₉₃Np + ⁰₋₁e + ν̅ₑ",note:"Phân rã beta làm số proton tăng một đơn vị."},
  {r:["Np239n"],p:["Pu239n","electron","antinu"],cond:"Phân rã beta trừ",eq:"²³⁹₉₃Np → ²³⁹₉₄Pu + ⁰₋₁e + ν̅ₑ",note:"Mô hình chuỗi phân rã beta tiếp theo."},
  {r:["C14n"],p:["N14n","electron","antinu"],cond:"Phân rã beta trừ",eq:"¹⁴₆C → ¹⁴₇N + ⁰₋₁e + ν̅ₑ",note:"Ví dụ phóng xạ beta của cacbon-14."},
// ===== MỞ RỘNG: BẮT NƠTRON, BẮT HẠT, PHÂN RÃ VÀ ĐỒNG PHÂN HẠT NHÂN =====
{r:["H1n","neutron"],p:["H2n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"H1n + n → H2n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Li7n","neutron"],p:["Li8n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Li7n + n → Li8n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Be9n","neutron"],p:["Be10n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Be9n + n → Be10n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["B11n","neutron"],p:["B12n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"B11n + n → B12n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["C12n","neutron"],p:["C13n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"C12n + n → C13n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["C13n","neutron"],p:["C14n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"C13n + n → C14n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["N14n","neutron"],p:["N15n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"N14n + n → N15n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["N15n","neutron"],p:["N16n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"N15n + n → N16n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["O16n","neutron"],p:["O17n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"O16n + n → O17n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["O17n","neutron"],p:["O18n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"O17n + n → O18n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["F19n","neutron"],p:["F20n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"F19n + n → F20n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Ne20n","neutron"],p:["Ne21n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Ne20n + n → Ne21n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Mg24n","neutron"],p:["Mg25n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Mg24n + n → Mg25n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Mg25n","neutron"],p:["Mg26n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Mg25n + n → Mg26n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Al27n","neutron"],p:["Al28n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Al27n + n → Al28n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Si28n","neutron"],p:["Si29n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Si28n + n → Si29n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Si29n","neutron"],p:["Si30n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Si29n + n → Si30n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["P31n","neutron"],p:["P32n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"P31n + n → P32n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["S33n","neutron"],p:["S34n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"S33n + n → S34n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Cl35n","neutron"],p:["Cl36n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Cl35n + n → Cl36n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Cl37n","neutron"],p:["Cl38n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Cl37n + n → Cl38n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Ar40n","neutron"],p:["Ar41n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Ar40n + n → Ar41n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["K39n","neutron"],p:["K40n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"K39n + n → K40n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["K40n","neutron"],p:["K41n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"K40n + n → K41n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Ca40n","neutron"],p:["Ca41n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Ca40n + n → Ca41n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Ca44n","neutron"],p:["Ca45n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Ca44n + n → Ca45n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Ti44n","neutron"],p:["Ti45n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Ti44n + n → Ti45n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Fe56n","neutron"],p:["Fe57n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Fe56n + n → Fe57n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Fe57n","neutron"],p:["Fe58n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Fe57n + n → Fe58n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Co59n","neutron"],p:["Co60n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Co59n + n → Co60n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Ni58n","neutron"],p:["Ni59n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Ni58n + n → Ni59n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Ni60n","neutron"],p:["Ni61n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Ni60n + n → Ni61n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Cu63n","neutron"],p:["Cu64n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Cu63n + n → Cu64n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Zn64n","neutron"],p:["Zn65n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Zn64n + n → Zn65n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Ag107n","neutron"],p:["Ag108n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Ag107n + n → Ag108n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["I127n","neutron"],p:["I128n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"I127n + n → I128n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Xe129n","neutron"],p:["Xe130n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Xe129n + n → Xe130n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Cs133n","neutron"],p:["Cs134n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Cs133n + n → Cs134n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Ba138n","neutron"],p:["Ba139n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Ba138n + n → Ba139n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["Th232n","neutron"],p:["Th233n","gamma"],cond:"bắt nơtron (nhánh gamma minh họa)",eq:"Th232n + n → Th233n + γ",note:"Phương trình dạng ký hiệu; xác suất bắt nơtron và các nhánh cạnh tranh phụ thuộc đồng vị, không biểu thị điều kiện thực nghiệm."},
{r:["H1n","H1n"],p:["H2n","positron","nu"],cond:"chuỗi proton–proton (mô phỏng khái niệm)",eq:"¹₁H + ¹₁H → ²₁H + e⁺ + νₑ",note:"Mô hình phản ứng tổng quát trong quá trình tổng hợp hạt nhân ở sao."},
{r:["H2n","proton"],p:["He3n","gamma"],cond:"bắt proton",eq:"²₁H + ¹₁p → ³₂He + γ",note:"Tổng số khối và điện tích hạt nhân được bảo toàn."},
{r:["He3n","alpha"],p:["Be7n","gamma"],cond:"bắt hạt alpha",eq:"³₂He + ⁴₂He → ⁷₄Be + γ",note:"Ví dụ phản ứng bắt alpha trong mạng phản ứng sao."},
{r:["O16n","alpha"],p:["Ne20n","gamma"],cond:"bắt hạt alpha",eq:"¹⁶₈O + ⁴₂He → ²⁰₁₀Ne + γ",note:"Phản ứng tổng hợp hạt nhân minh họa."},
{r:["Ne20n","alpha"],p:["Mg24n","gamma"],cond:"bắt hạt alpha",eq:"²⁰₁₀Ne + ⁴₂He → ²⁴₁₂Mg + γ",note:"Phản ứng tổng hợp hạt nhân minh họa."},
{r:["Mg24n","alpha"],p:["Si28n","gamma"],cond:"bắt hạt alpha",eq:"²⁴₁₂Mg + ⁴₂He → ²⁸₁₄Si + γ",note:"Phản ứng tổng hợp hạt nhân minh họa."},
{r:["Si28n","alpha"],p:["S32n","gamma"],cond:"bắt hạt alpha",eq:"²⁸₁₄Si + ⁴₂He → ³²₁₆S + γ",note:"Phản ứng tổng hợp hạt nhân minh họa."},
{r:["S32n","alpha"],p:["Ar36n","gamma"],cond:"bắt hạt alpha",eq:"³²₁₆S + ⁴₂He → ³⁶₁₈Ar + γ",note:"Đây là phương trình khái niệm; kho đồng vị được mở rộng theo từng phản ứng."},
{r:["Ca40n","alpha"],p:["Ti44n","gamma"],cond:"bắt hạt alpha",eq:"⁴⁰₂₀Ca + ⁴₂He → ⁴⁴₂₂Ti + γ",note:"Phản ứng tạo đồng vị titan-44."},
{r:["C12n","proton"],p:["N13n","gamma"],cond:"bắt proton",eq:"¹²₆C + ¹₁p → ¹³₇N + γ",note:"Đồng vị nitơ-13 có thể phân rã beta cộng."},
{r:["N14n","proton"],p:["O15n","gamma"],cond:"bắt proton",eq:"¹⁴₇N + ¹₁p → ¹⁵₈O + γ",note:"Phản ứng hạt nhân minh họa."},
{r:["O16n","proton"],p:["F17n","gamma"],cond:"bắt proton",eq:"¹⁶₈O + ¹₁p → ¹⁷₉F + γ",note:"Đồng vị flo-17 không bền và có thể phân rã beta cộng."},
{r:["N14n","neutron"],p:["C14n","proton"],cond:"phản ứng (n,p) minh họa",eq:"¹⁴₇N + ¹₀n → ¹⁴₆C + ¹₁p",note:"Phương trình phản ứng chuyển đổi hạt nhân, bảo toàn số khối và điện tích."},
{r:["Be7n","electron"],p:["Li7n","nu"],cond:"bắt electron",eq:"⁷₄Be + e⁻ → ⁷₃Li + νₑ",note:"Bắt electron là một kiểu biến đổi hạt nhân; không phải phản ứng hóa học."},
{r:["H3n"],p:["He3n","electron","antinu"],cond:"phân rã beta trừ",eq:"³₁H → ³₂He + e⁻ + ν̅ₑ",note:"Tritium phân rã beta thành heli-3."},
{r:["Na24n"],p:["Mg24n","electron","antinu"],cond:"phân rã beta trừ",eq:"²⁴₁₁Na → ²⁴₁₂Mg + e⁻ + ν̅ₑ",note:"Ví dụ phân rã beta của natri-24."},
{r:["P32n"],p:["S32n","electron","antinu"],cond:"phân rã beta trừ",eq:"³²₁₅P → ³²₁₆S + e⁻ + ν̅ₑ",note:"Photpho-32 phân rã beta thành lưu huỳnh-32."},
{r:["Co60n"],p:["Ni60n","electron","antinu"],cond:"phân rã beta trừ",eq:"⁶⁰₂₇Co → ⁶⁰₂₈Ni + e⁻ + ν̅ₑ",note:"Phương trình ghi phần biến đổi hạt nhân; các photon gamma sau phân rã không thể hiện tại đây."},
{r:["I128n"],p:["Xe128n","electron","antinu"],cond:"phân rã beta trừ (mô hình đồng vị)",eq:"¹²⁸₅₃I → ¹²⁸₅₄Xe + e⁻ + ν̅ₑ",note:"Mô hình minh họa phân rã beta của đồng vị iot phóng xạ."},
{r:["I131n"],p:["Xe131n","electron","antinu"],cond:"phân rã beta trừ",eq:"¹³¹₅₃I → ¹³¹₅₄Xe + e⁻ + ν̅ₑ",note:"Một ví dụ phân rã beta của iot-131."},
{r:["Cs134n"],p:["Ba134n","electron","antinu"],cond:"phân rã beta trừ — minh họa",eq:"¹³⁴₅₅Cs → ¹³⁴₅₆Ba + e⁻ + ν̅ₑ",note:"Phương trình minh họa bảo toàn số khối và điện tích."},
{r:["K40n"],p:["Ca40n","electron","antinu"],cond:"phân rã beta trừ (một nhánh)",eq:"⁴⁰₁₉K → ⁴⁰₂₀Ca + e⁻ + ν̅ₑ",note:"Kali-40 có nhiều nhánh phân rã; mô phỏng này chỉ biểu diễn nhánh beta trừ."},
{r:["C11n"],p:["B11n","positron","nu"],cond:"phân rã beta cộng",eq:"¹¹₆C → ¹¹₅B + e⁺ + νₑ",note:"Cacbon-11 phân rã beta cộng thành bo-11."},
{r:["N13n"],p:["C13n","positron","nu"],cond:"phân rã beta cộng",eq:"¹³₇N → ¹³₆C + e⁺ + νₑ",note:"Nitơ-13 phân rã beta cộng thành cacbon-13."},
{r:["O15n"],p:["N15n","positron","nu"],cond:"phân rã beta cộng",eq:"¹⁵₈O → ¹⁵₇N + e⁺ + νₑ",note:"Oxi-15 phân rã beta cộng thành nitơ-15."},
{r:["F17n"],p:["O17n","positron","nu"],cond:"phân rã beta cộng",eq:"¹⁷₉F → ¹⁷₈O + e⁺ + νₑ",note:"Flo-17 phân rã beta cộng thành oxi-17."},
{r:["Tc99mn"],p:["Tc99n","gamma"],cond:"chuyển trạng thái đồng phân hạt nhân",eq:"⁹⁹ᵐ₄₃Tc → ⁹⁹₄₃Tc + γ",note:"Đồng phân hạt nhân chuyển về trạng thái năng lượng thấp hơn bằng phát gamma."},
{r:["Ba137mn"],p:["Ba137n","gamma"],cond:"chuyển trạng thái đồng phân hạt nhân",eq:"¹³⁷ᵐ₅₆Ba → ¹³⁷₅₆Ba + γ",note:"Ví dụ chuyển trạng thái đồng phân hạt nhân phát photon gamma."},
{r:["In115mn"],p:["In115n","gamma"],cond:"chuyển trạng thái đồng phân hạt nhân (mô hình)",eq:"¹¹⁵ᵐ₄₉In → ¹¹⁵₄₉In + γ",note:"Mô hình minh họa trạng thái kích thích hạt nhân phát gamma."},
{r:["U238n"],p:["Th234n","He4n"],cond:"phân rã alpha",eq:"²³⁸₉₂U → ²³⁴₉₀Th + ⁴₂He",note:"Phân rã alpha giảm số khối bốn đơn vị và số proton hai đơn vị."},
{r:["Th232n"],p:["Ra228n","He4n"],cond:"phân rã alpha",eq:"²³²₉₀Th → ²²⁸₈₈Ra + ⁴₂He",note:"Phân rã alpha giảm số khối bốn đơn vị và số proton hai đơn vị."},
{r:["Ra226n"],p:["Rn222n","He4n"],cond:"phân rã alpha",eq:"²²⁶₈₈Ra → ²²²₈₆Rn + ⁴₂He",note:"Ví dụ phân rã alpha của radi-226."},
{r:["Po210n"],p:["Pb206n","He4n"],cond:"phân rã alpha",eq:"²¹⁰₈₄Po → ²⁰⁶₈₂Pb + ⁴₂He",note:"Ví dụ phân rã alpha của poloni-210."},
{r:["H2n","gamma"],p:["proton","neutron"],cond:"quang phân hạt nhân (mô hình khái niệm)",eq:"²₁H + γ → ¹₁p + ¹₀n",note:"Photon năng lượng đủ lớn có thể tách hạt nhân đơteri; đây là phương trình khái niệm."},
{r:["Li6n","proton"],p:["Be7n","gamma"],cond:"bắt proton",eq:"⁶₃Li + ¹₁p → ⁷₄Be + γ",note:"Ví dụ phản ứng tạo berili-7."}
];

/* =========================================================
   THƯ VIỆN ĐỒNG VỊ & ĐỒNG PHÂN HẠT NHÂN
   ========================================================= */
const ISOTOPE_CATALOG = [["H1n", "H", 1, 1, "Hiđro-1"], ["H2n", "H", 2, 1, "Hiđro-2 (đơteri)"], ["H3n", "H", 3, 1, "Hiđro-3 (triti)"], ["He3n", "He", 3, 2, "Heli-3"], ["He4n", "He", 4, 2, "Heli-4"], ["He6n", "He", 6, 2, "Heli-6"], ["Li6n", "Li", 6, 3, "Liti-6"], ["Li7n", "Li", 7, 3, "Liti-7"], ["Li8n", "Li", 8, 3, "Liti-8"], ["Be7n", "Be", 7, 4, "Berili-7"], ["Be9n", "Be", 9, 4, "Berili-9"], ["Be10n", "Be", 10, 4, "Berili-10"], ["B10n", "B", 10, 5, "Bo-10"], ["B11n", "B", 11, 5, "Bo-11"], ["B12n", "B", 12, 5, "Bo-12"], ["C11n", "C", 11, 6, "Cacbon-11"], ["C12n", "C", 12, 6, "Cacbon-12"], ["C13n", "C", 13, 6, "Cacbon-13"], ["C14n", "C", 14, 6, "Cacbon-14"], ["N13n", "N", 13, 7, "Nitơ-13"], ["N14n", "N", 14, 7, "Nitơ-14"], ["N15n", "N", 15, 7, "Nitơ-15"], ["N16n", "N", 16, 7, "Nitơ-16"], ["O15n", "O", 15, 8, "Oxi-15"], ["O16n", "O", 16, 8, "Oxi-16"], ["O17n", "O", 17, 8, "Oxi-17"], ["O18n", "O", 18, 8, "Oxi-18"], ["F17n", "F", 17, 9, "Flo-17"], ["F19n", "F", 19, 9, "Flo-19"], ["F20n", "F", 20, 9, "Flo-20"], ["Ne20n", "Ne", 20, 10, "Neon-20"], ["Ne21n", "Ne", 21, 10, "Neon-21"], ["Na22n", "Na", 22, 11, "Natri-22"], ["Na23n", "Na", 23, 11, "Natri-23"], ["Na24n", "Na", 24, 11, "Natri-24"], ["Mg24n", "Mg", 24, 12, "Magie-24"], ["Mg25n", "Mg", 25, 12, "Magie-25"], ["Mg26n", "Mg", 26, 12, "Magie-26"], ["Al27n", "Al", 27, 13, "Nhôm-27"], ["Al28n", "Al", 28, 13, "Nhôm-28"], ["Si28n", "Si", 28, 14, "Silic-28"], ["Si29n", "Si", 29, 14, "Silic-29"], ["Si30n", "Si", 30, 14, "Silic-30"], ["P30n", "P", 30, 15, "Photpho-30"], ["P31n", "P", 31, 15, "Photpho-31"], ["P32n", "P", 32, 15, "Photpho-32"], ["S32n", "S", 32, 16, "Lưu huỳnh-32"], ["S33n", "S", 33, 16, "Lưu huỳnh-33"], ["S34n", "S", 34, 16, "Lưu huỳnh-34"], ["Cl35n", "Cl", 35, 17, "Clo-35"], ["Cl36n", "Cl", 36, 17, "Clo-36"], ["Cl37n", "Cl", 37, 17, "Clo-37"], ["Cl38n", "Cl", 38, 17, "Clo-38"], ["Ar40n", "Ar", 40, 18, "Argon-40"], ["Ar41n", "Ar", 41, 18, "Argon-41"], ["K39n", "K", 39, 19, "Kali-39"], ["K40n", "K", 40, 19, "Kali-40"], ["K41n", "K", 41, 19, "Kali-41"], ["Ca40n", "Ca", 40, 20, "Canxi-40"], ["Ca41n", "Ca", 41, 20, "Canxi-41"], ["Ca44n", "Ca", 44, 20, "Canxi-44"], ["Ca45n", "Ca", 45, 20, "Canxi-45"], ["Ti44n", "Ti", 44, 22, "Titan-44"], ["Ti45n", "Ti", 45, 22, "Titan-45"], ["Fe56n", "Fe", 56, 26, "Sắt-56"], ["Fe57n", "Fe", 57, 26, "Sắt-57"], ["Fe58n", "Fe", 58, 26, "Sắt-58"], ["Co59n", "Co", 59, 27, "Coban-59"], ["Co60n", "Co", 60, 27, "Coban-60"], ["Ni58n", "Ni", 58, 28, "Niken-58"], ["Ni59n", "Ni", 59, 28, "Niken-59"], ["Ni60n", "Ni", 60, 28, "Niken-60"], ["Ni61n", "Ni", 61, 28, "Niken-61"], ["Cu63n", "Cu", 63, 29, "Đồng-63"], ["Cu64n", "Cu", 64, 29, "Đồng-64"], ["Zn64n", "Zn", 64, 30, "Kẽm-64"], ["Zn65n", "Zn", 65, 30, "Kẽm-65"], ["Ag107n", "Ag", 107, 47, "Bạc-107"], ["Ag108n", "Ag", 108, 47, "Bạc-108"], ["I127n", "I", 127, 53, "Iot-127"], ["I128n", "I", 128, 53, "Iot-128"], ["Xe129n", "Xe", 129, 54, "Xenon-129"], ["Xe130n", "Xe", 130, 54, "Xenon-130"], ["Xe131n", "Xe", 131, 54, "Xenon-131"], ["Cs133n", "Cs", 133, 55, "Xesi-133"], ["Cs134n", "Cs", 134, 55, "Xesi-134"], ["Ba137n", "Ba", 137, 56, "Bari-137"], ["Ba138n", "Ba", 138, 56, "Bari-138"], ["Ba139n", "Ba", 139, 56, "Bari-139"], ["Tc99n", "Tc", 99, 43, "Tecneti-99"], ["Tc99mn", "Tc", 99, 43, "Tecneti-99m (đồng phân hạt nhân)"], ["In115n", "In", 115, 49, "Indi-115"], ["In115mn", "In", 115, 49, "Indi-115m (đồng phân hạt nhân)"], ["Ba137mn", "Ba", 137, 56, "Bari-137m (đồng phân hạt nhân)"], ["Ar36n", "Ar", 36, 18, "Argon-36"], ["Th232n", "Th", 232, 90, "Thori-232"], ["Th233n", "Th", 233, 90, "Thori-233"], ["Ra226n", "Ra", 226, 88, "Radi-226"], ["Ra228n", "Ra", 228, 88, "Radi-228"], ["Rn222n", "Rn", 222, 86, "Radon-222"], ["Po210n", "Po", 210, 84, "Poloni-210"], ["Pb206n", "Pb", 206, 82, "Chì-206"], ["Th234n", "Th", 234, 90, "Thori-234"], ["Xe128n", "Xe", 128, 54, "Xenon-128"], ["I131n", "I", 131, 53, "Iot-131"], ["Cs134n", "Cs", 134, 55, "Xesi-134"], ["Ba134n", "Ba", 134, 56, "Bari-134"], ["U235n", "U", 235, 92, "Urani-235"], ["U238n", "U", 238, 92, "Urani-238"], ["U239n", "U", 239, 92, "Urani-239"], ["Np239n", "Np", 239, 93, "Neptuni-239"], ["Pu239n", "Pu", 239, 94, "Plutoni-239"], ["Ba141n", "Ba", 141, 56, "Bari-141"], ["Kr92n", "Kr", 92, 36, "Krypton-92"], ["Xe140n", "Xe", 140, 54, "Xenon-140"], ["Sr94n", "Sr", 94, 38, "Stronti-94"]];
const SUPERSCRIPT = {"0":"⁰","1":"¹","2":"²","3":"³","4":"⁴","5":"⁵","6":"⁶","7":"⁷","8":"⁸","9":"⁹"};
const SUBSCRIPT = {"0":"₀","1":"₁","2":"₂","3":"₃","4":"₄","5":"₅","6":"₆","7":"₇","8":"₈","9":"₉"};
function toSuperscript(value){ return String(value).split("").map(ch=>SUPERSCRIPT[ch] || ch).join(""); }
function toSubscript(value){ return String(value).split("").map(ch=>SUBSCRIPT[ch] || ch).join(""); }
for (const [id, symbol, mass, atomicNumber, name] of ISOTOPE_CATALOG) {
  const isomer = /\d+m(?:n)?$/.test(id);
  const massLabel = toSuperscript(mass) + (isomer ? "ᵐ" : "");
  const formula = massLabel + toSubscript(atomicNumber) + symbol;
  if (!S[id]) S[id] = {f: formula, n: name, c: "nuclear", kind: "isotope"};
  Object.assign(S[id], {f: formula, n: name, c: "nuclear", kind: "isotope", z: atomicNumber, a: mass, symbol, nuclearIsomer: isomer});
}
if (!S.nu) S.nu = {f:"⁰₀νₑ",n:"Nơtrinô electron",c:"nuclear",kind:"particle"};
for (const rx of NX) {
  if (rx.cond === "bắt nơtron (nhánh gamma minh họa)") {
    rx.eq = `${S[rx.r[0]]?.f || rx.r[0]} + ${S.neutron.f} → ${S[rx.p[0]]?.f || rx.p[0]} + ${S.gamma.f}`;
  }
}

/* =====================================================================
   KOI DATA WORKSHOP — KHO MỞ RỘNG & VÙNG CHỈNH SỬA
   ---------------------------------------------------------------------
   Mục tiêu kho hóa học: 1.800 chất (chưa tính hạt nhân).
   Đơn chất (c: "element") được mở đầu game; hợp chất luôn bị khóa.

   Thêm chất thủ công:
     MANUAL_SUBSTANCES: { MaChat: { f:"NaCl", n:"Natri clorua", c:"salt" } }
   c hợp lệ thường dùng: element, oxide, base, acid, salt, organic, polymer, other.

   Thêm phản ứng:
     MANUAL_CHEMISTRY_REACTIONS: [{ r:["H2","O2"], p:["H2O"],
       cond:"đốt cháy", eq:"2H₂ + O₂ → 2H₂O" }]
     MANUAL_NUCLEAR_REACTIONS: cùng cấu trúc, dùng ID hạt/đồng vị.

   Bỏ chất có sẵn: thêm ID vào REMOVED_SUBSTANCE_IDS. Các phản ứng liên
   quan đến ID bị bỏ sẽ tự loại để tránh tạo ra sản phẩm không còn tồn tại.
   ===================================================================== */
const KOI_TARGET_CHEMICALS = 1800;
const KOI_SUBSCRIPT_MAP = {"0":"₀","1":"₁","2":"₂","3":"₃","4":"₄","5":"₅","6":"₆","7":"₇","8":"₈","9":"₉"};
const KOI_ASCII_SUBSCRIPT_MAP = {"₀":"0","₁":"1","₂":"2","₃":"3","₄":"4","₅":"5","₆":"6","₇":"7","₈":"8","₉":"9"};
function koiSubscriptFormula(formula) {
  return String(formula).replace(/\d/g, digit => KOI_SUBSCRIPT_MAP[digit] || digit);
}
function koiFormulaKey(formula) {
  return String(formula || "")
    .replace(/<[^>]*>/g, "")
    .replace(/[₀-₉]/g, digit => KOI_ASCII_SUBSCRIPT_MAP[digit] || digit)
    .replace(/[\s·•↑↓]/g, "")
    .toUpperCase();
}
function koiChemicalCount() {
  return Object.keys(S).filter(id => S[id] && S[id].c !== "nuclear").length;
}
function koiGcd(a, b) {
  while (b) [a, b] = [b, a % b];
  return Math.abs(a) || 1;
}
function koiGroupedIon(formula, coefficient, polyatomic) {
  if (coefficient === 1) return formula;
  return (polyatomic ? `(${formula})` : formula) + coefficient;
}
function koiAddChemical(id, formula, name, category, extra = {}) {
  if (S[id]) return false;
  S[id] = { f: koiSubscriptFormula(formula), n: name, c: category, ...extra };
  return true;
}

/* Dữ liệu ion được mô tả ngắn gọn để sinh muối trung hòa điện tích.
   Bạn có thể bổ sung ion ở đây; công thức muối sẽ được tạo tự động. */
const KOI_CATIONS = [
  {key:"Li",s:"Li",q:1,n:"Liti",baseId:"LiOH",base:"LiOH"},
  {key:"Na",s:"Na",q:1,n:"Natri",baseId:"NaOH",base:"NaOH"},
  {key:"K",s:"K",q:1,n:"Kali",baseId:"KOH",base:"KOH"},
  {key:"Rb",s:"Rb",q:1,n:"Rubidi",base:"RbOH",base:"RbOH"},
  {key:"Cs",s:"Cs",q:1,n:"Xesi",baseId:"CsOH",base:"CsOH"},
  {key:"Ag",s:"Ag",q:1,n:"Bạc",baseId:"AgOH",base:"AgOH"},
  {key:"NH4",s:"NH4",q:1,n:"Amoni",poly:true,baseId:"NH3H2O",base:"NH4OH"},
  {key:"Mg",s:"Mg",q:2,n:"Magie",baseId:"MgOH2",base:"Mg(OH)2"},
  {key:"Ca",s:"Ca",q:2,n:"Canxi",baseId:"CaOH2",base:"Ca(OH)2"},
  {key:"Sr",s:"Sr",q:2,n:"Stronti",baseId:"SrOH2",base:"Sr(OH)2"},
  {key:"Ba",s:"Ba",q:2,n:"Bari",baseId:"BaOH2",base:"Ba(OH)2"},
  {key:"Zn",s:"Zn",q:2,n:"Kẽm",baseId:"ZnOH2",base:"Zn(OH)2"},
  {key:"Cd",s:"Cd",q:2,n:"Cadimi",baseId:"CdOH2",base:"Cd(OH)2"},
  {key:"FeII",s:"Fe",q:2,n:"Sắt(II)",baseId:"FeOH2",base:"Fe(OH)2"},
  {key:"FeIII",s:"Fe",q:3,n:"Sắt(III)",baseId:"FeOH3",base:"Fe(OH)3"},
  {key:"CuI",s:"Cu",q:1,n:"Đồng(I)",baseId:"CuOH",base:"CuOH"},
  {key:"CuII",s:"Cu",q:2,n:"Đồng(II)",baseId:"CuOH2",base:"Cu(OH)2"},
  {key:"NiII",s:"Ni",q:2,n:"Niken(II)",baseId:"NiOH2",base:"Ni(OH)2"},
  {key:"CoII",s:"Co",q:2,n:"Coban(II)",baseId:"CoOH2",base:"Co(OH)2"},
  {key:"CoIII",s:"Co",q:3,n:"Coban(III)",baseId:"CoOH3",base:"Co(OH)3"},
  {key:"MnII",s:"Mn",q:2,n:"Mangan(II)",baseId:"MnOH2",base:"Mn(OH)2"},
  {key:"CrIII",s:"Cr",q:3,n:"Crôm(III)",baseId:"CrOH3",base:"Cr(OH)3"},
  {key:"Al",s:"Al",q:3,n:"Nhôm",baseId:"AlOH3",base:"Al(OH)3"},
  {key:"Ga",s:"Ga",q:3,n:"Gali",baseId:"GaOH3",base:"Ga(OH)3"},
  {key:"In",s:"In",q:3,n:"Indi",baseId:"InOH3",base:"In(OH)3"},
  {key:"SnII",s:"Sn",q:2,n:"Thiếc(II)",baseId:"SnOH2",base:"Sn(OH)2"},
  {key:"SnIV",s:"Sn",q:4,n:"Thiếc(IV)",baseId:"SnOH4",base:"Sn(OH)4"},
  {key:"PbII",s:"Pb",q:2,n:"Chì(II)",baseId:"PbOH2",base:"Pb(OH)2"},
  {key:"PbIV",s:"Pb",q:4,n:"Chì(IV)",baseId:"PbOH4",base:"Pb(OH)4"},
  {key:"TiIV",s:"Ti",q:4,n:"Titan(IV)",baseId:"TiOH4",base:"Ti(OH)4"}
];
const KOI_ANIONS = [
  {key:"F",f:"F",q:1,n:"florua"}, {key:"Cl",f:"Cl",q:1,n:"clorua"},
  {key:"Br",f:"Br",q:1,n:"bromua"}, {key:"I",f:"I",q:1,n:"iodua"},
  {key:"NO3",f:"NO3",q:1,n:"nitrat",acidId:"HNO3",acidF:"HNO3",acidQ:1},
  {key:"NO2",f:"NO2",q:1,n:"nitrit",acidId:"HNO2",acidF:"HNO2",acidQ:1},
  {key:"ClO3",f:"ClO3",q:1,n:"clorat",acidId:"HClO3",acidF:"HClO3",acidQ:1},
  {key:"ClO4",f:"ClO4",q:1,n:"peclorat",acidId:"HClO4",acidF:"HClO4",acidQ:1},
  {key:"MnO4",f:"MnO4",q:1,n:"pemanganat",acidId:"HMnO4",acidF:"HMnO4",acidQ:1},
  {key:"IO3",f:"IO3",q:1,n:"iodat",acidId:"HIO3",acidF:"HIO3",acidQ:1},
  {key:"SO4",f:"SO4",q:2,n:"sunfat",acidId:"H2SO4 loãng",acidF:"H2SO4",acidQ:2},
  {key:"SO3",f:"SO3",q:2,n:"sunfit",acidId:"H2SO3",acidF:"H2SO3",acidQ:2},
  {key:"CO3",f:"CO3",q:2,n:"cacbonat",acidId:"H2CO3",acidF:"H2CO3",acidQ:2},
  {key:"C2O4",f:"C2O4",q:2,n:"oxalat",acidId:"H2C2O4",acidF:"H2C2O4",acidQ:2},
  {key:"CrO4",f:"CrO4",q:2,n:"cromat",acidId:"H2CrO4",acidF:"H2CrO4",acidQ:2},
  {key:"SiO3",f:"SiO3",q:2,n:"silicat",acidId:"H2SiO3",acidF:"H2SiO3",acidQ:2},
  {key:"S2O3",f:"S2O3",q:2,n:"thiosunfat"},
  {key:"HPO4",f:"HPO4",q:2,n:"hiđrophotphat",acidId:"H3PO4",acidF:"H3PO4",acidQ:3},
  {key:"HCO3",f:"HCO3",q:1,n:"hiđrocacbonat",acidId:"H2CO3",acidF:"H2CO3",acidQ:2},
  {key:"CH3COO",f:"C2H3O2",q:1,n:"axetat",acidId:"CH3COOH",acidF:"CH3COOH",acidQ:1},
  {key:"HCOO",f:"CHO2",q:1,n:"fomat",acidId:"HCOOH",acidF:"HCOOH",acidQ:1},
  {key:"PO4",f:"PO4",q:3,n:"photphat",acidId:"H3PO4",acidF:"H3PO4",acidQ:3},
  {key:"BO3",f:"BO3",q:3,n:"borat",acidId:"H3BO3",acidF:"H3BO3",acidQ:3},
  {key:"Cr2O7",f:"Cr2O7",q:2,n:"đicromat",acidId:"H2Cr2O7",acidF:"H2Cr2O7",acidQ:2},
  {key:"SCN",f:"SCN",q:1,n:"thiocyanat"}
];

/* Bổ sung vài axit thuộc các họ chất dùng trong kho muối. */
const KOI_ACID_ADDITIONS = [
  ["H2SiO3","H2SiO3","Axit silixic"],
  ["H2Cr2O7","H2Cr2O7","Axit đicromic"],
  ["HIO3","HIO3","Axit iotic"]
];
for (const [id, formula, name] of KOI_ACID_ADDITIONS) {
  if (!S[id]) koiAddChemical(id, formula, name, "acid");
}

const KOI_FORMULA_TO_ID = new Map();
const KOI_KNOWN_FORMULAS = new Set();
for (const [id, sub] of Object.entries(S)) {
  if (!sub || sub.c === "nuclear") continue;
  const key = koiFormulaKey(sub.f);
  if (key) {
    KOI_KNOWN_FORMULAS.add(key);
    if (!KOI_FORMULA_TO_ID.has(key)) KOI_FORMULA_TO_ID.set(key, id);
  }
}
function koiFormulaForSalt(cation, anion) {
  const gcd = koiGcd(cation.q, anion.q);
  const cations = anion.q / gcd;
  const anions = cation.q / gcd;
  return koiGroupedIon(cation.s, cations, !!cation.poly) + koiGroupedIon(anion.f, anions, !/^[A-Z][a-z]?$/.test(anion.f));
}
function koiBaseForCation(cation) {
  if (cation.baseId && S[cation.baseId]) return cation.baseId;
  const formulaKey = koiFormulaKey(cation.base);
  if (KOI_FORMULA_TO_ID.has(formulaKey)) return KOI_FORMULA_TO_ID.get(formulaKey);
  const id = `gen_base_${cation.key}`;
  if (koiAddChemical(id, cation.base, `${cation.n} hiđroxit`, "base", { generatedBy:"KOI salt library" })) {
    KOI_KNOWN_FORMULAS.add(formulaKey);
    KOI_FORMULA_TO_ID.set(formulaKey, id);
    return id;
  }
  return S[id] ? id : null;
}
function koiResolveAcid(anion) {
  if (!anion.acidId) return null;
  if (S[anion.acidId]) return anion.acidId;
  const key = koiFormulaKey(anion.acidF);
  if (KOI_FORMULA_TO_ID.has(key)) return KOI_FORMULA_TO_ID.get(key);
  const names = {
    HNO2:"Axit nitrơ", HClO3:"Axit cloric", HClO4:"Axit pecloric", HMnO4:"Axit pemanganic",
    H2CrO4:"Axit cromic", H2C2O4:"Axit oxalic", H2SiO3:"Axit silixic", H3BO3:"Axit boric",
    H2Cr2O7:"Axit đicromic", HIO3:"Axit iotic", HCOOH:"Axit fomic", H2CO3:"Axit cacbonic"
  };
  if (koiAddChemical(anion.acidId, anion.acidF, names[anion.acidF] || `Axit tạo ion ${anion.key}`, "acid")) {
    KOI_KNOWN_FORMULAS.add(key);
    KOI_FORMULA_TO_ID.set(key, anion.acidId);
  }
  return S[anion.acidId] ? anion.acidId : (KOI_FORMULA_TO_ID.get(key) || null);
}

/* Tạo các muối cân bằng điện tích, bỏ qua công thức đã có sẵn.
   Giới hạn số muối bổ sung để kho vẫn có nhiều chất hữu cơ. */
const KOI_GENERATED_SALT_ROUTES = [];
let koiGeneratedSaltCount = 0;
const KOI_SALT_LIMIT = 520;
const koiSaltPairs = [];
for (let diagonal = 0; diagonal < KOI_CATIONS.length + KOI_ANIONS.length - 1; diagonal++) {
  for (let ci = 0; ci < KOI_CATIONS.length; ci++) {
    const ai = diagonal - ci;
    if (ai >= 0 && ai < KOI_ANIONS.length) koiSaltPairs.push([KOI_CATIONS[ci], KOI_ANIONS[ai]]);
  }
}
for (const [cation, anion] of koiSaltPairs) {
  if (koiGeneratedSaltCount >= KOI_SALT_LIMIT || koiChemicalCount() >= KOI_TARGET_CHEMICALS) break;
  const formula = koiFormulaForSalt(cation, anion);
  const formulaKey = koiFormulaKey(formula);
  if (KOI_KNOWN_FORMULAS.has(formulaKey)) continue;
  const id = `gen_salt_${cation.key}_${anion.key}`;
  if (!koiAddChemical(id, formula, `${cation.n} ${anion.n}`, "salt", { generatedBy:"KOI balanced-ion library" })) continue;
  KOI_KNOWN_FORMULAS.add(formulaKey);
  KOI_FORMULA_TO_ID.set(formulaKey, id);
  koiGeneratedSaltCount++;
  const acidId = koiResolveAcid(anion);
  const baseId = koiBaseForCation(cation);
  if (acidId && baseId && S.H2O) {
    const gcd = koiGcd(cation.q, anion.q);
    KOI_GENERATED_SALT_ROUTES.push({
      r:[baseId, acidId], p:[id,"H2O"], cond:"trung hòa axit–bazơ (mô phỏng)",
      eq:`${(anion.q/gcd===1?"":anion.q/gcd)+koiSubscriptFormula(S[baseId].f.replace(/<[^>]*>/g,""))} + ${(cation.q/gcd===1?"":cation.q/gcd)+koiSubscriptFormula(anion.acidF || "")} → ${koiSubscriptFormula(formula)} + ${(cation.q*anion.q/gcd===1?"":cation.q*anion.q/gcd)+"H₂O"}`,
      note:"Phương trình tổng quát sinh từ điện tích ion; hãy kiểm tra điều kiện và độ tan của chất cụ thể."
    });
  }
}

/* Tên gốc dùng để sinh dãy đồng đẳng hữu cơ; các đồng phân có ID riêng. */
const KOI_ROOTS = ["","met","et","prop","but","pent","hex","hept","oct","non","dec","undec","dodec","tridec","tetradec","pentadec","hexadec","heptadec","octadec","nonadec","icos","henicos","docos","tricos","tetracos","pentacos","hexacos","heptacos","octacos","nonacos","triacont","hentriacont","dotriacont","tritriacont","tetratriacont","pentatriacont","hexatriacont","heptatriacont","octatriacont","nonatriacont","tetracont","hentetracont","dotetracont","tritetracont","tetratetracont","pentatetracont","hexatetracont","heptatetracont","octatetracont","nonatetracont","pentacont"];
function koiRoot(n) { return KOI_ROOTS[n] || `C${n}`; }
function koiMolecularFormula(parts) {
  return Object.entries(parts).filter(([,count]) => count > 0).map(([element,count]) => element + (count === 1 ? "" : count)).join("");
}
const KOI_ORGANIC_FAMILIES = [];
function koiAddOrganicFamily(familyName, items) { KOI_ORGANIC_FAMILIES.push({familyName, items}); }

const koiAlkanes = [];
for (let n = 1; n <= 50; n++) {
  if ([1,2,4,5].includes(n)) continue; // các chất đơn giản này đã có trong kho gốc
  koiAlkanes.push({id:`gen_alkane_${n}`, f:koiMolecularFormula({C:n,H:2*n+2}), n:`n-${koiRoot(n)}an · mạch thẳng`, c:"organic"});
}
koiAddOrganicFamily("ankan", koiAlkanes);

const koiAlkenes = [];
for (let n = 4; n <= 50; n++) {
  if (n === 4) continue; // buten và các đồng phân thường gặp đã có trong kho gốc
  for (let pos = 1; pos <= Math.floor(n/2); pos++) {
    const formula = koiMolecularFormula({C:n,H:2*n});
    koiAlkenes.push({id:`gen_alkene_${n}_p${pos}`,f:formula,n:`${koiRoot(n)}-${pos}-en`,c:"organic"});
    if (pos > 1 && n > 4) {
      koiAlkenes.push({id:`gen_alkene_${n}_p${pos}_E`,f:formula,n:`(E)-${koiRoot(n)}-${pos}-en`,c:"organic"});
      koiAlkenes.push({id:`gen_alkene_${n}_p${pos}_Z`,f:formula,n:`(Z)-${koiRoot(n)}-${pos}-en`,c:"organic"});
    }
  }
}
koiAddOrganicFamily("anken", koiAlkenes);

const koiAlkynes = [];
for (let n = 3; n <= 50; n++) {
  for (let pos = 1; pos <= Math.floor((n-1)/2); pos++) {
    koiAlkynes.push({id:`gen_alkyne_${n}_p${pos}`,f:koiMolecularFormula({C:n,H:2*n-2}),n:`${koiRoot(n)}-${pos}-in`,c:"organic"});
  }
}
koiAddOrganicFamily("ankin", koiAlkynes);

const koiAlcohols = [];
for (let n = 5; n <= 50; n++) {
  for (let pos = 1; pos <= Math.floor(n/2); pos++) {
    koiAlcohols.push({id:`gen_alcohol_${n}_p${pos}`,f:koiMolecularFormula({C:n,H:2*n+2,O:1}),n:`${koiRoot(n)}an-${pos}-ol`,c:"organic"});
  }
}
koiAddOrganicFamily("ancol", koiAlcohols);

const koiAldehydes = [];
for (let n = 5; n <= 50; n++) koiAldehydes.push({id:`gen_aldehyde_${n}`,f:koiMolecularFormula({C:n,H:2*n,O:1}),n:`${koiRoot(n)}anal`,c:"organic"});
koiAddOrganicFamily("andehit", koiAldehydes);

const koiKetones = [];
for (let n = 5; n <= 50; n++) {
  for (let pos = 2; pos <= Math.floor(n/2); pos++) koiKetones.push({id:`gen_ketone_${n}_p${pos}`,f:koiMolecularFormula({C:n,H:2*n,O:1}),n:`${koiRoot(n)}an-${pos}-on`,c:"organic"});
}
koiAddOrganicFamily("xeton", koiKetones);

const koiCarboxylicAcids = [];
for (let n = 4; n <= 50; n++) koiCarboxylicAcids.push({id:`gen_acid_${n}`,f:koiMolecularFormula({C:n,H:2*n,O:2}),n:`Axit ${koiRoot(n)}anoic`,c:"organic"});
koiAddOrganicFamily("axit cacboxylic", koiCarboxylicAcids);

const koiAmines = [];
for (let n = 3; n <= 40; n++) {
  for (let pos = 1; pos <= Math.floor((n+1)/2); pos++) koiAmines.push({id:`gen_amine_${n}_p${pos}`,f:koiMolecularFormula({C:n,H:2*n+3,N:1}),n:`${koiRoot(n)}an-${pos}-amin`,c:"organic"});
}
koiAddOrganicFamily("amin", koiAmines);

const koiHalides = [];
for (const [symbol, viName] of [["F","flo"],["Cl","clo"],["Br","bromo"],["I","iodo"]]) {
  for (let n = 1; n <= 35; n++) {
    for (let pos = 1; pos <= Math.floor((n+1)/2); pos++) {
      koiHalides.push({id:`gen_${viName}_${n}_p${pos}`,f:koiMolecularFormula({C:n,H:2*n+1,[symbol]:1}),n:`${pos}-${viName}${koiRoot(n)}an`,c:"organic"});
    }
  }
}
koiAddOrganicFamily("dẫn xuất halogen", koiHalides);

const koiEthers = [];
for (let total = 4; total <= 30; total++) {
  for (let a = 1; a <= Math.floor(total/2); a++) {
    const b = total - a;
    const alkyl = x => ({1:"metyl",2:"etyl",3:"propyl",4:"butyl"}[x] || `${koiRoot(x)}yl`);
    koiEthers.push({id:`gen_ether_${a}_${b}`,f:koiMolecularFormula({C:total,H:2*total+2,O:1}),n:`${alkyl(a)} ${alkyl(b)} ete`,c:"organic"});
  }
}
koiAddOrganicFamily("ete", koiEthers);

const koiEsters = [];
for (let total = 3; total <= 35; total++) {
  for (let acidC = 1; acidC < total; acidC++) {
    const alcoholC = total - acidC;
    if ((acidC === 1 && alcoholC === 2) || (acidC === 2 && alcoholC === 2)) continue; // ethyl formate and ethyl acetate đã có
    const alcoholName = ({1:"metyl",2:"etyl",3:"propyl",4:"butyl"}[alcoholC] || `${koiRoot(alcoholC)}yl`);
    const acidName = `${koiRoot(acidC)}anoat`;
    koiEsters.push({id:`gen_ester_a${acidC}_o${alcoholC}`,f:koiMolecularFormula({C:total,H:2*total,O:2}),n:`${alcoholName} ${acidName}`,c:"organic"});
  }
}
koiAddOrganicFamily("este", koiEsters);

const koiNitriles = [];
for (let n = 3; n <= 35; n++) koiNitriles.push({id:`gen_nitrile_${n}`,f:koiMolecularFormula({C:n,H:2*n-1,N:1}),n:`${koiRoot(n)}anonitril`,c:"organic"});
koiAddOrganicFamily("nitril", koiNitriles);

const koiAmides = [];
for (let n = 1; n <= 35; n++) koiAmides.push({id:`gen_amide_${n}`,f:koiMolecularFormula({C:n,H:2*n+1,N:1,O:1}),n:`${koiRoot(n)}anamit`,c:"organic"});
koiAddOrganicFamily("amit", koiAmides);

/* Chọn xen kẽ giữa các họ để kho đạt đủ 1.800 chất mà không nghiêng hẳn
   về một loại. Công thức lặp giữa đồng phân là bình thường trong hóa hữu cơ. */
let koiOrganicCursor = 0;
while (koiChemicalCount() < KOI_TARGET_CHEMICALS) {
  let addedThisRound = false;
  for (const family of KOI_ORGANIC_FAMILIES) {
    const item = family.items[koiOrganicCursor];
    if (!item) continue;
    if (koiChemicalCount() >= KOI_TARGET_CHEMICALS) break;
    if (!S[item.id]) {
      koiAddChemical(item.id, item.f, item.n, item.c, {generatedBy:family.familyName});
      addedThisRound = true;
    }
  }
  if (!addedThisRound && koiOrganicCursor > Math.max(...KOI_ORGANIC_FAMILIES.map(f => f.items.length))) break;
  koiOrganicCursor++;
}
if (koiChemicalCount() < KOI_TARGET_CHEMICALS) {
  console.warn(`KOI LAB: kho hóa học mới có ${koiChemicalCount()} / ${KOI_TARGET_CHEMICALS} chất; hãy bổ sung thêm họ chất trong KOI_ORGANIC_FAMILIES.`);
}

/* Tạo đường phản ứng trung hòa cho những muối được sinh từ cặp ion.
   R vẫn giữ nguyên toàn bộ phản ứng gốc; phần này chỉ bổ sung đường mới. */
const koiExistingReactionKeys = new Set(R.map(rx => `${[...(rx.r||[])].sort().join("+")}=>${[...(rx.p||[])].sort().join("+")}`));
for (const rx of KOI_GENERATED_SALT_ROUTES) {
  if (koiChemicalCount() < KOI_TARGET_CHEMICALS) break;
  const key = `${[...rx.r].sort().join("+")}=>${[...rx.p].sort().join("+")}`;
  if (koiExistingReactionKeys.has(key)) continue;
  R.push(rx);
  koiExistingReactionKeys.add(key);
}

/* Thêm đồng vị và hạt nhân thường gặp; tất cả vẫn khóa lúc đầu trừ khi
   được nêu trong nuclearUnlocked ở phần ENGINE. */
const KOI_NUCLEAR_ISOTOPES = [
  ["O19n","O",19,8,"Oxi-19"],["F18n","F",18,9,"Flo-18"],["Ne22n","Ne",22,10,"Neon-22"],
  ["Mg27n","Mg",27,12,"Magie-27"],["Al26n","Al",26,13,"Nhôm-26"],["Si31n","Si",31,14,"Silic-31"],
  ["P33n","P",33,15,"Photpho-33"],["S35n","S",35,16,"Lưu huỳnh-35"],["S36n","S",36,16,"Lưu huỳnh-36"],
  ["Ar39n","Ar",39,18,"Argon-39"],["K42n","K",42,19,"Kali-42"],["Ca42n","Ca",42,20,"Canxi-42"],
  ["Ca43n","Ca",43,20,"Canxi-43"],["Ca48n","Ca",48,20,"Canxi-48"],["Cr48n","Cr",48,24,"Crôm-48"],
  ["Fe54n","Fe",54,26,"Sắt-54"],["Ni62n","Ni",62,28,"Niken-62"],["Cu65n","Cu",65,29,"Đồng-65"],
  ["Zn66n","Zn",66,30,"Kẽm-66"],["Zn68n","Zn",68,30,"Kẽm-68"],["Br79n","Br",79,35,"Brom-79"],
  ["Br81n","Br",81,35,"Brom-81"],["Kr85n","Kr",85,36,"Krypton-85"],["Sr88n","Sr",88,38,"Stronti-88"],
  ["Sr90n","Sr",90,38,"Stronti-90"],["Y89n","Y",89,39,"Ytri-89"],["Y90n","Y",90,39,"Ytri-90"],
  ["Zr90n","Zr",90,40,"Zirconi-90"],["Mo99n","Mo",99,42,"Molypden-99"],["Ru103n","Ru",103,44,"Rutheni-103"],
  ["I129n","I",129,53,"Iot-129"],["Xe133n","Xe",133,54,"Xenon-133"],["Xe135n","Xe",135,54,"Xenon-135"],
  ["Cs137n","Cs",137,55,"Xesi-137"],["Ba140n","Ba",140,56,"Bari-140"],["La139n","La",139,57,"Lantan-139"],
  ["Ce140n","Ce",140,58,"Xeri-140"],["Nd144n","Nd",144,60,"Neodim-144"],["Eu152n","Eu",152,63,"Europi-152"],
  ["Gd157n","Gd",157,64,"Gadolini-157"],["W184n","W",184,74,"Wolfram-184"],["Au197n","Au",197,79,"Vàng-197"],
  ["Hg202n","Hg",202,80,"Thủy ngân-202"],["Pb208n","Pb",208,82,"Chì-208"],["Bi209n","Bi",209,83,"Bitmut-209"],
  ["Po218n","Po",218,84,"Poloni-218"],["Ra224n","Ra",224,88,"Radi-224"],["Ac227n","Ac",227,89,"Actini-227"],
  ["U234n","U",234,92,"Urani-234"],["U236n","U",236,92,"Urani-236"],["Th230n","Th",230,90,"Thori-230"],
  ["Th231n","Th",231,90,"Thori-231"],["Np237n","Np",237,93,"Neptuni-237"],["Pu240n","Pu",240,94,"Plutoni-240"],
  ["Am241n","Am",241,95,"Americi-241"],["Y90m","Y",90,39,"Ytri-90m (trạng thái kích thích)"],
  ["Cs137mn","Cs",137,55,"Xesi-137m (trạng thái kích thích)"],["Ba140mn","Ba",140,56,"Bari-140m (trạng thái kích thích)"]
];
for (const [id, symbol, mass, atomicNumber, name] of KOI_NUCLEAR_ISOTOPES) {
  if (S[id]) continue;
  const isomer = /\d+m(?:n)?$/.test(id);
  S[id] = {f:toSuperscript(mass)+(isomer?"ᵐ":"")+toSubscript(atomicNumber)+symbol,n:name,c:"nuclear",kind:"isotope",z:atomicNumber,a:mass,symbol,nuclearIsomer:isomer};
}

/* Phản ứng hạt nhân bổ sung: bắt hạt, phản ứng tổng hợp, phân rã và phân hạch
   mô phỏng. Đây là mô hình bảo toàn số khối/điện tích, không phải hướng dẫn vận hành. */
const KOI_EXTRA_NUCLEAR_REACTIONS = [
  {r:["C12n","proton"],p:["N13n","gamma"],cond:"bắt proton",eq:"¹²₆C + ¹₁p → ¹³₇N + γ",note:"Phản ứng bắt proton minh họa."},
  {r:["N14n","neutron"],p:["N15n","gamma"],cond:"bắt nơtron",eq:"¹⁴₇N + ¹₀n → ¹⁵₇N + γ",note:"Tạo nitơ-15 bằng bắt nơtron."},
  {r:["O16n","neutron"],p:["O17n","gamma"],cond:"bắt nơtron",eq:"¹⁶₈O + ¹₀n → ¹⁷₈O + γ",note:"Tạo oxi-17 bằng bắt nơtron."},
  {r:["F19n","proton"],p:["Ne20n","gamma"],cond:"bắt proton",eq:"¹⁹₉F + ¹₁p → ²⁰₁₀Ne + γ",note:"Ví dụ phản ứng bắt proton."},
  {r:["C12n","alpha"],p:["O16n","gamma"],cond:"bắt hạt alpha",eq:"¹²₆C + ⁴₂He → ¹⁶₈O + γ",note:"Mô phỏng phản ứng tổng hợp hạt nhân."},
  {r:["O16n","alpha"],p:["Ne20n","gamma"],cond:"bắt hạt alpha",eq:"¹⁶₈O + ⁴₂He → ²⁰₁₀Ne + γ",note:"Mô phỏng quá trình bắt hạt alpha."},
  {r:["Ne20n","alpha"],p:["Mg24n","gamma"],cond:"bắt hạt alpha",eq:"²⁰₁₀Ne + ⁴₂He → ²⁴₁₂Mg + γ",note:"Mô phỏng tổng hợp hạt nhân ở môi trường năng lượng cao."},
  {r:["Mg24n","alpha"],p:["Si28n","gamma"],cond:"bắt hạt alpha",eq:"²⁴₁₂Mg + ⁴₂He → ²⁸₁₄Si + γ",note:"Mô phỏng tổng hợp hạt nhân."},
  {r:["Si28n","alpha"],p:["S32n","gamma"],cond:"bắt hạt alpha",eq:"²⁸₁₄Si + ⁴₂He → ³²₁₆S + γ",note:"Mô phỏng tổng hợp hạt nhân."},
  {r:["S32n","alpha"],p:["Ar36n","gamma"],cond:"bắt hạt alpha",eq:"³²₁₆S + ⁴₂He → ³⁶₁₈Ar + γ",note:"Mô phỏng tổng hợp hạt nhân."},
  {r:["Ar36n","alpha"],p:["Ca40n","gamma"],cond:"bắt hạt alpha",eq:"³⁶₁₈Ar + ⁴₂He → ⁴⁰₂₀Ca + γ",note:"Mô phỏng tổng hợp hạt nhân."},
  {r:["H3n"],p:["He3n","electron","antinu"],cond:"phân rã beta trừ",eq:"³₁H → ³₂He + e⁻ + ν̅ₑ",note:"Triti phân rã beta trừ thành heli-3."},
  {r:["C14n"],p:["N14n","electron","antinu"],cond:"phân rã beta trừ",eq:"¹⁴₆C → ¹⁴₇N + e⁻ + ν̅ₑ",note:"Cacbon-14 phân rã beta trừ thành nitơ-14."},
  {r:["Na24n"],p:["Mg24n","electron","antinu"],cond:"phân rã beta trừ",eq:"²⁴₁₁Na → ²⁴₁₂Mg + e⁻ + ν̅ₑ",note:"Natri-24 phân rã beta trừ."},
  {r:["P32n"],p:["S32n","electron","antinu"],cond:"phân rã beta trừ",eq:"³²₁₅P → ³²₁₆S + e⁻ + ν̅ₑ",note:"Photpho-32 phân rã beta trừ."},
  {r:["S35n"],p:["Cl35n","electron","antinu"],cond:"phân rã beta trừ",eq:"³⁵₁₆S → ³⁵₁₇Cl + e⁻ + ν̅ₑ",note:"Lưu huỳnh-35 phân rã beta trừ."},
  {r:["Ar41n"],p:["K41n","electron","antinu"],cond:"phân rã beta trừ",eq:"⁴¹₁₈Ar → ⁴¹₁₉K + e⁻ + ν̅ₑ",note:"Argon-41 phân rã beta trừ."},
  {r:["Sr90n"],p:["Y90n","electron","antinu"],cond:"phân rã beta trừ",eq:"⁹⁰₃₈Sr → ⁹⁰₃₉Y + e⁻ + ν̅ₑ",note:"Stronti-90 phân rã beta trừ."},
  {r:["Y90n"],p:["Zr90n","electron","antinu"],cond:"phân rã beta trừ",eq:"⁹⁰₃₉Y → ⁹⁰₄₀Zr + e⁻ + ν̅ₑ",note:"Ytri-90 phân rã beta trừ."},
  {r:["I131n"],p:["Xe131n","electron","antinu"],cond:"phân rã beta trừ",eq:"¹³¹₅₃I → ¹³¹₅₄Xe + e⁻ + ν̅ₑ",note:"Iot-131 phân rã beta trừ."},
  {r:["Cs137n"],p:["Ba137mn","electron","antinu"],cond:"phân rã beta trừ",eq:"¹³⁷₅₅Cs → ¹³⁷ᵐ₅₆Ba + e⁻ + ν̅ₑ",note:"Một nhánh phân rã beta của xesi-137 tạo bari-137m."},
  {r:["F18n"],p:["O18n","positron","nu"],cond:"phân rã beta cộng",eq:"¹⁸₉F → ¹⁸₈O + e⁺ + νₑ",note:"Flo-18 phân rã beta cộng."},
  {r:["Na22n"],p:["Ne22n","positron","nu"],cond:"phân rã beta cộng",eq:"²²₁₁Na → ²²₁₀Ne + e⁺ + νₑ",note:"Natri-22 có nhánh phân rã beta cộng."},
  {r:["Rn222n"],p:["Po218n","He4n"],cond:"phân rã alpha",eq:"²²²₈₆Rn → ²¹⁸₈₄Po + ⁴₂He",note:"Radon-222 phân rã alpha."},
  {r:["Am241n"],p:["Np237n","He4n"],cond:"phân rã alpha",eq:"²⁴¹₉₅Am → ²³⁷₉₃Np + ⁴₂He",note:"Americi-241 phân rã alpha."},
  {r:["Pu240n"],p:["U236n","He4n"],cond:"phân rã alpha",eq:"²⁴⁰₉₄Pu → ²³⁶₉₂U + ⁴₂He",note:"Plutoni-240 phân rã alpha."},
  {r:["U235n","neutron"],p:["Ba141n","Kr92n","neutron","neutron","neutron"],cond:"phân hạch — mô hình giáo dục",eq:"²³⁵₉₂U + ¹₀n → ¹⁴¹₅₆Ba + ⁹²₃₆Kr + 3¹₀n",note:"Ví dụ phân hạch lý thuyết; sản phẩm phân hạch thay đổi theo nhánh. Chỉ dùng để học bảo toàn số khối và điện tích."},
  {r:["U239n"],p:["Np239n","electron","antinu"],cond:"phân rã beta trừ",eq:"²³⁹₉₂U → ²³⁹₉₃Np + e⁻ + ν̅ₑ",note:"Urani-239 phân rã beta trừ thành neptuni-239."},
  {r:["Np239n"],p:["Pu239n","electron","antinu"],cond:"phân rã beta trừ",eq:"²³⁹₉₃Np → ²³⁹₉₄Pu + e⁻ + ν̅ₑ",note:"Neptuni-239 phân rã beta trừ thành plutoni-239."}
];
const koiNuclearReactionKeys = new Set(NX.map(rx => `${[...(rx.r||[])].sort().join("+")}=>${[...(rx.p||[])].sort().join("+")}`));
for (const rx of KOI_EXTRA_NUCLEAR_REACTIONS) {
  const key = `${[...(rx.r||[])].sort().join("+")}=>${[...(rx.p||[])].sort().join("+")}`;
  if (!koiNuclearReactionKeys.has(key)) { NX.push(rx); koiNuclearReactionKeys.add(key); }
}

/* VÙNG TÙY CHỈNH — sửa các mảng/object dưới đây khi cần.
   Ví dụ chất mới (bỏ dấu // để sử dụng):
   DemoCompound: { f:"Na₂CO₃", n:"Natri cacbonat tùy chỉnh", c:"salt" }
*/
const MANUAL_SUBSTANCES = {
  // DemoCompound: { f:"Na₂CO₃", n:"Natri cacbonat tùy chỉnh", c:"salt" }
};
const MANUAL_CHEMISTRY_REACTIONS = [
  // { r:["H2","O2"], p:["H2O"], cond:"đốt cháy", eq:"2H₂ + O₂ → 2H₂O" }
];
const MANUAL_NUCLEAR_REACTIONS = [
  // { r:["C12n","neutron"], p:["C13n","gamma"], cond:"bắt nơtron", eq:"¹²₆C + ¹₀n → ¹³₆C + γ" }
];
const REMOVED_SUBSTANCE_IDS = [
  // "gen_salt_Na_Cl"
];
Object.assign(S, MANUAL_SUBSTANCES);
R.push(...MANUAL_CHEMISTRY_REACTIONS);
NX.push(...MANUAL_NUCLEAR_REACTIONS);
if (REMOVED_SUBSTANCE_IDS.length) {
  const removedIds = new Set(REMOVED_SUBSTANCE_IDS);
  for (const id of removedIds) delete S[id];
  for (const collection of [R, NX]) {
    const kept = collection.filter(rx => [...(rx.r||[]), ...(rx.p||[])].every(id => !removedIds.has(id)));
    collection.splice(0, collection.length, ...kept);
  }
}

/* =========================================================
   ENGINE
   ========================================================= */
const CATS = [
  {id:"all",label:"Tất cả"},
  {id:"element",label:"Đơn chất"},
  {id:"periodic",label:"Bảng tuần hoàn"},
  {id:"oxide",label:"Oxit"},
  {id:"base",label:"Bazơ"},
  {id:"acid",label:"Axit"},
  {id:"salt",label:"Muối"},
  {id:"organic",label:"Hữu cơ"},
  {id:"polymer",label:"Polymer"},
  {id:"other",label:"Khác"}
];
const allIds = Object.keys(S);
const elementIds = allIds.filter(id=>S[id].c==="element");
// Chemistry progression: only elemental substances are available at the start.
// Every compound (oxide, acid, base, salt, organic substance, polymer, etc.)
// stays locked until it appears as a product of a successful reaction.
let unlocked = new Set(elementIds);
// Tiến trình mở khóa riêng cho hạt nhân: chỉ mở một nhóm hạt và đồng vị cơ bản ban đầu.
const nuclearUnlocked = new Set(["neutron","proton","alpha","gamma","H2n","He3n","C12n"]);
let flask = [];
let activeCat = "all";
let activeMode = "chemistry";
let reactionCount = 0;

const elTiles = document.getElementById("tiles");
const elTabs = document.getElementById("tabs");
const elFlask = document.getElementById("flask");
const elResult = document.getElementById("resultArea");
const elLog = document.getElementById("log");
const elSearch = document.getElementById("search");
const reactBtn = document.getElementById("reactBtn");
const clearBtn = document.getElementById("clearBtn");
const chemModeBtn = document.getElementById("chemModeBtn");
const nuclearModeBtn = document.getElementById("nuclearModeBtn");

function currentReactions(){ return activeMode === "nuclear" ? NX : R; }
function modeCategories(){
  return activeMode === "nuclear"
    ? [{id:"all",label:"Tất cả"},{id:"particles",label:"Hạt bắn phá"},{id:"isotopes",label:"Đồng vị / hạt nhân"}]
    : CATS;
}
function updateModeCopy(){
  const nuclear = activeMode === "nuclear";
  document.body.dataset.mode = nuclear ? "nuclear" : "chemistry";
  chemModeBtn.classList.toggle("active", !nuclear);
  nuclearModeBtn.classList.toggle("active", nuclear);
  chemModeBtn.setAttribute("aria-pressed", String(!nuclear));
  nuclearModeBtn.setAttribute("aria-pressed", String(nuclear));
  document.getElementById("modeTitle").textContent = nuclear ? "Phản ứng hạt nhân" : "Phản ứng hóa học";
  document.getElementById("modeDescription").textContent = nuclear
    ? "Chọn hạt bắn phá cùng đồng vị mục tiêu để mô phỏng biến đổi hạt nhân."
    : "Kết hợp chất, khám phá sản phẩm và mở khóa kho chất.";
  document.getElementById("modeDisclaimer").innerHTML = nuclear
    ? '<span class="disclaimer-dot"></span><span>MÔ PHỎNG GIÁO DỤC · Theo dõi bảo toàn số khối và điện tích; không phải hướng dẫn thực nghiệm.</span>'
    : '<span class="disclaimer-dot"></span><span>CHẾ ĐỘ HỌC TẬP · Điều kiện phản ứng được hiển thị cùng phương trình.</span>';
  document.getElementById("inventoryTitle").textContent = nuclear ? "Kho hạt & đồng vị — chọn chất đầu vào" : "Kho chất — bấm để thêm vào bình";
  document.getElementById("flaskTitle").textContent = nuclear ? "Buồng tương tác hạt nhân" : "Bình phản ứng";
  document.getElementById("benchLabel").textContent = nuclear ? "NUCLEAR CHAMBER / HẠT NHÂN" : "REACTION CHAMBER / HÓA HỌC";
  document.getElementById("inventoryCount").textContent = nuclear ? "Hạt bắn phá + hạt nhân đồng vị" : "Kho chất vô cơ, hữu cơ và polymer";
}

document.getElementById("fCount").textContent = allIds.filter(id => S[id] && S[id].c !== "nuclear").length;
document.getElementById("nCount").textContent = allIds.filter(id => S[id] && S[id].c === "nuclear").length;
document.getElementById("fReact").textContent = R.length + NX.length;

function renderTabs(){
  elTabs.innerHTML = "";
  modeCategories().forEach(cat=>{
    const b = document.createElement("button");
    b.className = "tab" + (cat.id===activeCat ? " active":"");
    b.textContent = cat.label;
    b.type = "button";
    b.onclick = ()=>{ activeCat = cat.id; renderTabs(); renderTiles(); };
    elTabs.appendChild(b);
  });
}

function renderTiles(){
  const q = elSearch.value.trim().toLowerCase();
  elTiles.innerHTML = "";
  elTiles.classList.toggle("periodic-grid", activeMode === "chemistry" && activeCat === "periodic");
  let visibleCount = 0;
  allIds.forEach(id=>{
    const sub = S[id];
    const isNuclear = sub.c === "nuclear";
    if(activeMode === "nuclear" && !isNuclear) return;
    if(activeMode === "chemistry" && isNuclear) return;
    if(activeCat !== "all"){
      if(activeMode === "nuclear"){
        if(activeCat === "particles" && sub.kind !== "particle") return;
        if(activeCat === "isotopes" && sub.kind !== "isotope") return;
      } else if(activeCat === "periodic") {
        if(sub.c !== "element" || !sub.z) return;
      } else if(sub.c !== activeCat) return;
    }
    const plain = sub.f.replace(/<[^>]+>/g, "").toLowerCase();
    if(q && !plain.includes(q) && !sub.n.toLowerCase().includes(q) && !id.toLowerCase().includes(q) && !String(sub.z || "").includes(q)) return;
    visibleCount++;
    const isUnlocked = (activeMode === "nuclear" ? nuclearUnlocked : unlocked).has(id);
    const div = document.createElement("div");
    div.className = "tile c-" + sub.c + (isUnlocked ? "" : " locked");
    if(activeMode === "chemistry" && activeCat === "periodic"){
      div.classList.add("periodic-cell", "pt-" + (sub.family || "transition"));
      div.style.gridColumn = String(sub.group);
      div.style.gridRow = String(sub.period);
      div.innerHTML = `<span class="atomic-number">${sub.z}</span><span class="f">${sub.f}</span><span class="n">${sub.n}</span>`;
      div.title = `${sub.z} · ${sub.f} — ${sub.n}${sub.family ? " · " + sub.family : ""}. Bấm để thêm vào bình.`;
    }else{
      div.innerHTML = `<div class="catbar"></div><span class="f">${sub.f}</span><span class="n">${sub.n}</span>`;
    }
    if(isUnlocked){
      div.onclick = ()=>addToFlask(id);
      if(!(activeMode === "chemistry" && activeCat === "periodic")) div.title = "Thêm " + sub.n + " vào bình";
      div.setAttribute("role","button");
      div.tabIndex = 0;
      div.onkeydown = e=>{if(e.key === "Enter" || e.key === " "){e.preventDefault();addToFlask(id);}};
    } else {
      div.title = "Chưa được khám phá";
      div.setAttribute("aria-disabled","true");
    }
    elTiles.appendChild(div);
  });
  document.getElementById("inventoryCount").textContent = activeMode === "nuclear"
    ? `${visibleCount} mục trong kho hạt nhân`
    : `${visibleCount} mục trong kho hóa học`;
}

function addToFlask(id){ flask.push(id); renderFlask(); }
function removeFromFlask(idx){ flask.splice(idx,1); renderFlask(); }
function renderFlask(){
  elFlask.classList.toggle("empty", flask.length===0);
  elFlask.innerHTML = "";
  flask.forEach((id,idx)=>{
    const sub = S[id];
    const chip = document.createElement("div");
    chip.className = "chip" + (activeMode === "nuclear" ? " chip-nuclear" : "");
    chip.innerHTML = `<span class="f" style="font-weight:700">${sub.f}</span><span class="x" aria-hidden="true">✕</span>`;
    chip.title = "Bấm để bỏ " + sub.n;
    chip.setAttribute("role","button");
    chip.tabIndex = 0;
    chip.onclick = ()=>removeFromFlask(idx);
    chip.onkeydown = e=>{if(e.key === "Enter" || e.key === " "){e.preventDefault();removeFromFlask(idx);}};
    elFlask.appendChild(chip);
  });
  reactBtn.disabled = flask.length < 1;
}

function hasReactants(ingredients, selected){
  // Hóa học: mỗi chất được chọn một lần như danh sách thành phần. Hạt nhân: đếm từng hạt riêng.
  if(activeMode === "chemistry") return ingredients.every(id => selected.includes(id));
  const counts = new Map();
  selected.forEach(id=>counts.set(id,(counts.get(id)||0)+1));
  for(const id of ingredients){
    const count = counts.get(id)||0;
    if(count < 1) return false;
    counts.set(id,count-1);
  }
  return true;
}
function findReaction(selected){
  let best = null;
  for(const rx of currentReactions()){
    if(!hasReactants(rx.r,selected)) continue;
    if(!best || rx.r.length > best.r.length) best = rx;
  }
  return best;
}
function ensureProductSubstance(id){
  if(S[id]) return;
  const subs = {"0":"₀","1":"₁","2":"₂","3":"₃","4":"₄","5":"₅","6":"₆","7":"₇","8":"₈","9":"₉"};
  const formula = String(id).trim().replace(/[0-9]/g, d=>subs[d] || d);
  S[id] = {f:formula,n:"Sản phẩm " + String(id).trim(),c:activeMode === "nuclear" ? "nuclear" : "other",kind:activeMode === "nuclear" ? "isotope" : undefined};
  allIds.push(id);
}
function doReaction(){
  const rx = findReaction(flask);
  if(!rx){
    const msg = activeMode === "nuclear"
      ? "Chưa tìm thấy phương trình hạt nhân phù hợp với tổ hợp đã chọn. Hãy kiểm tra hạt bắn phá, đồng vị mục tiêu và số lượng từng hạt."
      : "Không tìm thấy phản ứng nào khớp với tổ hợp chất đã chọn trong cơ sở dữ liệu hiện tại.";
    elResult.innerHTML = `<div class="result no"><div class="eqline">${msg}</div></div>`;
    return;
  }
  rx.p.forEach(ensureProductSubstance);
  const consumedReactants = activeMode === "chemistry" ? [...new Set(rx.r)] : rx.r;
  consumedReactants.forEach(id=>{ const idx=flask.indexOf(id); if(idx>-1) flask.splice(idx,1); });
  const productsToAdd = activeMode === "chemistry" ? [...new Set(rx.p)] : rx.p;
  const newlyUnlocked = [];
  const activeUnlocks = activeMode === "nuclear" ? nuclearUnlocked : unlocked;
  productsToAdd.forEach(id=>{
    if(!activeUnlocks.has(id)){ activeUnlocks.add(id); newlyUnlocked.push(id); }
    flask.push(id);
  });
  reactionCount++;
  const condHtml = `<div class="cond">${rx.cond ? "Điều kiện / kiểu biến đổi: " + rx.cond : "Điều kiện: không ghi riêng"}</div>`;
  const unlockHtml = newlyUnlocked.length
    ? `<div class="unlockline">🔓 Mở khóa: ${newlyUnlocked.map(id=>S[id].f+" ("+S[id].n+")").join(", ")}</div>` : "";
  const noteHtml = activeMode === "nuclear" && rx.note ? `<div class="nuclear-note">${rx.note}<br><strong>Lưu ý:</strong> Mô phỏng lý thuyết; không dùng làm hướng dẫn thí nghiệm.</div>` : "";
  const resultClass = activeMode === "nuclear" ? "result ok nuclear-result" : "result ok";
  elResult.innerHTML = `<div class="${resultClass}"><div class="eqline">${rx.eq}</div>${condHtml}${noteHtml}${unlockHtml}</div>`;

  const li = document.createElement("div");
  li.className = "logitem" + (activeMode === "nuclear" ? " nuclear-entry" : "");
  li.innerHTML = `<b>${rx.eq}</b><span class="lcond">${activeMode === "nuclear" ? "HẠT NHÂN · " : "HÓA HỌC · "}${rx.cond || "không cần điều kiện"}</span>`;
  if(elLog.children.length===1 && elLog.children[0].style.border === "none") elLog.innerHTML="";
  elLog.appendChild(li);
  renderFlask();
  renderTiles();
  updateStats();
}
function updateStats(){
  const isNuclear = activeMode === "nuclear";
  const modeIds = allIds.filter(id => (S[id].c === "nuclear") === isNuclear);
  const modeUnlocks = isNuclear ? nuclearUnlocked : unlocked;
  const modeUnlockedCount = modeIds.filter(id => modeUnlocks.has(id)).length;
  document.getElementById("fCount").textContent = allIds.filter(id => S[id] && S[id].c !== "nuclear").length;
  document.getElementById("nCount").textContent = allIds.filter(id => S[id] && S[id].c === "nuclear").length;
  document.getElementById("fReact").textContent = R.length + NX.length;
  document.getElementById("statUnlocked").textContent = modeUnlockedCount + "/" + modeIds.length;
  document.getElementById("statReactions").textContent = reactionCount;
}
function switchMode(mode){
  activeMode = mode;
  activeCat = "all";
  flask = [];
  elResult.innerHTML = "";
  updateModeCopy();
  renderTabs();
  renderTiles();
  renderFlask();
  updateStats();
}
chemModeBtn.onclick = ()=>switchMode("chemistry");
nuclearModeBtn.onclick = ()=>switchMode("nuclear");
reactBtn.onclick = doReaction;
clearBtn.onclick = ()=>{flask=[];renderFlask();elResult.innerHTML="";};
elSearch.oninput = renderTiles;

updateModeCopy();
renderTabs();
renderTiles();
renderFlask();
updateStats();
</script>
<script>
const blockedLink = "https://2410phongnguyen-eng.github.io/KOILABORATORY/";

document.addEventListener("DOMContentLoaded", () => {
    document.querySelectorAll("a").forEach(link => {
        if (
            link.href === blockedLink ||
            link.href.startsWith(blockedLink)
        ) {
            link.remove(); // Xóa hoàn toàn khỏi trang
        }
    });
});
</script>
</body>
</html>
