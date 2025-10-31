<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Unwritten – The Unspoken Rules of the World</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  <style>
    *{margin:0;padding:0;box-sizing:border-box;}
    body{font-family:'Inter',sans-serif;background:#f6f9fc;color:#1c1c1c;}
    header{background:#fff;position:sticky;top:0;z-index:100;box-shadow:0 2px 5px rgba(0,0,0,0.05);display:flex;justify-content:space-between;align-items:center;padding:1rem 2rem;}
    header h1{font-weight:800;color:#0077ff;}
    nav a{margin:0 1rem;color:#333;text-decoration:none;font-weight:600;}
    nav a:hover{color:#0077ff;}
    select.language{border:none;background:#f0f0f0;padding:0.4rem;border-radius:6px;cursor:pointer;}
    section{padding:5rem 10%;transition:all 0.3s ease;}
    .hero{text-align:center;background:linear-gradient(135deg,#0077ff,#00b0ff);color:#fff;padding:6rem 10%;}
    .hero h2{font-size:3rem;font-weight:800;}
    .hero p{font-size:1.2rem;max-width:650px;margin:1rem auto;}
    .hero button{margin-top:2rem;padding:1rem 2rem;font-weight:700;border:none;border-radius:8px;color:#0077ff;background:#fff;cursor:pointer;}
    .hero button:hover{background:#0077ff;color:#fff;}
    .features{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:2rem;margin-top:3rem;}
    .feature-card{background:#fff;border-radius:12px;box-shadow:0 5px 15px rgba(0,0,0,0.05);padding:2rem;transition:transform 0.3s;}
    .feature-card:hover{transform:translateY(-5px);}
    .feature-card h3{color:#0077ff;margin-bottom:1rem;}
    .feature-card a{color:#0077ff;font-weight:600;text-decoration:none;}
    .chatbot{background:#fff;border-radius:16px;box-shadow:0 0 20px rgba(0,0,0,0.05);padding:2rem;max-width:700px;margin:3rem auto;}
    .chat-window{height:250px;border:1px solid #ddd;border-radius:8px;padding:1rem;overflow-y:auto;background:#fafafa;}
    .chat-input{display:flex;margin-top:1rem;}
    .chat-input input{flex:1;padding:0.8rem;border-radius:8px 0 0 8px;border:1px solid #ccc;outline:none;}
    .chat-input button{padding:0.8rem 1.2rem;border:none;border-radius:0 8px 8px 0;background:#0077ff;color:#fff;font-weight:600;cursor:pointer;}
    footer{text-align:center;background:#1d1d1f;color:#fff;padding:2rem;margin-top:3rem;}
    .link-list ul{list-style:none;padding:0;}
    .link-list li{margin:0.5rem 0;}
  </style>
</head>
<body>
  <header>
    <h1>Unwritten</h1>
    <nav>
      <a href="#about">About</a>
      <a href="#features">Features</a>
      <a href="#bot">AI Bot</a>
      <a href="#resources">Resources</a>
      <select class="language" id="languageSelect">
        <option value="en">English</option>
        <option value="hi">हिन्दी</option>
        <option value="ta">தமிழ்</option>
        <option value="bn">বাংলা</option>
        <option value="te">తెలుగు</option>
        <option value="mr">मराठी</option>
      </select>
    </nav>
  </header>

  <section class="hero">
    <h2 id="heroTitle">Discover What Locals Never Tell You</h2>
    <p id="heroText">Unwritten reveals unspoken local habits, social cues, and the invisible rules that shape every culture — in your own language.</p>
    <button onclick="window.location.href='#features'">Explore</button>
  </section>

  <section id="about">
    <h2>About</h2>
    <p id="aboutText">Unwritten bridges the gap between maps and manners. It’s not just about where to go — but *how to belong.*</p>
  </section>

  <section id="features">
    <h2>Key Features</h2>
    <div class="features">
      <div class="feature-card">
        <h3>🗣️ Local Habits Feed</h3>
        <p>Explore real tips shared by locals and travelers. Learn what time cafes open, how people greet, and what’s polite to say.</p>
        <div class="link-list">
          <ul>
            <li><a href="https://reddit.com/r/travel" target="_blank">Reddit Travel Threads</a></li>
            <li><a href="https://culturecrossing.net" target="_blank">Culture Crossing Database</a></li>
          </ul>
        </div>
      </div>
      <div class="feature-card">
        <h3>🧾 Visa & Legal Hub</h3>
        <p>Find verified links for official visa info and migration portals.</p>
        <div class="link-list">
          <ul>
            <li><a href="https://indianvisaonline.gov.in" target="_blank">🇮🇳 India Visa Portal</a></li>
            <li><a href="https://travel.state.gov" target="_blank">🇺🇸 U.S. Visa Resources</a></li>
            <li><a href="https://www.gov.uk/browse/visas-immigration" target="_blank">🇬🇧 UK Visas & Immigration</a></li>
            <li><a href="https://www.schengenvisainfo.com/" target="_blank">🇪🇺 Schengen Visa Guide</a></li>
          </ul>
        </div>
      </div>
      <div class="feature-card">
        <h3>💬 Cultural Dos & Don’ts</h3>
        <p>Instantly learn what to do (and not do) in new countries.</p>
        <div class="link-list">
          <ul>
            <li><a href="https://www.expatarrivals.com/" target="_blank">Expat Culture Guides</a></li>
            <li><a href="https://www.commisceo-global.com/resources/country-guides" target="_blank">Commisceo Global Etiquette Guides</a></li>
          </ul>
        </div>
      </div>
      <div class="feature-card">
        <h3>🏙️ Neighborhood Vibe</h3>
        <p>Find local neighborhoods based on atmosphere and lifestyle — quiet, trendy, family-friendly, or expat-heavy.</p>
        <a href="https://nomadlist.com/" target="_blank">Explore Nomad List</a>
      </div>
      <div class="feature-card">
        <h3>🧠 Expectation Radar</h3>
        <p>Understand local behavior patterns: punctuality, hierarchy, casualness, and communication norms.</p>
        <a href="https://hbr.org/2014/04/navigating-the-cultural-minefield" target="_blank">Read Harvard’s Culture Map</a>
      </div>
    </div>
  </section>

  <section id="bot">
    <div class="chatbot">
      <h2>🤖 Unwritten AI Assistant</h2>
      <div class="chat-window" id="chatWindow">
        <p><b>Bot:</b> Hi there! I can help with local culture, etiquette, or visa info. Ask me anything.</p>
      </div>
      <div class="chat-input">
        <input type="text" id="userInput" placeholder="Type your question...">
        <button onclick="sendMessage()">Send</button>
      </div>
    </div>
  </section>

  <section id="resources">
    <h2>🌐 Global Resource Hub</h2>
    <p>Trusted official references for travelers, students, and immigrants:</p>
    <ul>
      <li><a href="https://www.un.org/en/" target="_blank">United Nations – Global Mobility & Rights</a></li>
      <li><a href="https://www.iom.int/" target="_blank">International Organization for Migration (IOM)</a></li>
      <li><a href="https://www.who.int/travel-advice" target="_blank">WHO Travel Health Advice</a></li>
      <li><a href="https://www.icao.int/" target="_blank">International Civil Aviation Organization (ICAO)</a></li>
    </ul>
  </section>

  <footer>
    <p>© 2025 Unwritten — Making the invisible rules of the world visible.</p>
  </footer>

  <script>
    const translations={
      hi:{heroTitle:"जो स्थानीय लोग नहीं बताते, वह जानें",heroText:"Unwritten आपको स्थानीय संस्कृति, आदतें और व्यवहार अपने शब्दों में सिखाता है।",aboutText:"Unwritten नक्शों और व्यवहार के बीच की दूरी मिटाता है।"},
      ta:{heroTitle:"உள்ளூர்வாசிகள் சொல்லாததை அறியுங்கள்",heroText:"Unwritten உங்கள் மொழியில் கலாச்சாரம் மற்றும் பழக்கங்களை பகிர்கிறது.",aboutText:"Unwritten வரைபடங்கள் மற்றும் மனிதத் தன்மைகளுக்கு இடையேயான இடைவெளியை நிரப்புகிறது."},
      bn:{heroTitle:"যা স্থানীয়রা বলে না তা জানুন",heroText:"Unwritten আপনার ভাষায় সংস্কৃতি ও অভ্যাস বোঝায়।",aboutText:"Unwritten মানচিত্র ও শিষ্টাচারের ফাঁক পূরণ করে।"}
    };
    const langSelect=document.getElementById("languageSelect");
    langSelect.addEventListener("change",()=>{
      const lang=langSelect.value;
      if(translations[lang]){
        document.getElementById("heroTitle").innerText=translations[lang].heroTitle;
        document.getElementById("heroText").innerText=translations[lang].heroText;
        document.getElementById("aboutText").innerText=translations[lang].aboutText;
      }else{
        document.getElementById("heroTitle").innerText="Discover What Locals Never Tell You";
        document.getElementById("heroText").innerText="Unwritten reveals unspoken local habits, social cues, and invisible rules.";
        document.getElementById("aboutText").innerText="Unwritten bridges the gap between maps and manners.";
      }
    });

    const responses={
      visa:"Visa policies differ by country. Always check your nearest embassy’s official site for updated rules.",
      culture:"Cultural norms vary widely — observe locals respectfully and adapt slowly.",
      india:"In India, greetings often start with 'Namaste'. It’s polite to remove shoes before entering homes.",
      japan:"In Japan, punctuality and silence on public transport are signs of respect.",
      hello:"Hello! I’m your Unwritten guide — ask me about culture, visa, or local etiquette."
    };

    function sendMessage(){
      const input=document.getElementById("userInput");
      const chat=document.getElementById("chatWindow");
      const msg=input.value.trim();
      if(!msg)return;
      chat.innerHTML+=`<p><b>You:</b> ${msg}</p>`;
      input.value="";
      let reply="I'm still learning! Try asking about India, visa, or culture.";
      for(let key in responses){if(msg.toLowerCase().includes(key))reply=responses[key];}
      setTimeout(()=>{chat.innerHTML+=`<p><b>Bot:</b> ${reply}</p>`;chat.scrollTop=chat.scrollHeight;},600);
    }
  </script>
</body>
</html>
