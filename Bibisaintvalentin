<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Bibi ❤️</title>
  <style>
    :root{
      --bg:#0b0b12; --card:#141424; --txt:#ffffff; --muted:#c9c9d6;
      --yes:#ff3b7a; --no:#2b2b3f;
    }
    *{box-sizing:border-box;font-family:system-ui,-apple-system,Segoe UI,Roboto,Arial;}
    body{
      margin:0; min-height:100vh; display:grid; place-items:center;
      background:radial-gradient(1000px 520px at 50% 0%, #2a1b3d 0%, var(--bg) 60%);
      color:var(--txt);
    }
    .card{
      width:min(560px,92vw);
      background:rgba(20,20,36,.92);
      border:1px solid rgba(255,255,255,.08);
      border-radius:18px;
      padding:22px;
      box-shadow:0 20px 60px rgba(0,0,0,.45);
      text-align:center;
    }
    h1{margin:8px 0 6px;font-size:28px;}
    p{margin:0 0 14px;color:var(--muted);line-height:1.4;}
    img{
      width:170px;height:170px;object-fit:cover;border-radius:16px;
      border:1px solid rgba(255,255,255,.10);
      display:block;margin:12px auto 16px;
    }
    .stage{
      position:relative;height:150px;border-radius:16px;
      background:rgba(255,255,255,.04);
      border:1px dashed rgba(255,255,255,.10);
      overflow:hidden;
      display:flex;align-items:center;justify-content:center;
    }
    button{
      border:0;border-radius:999px;padding:12px 18px;font-weight:800;
      cursor:pointer; transition:transform .15s ease;
      user-select:none; -webkit-tap-highlight-color:transparent;
    }
    button:active{transform:scale(.98);}
    #yes{background:var(--yes);color:#fff;}
    #no{background:var(--no);color:#fff;position:absolute;}
    .hidden{display:none;}
    .big{font-size:34px;}
  </style>
</head>

<body>
  <main class="card">
    <h1 id="question">Bibi, tu veux être mon amoureuse pour la Saint-Valentin ?</h1>
    <p id="sub">Tu peux dire oui… c’est plus simple 😄</p>

    <!-- Remplace l'image par une photo de vous si tu veux -->
    <img id="pic"
      src="https://images.unsplash.com/photo-1518895949257-7621c3c786d7?auto=format&fit=crop&w=500&q=60"
      alt="coeur" />

    <div class="stage" id="stage">
      <button id="yes">OUI</button>
      <button id="no">NON</button>
    </div>

    <div id="result" class="hidden">
      <h1 class="big">YES !!!</h1>
      <p>Bibi, je savais que tu allais dire oui ❤️</p>
      <p>Rendez-vous le 14/02 : (mets ici ton plan / resto / surprise)</p>
    </div>
  </main>

  <script>
    const stage = document.getElementById("stage");
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    const result = document.getElementById("result");
    const sub = document.getElementById("sub");
    const question = document.getElementById("question");

    function placeNoCenter(){
      const r = stage.getBoundingClientRect();
      const bw = noBtn.offsetWidth, bh = noBtn.offsetHeight;
      noBtn.style.left = (r.width/2 - bw/2) + "px";
      noBtn.style.top  = (r.height/2 - bh/2) + "px";
    }

    function moveNo(){
      const r = stage.getBoundingClientRect();
      const bw = noBtn.offsetWidth, bh = noBtn.offsetHeight;
      const pad = 8;

      const maxX = Math.max(pad, r.width - bw - pad);
      const maxY = Math.max(pad, r.height - bh - pad);

      const x = Math.floor(Math.random() * (maxX - pad + 1)) + pad;
      const y = Math.floor(Math.random() * (maxY - pad + 1)) + pad;

      noBtn.style.left = x + "px";
      noBtn.style.top  = y + "px";
    }

    window.addEventListener("load", placeNoCenter);
    window.addEventListener("resize", placeNoCenter);

    // Effet viral: le bouton NON s'échappe au survol / au toucher
    noBtn.addEventListener("mouseenter", moveNo);
    noBtn.addEventListener("touchstart", (e) => { e.preventDefault(); moveNo(); }, { passive:false });

    yesBtn.addEventListener("click", () => {
      stage.classList.add("hidden");
      result.classList.remove("hidden");
      sub.textContent = "";
      question.textContent = "Bibi ❤️";
    });
  </script>
</body>
</html>
