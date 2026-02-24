<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AtillaOyuncu</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    height:100vh;
    overflow:hidden;
    font-family:"Segoe UI", Arial, sans-serif;
    color:white;
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
}

/* ================= DUYURU ================= */
.announcement{
    position:absolute;
    top:0;
    width:100%;
    height:45px;
    background:linear-gradient(90deg, #06141d, #0b2a3a);
    overflow:hidden;
    z-index:30;
    display:flex;
    align-items:center;
}

.announcement .label{
    display:flex;
    align-items:center;
    gap:8px;
    padding:0 20px;
    font-weight:600;
    color:#4da3ff;
    white-space:nowrap;
}

.announcement .text{
    position:absolute;
    left:100%;
    white-space:nowrap;
    color:#e6f6ff;
    animation:scrollText 18s linear infinite;
}

@keyframes scrollText{
    from{ transform:translateX(0); }
    to{ transform:translateX(-120%); }
}

/* ================= YAĞMUR ================= */
.rain{
    position:absolute;
    width:100%;
    height:100%;
    pointer-events:none;
}

.drop{
    position:absolute;
    bottom:100%;
    width:2px;
    height:80px;
    background:linear-gradient(to bottom, rgba(255,255,255,0), rgba(0,234,255,0.8));
    animation:fall linear infinite;
}

@keyframes fall{
    to{ transform:translateY(110vh); }
}

/* ================= HERO ================= */
.hero{
    position:relative;
    z-index:10;
    height:100%;
    padding-top:45px;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
}

/* TAG */
.tag{
    background:rgba(0,0,0,0.45);
    padding:8px 18px;
    border-radius:30px;
    font-size:14px;
    margin-bottom:20px;
    box-shadow:0 0 15px rgba(0,234,255,0.4);
}

/* BAŞLIK */
.hero h1{
    font-size:56px;
    font-weight:800;
    line-height:1.2;
    text-shadow:0 0 20px rgba(0,0,0,0.7);
}

/* AÇIKLAMA */
.hero p{
    margin-top:15px;
    font-size:18px;
    color:#d0eaff;
    max-width:650px;
}

/* ================= İSTATİSTİK ================= */
.stats{
    display:flex;
    gap:50px;
    margin-top:40px;
    flex-wrap:wrap;
    justify-content:center;
}

.stat h2{
    font-size:36px;
    color:#00eaff;
}

.stat span{
    font-size:14px;
    color:#aaa;
}

/* ================= BUTONLAR ================= */
.buttons{
    margin-top:40px;
    display:flex;
    gap:20px;
    flex-wrap:wrap;
}

.btn{
    padding:14px 28px;
    border-radius:14px;
    background:linear-gradient(135deg, #1e90ff, #00eaff);
    color:#000;
    font-weight:600;
    text-decoration:none;
    box-shadow:0 0 25px rgba(0,234,255,0.5);
    transition:0.3s;
}

.btn:hover{
    transform:translateY(-3px);
    box-shadow:0 0 35px rgba(0,234,255,0.8);
}

/* ================= FOOTER ================= */
.footer{
    position:absolute;
    bottom:25px;
    left:50%;
    transform:translateX(-50%);
    padding:12px 30px;
    border-radius:14px;
    background:rgba(0,0,0,0.45);
    backdrop-filter:blur(6px);
    box-shadow:0 0 25px rgba(0,234,255,0.35);
    font-size:18px;
    z-index:10;
}

.footer span{ color:#aaa; }
.footer strong{
    color:#00eaff;
    text-shadow:0 0 12px rgba(0,234,255,0.9);
    letter-spacing:1px;
}
</style>
</head>

<body>

<!-- DUYURU -->
<div class="announcement">
    <div class="label">📢 DUYURU</div>
    <div class="text">
        Tüm Kredi Yüklemelerine %50 Bonus Kredi Aktif! 
        Hemen Kredini Yükle, VIP Üye Ol!
    </div>
</div>

<!-- YAĞMUR -->
<div class="rain">
<script>
for(let i=0;i<45;i++){
    document.write(
        `<div class="drop" style="
            left:${Math.random()*100}%;
            animation-duration:${0.6+Math.random()}s;
            animation-delay:${Math.random()*2}s;
        "></div>`
    );
}
</script>
</div>

<!-- HERO -->
<div class="hero">
    <div class="tag">AtillaOyuncu</div>

    <h1>Hayalini Kur,<br> İnşa Et, Yönet!</h1>

    <p>
        Türkiye’nin en güçlü Minecraft sunucularından birine katıl,
        arkadaşlarınla birlikte eğlencenin zirvesine çık.
    </p>

    <div class="stats">
        <div class="stat">
            <h2>419,281</h2>
            <span>Aktif Oyuncu</span>
        </div>
        <div class="stat">
            <h2>14,713,970</h2>
            <span>Toplam Oyuncu</span>
        </div>
        <div class="stat">
            <h2>7/24</h2>
            <span>Çevrimiçi Destek</span>
        </div>
    </div>

    <div class="buttons">
        <a href="https://discord.gg/AmtmpXWv" class="btn" target="_blank">Discord</a>
        <a href="#" class="btn">Oyna</a>
        <a href="#" class="btn">İndir</a>
    </div>
</div>

<!-- ALT ADRES -->
<div class="footer">
    <span>Adres:</span>
    <strong>mc.atillaoyuncu.tr</strong>
</div>

</body>
</html>
