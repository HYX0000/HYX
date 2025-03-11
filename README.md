# HYX
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Collaboration Request</title>
    <style>
        body {
            background: #f0f4f8;
            font-family: 'Segoe UI', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }

        .card {
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 2rem;
            max-width: 500px;
            width: 90%;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        h1 {
            color: #2d3748;
            margin-bottom: 1.5rem;
            font-weight: 600;
        }

        .content {
            color: #4a5568;
            line-height: 1.6;
            margin-bottom: 2rem;
        }

        .button {
            background: #4299e1;
            color: white;
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            cursor: pointer;
            transition: background 0.3s ease;
        }

        .button:hover {
            background: #3182ce;
        }

        .response {
            margin-top: 1.5rem;
            display: none;
            color: #48bb78;
            font-weight: 500;
        }

        .emoji {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            opacity: 0.9;
        }
    </style>
</head>
<body>
    <div class="card">
        <div class="emoji">🤝</div>
        <h1>Teamwork Proposal</h1>
        <div class="content">
            <p>算了写的句子不给你看了.</p>
            <p>一大段你也别看了.</p>
        </div>
        <button class="button" onclick="showResponse()">View Proposal</button>
        <div id="response" class="response">
            Open to discuss whenever you're ready.
        </div>
    </div>

    <script>
        function showResponse() {
            const response = document.getElementById('response');
            response.style.display = 'block';
            
            // Add smooth appearance
            response.style.opacity = 0;
            let opacity = 0;
            const fadeIn = setInterval(() => {
                opacity += 0.1;
                response.style.opacity = opacity;
                if (opacity >= 1) clearInterval(fadeIn);
            }, 50);
        }
    </script>
</body>
</html>
