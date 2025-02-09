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
        }

        .popup button {
            margin-top: 10px;
            background-color: #8B0000;
            color: white;
        }
    </style>
</head>
<body>
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
        <p id="quiz-feedback" class="wrong-answer"></p>
        <button onclick="nextQuestion()">Next</button>
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
        function showSurprise() {
            document.getElementById("surprise").classList.remove("hidden");
        }

        function showQuiz() {
            quizIndex = 0;
            updateQuiz();
            document.getElementById("quiz-popup").style.display = "block";
        }

        function showStoryPopup() {
            document.getElementById("story-popup").style.display = "block";
        }

        function showLetterPopup() {
            document.getElementById("letter-popup").style.display = "block";
        }

        function closePopup(id) {
            document.getElementById(id).style.display = "none";
        }

        let quizIndex = 0;
        const quizData = [
            { question: "What is our anniversary date?", options: ["Jan 14", "Feb 13", "March 14"], answer: "Feb 13" },
            { question: "What is my favorite thing about you?", options: ["boobs", "Thighs", "personality", "Humor","ass"], answer: "Thighs" },
            { question: "Whats was our bonding song?", options: ["Wap", "Fever", "Baby", "Comfortabley Numb"], answer: "Comfortabley Numb" }
        ];

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
