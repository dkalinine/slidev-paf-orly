---
theme: default
title: DPAF Orly
transition: fade
mdc: true
class: text-white
---

<style>
:root {
  --bg-1: #06101d;
  --bg-2: #0d1d33;
  --bg-3: #133055;
  --line: rgba(255,255,255,0.10);
  --text: #eef4ff;
  --muted: #9db0c8;
  --accent: #6cc6ff;
  --accent-2: #8ea2ff;
  --glass: rgba(255,255,255,0.07);
}

.slidev-layout {
  color: var(--text);
  background:
    radial-gradient(circle at 15% 20%, rgba(108,198,255,.14), transparent 22%),
    radial-gradient(circle at 85% 12%, rgba(142,162,255,.12), transparent 24%),
    linear-gradient(135deg, var(--bg-1), var(--bg-2) 55%, var(--bg-3));
}

.fade-up-enter-active,
.fade-up-leave-active {
  transition: all .6s cubic-bezier(.22,1,.36,1);
}
.fade-up-enter-from,
.fade-up-leave-to {
  opacity: 0;
  transform: translateY(24px) scale(.985);
  filter: blur(10px);
}

.slidev-vclick-target {
  transition: all .45s cubic-bezier(.22,1,.36,1);
}
.slidev-vclick-hidden {
  opacity: 0;
  transform: translateY(18px);
  filter: blur(8px);
  pointer-events: none;
}

