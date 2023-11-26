# Quote-Generator
This is a Quote Generator web
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Random Quote Generator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f5f5f5;
      margin-top: 50px;
    }
    
    #quote-container {
      width: 60%;
      margin: 0 auto;
      padding: 20px;
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }
    
    button {
      padding: 10px 20px;
      margin-top: 20px;
      font-size: 16px;
      border: none;
      background-color: #3498db;
      color: #fff;
      border-radius: 4px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    
    button:hover {
      background-color: #2980b9;
    }
  </style>
</head>
<body>
  <div id="quote-container">
    <h1>Random Quote Generator</h1>
    <p id="quote-text">Click the button to generate a quote!</p>
    <button onclick="generateQuote()">Generate Quote</button>
  </div>

  <script>
    const quotes = [
      "The only way to do great work is to love what you do. - Steve Jobs",
      "In the middle of difficulty lies opportunity. - Albert Einstein",
      "Believe you can and you're halfway there. - Theodore Roosevelt",
      "The best way to predict the future is to create it. - Peter Drucker",
      "Success is not final, failure is not fatal: It is the courage to continue that counts. - Winston Churchill"
    ];

    function generateQuote() {
      const randomNumber = Math.floor(Math.random() * quotes.length);
      const randomQuote = quotes[randomNumber];
      document.getElementById("quote-text").textContent = randomQuote;
    }
  </script>
</body>
</html>
