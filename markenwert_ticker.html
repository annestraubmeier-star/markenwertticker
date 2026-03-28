<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Markenwert-Ticker</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #f8f6f2;
    --surface: #ffffff;
    --surface2: #f1efea;
    --border: rgba(0,0,0,0.09);
    --border-bright: rgba(0,0,0,0.18);
    --text: #1a1918;
    --muted: #8c8880;
    --accent: #2c2c2a;
    --gold: #a07828;
    --gold-dim: rgba(160,120,40,0.08);
    --green: #2d7d52;
    --green-dim: rgba(45,125,82,0.08);
    --red: #b84040;
    --red-dim: rgba(184,64,64,0.08);
    --purple: #534ab7;
  }

  html, body {
    height: 100%;
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    overflow: hidden;
  }

  #app {
    height: 100vh;
    display: flex;
    flex-direction: column;
    padding: 2rem 3rem;
    gap: 1.5rem;
    position: relative;
  }

  /* ── HEADER ── */
  header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-shrink: 0;
  }

  .header-left { display: flex; align-items: center; gap: 1.5rem; }

  .logo-mark {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.2em;
    color: var(--muted);
    text-transform: uppercase;
  }

  .logo-mark span { color: var(--gold); }

  .round-indicator {
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    color: var(--muted);
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .dots { display: flex; gap: 5px; }
  .dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--border-bright);
    transition: background 0.3s;
  }
  .dot.done { background: var(--gold); }
  .dot.active { background: var(--text); }

  .score-display {
    font-family: 'DM Mono', monospace;
    font-size: 13px;
    color: var(--muted);
  }
  .score-display span { color: var(--text); font-weight: 500; }

  /* ── QUESTION LINE ── */
  .question-bar {
    flex-shrink: 0;
    text-align: center;
  }

  .question-text {
    font-size: clamp(1.1rem, 2.5vw, 1.5rem);
    font-weight: 600;
    letter-spacing: -0.02em;
    color: var(--accent);
    opacity: 0;
    transform: translateY(8px);
    animation: fadeUp 0.4s ease forwards 0.1s;
  }

  /* ── ARENA ── */
  .arena {
    flex: 1;
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    gap: 1.5rem;
    align-items: center;
    min-height: 0;
  }

  .brand-card {
    height: 100%;
    max-height: 320px;
    border: 1px solid var(--border);
    border-radius: 16px;
    background: var(--surface);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    padding: 2rem;
    cursor: pointer;
    transition: border-color 0.25s, background 0.25s, transform 0.15s, box-shadow 0.25s;
    position: relative;
    overflow: hidden;
    box-shadow: 0 1px 3px rgba(0,0,0,0.06), 0 4px 16px rgba(0,0,0,0.04);
  }

  .brand-card::before {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 16px;
    opacity: 0;
    transition: opacity 0.3s;
  }

  .brand-card:hover:not(.disabled)::before { opacity: 1; background: rgba(0,0,0,0.02); }
  .brand-card:hover:not(.disabled) { border-color: var(--border-bright); transform: translateY(-2px); box-shadow: 0 4px 20px rgba(0,0,0,0.10); }
  .brand-card:active:not(.disabled) { transform: scale(0.99); }

  .brand-card.correct { border-color: var(--green); background: var(--green-dim); }
  .brand-card.wrong { border-color: var(--red); background: var(--red-dim); }
  .brand-card.revealed-winner { border-color: var(--gold); background: var(--gold-dim); }
  .brand-card.disabled { cursor: default; }

  .brand-sector {
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .brand-name {
    font-size: clamp(1.6rem, 4vw, 2.8rem);
    font-weight: 800;
    letter-spacing: -0.04em;
    text-align: center;
    line-height: 1;
    color: var(--text);
  }

  .brand-value {
    font-family: 'DM Mono', monospace;
    font-size: clamp(1.2rem, 2.5vw, 1.8rem);
    font-weight: 500;
    color: var(--gold);
    text-align: center;
    min-height: 2.2rem;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .brand-value.hidden-val {
    letter-spacing: 0.1em;
    color: var(--muted);
    font-size: 1.2rem;
  }

  .hint-label {
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.06em;
    text-align: center;
  }

  .choice-badge {
    position: absolute;
    top: 14px;
    right: 14px;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 0.15em;
    padding: 4px 10px;
    border-radius: 30px;
    opacity: 0;
    transition: opacity 0.3s;
  }
  .correct .choice-badge { background: var(--green); color: #ffffff; opacity: 1; }
  .wrong .choice-badge { background: var(--red); color: #ffffff; opacity: 1; }
  .revealed-winner .choice-badge { background: var(--gold); color: #ffffff; opacity: 1; }

  /* ── VS DIVIDER ── */
  .vs-divider {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    flex-shrink: 0;
  }

  .vs-circle {
    width: 52px; height: 52px;
    border-radius: 50%;
    border: 1px solid var(--border-bright);
    background: var(--surface2);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 13px;
    font-weight: 700;
    color: var(--muted);
    letter-spacing: 0.05em;
    box-shadow: 0 1px 4px rgba(0,0,0,0.06);
  }

  /* ── BOTTOM ── */
  .bottom-area {
    flex-shrink: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }

  .instruction {
    font-size: 13px;
    color: var(--muted);
    letter-spacing: 0.04em;
    text-align: center;
    opacity: 0;
    animation: fadeUp 0.4s ease forwards 0.3s;
  }

  .feedback-bar {
    height: 52px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    width: 100%;
    max-width: 640px;
  }

  .feedback-text {
    font-size: 14px;
    font-weight: 600;
    text-align: center;
    opacity: 0;
    transform: translateY(6px);
    transition: opacity 0.35s, transform 0.35s;
  }
  .feedback-text.show { opacity: 1; transform: translateY(0); }
  .feedback-text.correct { color: var(--green); }
  .feedback-text.wrong { color: var(--red); }

  .context-line {
    font-size: 12px;
    color: var(--muted);
    text-align: center;
    max-width: 560px;
    line-height: 1.6;
    opacity: 0;
    transition: opacity 0.4s 0.15s;
  }
  .context-line.show { opacity: 1; }

  .next-btn {
    background: var(--text);
    color: var(--bg);
    border: none;
    padding: 12px 36px;
    border-radius: 8px;
    font-family: 'Syne', sans-serif;
    font-size: 14px;
    font-weight: 700;
    letter-spacing: 0.05em;
    cursor: pointer;
    opacity: 0;
    transform: translateY(6px);
    transition: opacity 0.3s, transform 0.3s, background 0.15s;
    pointer-events: none;
  }
  .next-btn.show { opacity: 1; transform: translateY(0); pointer-events: auto; }
  .next-btn:hover { background: var(--accent); color: #f8f6f2; }

  /* ── RESULT SCREEN ── */
  #result-screen {
    display: none;
    height: 100vh;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1.5rem;
    padding: 3rem;
    text-align: center;
  }

  .result-score-num {
    font-size: clamp(4rem, 12vw, 8rem);
    font-weight: 800;
    letter-spacing: -0.05em;
    color: var(--gold);
    font-family: 'DM Mono', monospace;
    line-height: 1;
  }

  .result-label {
    font-size: 1.1rem;
    color: var(--muted);
    max-width: 400px;
    line-height: 1.6;
  }

  .result-insight {
    font-size: 13px;
    color: var(--muted);
    max-width: 520px;
    line-height: 1.7;
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.2rem 1.5rem;
    background: var(--surface);
    text-align: left;
  }

  .result-insight strong { color: var(--accent); font-weight: 600; }

  .restart-btn {
    background: transparent;
    border: 1px solid var(--border-bright);
    color: var(--text);
    padding: 11px 32px;
    border-radius: 8px;
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.06em;
    cursor: pointer;
    transition: border-color 0.2s, background 0.2s;
    margin-top: 0.5rem;
  }
  .restart-btn:hover { border-color: var(--text); background: var(--surface2); }

  .source-tag {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.08em;
    position: absolute;
    bottom: 1.2rem;
    right: 2rem;
  }

  @keyframes fadeUp {
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes revealPop {
    0% { transform: scale(0.9); opacity: 0; }
    60% { transform: scale(1.04); }
    100% { transform: scale(1); opacity: 1; }
  }

  .value-reveal { animation: revealPop 0.45s cubic-bezier(0.34,1.56,0.64,1) forwards; }
</style>
</head>
<body>

<div id="app">
  <header>
    <div class="header-left">
      <div class="logo-mark">Marken<span>wert</span> Ticker</div>
      <div class="dots" id="dots"></div>
    </div>
    <div class="score-display">Punkte: <span id="score-val">0</span> / <span id="total-val">6</span></div>
  </header>

  <div class="question-bar">
    <p class="question-text">Welche Marke hat den höheren Interbrand-Markenwert?</p>
  </div>

  <div class="arena">
    <div class="brand-card" id="card-a">
      <div class="brand-sector" id="sector-a"></div>
      <div class="brand-name" id="name-a"></div>
      <div class="brand-value" id="val-a"></div>
      <div class="hint-label" id="hint-a"></div>
      <span class="choice-badge" id="badge-a"></span>
    </div>

    <div class="vs-divider">
      <div class="vs-circle">VS</div>
    </div>

    <div class="brand-card" id="card-b">
      <div class="brand-sector" id="sector-b"></div>
      <div class="brand-name" id="name-b"></div>
      <div class="brand-value hidden-val" id="val-b">???</div>
      <div class="hint-label" id="hint-b"></div>
      <span class="choice-badge" id="badge-b"></span>
    </div>
  </div>

  <div class="bottom-area">
    <p class="instruction" id="instruction">Klicke auf die Marke mit dem höheren Markenwert</p>
    <div class="feedback-bar">
      <div>
        <div class="feedback-text" id="feedback"></div>
        <div class="context-line" id="context"></div>
      </div>
    </div>
    <button class="next-btn" id="next-btn" onclick="nextRound()">Weiter →</button>
  </div>

  <div class="source-tag">Quelle: Interbrand Best Global Brands 2024 · Werte in Mrd. USD</div>
</div>

<div id="result-screen">
  <div class="logo-mark" style="margin-bottom:0.5rem">Marken<span style="color:var(--gold)">wert</span> Ticker</div>
  <div class="result-score-num" id="final-score"></div>
  <div class="result-label" id="final-label"></div>
  <div class="result-insight">
    <strong>Was steckt hinter diesen Zahlen?</strong><br><br>
    Der Interbrand-Markenwert ist kein Buchwert – er ergibt sich aus drei Komponenten:
    dem wirtschaftlichen Gewinn der Marke (Financial Analysis), dem Anteil, den die Marke
    an der Kaufentscheidung hat (Role of Brand Index), und der Markenstärke auf einer
    0–100-Skala (Brand Strength Score). Starke Marken senken das Risiko, schwache erhöhen
    den Diskontierungssatz – und damit fällt der Wert.
  </div>
  <button class="restart-btn" onclick="restart()">Nochmal spielen</button>
  <div class="source-tag" style="position:static; margin-top:1rem;">Interbrand Best Global Brands 2024</div>
</div>

<script>
const pairs = [
  {
    a: { name: "Apple", sector: "Technologie", val: 503, hint: "Bekannter Wert" },
    b: { name: "Google", sector: "Technologie", val: 333, hint: "Raten!" },
    winner: "a",
    context: "Apple 50 % wertvoller als Google – obwohl Google mehr Menschen täglich nutzen. Apples Role of Brand Index ist deutlich höher: Kunden zahlen bewusst für die Marke, nicht nur das Produkt."
  },
  {
    a: { name: "Mercedes-Benz", sector: "Automobil", val: 61, hint: "Bekannter Wert" },
    b: { name: "BMW", sector: "Automobil", val: 41, hint: "Raten!" },
    winner: "a",
    context: "Mercedes vor BMW – beide Premiummarken, aber Mercedes erzielt höhere Preispremien und hat einen stärkeren Markenwert im Luxussegment, was den Brand Strength Score hebt."
  },
  {
    a: { name: "Louis Vuitton", sector: "Luxury & Fashion", val: 32, hint: "Bekannter Wert" },
    b: { name: "Hermès", sector: "Luxury & Fashion", val: 20, hint: "Raten!" },
    winner: "a",
    context: "LV 60 % wertvoller als Hermès – trotz Hermès' extremer Exklusivität. LVMHs Skalierung und globale Distribution erzeugen den höheren wirtschaftlichen Gewinn, den Interbrand bewertet."
  },
  {
    a: { name: "Coca-Cola", sector: "FMCG & Getränke", val: 106, hint: "Bekannter Wert" },
    b: { name: "Pepsi", sector: "FMCG & Getränke", val: 20, hint: "Raten!" },
    winner: "a",
    context: "Coca-Cola fünfmal wertvoller als Pepsi – bei ähnlichem Produkt. Ein Lehrbuchbeispiel: Der Role of Brand Index ist bei Cola extrem hoch. Die Marke ist das Produkt."
  },
  {
    a: { name: "Nike", sector: "Sport & Lifestyle", val: 50, hint: "Bekannter Wert" },
    b: { name: "Adidas", sector: "Sport & Lifestyle", val: 14, hint: "Raten!" },
    winner: "a",
    context: "Nike dreimal so hoch wie Adidas – obwohl Adidas in Europa stärker wahrgenommen wird. Nikes globale Lifestyle-Identifikation und höhere Margen treiben den Brand Strength Score."
  },
  {
    a: { name: "Visa", sector: "Finanzen", val: 136, hint: "Bekannter Wert" },
    b: { name: "JPMorgan", sector: "Finanzen", val: 27, hint: "Raten!" },
    winner: "a",
    context: "Visa fast fünfmal wertvoller als JPMorgan – obwohl JPMorgan eine riesige Bank ist. Visa's Marke beeinflusst direkt das Kaufverhalten bei jeder Transaktion: maximaler Role of Brand Index."
  },
  {
    a: { name: "Ferrari", sector: "Automobil", val: 9, hint: "Bekannter Wert" },
    b: { name: "Porsche", sector: "Automobil", val: 17, hint: "Raten!" },
    winner: "b",
    context: "Überraschung: Porsche fast doppelt so hoch wie Ferrari. Ferrari ist exklusiver – aber Porsches höhere Stückzahlen und breitere Marktrelevanz erzeugen deutlich mehr wirtschaftlichen Gewinn."
  },
  {
    a: { name: "Nescafé", sector: "FMCG & Getränke", val: 13, hint: "Bekannter Wert" },
    b: { name: "Starbucks", sector: "Gastronomie & Retail", val: 13, hint: "Raten!" },
    winner: "b",
    context: "Gleichstand – beide bei ca. 13 Mrd. USD. Zwei völlig unterschiedliche Geschäftsmodelle im selben Wertbereich: Das zeigt, wie Interbrand branchenübergreifend vergleichbar macht."
  },
  {
    a: { name: "Zara", sector: "Gastronomie & Retail", val: 16, hint: "Bekannter Wert" },
    b: { name: "H&M", sector: "Gastronomie & Retail", val: 11, hint: "Raten!" },
    winner: "a",
    context: "Zara vor H&M – Inditexs schnelleres Fast-Fashion-Modell und stärkere Markenwahrnehmung als 'erschwingliches Design' erzeugen höhere Markenloyalität und einen besseren Brand Strength Score."
  },
  {
    a: { name: "Samsung", sector: "Technologie", val: 91, hint: "Bekannter Wert" },
    b: { name: "Toyota", sector: "Automobil", val: 64, hint: "Raten!" },
    winner: "a",
    context: "Samsung vor Toyota – trotz ähnlicher Umsatzgröße. Consumer Electronics erzeugt kürzere Kaufzyklen und höhere Markenfrequenz, was den wirtschaftlichen Gewinn und den Cashflow stärkt."
  }
];

let current = 0, score = 0, answered = false;

function fmt(v) { return v + " Mrd. USD"; }

function buildDots() {
  const d = document.getElementById('dots');
  d.innerHTML = '';
  pairs.forEach((_, i) => {
    const dot = document.createElement('div');
    dot.className = 'dot' + (i < current ? ' done' : i === current ? ' active' : '');
    d.appendChild(dot);
  });
}

function resetAnimation(el) {
  el.style.animation = 'none';
  el.offsetHeight;
  el.style.animation = '';
}

function load(i) {
  answered = false;
  const p = pairs[i];
  document.getElementById('total-val').textContent = pairs.length;

  ['a','b'].forEach(side => {
    const card = document.getElementById('card-' + side);
    const data = p[side];
    card.className = 'brand-card';
    document.getElementById('sector-' + side).textContent = data.sector;
    document.getElementById('name-' + side).textContent = data.name;
    document.getElementById('hint-' + side).textContent = data.hint;
    document.getElementById('badge-' + side).textContent = '';
  });

  const valA = document.getElementById('val-a');
  valA.className = 'brand-value';
  valA.textContent = fmt(p.a.val);

  const valB = document.getElementById('val-b');
  resetAnimation(valB);
  valB.className = 'brand-value hidden-val';
  valB.textContent = '???';

  document.getElementById('feedback').className = 'feedback-text';
  document.getElementById('feedback').textContent = '';
  document.getElementById('context').className = 'context-line';
  document.getElementById('context').textContent = '';

  const nb = document.getElementById('next-btn');
  nb.className = 'next-btn';
  nb.textContent = i < pairs.length - 1 ? 'Weiter →' : 'Ergebnis →';

  document.getElementById('instruction').style.opacity = '1';
  buildDots();
}

function guess(side) {
  if (answered) return;
  answered = true;

  const p = pairs[current];
  const correct = side === p.winner;
  if (correct) score++;
  document.getElementById('score-val').textContent = score;

  const valB = document.getElementById('val-b');
  resetAnimation(valB);
  valB.className = 'brand-value value-reveal';
  valB.textContent = fmt(p.b.val);
  document.getElementById('hint-b').textContent = 'Echter Wert';

  ['a','b'].forEach(s => {
    const card = document.getElementById('card-' + s);
    card.classList.add('disabled');
    const badge = document.getElementById('badge-' + s);
    if (s === p.winner) {
      card.classList.add(s === side ? 'correct' : 'revealed-winner');
      badge.textContent = s === side ? '✓ RICHTIG' : 'HÖHER';
    } else {
      if (s === side) {
        card.classList.add('wrong');
        badge.textContent = '✗ NIEDRIGER';
      }
    }
  });

  const fb = document.getElementById('feedback');
  fb.className = 'feedback-text show ' + (correct ? 'correct' : 'wrong');
  fb.textContent = correct ? '+1 Punkt – Gut erkannt!' : 'Knapp daneben!';

  setTimeout(() => {
    const ctx = document.getElementById('context');
    ctx.textContent = p.context;
    ctx.className = 'context-line show';
  }, 300);

  document.getElementById('instruction').style.opacity = '0';

  setTimeout(() => {
    document.getElementById('next-btn').className = 'next-btn show';
  }, 600);

  buildDots();
}

function nextRound() {
  current++;
  if (current >= pairs.length) {
    showResult();
  } else {
    load(current);
  }
}

function showResult() {
  document.getElementById('app').style.display = 'none';
  const rs = document.getElementById('result-screen');
  rs.style.display = 'flex';
  document.getElementById('final-score').textContent = score + ' / ' + pairs.length;
  const labels = [
    "Markenwert ist überraschender als man denkt – genau das macht diesen Block spannend.",
    "Solides Markenwissen. Einige Werte überraschen selbst Experten.",
    "Hervorragend. Ihr kennt eure Marken – und versteht wie Interbrand denkt."
  ];
  const idx = score <= 2 ? 0 : score <= 4 ? 1 : 2;
  document.getElementById('final-label').textContent = labels[idx];
}

function restart() {
  current = 0; score = 0;
  document.getElementById('result-screen').style.display = 'none';
  document.getElementById('app').style.display = 'flex';
  document.getElementById('score-val').textContent = '0';
  load(0);
}

document.getElementById('card-a').addEventListener('click', () => guess('a'));
document.getElementById('card-b').addEventListener('click', () => guess('b'));

load(0);
</script>
</body>
</html>
