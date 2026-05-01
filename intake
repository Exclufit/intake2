<!DOCTYPE html>
<html lang="nl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Intakekaart — ExcluFit</title>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,300;0,600;1,300;1,600&family=Instrument+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #0f0f0f;
  --surface: #1a1a1a;
  --surface2: #222222;
  --border: #2e2e2e;
  --border2: #3a3a3a;
  --text: #e8e2d9;
  --muted: #7a7570;
  --accent: #d4a853;
  --accent2: #e8c47a;
  --green: #5a9a6a;
  --green-bg: rgba(90,154,106,0.08);
  --red: #c0504a;
  --red-bg: rgba(192,80,74,0.08);
  --blue: #4a7ab0;
  --radius: 10px;
}

* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'Instrument Sans', sans-serif;
  background: var(--bg);
  color: var(--text);
  min-height: 100vh;
  font-size: 14px;
  line-height: 1.6;
}

/* HEADER */
header {
  padding: 40px 40px 32px;
  border-bottom: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  flex-wrap: wrap;
  gap: 16px;
}
.header-left .logo {
  font-size: 11px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--accent);
  font-weight: 600;
  margin-bottom: 8px;
}
header h1 {
  font-family: 'Fraunces', serif;
  font-size: clamp(26px, 4vw, 38px);
  font-weight: 300;
  color: var(--text);
  line-height: 1.1;
}
header h1 em {
  font-style: italic;
  color: var(--accent);
}
header p {
  margin-top: 8px;
  color: var(--muted);
  font-size: 13px;
  max-width: 420px;
}
.header-meta {
  text-align: right;
  font-size: 12px;
  color: var(--muted);
}
.header-meta strong {
  display: block;
  color: var(--accent);
  font-size: 13px;
  margin-bottom: 2px;
}

/* PROGRESS */
.progress-bar {
  height: 3px;
  background: var(--border);
  position: sticky;
  top: 0;
  z-index: 100;
}
.progress-fill {
  height: 100%;
  background: linear-gradient(90deg, var(--accent), var(--accent2));
  transition: width 0.4s ease;
  width: 0%;
}

/* TABS */
.tab-nav {
  display: flex;
  border-bottom: 1px solid var(--border);
  padding: 0 40px;
  overflow-x: auto;
  scrollbar-width: none;
  background: var(--surface);
  position: sticky;
  top: 3px;
  z-index: 99;
}
.tab-nav::-webkit-scrollbar { display: none; }
.tab-btn {
  padding: 14px 20px 12px;
  font-family: 'Instrument Sans', sans-serif;
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 0.8px;
  text-transform: uppercase;
  color: var(--muted);
  background: none;
  border: none;
  border-bottom: 2px solid transparent;
  cursor: pointer;
  white-space: nowrap;
  transition: all 0.2s;
  display: flex;
  align-items: center;
  gap: 8px;
}
.tab-btn:hover { color: var(--text); }
.tab-btn.active { color: var(--accent); border-bottom-color: var(--accent); }
.tab-indicator {
  width: 6px; height: 6px;
  border-radius: 50%;
  background: var(--border2);
  transition: background 0.2s;
}
.tab-btn.filled .tab-indicator { background: var(--green); }
.tab-btn.active .tab-indicator { background: var(--accent); }

/* MAIN */
main {
  max-width: 860px;
  margin: 0 auto;
  padding: 36px 24px 80px;
}

/* SECTIONS */
.tab-section { display: none; }
.tab-section.active {
  display: block;
  animation: fadeIn 0.25s ease;
}
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(8px); }
  to { opacity: 1; transform: translateY(0); }
}

.section-title {
  font-family: 'Fraunces', serif;
  font-size: 22px;
  font-weight: 300;
  color: var(--text);
  margin-bottom: 4px;
}
.section-title em { font-style: italic; color: var(--accent); }
.section-sub {
  font-size: 13px;
  color: var(--muted);
  margin-bottom: 28px;
}

/* FORM ELEMENTS */
.form-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 14px;
  margin-bottom: 14px;
}
.form-grid.cols3 { grid-template-columns: 1fr 1fr 1fr; }
.form-grid.cols1 { grid-template-columns: 1fr; }

.field {
  display: flex;
  flex-direction: column;
  gap: 6px;
}
.field.span2 { grid-column: span 2; }
.field.span3 { grid-column: span 3; }

label {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: var(--muted);
}
label .req { color: var(--accent); margin-left: 2px; }

input[type="text"],
input[type="number"],
input[type="date"],
select,
textarea {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 6px;
  padding: 10px 14px;
  font-family: 'Instrument Sans', sans-serif;
  font-size: 13.5px;
  color: var(--text);
  transition: border-color 0.2s, box-shadow 0.2s;
  width: 100%;
  outline: none;
}
input:focus, select:focus, textarea:focus {
  border-color: var(--accent);
  box-shadow: 0 0 0 3px rgba(212,168,83,0.1);
}
textarea { resize: vertical; min-height: 80px; }
select option { background: var(--surface2); }

