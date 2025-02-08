
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Surprise ❤️</title>
    <link rel="stylesheet" href="style.css">
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Times New Roman', serif;
            text-align: center;
            color: #8B0000;
        }

        /* Fullscreen Background Circle Rotation */
        .background {
            position: fixed;
            top: 50%;
            left: 50%;
            width: 100vw;
            height: 100vh;
            transform: translate(-50%, -50%);
            z-index: -1;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .background img {
            position: absolute;
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            animation: rotate 10s linear infinite, spin 1s linear infinite;
        }

        /* Rotation of the whole group */
        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Individual spinning effect */
        @keyframes spin {
            0% { transform: translateX(-50%) translateY(-50%) rotate(0deg); }
            100% { transform: translateX(-50%) translateY(-50%) rotate(360deg); }
        }

        .background img:nth-child(1) {
            animation-delay: 0s;
        }

        .background img:nth-child(2) {
            animation-delay: 1s;
        }

        .background img:nth-child(3) {
            animation-delay: 2s;
        }

        .background img:nth-child(4) {
            animation-delay: 3s;
        }

        .background img:nth-child(5) {
            animation-delay: 4s;
        }

        .background img:nth-child(6) {
            animation-delay: 5s;
        }

        .background img:nth-child(7) {
            animation-delay: 6s;
        }

        .background img:nth-child(8) {
            animation-delay: 7s;
        }

        .background img:nth-child(9) {
            animation-delay: 8s;
        }

        .overlay-text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #FFFFFF;
            text-shadow: 2px 2px 5px #000000;
            font-size: 2em;
            font-weight: bold;
            z-index: 1;
        }

        button {
            background-color: #FFB6C1;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            color: white;
            cursor: pointer;
            border-radius: 20px;
            font-family: 'Times New Roman', serif;
        }
        button:hover {
            background-color: #FF69B4;
        }

        .hidden {
            display: none;
        }

        .spotify-container {
            position: fixed;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 2;
        }

        .spotify-container iframe {
            margin: 0 5px;
        }
    </style>
</head>
<body>
    <!-- Background Section -->
    <div class="background">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_1" alt="Background 1">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_2" alt="Background 2">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_3" alt="Background 3">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_4" alt="Background 4">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_5" alt="Background 5">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_6" alt="Background 6">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_7" alt="Background 7">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_8" alt="Background 8">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_9" alt="Background 9">
    </div>

    <!-- Overlay Text -->
    <div class="overlay-text">
        For the love of my life who I adore so much
    </div>

    <!-- Main Content -->
    <div class="container">
        <h1>Happy Valentine's Day, My Love! 💖</h1>
        <p>I've made something special just for you! 💕</p>
        <button onclick="showSurprise()">Click Here for a Surprise!</button>
        <div id="surprise" class="hidden">
            <p>You are the most amazing person in my life! I love you! 😘</p>
            <a href="quiz.html">Take a Fun Love Quiz 💘</a>
            <a href="story.html">Read Our Love Story 📖</a>
            <a href="letters.html">A Special Letter for You 💌</a>
        </div>
    </div>

    <!-- Spotify Embeds -->
    <div class="spotify-container">
        <iframe src="https://open.spotify.com/embed/playlist/0kos2AxTIUBaK7CNsEY2xb?utm_source=generator&theme=0" width="300" height="380" frameBorder="0" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" allow="autoplay"></iframe>
    </div>

    <script>
        function showSurprise() {
            document.getElementById("surprise").classList.remove("hidden");
        }
    </script>
</body>
</html>
