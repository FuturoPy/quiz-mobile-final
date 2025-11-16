<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
<title>Quiz Escolar 🎓</title>
<style>
  /* ---------- RESET & BASE ---------- */
  *{box-sizing:border-box}
  html,body{height:100%}
  body{
    margin:0;
    padding:0;
    font-family:"Comic Sans MS", Arial, sans-serif;
    -webkit-font-smoothing:antialiased;
    background-color:#000;
    color:#fff;
    overscroll-behavior-y:contain;
  }

  /* ----- CONTAINER (center) ----- */
  .app {
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    padding:env(safe-area-inset-top) 12px env(safe-area-inset-bottom);
  }

  /* ---------- TELA INICIAL ---------- */
  #tela-inicial{
    position:fixed;
    inset:0;
    background-image:url('https://uploads.onecompiler.io/444jywmud/444jyqxv3/inico%20de%20tela.png');
    background-size:cover;
    background-position:center;
    z-index:5;
    display:flex;
    align-items:center;
    justify-content:center;
    transition:opacity .4s ease;
  }
  #start-btn{
    appearance:none;
    -webkit-appearance:none;
    border:none;
    background:linear-gradient(180deg,#0b7f8f,#006d74);
    color:white;
    font-weight:800;
    font-size:20px;
    padding:14px 26px;
    border-radius:16px;
    box-shadow:0 8px 20px rgba(0,0,0,.6);
    cursor:pointer;
  }
  #start-btn:active{transform:translateY(1px) scale(.998)}
  #particles{ position:fixed; inset:0; pointer-events:none; z-index:4; }

  /* ---------- QUIZ LAYOUT (MOBILE-FIRST) ---------- */
  .quiz-container{
    width:100%;
    max-width:420px; /* muito próximo do iPhone13 lógico 390 */
    margin:0 auto;
    background:linear-gradient(180deg, rgba(0,0,0,0.55), rgba(0,0,0,0.45));
    border-radius:18px;
    padding:14px;
    display:none;
    flex-direction:column;
    gap:12px;
    box-shadow:0 10px 30px rgba(0,0,0,.7);
    position:relative;
    z-index:2;
  }

  .top-row{
    display:flex;
    gap:12px;
    align-items:flex-start;
  }

  /* professora ao lado / mobile otimizado: professora em cima em telas muito pequenas */
  .professor{
    flex:0 0 120px;
    height:150px;
    background-repeat:no-repeat;
    background-position:bottom center;
    background-size:contain;
    border-radius:12px;
    align-self:flex-start;
  }

  /* quadro ocupa a maior parte */
  .quadro-fundo{
    flex:1 1 auto;
    background: linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));
    border-radius:12px;
    padding:12px;
    min-height:180px;
    display:flex;
    flex-direction:column;
    justify-content:flex-start;
    gap:10px;
  }
  #question{ font-size:18px; line-height:1.25; margin:0; min-height:48px; }

  /* respostas (botões grandes e touch-friendly) */
  #answers{ display:flex; flex-direction:column; gap:10px; margin-top:6px; }
  #answers button{
    appearance:none; -webkit-appearance:none;
    border:2px solid rgba(255,255,255,0.14);
    background:rgba(255,255,255,0.02);
    color:#fff;
    padding:14px 12px;
    font-size:16px;
    border-radius:12px;
    text-align:center;
    cursor:pointer;
    width:100%;
    transition:transform .12s ease, box-shadow .12s ease, border-color .12s ease;
  }
  #answers button:hover{ transform:translateY(-2px) }
  #answers button:active{ transform:translateY(0) scale(.998) }
  #answers button:disabled{ opacity:.55; cursor:not-allowed; transform:none }

  /* classes visuais para selecionada/correta/errada */
  #answers button.selecionada{ box-shadow:0 6px 18px rgba(255,255,255,0.06); }
  #answers button.correta{ border-color:#00ff99; color:#00ff99; font-weight:700; background:rgba(0,255,153,0.03) }
  #answers button.errada{ border-color:#ff9999; color:#ff9999; font-weight:700; background:rgba(255,153,153,0.02) }

  /* feedback */
  .feedback{ min-height:28px; font-size:18px; font-weight:700; margin-top:6px; text-shadow:0 1px 2px rgba(0,0,0,0.6) }
  .feedback.correct{ color:#00ff99 }
  .feedback.wrong{ color:#ff9999 }

  /* controles inferiores (avançar/voltar/terminar) */
  .controls{
    display:flex;
    justify-content:space-between;
    gap:8px;
    margin-top:6px;
  }
  .controls button{
    flex:1;
    background:rgba(255,255,255,0.03);
    border:2px solid rgba(255,255,255,0.06);
    color:#fff;
    padding:12px 10px;
    border-radius:12px;
    font-weight:700;
    cursor:pointer;
    font-size:15px;
  }
  .controls button:disabled{ opacity:.45; cursor:not-allowed }

  /* painel do professor (cadastro) - botão simples flutuante */
  #professor-login{ position:fixed; top:12px; left:50%; transform:translateX(-50%); background:rgba(0,0,0,0.6); padding:8px; border-radius:12px; z-index:10; display:flex; gap:8px; align-items:center; }
  #professor-login input{ padding:8px; border-radius:8px; border:none; outline:none; width:120px }
  #cadastro-perguntas{ position:fixed; left:50%; top:60px; transform:translateX(-50%); width:340px; max-height:66vh; overflow:auto; background:rgba(0,0,0,0.75); padding:12px; border-radius:12px; display:none; z-index:12 }
  #cadastro-perguntas input, #cadastro-perguntas select{ width:100%; padding:8px; margin:6px 0; border-radius:8px; border:none }

  #btn-sair-edicao{ position:fixed; right:12px; top:12px; background:#ff4444; border:none; color:#fff; padding:8px 12px; border-radius:10px; display:none; z-index:11; }

  /* pequenas melhorias para iPhone 13 (largura lógica 390) */
  @media (min-width:360px) and (max-width:430px){
    .quiz-container{ padding:12px; border-radius:14px; max-width:390px }
    .professor{ flex:0 0 110px; height:140px }
    #question{ font-size:18px }
    #answers button{ padding:13px; font-size:16px; border-radius:12px }
    .controls button{ padding:12px; font-size:15px }
  }

  /* Em telas maiores (tablet/desktop) mantemos estilo porém com mais espaço */
  @media (min-width:900px){
    .app{ padding:40px }
    .quiz-container{ max-width:920px; display:flex; gap:18px; padding:18px; flex-direction:row; align-items:flex-start }
    .top-row{ flex-direction:row }
    .professor{ flex:0 0 300px; height:420px; background-size:contain; }
    .quadro-fundo{ min-height:420px; }
    #answers{ gap:14px }
    #answers button{ font-size:18px; padding:16px 18px; width:420px }
    .controls{ margin-top:18px }
  }

  /* utility */
  .hidden{ display:none !important }
</style>
</head>
<body>
  <div id="tela-inicial">
    <canvas id="particles"></canvas>
    <button id="start-btn">COMEÇAR</button>
  </div>

  <!-- painel professor (pequeno) -->
  <div id="professor-login">
    <input id="senha-professor" type="password" placeholder="Senha professor" />
    <button id="btn-entrar">Entrar</button>
  </div>

  <div id="cadastro-perguntas" aria-hidden="true">
    <h3 style="margin:6px 0 10px 0">Adicionar Pergunta</h3>
    <input id="nova-pergunta" placeholder="Pergunta" />
    <input id="alt1" placeholder="Alternativa 1" />
    <input id="alt2" placeholder="Alternativa 2" />
    <input id="alt3" placeholder="Alternativa 3" />
    <select id="certa">
      <option value="0">Alternativa 1</option>
      <option value="1">Alternativa 2</option>
      <option value="2">Alternativa 3</option>
    </select>
    <button id="btn-adicionar">Adicionar Pergunta</button>
  </div>

  <button id="btn-sair-edicao">SAIR</button>

  <div class="app">
    <main class="quiz-container" id="quiz">
      <div class="top-row" style="width:100%">
        <div class="professor" id="professor" aria-hidden="true" ></div>

        <div class="quadro-fundo" role="region" aria-label="Quadro de perguntas">
          <div id="question" aria-live="polite"></div>
          <div id="answers" role="list"></div>
          <div class="feedback" id="feedback" aria-live="assertive"></div>

          <div class="controls" style="margin-top:8px">
            <button id="btn-voltar">◀ Voltar</button>
            <button id="btn-avancar">Avançar ▶</button>
            <button id="btn-terminar" style="flex:0 0 120px; background:#0b7f8f; border:none">Terminar</button>
          </div>
        </div>
      </div>
    </main>
  </div>

<script>
/* ================= PARTICULAS (leve) ================= */
const canvas = document.getElementById('particles'), ctx = canvas.getContext('2d');
function fitCanvas(){ canvas.width = window.innerWidth; canvas.height = window.innerHeight; }
fitCanvas(); window.addEventListener('resize', fitCanvas);
let mouse = {x:-9999, y:-9999};
window.addEventListener('mousemove', e => { mouse.x = e.clientX; mouse.y = e.clientY; });

class Particle {
  constructor(){
    this.x = Math.random()*canvas.width;
    this.y = Math.random()*canvas.height;
    this.r = Math.random()*1.6 + 0.6;
    this.vx = (Math.random()-0.5)*0.3;
    this.vy = (Math.random()-0.5)*0.3;
    this.alpha = Math.random()*0.6 + 0.2;
  }
  move(){
    this.x += this.vx; this.y += this.vy;
    if(this.x < 0 || this.x > canvas.width) this.vx *= -1;
    if(this.y < 0 || this.y > canvas.height) this.vy *= -1;
  }
  draw(){
    ctx.beginPath();
    ctx.fillStyle = `rgba(255,255,200,${this.alpha})`;
    ctx.arc(this.x, this.y, this.r, 0, Math.PI*2);
    ctx.fill();
  }
}
const particles = Array.from({length:48}, ()=> new Particle());
function animParticles(){
  ctx.clearRect(0,0,canvas.width,canvas.height);
  for(const p of particles){ p.move(); p.draw(); }
  requestAnimationFrame(animParticles);
}
animParticles();

/* ================= IMAGENS & ELEMENTOS ================= */
const imgFrames = [
  "https://uploads.onecompiler.io/444jywmud/444jyqxv3/professora%20frame%201.png",
  "https://uploads.onecompiler.io/444jywmud/444jyqxv3/professora%20frame%202.png",
  "https://uploads.onecompiler.io/444jywmud/444jyqxv3/professora%20frame%203.png"
];
const imgCerta = "https://uploads.onecompiler.io/444jywmud/444jyqxv3/joinhaa.png";
const imgErrada = "https://uploads.onecompiler.io/444jywmud/444jyqxv3/errada.png";

const startBtn = document.getElementById('start-btn');
const telaInicial = document.getElementById('tela-inicial');
const quizEl = document.getElementById('quiz');
const professorEl = document.getElementById('professor');
const questionEl = document.getElementById('question');
const answersEl = document.getElementById('answers');
const feedbackEl = document.getElementById('feedback');

const btnAvancar = document.getElementById('btn-avancar');
const btnVoltar  = document.getElementById('btn-voltar');
const btnTerminar = document.getElementById('btn-terminar');

/* ============== ESTADO ============== */
let perguntas = [];           // array de perguntas {pergunta, opcoes:[], certa}
let indice = 0;
let pontuacao = 0;
let escreverVelocidade = 40;
let perguntasRespondidas = {}; // { indice: { choice: n, correct: bool } }

/* ============== UTIL: salvar / carregar perguntas ============== */
function salvarPerguntas(){
  try{ localStorage.setItem('perguntasQuiz', JSON.stringify(perguntas)); }catch(e){}
}
function carregarPerguntas(){
  try{
    const raw = localStorage.getItem('perguntasQuiz');
    if(raw) perguntas = JSON.parse(raw);
  }catch(e){ perguntas = []; }
}
carregarPerguntas();

/* ============== PAINEL PROFESSOR ============== */
const btnEntrar = document.getElementById('btn-entrar');
const boxCadastro = document.getElementById('cadastro-perguntas');
const btnAdicionar = document.getElementById('btn-adicionar');
const btnSair = document.getElementById('btn-sair-edicao');

btnEntrar.addEventListener('click', ()=>{
  const senha = document.getElementById('senha-professor').value;
  if(senha === '2702'){
    boxCadastro.style.display = 'block';
    btnSair.style.display = 'block';
    document.getElementById('professor-login').style.display = 'none';
  } else alert('Senha incorreta');
});
btnSair.addEventListener('click', ()=>{
  boxCadastro.style.display = 'none';
  btnSair.style.display = 'none';
  document.getElementById('professor-login').style.display = 'flex';
  document.getElementById('senha-professor').value = '';
});

/* Adicionar pergunta */
btnAdicionar.addEventListener('click', ()=>{
  const p = document.getElementById('nova-pergunta').value.trim();
  const a1 = document.getElementById('alt1').value.trim();
  const a2 = document.getElementById('alt2').value.trim();
  const a3 = document.getElementById('alt3').value.trim();
  const c = parseInt(document.getElementById('certa').value);
  if(!p || !a1 || !a2 || !a3){ return alert('Preencha todos os campos!'); }
  perguntas.push({pergunta:p, opcoes:[a1,a2,a3], certa:c});
  document.getElementById('nova-pergunta').value='';
  document.getElementById('alt1').value=''; document.getElementById('alt2').value=''; document.getElementById('alt3').value='';
  salvarPerguntas(); atualizarCadastro();
});

/* Atualiza lista no painel professor (simples) */
function atualizarCadastro(){
  // limpa e recria
  const box = document.getElementById('cadastro-perguntas');
  box.querySelectorAll('.pergunta-item')?.forEach(x=>x.remove());
  perguntas.forEach((p,i)=>{
    const d = document.createElement('div');
    d.className = 'pergunta-item';
    d.style.border = '1px solid rgba(255,255,255,0.08)';
    d.style.padding = '6px';
    d.style.margin = '6px 0';
    d.style.borderRadius = '8px';
    d.style.cursor = 'pointer';
    d.textContent = `${i+1}. ${p.pergunta}`;
    d.addEventListener('click', ()=>{
      document.getElementById('nova-pergunta').value = p.pergunta;
      document.getElementById('alt1').value = p.opcoes[0];
      document.getElementById('alt2').value = p.opcoes[1];
      document.getElementById('alt3').value = p.opcoes[2];
      document.getElementById('certa').value = p.certa;
      perguntas.splice(i,1);
      salvarPerguntas(); atualizarCadastro();
    });
    box.appendChild(d);
  });
}
atualizarCadastro();

/* ============== HELPERS: escrever no quadro ============== */
let escreverInterval = null;
function escreverNoQuadro(el, texto){
  return new Promise(resolve=>{
    if(escreverInterval) clearInterval(escreverInterval);
    el.textContent = '';
    let i=0, frameIndex=0;
    escreverInterval = setInterval(()=>{
      el.textContent += texto[i] || '';
      // anima professora trocando frames
      professorEl.style.backgroundImage = `url(${imgFrames[frameIndex]})`;
      frameIndex = (frameIndex+1) % imgFrames.length;
      i++;
      if(i>=texto.length){
        clearInterval(escreverInterval);
        escreverInterval = null;
        professorEl.style.backgroundImage = `url(${imgFrames[0]})`;
        resolve();
      }
    }, escreverVelocidade);
  });
}

/* ============== RENDER: mostrarPergunta ============== */
async function mostrarPergunta(){
  if(!perguntas.length){ questionEl.textContent = 'Sem perguntas. Entre com o professor.'; answersEl.innerHTML=''; feedbackEl.textContent=''; return; }
  const q = perguntas[indice];
  answersEl.innerHTML = '';
  feedbackEl.textContent = '';
  // escreve a pergunta
  await escreverNoQuadro(questionEl, q.pergunta);

  // cria botoes
  q.opcoes.forEach((op,i)=>{
    const b = document.createElement('button');
    b.type='button';
    b.textContent = op;
    b.dataset.index = i;
    // se já respondeu essa pergunta
    const saved = perguntasRespondidas[indice];
    if(saved){
      b.disabled = true;
      if(saved.choice == i){
        b.classList.add('selecionada');
        if(saved.correct) b.classList.add('correta'); else b.classList.add('errada');
      }
    } else {
      b.addEventListener('click', ()=> checkAnswer(i === q.certa, i) );
    }
    answersEl.appendChild(b);
  });

  // mostra feedback se já respondida
  const sav = perguntasRespondidas[indice];
  if(sav){
    if(sav.correct){
      feedbackEl.textContent = 'Muito bem!'; feedbackEl.className = 'feedback correct';
      professorEl.style.backgroundImage = `url(${imgCerta})`;
    } else {
      feedbackEl.textContent = 'Tente novamente!'; feedbackEl.className = 'feedback wrong';
      professorEl.style.backgroundImage = `url(${imgErrada})`;
    }
  } else {
    feedbackEl.textContent = ''; feedbackEl.className = 'feedback';
    professorEl.style.backgroundImage = `url(${imgFrames[0]})`;
  }
}

/* ============== checkAnswer ============== */
function desativarRespostasAtuais(){
  answersEl.querySelectorAll('button').forEach(b=> b.disabled = true);
}

function checkAnswer(certa, choiceIndex){
  perguntasRespondidas[indice] = { choice: choiceIndex, correct: certa };
  desativarRespostasAtuais();

  // marca visualmente
  answersEl.querySelectorAll('button').forEach(b=>{
    const idx = Number(b.dataset.index);
    if(idx === choiceIndex){
      b.classList.add('selecionada');
      if(certa) b.classList.add('correta'); else b.classList.add('errada');
    }
  });

  if(certa){
    pontuacao++;
    feedbackEl.textContent = 'Muito bem!'; feedbackEl.className = 'feedback correct';
    professorEl.style.backgroundImage = `url(${imgCerta})`;
    professorEl.style.animation = 'none';
    setTimeout(()=> professorEl.style.animation = '', 700);
  } else {
    feedbackEl.textContent = 'Tente novamente!'; feedbackEl.className = 'feedback wrong';
    professorEl.style.backgroundImage = `url(${imgErrada})`;
    professorEl.style.animation = 'none';
    setTimeout(()=> professorEl.style.animation = '', 500);
  }
}

/* ============== START / NAV / END ============== */
startBtn.addEventListener('click', ()=>{
  if(perguntas.length === 0) return alert('Adicione pelo menos uma pergunta no painel do professor.');
  telaInicial.style.opacity = 0;
  setTimeout(()=> telaInicial.style.display = 'none', 260);
  quizEl.style.display = 'flex';
  professorEl.style.backgroundImage = `url(${imgFrames[0]})`;
  mostrarPergunta();
});

btnAvancar.addEventListener('click', ()=>{
  if(indice < perguntas.length - 1){ indice++; mostrarPergunta(); }
});
btnVoltar.addEventListener('click', ()=>{
  if(indice > 0){ indice--; mostrarPergunta(); }
});
btnTerminar.addEventListener('click', mostrarFim);

/* ============== MOSTRAR FIM ============== */
function mostrarFim(){
  quizEl.style.display = 'none';
  const fim = document.createElement('div');
  fim.style.position = 'fixed';
  fim.style.inset = 0;
  fim.style.display = 'flex';
  fim.style.flexDirection = 'column';
  fim.style.justifyContent = 'center';
  fim.style.alignItems = 'center';
  fim.style.background = "linear-gradient(180deg, rgba(0,0,0,0.7), rgba(0,0,0,0.9))";
  fim.style.color = '#fff';
  fim.style.zIndex = 9999;
  fim.innerHTML = `<div style="font-size:20px; text-align:center">Quiz finalizado!<br><b>${pontuacao} de ${perguntas.length}</b></div>`;

  const bt = document.createElement('button');
  bt.textContent = 'Reiniciar';
  bt.style.marginTop = '20px';
  bt.style.padding = '12px 18px';
  bt.style.borderRadius = '12px';
  bt.style.border = 'none';
  bt.style.background = '#0b7f8f';
  bt.style.color = '#fff';
  bt.addEventListener('click', ()=>{
    document.body.removeChild(fim);
    resetarJogo();
  });
  fim.appendChild(bt);
  document.body.appendChild(fim);
}

/* ============== RESETAR ============== */
function resetarJogo(){
  perguntasRespondidas = {};
  indice = 0; pontuacao = 0;
  questionEl.textContent = ''; answersEl.innerHTML = ''; feedbackEl.textContent = '';
  telaInicial.style.display = 'flex';
  telaInicial.style.opacity = 1;
  quizEl.style.display = 'none';
  professorEl.style.backgroundImage = `url(${imgFrames[0]})`;
}

/* ============== ACESSIBILIDADE / INIT ============== */
window.addEventListener('load', ()=>{
  // se não tiver perguntas, adiciona exemplo para teste
  if(!perguntas.length){
    perguntas = [
      { pergunta: "Qual é a capital do Brasil?", opcoes:["São Paulo","Rio de Janeiro","Brasília"], certa:2 },
      { pergunta: "2 + 2 = ?", opcoes:["3","4","5"], certa:1 },
      { pergunta: "Água é composta por?", opcoes:["H2O","CO2","O2"], certa:0 }
    ];
    salvarPerguntas();
    atualizarCadastro();
  } else {
    atualizarCadastro();
  }
});

/* permite fechar painel com ESC */
document.addEventListener('keydown', e=>{
  if(e.key === 'Escape'){ boxCadastro.style.display = 'none'; btnSair.style.display = 'none'; document.getElementById('professor-login').style.display = 'flex'; }
});
</script>
</body>
</html>
