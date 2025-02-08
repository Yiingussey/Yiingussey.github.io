
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
            background-color: #fff0f5;
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

        .title {
            font-size: 3em;
            font-weight: bold;
            margin-top: 30px;
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

        /* Quiz Pop-up */
        .quiz-popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
            text-align: center;
            width: 300px;
        }

        .quiz-popup button {
            margin-top: 10px;
        }

        .wrong {
            color: red;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <!-- Background Images -->
    <div class="background">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_1" alt="Background 1">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_2" alt="Background 2">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_3" alt="Background 3">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_4" alt="Background 4">
        <img src="https://drive.google.com/uc?id=YOUR_IMAGE_ID_5" alt="Background 5">
    </div>

    <!-- Title -->
    <h1 class="title">For the love of my life who I adore so much</h1>

    <!-- Main Content -->
    <div class="container">
        <button onclick="showSurprise()">Click Here for a Surprise!</button>
        <div id="surprise" class="hidden">
            <a href="#" onclick="openQuiz()">Take a Fun Love Quiz 💘</a>
            <a href="story.html">Read Our Love Story 📖</a>
            <a href="letters.html">A Special Letter for You 💌</a>
        </div>
    </div>

    <!-- Quiz Pop-up -->
    <div id="quiz-popup" class="quiz-popup">
        <p id="quiz-question">Question 1: What is my favorite color?</p>
        <button onclick="checkAnswer(this, true)">Red</button>
        <button onclick="checkAnswer(this, false)">Blue</button>
        <button onclick="checkAnswer(this, false)">Green</button>
        <button onclick="checkAnswer(this, false)">Yellow</button>
        <p id="feedback" class="hidden"></p>
        <button onclick="nextQuestion()">Next</button>
    </div>

    <script>
        function showSurprise() {
            document.getElementById("surprise").classList.remove("hidden");
        }

        function openQuiz() {
            document.getElementById("quiz-popup").style.display = "block";
        }

        let currentQuestion = 0;
        const questions = [
            { question: "What is my favorite color?", answers: ["Red", "Blue", "Green", "Yellow"], correct: 0 },
            { question: "Where did we first meet?", answers: ["School", "Cafe", "Park", "Online"], correct: 3 },
            { question: "What is my favorite dessert?", answers: ["Cake", "Ice Cream", "Cookies", "Chocolate"], correct: 1 }
        ];

        function checkAnswer(button, isCorrect) {
            if (isCorrect) {
                document.getElementById("feedback").textContent = "Correct! 😊";
                document.getElementById("feedback").classList.remove("wrong");
            } else {
                document.getElementById("feedback").textContent = "Oops, wrong answer! 😢";
                document.getElementById("feedback").classList.add("wrong");
            }
            document.getElementById("feedback").classList.remove("hidden");
        }

        function nextQuestion() {
            currentQuestion++;
            if (currentQuestion < questions.length) {
                document.getElementById("quiz-question").textContent = questions[currentQuestion].question;
                const buttons = document.querySelectorAll("#quiz-popup button:not(:last-child)");
                buttons.forEach((btn, index) => {
                    btn.textContent = questions[currentQuestion].answers[index];
                    btn.setAttribute("onclick", `checkAnswer(this, ${index === questions[currentQuestion].correct})`);
                });
                document.getElementById("feedback").classList.add("hidden");
            } else {
                document.getElementById("quiz-popup").innerHTML = "<p>You're amazing! Quiz completed! 🎉</p><button onclick='closeQuiz()'>Close</button>";
            }
        }

        function closeQuiz() {
            document.getElementById("quiz-popup").style.display = "none";
        }
    </script>

</body>
</html>


            iframe.style.border = "none";
            document.body.appendChild(iframe);
        };
    </script>
</body>
</html>
