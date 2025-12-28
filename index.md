---
layout: none
permalink: /
---

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta http-equiv="refresh" content="0; url=portfolio.html">
    <link rel="canonical" href="portfolio.html">
    <title>Redirecting to Portfolio...</title>
    <style>
        body {
            background: #0f172a;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: 'Segoe UI', sans-serif;
            text-align: center;
        }
        .spinner {
            border: 5px solid rgba(99, 102, 241, 0.3);
            border-top: 5px solid #6366f1;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            animation: spin 1s linear infinite;
            margin: 20px auto;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <div>
        <div class="spinner"></div>
        <h1>Loading Portfolio...</h1>
        <p>If not redirected automatically, <a href="portfolio.html" style="color:#8b5cf6;">click here</a></p>
    </div>
</body>
</html>
