# Index.html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Do You Love Me?</title>

    <style>
        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ffb6c1, #ffe4e1);
            font-family: Arial, sans-serif;
            text-align: center;
        }

        .container {
            background: white;
            padding: 40px 25px;
            border-radius: 25px;
            width: 80%;
            max-width: 400px;
            box-shadow: 0 5px 20px #d88a9a;
        }

        h1 {
            color: #e75480;
        }

        button {
            padding: 12px 30px;
            margin: 15px 10px;
            border: none;
            border-radius: 25px;
            font-size: 18px;
            cursor: pointer;
        }

        #yes {
            background: #ff4d79;
            color: white;
        }

        #no {
            background: #888;
            color: white;
            position: relative;
        }

        #no:hover {
            transform: translate(40px, -30px);
        }

        .hidden {
            display: none;
        }
    </style>
</head>

<body>

    <div class="container" id="firstPage">
        <h1>Do you love me? ❤️</h1>

        <button id="yes" onclick="showLove()">
            YES 💗
        </button>

        <button id="no" onclick="moveNo()">
            NO 😜
        </button>
    </div>

    <div class="container hidden" id="secondPage">
        <h1>Congratulations! ❤️</h1>
        <h2>I love you too! 💕</h2>
        <p>You just made my day! 🥰</p>
    </div>

    <script>
        function showLove() {
            document.getElementById("firstPage").style.display = "none";
            document.getElementById("secondPage").style.display = "block";
        }

        function moveNo() {
            const noButton = document.getElementById("no");

            noButton.style.position = "fixed";
            noButton.style.left = Math.random() * 70 + 10 + "%";
            noButton.style.top = Math.random() * 70 + 10 + "%";
        }
    </script>

</body>
</html>

