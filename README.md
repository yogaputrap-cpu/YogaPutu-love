# YogaPutu-love
hmmm kepo deh
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#6f4936">
  <title>Surat Kecil untuk Putu Sri Anjani ♡</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Dancing+Script:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root { --paper:#fff8eb; --ink:#513b2b; --brown:#8b5e45; --line:#c5a67e; --rose:#a34c58; }
    * { box-sizing:border-box; }
    body {
      margin:0; min-height:100vh; padding:28px 14px 50px;
      color:var(--ink); font-family:"Cormorant Garamond",Georgia,serif;
      background:radial-gradient(ellipse at top,#f9edda 0%,transparent 70%),
                 linear-gradient(135deg,#e7d1b2,#f4e7d1,#d7bd9b);
    }
    .paper {
      position:relative; width:min(100%,760px); margin:auto; padding:clamp(24px,5vw,48px);
      background:var(--paper); border:1px solid var(--line);
      box-shadow:0 18px 50px #63452b35; outline:5px double var(--line); outline-offset:-12px;
      text-align:center; overflow:hidden;
    }
    .ornament { color:#a4774f; font-size:23px; letter-spacing:7px; margin:14px 0; }
    .eyebrow { text-transform:uppercase; letter-spacing:3px; font:12px Arial,sans-serif; }
    h1,h2,.script { font-family:"Dancing Script",cursive; font-weight:600; }
    h1 { font-size:clamp(40px,8vw,66px); color:#8b4e36; margin:17px 0; }
    h2 { font-size:clamp(28px,5vw,38px); color:#8b4e36; margin:8px 0 16px; }
    p { font-size:clamp(18px,3.2vw,21px); line-height:1.75; }
    .intro { max-width:540px; margin:0 auto 22px; }
    .envelope-wrap { margin:24px auto 28px; }
    .envelope {
      position:relative; display:block; margin:0 auto; width:min(100%,310px); height:190px;
      border:0; background:#d9b995; cursor:pointer; box-shadow:0 10px 22px #4c332022;
      overflow:visible; padding:0;
    }
    .env-back { position:absolute; inset:0; background:#d9b995; }
    .env-letter {
      position:absolute; z-index:1; left:9%; right:9%; bottom:12px; height:145px;
      background:#fff8eb; border:1px solid #c7a782; padding:13px 7px;
      display:flex; flex-direction:column; align-items:center; justify-content:center;
      transition:transform .7s ease;
    }
    .env-letter span { font:26px "Dancing Script",cursive; color:#8b4e36; }
    .env-letter small { font:11px Arial,sans-serif; letter-spacing:2px; margin-top:6px; }
    .env-front {
      position:absolute; inset:0; z-index:3; background:#cda780;
      clip-path:polygon(0 0,50% 57%,100% 0,100% 100%,0 100%);
      border-bottom:1px solid #a77d59;
    }
    .env-flap {
      position:absolute; z-index:4; top:0; left:0; width:100%; height:100%;
      background:#b98d68; clip-path:polygon(0 0,100% 0,50% 58%);
      transform-origin:top; transition:transform .65s ease;
    }
    .seal {
      position:absolute; z-index:5; left:50%; top:53%; transform:translate(-50%,-50%);
      display:grid; place-items:center; width:42px; height:42px; border-radius:50%;
      color:#fff0db; background:#8e3f42; border:2px solid #e1bfa0; font-size:22px;
    }
    .envelope.open .env-flap { transform:rotateX(180deg); z-index:0; }
    .envelope.open .env-letter { transform:translateY(-90px); }
    .hint { font-size:15px; margin-top:12px; }
    .photo-grid { display:grid; grid-template-columns:repeat(3,minmax(0,1fr)); gap:18px; margin:28px 0; align-items:start; }
    .polaroid { background:#fffdf6; padding:9px 9px 13px; border:1px solid #d2b795; box-shadow:0 6px 14px #4c33201a; }
    .polaroid:nth-child(1) { transform:rotate(-2deg); }
    .polaroid:nth-child(2) { transform:rotate(1.5deg); margin-top:14px; }
    .polaroid:nth-child(3) { transform:rotate(-1deg); }
    .polaroid img { display:block; width:100%; height:210px; object-fit:cover; background:#eadbc5; }
    .caption { font:19px "Dancing Script",cursive; margin-top:10px; }
    .tools { display:flex; flex-wrap:wrap; justify-content:center; gap:10px; margin:18px 0; }
    button,.upload-label {
      font-family:inherit; font-size:17px; display:inline-block; border:1px solid #8d6045;
      background:var(--brown); color:#fff8eb; padding:12px 18px; border-radius:3px;
      cursor:pointer; transition:.2s;
    }
    button:hover,.upload-label:hover { background:#68442f; transform:translateY(-2px); }
    button.envelope { padding:0; border:0; border-radius:0; background:transparent; color:inherit; box-shadow:0 10px 22px #4c332022; transform:none; }
    button.envelope:hover { background:transparent; transform:none; }
    .secondary { background:#e9d8be; color:#513b2b; }
    .secondary:hover { background:#d8c09f; }
    .letter {
      display:none; text-align:left; margin:24px 0; padding:22px;
      border-top:1px dashed #b28d69; border-bottom:1px dashed #b28d69;
      background:#f9eedb; animation:appear .65s ease;
    }
    .letter.show { display:block; }
    .signature { text-align:right; font:clamp(25px,5vw,32px) "Dancing Script",cursive; color:#8b4e36; }
    .response { min-height:35px; font:25px "Dancing Script",cursive; color:#8b4e36; }
    .music-box { background:#f4e6d1; border:1px dashed #c5a67e; padding:18px; margin:18px auto; max-width:510px; }
    .music-status { font-size:15px; margin:8px 0 0; }
    .footer { border-top:1px solid #d8c09f; padding-top:16px; margin-top:30px; font-size:15px; }
    .heart { display:inline-block; color:var(--rose); animation:beat 1.4s infinite; }
    .floating-heart { position:fixed; bottom:-30px; z-index:0; pointer-events:none; animation:float-up 6s linear forwards; }
    @keyframes appear { from { opacity:0; transform:translateY(12px); } to { opacity:1; transform:translateY(0); } }
    @keyframes beat { 50% { transform:scale(1.2); } }
    @keyframes float-up { to { transform:translateY(-110vh) rotate(25deg); opacity:0; } }
    @media(max-width:600px) {
      body { padding:20px 12px 35px; }
      .photo-grid { grid-template-columns:1fr; max-width:390px; margin:24px auto; gap:16px; }
      .polaroid:nth-child(2) { margin-top:0; }
      .polaroid img { height:auto; max-height:420px; object-fit:contain; }
      .tools button,.tools .upload-label { width:100%; }
      .letter { padding:16px; }
    }
  </style>
</head>
<body>
  <main class="paper">
    <div class="ornament">✦ ❧ ✦</div>
    <div class="eyebrow">A little letter from my heart</div>
    <h1>Untuk Putu Sri Anjani</h1>
    <div class="ornament">──────── ♡ ────────</div>

    <p class="intro">
      Ada sesuatu yang ingin aku sampaikan. Mungkin sederhana,
      tapi aku berharap kamu bisa merasakan ketulusan di dalamnya.
    </p>

    <section class="envelope-wrap" aria-label="Amplop surat">
      <button class="envelope" id="envelope" aria-label="Buka amplop surat" onclick="openEnvelope()">
        <span class="env-back"></span>
        <span class="env-letter"><span>Untuk Putu ♡</span><small>PLEASE OPEN</small></span>
        <span class="env-front"></span>
        <span class="env-flap"></span>
        <span class="seal">♥</span>
      </button>
      <p class="hint">Klik amplopnya untuk membuka surat kecil ini.</p>
    </section>

    <div class="ornament">❦</div>
    <h2>Potongan Kenangan Kita</h2>
    <p>Beberapa momen kecil yang ingin aku simpan dengan baik.</p>

    <section class="photo-grid" aria-label="Galeri foto kenangan">
      <div class="polaroid">
        <img src="assets/foto-kenangan-1.png" alt="Kenangan berdua di taman malam" loading="lazy">
        <div class="caption">A night to remember ♡</div>
      </div>
      <div class="polaroid">
        <img src="assets/foto-kenangan-2.png" alt="Kenangan berdua di tepi pantai" loading="lazy">
        <div class="caption">Just you and me</div>
      </div>
      <div class="polaroid">
        <img src="assets/foto-kenangan-3.png" alt="Foto selfie berdua" loading="lazy">
        <div class="caption">Our silly little moments</div>
      </div>
    </section>

    <p>
      Setiap orang pasti pernah melakukan kesalahan, termasuk aku.
      Tapi aku nggak ingin menjadikan itu alasan untuk mengabaikan perasaanmu.
    </p>
    <p>
      Aku ingin belajar dari kesalahanku, lebih mendengarkan,
      dan menunjukkan perubahan lewat sikap, bukan cuma kata-kata.
    </p>

    <div class="tools">
      <button onclick="toggleLetter()" id="letterButton">💌 Buka Suratku</button>
      <label for="photoInput" class="upload-label">📷 Ganti Foto</label>
      <input id="photoInput" type="file" accept="image/*" hidden>
    </div>
    <p style="font-size:14px;margin-top:-8px;">Ganti Foto mengubah foto pertama untuk pratinjau saja. Untuk mengganti foto permanen, ikuti tutorial.</p>

    <section class="letter" id="letter">
      <h2>Dear Putu...</h2>
      <p>
        Aku mau minta maaf ya, Putu Sri Anjani. Maaf kalau perkataan
        atau sikapku pernah bikin kamu sedih, kecewa, atau merasa nggak dihargai.
      </p>
      <p>
        Aku mungkin belum selalu bisa memahami perasaanmu dengan baik.
        Tapi aku ingin belajar, memperbaiki diri, dan lebih menghargai
        apa yang kamu rasakan.
      </p>
      <p>
        Aku nggak berharap semuanya langsung baik-baik saja. Aku cuma
        ingin kamu tahu kalau permintaan maaf ini tulus dari hati.
      </p>
      <p>
        Terima kasih sudah menjadi bagian dari cerita hidupku.
        Aku harap kita bisa bicara baik-baik, dan aku akan menghargai
        perasaan serta waktumu.
      </p>
      <p>Maaf ya, untuk hal-hal yang pernah membuat hatimu terluka.</p>
      <div class="signature">Maafin aku ya, Putu. ♡</div>
    </section>

    <div class="tools">
      <button class="secondary" onclick="showFinalMessage()">🤎 Pesan Terakhir</button>
    </div>
    <div id="response" class="response" aria-live="polite"></div>

    <div class="ornament">♫</div>
    <h2>Our Little Song</h2>
    <p>Putar musik sambil membaca surat ini.</p>
    <div class="music-box">
      <audio id="music" controls loop preload="metadata">
        <source src="assets/musik.mp3" type="audio/mpeg">
        Browser kamu tidak mendukung pemutar audio.
      </audio>
      <div class="tools">
        <label for="musicInput" class="upload-label">🎵 Pilih Musik dari Perangkat</label>
        <input id="musicInput" type="file" accept="audio/*" hidden>
      </div>
      <p class="music-status" id="musicStatus">Jika musik belum ada, pilih file lagu dari perangkatmu.</p>
    </div>

    <div class="footer">
      Dibuat dengan tulus dan sepenuh hati <span class="heart">♥</span><br>
      Untuk Putu Sri Anjani<br><br>
      <em>Some feelings are better written from the heart.</em>
    </div>
  </main>

  <script>
    // Membuka animasi amplop.
    function openEnvelope() {
      const envelope = document.getElementById("envelope");
      envelope.classList.toggle("open");
      if (envelope.classList.contains("open")) {
        const music = document.getElementById("music");
        music.play().then(() => {
          document.getElementById("musicStatus").textContent = "Musik sedang diputar.";
        }).catch(() => {
          document.getElementById("musicStatus").textContent = "Tekan Play pada pemutar musik jika lagu belum terdengar.";
        });
        document.getElementById("letter").classList.add("show");
        document.getElementById("letterButton").textContent = "✉️ Tutup Surat";
        setTimeout(() => document.getElementById("letter").scrollIntoView({
          behavior: "smooth", block: "nearest"
        }), 250);
      }
    }

    // Membuka atau menutup surat.
    function toggleLetter() {
      const letter = document.getElementById("letter");
      const button = document.getElementById("letterButton");
      const isOpen = letter.classList.toggle("show");
      button.textContent = isOpen ? "✉️ Tutup Surat" : "💌 Buka Suratku";
    }

    // Menampilkan pesan penutup.
    function showFinalMessage() {
      document.getElementById("response").textContent =
        "Aku nggak minta kamu melupakan semuanya. Aku cuma berharap masih ada kesempatan untuk memperbaiki keadaan. Maafin aku ya, Putu. 🤎";
    }

    // Mengganti foto pertama sementara di browser.
    let temporaryPhotoURL = null;
    document.getElementById("photoInput").addEventListener("change", function(event) {
      const file = event.target.files[0];
      if (!file) return;
      if (!file.type.startsWith("image/")) {
        alert("Pilih file gambar seperti JPG, PNG, atau WEBP.");
        return;
      }
      if (temporaryPhotoURL) URL.revokeObjectURL(temporaryPhotoURL);
      temporaryPhotoURL = URL.createObjectURL(file);
      document.querySelector(".photo-grid img").src = temporaryPhotoURL;
    });

    // Memilih musik dari perangkat dan memutarnya.
    let temporaryMusicURL = null;
    document.getElementById("musicInput").addEventListener("change", async function(event) {
      const file = event.target.files[0];
      if (!file) return;
      if (!file.type.startsWith("audio/")) {
        alert("Pilih file musik/audio yang sesuai.");
        return;
      }
      const music = document.getElementById("music");
      if (temporaryMusicURL) URL.revokeObjectURL(temporaryMusicURL);
      temporaryMusicURL = URL.createObjectURL(file);
      music.src = temporaryMusicURL;
      document.getElementById("musicStatus").textContent =
        "Musik pilihanmu: " + file.name;
      try {
        await music.play();
      } catch (error) {
        document.getElementById("musicStatus").textContent =
          "Musik siap diputar. Tekan tombol Play pada pemutar audio.";
      }
    });

    // Animasi hati kecil yang melayang.
    function createHeart() {
      const heart = document.createElement("span");
      heart.className = "floating-heart";
      heart.textContent = Math.random() > 0.5 ? "♡" : "♥";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = (14 + Math.random() * 18) + "px";
      heart.style.color = Math.random() > 0.5 ? "#a34c58" : "#a4774f";
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 6000);
    }
    setInterval(createHeart, 850);
  </script>
</body>
</html>
