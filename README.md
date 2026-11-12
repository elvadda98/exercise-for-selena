
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Everyday English – Social Conversations</title>
<style>
:root {
  --navy:#20354d;
  --blue:#477da5;
  --light:#edf4f8;
  --cream:#fbf8f1;
  --green:#477d68;
  --text:#293746;
  --muted:#718091;
  --border:#dce5eb;
}
* { box-sizing:border-box; }
body {
  margin:0;
  background:#e9eef2;
  color:var(--text);
  font-family:Arial, Helvetica, sans-serif;
}
.app {
  max-width:1050px;
  min-height:690px;
  margin:24px auto;
  background:white;
  border-radius:18px;
  overflow:hidden;
  box-shadow:0 12px 40px #24384c20;
}
header {
  background:var(--navy);
  color:white;
  padding:20px 30px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:16px;
}
.brand { font-size:14px; letter-spacing:1.5px; text-transform:uppercase; opacity:.8; }
header h1 { font-size:21px; margin:5px 0 0; }
.counter { font-size:13px; opacity:.85; white-space:nowrap; }
.progress { height:5px; background:#dce5eb; }
.progress div { height:5px; background:#75b49a; width:33.33%; transition:.3s; }
main { padding:32px 42px; min-height:540px; }
.slide { display:none; animation:fade .25s ease; }
.slide.active { display:block; }
@keyframes fade { from {opacity:.4; transform:translateY(5px)} to {opacity:1; transform:none} }
.eyebrow { color:var(--blue); font-size:12px; font-weight:bold; letter-spacing:1.5px; text-transform:uppercase; }
h2 { color:var(--navy); font-size:29px; margin:10px 0; }
.subtitle { color:var(--muted); line-height:1.6; margin:0 0 25px; }
.expression-grid {
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:13px;
}
.expression {
  border:1px solid var(--border);
  border-radius:12px;
  padding:17px 18px;
  background:#fff;
}
.expression .phrase { font-size:18px; font-weight:bold; color:var(--navy); margin-bottom:7px; }
.expression .meaning { font-size:14px; color:var(--green); font-weight:bold; margin-bottom:8px; }
.expression .example { font-size:14px; line-height:1.5; color:#586777; }
.expression:last-child { grid-column:1 / -1; }
.tip {
  margin-top:20px;
  background:var(--light);
  border-left:4px solid var(--blue);
  border-radius:7px;
  padding:14px 17px;
  font-size:14px;
  line-height:1.55;
}
.dialogue {
  background:var(--cream);
  border:1px solid #eee7d9;
  border-radius:13px;
  padding:20px;
  margin:20px 0;
}
.line { margin:13px 0; line-height:1.7; }
.speaker { font-weight:bold; color:var(--blue); }
select {
  padding:8px 10px;
  border:1px solid #b8c9d5;
  border-radius:7px;
  background:white;
  color:var(--navy);
  font-size:14px;
  max-width:100%;
}
select.correct { border:2px solid var(--green); background:#eff8f2; }
select.incorrect { border:2px solid #c66b61; background:#fff3f1; }
button {
  border:0;
  border-radius:8px;
  padding:12px 19px;
  font-size:14px;
  font-weight:bold;
  cursor:pointer;
  background:var(--blue);
  color:white;
}
button:hover { filter:brightness(.93); }
button.secondary { background:#e8eef3; color:var(--navy); }
.feedback { margin-top:13px; font-size:14px; font-weight:bold; min-height:22px; }
.scene {
  width:100%;
  background:#f3eee4;
  border-radius:14px;
  overflow:hidden;
  margin:18px 0;
}
.scene svg { width:100%; height:auto; display:block; }
.prompt-grid {
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:12px;
}
.prompt {
  background:var(--light);
  border-radius:10px;
  padding:14px;
  line-height:1.5;
  font-size:14px;
}
.wordbank {
  background:#f5f7f8;
  border:1px solid var(--border);
  border-radius:12px;
  padding:15px;
  margin:17px 0;
}
.wordbank strong { display:block; margin-bottom:10px; color:var(--navy); }
.chips { display:flex; flex-wrap:wrap; gap:8px; }
.chip {
  background:white;
  border:1px solid #cbd8e0;
  border-radius:20px;
  padding:7px 11px;
  color:var(--navy);
  font-size:13px;
}
footer {
  border-top:1px solid var(--border);
  padding:17px 28px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:12px;
}
.footer-note { color:var(--muted); font-size:12px; }
.nav { display:flex; gap:9px; }
@media(max-width:650px) {
  .app { margin:0; border-radius:0; }
  main { padding:25px 19px; }
  header { padding:17px 19px; }
  h2 { font-size:24px; }
  .expression-grid,.prompt-grid { grid-template-columns:1fr; }
  .expression:last-child { grid-column:auto; }
  footer { padding:14px 17px; }
  .footer-note { display:none; }
}
</style>
</head>
<body>
<div class="app">
<header>
  <div>
    <div class="brand">Everyday English</div>
    <h1>Feel more confident speaking English</h1>
  </div>
  <div class="counter" id="counter">Slide 1 of 3</div>
</header>
<div class="progress"><div id="progress"></div></div>

<main>
<section class="slide active">
  <div class="eyebrow">Part 1 · Useful language</div>
  <h2>Five expressions for everyday conversations</h2>
  <p class="subtitle">These expressions can help you sound more natural when meeting people and talking about yourself.</p>

  <div class="expression-grid">
    <div class="expression">
      <div class="phrase">1. What brings you here?</div>
      <div class="meaning">Why are you here?</div>
      <div class="example">“So, what brings you to Chicago?”<br>“I'm here to study and experience life in the US.”</div>
    </div>
    <div class="expression">
      <div class="phrase">2. How's it going?</div>
      <div class="meaning">How are things? / How are you?</div>
      <div class="example">“Hey, how's it going?”<br>“Pretty good, thanks! How about you?”</div>
    </div>
    <div class="expression">
      <div class="phrase">3. I'm really looking forward to...</div>
      <div class="meaning">I'm excited about something in the future.</div>
      <div class="example">“I'm really looking forward to moving to the US.”</div>
    </div>
    <div class="expression">
      <div class="phrase">4. I'm still getting used to...</div>
      <div class="meaning">Something is still new or unfamiliar to me.</div>
      <div class="example">“I'm still getting used to speaking English every day.”</div>
    </div>
    <div class="expression">
      <div class="phrase">5. That sounds interesting!</div>
      <div class="meaning">A friendly way to show interest in what someone says.</div>
      <div class="example">“I work with children.”<br>“Oh, that sounds interesting! What do you do?”</div>
    </div>
  </div>

  <div class="tip">
    <strong>Remember:</strong> These are useful expressions to learn as complete phrases. Try to remember when people use them, not just their Italian translation.
  </div>
</section>

<section class="slide">
  <div class="eyebrow">Part 2 · Let's practise</div>
  <h2>Complete the conversation</h2>
  <p class="subtitle">Imagine you've just met someone at a café in the United States. Choose the best expression for each gap.</p>

  <div class="wordbank">
    <strong>Expression bank</strong>
    <div class="chips">
      <span class="chip">What brings you here?</span>
      <span class="chip">How's it going?</span>
      <span class="chip">I'm really looking forward to...</span>
      <span class="chip">I'm still getting used to...</span>
      <span class="chip">That sounds interesting!</span>
    </div>
  </div>

  <div class="dialogue">
    <div class="line"><span class="speaker">Alex:</span> Hey! Nice to meet you. <select id="q1"><option value="">Choose an expression...</option><option>How's it going?</option><option>What brings you here?</option><option>That sounds interesting!</option><option>I'm still getting used to...</option><option>I'm really looking forward to...</option></select></div>

    <div class="line"><span class="speaker">Selena:</span> Hi! I'm good, thanks! I'm from Italy. I arrived here a few days ago.</div>

    <div class="line"><span class="speaker">Alex:</span> Oh, cool! <select id="q2"><option value="">Choose an expression...</option><option>How's it going?</option><option>What brings you here?</option><option>That sounds interesting!</option><option>I'm still getting used to...</option><option>I'm really looking forward to...</option></select></div>

    <div class="line"><span class="speaker">Selena:</span> I'm going to work as an au pair and improve my English.</div>

    <div class="line"><span class="speaker">Alex:</span> Wow! <select id="q3"><option value="">Choose an expression...</option><option>How's it going?</option><option>What brings you here?</option><option>That sounds interesting!</option><option>I'm still getting used to...</option><option>I'm really looking forward to...</option></select></div>

    <div class="line"><span class="speaker">Selena:</span> Yes! <select id="q4"><option value="">Choose an expression...</option><option>How's it going?</option><option>What brings you here?</option><option>That sounds interesting!</option><option>I'm still getting used to...</option><option>I'm really looking forward to...</option></select> meeting new people and discovering American culture.</div>

    <div class="line"><span class="speaker">Alex:</span> That's great! Is everything easy so far?</div>

    <div class="line"><span class="speaker">Selena:</span> Not everything! <select id="q5"><option value="">Choose an expression...</option><option>How's it going?</option><option>What brings you here?</option><option>That sounds interesting!</option><option>I'm still getting used to...</option><option>I'm really looking forward to...</option></select> speaking English every day.</div>
  </div>

  <button onclick="checkAnswers()">Check my answers</button>
  <button class="secondary" onclick="showAnswers()">Show answers</button>
  <div class="feedback" id="feedback" aria-live="polite"></div>
</section>

<section class="slide">
  <div class="eyebrow">Part 3 · Your turn!</div>
  <h2>Let's meet at a café!</h2>
  <p class="subtitle">Imagine you're in the US and you've just met someone new. Let's have a natural conversation!</p>

  <div class="scene">
    <svg viewBox="0 0 800 340" role="img" aria-label="Two young adults chatting across a table in a cosy café">
      <rect width="800" height="340" fill="#e9dfcf"/>
      <rect x="0" y="0" width="800" height="220" fill="#e8eee9"/>
      <rect x="45" y="28" width="210" height="150" rx="8" fill="#b7c8c1"/>
      <rect x="57" y="40" width="186" height="126" fill="#dce8df"/>
      <path d="M150 40V166 M57 102H243" stroke="#a0b7ad" stroke-width="7"/>
      <circle cx="665" cy="60" r="34" fill="#e0c58e"/>
      <path d="M665 12V0 M665 108V126 M617 60H595 M713 60H735" stroke="#c8ad78" stroke-width="5"/>
      <rect x="0" y="220" width="800" height="120" fill="#c7a887"/>
      <rect x="265" y="207" width="280" height="17" rx="8" fill="#8e6e55"/>
      <path d="M290 224L280 340 M520 224L535 340" stroke="#765b49" stroke-width="13"/>
      <!-- left person -->
      <path d="M115 230 Q110 170 175 170 Q235 170 230 230Z" fill="#63869a"/>
      <circle cx="174" cy="124" r="43" fill="#d99f78"/>
      <path d="M132 124 Q126 70 174 75 Q222 73 218 123 Q204 91 174 94 Q145 92 132 124" fill="#4b3830"/>
      <circle cx="159" cy="126" r="4" fill="#493b36"/>
      <circle cx="191" cy="126" r="4" fill="#493b36"/>
      <path d="M162 145 Q174 155 188 145" stroke="#9b5e55" fill="none" stroke-width="3" stroke-linecap="round"/>
      <!-- right person -->
      <path d="M575 230 Q570 170 640 170 Q710 170 700 230Z" fill="#b9785d"/>
      <circle cx="640" cy="124" r="43" fill="#edc09a"/>
      <path d="M598 122 Q588 64 644 72 Q696 73 682 132 Q670 93 639 94 Q613 92 598 122" fill="#6a4936"/>
      <circle cx="625" cy="126" r="4" fill="#493b36"/>
      <circle cx="653" cy="126" r="4" fill="#493b36"/>
      <path d="M628 145 Q640 155 654 145" stroke="#a76658" fill="none" stroke-width="3" stroke-linecap="round"/>
      <!-- cups and books -->
      <ellipse cx="400" cy="210" rx="22" ry="7" fill="#f8f4e9"/>
      <path d="M378 186H422L417 210H383Z" fill="#fffaf0"/>
      <path d="M422 192Q442 188 437 205Q433 213 419 207" stroke="#fffaf0" fill="none" stroke-width="7"/>
      <rect x="320" y="191" width="44" height="8" rx="3" fill="#71917f"/>
      <path d="M320 190L364 190" stroke="#f4e6ca" stroke-width="3"/>
      <path d="M440 180Q460 161 478 180" fill="none" stroke="#8eaa8c" stroke-width="5"/>
      <path d="M459 180Q453 159 444 155 M459 180Q472 157 484 158" fill="none" stroke="#63886d" stroke-width="5"/>
      <text x="400" y="30" text-anchor="middle" font-size="17" fill="#60766b" font-family="Arial" letter-spacing="3">A FRIENDLY CAFÉ</text>
    </svg>
  </div>

  <div class="prompt-grid">
    <div class="prompt"><strong>1. Start the conversation</strong><br>Greet the other person. Ask how they are doing.</div>
    <div class="prompt"><strong>2. Get to know them</strong><br>Ask where they're from and what brings them here.</div>
    <div class="prompt"><strong>3. Talk about yourself</strong><br>Explain why you're in the US and what you're looking forward to.</div>
    <div class="prompt"><strong>4. Keep it going</strong><br>Ask questions, react naturally and show interest in what they say.</div>
  </div>

  <div class="wordbank">
    <strong>Your expression bank — use these whenever you need them!</strong>
    <div class="chips">
      <span class="chip">How's it going?</span>
      <span class="chip">What brings you here?</span>
      <span class="chip">That sounds interesting!</span>
      <span class="chip">I'm really looking forward to...</span>
      <span class="chip">I'm still getting used to...</span>
    </div>
  </div>

  <div class="tip">
    <strong>Your challenge:</strong> Try to use at least three of the five expressions in your conversation. Don't worry about making mistakes — the goal is to communicate!
  </div>
</section>
</main>

<footer>
  <div class="footer-note">Everyday English · Practical speaking activity</div>
  <div class="nav">
    <button class="secondary" id="prev" onclick="move(-1)" disabled>← Back</button>
    <button id="next" onclick="move(1)">Next →</button>
  </div>
</footer>
</div>

<script>
let current = 0;
const slides = document.querySelectorAll('.slide');
const correct = [
  "How's it going?",
  "What brings you here?",
  "That sounds interesting!",
  "I'm really looking forward to...",
  "I'm still getting used to..."
];

function render() {
  slides.forEach((s,i)=>s.classList.toggle('active',i===current));
  document.getElementById('counter').textContent = `Slide ${current+1} of 3`;
  document.getElementById('progress').style.width = `${(current+1)*33.333}%`;
  document.getElementById('prev').disabled = current===0;
  document.getElementById('next').textContent = current===2 ? 'Start again ↻' : 'Next →';
}
function move(direction) {
  if(current===2 && direction===1) current=0;
  else current=Math.max(0,Math.min(2,current+direction));
  render();
}
function checkAnswers() {
  let score=0;
  correct.forEach((answer,i)=>{
    const el=document.getElementById('q'+(i+1));
    el.classList.remove('correct','incorrect');
    if(el.value===answer) {
      score++;
      el.classList.add('correct');
    } else {
      el.classList.add('incorrect');
    }
  });
  document.getElementById('feedback').textContent =
    score===5 ? 'Excellent! All five answers are correct!' :
    `You got ${score} out of 5 correct. Try again!`;
}
function showAnswers() {
  correct.forEach((answer,i)=>{
    const el=document.getElementById('q'+(i+1));
    el.value=answer;
    el.classList.remove('incorrect');
    el.classList.add('correct');
  });
  document.getElementById('feedback').textContent='Here are the correct answers. Read the conversation aloud!';
}
render();
</script>
</body>
</html>
