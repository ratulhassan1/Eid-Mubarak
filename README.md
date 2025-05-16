# Eid-Mubarak
<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ঈদ মোবারক</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Bengali:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Noto Sans Bengali', sans-serif;
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364); /* একটি সুন্দর ডার্ক গ্র্যাডিয়েন্ট */
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
            box-sizing: border-box;
            text-align: center;
        }

        .container {
            background-color: rgba(255, 255, 255, 0.1); /* হালকা স্বচ্ছ সাদা ব্যাকগ্রাউন্ড */
            padding: 30px 40px;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            max-width: 600px; /* কন্টেইনারের সর্বোচ্চ প্রস্থ */
            width: 90%; /* ছোট স্ক্রিনের জন্য */
        }

        header h1 {
            font-size: 2.8em; /* বড় শিরোনাম */
            color: #4CAF50; /* ঈদের জন্য সবুজ রঙ */
            margin-bottom: 20px;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .greeting-message {
            font-size: 1.2em;
            line-height: 1.6;
            margin-bottom: 30px;
        }

        .sender-info {
            font-size: 1.1em;
            margin-top: 20px;
            color: #f0f0f0;
        }

        #senderName {
            font-weight: bold;
            color: #FFD700; /* প্রেরকের নামের জন্য সোনালী রঙ */
        }

        footer p {
            font-size: 0.9em;
            margin-top: 30px;
            color: #aaa;
        }

        /* Responsive ডিজাইন */
        @media (max-width: 600px) {
            header h1 {
                font-size: 2.2em;
            }
            .greeting-message, .sender-info {
                font-size: 1em;
            }
            .container {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>ঈদ মোবারক</h1>
        </header>
        <main>
            <p class="greeting-message">
                এই পবিত্র ঈদে আপনাকে এবং আপনার পরিবারের সকলকে জানাই আন্তরিক শুভেচ্ছা ও অভিনন্দন।
                আল্লাহ আপনার সকল দোয়া কবুল করুন এবং আপনার জীবনকে সুখ, শান্তি ও সমৃদ্ধিতে ভরিয়ে দিন।
            </p>
            <p class="sender-info">
                শুভেচ্ছান্তে,
                <span id="senderName">একজন শুভাকাঙ্ক্ষী</span>
            </p>
        </main>
        <footer>
            <p>সবাইকে ঈদ মোবারক!</p>
        </footer>
    </div>

    <script>
        window.onload = function() {
            // URL থেকে প্যারামিটার পাওয়ার জন্য
            const urlParams = new URLSearchParams(window.location.search);
            const sender = urlParams.get('sender'); // 'sender' নামের প্যারামিটারটি পান

            const senderNameElement = document.getElementById('senderName');

            if (sender) {
                // URL-এ + চিহ্ন থাকলে সেটাকে স্পেস দিয়ে রিপ্লেস করুন এবং ডিকোড করুন
                const decodedSender = decodeURIComponent(sender.replace(/\+/g, ' '));
                senderNameElement.textContent = decodedSender;
            } else {
                // যদি sender প্যারামিটার না থাকে, তাহলে ডিফল্ট নামটিই থাকবে
                // অথবা আপনি চাইলে এই অংশটুকু হাইড করে দিতে পারেন:
                // document.querySelector('.sender-info').style.display = 'none';
            }
        };
    </script>
</body>
</html>
