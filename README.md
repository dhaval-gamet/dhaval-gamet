---
layout: none
permalink: /
---

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dhaval | Portfolio</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            width: 100%;
            overflow: hidden;
        }
        iframe {
            width: 100%;
            height: 100vh;
            border: none;
        }
        .fallback {
            display: none;
        }
        @media (max-width: 768px) {
            iframe {
                height: 100vh;
            }
        }
    </style>
</head>
<body>
    <iframe src="portfolio.html" title="Dhaval Portfolio"></iframe>
    
    <!-- Fallback content -->
    <div class="fallback">
        <h1>Dhaval | Solo Developer & Tech Explorer</h1>
        <p>If you see this, please <a href="portfolio.html">click here to view the portfolio</a></p>
    </div>
    
    <script>
        // Fallback for iframe issues
        setTimeout(function() {
            const iframe = document.querySelector('iframe');
            if (!iframe.contentDocument || !iframe.contentDocument.body) {
                document.querySelector('.fallback').style.display = 'block';
                iframe.style.display = 'none';
            }
        }, 3000);
    </script>
</body>
</html>