/* RANGE SLIDERS */
.range-group {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 16px 18px;
  margin-bottom: 14px;
}
.range-row {
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 8px 0;
  border-bottom: 1px solid var(--border);
}
.range-row:last-child { border-bottom: none; }
.range-label {
  font-size: 13px;
  color: var(--text);
  min-width: 160px;
  flex-shrink: 0;
}
.range-label small {
  display: block;
  font-size: 11px;
  color: var(--muted);
}
input[type="range"] {
  flex: 1;
  appearance: none;
  height: 4px;
  background: var(--border2);
  border-radius: 2px;
  border: none;
  padding: 0;
  cursor: pointer;
}
input[type="range"]::-webkit-slider-thumb {
  appearance: none;
  width: 16px; height: 16px;
  border-radius: 50%;
  background: var(--accent);
  cursor: pointer;
  box-shadow: 0 0 0 3px rgba(212,168,83,0.2);
}
.range-val {
  font-size: 14px;
  font-weight: 600;
  color: var(--accent);
  min-width: 28px;
  text-align: right;
}

/* DOMEIN CARDS */
.domein-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
  margin-bottom: 14px;
}
.domein-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 16px;
  border-left: 3px solid var(--border2);
  transition: border-color 0.2s;
}
.domein-card.d1 { border-left-color: #d4a853; }
.domein-card.d2 { border-left-color: #5a9a6a; }
.domein-card.d3 { border-left-color: #4a7ab0; }
.domein-card.d4 { border-left-color: #9a5ab0; }
.domein-card.d5 { border-left-color: #b05a5a; }
.domein-card.d6 { border-left-color: #5a8ab0; }

.domein-num {
  font-size: 10px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--muted);
  margin-bottom: 4px;
}
.domein-card h4 {
  font-size: 13px;
  font-weight: 600;
  color: var(--text);
  margin-bottom: 10px;
}
.domein-card textarea {
  font-size: 12.5px;
  min-height: 70px;
  background: var(--surface2);
  border-color: var(--border);
}

/* CHECKBOXES */
.check-group {
  display: flex;
  flex-direction: column;
  gap: 8px;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 14px 16px;
  margin-bottom: 14px;
}
.check-group-title {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: var(--muted);
  margin-bottom: 6px;
  border-bottom: 1px solid var(--border);
  padding-bottom: 8px;
}
.check-item {
  display: flex;
  align-items: flex-start;
  gap: 10px;
  cursor: pointer;
}
.check-item input[type="checkbox"] {
  width: 16px; height: 16px;
  border: 1.5px solid var(--border2);
  border-radius: 3px;
  background: var(--surface2);
  appearance: none;
  cursor: pointer;
  flex-shrink: 0;
  margin-top: 2px;
  position: relative;
  transition: all 0.15s;
}
.check-item input[type="checkbox"]:checked {
  background: var(--accent);
  border-color: var(--accent);
}
.check-item input[type="checkbox"]:checked::after {
  content: '✓';
  position: absolute;
  top: -1px; left: 1px;
  font-size: 11px;
  color: #000;
  font-weight: 700;
}
.check-text {
  font-size: 13px;
  color: var(--text);
  line-height: 1.4;
}
.check-text small { color: var(--muted); font-size: 11.5px; }

/* FLAG BOX */
.flag-box {
  background: var(--red-bg);
  border: 1px solid rgba(192,80,74,0.2);
  border-radius: var(--radius);
  padding: 14px 16px;
  margin-bottom: 14px;
}
.flag-label {
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--red);
  margin-bottom: 8px;
}

/* DIVIDER */
.divider {
  height: 1px;
  background: var(--border);
  margin: 24px 0;
}

/* NAV BUTTONS */
.form-nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 36px;
  padding-top: 20px;
  border-top: 1px solid var(--border);
  flex-wrap: wrap;
  gap: 12px;
}
.btn {
  padding: 11px 22px;
  border-radius: 6px;
  font-family: 'Instrument Sans', sans-serif;
  font-size: 13px;
  font-weight: 600;
  cursor: pointer;
  border: none;
  transition: all 0.2s;
  letter-spacing: 0.3px;
}
.btn-primary {
  background: var(--accent);
  color: #0f0f0f;
}
.btn-primary:hover { background: var(--accent2); transform: translateY(-1px); }
.btn-secondary {
  background: transparent;
  color: var(--muted);
  border: 1px solid var(--border2);
}
.btn-secondary:hover { color: var(--text); border-color: var(--muted); }
.btn:disabled { opacity: 0.3; cursor: not-allowed; transform: none !important; }
.btn-generate {
  background: linear-gradient(135deg, var(--accent), #b8862a);
  color: #0f0f0f;
  font-size: 14px;
  padding: 13px 28px;
  display: flex;
  align-items: center;
  gap: 10px;
}
.btn-generate:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(212,168,83,0.25); }

/* OUTPUT SECTION */
#output-section {
  margin-top: 0;
}
.output-loading {
  display: none;
  text-align: center;
  padding: 60px 20px;
}
.output-loading.active { display: block; }
.loader {
  display: inline-block;
  width: 40px; height: 40px;
  border: 3px solid var(--border2);
  border-top-color: var(--accent);
  border-radius: 50%;
  animation: spin 0.8s linear infinite;
  margin-bottom: 16px;
}
@keyframes spin { to { transform: rotate(360deg); } }
.loading-text {
  color: var(--muted);
  font-size: 14px;
}
.loading-text strong { color: var(--accent); display: block; font-size: 16px; margin-bottom: 6px; }

.output-result {
  display: none;
}
.output-result.active { display: block; }

.program-output {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 28px 32px;
  line-height: 1.75;
  font-size: 14px;
  color: var(--text);
}
.program-output h2 {
  font-family: 'Fraunces', serif;
  font-size: 22px;
  font-weight: 300;
  color: var(--accent);
  margin: 24px 0 10px;
}
.program-output h2:first-child { margin-top: 0; }
.program-output h3 {
  font-size: 14px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 1px;
  color: var(--text);
  margin: 18px 0 8px;
  border-bottom: 1px solid var(--border);
  padding-bottom: 6px;
}
.program-output h4 {
  font-size: 13px;
  font-weight: 600;
  color: var(--accent2);
  margin: 14px 0 6px;
}
.program-output p { margin-bottom: 10px; }
.program-output ul, .program-output ol {
  padding-left: 20px;
  margin-bottom: 12px;
}
.program-output li { margin-bottom: 5px; }
.program-output strong { color: var(--accent2); }
.program-output em { color: var(--muted); font-style: italic; }
.program-output table {
  width: 100%;
  border-collapse: collapse;
  margin: 12px 0;
  font-size: 13px;
}
.program-output th {
  background: var(--surface2);
  padding: 8px 12px;
  text-align: left;
  font-size: 11px;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: var(--muted);
  border-bottom: 1px solid var(--border2);
}
.program-output td {
  padding: 8px 12px;
  border-bottom: 1px solid var(--border);
  vertical-align: top;
}
.program-output tr:last-child td { border-bottom: none; }

.output-actions {
  display: flex;
  gap: 10px;
  margin-top: 20px;
  flex-wrap: wrap;
}
.btn-outline {
  background: transparent;
  border: 1px solid var(--border2);
  color: var(--muted);
  font-size: 12px;
  padding: 8px 16px;
}
.btn-outline:hover { border-color: var(--accent); color: var(--accent); }

.error-box {
  background: var(--red-bg);
  border: 1px solid rgba(192,80,74,0.3);
  border-radius: var(--radius);
  padding: 16px 20px;
  color: var(--red);
  font-size: 13px;
  display: none;
}
.error-box.active { display: block; }

@media (max-width: 640px) {
  header { padding: 24px 16px; }
  main { padding: 24px 16px 60px; }
  .tab-nav { padding: 0 16px; }
  .form-grid, .form-grid.cols3 { grid-template-columns: 1fr; }
  .field.span2, .field.span3 { grid-column: span 1; }
  .domein-grid { grid-template-columns: 1fr; }
  .program-output { padding: 20px 18px; }
}
</style>
</head>
<body>

<div class="progress-bar"><div class="progress-fill" id="progressFill"></div></div>

<header>
  <div class="header-left">
    <div class="logo">ExcluFit · Lynn's Tool</div>
    <h1>Intake & <em>Programma</em><br>Generator</h1>
    <p>Vul de intakekaart in — het AI-systeem genereert automatisch een persoonlijk trainingsplan.</p>
  </div>
  <div class="header-meta">
    <strong>Stap <span id="currentStepLabel">1</span> van 5</strong>
    Gebruik de tabs om te navigeren
  </div>
</header>

<nav class="tab-nav">
  <button class="tab-btn active" onclick="goTab(0)"><span class="tab-indicator"></span>Persoonlijk</button>
  <button class="tab-btn" onclick="goTab(1)"><span class="tab-indicator"></span>Gezondheid</button>
  <button class="tab-btn" onclick="goTab(2)"><span class="tab-indicator"></span>6 Domeinen</button>
  <button class="tab-btn" onclick="goTab(3)"><span class="tab-indicator"></span>Doelstelling</button>
  <button class="tab-btn" onclick="goTab(4)"><span class="tab-indicator"></span>Programma ✨</button>
</nav>

<main>

<!-- TAB 1: PERSOONLIJK -->
<section class="tab-section active" id="tab-0">
  <div class="section-title">Persoonlijke <em>gegevens</em></div>
  <div class="section-sub">Basisinformatie van de klant</div>

  <div class="form-grid">
    <div class="field">
      <label>Voornaam <span class="req">*</span></label>
      <input type="text" id="naam" placeholder="Naam klant">
    </div>
    <div class="field">
      <label>Achternaam</label>
      <input type="text" id="achternaam" placeholder="Achternaam">
    </div>
    <div class="field">
      <label>Leeftijd <span class="req">*</span></label>
      <input type="number" id="leeftijd" placeholder="Bijv. 34" min="10" max="100">
    </div>
    <div class="field">
      <label>Geslacht</label>
      <select id="geslacht">
        <option value="">Selecteer...</option>
        <option>Man</option>
        <option>Vrouw</option>
        <option>Anders / niet invullen</option>
      </select>
    </div>
    <div class="field">
      <label>Gewicht (kg)</label>
      <input type="number" id="gewicht" placeholder="Bijv. 72">
    </div>
    <div class="field">
      <label>Lengte (cm)</label>
      <input type="number" id="lengte" placeholder="Bijv. 170">
    </div>
    <div class="field span2">
      <label>Beroep / dagelijkse bezigheden</label>
      <input type="text" id="beroep" placeholder="Bijv. kantoormedewerker, verpleegkundige, student...">
    </div>
  </div>

  <div class="divider"></div>

  <div class="section-title" style="font-size:17px;">Bewegings<em>achtergrond</em></div>
  <div class="section-sub" style="margin-bottom:16px;">Hoe actief is de klant nu?</div>

  <div class="form-grid">
    <div class="field">
      <label>Huidig activiteitsniveau</label>
      <select id="activiteit">
        <option value="">Selecteer...</option>
        <option>Volledig inactief (geen sport)</option>
        <option>Licht actief (wandelen, fietsen)</option>
        <option>Matig actief (1-2x/week sporten)</option>
        <option>Actief (3-4x/week sporten)</option>
        <option>Zeer actief (5+ x/week)</option>
      </select>
    </div>
    <div class="field">
      <label>Ervaring met fitness/PT</label>
      <select id="ervaring">
        <option value="">Selecteer...</option>
        <option>Geen ervaring (beginner)</option>
        <option>Beperkte ervaring (< 6 maanden)</option>
        <option>Enige ervaring (6 mnd – 2 jaar)</option>
        <option>Gevorderd (2+ jaar)</option>
      </select>
    </div>
    <div class="field span2">
      <label>Eerdere sporten / activiteiten</label>
      <textarea id="sportenVerleden" placeholder="Wat heeft de klant vroeger of recent gedaan? Wat vond hij/zij leuk of juist niet?"></textarea>
    </div>
    <div class="field">
      <label>Beschikbare sessies per week</label>
      <select id="sessies">
        <option value="">Selecteer...</option>
        <option>1x per week</option>
        <option>2x per week</option>
        <option>3x per week</option>
        <option>4x per week</option>
        <option>5+ per week</option>
      </select>
    </div>
    <div class="field">
      <label>Beschikbare tijd per sessie</label>
      <select id="tijdPerSessie">
        <option value="">Selecteer...</option>
        <option>30 minuten</option>
        <option>45 minuten</option>
        <option>60 minuten</option>
        <option>75 minuten</option>
        <option>90+ minuten</option>
      </select>
    </div>
    <div class="field">
      <label>Trainingslocatie</label>
      <select id="locatie">
        <option value="">Selecteer...</option>
        <option>Fitness / sportschool (volledig uitgerust)</option>
        <option>ExcluFit (eigen locatie)</option>
        <option>Thuis (beperkte middelen)</option>
        <option>Buiten</option>
        <option>Combinatie</option>
      </select>
    </div>
    <div class="field">
      <label>Trainingsvoorkeur</label>
      <select id="voorkeur">
        <option value="">Selecteer...</option>
        <option>Kracht / gewichten</option>
        <option>Conditie / cardio</option>
        <option>Functioneel / beweging</option>
        <option>Groep / sociaal</option>
        <option>Geen voorkeur</option>
      </select>
    </div>
  </div>

  <div class="form-nav">
    <button class="btn btn-secondary" disabled>← Vorige</button>
    <button class="btn btn-primary" onclick="goTab(1)">Volgende →</button>
  </div>
</section>

<!-- TAB 2: GEZONDHEID -->
<section class="tab-section" id="tab-1">
  <div class="section-title">Gezondheid & <em>medisch</em></div>
  <div class="section-sub">Altijd zorgvuldig invullen — dit bepaalt de veiligheid van het programma</div>

  <div class="flag-box">
    <div class="flag-label">⚠️ Let op</div>
    <div style="font-size:13px; color: var(--text);">Bij twijfel over medische klachten altijd overleggen met huisarts of specialist vóór aanvang. Markeer zo nodig door te verwijzen.</div>
  </div>

  <div class="check-group">
    <div class="check-group-title">Heeft de klant (momenteel of in het verleden) last van:</div>
    <label class="check-item"><input type="checkbox" class="health-check" value="Hart- of vaatproblemen"> <span class="check-text">Hart- of vaatproblemen</span></label>
    <label class="check-item"><input type="checkbox" class="health-check" value="Hoge bloeddruk"> <span class="check-text">Hoge bloeddruk</span></label>
    <label class="check-item"><input type="checkbox" class="health-check" value="Diabetes (type 1 of 2)"> <span class="check-text">Diabetes (type 1 of 2)</span></label>
    <label class="check-item"><input type="checkbox" class="health-check" value="Rugklachten / hernia"> <span class="check-text">Rugklachten / hernia</span></label>
    <label class="check-item"><input type="checkbox" class="health-check" value="Knie- of gewrichtsklachten"> <span class="check-text">Knie- of gewrichtsklachten</span></label>
    <label class="check-item"><input type="checkbox" class="health-check" value="Schouder- of nekklachten"> <span class="check-text">Schouder- of nekklachten</span></label>
    <label class="check-item"><input type="checkbox" class="health-check" value="Astma / ademhalingsproblemen"> <span class="check-text">Astma / ademhalingsproblemen</span></label>
    <label class="check-item"><input type="checkbox" class="health-check" value="Chronische vermoeidheid"> <span class="check-text">Chronische vermoeidheid</span></label>
    <label class="check-item"><input type="checkbox" class="health-check" value="Psychische klachten (angst, burn-out, depressie)"> <span class="check-text">Psychische klachten <small>(angst, burn-out, depressie)</small></span></label>
    <label class="check-item"><input type="checkbox" class="health-check" value="Zwangerschap / postpartum"> <span class="check-text">Zwangerschap / postpartum</span></label>
    <label class="check-item"><input type="checkbox" class="health-check" value="Recent geopereerd"> <span class="check-text">Recent geopereerd</span></label>
  </div>

  <div class="form-grid">
    <div class="field span2">
      <label>Toelichting medische achtergrond</label>
      <textarea id="medischToelichting" placeholder="Beschrijf blessures, operaties, chronische klachten, medicatie. Hoe lang geleden? Nog actieve klachten?"></textarea>
    </div>
    <div class="field span2">
      <label>Huidige pijnklachten bij bewegen</label>
      <textarea id="pijn" placeholder="Waar zit de pijn? Bij welke beweging? Score 1-10? Wanneer begonnen?"></textarea>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section-title" style="font-size:17px;">Leefstijl <em>basis</em></div>
  <div class="section-sub" style="margin-bottom:16px;"></div>

  <div class="range-group">
    <div class="range-row">
      <div class="range-label">Slaap (uren per nacht) <small>Gemiddeld</small></div>
      <input type="range" id="slaap" min="3" max="10" value="7" oninput="updateRange('slaap','slaapVal')">
      <div class="range-val" id="slaapVal">7u</div>
    </div>
    <div class="range-row">
      <div class="range-label">Stressniveau <small>1 = rustig, 10 = hoog</small></div>
      <input type="range" id="stress" min="1" max="10" value="5" oninput="updateRange('stress','stressVal')">
      <div class="range-val" id="stressVal">5/10</div>
    </div>
    <div class="range-row">
      <div class="range-label">Energieniveau overdag <small>1 = uitgeput, 10 = vol energie</small></div>
      <input type="range" id="energie" min="1" max="10" value="6" oninput="updateRange('energie','energieVal')">
      <div class="range-val" id="energieVal">6/10</div>
    </div>
  </div>

  <div class="form-grid cols1">
    <div class="field">
      <label>Voeding (globale indruk)</label>
      <select id="voeding">
        <option value="">Selecteer...</option>
        <option>Zeer onregelmatig / weinig aandacht voor voeding</option>
        <option>Maaltijden worden regelmatig overgeslagen</option>
        <option>Redelijk — 3 maaltijden maar weinig bewust</option>
        <option>Goed — bewust bezig met voeding</option>
        <option>Uitstekend — gericht en gestructureerd</option>
      </select>
    </div>
    <div class="field">
      <label>Aanvullende leefstijlopmerkingen</label>
      <textarea id="leefstijlOpmerkingen" placeholder="Alcohol, roken, ploegendiensten, reizen, onregelmatig schema..."></textarea>
    </div>
  </div>

  <div class="form-nav">
    <button class="btn btn-secondary" onclick="goTab(0)">← Vorige</button>
    <button class="btn btn-primary" onclick="goTab(2)">Volgende →</button>
  </div>
</section>

<!-- TAB 3: 6 DOMEINEN -->
<section class="tab-section" id="tab-2">
  <div class="section-title">De <em>6 domeinen</em></div>
  <div class="section-sub">Noteer per domein wat de klant aangeeft. Dit is de kern van een holistisch programma.</div>

  <div class="domein-grid">
    <div class="domein-card d1">
      <div class="domein-num">Domein 1</div>
      <h4>🏃 Bewegen & Fysiek</h4>
      <textarea id="d1" placeholder="Wat is de belastbaarheid? Welke bewegingspatronen zijn aandachtspunten? Hoe is de houding?"></textarea>
    </div>
    <div class="domein-card d2">
      <div class="domein-num">Domein 2</div>
      <h4>🥗 Voeding & Energie</h4>
      <textarea id="d2" placeholder="Eet de klant genoeg? Regelmatig? Welke relatie heeft hij/zij met voeding?"></textarea>
    </div>
    <div class="domein-card d3">
      <div class="domein-num">Domein 3</div>
      <h4>😴 Slaap & Herstel</h4>
      <textarea id="d3" placeholder="Slaapkwaliteit, herstelcapaciteit, nachtrust. Risico op overtraining?"></textarea>
    </div>
    <div class="domein-card d4">
      <div class="domein-num">Domein 4</div>
      <h4>🧠 Mentaal & Stress</h4>
      <textarea id="d4" placeholder="Stressfactoren, mentale belastbaarheid, coping. Heeft training een therapeutische rol?"></textarea>
    </div>
    <div class="domein-card d5">
      <div class="domein-num">Domein 5</div>
      <h4>👥 Sociaal & Omgeving</h4>
      <textarea id="d5" placeholder="Steun vanuit omgeving, sociale invloeden op gedrag, praktische belemmeringen?"></textarea>
    </div>
    <div class="domein-card d6">
      <div class="domein-num">Domein 6</div>
      <h4>🎯 Gedrag & Motivatie</h4>
      <textarea id="d6" placeholder="Motivatiestijl, zelfeffectiviteit, eerder gestopt? Wat helpt deze persoon vol te houden?"></textarea>
    </div>
  </div>

  <div class="form-grid cols1">
    <div class="field">
      <label>Meest kritieke domein (aandachtspunt programma)</label>
      <select id="kritiekDomein">
        <option value="">Geen specifiek</option>
        <option>Domein 1 — Bewegen & Fysiek</option>
        <option>Domein 2 — Voeding & Energie</option>
        <option>Domein 3 — Slaap & Herstel</option>
        <option>Domein 4 — Mentaal & Stress</option>
        <option>Domein 5 — Sociaal & Omgeving</option>
        <option>Domein 6 — Gedrag & Motivatie</option>
      </select>
    </div>
  </div>

  <div class="form-nav">
    <button class="btn btn-secondary" onclick="goTab(1)">← Vorige</button>
    <button class="btn btn-primary" onclick="goTab(3)">Volgende →</button>
  </div>
</section>

<!-- TAB 4: DOELSTELLING -->
<section class="tab-section" id="tab-3">
  <div class="section-title">Doelstelling & <em>verwachting</em></div>
  <div class="section-sub">Van wens naar concreet SMART-doel</div>

  <div class="form-grid cols1">
    <div class="field">
      <label>Wens van de klant (eigen woorden) <span class="req">*</span></label>
      <textarea id="wens" placeholder="Schrijf exact op wat de klant zegt. Bijv: 'ik wil afvallen', 'ik wil sterker worden', 'ik wil me beter voelen'..."></textarea>
    </div>
    <div class="field">
      <label>Achterliggende motivatie (de echte waarom)</label>
      <textarea id="motivatie" placeholder="Na het 'waarom 3x' vragen: wat is de diepere drijfveer? Wat is de echte reden achter het doel?"></textarea>
    </div>
  </div>

  <div class="form-grid">
    <div class="field">
      <label>Primair doel</label>
      <select id="primairDoel">
        <option value="">Selecteer...</option>
        <option>Gewicht verliezen / vetpercentage verlagen</option>
        <option>Spiermassa opbouwen</option>
        <option>Conditie verbeteren</option>
        <option>Kracht vergroten</option>
        <option>Beweeglijkheid / mobiliteit verbeteren</option>
        <option>Revalideren / blessure herstel</option>
        <option>Algemeen fitter en energieker voelen</option>
        <option>Stressreductie / mentaal welzijn</option>
        <option>Sport-specifieke prestatieverbetering</option>
      </select>
    </div>
    <div class="field">
      <label>Gewenste tijdframe</label>
      <select id="tijdframe">
        <option value="">Selecteer...</option>
        <option>4 weken</option>
        <option>6 weken</option>
        <option>8 weken</option>
        <option>12 weken</option>
        <option>6 maanden</option>
        <option>Geen specifieke deadline</option>
      </select>
    </div>
    <div class="field span2">
      <label>Specifiek meetbaar doel (SMART)</label>
      <input type="text" id="smartDoel" placeholder="Bijv: 5 kg afvallen in 12 weken, 10 push-ups in 1 set kunnen doen, 5 km lopen zonder stop...">
    </div>
    <div class="field span2">
      <label>Eerdere pogingen & obstakels</label>
      <textarea id="obstakels" placeholder="Wat heeft eerder niet gewerkt? Wat zijn verwachte belemmeringen?"></textarea>
    </div>
  </div>

  <div class="range-group">
    <div class="range-row">
      <div class="range-label">Motivatie nu <small>1 = laag, 10 = hoog</small></div>
      <input type="range" id="motivatieScore" min="1" max="10" value="7" oninput="updateRange('motivatieScore','motivatieScoreVal')">
      <div class="range-val" id="motivatieScoreVal">7/10</div>
    </div>
    <div class="range-row">
      <div class="range-label">Vertrouwen in succes <small>1 = laag, 10 = hoog</small></div>
      <input type="range" id="vertrouwen" min="1" max="10" value="6" oninput="updateRange('vertrouwen','vertrouwenVal')">
      <div class="range-val" id="vertrouwenVal">6/10</div>
    </div>
  </div>

  <div class="form-grid cols1">
    <div class="field">
      <label>Aanvullende opmerkingen of wensen</label>
      <textarea id="aanvullend" placeholder="Alles wat nog niet aan bod is gekomen maar relevant is voor het programma..."></textarea>
    </div>
  </div>

  <div class="form-nav">
    <button class="btn btn-secondary" onclick="goTab(2)">← Vorige</button>
    <button class="btn btn-primary" onclick="goTab(4)">Genereer programma ✨</button>
  </div>
</section>

<!-- TAB 5: PROGRAMMA OUTPUT -->
<section class="tab-section" id="tab-4">
  <div id="output-section">
    <div class="section-title">Persoonlijk <em>trainingsplan</em></div>
    <div class="section-sub" id="outputSubtitle">Klik op de knop om het programma te genereren op basis van de ingevulde intake.</div>

    <div id="generateBtn" style="margin-bottom:28px;">
      <button class="btn btn-generate" onclick="generateProgram()">
        <span>✨</span> Genereer trainingsplan
      </button>
    </div>

    <div class="error-box" id="errorBox">
      Er is iets misgegaan bij het genereren. Controleer of alle verplichte velden zijn ingevuld en probeer opnieuw.
    </div>

    <div class="output-loading" id="loadingBox">
      <div class="loader"></div>
      <div class="loading-text">
        <strong>Programma wordt aangemaakt...</strong>
        De intakegegevens worden geanalyseerd en vertaald naar een persoonlijk plan.
      </div>
    </div>

    <div class="output-result" id="resultBox">
      <div class="program-output" id="programOutput"></div>
      <div class="output-actions">
        <button class="btn btn-outline" onclick="window.print()">🖨️ Afdrukken</button>
        <button class="btn btn-outline" onclick="copyOutput()">📋 Kopiëren</button>
        <button class="btn btn-outline" onclick="resetOutput()">🔄 Opnieuw genereren</button>
      </div>
    </div>
  </div>

  <div class="form-nav">
    <button class="btn btn-secondary" onclick="goTab(3)">← Terug naar intake</button>
    <span></span>
  </div>
</section>

</main>

<script>
// --- NAVIGATION ---
let currentTab = 0;
const tabCount = 5;

function goTab(index) {
  document.querySelectorAll('.tab-section').forEach((s, i) => s.classList.toggle('active', i === index));
  document.querySelectorAll('.tab-btn').forEach((b, i) => b.classList.toggle('active', i === index));
  currentTab = index;
  document.getElementById('currentStepLabel').textContent = index + 1;
  document.getElementById('progressFill').style.width = ((index + 1) / tabCount * 100) + '%';
  window.scrollTo({ top: 0, behavior: 'smooth' });
  updateTabFilled(index);
}

function updateTabFilled(activeIndex) {
  // Mark tabs with content as 'filled' (green dot)
  document.querySelectorAll('.tab-btn').forEach((b, i) => {
    if (i < activeIndex) b.classList.add('filled');
  });
}

// --- RANGE SLIDERS ---
function updateRange(id, valId) {
  const val = document.getElementById(id).value;
  const el = document.getElementById(valId);
  if (id === 'slaap') el.textContent = val + 'u';
  else el.textContent = val + '/10';
}

// --- COLLECT DATA ---
function collectIntake() {
  const checks = Array.from(document.querySelectorAll('.health-check:checked')).map(c => c.value);

  return {
    naam: document.getElementById('naam').value || 'Onbekend',
    achternaam: document.getElementById('achternaam').value,
    leeftijd: document.getElementById('leeftijd').value,
    geslacht: document.getElementById('geslacht').value,
    gewicht: document.getElementById('gewicht').value,
    lengte: document.getElementById('lengte').value,
    beroep: document.getElementById('beroep').value,
    activiteit: document.getElementById('activiteit').value,
    ervaring: document.getElementById('ervaring').value,
    sportenVerleden: document.getElementById('sportenVerleden').value,
    sessies: document.getElementById('sessies').value,
    tijdPerSessie: document.getElementById('tijdPerSessie').value,
    locatie: document.getElementById('locatie').value,
    voorkeur: document.getElementById('voorkeur').value,
    gezondheidKlachten: checks,
    medischToelichting: document.getElementById('medischToelichting').value,
    pijn: document.getElementById('pijn').value,
    slaap: document.getElementById('slaap').value,
    stress: document.getElementById('stress').value,
    energie: document.getElementById('energie').value,
    voeding: document.getElementById('voeding').value,
    leefstijlOpmerkingen: document.getElementById('leefstijlOpmerkingen').value,
    d1: document.getElementById('d1').value,
    d2: document.getElementById('d2').value,
    d3: document.getElementById('d3').value,
    d4: document.getElementById('d4').value,
    d5: document.getElementById('d5').value,
    d6: document.getElementById('d6').value,
    kritiekDomein: document.getElementById('kritiekDomein').value,
    wens: document.getElementById('wens').value,
    motivatie: document.getElementById('motivatie').value,
    primairDoel: document.getElementById('primairDoel').value,
    tijdframe: document.getElementById('tijdframe').value,
    smartDoel: document.getElementById('smartDoel').value,
    obstakels: document.getElementById('obstakels').value,
    motivatieScore: document.getElementById('motivatieScore').value,
    vertrouwen: document.getElementById('vertrouwen').value,
    aanvullend: document.getElementById('aanvullend').value
  };
}

function buildPrompt(d) {
  return `Je bent een ervaren personal trainer en sport-coach werkzaam bij ExcluFit. Op basis van de volgende intakegegevens maak je een volledig, professioneel en persoonlijk trainingsplan. Schrijf in het Nederlands. Wees concreet, praktisch en motiverend. Verwerk de 6 domeinen expliciet in het plan.

=== INTAKEGEGEVENS ===

KLANT: ${d.naam} ${d.achternaam}, ${d.leeftijd} jaar, ${d.geslacht}
Gewicht: ${d.gewicht} kg | Lengte: ${d.lengte} cm
Beroep: ${d.beroep}

BEWEEGGESCHIEDENIS:
- Activiteitsniveau: ${d.activiteit}
- Fitnesservaring: ${d.ervaring}
- Eerdere sporten: ${d.sportenVerleden}
- Sessies per week: ${d.sessies} | Tijd: ${d.tijdPerSessie}
- Locatie: ${d.locatie}
- Trainingsvoorkeur: ${d.voorkeur}

GEZONDHEID:
- Medische aandachtspunten: ${d.gezondheidKlachten.length ? d.gezondheidKlachten.join(', ') : 'Geen'}
- Medische toelichting: ${d.medischToelichting || 'Geen'}
- Pijnklachten: ${d.pijn || 'Geen'}

LEEFSTIJL:
- Slaap: ${d.slaap} uur/nacht
- Stress: ${d.stress}/10
- Energieniveau: ${d.energie}/10
- Voeding: ${d.voeding}
- Overig: ${d.leefstijlOpmerkingen || 'Geen'}

DE 6 DOMEINEN (observaties trainer):
1. Bewegen & Fysiek: ${d.d1 || 'Niet ingevuld'}
2. Voeding & Energie: ${d.d2 || 'Niet ingevuld'}
3. Slaap & Herstel: ${d.d3 || 'Niet ingevuld'}
4. Mentaal & Stress: ${d.d4 || 'Niet ingevuld'}
5. Sociaal & Omgeving: ${d.d5 || 'Niet ingevuld'}
6. Gedrag & Motivatie: ${d.d6 || 'Niet ingevuld'}
Meest kritiek domein: ${d.kritiekDomein || 'Geen'}

DOELSTELLING:
- Wens klant: ${d.wens}
- Achterliggende motivatie: ${d.motivatie || 'Niet ingevuld'}
- Primair doel: ${d.primairDoel}
- Tijdframe: ${d.tijdframe}
- SMART doel: ${d.smartDoel || 'Niet geformuleerd'}
- Obstakels: ${d.obstakels || 'Geen'}
- Motivatiescore: ${d.motivatieScore}/10
- Vertrouwen in succes: ${d.vertrouwen}/10
- Aanvullend: ${d.aanvullend || 'Geen'}

=== OPDRACHT ===

Maak een professioneel trainingsplan met de volgende secties:

## Samenvatting van de klant
Korte analyse van het profiel, de kansen en de aandachtspunten. Benoem ook eventuele voorzorgsmaatregelen op basis van medische of gezondheidsgegevens.

## SMART-doelstelling
Formuleer of verfijn het doel SMART. Maak onderscheid tussen het lange termijn doel en 1-2 korte termijn (4-weken) doelen.

## Analyse per domein
Beschrijf per relevant domein hoe dit het programma beïnvloedt en welke aanpak je hanteert.

## Programmastructuur (fasen)
Beschrijf de fasering over het gekozen tijdframe met per fase: doel, focus, duur en belasting.

## Weekschema
Maak een concreet weekschema met trainingen en eventuele rustdagen. Geef per trainingsdag aan: type training, duur, intensiteit.

## Oefeningenoverzicht per fase
Geef per fase 6-8 concrete oefeningen met sets, herhalingen en aanwijzingen. Pas dit aan op het niveau en de locatie.

## Progressierichtlijnen
Hoe en wanneer wordt de belasting verhoogd? Welke signalen geven aan dat bijsturen nodig is?

## Coachingstips voor de trainer
Specifieke adviezen voor Lynn als begeleider van deze klant, gebaseerd op het profiel en de domeinen.

## Evaluatiemomenten
Wanneer en hoe wordt geëvalueerd? Welke meetpunten gebruik je?

Schrijf professioneel maar toegankelijk. Wees specifiek en praktisch. Maak het plan direct bruikbaar.`;
}

// --- GENERATE ---
async function generateProgram() {
  const data = collectIntake();

  if (!data.naam || data.naam === 'Onbekend' || !data.wens || !data.primairDoel) {
    const err = document.getElementById('errorBox');
    err.textContent = 'Vul minimaal de naam, wens en het primaire doel in (tab 1 en 4) voordat je het programma genereert.';
    err.classList.add('active');
    return;
  }

  document.getElementById('errorBox').classList.remove('active');
  document.getElementById('generateBtn').style.display = 'none';
  document.getElementById('loadingBox').classList.add('active');
  document.getElementById('resultBox').classList.remove('active');

  const prompt = buildPrompt(data);

  try {
    const response = await fetch("https://api.anthropic.com/v1/messages", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({
        model: "claude-sonnet-4-20250514",
        max_tokens: 1000,
        messages: [{ role: "user", content: prompt }]
      })
    });

    const result = await response.json();
    const text = result.content?.[0]?.text || '';

    document.getElementById('loadingBox').classList.remove('active');

    if (!text) throw new Error('Leeg antwoord');

    document.getElementById('programOutput').innerHTML = markdownToHtml(text);
    document.getElementById('resultBox').classList.add('active');
    document.getElementById('outputSubtitle').textContent = `Trainingsplan voor ${data.naam} — gegenereerd op basis van intake.`;

  } catch (e) {
    document.getElementById('loadingBox').classList.remove('active');
    document.getElementById('generateBtn').style.display = 'block';
    const err = document.getElementById('errorBox');
    err.textContent = 'Er is iets misgegaan. Probeer opnieuw of controleer de verbinding.';
    err.classList.add('active');
  }
}

// --- MARKDOWN TO HTML ---
function markdownToHtml(md) {
  return md
    .replace(/^## (.+)$/gm, '<h2>$1</h2>')
    .replace(/^### (.+)$/gm, '<h3>$1</h3>')
    .replace(/^#### (.+)$/gm, '<h4>$1</h4>')
    .replace(/\*\*(.+?)\*\*/g, '<strong>$1</strong>')
    .replace(/\*(.+?)\*/g, '<em>$1</em>')
    .replace(/^- (.+)$/gm, '<li>$1</li>')
    .replace(/^(\d+)\. (.+)$/gm, '<li>$2</li>')
    .replace(/(<li>.*<\/li>)/gs, '<ul>$1</ul>')
    .replace(/\n\n/g, '</p><p>')
    .replace(/^(?!<[hul])/gm, '')
    .split('\n').filter(l => l.trim()).map(l => {
      if (l.startsWith('<h') || l.startsWith('<ul') || l.startsWith('<li')) return l;
      if (!l.startsWith('<')) return '<p>' + l + '</p>';
      return l;
    }).join('\n');
}

function copyOutput() {
  const text = document.getElementById('programOutput').innerText;
  navigator.clipboard.writeText(text).then(() => {
    alert('Trainingsplan gekopieerd naar klembord!');
  });
}

function resetOutput() {
  document.getElementById('resultBox').classList.remove('active');
  document.getElementById('generateBtn').style.display = 'block';
  document.getElementById('outputSubtitle').textContent = 'Klik op de knop om het programma te genereren op basis van de ingevulde intake.';
}
</script>

</body>
</html>
