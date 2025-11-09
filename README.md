<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>PawwGamingZY - Pendaftaran Turnamen 2025</title>
  <meta name="description" content="Pendaftaran PawwGamingZY Esports Tournament 2025 - MLBB | FF | PUBG Mobile | Valorant" />
  <style>
    :root{
      --bg1:#e8eaee;
      --bg2:#f4f5f8;
      --card:#ffffff;
      --muted:#8b8f98;
      --accent:#6b7280;
      --accent-2:#7c3aed;
      --anime-accent:#b7c0ff;
      --radius:18px;
      font-family:Inter,ui-sans-serif,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;
    }

    html, body {
      margin: 0;
      padding: 0;
      min-height: 100%;
      overflow-x: hidden;
      overflow-y: auto;
      background: linear-gradient(135deg,var(--bg1),var(--bg2));
      color: #111;
    }
    canvas#particles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -2;
      pointer-events: none;
    }

    .wrap {
      max-width: 1100px;
      margin: 28px auto;
      padding: 24px;
      display: grid;
      grid-template-columns: 1fr 420px;
      gap: 20px;
      position: relative;
      z-index: 2;
    }

    .hero {
      background: linear-gradient(180deg, rgba(255,255,255,0.92), rgba(250,250,253,0.9));
      backdrop-filter: blur(6px);
      border-radius: var(--radius);
      padding: 26px;
      box-shadow: 0 10px 30px rgba(16,24,40,0.08);
      display: flex;
      flex-direction: column;
      gap: 18px;
      align-items: flex-start;
      min-height: auto;
    }

    .brand {display: flex; align-items:center; gap:14px;}
    .logo {
      position: relative;
      width: 88px; height:88px;
      border-radius:16px;
      display:flex; align-items:center; justify-content:center;
      background:linear-gradient(135deg,var(--anime-accent),#dfe6ff);
      font-weight:900; color:#0f172a; font-size:20px;
      box-shadow:0 10px 30px rgba(124,58,237,0.12);
      transform-style: preserve-3d;
    }
    .logo::before {
      content:"";
      position:absolute; left:50%; top:50%;
      transform:translate(-50%,-50%);
      width:120px; height:120px;
      border-radius:20px;
      background: radial-gradient(circle at 30% 20%, rgba(123,102,255,0.18), transparent 30%),
                  radial-gradient(circle at 80% 80%, rgba(183,192,255,0.12), transparent 30%);
      filter: blur(12px);
      z-index:-1;
    }
    .brand-text h1{margin:0;font-size:22px;color:#0f172a;animation:fadeUp .7s ease both}
    .brand-text p{margin:0;color:var(--muted);line-height:1.4;animation:fadeUp .9s ease both}

    .features{display:flex;gap:10px;flex-wrap:wrap;margin-top:6px}
    .chip{background:var(--card);padding:8px 12px;border-radius:999px;border:1px solid rgba(230,232,250,0.8);font-weight:700;color:var(--accent);font-size:13px}

    .card{background:var(--card);border-radius:14px;padding:14px;border:1px solid #eef0f5;box-shadow:0 6px 20px rgba(15,23,42,0.03)}
    .side{display:flex;flex-direction:column;gap:16px}
    .embed-wrap{height:560px;border-radius:14px;overflow:hidden;border:1px solid #e6e8eb;box-shadow:0 6px 20px rgba(15,23,42,0.04)}
    iframe{width:100%;height:100%;border:0;background:white}

    .cta{display:inline-flex;align-items:center;gap:10px;background:linear-gradient(90deg,var(--accent),var(--accent-2));color:#fff;padding:12px 18px;border-radius:12px;font-weight:800;text-decoration:none;box-shadow:0 8px 26px rgba(99,102,241,0.18);border:0;cursor:pointer;transform:translateZ(0);transition:all .22s ease}
    .cta:hover{transform:translateY(-6px) scale(1.02);box-shadow:0 18px 40px rgba(124,58,237,0.22)}

    .grid-2{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:12px}
    .section-title{font-weight:800;color:#0f172a;margin:0 0 8px 0}
    .muted{color:var(--muted);font-size:14px}

    .timeline{display:flex;flex-direction:column;gap:12px}
    .timeline .item{background:linear-gradient(180deg,#fff,#fbfbff);padding:10px;border-radius:10px;border:1px solid #eef2ff}

    .prize{display:flex;flex-direction:column;gap:8px}
    .prize-amount{font-size:20px;font-weight:900;color:var(--accent-2)}

    .audio-btn{position:fixed;right:18px;top:18px;background:rgba(255,255,255,0.9);border-radius:12px;padding:10px;box-shadow:0 6px 18px rgba(2,6,23,0.08);z-index:999;cursor:pointer;border:1px solid #eef2ff}

    .payment-wrap{margin-top:18px}
    .payment-card{background:linear-gradient(180deg,rgba(124,58,237,0.06),rgba(167,139,250,0.03));border-radius:14px;padding:18px;display:flex;flex-direction:column;align-items:center;gap:12px;border:1px solid rgba(124,58,237,0.08);box-shadow:0 14px 40px rgba(124,58,237,0.08)}
    .qr-img{width:200px;height:200px;border-radius:12px;object-fit:contain;box-shadow:0 8px 30px rgba(99,102,241,0.12);transition:transform .18s ease,box-shadow .18s ease}
    .qr-img:hover{transform:scale(1.05);box-shadow:0 20px 60px rgba(124,58,237,0.18)}
    .pay-note{color:var(--muted);font-size:14px;text-align:center}
    .wh-btn{display:inline-flex;align-items:center;gap:10px;background:linear-gradient(90deg,#06b6d4,#7c3aed);color:#fff;padding:10px 14px;border-radius:12px;font-weight:800;text-decoration:none;box-shadow:0 10px 30px rgba(0,0,0,0.12)}

    @keyframes fadeUp{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:translateY(0)}}

    @media(max-width:980px){
      .wrap{grid-template-columns:1fr;padding:18px}
      .embed-wrap{height:420px}
      .grid-2{grid-template-columns:1fr}
      .qr-img{width:160px;height:160px}
    }
  </style>
</head>
<body>
  <canvas id="particles"></canvas>
  <audio id="bgAudio" loop preload="auto" src="assets/lofi-chill-loop.mp3"></audio>
  <button class="audio-btn" id="audioToggle" aria-pressed="false">🔈 Musik: Mati</button>

  <main class="wrap">
    <!-- Konten Hero, Form, Timeline, Payment seperti sebelumnya -->
    <!-- Bisa copy langsung dari versi terakhir yang sudah kita perbaiki -->
  </main>

  <script>
    // Script particles, audio toggle, logo hover (sama seperti versi terakhir)
  </script>
</body>
</html>

