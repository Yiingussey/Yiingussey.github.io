
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Surprise ❤️</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Times New Roman', serif;
            text-align: center;
            color: #4B0000;
            background-color: #fff0f5;
            overflow: hidden;
            position: relative;
            background-image: url('https://i.pinimg.com/736x/6c/5f/6e/6c5f6e73039c2bbc79d5dd4a4266b801.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            height: 100vh;
            width: 100vw;
        }

        .floating-image {
            position: absolute;
            width: 80px;
            height: 80px;
            opacity: 0.9;
            transition: transform 0.3s ease, opacity 0.3s ease;
            animation: floatAnimation linear infinite;
        }

        .floating-image:hover {
            transform: scale(1.2);
            opacity: 1;
        }

        .title {
            font-size: 3em;
            font-weight: bold;
            margin-top: 50px;
        }

        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 2.5rem;
            margin-top: 3rem;
        }

        button {
            background-color: #8B0000;
            border: none;
            padding: 15px 30px;
            font-size: 20px;
            color: white;
            cursor: pointer;
            border-radius: 20px;
            font-family: 'Times New Roman', serif;
        }

        button:hover {
            background-color: #600000;
        }

        .hidden {
            display: none;
        }

        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
            color: #4B0000;
            width: 80%;
            max-width: 500px;
            z-index: 10;
        }

        @keyframes floatAnimation {
            from {
                transform: translateY(100vh);
                opacity: 0;
            }
            20% {
                opacity: 1;
            }
            to {
                transform: translateY(-10vh);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <audio id="background-music" autoplay loop>
        <source src="spotifydown.com - 寻一个你 (电视剧《苍兰诀》温情主题曲) - 摩登兄弟刘宇宁.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>

    <script>
        document.addEventListener("DOMContentLoaded", function () {
            const audio = document.getElementById("background-music");

            // Attempt to autoplay the music
            audio.play()
                .then(() => console.log("Music is playing"))
                .catch((err) => {
                    console.error("Autoplay blocked:", err);
                    alert("Autoplay was blocked by the browser. Please click anywhere on the page to start the music.");
                    
                    // Allow playback on interaction if autoplay is blocked
                    document.body.addEventListener("click", () => {
                        audio.play();
                    }, { once: true });
                });
        });
    </script>

    <h1 class="title">For the love of my life who I adore so much</h1>

    <div class="container">
        <button onclick="showSurprise()">Click Here for a Surprise!</button>
        <div id="surprise" class="hidden">
            <button onclick="showQuiz()">Take a Fun Love Quiz 💘</button>
            <button onclick="showStoryPopup()">Read Our Love Story 📖</button>
            <button onclick="showLetterPopup()">A Special Letter for You 💌</button>
        </div>
    </div>

    <div id="quiz-popup" class="popup">
        <p id="quiz-question"></p>
        <div id="quiz-options"></div>
        <p id="quiz-feedback"></p>
        <button onclick="closePopup('quiz-popup')">Close</button>
    </div>

    <div id="story-popup" class="popup">
        <h2>Our Love Story</h2>
        <p><a href="Thank You Letter Doc in Green Gold White Watercolor Elegant Style.pdf" target="_blank">Click here to read our love story ❤️</a></p>
        <button onclick="closePopup('story-popup')">Close</button>
    </div>

    <div id="letter-popup" class="popup">
        <h2>A Special Letter for You 💌</h2>
        <p>My love, every moment with you is magical. You are my world, my everything... 💖</p>
        <button onclick="closePopup('letter-popup')">Close</button>
    </div>

    <script>
        let quizIndex = 0;
        let score = 0;
        const quizData = [
            { question: "What is our anniversary date?", options: ["Jan 14", "Feb 13", "March 14"], answer: "Feb 13" },
            { question: "What is my favorite thing about you?", options: ["boobs", "Thighs", "personality", "Humor", "ass"], answer: "Thighs" },
            { question: "What was our bonding song?", options: ["Wap", "Fever", "Baby", "Comfortably Numb"], answer: "Comfortably Numb" }
        ];

        function showSurprise() {
            document.getElementById("surprise").style.display = "block";
        }

        function showQuiz() {
            document.getElementById("quiz-popup").style.display = "block";
            updateQuiz();
        }

        function updateQuiz() {
            if (quizIndex < quizData.length) {
                document.getElementById("quiz-question").textContent = quizData[quizIndex].question;
                document.getElementById("quiz-options").innerHTML = quizData[quizIndex].options.map(option => 
                    `<button onclick="checkAnswer('${option}')">${option}</button>`).join('');
            } else {
                document.getElementById("quiz-question").textContent = `Quiz Completed! You got ${score}/${quizData.length} questions right! 🎉`;
                document.getElementById("quiz-options").innerHTML = "";
            }
        }

        function checkAnswer(option) {
            if (option === quizData[quizIndex].answer) {
                document.getElementById("quiz-feedback").textContent = "Correct! 💖";
                score++;
            } else {
                document.getElementById("quiz-feedback").textContent = "Wrong answer 😔";
            }
            quizIndex++;
            setTimeout(updateQuiz, 1500);
        }

        const imagePaths = [
            "14-20250209T064610Z-001/14/-rp8jrl.jpg", 
            "14-20250209T064610Z-001/14/6364d646a85bd0bb5298a3aa170d4169.jpg", 
            "14-20250209T064610Z-001/14/847d1d6279e25d4b1b1b37a943d21285.jpg",
            "14-20250209T064610Z-001/14/IMG-20211220-WA0000.jpg",
            "14-20250209T064610Z-001/14/IMG-20220531-WA0002.jpg",
            "14-20250209T064610Z-001/14/IMG-20220806-WA0007 (1).jpg",
            "14-20250209T064610Z-001/14/IMG-20220819-WA0003.jpg",
            "14-20250209T064610Z-001/14/IMG-20221019-WA0007.jpg",
            "14-20250209T064610Z-001/14/IMG-20221114-WA0001.jpg",
            "14-20250209T064610Z-001/14/IMG-20230420-WA0009.jpg"
        ];

        window.onload = function() {
            imagePaths.forEach((path) => {
                const img = document.createElement('img');
                img.src = path;
                img.className = 'floating-image';
                img.style.left = `${Math.random() * 100}%`;
                img.style.animationDuration = `${Math.random() * 5 + 5}s`; 
                document.body.appendChild(img);
            });
        };

        function closePopup(id) {
            document.getElementById(id).style.display = "none";
        }

        function showStoryPopup() {
            document.getElementById("story-popup").style.display = "block";
        }

        function showLetterPopup() {
            document.getElementById("letter-popup").style.display = "block";
        }
    </script>
</body>
</html>

