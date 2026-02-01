<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be my Valentine❤️</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body{
            font-family: Arial, Helvetica, sans-serif;
            background: linear-gradient(135deg,#0f0809,#280108);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            margin:0;
            color: white;
            text-align: center;

        }
        .card {
            background: rgba(255, 255, 255, 0.2);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
            backdrop-filter: blur(8.5px);
            -webkit-backdrop-filter: blur(8.5px);
            border: 1px solid rgba(255, 255, 255, 0.18);
        
        }
        h1{
            font-size: 26px;
            margin-bottom: 10px;
        }
        p{
            font-size: 18px;
            margin-bottom: 25px;

        }
        button{
            text-align: center;
            background-color: #ff4d6d;
            border: none;
            padding: 5px 30px;
            border-radius: 20px;
            color: white;
            font-size: 16px;
            cursor: pointer;
            transition: left 0.3s ease, top 0.3s ease;

            margin: 0 10px;
        }
        #yes{
            background: #2ecc71;
            color: white;
        }
        #no{
            background: #e74c3c;
            color: white;
            position: absolute
        }
    </style>
</head>
<body>
    <div class="card">
        <h1>Hey Love❤️!!</h1>
        <p>From my heart to this screen,,,,<br>
            <br>
           Will you be my Valentine? ❤️
        </p>
        <button id="yes" onclick="sayYes()">Yes❤️</button>
        
        <button id="no" onmouseover="moveNo()">Noo</button>
    </div>
    <script>

function sayYes() {
    document.body.innerHTML =
        '<div class="card"><h1>Yay!❤️</h1><p>Best decision ever 😘<br>Let play song for us!!</p></div>';

    setTimeout(() => {
        window.open("https://youtu.be/vDmVblfzek4?si=wh2Z8R3M83ir50B7", "_blank");
    }, 1500);
}
function moveNo() {
    const noButton = document.getElementById("no");
    const card = document.querySelector(".card");

    const cardRect = card.getBoundingClientRect();
    const btnRect = noButton.getBoundingClientRect();

    const maxX = card.clientWidth - btnRect.width;
    const maxY = card.clientHeight - btnRect.height;

    const x = Math.random() * maxX;
    const y = Math.random() * maxY;

    noButton.style.left = x + "px";
    noButton.style.top = y + "px";
}
</script>

</body>
</html>
