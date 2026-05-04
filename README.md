<!DOCTYPE html>

<html lang="ru">
<head>
<meta charset="UTF-8">
<title>Устройство кондиционера</title>

<style>
    body {
        margin: 0;
        font-family: Arial, sans-serif;
        background: #f4f7fb;
        color: #222;
    }

    header {
        background: linear-gradient(135deg, #1e3c72, #2a5298);
        color: white;
        padding: 30px;
        text-align: center;
    }

    nav {
        background: #fff;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        border-bottom: 2px solid #ddd;
    }

    nav a {
        padding: 15px 20px;
        text-decoration: none;
        color: #1e3c72;
        font-weight: bold;
    }

    nav a:hover {
        background: #1e3c72;
        color: white;
    }

    .container {
        max-width: 1100px;
        margin: auto;
        padding: 20px;
    }

    .card {
        background: white;
        margin: 20px 0;
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    h2 {
        color: #1e3c72;
    }

    img {
        width: 100%;
        border-radius: 10px;
        margin-top: 10px;
    }

    .grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 15px;
    }

    .box {
        background: #eaf0ff;
        padding: 15px;
        border-radius: 10px;
    }

    button {
        padding: 10px 15px;
        margin-top: 10px;
        border: none;
        background: #1e3c72;
        color: white;
        border-radius: 8px;
        cursor: pointer;
    }

    button:hover {
        background: #2a5298;
    }

    footer {
        text-align: center;
        padding: 20px;
        background: #1e3c72;
        color: white;
    }

    .modal {
        display: none;
        position: fixed;
        z-index: 1000;
        left: 0;
        top: 0;
        width: 100%;
        height: 200%;
        background: rgba(0,0,0,0.7);
    }

    .modal-content {
        background: white;
        margin: 8% auto;
        padding: 20px;
        width: 100%;
        max-width: 700px;
        border-radius: 12px;
        position: relative;
        animation: fadeIn 0.3s ease-in-out;
    }

    @keyframes fadeIn {
        from {transform: scale(0.8); opacity: 0;}
        to {transform: scale(1); opacity: 1;}
    }

    .close {
        position: absolute;
        right: 15px;
        top: 10px;
        font-size: 24px;
        cursor: pointer;
        color: #333;
    }
</style>

</head>

<body>

<header>
    <h1>Устройство кондиционера</h1>
</header>

<nav>
    <a href="#concept">Понятие</a>
    <a href="#device">Устройство</a>
</nav>

<div class="container">

<section id="concept" class="card">
<h2>Понятие кондиционера</h2>

<p><b>Кондиционер</b> — это устройство для поддержания комфортного микроклимата.</p>

<img src="https://domsplit.ru/upload/iblock/b98/9cft3fz6wbxe7of12vwwxz3fbsxuq84v.jpg">
</section>

<section id="device" class="card">
<h2>Основные узлы кондиционера</h2>

<div class="grid">
<div class="box">
<h3>Компрессор</h3>
<button onclick="openModal('m1')">Открыть схему</button>
</div>

<div class="box">
<h3>Конденсатор</h3>
<button onclick="openModal('m2')">Открыть схему</button>
</div>

<div class="box">
<h3>Испаритель</h3>
<button onclick="openModal('m3')">Открыть схему</button>
</div>
</div>

</section>
</div>

<div id="m1" class="modal">
<div class="modal-content">
<span class="close" onclick="closeModal('m1')">&times;</span>
<h2>Компрессор</h2>
<img src="https://www.stron-parts.ru/files/image/kompressor_avtomobilya.jpg">
</div>
</div>

<div id="m2" class="modal">
<div class="modal-content">
<span class="close" onclick="closeModal('m2')">&times;</span>
<h2>Конденсатор</h2>
<img src="https://avatars.mds.yandex.net/i?id=3e3f15b59a33fb37d78677c266f51f0c_l-8750288-images-thumbs&n=13">
</div>
</div>

<div id="m3" class="modal">
<div class="modal-content">
<span class="close" onclick="closeModal('m3')">&times;</span>
<h2>Испаритель</h2>
<img src="https://avatars.mds.yandex.net/i?id=344952dec221a29b60b6a346bc098229_l-4078174-images-thumbs&n=13">
</div>
</div>

<script>
function openModal(id){
    document.getElementById(id).style.display = "block";
}

function closeModal(id){
    document.getElementById(id).style.display = "none";
}

window.onclick = function(event){
    let modals = document.querySelectorAll(".modal");
    modals.forEach(m => {
        if(event.target == m){
            m.style.display = "none";
        }
    });
}
</script>

</body>
</html>
