<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Unwritten – The Human Map</title>

  <!-- Apple-style dark gold glass theme -->
  <style>
    :root {
      --bg-dark: #0d0d0f;
      --glass: rgba(255, 255, 255, 0.08);
      --accent-gold: #d4af37;
      --text-light: #f2f2f2;
      --text-soft: #b5b5b5;
      --blur: blur(18px);
    }

    body {
      margin: 0;
      padding: 0;
      background: var(--bg-dark);
      color: var(--text-light);
      font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", "SF Pro Text", Helvetica, Arial, sans-serif;
      overflow-x: hidden;
    }

    /* Smooth fade-in animation */
    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(20px);}
      to {opacity: 1; transform: translateY(0);}
    }

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      backdrop-filter: var(--blur);
      background: var(--glass);
      border-bottom: 1px solid rgba(255, 255, 255, 0.1);
      z-index: 10;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 12px 40px;
    }

    header h1 {
      font-size: 1.3rem;
      letter-spacing: 1px;
      color: var(--accent-gold);
      font-weight: 500;
    }

    nav a {
      color: var(--text-soft);
      text-decoration: none;
      margin: 0 14px;
      font-size: 0.95rem;
      transition: 0.3s ease;
    }

    nav a:hover {
      color: var(--accent-gold);
    }

    section {
      min-height: 100vh;
      padding: 120px 10%;
      animation: fadeIn 1s ease both;
    }

    .hero {
      text-align: center;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding-top: 80px;
    }

    .hero h2 {
      font-size: 3rem;
      margin: 0;
      font-weight: 500;
      color: var(--accent-gold);
    }

    .hero p {
      margin-top: 18px;
      color: var(--text-soft);
      max-width: 650px;
      font-size: 1.2rem;
      line-height: 1.6;
    }

    .cta-button {
      margin-top: 40px;
      padding: 12px 28px;
      border: 1px solid var(--accent-gold);
      background: transparent;
      border-radius: 8px;
      color: var(--accent-gold);
      font-size: 1rem;
      cursor: pointer;
      transition: all 0.4s ease;
    }

    .cta-button:hover {
      background: var(--accent-gold);
      color: #000;
    }

    .glass-card {
      background: var(--glass);
      backdrop-filter: var(--blur);
      border-radius: 16px;
      padding: 24px;
      margin: 20px 0;
      border: 1px solid rgba(255, 255, 255, 0.08);
      transition: transform 0.3s ease;
    }

    .glass-card:hover {
      transform: translateY(-6px);
    }

    footer {
      text-align: center;
      padding: 40px;
      color: var(--text-soft);
      font-size: 0.9rem;
      border-top: 1px solid rgba(255, 255, 255, 0.1);
    }

    .gold-text {
      color: var(--accent-gold);
    }

    .language-selector {
      position: fixed;
      bottom: 20px;
      right: 30px;
      background: var(--glass);
      border: 1px solid rgba(255,255,255,0.1);
      border-radius: 12px;
      padding: 8px 16px;
      backdrop-filter: var(--blur);
      color: var(--accent-gold);
      cursor: pointer;
      z-index: 50;
      font-size: 0.95rem;
    }

  </style>
</head>

