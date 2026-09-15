# Our-2years-anniversary-
For PU TUU LAY
<html lang="my">
<head>
    <link rel="apple-touch-icon" href="IMG_1064.jpeg">
<link rel="icon" type="image/jpeg" href="IMG_1064.jpeg">

    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Our 2nd Anniversary 💕</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 100%);
            color: #333;
            text-align: center;
            padding: 20px;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Passcode Screen */
        #passcode-screen {
            background: rgba(255, 255, 255, 0.95);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
            max-width: 350px;
            width: 100%;
        }

        #passcode-screen h2 {
            color: #e63946;
            margin-bottom: 15px;
        }

        .pass-input {
            width: 80%;
            padding: 12px;
            font-size: 1.2em;
            text-align: center;
            border: 2px solid #ffb3c1;
            border-radius: 10px;
            outline: none;
            margin-bottom: 15px;
            letter-spacing: 5px;
        }

        .btn-unlock {
            background-color: #ff4d6d;
            color: white;
            border: none;
            padding: 10px 25px;
            font-size: 1em;
            border-radius: 20px;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn-unlock:hover {
            background-color: #c9184a;
        }

        .error-msg {
            color: red;
            font-size: 0.85em;
            margin-top: 10px;
            display: none;
        }

        /* Main Content Screen (Hidden by default) */
        #main-content {
            display: none;
            max-width: 600px;
            width: 100%;
            background: rgba(255, 255, 255, 0.9);
            padding: 25px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        h1 {
            color: #e63946;
            margin-bottom: 10px;
            font-size: 2em;
        }

        .subtitle {
            font-size: 1em;
            color: #555;
            margin-bottom: 20px;
        }

        /* Timer Box */
        .timer-box {
            background: #ffe5ec;
            padding: 15px;
            border-radius: 12px;
            margin-bottom: 20px;
            border: 2px dashed #ffb3c1;
        }

        #days-count {
            font-size: 1.8em;
            color: #a4133c;
            font-weight: bold;
        }

        /* Photo Slideshow */
        .slideshow-container {
            position: relative;
            max-width: 100%;
            height: 250px;
            margin: 0 auto 20px auto;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
        }

        .slide {
            display: none;
            width: 100%;
            height: 100%;
        }

        .slide img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            padding: 10px 15px;
            color: white;
            font-weight: bold;
            font-size: 18px;
            background-color: rgba(0,0,0,0.4);
            border-radius: 50%;
            user-select: none;
            transition: 0.3s;
        }

        .next { right: 10px; }
        .prev { left: 10px; }
        .prev:hover, .next:hover { background-color: rgba(0,0,0,0.8); }

        /* Letter Box */
        .letter-box {
            background: #fff;
            padding: 20px;
            border-radius: 12px;
            text-align: left;
            line-height: 1.6;
            color: #444;
            margin-bottom: 20px;
            box-shadow: inset 0 0 8px rgba(0,0,0,0.03);
        }

        /* Controls */
        .controls {
            display: flex;
            justify-content: center;
            gap: 10px;
            flex-wrap: wrap;
        }

        .btn-action {
            background-color: #ff4d6d;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 0.9em;
            border-radius: 20px;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn-action:hover { background-color: #c9184a; }

        /* Hearts Animation */
        .heart {
            position: fixed;
            font-size: 24px;
            animation: float 2.5s linear forwards;
            pointer-events: none;
        }

        @keyframes float {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            100% { transform: translateY(-100vh) scale(1.5); opacity: 0; }
        }
    </style>
</head>
<body>

    <!-- Passcode Lock Screen -->
    <div id="passcode-screen">
        <h2>🔒 Lock Screen</h2>
        <p style="margin-bottom: 15px; color: #666;">ဖွင့်ရန် Passcode ထည့်ပါ</p>
        <input type="password" id="passcode-input" class="pass-input" placeholder="••••" maxlength="10">
        <br>
        <button class="btn-unlock" onclick="checkPasscode()">Open ❤️</button>
        <p id="error-msg" class="error-msg">Passcode မှားယွင်းနေပါသည်။ ပြန်ကြိုးစားပါ။</p>
    </div>

    <!-- Main Content Screen -->
    <div id="main-content">
        <h1>Happy 2years Anniversary! ❤️</h1>
        <p class="subtitle">ငါတို့နှစ်ယောက်ရဲ့ အမှတ်တရနေ့လေး</p>

        <!-- Day Counter -->
        <div class="timer-box">
            <div style="font-size:0.9em; color:#c9184a; font-weight:bold;">ငါတို့ စတင်ချစ်ကြိုက်ခဲ့တာ</div>
            <div id="days-count">0 ရက်</div>
        </div>

        <!-- Slideshow Gallery -->
        <div class="slideshow-container">
            <div class="slide"><img src="IMG_5281.jpeg" alt="Photo 1"></div>
            <div class="slide"><img src="IMG_5273.jpeg" alt="Photo 2"></div>
            <div class="slide"><img src="IMG_2334.jpg" alt="Photo 3"></div>

            <a class="prev" onclick="moveSlide(-1)">&#10094;</a>
            <a class="next" onclick="moveSlide(1)">&#10095;</a>
        </div>

        <!-- Message Box -->
        <div class="letter-box">
            <p><b>ချစ်ရတဲ့သူလေးသို့... 💌</b></p><br>
            <p>ငါတို့နှစ်ယောက် အတူတူလက်တွဲလာတာ အခုဆိုရင် ၂ နှစ်တိုင်ခဲ့ပြီနော်။ ဒီအချိန်တွေအတွင်းမှာ ပျော်စရာတွေ၊ ရန်ဖြစ်လိုက် ပြန်စလိုက်နဲ့ အမှတ်တရတွေအများကြီး ဖန်တီးခဲ့ကြတယ်။ ငါ့ဘေးမှာ အမြဲရှိပေးပြီး နားလည်ပေးလို့ ကျေးဇူးအများကြီးတင်ပါတယ်။ ရှေ့ဆက်ပြီးတော့လည်း အကြာကြီး လက်တွဲသွားကြရအောင်နော်။ ချစ်တယ်! ❤️</p>
        </div>

        <!-- Buttons -->
        <div class="controls">
            <button class="btn-action" onclick="toggleAudio()">🎵 Music Play / Pause</button>
            <button class="btn-action" onclick="createHearts()">Click Me! ❤️</button>
        </div>
    </div>

    <!-- Background Music -->
    <audio id="bg-music" loop>
        <source src="music.mp3" type="audio/mpeg">
    </audio>

    <script>
        // 1. Passcode စစ်ဆေးခြင်း
        const CORRECT_PASSCODE = "250924"; // ဒီနေရာမှာ ကြိုက်နှစ်သက်ရာ Passcode ပြောင်းပါ

        function checkPasscode() {
            const input = document.getElementById('passcode-input').value;
            const error = document.getElementById('error-msg');
            const music = document.getElementById('bg-music');

            if (input === CORRECT_PASSCODE) {
                document.getElementById('passcode-screen').style.display = 'none';
                document.getElementById('main-content').style.display = 'block';
                updateCounter();
                showSlides(slideIndex);
                
                // Passcode မှန်ရင် သီချင်းအလိုအလျောက် ပွင့်မည်
                music.play().catch(() => {
                    console.log("Autoplay was prevented by browser.");
                });
            } else {
                error.style.display = 'block';
            }
        }

        // 2. Day Counter
        const startDate = new Date(2024, 8, 25); // မိမိတို့ စတင်တွဲခဲ့သည့် (၂၀၂၄နှစ်, လ-၈, ၂၅ရက်)

        function updateCounter() {
            const today = new Date();
            const timeDiff = today - startDate;
            const daysDiff = Math.floor(timeDiff / (1000 * 60 * 60 * 24));
            document.getElementById('days-count').innerText = daysDiff + " ရက် ရှိပြီ";
        }

        // 3. Slideshow Logic
        let slideIndex = 1;

        function moveSlide(n) {
            showSlides(slideIndex += n);
        }

        function showSlides(n) {
            let slides = document.getElementsByClassName("slide");
            if (n > slides.length) { slideIndex = 1 }
            if (n < 1) { slideIndex = slides.length }
            for (let i = 0; i < slides.length; i++) {
                slides[i].style.display = "none";
            }
            slides[slideIndex-1].style.display = "block";
        }

        // Auto Slide (၅ စက္ကန့်တစ်ခါ အလိုအလျောက် ပုံပြောင်းမည်)
        setInterval(() => {
            if(document.getElementById('main-content').style.display === 'block') {
                moveSlide(1);
            }
        }, 5000);

        // 4. Music Toggle
        function toggleAudio() {
            const music = document.getElementById('bg-music');
            if (music.paused) {
                music.play();
            } else {
                music.pause();
            }
        }

        // 5. Floating Hearts Animation
        function createHearts() {
            for (let i = 0; i < 15; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.classList.add('heart');
                    heart.innerHTML = '❤️';
                    heart.style.left = Math.random() * 100 + 'vw';
                    heart.style.bottom = '0px';
                    heart.style.animationDuration = (Math.random() * 2 + 2) + 's';
                    document.body.appendChild(heart);

                    setTimeout(() => { heart.remove(); }, 3000);
                }, i * 150);
            }
        }
    </script>
</body>
</html>
