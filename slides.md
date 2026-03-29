---
theme: default
title: DPAF Orly
transition: fade
mdc: true
---

<style>
/* === Fonts Marianne (embarquées localement) === */
@font-face {
  font-family: 'Marianne';
  src: url('/fonts/Marianne-Light.woff2') format('woff2');
  font-weight: 300;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Marianne';
  src: url('/fonts/Marianne-Regular.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Marianne';
  src: url('/fonts/Marianne-Medium.woff2') format('woff2');
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Marianne';
  src: url('/fonts/Marianne-Bold.woff2') format('woff2');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

/* === Variables DSFR === */
:root {
  --blue-france: #000091;
  --red-marianne: #e1000f;
  --bg-primary: #ffffff;
  --bg-alt: #f6f6f6;
  --bg-contrast: #e5e5e5;
  --text-primary: #161616;
  --text-secondary: #666666;
  --text-inverted: #ffffff;
  --border-default: #e5e5e5;
  --border-active: #000091;
  --shadow-sm: 0 2px 6px rgba(0,0,9,0.08);
  --shadow-md: 0 6px 18px rgba(0,0,9,0.12);
  --shadow-lg: 0 12px 32px rgba(0,0,9,0.16);
}

/* === Base Slidev === */
.slidev-layout,
.slidev-layout * {
  font-family: 'Marianne', arial, sans-serif;
}

.slidev-layout {
  color: var(--text-primary);
  background: var(--bg-primary);
}

/* Bande tricolore en haut de chaque slide */
.slidev-layout::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg,
    var(--blue-france) 0%, var(--blue-france) 33%,
    var(--bg-primary) 33%, var(--bg-primary) 66%,
    var(--red-marianne) 66%, var(--red-marianne) 100%
  );
  z-index: 10;
}

/* === Animations === */
.fade-up-enter-active,
.fade-up-leave-active {
  transition: all .5s cubic-bezier(.22,1,.36,1);
}
.fade-up-enter-from,
.fade-up-leave-to {
  opacity: 0;
  transform: translateY(20px);
}

.slidev-vclick-target {
  transition: all .4s cubic-bezier(.22,1,.36,1);
}
.slidev-vclick-hidden {
  opacity: 0;
  transform: translateY(14px);
  pointer-events: none;
}

/* === Composants de présentation DSFR === */

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

.kicker {
  text-transform: uppercase;
  letter-spacing: .2em;
  font-size: 13px;
  font-weight: 700;
  color: var(--red-marianne);
  margin-bottom: 16px;
}

.title-xl {
  font-size: 56px;
  line-height: 1.08;
  font-weight: 700;
  max-width: 920px;
  margin: 0;
  color: var(--blue-france);
}

.title-lg {
  font-size: 44px;
  line-height: 1.1;
  font-weight: 700;
  margin: 0;
  color: var(--text-primary);
}

.subtitle {
  margin-top: 20px;
  max-width: 760px;
  font-size: 20px;
  line-height: 1.5;
  color: var(--text-secondary);
}

.grid-2 {
  display: grid;
  grid-template-columns: 1.15fr .85fr;
  gap: 32px;
  align-items: center;
}

.card {
  background: var(--bg-alt);
  border: 1px solid var(--border-default);
  border-radius: 8px;
  padding: 24px;
  box-shadow: var(--shadow-md);
}

.kpi-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 14px;
}

.kpi {
  border-radius: 8px;
  padding: 16px;
  background: var(--bg-primary);
  border: 1px solid var(--border-default);
}

.kpi-num {
  font-size: 36px;
  line-height: 1;
  font-weight: 700;
  color: var(--blue-france);
}

.kpi-label {
  margin-top: 6px;
  font-size: 12px;
  letter-spacing: .06em;
  text-transform: uppercase;
  color: var(--text-secondary);
}

.big-number {
  font-size: 110px;
  line-height: .95;
  font-weight: 700;
  margin: 0;
  color: var(--blue-france);
}

.big-sub {
  margin-top: 14px;
  font-size: 22px;
  color: var(--text-secondary);
  letter-spacing: .06em;
  text-transform: uppercase;
}

.balance {
  display: grid;
  grid-template-columns: 1fr 100px 1fr;
  gap: 20px;
  align-items: center;
  margin-top: 28px;
}

.pillar {
  border-radius: 8px;
  padding: 32px;
  text-align: center;
  font-size: 30px;
  font-weight: 700;
  border: 2px solid var(--blue-france);
  background: var(--bg-alt);
  box-shadow: var(--shadow-sm);
  color: var(--blue-france);
}

.vs {
  text-align: center;
  font-size: 28px;
  font-weight: 700;
  color: var(--red-marianne);
  letter-spacing: .06em;
}

.flow {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-top: 24px;
}

.step {
  border-radius: 8px;
  padding: 22px;
  background: var(--bg-alt);
  border: 1px solid var(--border-default);
  border-top: 3px solid var(--blue-france);
  min-height: 200px;
}

.step-n {
  font-size: 12px;
  letter-spacing: .16em;
  color: var(--blue-france);
  text-transform: uppercase;
  margin-bottom: 10px;
  font-weight: 700;
}

.step-t {
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 8px;
  color: var(--text-primary);
}

.step-p {
  color: var(--text-secondary);
  line-height: 1.5;
  font-size: 16px;
}

.list-premium {
  display: grid;
  gap: 12px;
  margin-top: 22px;
}

.list-item {
  padding: 16px 20px;
  border-radius: 8px;
  border: 1px solid var(--border-default);
  border-left: 4px solid var(--blue-france);
  background: var(--bg-alt);
  font-size: 22px;
  font-weight: 500;
  color: var(--text-primary);
}

.final-box {
  padding: 36px 40px;
  border-radius: 8px;
  border: 2px solid var(--blue-france);
  background: var(--bg-alt);
  box-shadow: var(--shadow-lg);
}

.final-box .title-lg {
  color: var(--blue-france);
}
</style>

<div class="hero">
  <div style="display: flex; align-items: center; gap: 20px; margin-bottom: 20px;">
    <img src="/logo-ministere-interieur.png" style="height: 80px;" alt="Ministère de l'Intérieur" />
    <img src="/logo-paf.png" style="height: 70px;" alt="PAF" />
  </div>
  <div class="kicker">Police aux Frontières · Orly</div>
  <h1 class="title-xl">Organisation du contrôle transfrontière</h1>
  <div class="subtitle">
    Une lecture visuelle de la mission : pression, arbitrage, adaptation.
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
    <h1 class="big-number">13 M</h1>
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
  <h1 class="title-lg">Trouver l'équilibre</h1>
  <div class="balance">
    <div class="pillar" v-click>Sécurité</div>
    <div class="vs" v-click>VS</div>
    <div class="pillar" v-click>Fluidité</div>
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
    <div class="list-item" v-click>Rigidité relative de l'organisation horaire</div>
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
      <div class="step-p">Ouvrir, fermer, prioriser et adapter l'emploi des ressources disponibles.</div>
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
      La performance repose sur l'organisation, l'anticipation et la capacité d'adaptation.
    </h1>
  </div>
</div>