.hero,
.full-center {
  min-height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.full-center {
  align-items: center;
  text-align: center;
}

.rel {
  position: relative;
  overflow: hidden;
}

.orb {
  position: absolute;
  border-radius: 999px;
  filter: blur(34px);
  opacity: .42;
}
.orb.a {
  width: 240px;
  height: 240px;
  right: 8%;
  top: 10%;
  background: #4cc4ff;
}
.orb.b {
  width: 180px;
  height: 180px;
  left: 6%;
  bottom: 10%;
  background: #7887ff;
}

.kicker {
  text-transform: uppercase;
  letter-spacing: .24em;
  font-size: 13px;
  color: var(--muted);
  margin-bottom: 18px;
}

.title-xl {
  font-size: 62px;
  line-height: 1.02;
  font-weight: 800;
  max-width: 980px;
  margin: 0;
}

.title-lg {
  font-size: 48px;
  line-height: 1.06;
  font-weight: 800;
  margin: 0;
}

.subtitle {
  margin-top: 22px;
  max-width: 760px;
  font-size: 22px;
  line-height: 1.45;
  color: var(--muted);
}

.shimmer {
  background: linear-gradient(90deg, #ffffff, #8fd7ff, #b7c6ff, #ffffff);
  background-size: 220% auto;
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  animation: shimmer 7s linear infinite;
}

.grid-2 {
  display: grid;
  grid-template-columns: 1.15fr .85fr;
  gap: 28px;
  align-items: center;
}

.card {
  background: var(--glass);
  border: 1px solid var(--line);
  border-radius: 26px;
  padding: 26px;
  backdrop-filter: blur(14px);
  box-shadow: 0 18px 50px rgba(0,0,0,.28);
}

.kpi-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}

.kpi {
  border-radius: 20px;
  padding: 18px;
  background: rgba(255,255,255,.05);
  border: 1px solid var(--line);
}

.kpi-num {
  font-size: 40px;
  line-height: 1;
  font-weight: 800;
}

.kpi-label {
  margin-top: 8px;
  font-size: 13px;
  letter-spacing: .08em;
  text-transform: uppercase;
  color: var(--muted);
}

.big-number {
  font-size: 120px;
  line-height: .95;
  font-weight: 900;
  margin: 0;
}

.big-sub {
  margin-top: 16px;
  font-size: 24px;
  color: var(--muted);
  letter-spacing: .08em;
  text-transform: uppercase;
}

.balance {
  display: grid;
  grid-template-columns: 1fr 120px 1fr;
  gap: 20px;
  align-items: center;
  margin-top: 30px;
}

.pillar {
  border-radius: 26px;
  padding: 34px;
  text-align: center;
  font-size: 34px;
  font-weight: 800;
  border: 1px solid var(--line);
  background: rgba(255,255,255,.06);
  box-shadow: 0 10px 30px rgba(0,0,0,.18);
}

.vs {
  text-align: center;
  font-size: 30px;
  font-weight: 900;
  color: var(--accent);
  letter-spacing: .08em;
}

.flow {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
  margin-top: 26px;
}

.step {
  border-radius: 22px;
  padding: 24px;
  background: rgba(255,255,255,.06);
  border: 1px solid var(--line);
  min-height: 210px;
}

.step-n {
  font-size: 12px;
  letter-spacing: .18em;
  color: var(--accent);
  text-transform: uppercase;
  margin-bottom: 10px;
}

.step-t {
  font-size: 26px;
  font-weight: 800;
  margin-bottom: 8px;
}

.step-p {
  color: var(--muted);
  line-height: 1.45;
  font-size: 17px;
}

.list-premium {
  display: grid;
  gap: 14px;
  margin-top: 24px;
}

.list-item {
  padding: 18px 20px;
  border-radius: 18px;
  border: 1px solid var(--line);
  background: rgba(255,255,255,.05);
  font-size: 24px;
  font-weight: 700;
}

.final-box {
  padding: 38px 44px;
  border-radius: 30px;
  border: 1px solid var(--line);
  background: rgba(255,255,255,.06);
  box-shadow: 0 18px 50px rgba(0,0,0,.28);
}

@keyframes shimmer {
  to { background-position: 220% center; }
}
</style>

<div class="hero rel">
  <div class="orb a"></div>
  <div class="orb b"></div>
  <div class="kicker">Police aux Frontières · Orly</div>
  <h1 class="title-xl shimmer">Organisation du contrôle transfrontière</h1>
  <div class="subtitle">
    Une lecture visuelle et cinématique de la mission : pression, arbitrage, adaptation.
  </div>
</div>

---
transition: fade-up
---

<div class="full-center">
  <div
    v-motion
    :initial="{ opacity: 0, y: 40, scale: 0.96 }"
    :enter="{ opacity: 1, y: 0, scale: 1, transition: { duration: 800 } }"
  >
    <h1 class="big-number shimmer">13 M</h1>
    <div class="big-sub">de passagers contrôlés par an</div>
  </div>
</div>

---
transition: fade-up
---

<div class="grid-2">
  <div>
    <div class="kicker">Constat</div>
    <h1 class="title-lg">Une mission sous tension permanente</h1>
    <div class="subtitle">
      Variabilité du trafic, concentration des pics, contrainte de temps et exigence de sécurité maximale.
    </div>
  </div>

  <div
    class="card"
    v-motion
    :initial="{ opacity: 0, x: 60 }"
    :enter="{ opacity: 1, x: 0, transition: { duration: 700 } }"
  >
    <div class="kpi-grid">
      <div class="kpi">
        <div class="kpi-num">4</div>
        <div class="kpi-label">Lignes frontières</div>
      </div>
      <div class="kpi">
        <div class="kpi-num">24/7</div>
        <div class="kpi-label">Pression opérationnelle</div>
      </div>
      <div class="kpi">
        <div class="kpi-num">T0</div>
        <div class="kpi-label">Décision temps réel</div>
      </div>
    </div>
  </div>
</div>

---
transition: fade-up
---

<div>
  <div class="kicker">Enjeu central</div>
  <h1 class="title-lg">Trouver l’équilibre</h1>

  <div class="balance">
    <div class="pillar" v-click>🔒 Sécurité</div>
    <div class="vs" v-click>VS</div>
    <div class="pillar" v-click>🚶 Fluidité</div>
  </div>

  <div class="subtitle" v-after>
    Toute la difficulté réside dans la capacité à absorber le flux sans affaiblir la qualité du contrôle.
  </div>
</div>

---
transition: fade-up
---

<div>
  <div class="kicker">Complexité opérationnelle</div>
  <h1 class="title-lg">Des temps de contrôle hétérogènes</h1>

  <div class="list-premium">
    <div class="list-item" v-click>Union européenne · contrôle rapide</div>
    <div class="list-item" v-click>Pays tiers non éligibles EES · contrôle plus long</div>
    <div class="list-item" v-click>Pays tiers éligibles EES · contrôle renforcé</div>
    <div class="list-item" v-click>Familles avec mineurs · traitement plus complexe</div>
  </div>
</div>

---
transition: fade-up
---

<div>
  <div class="kicker">Risque</div>
  <h1 class="title-lg">Une ressource contrainte face à des pics irréguliers</h1>

  <div class="list-premium">
    <div class="list-item" v-click>Effectifs limités</div>
    <div class="list-item" v-click>Rigidité relative de l’organisation horaire</div>
    <div class="list-item" v-click>Variabilité forte selon les vols et créneaux</div>
  </div>
</div>

---
transition: fade-up
---

<div>
  <div class="kicker">Réponse opérationnelle</div>
  <h1 class="title-lg">Adapter, piloter, réallouer</h1>

  <div class="flow">
    <div class="step" v-click>
      <div class="step-n">01</div>
      <div class="step-t">Observer</div>
      <div class="step-p">Lire le flux, détecter le pic, mesurer la tension opérationnelle.</div>
    </div>

   <div class="step" v-click>
      <div class="step-n">02</div>
      <div class="step-t">Décider</div>
      <div class="step-p">Ouvrir, fermer, prioriser et adapter l’emploi des ressources disponibles.</div>
    </div>

   <div class="step" v-click>
      <div class="step-n">03</div>
      <div class="step-t">Réallouer</div>
      <div class="step-p">Aubettes, PARAFE, supervision et coordination terrain en temps réel.</div>
    </div>
  </div>
</div>

---
transition: fade-up
---

<div>
  <div class="kicker">Facteurs de succès</div>
  <h1 class="title-lg">Trois leviers décisifs</h1>

  <div class="list-premium">
    <div class="list-item" v-click>Anticipation</div>
    <div class="list-item" v-click>Coordination interservices</div>
    <div class="list-item" v-click>Réactivité opérationnelle</div>
  </div>
</div>

---
transition: fade-up
---

<div class="full-center">
  <div class="final-box">
    <div class="kicker">Message final</div>
    <h1 class="title-lg" style="max-width: 900px;">
      La performance repose sur l’organisation, l’anticipation et la capacité d’adaptation.
    </h1>
  </div>
</div>
