
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
            overflow: hidden; /* Prevent scrolling */
        }

        /* Fullscreen Background Circle Rotation */
        .background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        .background img {
            position: absolute;
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            animation: move 10s linear infinite;
        }

        @keyframes move {
            0% { transform: translate(0%, 0%); }
            25% { transform: translate(90vw, 0%); }
            50% { transform: translate(90vw, 90vh); }
            75% { transform: translate(0%, 90vh); }
            100% { transform: translate(0%, 0%); }
        }

        .background img:nth-child(odd) {
            animation-direction: reverse;
        }

        .overlay-text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #FFFFFF;
            text-shadow: 2px 2px 5px #000000;
            font-size: 3em;
            font-weight: bold;
            z-index: 1;
        }

        button {
            background-color: #FFB6C1;
            border: none;
            padding: 10px 20px;
            font-size: 18px;
            color: white;
            cursor: pointer;
            border-radius: 20px;
            font-family: 'Times New Roman', serif;
            margin-top: 20px;
        }

        button:hover {
            background-color: #FF69B4;
        }

        .hidden {
            display: none;
        }

        .spotify-container {
            display: none; /* Hide the Spotify iframe */
        }

        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 2.5rem;
            margin-top: 3rem;
        }

        .container a {
            display: block;
            background-color: #FFB6C1;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 20px;
            font-size: 18px;
            font-family: 'Times New Roman', serif;
        }

        .container a:hover {
            background-color: #FF69B4;
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
        <iframe src="https://open.spotify.com/embed/playlist/0kos2AxTIUBaK7CNsEY2xb?utm_source=generator&theme=0&autoplay=1" width="0" height="0" frameBorder="0" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>
    </div>

    <script>
        function showSurprise() {
            document.getElementById("surprise").classList.remove("hidden");
        }

        // Ensure autoplay works by dynamically creating the iframe
        window.onload = function() {
            const iframe = document.createElement('iframe');
            iframe.src = "https://open.spotify.com/embed/playlist/0kos2AxTIUBaK7CNsEY2xb?utm_source=generator&theme=0&autoplay=1";
            iframe.width = "0";
            iframe.height = "0";
            iframe.style.border = "none";
            document.body.appendChild(iframe);
        };
    </script>
</body>
</html>
