<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>PAYMENT NISYA — VVIP</title>
<meta name="description" content="Payment NISYA — Premium VVIP: DANA. Blur glassmorphism, HD + smooth UI." />
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --bg-1:#070617;
    --bg-2:#0f1630;
    --accent-a:#7c5cff;
    --accent-b:#00d4ff;
    --glass: rgba(255,255,255,0.06);
    --stroke: rgba(255,255,255,0.12);
    --text:#eef1ff;
    --muted:#b6c0ff;
    --radius:20px;
    --blur:18px;
    --shadow-lg: 0 24px 68px rgba(3,6,23,0.65);
    --transition: 320ms cubic-bezier(.2,.9,.2,1);
  }

  *{box-sizing:border-box}
  html,body{height:100%;margin:0;font-family:'Poppins',system-ui,-apple-system; background: radial-gradient(800px 500px at 10% 10%, rgba(124,92,255,0.12), transparent 30%), radial-gradient(700px 420px at 90% 30%, rgba(0,212,255,0.06), transparent 30%), linear-gradient(135deg,var(--bg-1),var(--bg-2)); color:var(--text); -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;}

  /* Preloader (full-screen) */
  #preloader{
    position:fixed; inset:0; display:grid; place-items:center; z-index:9999;
    background: linear-gradient(180deg, rgba(3,6,23,0.85), rgba(3,6,23,0.92));
  }
  .preloader-card{
    display:grid; gap:12px; place-items:center; padding:26px; border-radius:18px;
    background: linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.02));
    border:1px solid rgba(255,255,255,0.06); backdrop-filter: blur(8px);
    box-shadow: var(--shadow-lg);
  }
  .spinner {
    width:72px; height:72px; border-radius:50%;
    border:6px solid rgba(255,255,255,0.12); border-top-color:var(--accent-a);
    animation:spin 1s linear infinite;
    box-shadow: 0 8px 28px rgba(124,92,255,0.12);
  }
  @keyframes spin{to{transform:rotate(360deg)}}
  .preloader-title{font-weight:800; letter-spacing:1px; font-size:14px; background:linear-gradient(90deg,#fff,#b8c4ff,#fff); -webkit-background-clip:text; background-clip:text; color:transparent; filter:drop-shadow(0 8px 30px rgba(124,92,255,0.18));}

  /* background orbs */
  .orbs{position:fixed;inset:-10% -10% auto -10%;pointer-events:none;z-index:0;filter:blur(70px)}
  .orb{position:absolute;border-radius:50%;opacity:.55;mix-blend-mode:screen}
  .orb.a{width:420px;height:420px;left:3vw;top:8vh;background:radial-gradient(circle at 30% 30%,var(--accent-a),transparent 60%);animation:orbA 14s ease-in-out infinite alternate}
  .orb.b{width:380px;height:380px;right:6vw;top:24vh;background:radial-gradient(circle at 70% 70%,var(--accent-b),transparent 60%);animation:orbB 18s ease-in-out infinite alternate}
  .orb.c{width:460px;height:460px;left:35vw;bottom:-6vh;background:radial-gradient(circle at 50% 50%, #ff7ab1,transparent 60%);animation:orbC 20s ease-in-out infinite alternate}
  @keyframes orbA{from{transform:translateY(0)}to{transform:translateY(-40px) translateX(18px)}}
  @keyframes orbB{from{transform:translateY(0)}to{transform:translateY(28px) translateX(-28px)}}
  @keyframes orbC{from{transform:translateY(0)}to{transform:translateY(-30px) translateX(20px)}}

  /* layout container */
  .wrap{position:relative;z-index:2;max-width:1100px;margin:48px auto;padding:28px;display:grid;grid-template-columns: 1fr;gap:20px}
  @media(min-width:980px){.wrap{grid-template-columns: 360px 1fr;align-items:start}}

  /* left panel - hero */
  .hero{
    display:flex;flex-direction:column;gap:18px;
    align-items:center;text-align:center;
  }
  .brandCard{width:100%;padding:22px;border-radius:18px;background:var(--glass);border:1px solid var(--stroke);backdrop-filter:blur(var(--blur));box-shadow:var(--shadow-lg)}
  .brandLogo{width:72px;height:72px;border-radius:16px;background:linear-gradient(135deg,var(--accent-a),var(--accent-b));display:grid;place-items:center;font-weight:800;color:#07101a;font-size:22px;box-shadow:0 10px 30px rgba(12,16,40,0.45)}
  .mainTitle{font-size:22px;font-weight:800}
  .desc{color:var(--muted);font-size:13px;line-height:1.5;max-width:320px;margin:0 auto}

  /* right panel - cards grid */
  .grid{display:grid;gap:18px}
  @media(min-width:720px){.grid{grid-template-columns:repeat(1,1fr)}}
  @media(min-width:1100px){.grid{grid-template-columns:repeat(2,1fr)}}

  .card{
    background:var(--glass); border-radius:16px; padding:18px; border:1px solid var(--stroke);
    backdrop-filter: blur(var(--blur)); transition:transform var(--transition), box-shadow var(--transition);
    box-shadow: 0 10px 40px rgba(2,6,20,0.45); position:relative; overflow:hidden;
  }
  .card:hover{transform:translateY(-8px); box-shadow: 0 22px 80px rgba(2,6,20,0.6)}
  .badge{display:inline-flex;padding:8px 12px;border-radius:999px;background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.04);font-weight:600;font-size:13px;color:var(--muted)}
  .brandRow{display:flex;align-items:center;gap:12px;margin-top:12px}
  .brandRow h3{margin:0;font-size:18px;font-weight:800}
  .muted{color:var(--muted);font-size:13px}

  .field{display:flex;align-items:center;gap:10px;margin-top:14px;padding:10px;border-radius:12px;background:rgba(255,255,255,0.03);border:1px dashed rgba(255,255,255,0.04);font-family:ui-monospace,monospace;font-weight:600;color:var(--text)}
  .field .val{letter-spacing:1px}
  .btn{cursor:pointer;padding:10px 12px;border-radius:12px;border:1px solid var(--stroke);background:linear-gradient(135deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));color:var(--text);font-weight:700;transition:all var(--transition)}
  .btn:hover{transform:translateY(-4px);box-shadow:0 12px 30px rgba(2,6,20,0.45)}
  .btnPrimary{background:linear-gradient(135deg,var(--accent-a),var(--accent-b));color:#07101a;border-color:transparent}

  /* toast */
  .toast{position:fixed;right:22px;bottom:22px;padding:12px 16px;border-radius:12px;background:linear-gradient(90deg,rgba(255,255,255,0.06),rgba(255,255,255,0.03));border:1px solid rgba(255,255,255,0.06);color:var(--text);box-shadow:0 14px 40px rgba(2,6,20,0.5);transform:translateY(20px);opacity:0;pointer-events:none;transition:all 320ms}
  .toast.show{transform:translateY(0);opacity:1;pointer-events:auto}

  footer{margin-top:18px;color:var(--muted);text-align:center;font-size:13px}
  /* small helpers */
  .linkSmall{font-size:13px;color:var(--muted);text-decoration:underline}
</style>
</head>
<body>

  <!-- Preloader -->
  <div id="preloader" aria-hidden="false">
    <div class="preloader-card" role="status" aria-live="polite">
      <div class="spinner" aria-hidden="true"></div>
      <div class="preloader-title">PAYMENT NISYA — VVIP LOADING</div>
    </div>
  </div>

  <!-- Orbs -->
  <div class="orbs" aria-hidden="true">
    <div class="orb a"></div><div class="orb b"></div><div class="orb c"></div>
  </div>

  <main class="wrap" role="main">
    <!-- Left Hero / Brand -->
    <section class="hero">
      <div class="brandCard">
        <div style="display:flex;gap:14px;align-items:center;justify-content:center;flex-direction:column">
          <div class="brandLogo">N</div>
          <div class="mainTitle">PAYMENT NISYA — VVIP</div>
          <p class="desc">Desain premium VVIP — HD, glassmorphism, animasi halus. Salin nomor DANA untuk konfirmasi cepat.</p>
          <div style="display:flex;gap:12px;margin-top:12px">
            <a class="btn btnPrimary" href="#dana">DANA</a>
          </div>
        </div>
      </div>

      <footer style="margin-top:14px">© <strong>NISYA</strong> · VVIP Interface</footer>
    </section>

    <!-- Right content grid -->
    <section class="grid" aria-label="Metode Pembayaran">
      <!-- DANA -->
      <article id="dana" class="card" aria-labelledby="dana-title">
        <span class="badge">🏦 Dompet Digital</span>
        <div class="brandRow">
          <svg width="36" height="36" viewBox="0 0 48 48" fill="none"><circle cx="24" cy="24" r="22" fill="#1DA1F2"/><rect x="12" y="18" width="24" height="12" rx="6" fill="white"/></svg>
          <h3 id="dana-title">DANA</h3>
        </div>
        <p class="muted">Transfer cepat & aman — klik salin lalu paste di aplikasi DANA.</p>

        <div class="field" role="region" aria-label="Nomor DANA">
          <div style="flex:1">
            <div style="font-size:12px;color:var(--muted)">No. DANA</div>
            <div class="val" id="dana-real">082197700833</div>
            <div style="font-size:12px;color:var(--muted);margin-top:4px">A/N: NISYA</div>
          </div>
          <div style="display:flex;flex-direction:column;gap:8px;margin-left:12px">
            <button class="btn btnPrimary" onclick="copyValue('dana-real')">Salin</button>
            <button class="btn" onclick="qrHint()">Cara Bayar</button>
          </div>
        </div>
      </article>

      <!-- Extra: Info Card -->
      <article class="card" aria-hidden="true">
        <span class="badge">ℹ️ Info</span>
        <div style="margin-top:12px">
          <p class="muted">Transaksi dikonfirmasi setelah transfer. Simpan bukti transfer dan hubungi NISYA bila perlu.</p>
          <p style="margin-top:12px"><span class="linkSmall">Desain: https://wa.me/6282197700833</span></p>
        </div>
      </article>

    </section>
  </main>

  <!-- toast -->
  <div id="toast" class="toast" role="status" aria-live="polite"></div>

<script>
  // Preloader hide
  window.addEventListener('load', ()=> {
    const p = document.getElementById('preloader');
    p.style.transition = 'opacity 420ms ease';
    p.style.opacity = '0';
    setTimeout(()=> { p.remove(); }, 480);
  });

  // Copy value helper
  function copyValue(id){
    const el = document.getElementById(id);
    if(!el) return showToast('Tidak ditemukan');
    const text = el.textContent.trim();
    navigator.clipboard?.writeText(text).then(()=> showToast('Tersalin: ' + text)).catch(()=> {
      // fallback
      try{
        const ta = document.createElement('textarea'); ta.value = text; document.body.appendChild(ta); ta.select();
        document.execCommand('copy'); ta.remove(); showToast('Tersalin: ' + text);
      }catch(e){ showToast('Gagal menyalin'); }
    });
  }

  // Toast
  function showToast(msg, ms=2200){
    const t = document.getElementById('toast');
    t.textContent = msg; t.classList.add('show');
    clearTimeout(showToast._t); showToast._t = setTimeout(()=> t.classList.remove('show'), ms);
  }

  // quick user hint
  function qrHint(){ showToast('Untuk bayar: buka aplikasi DANA → pilih transfer → masukkan nomor.'); }
</script>
</body>
</html>
