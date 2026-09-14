# Takasla.com
Create 
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Takasla</title>

<style>
*{
    box-sizing:border-box;
}

body{
    margin:0;
    font-family:Arial,sans-serif;
    background:#f4f6f9;
    color:#17202a;
}

header{
    background:white;
    padding:15px 20px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    border-bottom:1px solid #ddd;
    position:sticky;
    top:0;
    z-index:10;
}

.logo{
    font-size:25px;
    font-weight:bold;
    color:#1264d8;
}

button{
    border:0;
    border-radius:10px;
    padding:12px 18px;
    font-weight:bold;
    cursor:pointer;
}

.primary{
    background:#1264d8;
    color:white;
}

.secondary{
    background:#e9edf3;
    color:#17202a;
}

.container{
    max-width:950px;
    margin:25px auto;
    padding:0 15px;
}

.page{
    display:none;
}

.page.active{
    display:block;
}

.hero{
    background:#1264d8;
    color:white;
    padding:30px;
    border-radius:18px;
    margin-bottom:20px;
}

.hero h1{
    margin-top:0;
    font-size:30px;
}

.search{
    width:100%;
    padding:15px;
    border:1px solid #ddd;
    border-radius:10px;
    margin-bottom:20px;
    font-size:16px;
}

.products{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:18px;
}

.card{
    background:white;
    padding:18px;
    border-radius:16px;
    box-shadow:0 3px 15px rgba(0,0,0,.08);
}

.product-image{
    height:190px;
    background:#eef2f7;
    border-radius:12px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:75px;
    margin-bottom:15px;
}

.muted{
    color:#6d7785;
    font-size:14px;
}

.box{
    background:white;
    padding:25px;
    border-radius:16px;
    box-shadow:0 3px 15px rgba(0,0,0,.08);
}

input,
textarea,
select{
    width:100%;
    padding:13px;
    border:1px solid #d5dbe3;
    border-radius:9px;
    margin:7px 0 15px;
    font-size:15px;
}

textarea{
    resize:vertical;
}

.success{
    background:#e8f8ee;
    padding:18px;
    border-radius:10px;
    margin-bottom:15px;
}

.warning{
    background:#fff4d6;
    padding:18px;
    border-radius:10px;
    margin-top:20px;
}

.offer{
    border:1px solid #ddd;
    border-radius:12px;
    padding:18px;
    margin-bottom:15px;
}

.big-icon{
    font-size:60px;
}

footer{
    text-align:center;
    color:#777;
    padding:40px 10px;
}

@media(max-width:650px){

    .products{
        grid-template-columns:1fr;
    }

    .hero h1{
        font-size:25px;
    }

}
</style>
</head>

<body>

<header>

<div class="logo">
Takasla
</div>

<button class="primary" onclick="showPage('add')">
+ Takasa Koy
</button>

</header>


<div class="container">


<!-- ANA SAYFA -->

<div id="home" class="page active">

<div class="hero">

<h1>
Elindekini takasa koy.
</h1>

<p>
İstediğin ürünü bul. Teklif gönder.
Anlaşınca numaranı paylaş.
</p>

</div>


<input
class="search"
placeholder="Ürün ara..."
>


<div class="products">


<div class="card">

<div class="product-image">
📱
</div>

<h3>
iPhone 13 128 GB
</h3>

<p class="muted">
İstanbul · 5 dakika önce
</p>

<button
class="primary"
onclick="showPage('product')"
>
Takas Teklifi Gönder
</button>

</div>


<div class="card">

<div class="product-image">
🎮
</div>

<h3>
PlayStation 5
</h3>

<p class="muted">
Ankara · 18 dakika önce
</p>

<button
class="primary"
onclick="showPage('product')"
>
Takas Teklifi Gönder
</button>

</div>


<div class="card">

<div class="product-image">
🚲
</div>

<h3>
Elektrikli Bisiklet
</h3>

<p class="muted">
Bursa · 32 dakika önce
</p>

<button
class="primary"
onclick="showPage('product')"
>
Takas Teklifi Gönder
</button>

</div>


<div class="card">

<div class="product-image">
💻
</div>

<h3>
MacBook Air
</h3>

<p class="muted">
İstanbul · 1 saat önce
</p>

<button
class="primary"
onclick="showPage('product')"
>
Takas Teklifi Gönder
</button>

</div>

</div>

</div>



<!-- ÜRÜN DETAY -->

<div id="product" class="page">

<div class="box">

<button
class="secondary"
onclick="showPage('home')"
>
← Geri
</button>

<h2>
iPhone 13 128 GB
</h2>

<div class="product-image">
📱
</div>

<p>
<b>Konum:</b> İstanbul
</p>

<p>
<b>İlan sahibi:</b> Mehmet
</p>

<hr>

<h3>
Karşılığında ne teklif ediyorsun?
</h3>

<select>

<option>
PlayStation 5
</option>

<option>
Samsung Galaxy S24
</option>

<option>
Elektrikli Bisiklet
</option>

</select>


<textarea
rows="4"
placeholder="Teklif mesajın..."
></textarea>


<button
class="primary"
onclick="showPage('sent')"
>
Teklifi Gönder
</button>

</div>

</div>



<!-- TEKLİF GÖNDERİLDİ -->

