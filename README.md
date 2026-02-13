<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Valentine</title>
<style>
    body {
        margin: 0;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background: linear-gradient(135deg, #ff9ec4, #ff4d94);
        font-family: Arial, sans-serif;
        overflow: hidden;
    }

    .card {
        text-align: center;
        background: white;
        padding: 40px;
        border-radius: 20px;
        box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    }

    h1 {
        color: #ff2e7a;
    }

    .buttons {
        margin-top: 30px;
        position: relative;
        height: 100px;
    }

    button {
        padding: 15px 30px;
        font-size: 18px;
        border: none;
        border-radius: 30px;
        cursor: pointer;
        transition: 0.3s ease;
        position: absolute;
    }

    #yesBtn {
        background-color: hotpink;
        color: white;
        left: 30%;
    }

    #yesBtn:hover {
        transform: scale(1.1);
    }

    #noBtn {
        background-color: gray;
        color: white;
        opacity: 0.3;
        left: 55%;
    }
</style>
</head>
<body>

<div class="card">
    <h1>Dear Efekan.. <br> will you be my valentine? 💌</h1>
    <div class="buttons">
        <button id="yesBtn" onclick="yesClicked()">YEAA 💖</button>
        <button id="noBtn">nah</button>
    </div>
</div>

<script>
    const noBtn = document.getElementById("noBtn");

    noBtn.addEventListener("mouseover", () => {
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 50);

        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    });

    function yesClicked() {
        document.body.innerHTML = 
            <div style="display:flex;justify-content:center;align-items:center;height:100vh;background:#ff4d94;color:white;font-size:40px;font-family:Arial;">
                YAYYY 💖 I love you!!
            </div>
        ;
    }
</script>

</body>
</html>
