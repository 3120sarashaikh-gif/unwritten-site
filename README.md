<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Unwritten – Global Cultural Guide</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  <style>
    * {margin: 0; padding: 0; box-sizing: border-box;}
    body {
      font-family: 'Inter', sans-serif;
      background: linear-gradient(180deg, #f7faff, #e9f3ff);
      color: #1d1d1f;
      overflow-x: hidden;
    }
    header {
      background: rgba(255,255,255,0.75);
      backdrop-filter: blur(10px);
      position: sticky;
      top: 0;
      z-index: 10;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      border-bottom: 1px solid rgba(0,0,0,0.1);
    }
    header h1 {font-weight: 800; color: #0077ff;}
    nav a {
      margin-left: 1rem; color: #333; text-decoration: none;
      font-weight: 600; transition: color 0.3s ease;
    }
    nav a:hover {color: #0077ff;}
    select.language {
      border: none;
      font-weight: 600;
      padding: 0.4rem;
      border-radius: 6px;
      background: #e9f3ff;
      cursor: pointer;
    }
    section {padding: 5rem 10%; transition: all 0.3s ease;}
    .hero {
      text-align: center;
      background: linear-gradient(135deg, #0077ff, #00b0ff);
      color: #fff;
      padding: 6rem 10%;
    }
    .hero h2 {font-size: 3rem; font-weight: 800;}
    .hero p {font-size: 1.2rem; max-width: 650px; margin: 1rem auto;}
    .hero button {
      margin-top: 2rem;
      padding: 1rem 2rem;
      font-weight: 700;
      border: none;
      border-radius: 8px;
      color: #0077ff;
      background: #fff;
      cursor: pointer;
      transition: 0.3s;
    }
    .hero button:hover {background: #0077ff; color: #fff;}
    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 2rem;
      margin-top: 3rem;
    }
    .feature-card {
      background: rgba(255,255,255,0.8);
      backdrop-filter: blur(12px);
      border-radius: 12px;
      padding: 2rem;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      transition: transform 0.3s ease;
    }
    .feature-card:hover {transform: translateY(-5px);}
    .feature-card h3 {color: #0077ff;}
    .chatbot {
      background: #fff;
      border-radius: 16px;
      box-shadow: 0 0 20px rgba(0,0,0,0.05);
      padding: 2rem;
      max-width: 700px;
      margin: 3rem auto;
    }
    .chatbot h2 {text-align: center; margin-bottom: 1rem;}
    .chat-window {
      height: 250px;
      border: 1px solid #ddd;
      border-radius: 8px;
      padding: 1rem;
      overflow-y: auto;
      background: #fafafa;
    }
    .chat-input {
      display: flex;
      margin-top: 1rem;
    }
    .chat-input input {
      flex: 1;
      padding: 0.8rem;
      border-radius: 8px 0 0 8px;
      border: 1px solid #ccc;
      outline: none;
    }
    .chat-input button {
      padding: 0.8rem 1.2rem;
      border: none;
      border-radius: 0 8px 8px 0;
      background: #0077ff;
      color: #fff;
      font-weight: 600;
      cursor: pointer;
    }
    footer {
      text-align: center;
      background: #1d1d1f;
      color: #fff;
      padding: 2rem;
    }
  </style>
</head>
<body>
  <header>
    <h1>Unwritten</h1>
    <nav>
      <a href="#about">About</a>
      <a href="#features">Features</a>
      <a href="#bot">AI Assistant</a>
      <select class="language" id="languageSelect">
        <option value="en">English</option>
        <option value="hi">हिन्दी</option>
        <option value="ta">தமிழ்</option>
        <option value="bn">বাংলা</option>
        <option value="ml">മലയാളം</option>
        <option value="mr">मराठी</option>
        <option value="te">తెలుగు</option>
      </select>
    </nav>
  </header>

  <section class="hero" id="hero">
    <h2 id="heroTitle">Discover What Locals Never Tell You</h2>
    <p id="heroText">Get unspoken local insights, cultural etiquette, and real-time help — in your own language.</p>
    <button onclick="window.location.href='#bot'">Try AI Assistant</button>
  </section>

  <section id="about">
    <h2>About Unwritten</h2>
    <p id="aboutText">Unwritten helps travelers and immigrants understand the small, human details that define local life — from how to greet people to how to navigate daily habits.</p>
  </section>

  <section id="features">
    <h2>Key Features</h2>
    <div class="features">
      <div class="feature-card">
        <h3>🗣️ Local Habits Feed</h3>
        <p>Short, crowd-sourced insights verified by locals.</p>
      </div>
      <div class="feature-card">
        <h3>🧾 Visa & Legal Hub</h3>
        <p>Up-to-date info on visa categories, local documents, and expat regulations.</p>
      </div>
      <div class="feature-card">
        <h3>💬 Cultural AI</h3>
        <p>Ask questions and get translated cultural answers instantly.</p>
      </div>
    </div>
  </section>

  <section id="bot">
    <div class="chatbot">
      <h2>🤖 Unwritten Assistant</h2>
      <div class="chat-window" id="chatWindow">
        <p><b>Bot:</b> Hi there! Ask me about any country's culture or visa info.</p>
      </div>
      <div class="chat-input">
        <input type="text" id="userInput" placeholder="Type your question...">
        <button onclick="sendMessage()">Send</button>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2025 Unwritten — Making the invisible rules of the world visible.</p>
  </footer>

  <script>
    // --- Language System (simple dictionary-based) ---
    const translations = {
      hi: {
        heroTitle: "जो स्थानीय लोग नहीं बताते, वह जानें",
        heroText: "अपनी भाषा में स्थानीय आदतें, संस्कृति और व्यवहार जानें।",
        aboutText: "Unwritten यात्रियों और प्रवासियों को स्थानीय जीवन की छोटी-छोटी बारीकियां समझने में मदद करता है।"
      },
      ta: {
        heroTitle: "உள்ளூர்வாசிகள் சொல்லாததை கண்டறிக",
        heroText: "உங்கள் மொழியில் கலாச்சார குறிப்புகள் மற்றும் பழக்கங்கள்.",
        aboutText: "Unwritten சுற்றுலாப் பயணிகளுக்கும் குடியேறிகளுக்கும் உள்ளூர் வாழ்க்கையின் நுணுக்கங்களைப் புரிந்துகொள்கிறது."
      },
      bn: {
        heroTitle: "যা স্থানীয়রা বলে না তা জানুন",
        heroText: "আপনার ভাষায় সংস্কৃতি এবং অভ্যাসগুলি জানুন।",
        aboutText: "Unwritten ভ্রমণকারী এবং অভিবাসীদের স্থানীয় জীবনের সূক্ষ্মতা বুঝতে সাহায্য করে।"
      }
    };

    const langSelect = document.getElementById('languageSelect');
    langSelect.addEventListener('change', () => {
      const lang = langSelect.value;
      if (translations[lang]) {
        document.getElementById('heroTitle').innerText = translations[lang].heroTitle;
        document.getElementById('heroText').innerText = translations[lang].heroText;
        document.getElementById('aboutText').innerText = translations[lang].aboutText;
      } else {
        // default back to English
        document.getElementById('heroTitle').innerText = "Discover What Locals Never Tell You";
        document.getElementById('heroText').innerText = "Get unspoken local insights, cultural etiquette, and real-time help — in your own language.";
        document.getElementById('aboutText').innerText = "Unwritten helps travelers and immigrants understand the small, human details that define local life.";
      }
    });

    // --- Simple Local Chatbot Simulation ---
    const responses = {
      visa: "Visa requirements differ by country. Always check official embassy websites for the most accurate info.",
      culture: "Cultural norms vary widely — always observe locals and follow their lead respectfully.",
      hello: "Hello! I'm your Unwritten assistant. You can ask about cultural habits, visa, or etiquette.",
      india: "In India, greetings often start with 'Namaste' and it's common to remove shoes before entering homes."
    };

    function sendMessage() {
      const input = document.getElementById("userInput");
      const chatWindow = document.getElementById("chatWindow");
      const userMsg = input.value.trim();
      if (!userMsg) return;
      chatWindow.innerHTML += `<p><b>You:</b> ${userMsg}</p>`;
      input.value = "";
      let reply = "I'm still learning! Try asking about culture, visa, or a country.";
      for (let key in responses) {
        if (userMsg.toLowerCase().includes(key)) reply = responses[key];
      }
      setTimeout(() => {
        chatWindow.innerHTML += `<p><b>Bot:</b> ${reply}</p>`;
        chatWindow.scrollTop = chatWindow.scrollHeight;
      }, 500);
    }
  </script>
</body>
</html>
