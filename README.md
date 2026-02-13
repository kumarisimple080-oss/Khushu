<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Khushu ✧༺♥༻✧</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #ffebee;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
            text-align: center;
        }

        #container {
            z-index: 10;
        }

        h1 {
            color: #d32f2f;
            font-size: 3rem;
            margin-bottom: 30px;
            text-shadow: 2px 2px #ffcdd2;
        }

        .buttons {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
        }

        button {
            padding: 15px 40px;
            font-size: 1.5rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: transform 0.2s;
            font-weight: bold;
        }

        #yesBtn {
            background-color: #ff4081;
            color: white;
            box-shadow: 0 4px 15px rgba(255, 64, 129, 0.4);
        }

        #yesBtn:hover {
            transform: scale(1.1);
            background-color: #f50057;
        }

        #noBtn {
            background-color: #9e9e9e;
            color: white;
            position: absolute;
        }

        canvas {
            position: fixed;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 999;
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>

    <div id="container">
        <h1>Will you be my Valentine? <br> [Khushu✧༺♥༻✧]</h1>
        <div class="buttons">
            <button id="yesBtn" onclick="celebrate()">Yes!</button>
            <button id="noBtn" onmouseover="moveButton()">No</button>
        </div>
    </div>

    <canvas id="heartCanvas"></canvas>

    <script>
        const noBtn = document.getElementById('noBtn');
        const canvas = document.getElementById('heartCanvas');
        const ctx = canvas.getContext('2d');

        // Move the "No" button randomly
        function moveButton() {
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
