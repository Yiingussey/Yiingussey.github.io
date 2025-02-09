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

        .container a {
            display: block;
            background-color: #8B0000;
            color: white;
            text-decoration: none;
            padding: 15px 30px;
            border-radius: 20px;
            font-size: 20px;
            font-family: 'Times New Roman', serif;
        }

        .container a:hover {
            background-color: #600000;
        }

        /* Tulip Frame */
        .tulip-frame {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            background-image: url('https://i.pinimg.com/736x/6c/5f/6e/6c5f6e73039c2bbc79d5dd4a4266b801.jpg'); /* Updated background */
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            opacity: 0.3;
            z-index: -1;
        }

        .quiz-popup {
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
        }

        .quiz-popup button {
            margin-top: 10px;
            background-color: #8B0000;
            color: white;
        }

        .wrong-answer {
            color: red;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="tulip-frame"></div>

    <h1 class="title">For the love of my life who I adore so much</h1>

    <div class="container">
        <button onclick="showSurprise()">Click Here for a Surprise!</button>
        <div id="surprise" class="hidden">
            <button onclick="showQuiz()">Take a Fun Love Quiz 💘</button>
            <a href="story.html">Read Our Love Story 📖</a>
            <a href="letters.html">A Special Letter for You 💌</a>
        </div>
    </div>

    <div id="quiz-popup" class="quiz-popup">
        <p id="quiz-question"></p>
        <div id="quiz-options"></div>
        <p id="quiz-feedback" class="wrong-answer"></p>
        <button onclick="nextQuestion()">Next</button>
    </div>

    <script>
        function showSurprise() {
            document.getElementById("surprise").classList.remove("hidden");
        }

        let quizIndex = 0;
        const quizData = [
            { question: "What is our anniversary date?", options: ["Jan 14", "Feb 13", "March 14"], answer: "Feb 13" },
            { question: "What is my favorite thing about you?", options: ["boobs", "Thighs", "personality", "Humor","ass"], answer: "Thighs" },
            { question: "Whats was our bonding song?", options: ["Wap", "Fever", "Baby", "Comfortabley Numb"], answer: "Comfortabley Numb" }
        ];

        function showQuiz() {
            quizIndex = 0;
            updateQuiz();
            document.getElementById("quiz-popup").style.display = "block";
        }

        function updateQuiz() {
            let questionData = quizData[quizIndex];
            document.getElementById("quiz-question").textContent = questionData.question;
            let optionsHTML = "";
            questionData.options.forEach(option => {
                optionsHTML += `<button onclick='checkAnswer("${option}")'>${option}</button><br>`;
            });
            document.getElementById("quiz-options").innerHTML = optionsHTML;
            document.getElementById("quiz-feedback").textContent = "";
        }

        function checkAnswer(selected) {
            let correct = quizData[quizIndex].answer;
            if (selected === correct) {
                document.getElementById("quiz-feedback").textContent = "Correct!";
                document.getElementById("quiz-feedback").style.color = "green";
            } else {
                document.getElementById("quiz-feedback").textContent = "Oops! Try again.";
                document.getElementById("quiz-feedback").style.color = "red";
            }
        }

        function nextQuestion() {
            if (quizIndex < quizData.length - 1) {
                quizIndex++;
                updateQuiz();
            } else {
                document.getElementById("quiz-popup").style.display = "none";
                alert("You're amazing! Quiz finished ❤️");
            }
        }
    </script>
</body>
</html>

