<!-- ======= CUADERNO: Semana 01 | Estudiante: Huamán Rojas Jhordan Armando ======= -->

<style>
:root{
  --bg: #f8fafc;
  --ink:#1f2937;
  --brand:#6d28d9;
  --brand-2:#22d3ee;
  --paper:#fffef9;
  --line:#e9eef5;
  --ring:#b48ede;
  --card:#ffffff;
  --muted:#6b7280;
  --ok:#10b981; --pend:#f59e0b; --no:#ef4444;
  --shadow: 0 10px 30px rgba(17,24,39,.15);
}
@media (prefers-color-scheme: dark){
  :root{
    --bg:#0b1020; --ink:#f1f5f9; --paper:#0f172a;
    --line:#17223b; --card:#0e162c; --shadow: 0 10px 30px rgba(0,0,0,.45);
  }
}
*{box-sizing:border-box}
body{background:var(--bg); color:var(--ink);}

.notebook{
  max-width: 980px; margin: 34px auto; padding:28px;
  background:
    repeating-linear-gradient(#0000 0 31px, var(--line) 31px 32px),
    var(--paper);
  border: 2px solid #d6d3e8;
  border-radius: 22px;
  box-shadow: var(--shadow);
  position: relative;
}

/* Margen izquierda tipo cuaderno */
.notebook::before{
  content:"";
  position:absolute; inset:0 0 0 0;
  background:
    linear-gradient(90deg,#0000 54px,#fca5a5 55px,#0000 56px);
  border-radius:20px;
  pointer-events:none;
}

/* Espiral */
.spiral{
  position:absolute; top:18px; left:10px; height: calc(100% - 36px);
  width:42px; display:flex; flex-direction:column; gap:14px;
}
.ring{
  margin-left:8px; width:26px; height:14px; border:3px solid var(--ring);
  border-radius:10px; background: radial-gradient(circle at 60% 50%, #eee4ff 0 35%, #0000 36%) ;
  box-shadow: inset 0 0 0 2px #0000, 0 1px 0 rgba(255,255,255,.35);
}

/* Portada */
.cover{
  margin-left:46px; padding:22px 26px;
  border-radius:18px;
  background: linear-gradient(135deg, rgba(109,40,217,.18), rgba(34,211,238,.14));
  border:1px solid rgba(125,125,200,.35);
}
.title{
  font-size: clamp(28px, 4vw, 40px);
  font-weight: 800; letter-spacing:.3px;
  display:flex; align-items:center; gap:12px;
}
.badge{
  display:inline-flex; align-items:center; gap:8px;
  margin-top:10px; padding:10px 14px; border-radius:12px;
  background: linear-gradient(90deg, rgba(34,211,238,.18), rgba(109,40,217,.18));
  border: 1px solid rgba(255,255,255,.2);
  font-weight:700;
}

/* Animación typing */
.typing{
  position: relative; display:inline-block; white-space:nowrap; overflow:hidden;
  border-right: 3px solid var(--brand-2);
  width: 0;
  animation: typing 2.7s steps(30,end) forwards, blink 1s step-end infinite;
}
@keyframes typing{ to{ width: 100%; } }
@keyframes blink{ 50%{ border-color: transparent; } }

/* Secciones/tarjetas */
.section{
  margin:22px 0 0 46px;
  background: var(--card);
  border:1px solid rgba(140,140,200,.25);
  border-left: 6px solid var(--brand);
  border-radius:16px;
  padding:18px 22px;
  box-shadow: var(--shadow);
}
.section h2{
  margin:0 0 10px 0; font-size:22px; display:flex; align-items:center; gap:10px;
}
.hr{ height:1px; background:linear-gradient(90deg,#0000,rgba(125,125,200,.5),#0000); margin:18px 0; }

ul{ margin:8px 0 0 2px }
li + li{ margin-top:6px }

.note{
  background: linear-gradient(180deg, rgba(34,211,238,.12), rgba(109,40,217,.12));
  border:1px dashed rgba(109,40,217,.45);
  padding:12px 14px; border-radius:12px; margin-top:8px;
}

.table{
  width:100%; border-collapse:separate; border-spacing:0; overflow:hidden;
  border-radius:14px; border:1px solid rgba(140,140,200,.25);
}
.table thead th{
  padding:12px 14px; text-align:left; background:linear-gradient(180deg, rgba(34,211,238,.18), rgba(109,40,217,.18));
  font-weight:800;
}
.table tbody td{ padding:12px 14px; border-top:1px solid rgba(140,140,200,.25); }
.status{ font-weight:700; padding:.2em .5em; border-radius:8px; }
.ok{ background:rgba(16,185,129,.18); color:var(--ok); }
.pend{ background:rgba(245,158,11,.18); color:var(--pend); }
.no{ background:rgba(239,68,68,.18); color:var(--no); }

.footer{
  margin: 26px 0 2px 46px; text-align:center; color:var(--muted);
  font-style:italic;
}

/* entrada suave */
.fade-in{ animation: fade .9s ease both; }
@keyframes fade{ from{opacity:0; transform:translateY(6px)} to{opacity:1; transform:none} }
</style>

<div class="notebook">

  <div class="spiral" aria-hidden="true">
    <span class="ring"></span><span class="ring"></span><span class="ring"></span>
    <span class="ring"></span><span class="ring"></span><span class="ring"></span>
    <span class="ring"></span><span class="ring"></span><span class="ring"></span>
    <span class="ring"></span><span class="ring"></span><span class="ring"></span>
  </div>

  <div class="cover fade-in">
    <div class="title">📒 <span class="typing">Semana 01</span></div>
    <div class="badge">✍️ Estudiante: <strong>Huamán Rojas Jhordan Armando</strong></div>
  </div>

  <div class="section fade-in">
    <h2>🗂️ Agenda de la semana</h2>
    <div class="hr"></div>
    <ul>
      <li>[ ] Tema 1: Introducción</li>
      <li>[ ] Tema 2: Desarrollo</li>
      <li>[ ] Tema 3: Conclusiones</li>
    </ul>
  </div>

  <div class="section fade-in">
    <h2>📝 Notas importantes</h2>
    <div class="hr"></div>
    <div class="note">
      ✨ Aquí puedes escribir tus apuntes principales. <br>
      📌 Usa listas, citas y <strong>negritas</strong> para resaltar.
    </div>
  </div>

  <div class="section fade-in">
    <h2>📊 Resumen</h2>
    <div class="hr"></div>
    <table class="table">
      <thead><tr><th>Día</th><th>Actividad realizada</th><th>Estado</th></tr></thead>
      <tbody>
        <tr><td>Lunes</td><td>Revisión de teoría</td><td><span class="status ok">Completado</span></td></tr>
        <tr><td>Martes</td><td>Ejercicios prácticos</td><td><span class="status pend">En proceso</span></td></tr>
        <tr><td>Miércoles</td><td>Reunión de retroalimentación</td><td><span class="status no">Pendiente</span></td></tr>
      </tbody>
    </table>
  </div>

  <div class="footer">🖋️ Fin de la semana 01</div>
</div>
