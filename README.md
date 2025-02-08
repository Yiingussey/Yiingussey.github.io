<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Surprise ❤️</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
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
    
    <script>
        function showSurprise() {
            document.getElementById("surprise").classList.remove("hidden");
        }
    </script>
</body>
</html>