<body>
  <header>
    <h1>Unwritten</h1>
    <nav>
      <a href="#about">About</a>
      <a href="#features">Features</a>
      <a href="#chat">Ask AI</a>
      <a href="#culture">Culture Feed</a>
      <a href="#visa">Visa Info</a>
    </nav>
  </header>

  <section class="hero" id="about">
    <h2>The Human Map</h2>
    <p>What Google Maps won’t tell you — Unwritten reveals the quiet social codes, hidden rhythms, and human truths that define every city.</p>
    <button class="cta-button" onclick="document.querySelector('#features').scrollIntoView({behavior:'smooth'})">
      Explore the Details
    </button>
  </section>
    <!-- =================== FEATURES SECTION =================== -->
  <section id="features">
    <h2 style="text-align:center;color:var(--accent-gold);font-weight:500;font-size:2.4rem;">
      Designed for the Details
    </h2>
    <p style="text-align:center;color:var(--text-soft);max-width:650px;margin:20px auto;">
      Every feature in Unwritten exists to make the unfamiliar feel human.
    </p>

    <!-- Local Habits Feed -->
    <div class="glass-card">
      <h3 class="gold-text">🗣️ Local Habits Feed</h3>
      <p>Short, authentic insights from locals & verified travelers.  
         Scroll through cultural nuances that never make it to travel guides.</p>
      <ul>
        <li>🕐 “Shops in Paris close early on Sundays.”</li>
        <li>😶 “In Japan, avoid phone calls on public transport.”</li>
        <li>💬 “In India, bargaining in small markets is expected.”</li>
      </ul>
      <a href="https://reddit.com/r/travel/" target="_blank" style="color:var(--accent-gold);">Discover community threads ›</a>
    </div>

    <!-- Daily Rhythm -->
    <div class="glass-card">
      <h3 class="gold-text">🕓 Daily Rhythm</h3>
      <p>A dynamic guide to local life — when cafés open, when streets quiet down, when to fit in seamlessly.</p>
      <a href="https://www.timeanddate.com/worldclock/" target="_blank" style="color:var(--accent-gold);">Check local time zones ›</a>
    </div>

    <!-- Cultural Dos and Don'ts -->
    <div class="glass-card">
      <h3 class="gold-text">💬 Cultural Dos & Don’ts</h3>
      <p>Practical etiquette cards to help you blend in.  
         Each country has its own social grammar — master it gracefully.</p>
      <ul>
        <li>✅ Smile at cashiers in Canada.</li>
        <li>🚫 Don’t tip in Japan — it’s considered rude.</li>
        <li>☕ Accept tea if offered in India — it’s a sign of respect.</li>
      </ul>
      <a href="https://en.wikipedia.org/wiki/Etiquette_by_region" target="_blank" style="color:var(--accent-gold);">Learn more ›</a>
    </div>

    <!-- Neighborhood Vibe -->
    <div class="glass-card">
      <h3 class="gold-text">📍 Neighborhood Vibe</h3>
      <p>Instead of stars, Unwritten rates places by their mood.  
         Find the rhythm that matches your own.</p>
      <ul>
        <li>“Quiet Residential” — Calm streets & families walking dogs.</li>
        <li>“Trendy but Pricey” — Cafés with MacBooks and matcha.</li>
        <li>“Touristy but Friendly” — Helpful locals and photo spots everywhere.</li>
      </ul>
      <a href="https://www.google.com/maps" target="_blank" style="color:var(--accent-gold);">Explore maps ›</a>
    </div>

    <!-- Expectation Radar -->
    <div class="glass-card">
      <h3 class="gold-text">💭 Expectation Radar</h3>
      <p>Understand local mindsets before you arrive.  
         Learn how formal, punctual, or open people are in daily life.</p>
      <ul>
        <li>🇩🇪 Germany — Highly punctual, direct communication.</li>
        <li>🇮🇹 Italy — Late is normal; warm but expressive interaction.</li>
        <li>🇮🇳 India — Flexible time culture; context matters more than clock.</li>
      </ul>
      <a href="https://hbr.org/2015/12/the-culture-map" target="_blank" style="color:var(--accent-gold);">Read Erin Meyer’s Culture Map ›</a>
    </div>

    <!-- Visa and Legal Info -->
    <div class="glass-card" id="visa">
      <h3 class="gold-text">🛂 Visa & Legal Essentials</h3>
      <p>Verified links to official visa resources and entry requirements — because small paperwork details shape big journeys.</p>
      <ul>
        <li>🇮🇳 <a href="https://indianvisaonline.gov.in/" target="_blank" style="color:var(--accent-gold);">India Visa Portal</a></li>
        <li>🇺🇸 <a href="https://travel.state.gov/content/travel/en/us-visas.html" target="_blank" style="color:var(--accent-gold);">US Visa Information</a></li>
        <li>🇬🇧 <a href="https://www.gov.uk/browse/visas-immigration" target="_blank" style="color:var(--accent-gold);">UK Visa & Immigration</a></li>
        <li>🌐 <a href="https://schengenvisainfo.com/" target="_blank" style="color:var(--accent-gold);">Schengen Visa Info</a></li>
        <li>🏛️ <a href="https://whc.unesco.org/en/list/" target="_blank" style="color:var(--accent-gold);">UNESCO World Heritage Sites</a></li>
      </ul>
    </div>

    <!-- Ethical Use & Community -->
    <div class="glass-card">
      <h3 class="gold-text">🤝 Community & Ethics</h3>
      <p>Unwritten thrives on authentic human input.  
         Every fact is verified by locals before it goes live — no AI hallucinations, no misinformation.</p>
      <a href="https://github.com/" target="_blank" style="color:var(--accent-gold);">Contribute on GitHub ›</a>
    </div>
  </section>
    <!-- =================== CHATBOT SECTION =================== -->
  <section id="chat">
    <h2 style="text-align:center;color:var(--accent-gold);font-weight:500;font-size:2.4rem;margin-bottom:30px;">
      Your Cultural Companion
    </h2>
    <div id="chat-container" style="max-width:700px;margin:0 auto;background:var(--glass);backdrop-filter:var(--blur);border-radius:16px;padding:24px;border:1px solid rgba(255,255,255,0.08);">
      <div id="chat-box" style="height:350px;overflow-y:auto;scroll-behavior:smooth;padding:10px;font-size:1rem;line-height:1.5;"></div>
      <div style="display:flex;margin-top:12px;">
        <input id="user-input" type="text" placeholder="Ask about etiquette, visas, or local habits..." 
          style="flex:1;padding:12px;border:none;border-radius:8px;background:rgba(255,255,255,0.06);color:var(--text-light);font-size:1rem;">
        <button onclick="sendMessage()" 
          style="margin-left:8px;padding:12px 16px;border:none;background:var(--accent-gold);color:#000;border-radius:8px;cursor:pointer;font-weight:600;">
          ➤
        </button>
      </div>
    </div>
  </section>

  <!-- =================== LANGUAGE SELECTOR =================== -->
  <div class="language-selector" onclick="toggleLanguageMenu()">🌐 Language</div>
  <div id="language-menu" style="display:none;position:fixed;bottom:70px;right:30px;background:var(--glass);padding:16px;border-radius:12px;backdrop-filter:var(--blur);">
    <p style="margin:0 0 8px 0;color:var(--accent-gold);font-weight:500;">Select Language</p>
    <select id="language-dropdown" style="padding:8px;width:200px;border-radius:6px;border:none;background:rgba(255,255,255,0.08);color:var(--text-light);">
      <option value="en">English</option>
      <option value="hi">हिन्दी (Hindi)</option>
      <option value="ta">தமிழ் (Tamil)</option>
      <option value="bn">বাংলা (Bengali)</option>
      <option value="te">తెలుగు (Telugu)</option>
      <option value="mr">मराठी (Marathi)</option>
      <option value="ml">മലയാളം (Malayalam)</option>
    </select>
    <button onclick="translatePage()" style="margin-top:10px;padding:8px 16px;border:none;background:var(--accent-gold);color:#000;border-radius:6px;cursor:pointer;">Apply</button>
  </div>

  <!-- =================== CHATBOT + TRANSLATION SCRIPT =================== -->
  <script>
    const GOOGLE_API_KEY = "YOUR_GOOGLE_TRANSLATE_API_KEY"; // Insert your key here

    function toggleLanguageMenu() {
      const menu = document.getElementById('language-menu');
      menu.style.display = menu.style.display === 'none' ? 'block' : 'none';
    }

    async function translateText(text, targetLang) {
      try {
        const response = await fetch(`https://translation.googleapis.com/language/translate/v2?key=${GOOGLE_API_KEY}`, {
          method: "POST",
          headers: { "Content-Type": "application/json" },
          body: JSON.stringify({
            q: text,
            target: targetLang,
          }),
        });
        const data = await response.json();
        return data.data.translations[0].translatedText;
      } catch (error) {
        console.error("Translation error:", error);
        return text;
      }
    }

    async function translatePage() {
      const lang = document.getElementById('language-dropdown').value;
      const elements = document.querySelectorAll('h2, h3, p, li, button, a');
      for (let el of elements) {
        const translated = await translateText(el.innerText, lang);
        el.innerText = translated;
      }
      document.getElementById('language-menu').style.display = 'none';
    }

    // ============ CHATBOT LOGIC ==============
    const chatBox = document.getElementById('chat-box');

    function addMessage(sender, message) {
      const msgDiv = document.createElement('div');
      msgDiv.style.margin = '12px 0';
      msgDiv.style.color = sender === 'user' ? 'var(--text-light)' : 'var(--accent-gold)';
      msgDiv.innerHTML = `<strong>${sender === 'user' ? 'You' : 'Unwritten AI'}:</strong> ${message}`;
      chatBox.appendChild(msgDiv);
      chatBox.scrollTop = chatBox.scrollHeight;
    }

    function sendMessage() {
      const input = document.getElementById('user-input');
      const text = input.value.trim();
      if (!text) return;
      addMessage('user', text);
      input.value = '';
      respondToQuery(text);
    }

    async function respondToQuery(text) {
      let reply = "";

      // simple contextual AI logic
      const t = text.toLowerCase();
      if (t.includes("visa")) {
        reply = "You can explore verified visa details here: 🇮🇳 India: indianvisaonline.gov.in | 🇬🇧 UK: gov.uk/visas-immigration | 🇺🇸 USA: travel.state.gov.";
      } else if (t.includes("food") || t.includes("eat")) {
        reply = "In many Asian countries, sharing food shows community — in Taiwan or India, it's polite to offer before eating.";
      } else if (t.includes("greeting")) {
        reply = "Greetings differ beautifully: Japan bows, France kisses cheeks, India joins hands with a Namaste.";
      } else if (t.includes("thank") || t.includes("appreciate")) {
        reply = "You’re welcome. Every culture values gratitude — even if the gesture looks different.";
      } else if (t.includes("language")) {
        reply = "Unwritten supports multilingual exploration — from Hindi to Tamil, Telugu, and Malayalam.";
      } else {
        reply = "That’s an interesting question. While local customs vary, the key is observing and adapting kindly — it always translates.";
      }

      addMessage('bot', reply);
    }
  </script>

    <!-- =================== ANIMATED SECTION TRANSITIONS =================== -->
  <script>
    // Smooth fade-in animations on scroll
    const fadeElements = document.querySelectorAll('section, .feature-card');
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = 1;
          entry.target.style.transform = 'translateY(0)';
        }
      });
    }, { threshold: 0.2 });

    fadeElements.forEach(el => {
      el.style.opacity = 0;
      el.style.transform = 'translateY(40px)';
      el.style.transition = 'opacity 1.2s ease-out, transform 1.2s ease-out';
      observer.observe(el);
    });

    // Elegant Apple-style scroll
    window.addEventListener("scroll", () => {
      const scrollPos = window.scrollY;
      document.querySelector(".hero-content h1").style.transform = `translateY(${scrollPos * 0.3}px)`;
      document.querySelector(".hero-content p").style.opacity = `${1 - scrollPos / 400}`;
    });
  </script>

  <!-- =================== FOOTER =================== -->
  <footer style="margin-top:100px;background:rgba(255,255,255,0.03);backdrop-filter:var(--blur);padding:40px 0;text-align:center;border-top:1px solid rgba(255,255,255,0.08);">
    <div style="max-width:800px;margin:auto;">
      <h3 style="color:var(--accent-gold);font-weight:500;font-size:1.4rem;">Unwritten</h3>
      <p style="color:rgba(255,255,255,0.6);margin:10px 0 20px;">A cultural intelligence project blending AI, translation, and human connection — designed for a world without borders.</p>
      <div style="margin:20px 0;">
        <a href="https://github.com" target="_blank" style="color:var(--accent-gold);text-decoration:none;margin:0 10px;">GitHub</a>
        <a href="https://openai.com" target="_blank" style="color:var(--accent-gold);text-decoration:none;margin:0 10px;">OpenAI</a>
        <a href="https://translate.google.com/" target="_blank" style="color:var(--accent-gold);text-decoration:none;margin:0 10px;">Google Translate</a>
        <a href="https://developer.apple.com/" target="_blank" style="color:var(--accent-gold);text-decoration:none;margin:0 10px;">Apple Developers</a>
      </div>
      <p style="color:rgba(255,255,255,0.4);font-size:0.85rem;">© 2025 Unwritten Project. All rights reserved.</p>
    </div>
  </footer>

  <!-- =================== BACK TO TOP BUTTON =================== -->
  <button id="backToTop" onclick="window.scrollTo({top: 0, behavior: 'smooth'});" 
    style="position:fixed;bottom:30px;right:30px;background:var(--accent-gold);border:none;color:#000;font-weight:600;padding:12px 16px;border-radius:8px;cursor:pointer;display:none;">
    ↑
  </button>

  <script>
    const backToTop = document.getElementById('backToTop');
    window.addEventListener('scroll', () => {
      backToTop.style.display = window.scrollY > 400 ? 'block' : 'none';
    });
  </script>

  <!-- =================== END OF PAGE =================== -->
  </body>
</html>