<div id="sent" class="page">

<div class="box">

<div class="success">

<h2>
✅ Teklif gönderildi
</h2>

<p>
Ürün sahibine takas teklifin gönderildi.
</p>

<p>
Teklif kabul edilirse telefon numarası
paylaşımı için ayrıca onay alınacaktır.
</p>

</div>

<button
class="primary"
onclick="showPage('offer')"
>
Karşı tarafın ekranını gör
</button>

</div>

</div>



<!-- GELEN TEKLİF -->

<div id="offer" class="page">

<div class="box">

<h2>
🔔 Yeni Takas Teklifi
</h2>

<div class="offer">

<p>
<b>Mehmet</b>
senin ilanındaki
<b>iPhone 13</b> için
<b>PlayStation 5</b> teklif ediyor.
</p>

</div>


<button
class="primary"
onclick="showPage('phone')"
>
Teklifi Kabul Et
</button>

<button
class="secondary"
onclick="showPage('home')"
>
Reddet
</button>

</div>

</div>



<!-- TELEFON ONAYI -->

<div id="phone" class="page">

<div class="box">

<h2>
📞 Telefon numarası paylaşımı
</h2>

<p>
Takas teklifini kabul ettin.
</p>

<p>
Şimdi iki tarafın telefon numaralarını
karşılıklı paylaşması gerekiyor.
</p>

<label>

<input
type="checkbox"
id="phoneAgree"
style="width:auto"
>

Telefon numaramın karşı tarafa
paylaşılmasını onaylıyorum.

</label>

<br><br>

<button
class="primary"
onclick="sharePhone()"
>
Numaraları Paylaş
</button>

</div>

</div>



<!-- NUMARALAR PAYLAŞILDI -->

<div id="shared" class="page">

<div class="box">

<div class="success">

<h2>
✅ Numaralar paylaşıldı
</h2>

<p>
Telefon numaraları karşılıklı olarak
paylaşıldı.
</p>

</div>

<h3>
Artık takas tarafların arasında.
</h3>

<p>
Görüşebilir, buluşabilir, ürünleri
kontrol edebilir ve takası
gerçekleştirebilirsiniz.
</p>

<div class="warning">

⏰ 24 saat sonra iki tarafa:

<b>
"Takas gerçekleşti mi?"
</b>

bildirimi gönderilecek.

</div>

<br>

<button
class="primary"
onclick="showPage('confirm')"
>
24 Saat Sonraki Ekranı Gör
</button>

</div>

</div>



<!-- TAKAS ONAYI -->

<div id="confirm" class="page">

<div class="box">

<h2>
🔔 Takas gerçekleşti mi?
</h2>

<p>
iPhone 13 ↔ PlayStation 5
</p>

<br>

<button
class="primary"
onclick="showPage('done')"
>
Evet, takas gerçekleşti
</button>

<br><br>

<button
class="secondary"
onclick="showPage('failed')"
>
Hayır, gerçekleşmedi
</button>


<div class="warning">

3 gün içerisinde cevap verilmezse
ilan aktif yayınlardan kaldırılır.

</div>

</div>

</div>



<!-- TAKAS TAMAMLANDI -->

<div id="done" class="page">

<div class="box">

<div class="success">

<h2>
🎉 Takas tamamlandı
</h2>

<p>
Takas başarıyla tamamlandı.
</p>

<p>
İlan aktif yayınlardan kaldırıldı.
</p>

</div>

</div>

</div>



<!-- TAKAS OLMADI -->

<div id="failed" class="page">

<div class="box">

<div class="warning">

<h2>
Takas gerçekleşmedi
</h2>

<p>
Bu takas gerçekleşmedi olarak
işaretlendi.
</p>

</div>

<br>

<button
class="primary"
onclick="showPage('home')"
>
Ana Sayfaya Dön
</button>

</div>

</div>



<!-- İLAN EKLE -->

<div id="add" class="page">

<div class="box">

<h2>
Ürünü Takasa Koy
</h2>

<label>
Ürün adı
</label>

<input
placeholder="Örneğin: iPhone 13"
>


<label>
Şehir
</label>

<input
placeholder="İstanbul"
>


<label>
Ürün açıklaması
</label>

<textarea
rows="5"
placeholder="Ürünün durumunu açıklayın..."
></textarea>


<label>
Fotoğraf
</label>

<input
type="file"
accept="image/*"
>


<div class="warning">

İlan yayınlama hizmet bedeli:

<b>5 TL</b>

</div>

<br>

<button
class="primary"
onclick="publish()"
>
5 TL ile Yayınla
</button>

</div>

</div>


</div>


<footer>

Takasla © 2026

</footer>



<script>

function showPage(page){

    document
    .querySelectorAll(".page")
    .forEach(function(p){

        p.classList.remove("active");

    });

    document
    .getElementById(page)
    .classList.add("active");

    window.scrollTo(0,0);

}


function sharePhone(){

    var check =
    document.getElementById("phoneAgree");

    if(!check.checked){

        alert(
        "Telefon numaranın paylaşılması için onay vermelisin."
        );

        return;

    }

    showPage("shared");

}


function publish(){

    alert(
    "Demo: 5 TL ödeme ekranına geçilecek."
    );

}

</script>

</body>
</html>
