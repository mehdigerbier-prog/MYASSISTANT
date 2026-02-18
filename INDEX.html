<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Analyseur RAC — Assistant Conseiller</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #FFFFFF;
    --navy2: #F8F9FC;
    --blue: #1E3A8A;
    --accent: #3B82F6;
    --accent2: #60A5FA;
    --gold: #F59E0B;
    --green: #10B981;
    --orange: #F97316;
    --red: #EF4444;
    --surface: #F8F9FC;
    --card: #FFFFFF;
    --card2: #F1F4F9;
    --border: #E2E8F0;
    --text: #1E293B;
    --muted: #64748B;
    --mono: 'JetBrains Mono', 'Fira Code', monospace;
    --serif: 'Inter', system-ui, sans-serif;
    --sans: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--surface);
    color: var(--text);
    font-family: var(--sans);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* BG GRID */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(59,130,246,0.025) 1px, transparent 1px),
      linear-gradient(90deg, rgba(59,130,246,0.025) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .app { position: relative; z-index: 1; display: flex; min-height: 100vh; }

  /* SIDEBAR */
  .sidebar {
    width: 260px;
    min-width: 260px;
    background: #F1F5FB;
    border-right: 1px solid var(--border);
    display: flex;
    flex-direction: column;
    position: fixed;
    top: 0; left: 0; bottom: 0;
    z-index: 100;
    overflow-y: auto;
  }

  .logo {
    padding: 24px 20px 20px;
    border-bottom: 1px solid var(--border);
  }
  .logo-badge {
    display: inline-block;
    background: var(--accent);
    color: white;
    font-size: 9px;
    font-family: var(--mono);
    letter-spacing: 2px;
    padding: 3px 8px;
    border-radius: 3px;
    margin-bottom: 8px;
    text-transform: uppercase;
  }
  .logo h1 {
    font-size: 19px;
    font-weight: 700;
    line-height: 1.2;
    color: white;
  }
  .logo p {
    font-size: 11px;
    color: var(--muted);
    font-family: var(--mono);
    margin-top: 4px;
    letter-spacing: 0.5px;
  }

  .nav { padding: 16px 12px; flex: 1; }

  .nav-section-label {
    font-size: 9px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--muted);
    font-family: var(--mono);
    padding: 8px 8px 4px;
    margin-top: 8px;
  }

  .nav-item {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 10px 12px;
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.15s;
    font-size: 13px;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 3px;
    border: 1px solid transparent;
    line-height: 1.3;
  }
  .nav-item:hover { background: var(--card); color: var(--text); }
  .nav-item.active {
    background: rgba(59,130,246,0.10);
    color: #2563EB;
    border-color: rgba(59,130,246,0.25);
  }
  .nav-item .icon { font-size: 16px; min-width: 20px; text-align: center; }
  .nav-item .step-num {
    min-width: 24px;
    height: 24px;
    border-radius: 50%;
    background: var(--border);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 11px;
    font-family: var(--mono);
    font-weight: 700;
    color: var(--muted);
    flex-shrink: 0;
    transition: all 0.2s;
  }
  .nav-item.active .step-num {
    background: var(--accent);
    color: white;
    box-shadow: 0 0 8px rgba(59,130,246,0.5);
  }
  .nav-item.done .step-num {
    background: var(--green);
    color: white;
  }
  .nav-item.done { color: var(--text); }

  .sidebar-bottom {
    padding: 16px;
    border-top: 1px solid var(--border);
  }

  .rgpd-badge {
    background: rgba(16,185,129,0.1);
    border: 1px solid rgba(16,185,129,0.3);
    border-radius: 8px;
    padding: 10px 12px;
    font-size: 10px;
    color: var(--green);
    font-family: var(--mono);
    line-height: 1.5;
  }

  /* MAIN */
  .main {
    margin-left: 260px;
    flex: 1;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  /* TOPBAR */
  .topbar {
    background: rgba(15,23,42,0.9);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: 0 32px;
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: sticky;
    top: 0;
    z-index: 50;
  }
  .topbar-title {
    font-size: 14px;
    font-weight: 700;
    color: var(--text);
    font-family: var(--sans);
  }
  .topbar-title span { color: var(--accent2); }

  .progress-bar-wrap {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 11px;
    color: var(--muted);
    font-family: var(--mono);
  }
  .progress-track {
    width: 140px;
    height: 4px;
    background: var(--border);
    border-radius: 4px;
    overflow: hidden;
  }
  .progress-fill {
    height: 100%;
    background: linear-gradient(90deg, var(--accent), var(--gold));
    border-radius: 4px;
    transition: width 0.4s ease;
    width: 14%;
  }

  .btn-analyze {
    background: linear-gradient(135deg, var(--accent), #2563EB);
    color: white;
    border: none;
    padding: 10px 24px;
    border-radius: 8px;
    font-family: var(--sans);
    font-size: 13px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.2s;
    letter-spacing: 0.5px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .btn-analyze:hover { transform: translateY(-1px); box-shadow: 0 8px 24px rgba(59,130,246,0.4); }
  .btn-analyze:active { transform: none; }

  /* CONTENT */
  .content {
    flex: 1;
    padding: 32px;
    max-width: 1100px;
  }

  /* SECTION PANELS */
  .section-panel {
    display: none;
    animation: fadeIn 0.2s ease;
  }
  .section-panel.active { display: block; }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .panel-header {
    margin-bottom: 28px;
  }
  .panel-header h2 {
    font-size: 24px;
    font-weight: 700;
    color: white;
    margin-bottom: 6px;
    letter-spacing: -0.3px;
  }
  .panel-header p {
    color: var(--muted);
    font-size: 13px;
    font-family: var(--mono);
  }

  /* FORM GRID */
  .form-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }
  .form-grid.cols3 { grid-template-columns: 1fr 1fr 1fr; }
  .form-grid.full { grid-template-columns: 1fr; }

  .form-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    transition: border-color 0.2s;
  }
  .form-card:hover { border-color: rgba(59,130,246,0.3); }
  .form-card.span2 { grid-column: span 2; }
  .form-card.span3 { grid-column: span 3; }

  .form-label {
    font-size: 11px;
    font-family: var(--mono);
    letter-spacing: 1px;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 8px;
    display: block;
  }
  .form-label span {
    color: var(--gold);
    margin-left: 4px;
  }

  .form-input {
    width: 100%;
    background: #FFFFFF;
    border: 1.5px solid var(--border);
    border-radius: 8px;
    color: var(--text);
    font-family: var(--mono);
    font-size: 14px;
    padding: 10px 14px;
    outline: none;
    transition: border-color 0.2s;
    appearance: none;
  }
  .form-input:focus { border-color: var(--accent); box-shadow: 0 0 0 3px rgba(59,130,246,0.15); }
  .form-input option { background: var(--card); }

  .form-hint {
    font-size: 10px;
    color: var(--muted);
    font-family: var(--mono);
    margin-top: 6px;
    opacity: 0.8;
    line-height: 1.5;
  }

  /* RADIO BUTTONS */
  .radio-group {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
  }
  .radio-btn {
    padding: 7px 16px;
    border-radius: 6px;
    border: 1px solid var(--border);
    background: var(--surface);
    color: var(--muted);
    font-family: var(--mono);
    font-size: 12px;
    cursor: pointer;
    transition: all 0.15s;
    user-select: none;
  }
  .radio-btn:hover { border-color: var(--accent); color: var(--text); }
  .radio-btn.selected {
    background: rgba(59,130,246,0.15);
    border-color: var(--accent);
    color: var(--accent2);
    font-weight: 500;
  }

  /* CHECKBOX */
  .check-group {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }
  .check-item {
    display: flex;
    align-items: center;
    gap: 10px;
    cursor: pointer;
    font-size: 13px;
    color: var(--text);
    padding: 6px 0;
  }
  .check-item input[type=checkbox] { display: none; }
  .check-box {
    width: 18px; height: 18px;
    border: 1px solid var(--border);
    border-radius: 4px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 11px;
    transition: all 0.15s;
    min-width: 18px;
    background: var(--surface);
  }
  .check-item.checked .check-box {
    background: var(--accent);
    border-color: var(--accent);
    color: white;
  }

  .section-title {
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--accent2);
    font-family: var(--mono);
    margin-bottom: 16px;
    margin-top: 8px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  .nav-buttons {
    display: flex;
    gap: 12px;
    margin-top: 32px;
  }
  .btn-prev {
    padding: 11px 24px;
    background: transparent;
    border: 1px solid var(--border);
    border-radius: 8px;
    color: var(--muted);
    font-family: var(--sans);
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.15s;
  }
  .btn-prev:hover { border-color: var(--text); color: var(--text); }
  .btn-next {
    padding: 11px 28px;
    background: linear-gradient(135deg, var(--accent), #2563EB);
    border: none;
    border-radius: 8px;
    color: white;
    font-family: var(--sans);
    font-size: 13px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.2s;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .btn-next:hover { transform: translateY(-1px); box-shadow: 0 6px 20px rgba(59,130,246,0.35); }

  /* RESULTS PAGE */
  #section-result {
    max-width: 1100px;
  }

  .result-hero {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 32px;
    margin-bottom: 24px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .result-hero::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 4px;
  }
  .result-hero.vert::before { background: linear-gradient(90deg, var(--green), #34D399); }
  .result-hero.orange::before { background: linear-gradient(90deg, var(--orange), #FBBF24); }
  .result-hero.rouge::before { background: linear-gradient(90deg, var(--red), #F87171); }

  .result-verdict {
    font-size: 48px;
    margin-bottom: 8px;
  }
  .result-label {
    font-size: 30px;
    font-weight: 700;
    color: white;
    margin-bottom: 8px;
    letter-spacing: -0.5px;
  }
  .result-label.vert { color: var(--green); }
  .result-label.orange { color: var(--orange); }
  .result-label.rouge { color: var(--red); }

  .result-summary {
    color: var(--muted);
    font-size: 14px;
    font-family: var(--mono);
    max-width: 600px;
    margin: 0 auto;
    line-height: 1.7;
  }

  .result-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 16px;
    margin-bottom: 24px;
  }

  .result-kpi {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    text-align: center;
  }
  .result-kpi .kpi-val {
    font-family: var(--mono);
    font-size: 30px;
    font-weight: 700;
    color: white;
    margin-bottom: 4px;
  }
  .result-kpi .kpi-val.good { color: var(--green); }
  .result-kpi .kpi-val.warn { color: var(--orange); }
  .result-kpi .kpi-val.bad { color: var(--red); }
  .result-kpi .kpi-label {
    font-size: 10px;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: var(--muted);
    font-family: var(--mono);
  }

  .partner-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-bottom: 24px;
  }

  .partner-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    transition: border-color 0.2s;
  }
  .partner-card.eligible {
    border-color: rgba(16,185,129,0.4);
    background: linear-gradient(135deg, rgba(16,185,129,0.05), var(--card));
  }
  .partner-card.partiel {
    border-color: rgba(249,115,22,0.4);
    background: linear-gradient(135deg, rgba(249,115,22,0.05), var(--card));
  }
  .partner-card.non-eligible {
    border-color: rgba(239,68,68,0.25);
    opacity: 0.7;
  }

  .partner-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 12px;
  }
  .partner-name {
    font-size: 16px;
    font-weight: 800;
    color: white;
  }
  .partner-badge {
    font-size: 10px;
    font-family: var(--mono);
    padding: 3px 10px;
    border-radius: 20px;
    letter-spacing: 1px;
  }
  .partner-badge.ok { background: rgba(16,185,129,0.2); color: var(--green); border: 1px solid rgba(16,185,129,0.3); }
  .partner-badge.partiel { background: rgba(249,115,22,0.2); color: var(--orange); border: 1px solid rgba(249,115,22,0.3); }
  .partner-badge.ko { background: rgba(239,68,68,0.15); color: var(--red); border: 1px solid rgba(239,68,68,0.25); }

  .partner-rules {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 5px;
  }
  .partner-rule {
    font-size: 12px;
    font-family: var(--mono);
    color: var(--muted);
    display: flex;
    gap: 8px;
    align-items: flex-start;
    line-height: 1.5;
  }
  .partner-rule .dot { min-width: 14px; }
  .partner-rule.ok { color: #4ADE80; }
  .partner-rule.warn { color: #FCD34D; }
  .partner-rule.ko-rule { color: #F87171; }

  .blocking-box {
    background: rgba(239,68,68,0.08);
    border: 1px solid rgba(239,68,68,0.3);
    border-radius: 12px;
    padding: 20px;
    margin-bottom: 24px;
  }
  .blocking-title {
    font-size: 12px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--red);
    font-family: var(--mono);
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .blocking-items {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }
  .blocking-item {
    font-size: 13px;
    font-family: var(--mono);
    color: #FCA5A5;
    display: flex;
    gap: 10px;
    align-items: flex-start;
    line-height: 1.5;
  }

  .note-box {
    background: var(--card2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 24px;
    margin-bottom: 24px;
    white-space: pre-wrap;
    font-family: var(--mono);
    font-size: 12px;
    color: var(--text);
    line-height: 1.8;
    position: relative;
  }
  .note-box-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 16px;
  }
  .copy-btn {
    font-size: 11px;
    font-family: var(--mono);
    background: var(--card);
    border: 1px solid var(--border);
    color: var(--muted);
    padding: 5px 14px;
    border-radius: 6px;
    cursor: pointer;
    transition: all 0.15s;
  }
  .copy-btn:hover { border-color: var(--accent); color: var(--accent2); }

  .checklist-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-bottom: 24px;
  }
  .checklist-group {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
  }
  .checklist-group-title {
    font-size: 11px;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: var(--accent2);
    font-family: var(--mono);
    margin-bottom: 12px;
  }
  .checklist-item {
    display: flex;
    gap: 10px;
    align-items: flex-start;
    font-size: 12px;
    font-family: var(--mono);
    color: var(--text);
    margin-bottom: 8px;
    cursor: pointer;
    line-height: 1.5;
  }
  .checklist-item .cb {
    min-width: 16px;
    height: 16px;
    border: 1px solid var(--border);
    border-radius: 3px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 1px;
    transition: all 0.15s;
  }
  .checklist-item.done .cb { background: var(--green); border-color: var(--green); }
  .checklist-item.done { color: var(--muted); text-decoration: line-through; }

  .btn-reset {
    padding: 11px 24px;
    background: transparent;
    border: 1px solid var(--border);
    border-radius: 8px;
    color: var(--muted);
    font-family: var(--sans);
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.15s;
    margin-top: 16px;
  }
  .btn-reset:hover { border-color: var(--red); color: var(--red); }

  .alert-box {
    border-radius: 8px;
    padding: 12px 16px;
    font-size: 12px;
    font-family: var(--mono);
    margin-bottom: 12px;
    line-height: 1.6;
    display: flex;
    gap: 10px;
    align-items: flex-start;
  }
  .alert-box.info { background: rgba(59,130,246,0.1); border: 1px solid rgba(59,130,246,0.25); color: var(--accent2); }
  .alert-box.warn { background: rgba(249,115,22,0.1); border: 1px solid rgba(249,115,22,0.3); color: #FDBA74; }

  .montage-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-family: var(--mono);
    font-size: 13px;
    padding: 6px 16px;
    border-radius: 20px;
    font-weight: 500;
    margin: 4px;
  }
  .montage-badge.pp { background: rgba(59,130,246,0.15); border: 1px solid rgba(59,130,246,0.3); color: var(--accent2); }
  .montage-badge.lcc { background: rgba(16,185,129,0.15); border: 1px solid rgba(16,185,129,0.3); color: var(--green); }
  .montage-badge.ls2 { background: rgba(245,158,11,0.15); border: 1px solid rgba(245,158,11,0.3); color: var(--gold); }

  @media (max-width: 900px) {
    .sidebar { display: none; }
    .main { margin-left: 0; }
    .form-grid { grid-template-columns: 1fr; }
    .form-card.span2, .form-card.span3 { grid-column: span 1; }
    .result-grid, .partner-grid, .checklist-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>
<div class="app">

  <!-- SIDEBAR -->
  <aside class="sidebar">
    <div class="logo">
      <div class="logo-badge">Outil interne</div>
      <h1>Analyseur<br>RAC</h1>
      <p>Book Normes v2024</p>
    </div>
    <nav class="nav">
      <div class="nav-section-label">Saisie dossier</div>
      <div class="nav-item active" onclick="goTo(0)" id="nav0">
        <div class="step-num" id="stepnum0">1</div>
        <span>Situation & Logement</span>
      </div>
      <div class="nav-item" onclick="goTo(1)" id="nav1">
        <div class="step-num" id="stepnum1">2</div>
        <span>Revenus</span>
      </div>
      <div class="nav-item" onclick="goTo(2)" id="nav2">
        <div class="step-num" id="stepnum2">3</div>
        <span>Charges & Crédits</span>
      </div>
      <div class="nav-item" onclick="goTo(3)" id="nav3">
        <div class="step-num" id="stepnum3">4</div>
        <span>Comportement Bancaire</span>
      </div>
      <div class="nav-item" onclick="goTo(4)" id="nav4">
        <div class="step-num" id="stepnum4">5</div>
        <span>Projet & Trésorerie</span>
      </div>
      <div class="nav-section-label">Résultat</div>
      <div class="nav-item" onclick="analyser()" id="nav5">
        <div class="step-num" id="stepnum5">⚡</div>
        <span>Analyse & Verdict</span>
      </div>
    </nav>
    <div class="sidebar-bottom">
      <div class="rgpd-badge">🔒 RGPD compliant<br>Aucune donnée nominative<br>Variables anonymisées</div>
    </div>
  </aside>

  <!-- MAIN -->
  <div class="main">
    <div class="topbar">
      <div class="topbar-title">Assistant <span>Regroupement de Crédits</span></div>
      <div class="progress-bar-wrap">
        <span id="progressLabel">Étape 1/5</span>
        <div class="progress-track">
          <div class="progress-fill" id="progressFill"></div>
        </div>
      </div>
      <button class="btn-analyze" onclick="analyser()">⚡ Analyser maintenant</button>
    </div>

    <div class="content">

      <!-- ===== SECTION 1 : SITUATION & LOGEMENT ===== -->
      <div class="section-panel active" id="section-0">
        <div class="panel-header">
          <h2>Situation personnelle & Logement</h2>
          <p>Variables anonymisées — aucun nom, adresse ou identifiant requis</p>
        </div>

        <div class="section-title">Foyer</div>
        <div class="form-grid cols3">
          <div class="form-card">
            <label class="form-label">Année de naissance emprunteur 1 <span>*</span></label>
            <input type="number" class="form-input" id="annee_naissance" placeholder="ex: 1975" min="1935" max="2006">
            <div class="form-hint">Calcul âge et durée max selon partenaire</div>
          </div>
          <div class="form-card">
            <label class="form-label">Année de naissance emprunteur 2</label>
            <input type="number" class="form-input" id="annee_naissance2" placeholder="Si co-emprunteur" min="1935" max="2006">
          </div>
          <div class="form-card">
            <label class="form-label">Situation familiale</label>
            <select class="form-input" id="situation_fam">
              <option value="">-- Sélectionner --</option>
              <option value="seul">Seul(e)</option>
              <option value="couple">En couple</option>
              <option value="couple_enfants">En couple avec enfants</option>
              <option value="seul_enfants">Seul(e) avec enfants</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Enfants à charge (nombre)</label>
            <select class="form-input" id="nb_enfants">
              <option value="0">0</option>
              <option value="1">1</option>
              <option value="2">2</option>
              <option value="3">3</option>
              <option value="4">4+</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Garde alternée</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'garde_alternee','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'garde_alternee','oui')">Oui</div>
            </div>
            <input type="hidden" id="garde_alternee" value="non">
          </div>
          <div class="form-card">
            <label class="form-label">Instance de divorce / séparation</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'divorce','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'divorce','oui')">Oui</div>
            </div>
            <input type="hidden" id="divorce" value="non">
          </div>
        </div>

        <div class="section-title">Logement</div>
        <div class="form-grid cols3">
          <div class="form-card">
            <label class="form-label">Statut logement <span>*</span></label>
            <select class="form-input" id="statut_logement" onchange="toggleImmo(); toggleForcePP()">
              <option value="">-- Sélectionner --</option>
              <option value="proprietaire">Propriétaire</option>
              <option value="locataire">Locataire</option>
              <option value="heberge">Hébergé</option>
            </select>
            <div class="form-hint">Détermine l'orientation PP / LCC / LS2</div>
          </div>
          <div class="form-card" id="force_pp_card" style="display:none; border: 1px solid rgba(59,130,246,0.35); background: linear-gradient(135deg, rgba(59,130,246,0.08), var(--card));">
            <label class="form-label" style="color:var(--accent2)">Forcer le montage en PP <span style="color:var(--gold)">★</span></label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn selected" onclick="selectRadio(this,'force_pp','non')">Non — laisser choisir</div>
              <div class="radio-btn" onclick="selectRadio(this,'force_pp','oui')">Oui — PP uniquement</div>
            </div>
            <input type="hidden" id="force_pp" value="non">
            <div class="form-hint" style="color:rgba(96,165,250,0.85)">Propriétaire souhaitant rester en sans garantie — exclut LCC et LS2 de l'analyse</div>
          </div>
          <div class="form-card">
            <label class="form-label">Ancienneté logement</label>
            <select class="form-input" id="anciennete_logement">
              <option value="moins2">Moins de 2 ans</option>
              <option value="2a5">2 à 5 ans</option>
              <option value="5a10">5 à 10 ans</option>
              <option value="plus10">Plus de 10 ans</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Nationalité / Titre de séjour</label>
            <select class="form-input" id="nationalite">
              <option value="fr">Français / EU</option>
              <option value="sejour">Titre de séjour valide</option>
              <option value="hors_fr">Hors France non frontalier</option>
            </select>
          </div>
        </div>

        <div id="immo_section" style="display:none">
          <div class="section-title">Bien immobilier</div>
          <div class="form-grid cols3">
            <div class="form-card">
              <label class="form-label">Type de bien</label>
              <select class="form-input" id="type_bien">
                <option value="maison_rp">Maison — Résidence principale</option>
                <option value="appart_rp">Appartement — Résidence principale</option>
                <option value="locatif">Bien locatif</option>
                <option value="mixte">Mixte</option>
              </select>
            </div>
            <div class="form-card">
              <label class="form-label">Valeur estimée du bien</label>
              <select class="form-input" id="valeur_bien">
                <option value="">Non renseignée</option>
                <option value="moins100">Moins de 100 000 €</option>
                <option value="100_200">100 000 — 200 000 €</option>
                <option value="200_350">200 000 — 350 000 €</option>
                <option value="350_500">350 000 — 500 000 €</option>
                <option value="plus500">Plus de 500 000 €</option>
              </select>
            </div>
            <div class="form-card">
              <label class="form-label">Capital restant dû immobilier</label>
              <select class="form-input" id="crd_immo">
                <option value="0">Aucun (acquitté)</option>
                <option value="moins30">Moins de 30 000 €</option>
                <option value="30_80">30 000 — 80 000 €</option>
                <option value="80_150">80 000 — 150 000 €</option>
                <option value="plus150">Plus de 150 000 €</option>
              </select>
            </div>
            <div class="form-card">
              <label class="form-label">Rang hypothécaire actuel</label>
              <div class="radio-group" style="margin-top:4px">
                <div class="radio-btn" onclick="selectRadio(this,'rang_hypo','1er')">1er rang</div>
                <div class="radio-btn" onclick="selectRadio(this,'rang_hypo','2eme')">2ème rang</div>
                <div class="radio-btn" onclick="selectRadio(this,'rang_hypo','cautionne')">Cautionné</div>
                <div class="radio-btn" onclick="selectRadio(this,'rang_hypo','na')">N/A</div>
              </div>
              <input type="hidden" id="rang_hypo" value="na">
            </div>
            <div class="form-card">
              <label class="form-label">Prêt immobilier en cours</label>
              <div class="radio-group" style="margin-top:4px">
                <div class="radio-btn" onclick="selectRadio(this,'pret_immo_encours','non')">Non</div>
                <div class="radio-btn" onclick="selectRadio(this,'pret_immo_encours','oui')">Oui — à reprendre</div>
                <div class="radio-btn" onclick="selectRadio(this,'pret_immo_encours','conserver')">Oui — à conserver</div>
              </div>
              <input type="hidden" id="pret_immo_encours" value="non">
            </div>
            <div class="form-card">
              <label class="form-label">RAC antérieur en cours</label>
              <div class="radio-group" style="margin-top:4px">
                <div class="radio-btn" onclick="selectRadio(this,'rac_anterieur','non')">Non</div>
                <div class="radio-btn" onclick="selectRadio(this,'rac_anterieur','plus1an')">Oui &gt;1 an</div>
                <div class="radio-btn" onclick="selectRadio(this,'rac_anterieur','moins1an')">Oui &lt;1 an</div>
              </div>
              <input type="hidden" id="rac_anterieur" value="non">
              <div class="form-hint">RAC &lt;1 an : bloquant MYMB, LBP et certains produits CREATIS</div>
            </div>
          </div>
        </div>

        <div class="nav-buttons">
          <button class="btn-next" onclick="goTo(1)">Revenus →</button>
        </div>
      </div>

      <!-- ===== SECTION 2 : REVENUS ===== -->
      <div class="section-panel" id="section-1">
        <div class="panel-header">
          <h2>Situation professionnelle & Revenus</h2>
          <p>Saisie des montants exacts en € pour un calcul précis du TEAP et du RAV</p>
        </div>

        <div class="section-title">Emprunteur 1</div>
        <div class="form-grid">
          <div class="form-card">
            <label class="form-label">Type de contrat <span>*</span></label>
            <select class="form-input" id="contrat1">
              <option value="">-- Sélectionner --</option>
              <option value="cdi">CDI secteur privé</option>
              <option value="fonctionnaire">Fonctionnaire titulaire</option>
              <option value="retraite">Retraité(e)</option>
              <option value="cdd">CDD</option>
              <option value="interim">Intérimaire</option>
              <option value="ae">Auto-entrepreneur / Micro</option>
              <option value="tns">TNS / Indépendant</option>
              <option value="liberal">Profession libérale</option>
              <option value="chomage">Chômage / ARE</option>
              <option value="sans">Sans emploi</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Ancienneté poste</label>
            <select class="form-input" id="anciennete1">
              <option value="moins6m">Moins de 6 mois</option>
              <option value="6m_1an">6 mois à 1 an</option>
              <option value="1a3an">1 à 3 ans</option>
              <option value="plus3an">Plus de 3 ans</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Revenus mensuels nets <span>*</span></label>
            <input type="number" class="form-input" id="revenus1" placeholder="ex : 2 350" min="0" max="99999" step="1">
            <div class="form-hint">Montant exact en € — moyenne 3 derniers BS nets à payer</div>
          </div>
          <div class="form-card">
            <label class="form-label">Arrêt maladie en cours</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'arret_maladie','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'arret_maladie','court')">Oui ≤15j</div>
              <div class="radio-btn" onclick="selectRadio(this,'arret_maladie','long')">Oui &gt;15j</div>
            </div>
            <input type="hidden" id="arret_maladie" value="non">
            <div class="form-hint">YOUNITED : OK si ≤15j. Autres partenaires : généralement KO</div>
          </div>
        </div>

        <div class="section-title">Emprunteur 2 (si applicable)</div>
        <div class="form-grid">
          <div class="form-card">
            <label class="form-label">Type de contrat co-emprunteur</label>
            <select class="form-input" id="contrat2">
              <option value="aucun">Pas de co-emprunteur</option>
              <option value="cdi">CDI secteur privé</option>
              <option value="fonctionnaire">Fonctionnaire titulaire</option>
              <option value="retraite">Retraité(e)</option>
              <option value="cdd">CDD</option>
              <option value="ae">Auto-entrepreneur / Micro</option>
              <option value="tns">TNS / Indépendant</option>
              <option value="liberal">Profession libérale</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Revenus co-emprunteur</label>
            <input type="number" class="form-input" id="revenus2" placeholder="0 si pas de co-emprunteur" min="0" max="99999" step="1">
            <div class="form-hint">Montant exact en € — laisser 0 si pas de co-emprunteur</div>
          </div>
        </div>

        <div class="section-title">Revenus complémentaires</div>
        <div class="form-grid cols3">
          <div class="form-card">
            <label class="form-label">CAF / APL / AL</label>
            <select class="form-input" id="caf">
              <option value="non">Non</option>
              <option value="apl">APL / AL</option>
              <option value="caf_autre">Autre aide CAF</option>
              <option value="apl_caf">APL + aide CAF</option>
            </select>
            <div class="form-hint">APL : 70% chez CREATIS/CGI (100% si retraité)</div>
          </div>
          <div class="form-card">
            <label class="form-label">Pension alimentaire reçue</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'pension_recue','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'pension_recue','oui')">Oui</div>
            </div>
            <input type="hidden" id="pension_recue" value="non">
          </div>
          <div class="form-card">
            <label class="form-label">Revenus fonciers / locatifs</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'revenus_fonciers','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'revenus_fonciers','oui')">Oui</div>
            </div>
            <input type="hidden" id="revenus_fonciers" value="non">
          </div>
        </div>

        <div class="nav-buttons">
          <button class="btn-prev" onclick="goTo(0)">← Retour</button>
          <button class="btn-next" onclick="goTo(2)">Charges & Crédits →</button>
        </div>
      </div>

      <!-- ===== SECTION 3 : CHARGES & CREDITS ===== -->
      <div class="section-panel" id="section-2">
        <div class="panel-header">
          <h2>Charges & Encours crédits</h2>
          <p>Estimations par fourchettes — clé pour le calcul TEAP et RAV</p>
        </div>

        <div class="section-title">Charges hors crédits</div>
        <div class="form-grid cols3">
          <div class="form-card">
            <label class="form-label">Pension alimentaire versée</label>
            <select class="form-input" id="pension_versee">
              <option value="0">Aucune</option>
              <option value="moins300">Moins de 300 €/mois</option>
              <option value="300_600">300 — 600 €/mois</option>
              <option value="plus600">Plus de 600 €/mois</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Loyer actuel (si locataire)</label>
            <select class="form-input" id="loyer">
              <option value="0">Non applicable / Hébergé</option>
              <option value="moins500">Moins de 500 €/mois</option>
              <option value="500_800">500 — 800 €/mois</option>
              <option value="plus800">Plus de 800 €/mois</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Autres charges récurrentes visibles RDC</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'autres_charges','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'autres_charges','oui')">Oui</div>
            </div>
            <input type="hidden" id="autres_charges" value="non">
            <div class="form-hint">Virements tiers récurrents = 100% charges (CREATIS/SYGMA)</div>
          </div>
        </div>

        <div class="section-title">Encours crédits</div>
        <div class="form-grid cols3">
          <div class="form-card">
            <label class="form-label">Nombre de prêts consommation <span>*</span></label>
            <select class="form-input" id="nb_prets_conso">
              <option value="0">0</option>
              <option value="1">1</option>
              <option value="2">2</option>
              <option value="3">3</option>
              <option value="4">4</option>
              <option value="5">5+</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Nombre de revolving / réserves</label>
            <select class="form-input" id="nb_revolving">
              <option value="0">0</option>
              <option value="1">1</option>
              <option value="2">2</option>
              <option value="3">3+</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Crédit auto / LOA / LLD</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'credit_auto','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'credit_auto','oui')">Oui</div>
            </div>
            <input type="hidden" id="credit_auto" value="non">
          </div>
        </div>

        <div class="form-grid cols3">
          <div class="form-card">
            <label class="form-label">Mensualités crédits conso <span>*</span></label>
            <input type="number" class="form-input" id="mens_conso" placeholder="ex : 850" min="0" max="99999" step="1" oninput="calcTotalMens()">
            <div class="form-hint">Prêts perso + revolving + auto — crédits à <strong style="color:var(--green)">reprendre dans le RAC</strong></div>
          </div>
          <div class="form-card" style="border-color:rgba(245,158,11,0.35); background:linear-gradient(135deg,rgba(245,158,11,0.05),var(--card))">
            <label class="form-label" style="color:var(--gold)">Mensualité prêt immobilier <span>*</span></label>
            <input type="number" class="form-input" id="mens_immo" placeholder="ex : 420" min="0" max="99999" step="1" oninput="calcTotalMens()">
            <div class="form-hint" style="color:rgba(245,158,11,0.8)">Mensualité immo actuelle — <strong>reste inchangée en PP</strong>, reprise en LCC/LS2</div>
          </div>
          <div class="form-card">
            <label class="form-label">Total mensualités (calculé)</label>
            <div id="total_mens_display" style="font-family:var(--mono); font-size:22px; font-weight:700; color:var(--accent2); padding:8px 0;">— €</div>
            <input type="hidden" id="total_mensualites" value="0">
            <div class="form-hint">Conso + immo — mis à jour automatiquement</div>
          </div>
          <div class="form-card">
            <label class="form-label">Dettes hors crédits (huissier, impôts, copro)</label>
            <select class="form-input" id="dettes_hors_credits">
              <option value="non">Aucune</option>
              <option value="impots">Retard impôts uniquement</option>
              <option value="huissier">Dette huissier</option>
              <option value="copro">Charges de copropriété</option>
              <option value="multiple">Plusieurs dettes</option>
            </select>
            <div class="form-hint">Huissier : CREATIS OK si &lt;40% MAF. CL/SYGMA : refus</div>
          </div>
        </div>

        <div class="nav-buttons">
          <button class="btn-prev" onclick="goTo(1)">← Retour</button>
          <button class="btn-next" onclick="goTo(3)">Comportement Bancaire →</button>
        </div>
      </div>

      <!-- ===== SECTION 4 : COMPORTEMENT BANCAIRE ===== -->
      <div class="section-panel" id="section-3">
        <div class="panel-header">
          <h2>Comportement bancaire</h2>
          <p>Section critique — détermine l'éligibilité partenaire sur les incidents</p>
        </div>

        <div class="form-grid">
          <div class="form-card">
            <label class="form-label">Rejets de prélèvements (hors prêt immo) <span>*</span></label>
            <select class="form-input" id="nb_rejets">
              <option value="0">Aucun</option>
              <option value="1_5">1 à 5 rejets</option>
              <option value="6_10">6 à 10 rejets</option>
              <option value="11_14">11 à 14 rejets</option>
              <option value="15_20">15 à 20 rejets</option>
              <option value="plus20">Plus de 20 rejets</option>
            </select>
            <div class="form-hint">Seuls les rejets de prélèvement sont comptabilisés (pas virements ni RBT IMP)</div>
          </div>
          <div class="form-card">
            <label class="form-label">Rejet(s) sur prêt immobilier <span>*</span></label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'rejet_immo','non')">Aucun</div>
              <div class="radio-btn" onclick="selectRadio(this,'rejet_immo','1_2')">1 à 2 rejets</div>
              <div class="radio-btn" onclick="selectRadio(this,'rejet_immo','plus3')">3+ rejets</div>
            </div>
            <input type="hidden" id="rejet_immo" value="non">
            <div class="form-hint">CGI LS2 : 0 toléré. CFCAL LS2 : max 6. CREATIS LS2 : max 9</div>
          </div>
          <div class="form-card">
            <label class="form-label">FICP (fichage Banque de France)</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'ficp','non')">Non / Inconnu</div>
              <div class="radio-btn" onclick="selectRadio(this,'ficp','oui')">Oui FICP</div>
            </div>
            <input type="hidden" id="ficp" value="non">
          </div>
          <div class="form-card">
            <label class="form-label">FCC (fichage chèques)</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'fcc','non')">Non / Inconnu</div>
              <div class="radio-btn" onclick="selectRadio(this,'fcc','oui')">Oui FCC</div>
            </div>
            <input type="hidden" id="fcc" value="non">
          </div>
          <div class="form-card">
            <label class="form-label">Surendettement en cours ou passé récent</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'surendettement','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'surendettement','en_cours')">En cours</div>
              <div class="radio-btn" onclick="selectRadio(this,'surendettement','passe')">Passé soldé</div>
            </div>
            <input type="hidden" id="surendettement" value="non">
            <div class="form-hint">En cours : KO absolu tous partenaires</div>
          </div>
          <div class="form-card">
            <label class="form-label">Prêt au contentieux</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'contentieux','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'contentieux','oui')">Oui</div>
            </div>
            <input type="hidden" id="contentieux" value="non">
            <div class="form-hint">Prêt immo au contentieux : KO absolu</div>
          </div>
          <div class="form-card">
            <label class="form-label">Caution mutuelle activée</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'caution_mutuelle','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'caution_mutuelle','oui')">Oui</div>
            </div>
            <input type="hidden" id="caution_mutuelle" value="non">
            <div class="form-hint">KO tous partenaires sauf SYGMA sous conditions</div>
          </div>
          <div class="form-card">
            <label class="form-label">Déchéance du terme</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'decheance','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'decheance','oui')">Oui</div>
            </div>
            <input type="hidden" id="decheance" value="non">
            <div class="form-hint">KO absolu tous partenaires</div>
          </div>
        </div>

        <div class="nav-buttons">
          <button class="btn-prev" onclick="goTo(2)">← Retour</button>
          <button class="btn-next" onclick="goTo(4)">Projet & Trésorerie →</button>
        </div>
      </div>

      <!-- ===== SECTION 5 : PROJET ===== -->
      <div class="section-panel" id="section-4">
        <div class="panel-header">
          <h2>Projet & Trésorerie</h2>
          <p>Définit la structure du montage et les partenaires éligibles</p>
        </div>

        <div class="form-grid">
          <div class="form-card">
            <label class="form-label">Objectif principal <span>*</span></label>
            <select class="form-input" id="objectif">
              <option value="mensualites">Baisser les mensualités</option>
              <option value="tresorerie">Dégager de la trésorerie</option>
              <option value="travaux">Financer des travaux</option>
              <option value="dettes">Solder des dettes</option>
              <option value="mixte">Baisser mensualités + trésorerie</option>
            </select>
          </div>
          <div class="form-card">
            <label class="form-label">Objet de la trésorerie</label>
            <select class="form-input" id="objet_tresorerie">
              <option value="na">Non applicable</option>
              <option value="conso">Consommation / Non affecté</option>
              <option value="travaux_sans_permis">Travaux (sans permis de construire)</option>
              <option value="travaux_avec_permis">Travaux (avec permis de construire)</option>
              <option value="vehicule">Véhicule</option>
              <option value="voyage">Voyage / Loisirs</option>
            </select>
            <div class="form-hint">Travaux avec permis : KO CFCAL/SYGMA/LBP</div>
          </div>
          <div class="form-card">
            <label class="form-label">Part immobilière estimée dans le MAF</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn" onclick="selectRadio(this,'part_immo','moins60')">Moins de 60%</div>
              <div class="radio-btn" onclick="selectRadio(this,'part_immo','plus60')">Plus de 60%</div>
              <div class="radio-btn" onclick="selectRadio(this,'part_immo','inconnue')">Inconnue</div>
            </div>
            <input type="hidden" id="part_immo" value="inconnue">
            <div class="form-hint">&gt;60% = régime LS2. &lt;60% = régime LCC</div>
          </div>
        </div>

        <div class="section-title">MAF — Montant à financer</div>
        <div class="form-grid cols3">
          <div class="form-card" style="border-color: rgba(245,158,11,0.4); background: linear-gradient(135deg, rgba(245,158,11,0.06), var(--card));">
            <label class="form-label" style="color:var(--gold)">MAF total <span>*</span> <span style="color:var(--muted); font-size:10px; text-transform:none; letter-spacing:0">(Montant à financer)</span></label>
            <div style="display:flex; align-items:center; gap:8px;">
              <input type="number" class="form-input" id="maf" placeholder="ex : 85 000" min="0" max="9999999" step="100" oninput="calcMAF()" style="font-size:18px; font-weight:700; color:var(--gold);">
              <span style="color:var(--muted); font-family:var(--mono); font-size:13px; white-space:nowrap;">€</span>
            </div>
            <div class="form-hint" style="color:var(--gold); opacity:0.85">CRD conso + CRD immo + trésorerie + frais. Peut être calculé ci-dessous ↓</div>
          </div>
          <div class="form-card">
            <label class="form-label">Durée souhaitée (en mois) <span>*</span></label>
            <input type="number" class="form-input" id="duree" placeholder="ex : 180" min="12" max="420" step="6">
            <div class="form-hint">Durées max partenaires : PP 180m · LCC 300-420m · LS2 300m</div>
          </div>
          <div class="form-card">
            <label class="form-label">Doublon courtier</label>
            <div class="radio-group" style="margin-top:4px">
              <div class="radio-btn selected" onclick="selectRadio(this,'doublon','non')">Non</div>
              <div class="radio-btn" onclick="selectRadio(this,'doublon','oui')">Oui</div>
            </div>
            <input type="hidden" id="doublon" value="non">
            <div class="form-hint">Doublon : CFCAL = 1er déposant prime. MYMB : délai 3j max</div>
          </div>
        </div>

        <div class="section-title" style="margin-top:8px">Calculateur MAF automatique <span style="color:var(--muted); font-size:10px; font-family:var(--mono); text-transform:none; letter-spacing:0; margin-left:8px">— optionnel, remplit le MAF ci-dessus</span></div>
        <div class="form-grid cols3">
          <div class="form-card">
            <label class="form-label">CRD crédits conso à reprendre</label>
            <input type="number" class="form-input" id="crd_conso" placeholder="ex : 32 000" min="0" step="100" oninput="calcMAF()">
            <div class="form-hint">Somme des capitaux restants dus conso + revolving</div>
          </div>
          <div class="form-card">
            <label class="form-label">CRD immobilier à reprendre</label>
            <input type="number" class="form-input" id="crd_immo_exact" placeholder="ex : 45 000" min="0" step="100" oninput="calcMAF()">
            <div class="form-hint">CRD prêt immobilier à racheter (0 si conservé ou inexistant)</div>
          </div>
          <div class="form-card">
            <label class="form-label">Trésorerie souhaitée</label>
            <input type="number" class="form-input" id="tresorerie_exacte" placeholder="ex : 8 000" min="0" step="100" oninput="calcMAF()">
            <div class="form-hint">Montant exact de l'enveloppe trésorerie demandée</div>
          </div>
          <div class="form-card">
            <label class="form-label">Dettes hors crédits à intégrer</label>
            <input type="number" class="form-input" id="dettes_montant" placeholder="ex : 3 500" min="0" step="100" oninput="calcMAF()">
            <div class="form-hint">Huissier, impôts, copropriété à racheter</div>
          </div>
          <div class="form-card">
            <label class="form-label">Frais de dossier estimés</label>
            <input type="number" class="form-input" id="frais_dossier" placeholder="ex : 3 200" min="0" step="100" oninput="calcMAF()">
            <div class="form-hint">Honoraires courtier + frais de garantie (si hypo)</div>
          </div>
          <div class="form-card" style="background: rgba(16,185,129,0.06); border-color: rgba(16,185,129,0.3);">
            <label class="form-label" style="color:var(--green)">MAF calculé automatiquement</label>
            <div style="font-family:var(--mono); font-size:22px; font-weight:700; color:var(--green); padding:6px 0;" id="maf_calcule">— €</div>
            <div class="form-hint" style="color:var(--green); opacity:0.8">Cliquer pour reporter dans le MAF ↑</div>
            <button onclick="reporterMAF()" style="margin-top:8px; padding:6px 14px; background:rgba(16,185,129,0.2); border:1px solid rgba(16,185,129,0.4); color:var(--green); border-radius:6px; font-family:var(--mono); font-size:11px; cursor:pointer; transition:all 0.15s;" onmouseover="this.style.background='rgba(16,185,129,0.35)'" onmouseout="this.style.background='rgba(16,185,129,0.2)'">↑ Reporter ce montant</button>
          </div>
        </div>

        <div class="nav-buttons">
          <button class="btn-prev" onclick="goTo(3)">← Retour</button>
          <button class="btn-next" onclick="analyser()">⚡ Lancer l'analyse</button>
        </div>
      </div>

      <!-- ===== SECTION RÉSULTAT ===== -->
      <div class="section-panel" id="section-5">
        <div id="result-content"></div>
        <button class="btn-reset" onclick="goTo(0)">← Nouveau dossier</button>
      </div>

    </div><!-- /content -->
  </div><!-- /main -->
</div><!-- /app -->

<script>
let currentSection = 0;
const totalSteps = 5;

function goTo(n) {
  document.querySelectorAll('.section-panel').forEach(p => p.classList.remove('active'));
  document.getElementById('section-' + n).classList.add('active');

  document.querySelectorAll('.nav-item').forEach((item, i) => {
    item.classList.remove('active', 'done');
    if (i === n) item.classList.add('active');
    else if (i < n) item.classList.add('done');
  });

  // Update step numbers
  for (let i = 0; i < 6; i++) {
    const sn = document.getElementById('stepnum' + i);
    if (!sn) continue;
    if (i < n) sn.textContent = '✓';
    else if (i === 5) sn.textContent = '⚡';
    else sn.textContent = i + 1;
  }

  const pct = n === 5 ? 100 : Math.round((n / totalSteps) * 100);
  document.getElementById('progressFill').style.width = pct + '%';
  document.getElementById('progressLabel').textContent = n === 5 ? 'Analyse complète' : `Étape ${n + 1}/${totalSteps}`;

  currentSection = n;
  window.scrollTo(0, 0);
}

function selectRadio(el, fieldId, value) {
  const parent = el.parentElement;
  parent.querySelectorAll('.radio-btn').forEach(b => b.classList.remove('selected'));
  el.classList.add('selected');
  document.getElementById(fieldId).value = value;
}

function toggleImmo() {
  const val = document.getElementById('statut_logement').value;
  document.getElementById('immo_section').style.display = val === 'proprietaire' ? 'block' : 'none';
}

function toggleForcePP() {
  const val = document.getElementById('statut_logement').value;
  const card = document.getElementById('force_pp_card');
  if (val === 'proprietaire') {
    card.style.display = 'block';
  } else {
    card.style.display = 'none';
    // Reset to non when not proprietaire
    document.getElementById('force_pp').value = 'non';
    card.querySelectorAll('.radio-btn').forEach((b, i) => {
      b.classList.toggle('selected', i === 0);
    });
  }
}

function getVal(id) {
  const el = document.getElementById(id);
  return el ? el.value : '';
}

// ===== MOTEUR D'ANALYSE =====
function calcTotalMens() {
  const conso = parseFloat(document.getElementById('mens_conso').value) || 0;
  const immo = parseFloat(document.getElementById('mens_immo').value) || 0;
  const total = conso + immo;
  document.getElementById('total_mensualites').value = total;
  document.getElementById('total_mens_display').textContent = total > 0 ? total.toLocaleString('fr') + ' €' : '— €';
}

function calcMAF() {
  const crdConso = parseFloat(document.getElementById('crd_conso').value) || 0;
  const crdImmo = parseFloat(document.getElementById('crd_immo_exact').value) || 0;
  const treso = parseFloat(document.getElementById('tresorerie_exacte').value) || 0;
  const dettes = parseFloat(document.getElementById('dettes_montant').value) || 0;
  const frais = parseFloat(document.getElementById('frais_dossier').value) || 0;
  const total = crdConso + crdImmo + treso + dettes + frais;
  const el = document.getElementById('maf_calcule');
  el.textContent = total > 0 ? total.toLocaleString('fr') + ' €' : '— €';
  el.dataset.val = total;
}

function reporterMAF() {
  const el = document.getElementById('maf_calcule');
  const val = parseFloat(el.dataset.val) || 0;
  if (val > 0) {
    document.getElementById('maf').value = val;
    // Flash confirmation
    const mafInput = document.getElementById('maf');
    mafInput.style.borderColor = 'var(--green)';
    mafInput.style.boxShadow = '0 0 0 3px rgba(16,185,129,0.25)';
    setTimeout(() => {
      mafInput.style.borderColor = '';
      mafInput.style.boxShadow = '';
    }, 1500);
  }
}

function analyser() {
  const d = {
    annee1: parseInt(getVal('annee_naissance')) || 1970,
    annee2: parseInt(getVal('annee_naissance2')) || 0,
    statut: getVal('statut_logement'),
    crd_immo: getVal('crd_immo'),
    valeur_bien: getVal('valeur_bien'),
    rang_hypo: getVal('rang_hypo'),
    pret_immo: getVal('pret_immo_encours'),
    rac_anterieur: getVal('rac_anterieur'),
    contrat1: getVal('contrat1'),
    anciennete1: getVal('anciennete1'),
    revenus1: getVal('revenus1'),
    contrat2: getVal('contrat2'),
    revenus2: getVal('revenus2'),
    arret_maladie: getVal('arret_maladie'),
    caf: getVal('caf'),
    nb_prets: parseInt(getVal('nb_prets_conso')) || 0,
    nb_revolving: parseInt(getVal('nb_revolving')) || 0,
    credit_auto: getVal('credit_auto'),
    total_mens: getVal('total_mensualites'),
    mens_conso: parseFloat(getVal('mens_conso')) || 0,
    mens_immo: parseFloat(getVal('mens_immo')) || 0,
    dettes: getVal('dettes_hors_credits'),
    pension: getVal('pension_versee'),
    nb_rejets: getVal('nb_rejets'),
    rejet_immo: getVal('rejet_immo'),
    ficp: getVal('ficp'),
    fcc: getVal('fcc'),
    surendettement: getVal('surendettement'),
    contentieux: getVal('contentieux'),
    caution_mutuelle: getVal('caution_mutuelle'),
    decheance: getVal('decheance'),
    objectif: getVal('objectif'),
    tresorerie: getVal('tresorerie_exacte'),
    objet_tresorerie: getVal('objet_tresorerie'),
    part_immo: getVal('part_immo'),
    maf: parseFloat(getVal('maf')) || 0,
    duree: parseInt(getVal('duree')) || 0,
    divorce: getVal('divorce'),
    nationalite: getVal('nationalite'),
    nb_enfants: parseInt(getVal('nb_enfants')) || 0,
    force_pp: getVal('force_pp'),
  };

  const now = new Date().getFullYear();
  const age1 = now - d.annee1;
  const age2 = d.annee2 ? now - d.annee2 : 0;
  const ageMax = Math.max(age1, age2 || 0);

  // TEAV estimé (toutes mensualités actuelles)
  const rev1 = parseFloat(getVal('revenus1')) || 0;
  const rev2 = parseFloat(getVal('revenus2')) || 0;
  const revTotal = rev1 + rev2;
  const mensConso = d.mens_conso;
  const mensImmo = d.mens_immo;
  const mensTotal = mensConso + mensImmo;
  const teav = revTotal > 0 ? Math.round((mensTotal / revTotal) * 100) : 0;

  // Orientation montage (calculée avant TEAP car TEAP en dépend)
  let montages = [];
  if (d.force_pp === 'oui') {
    montages = ['PP'];
  } else if (d.statut === 'proprietaire') {
    if (d.part_immo === 'plus60' || d.crd_immo === 'plus150' || d.crd_immo === '80_150') {
      montages = ['LS2', 'LCC'];
    } else {
      montages = ['LCC'];
      if (d.crd_immo === '0') montages.push('PP');
    }
  } else {
    montages = ['PP'];
  }

  const isPP = montages.length === 1 && montages[0] === 'PP';

  // TEAP post-RAC : distingue PP vs LCC/LS2
  // En PP : la mensualité immo reste inchangée, seul le conso est regroupé (-35%)
  // En LCC/LS2 : tout est repris, gain global estimé à -35%
  let mensPostRac, teap, rav;
  if (isPP) {
    // Conso regroupé avec gain ~35%, immo reste identique
    const mensConsoPostRac = Math.round(mensConso * 0.65);
    mensPostRac = mensConsoPostRac + mensImmo;
  } else {
    // Tout repris : gain global ~35%
    mensPostRac = Math.round(mensTotal * 0.65);
  }
  teap = revTotal > 0 ? Math.round((mensPostRac / revTotal) * 100) : 0;
  rav = revTotal - mensPostRac;

  // KO absolus
  const koAbsolus = [];
  if (d.surendettement === 'en_cours') koAbsolus.push('🔴 Surendettement en cours — KO absolu tous partenaires');
  if (d.decheance === 'oui') koAbsolus.push('🔴 Déchéance du terme — KO absolu tous partenaires');
  if (d.contentieux === 'oui') koAbsolus.push('🔴 Prêt immobilier au contentieux — KO absolu');
  if (d.ficp === 'oui') koAbsolus.push('🔴 Fichage FICP — quasi-rédhibitoire (seul CFCAL hypowash 2 possible)');
  if (d.fcc === 'oui') koAbsolus.push('🔴 Fichage FCC — KO général (seul CFCAL sous conditions)');
  if (d.caution_mutuelle === 'oui') koAbsolus.push('🔴 Caution mutuelle activée — KO tous sauf SYGMA');
  if (d.contrat1 === 'sans' && d.contrat2 === 'aucun') koAbsolus.push('🔴 Aucun revenu stable — financement impossible');
  if (d.objet_tresorerie === 'travaux_avec_permis') koAbsolus.push('🔴 Travaux avec permis de construire — KO CFCAL/SYGMA/LBP');
  if (d.arret_maladie === 'long') koAbsolus.push('🔴 Arrêt maladie >15 jours — KO quasi-général (seul YOUNITED OK si ≤15j)');

  // Règle TEAP max PP selon rejets
  const rejetsNum = { '0': 0, '1_5': 3, '6_10': 8, '11_14': 12, '15_20': 17, 'plus20': 25 };
  const nbRejets = rejetsNum[d.nb_rejets] || 0;
  const teapMaxPP = nbRejets >= 5 ? 45 : 50;
  const teapDepassePP = isPP && teap > teapMaxPP;
  if (teapDepassePP) {
    koAbsolus.push(`🔴 TEAP post-RAC PP estimé ${teap}% > ${teapMaxPP}% max (${nbRejets >= 5 ? '≥5 rejets → 45%' : 'sans rejet → 50%'}) — montage PP non finançable en l'état`);
  }

  // Analyse partenaires
  const partners = analysePartenaires(d, age1, age2, ageMax, teav, teap, rav, montages, teapMaxPP, teapDepassePP);

  // Verdict global
  const eligibles = partners.filter(p => p.statut === 'eligible').length;
  const partiels = partners.filter(p => p.statut === 'partiel').length;

  let verdict, verdictClass, verdictEmoji;
  if (koAbsolus.length > 0) {
    verdict = 'Non finançable'; verdictClass = 'rouge'; verdictEmoji = '🔴';
  } else if (eligibles >= 2) {
    verdict = 'Finançable'; verdictClass = 'vert'; verdictEmoji = '✅';
  } else if (eligibles >= 1 || partiels >= 2) {
    verdict = 'À étudier'; verdictClass = 'orange'; verdictEmoji = '🟠';
  } else if (partiels >= 1) {
    verdict = 'Incertain'; verdictClass = 'orange'; verdictEmoji = '🟠';
  } else {
    verdict = 'Non finançable'; verdictClass = 'rouge'; verdictEmoji = '🔴';
  }

  // Montage recommandé
  const montageLabel = montages.includes('LS2') ? 'LS2' : montages.includes('LCC') ? 'LCC' : 'PP';
  const montageClass = montageLabel.toLowerCase();

  // Générer note analyste
  const note = genNote(d, age1, age2, teav, teap, rav, montages, partners, verdictClass, rev1, rev2, revTotal, mensTotal, mensConso, mensImmo, isPP);

  // Checklist pièces

  // AFFICHAGE
  const rc = document.getElementById('result-content');
  rc.innerHTML = `
    <div class="result-hero ${verdictClass}">
      <div class="result-verdict">${verdictEmoji}<\/div>
      <div class="result-label ${verdictClass}">${verdict}<\/div>
      <div style="margin:12px 0">
        ${montages.map(m => `<span class="montage-badge ${m.toLowerCase()}">${m}<\/span>`).join('')}
      <\/div>
      <div class="result-summary">
        ${d.force_pp === 'oui' ? '⚠️ Montage forcé en PP (sans garantie) — LCC et LS2 exclus de l\'analyse.<br>' : ''}
        ${isPP && mensImmo > 0 ? '<strong style="color:var(--orange)">⚠️ PP : mensualité immo ' + mensImmo.toLocaleString('fr') + ' €/mois maintenue hors RAC.<\/strong><br>' : ''}
        ${verdictClass === 'rouge' ? 'Des blocages majeurs empêchent le montage.' : ''}
        ${verdictClass === 'vert' ? `Dossier présentable chez ${eligibles} partenaire(s). TEAP estimé ${teap}% — RAV estimé ${rav > 0 ? rav.toLocaleString('fr') + ' €' : 'à préciser'}.` : ''}
        ${verdictClass === 'orange' ? `Dossier à affiner. ${eligibles} partenaire(s) OK, ${partiels} sous conditions. Vérifier les points de vigilance avant envoi.` : ''}
      <\/div>
    <\/div>

    ${koAbsolus.length > 0 ? `
    <div class="blocking-box">
      <div class="blocking-title">⛔ Points bloquants identifiés<\/div>
      <div class="blocking-items">
        ${koAbsolus.map(k => `<div class="blocking-item"><span>→<\/span><span>${k}<\/span><\/div>`).join('')}
      <\/div>
    <\/div>` : ''}

    <div class="result-grid" style="grid-template-columns: repeat(5, 1fr);">
      <div class="result-kpi">
        <div class="kpi-val ${teav > 90 ? 'bad' : teav > 70 ? 'warn' : 'good'}">${teav > 0 ? teav + '%' : 'N/A'}<\/div>
        <div class="kpi-label">TEAV actuel<\/div>
      <\/div>
      <div class="result-kpi">
        <div class="kpi-val ${teap > 50 ? 'bad' : teap > 45 ? 'warn' : 'good'}">${teap > 0 ? teap + '%' : 'N/A'}<\/div>
        <div class="kpi-label">TEAP post-RAC estimé<\/div>
      <\/div>
      <div class="result-kpi">
        <div class="kpi-val ${rav < 700 ? 'bad' : rav < 1200 ? 'warn' : 'good'}">${rav > 0 ? rav.toLocaleString('fr') + ' €' : 'N/A'}<\/div>
        <div class="kpi-label">RAV estimé / mois<\/div>
      <\/div>
      <div class="result-kpi">
        <div class="kpi-val" style="font-size:26px;">${d.maf > 0 ? Number(d.maf).toLocaleString('fr') + ' €' : 'N/A'}<\/div>
        <div class="kpi-label">MAF<\/div>
      <\/div>
      <div class="result-kpi">
        <div class="kpi-val" style="font-size:26px;">${d.duree > 0 ? d.duree + ' mois' : 'N/A'}<\/div>
        <div class="kpi-label">Durée souhaitée<\/div>
      <\/div>
    <\/div>

    <div class="section-title">Éligibilité par partenaire<\/div>
    <div class="partner-grid">
      ${partners.map(p => `
        <div class="partner-card ${p.statut === 'eligible' ? 'eligible' : p.statut === 'partiel' ? 'partiel' : 'non-eligible'}">
          <div class="partner-header">
            <div class="partner-name">${p.nom}<\/div>
            <div class="partner-badge ${p.statut === 'eligible' ? 'ok' : p.statut === 'partiel' ? 'partiel' : 'ko'}">
              ${p.statut === 'eligible' ? '✓ ÉLIGIBLE' : p.statut === 'partiel' ? '~ SOUS CONDITIONS' : '✗ KO'}
            <\/div>
          <\/div>
          <ul class="partner-rules">
            ${p.regles.map(r => `<li class="partner-rule ${r.type}"><span class="dot">${r.type === 'ok' ? '✓' : r.type === 'warn' ? '⚠' : '✗'}<\/span><span>${r.text}<\/span><\/li>`).join('')}
          <\/ul>
        <\/div>
      `).join('')}
    <\/div>

    <div class="section-title" style="margin-top:24px">Note analyste — Copier-coller<\/div>
    <div class="note-box">
      <div class="note-box-header">
        <span class="form-label" style="margin:0">TEMPLATE NOTE ANALYSTE<\/span>
        <button class="copy-btn" onclick="copyNote()">📋 Copier<\/button>
      <\/div>
      <div id="note-analyste">${note}<\/div>
    <\/div>

    <div class="section-title">Export<\/div>
    <div style="display:flex;gap:12px;align-items:center;flex-wrap:wrap;margin-bottom:24px;">
      <button onclick="exportPDF(partners, montages, d, teap, teav, rav)" style="display:flex;align-items:center;gap:8px;padding:11px 22px;background:var(--accent);color:white;border:none;border-radius:10px;font-family:var(--sans);font-size:13px;font-weight:700;cursor:pointer;box-shadow:0 2px 10px rgba(59,130,246,.3);transition:all .18s;" onmouseover="this.style.background='#2563EB'" onmouseout="this.style.background='var(--accent)'">
        📄 Télécharger PDF partenaires
      <\/button>
      <span style="font-size:11px;color:var(--muted);font-family:var(--mono)">Synthèse éligibilité · statut · points clés<\/span>
    <\/div>
  `;

  // Switch to result section without calling analyser() again
  document.querySelectorAll('.section-panel').forEach(p => p.classList.remove('active'));
  document.getElementById('section-5').classList.add('active');
  document.querySelectorAll('.nav-item').forEach((item, i) => {
    item.classList.remove('active', 'done');
    if (i === 5) item.classList.add('active');
    else item.classList.add('done');
  });
  for (let i = 0; i < 6; i++) {
    const sn = document.getElementById('stepnum' + i);
    if (!sn) continue;
    sn.textContent = i === 5 ? '⚡' : '✓';
  }
  document.getElementById('progressFill').style.width = '100%';
  document.getElementById('progressLabel').textContent = 'Analyse complète';
  currentSection = 5;
  window.scrollTo(0, 0);
}

function analysePartenaires(d, age1, age2, ageMax, teav, teap, rav, montages, teapMaxPP, teapDepassePP) {
  const now = new Date().getFullYear();
  const hasMontageHypo = montages.includes('LCC') || montages.includes('LS2');
  const hasMontageLS2 = montages.includes('LS2');
  const isPP = montages.length === 1 && montages[0] === 'PP';

  const maf = (d.maf || 0) / 1000; // converti en k€ pour les comparaisons

  const rejetNum = { '0': 0, '1_5': 3, '6_10': 8, '11_14': 12, '15_20': 17, 'plus20': 25 };
  const rejets = rejetNum[d.nb_rejets] || 0;

  const contratStable = ['cdi', 'fonctionnaire', 'retraite', 'liberal'];
  const c1stable = contratStable.includes(d.contrat1);
  const c2stable = d.contrat2 !== 'aucun' && contratStable.includes(d.contrat2);

  const fiKO = d.ficp === 'oui' || d.fcc === 'oui' || d.surendettement === 'en_cours' || d.decheance === 'oui' || d.contentieux === 'oui';

  function makeRule(text, type) { return { text, type }; }

  // Helper : ajoute la règle TEAP max PP à une liste de règles
  function addTeapPPRule(regles, partnerOkRef) {
    if (!isPP) return partnerOkRef;
    const limite = teapMaxPP;
    const label = rejets >= 5 ? `≥5 rejets → max ${limite}%` : `sans rejet significatif → max ${limite}%`;
    if (teapDepassePP) {
      regles.push(makeRule(`TEAP PP estimé ${teap}% > ${limite}% max PP (${label})`, 'ko'));
      return false;
    } else {
      regles.push(makeRule(`TEAP PP estimé ${teap}% ≤ ${limite}% max PP (${label})`, 'ok'));
      return partnerOkRef;
    }
  }

  // CREATIS
  const creatisRegles = [];
  let creatisOk = true;
  if (fiKO) { creatisRegles.push(makeRule('FICP/FCC/Contentieux/Surendettement : KO', 'ko')); creatisOk = false; }
  if (hasMontageLS2 && rejets > 9) { creatisRegles.push(makeRule(`LS2 : max 9 rejets — ${rejets} détectés`, 'ko')); creatisOk = false; }
  else if (!hasMontageLS2 && rejets > 14) { creatisRegles.push(makeRule(`LCC/PP : max 14 rejets — ${rejets} détectés`, 'ko')); creatisOk = false; }
  else { creatisRegles.push(makeRule('Rejets dans les normes', 'ok')); }
  if (d.rac_anterieur === 'moins1an') { creatisRegles.push(makeRule('RAC <1 an : produit Fusion impossible (RAC >2 ans requis)', 'warn')); }
  if (!c1stable && !c2stable) { creatisRegles.push(makeRule('Contrat atypique : co-emprunteur CDI/fonc requis si AE', 'warn')); }
  if (hasMontageHypo && maf >= 50) { creatisRegles.push(makeRule(`MAF LCC ≥ 50k€ OK (min 50k€ hypo)`, 'ok')); }
  else if (hasMontageHypo && maf < 50) { creatisRegles.push(makeRule(`MAF LCC ${maf}k€ < 50k€ min hypo`, 'ko')); creatisOk = false; }
  if (!hasMontageHypo && maf >= 7.5) { creatisRegles.push(makeRule('MAF PP OK', 'ok')); }
  if (d.rejet_immo === 'plus3' && hasMontageLS2) { creatisRegles.push(makeRule('LS2 : max 2 rejets immo tolérés', 'warn')); }
  if (d.dettes === 'huissier') { creatisRegles.push(makeRule('Dette huissier : OK si <40% MAF', 'warn')); }
  if (creatisOk && !fiKO) { creatisRegles.push(makeRule('Profil globalement éligible', 'ok')); }
  creatisOk = addTeapPPRule(creatisRegles, creatisOk);

  // CGI
  const cgiRegles = [];
  let cgiOk = true;
  if (fiKO) { cgiRegles.push(makeRule('FICP/FCC/Contentieux : KO', 'ko')); cgiOk = false; }
  if (hasMontageLS2 && rejets > 0) { cgiRegles.push(makeRule(`LS2 : 0 rejet toléré — ${rejets} détectés`, 'ko')); cgiOk = false; }
  else if (!hasMontageLS2 && rejets > 20) { cgiRegles.push(makeRule(`LCC : max 20 rejets — ${rejets} détectés`, 'ko')); cgiOk = false; }
  else { cgiRegles.push(makeRule('Rejets dans normes CGI', 'ok')); }
  if (d.rejet_immo !== 'non' && hasMontageLS2) { cgiRegles.push(makeRule('LS2 : 0 rejet toléré sur immo', 'ko')); cgiOk = false; }
  if (maf < 30 && hasMontageHypo) { cgiRegles.push(makeRule(`MAF ${maf}k€ < 30k€ min LCC CGI`, 'ko')); cgiOk = false; }
  if (age1 >= 80 || (age2 && age2 >= 80)) { cgiRegles.push(makeRule('Âge dépassé : CGI max fin < 80 ans', 'ko')); cgiOk = false; }
  else if (age1 >= 70 || (age2 && age2 >= 70)) { cgiRegles.push(makeRule('Âge : max début < 70 ans chez CGI', 'warn')); }
  if (d.rac_anterieur === 'moins1an') { cgiRegles.push(makeRule('RAC <1 an : TEAV max 50%', 'warn')); }
  if (d.dettes === 'huissier') { cgiRegles.push(makeRule('Dette huissier : OK chez CGI', 'ok')); }
  if (cgiOk && !fiKO) { cgiRegles.push(makeRule('Profil éligible CGI', 'ok')); }
  cgiOk = addTeapPPRule(cgiRegles, cgiOk);

  // CFCAL
  const cfcalRegles = [];
  let cfcalStat = 'eligible';
  if (fiKO && d.ficp !== 'oui') { cfcalRegles.push(makeRule('FCC/Contentieux : KO', 'ko')); cfcalStat = 'non'; }
  if (d.ficp === 'oui' && hasMontageHypo) { cfcalRegles.push(makeRule('FICP : possible en LCC (hypowash 2)', 'warn')); cfcalStat = 'partiel'; }
  if (hasMontageLS2 && rejets > 6) { cfcalRegles.push(makeRule(`LS2 : max 6 rejets — ${rejets} détectés`, 'ko')); cfcalStat = 'non'; }
  else if (!hasMontageLS2 && rejets === 0) { cfcalRegles.push(makeRule('Aucun rejet — profil idéal CFCAL', 'ok')); }
  if (d.objet_tresorerie === 'travaux_avec_permis') { cfcalRegles.push(makeRule('Travaux avec permis : KO CFCAL', 'ko')); cfcalStat = 'non'; }
  if (d.rac_anterieur === 'moins1an') { cfcalRegles.push(makeRule('RAC <1 an : pas de norme spécifique CFCAL', 'ok')); }
  if (maf < 22 && hasMontageHypo) { cfcalRegles.push(makeRule(`MAF ${maf}k€ < 22k€ min CFCAL`, 'ko')); cfcalStat = 'non'; }
  if (d.dettes === 'huissier' && hasMontageLS2) { cfcalRegles.push(makeRule('Dette huissier : KO en LS2 CFCAL', 'warn')); cfcalStat = cfcalStat === 'eligible' ? 'partiel' : cfcalStat; }
  if (cfcalStat === 'eligible') { cfcalRegles.push(makeRule('Éligible CFCAL (durée max 420m!)', 'ok')); }
  if (isPP && teapDepassePP) { cfcalRegles.push(makeRule(`TEAP PP estimé ${teap}% > ${teapMaxPP}% max PP`, 'ko')); cfcalStat = 'non'; }
  else if (isPP) { cfcalRegles.push(makeRule(`TEAP PP estimé ${teap}% ≤ ${teapMaxPP}% max PP`, 'ok')); }

  // MYMB
  const mymbRegles = [];
  let mymbOk = true;
  if (fiKO) { mymbRegles.push(makeRule('FICP/FCC/Contentieux : KO', 'ko')); mymbOk = false; }
  if (d.rac_anterieur === 'moins1an') { mymbRegles.push(makeRule('RAC <1 an : KO MYMB (RAC doit avoir >1 an)', 'ko')); mymbOk = false; }
  else { mymbRegles.push(makeRule('Ancienneté RAC OK', 'ok')); }
  if (d.rejet_immo !== 'non') { mymbRegles.push(makeRule('Rejet prêt immo : 0 toléré (produit S/2X)', 'ko')); mymbOk = false; }
  if (hasMontageLS2 && maf < 100) { mymbRegles.push(makeRule(`LS2 : min 100k€ MAF — ${maf}k€ détecté`, 'ko')); mymbOk = false; }
  if (!hasMontageLS2 && maf < 30) { mymbRegles.push(makeRule(`LCC : min 30k€ MAF`, 'warn')); }
  if (d.dettes === 'huissier' || d.dettes === 'multiple') { mymbRegles.push(makeRule('Dettes : profil M requis (produit étendu)', 'warn')); }
  if (age1 > 85) { mymbRegles.push(makeRule('Âge max MYMB : 85 ans 11 mois', 'ko')); mymbOk = false; }
  if (mymbOk && !fiKO) { mymbRegles.push(makeRule('Profil éligible MYMB', 'ok')); }
  mymbOk = addTeapPPRule(mymbRegles, mymbOk);

  // CL (Crédit Lift)
  const clRegles = [];
  let clOk = true;
  if (fiKO) { clRegles.push(makeRule('FICP/FCC/Contentieux : KO', 'ko')); clOk = false; }
  if (rejets > 0 && hasMontageLS2) { clRegles.push(makeRule('LS2 : rejets à vérifier (doivent être régularisés)', 'warn')); }
  if (d.rac_anterieur === 'moins1an' && hasMontageLS2) { clRegles.push(makeRule('LS2 : RAC <1 an KO', 'ko')); clOk = false; }
  if (hasMontageHypo && maf < 80) { clRegles.push(makeRule(`LCC CL : min 80k€ MAF — ${maf}k€ détecté`, 'ko')); clOk = false; }
  if (d.dettes === 'huissier') { clRegles.push(makeRule('Dette huissier : KO CL', 'ko')); clOk = false; }
  if (d.nb_prets + d.nb_revolving > 16) { clRegles.push(makeRule('Max 16 prêts externes (CL)', 'warn')); }
  if (age1 > 90) { clRegles.push(makeRule('Âge max CL : 90 ans', 'ko')); clOk = false; }
  if (clOk && !fiKO) { clRegles.push(makeRule('Éligible CL (Hypolift / Cautiolift)', 'ok')); }
  clOk = addTeapPPRule(clRegles, clOk);

  // SYGMA
  const sygmaRegles = [];
  let sygmaOk = true;
  if (fiKO && d.caution_mutuelle !== 'oui') { sygmaRegles.push(makeRule('FICP/FCC/Contentieux : KO', 'ko')); sygmaOk = false; }
  if (d.caution_mutuelle === 'oui') { sygmaRegles.push(makeRule('Caution mutuelle : SYGMA = exception sous conditions', 'warn')); }
  if (hasMontageHypo && maf < 30) { sygmaRegles.push(makeRule(`LCC : min 30k€ MAF`, 'warn')); }
  if (d.objet_tresorerie === 'travaux_avec_permis') { sygmaRegles.push(makeRule('Travaux avec permis : KO SYGMA', 'ko')); sygmaOk = false; }
  if (age1 > 85) { sygmaRegles.push(makeRule('Âge max SYGMA : 85 ans', 'ko')); sygmaOk = false; }
  if (age1 < 21) { sygmaRegles.push(makeRule('Âge min SYGMA : 21 ans', 'ko')); sygmaOk = false; }
  if (d.rac_anterieur === 'moins1an') { sygmaRegles.push(makeRule('RAC <1 an : 1ère mensualité doit être passée', 'warn')); }
  if (sygmaOk && !fiKO) { sygmaRegles.push(makeRule('Profil éligible SYGMA (dérogation 50% TEAP possible)', 'ok')); }
  sygmaOk = addTeapPPRule(sygmaRegles, sygmaOk);

  // YOUNITED
  const younRegles = [];
  let younOk = true;
  if (fiKO) { younRegles.push(makeRule('FICP/FCC/Contentieux : KO', 'ko')); younOk = false; }
  if (hasMontageHypo) { younRegles.push(makeRule('YOUNITED = sans garantie uniquement (PP)', 'warn')); younOk = montages.includes('PP'); }
  if (!montages.includes('PP') && !hasMontageHypo) { younRegles.push(makeRule('PP possible', 'ok')); }
  if (d.arret_maladie === 'long') { younRegles.push(makeRule('Arrêt maladie >15j : KO YOUNITED', 'ko')); younOk = false; }
  else if (d.arret_maladie === 'court') { younRegles.push(makeRule('Arrêt maladie ≤15j : OK YOUNITED', 'ok')); }
  if (rejets > 4) { younRegles.push(makeRule(`YOUNITED : max 4 rejets — ${rejets} détectés`, 'ko')); younOk = false; }
  if (maf > 50) { younRegles.push(makeRule('MAF max YOUNITED : 50k€', 'ko')); younOk = false; }
  if (age1 >= 80) { younRegles.push(makeRule('Âge max YOUNITED : <80 ans 365j à la souscription', 'ko')); younOk = false; }
  if (younOk && !fiKO) { younRegles.push(makeRule('Éligible YOUNITED PP', 'ok')); }
  younOk = addTeapPPRule(younRegles, younOk);

  // LBP
  const lbpRegles = [];
  let lbpOk = true;
  if (fiKO) { lbpRegles.push(makeRule('FICP/FCC/Contentieux : KO', 'ko')); lbpOk = false; }
  if (d.rac_anterieur === 'moins1an') { lbpRegles.push(makeRule('RAC <1 an : KO LBP (>1 an requis)', 'ko')); lbpOk = false; }
  if (d.objet_tresorerie === 'travaux_avec_permis') { lbpRegles.push(makeRule('Travaux avec permis : KO LBP', 'ko')); lbpOk = false; }
  if (maf > 100 && hasMontageHypo) { lbpRegles.push(makeRule('MAF max LBP hypo : 100k€', 'ko')); lbpOk = false; }
  if (parseFloat(d.tresorerie) > 21500) { lbpRegles.push(makeRule('Tréso max LBP : 21 500€', 'ko')); lbpOk = false; }
  if (age1 > 80) { lbpRegles.push(makeRule('Âge max LBP : 80 ans', 'ko')); lbpOk = false; }
  if (lbpOk && !fiKO) { lbpRegles.push(makeRule('Éligible LBP', 'ok')); }
  lbpOk = addTeapPPRule(lbpRegles, lbpOk);

  const toStatut = (ok) => ok ? 'eligible' : 'non';

  return [
    { nom: 'CREATIS', statut: (creatisOk && !fiKO) ? 'eligible' : fiKO ? 'non' : 'partiel', regles: creatisRegles },
    { nom: 'CGI', statut: (cgiOk && !fiKO) ? 'eligible' : fiKO ? 'non' : 'partiel', regles: cgiRegles },
    { nom: 'CFCAL', statut: cfcalStat === 'eligible' ? 'eligible' : cfcalStat === 'partiel' ? 'partiel' : 'non', regles: cfcalRegles },
    { nom: 'MYMB', statut: toStatut(mymbOk && !fiKO), regles: mymbRegles },
    { nom: 'CL', statut: toStatut(clOk && !fiKO), regles: clRegles },
    { nom: 'SYGMA', statut: toStatut(sygmaOk && !(fiKO && d.caution_mutuelle !== 'oui')), regles: sygmaRegles },
    { nom: 'LBP', statut: toStatut(lbpOk && !fiKO), regles: lbpRegles },
    { nom: 'YOUNITED', statut: toStatut(younOk && !fiKO), regles: younRegles },
  ];
}

function genNote(d, age1, age2, teav, teap, rav, montages, partners, verdictClass, rev1, rev2, revTotal, mensTotal, mensConso, mensImmo, isPP) {
  const contratLabel = { 'cdi': 'CDI secteur privé', 'fonctionnaire': 'Fonctionnaire titulaire', 'retraite': 'Retraité', 'cdd': 'CDD', 'interim': 'Intérimaire', 'ae': 'Auto-entrepreneur', 'tns': 'TNS/Indépendant', 'liberal': 'Profession libérale', 'chomage': 'Allocataire ARE', 'sans': 'Sans emploi' };
  const statLabel = { 'proprietaire': 'Propriétaire', 'locataire': 'Locataire', 'heberge': 'Hébergé' };
  const montageStr = montages.join(' / ');
  const eligible = partners.filter(p => p.statut === 'eligible').map(p => p.nom).join(', ') || 'Aucun';
  const conditionnel = partners.filter(p => p.statut === 'partiel').map(p => p.nom).join(', ') || 'Aucun';

  return `SITUATION LOGEMENT
Client ${statLabel[d.statut] || d.statut}. ${d.statut === 'proprietaire' ? `Bien immobilier : type ${d.type_bien || 'à préciser'}, valeur estimée ${d.valeur_bien || 'non renseignée'}, CRD immobilier ${d.crd_immo || 'non renseigné'}. Rang hypothécaire : ${d.rang_hypo}. RAC antérieur : ${d.rac_anterieur}.` : ''}

SITUATION PROFESSIONNELLE
Emprunteur 1 : ${contratLabel[d.contrat1] || d.contrat1}, ancienneté ${d.anciennete1}. ${d.contrat2 !== 'aucun' ? `Co-emprunteur : ${contratLabel[d.contrat2] || d.contrat2}.` : 'Pas de co-emprunteur.'}

REVENUS ET CHARGES
Revenus mensuels nets : ${rev1 > 0 ? rev1.toLocaleString('fr') + ' €' : 'non renseigné'}${rev2 > 0 ? ' + co-emprunteur ' + rev2.toLocaleString('fr') + ' €' : ''} (total : ${revTotal.toLocaleString('fr')} €). TEAV actuel : ${teav}%.
Mensualités actuelles — Conso : ${mensConso > 0 ? mensConso.toLocaleString('fr') + ' €' : 'non renseigné'} | Immo : ${mensImmo > 0 ? mensImmo.toLocaleString('fr') + ' €' : '0 €'} | Total : ${mensTotal > 0 ? mensTotal.toLocaleString('fr') + ' €' : 'non renseigné'}. ${isPP && mensImmo > 0 ? 'PP : mensualité immo maintenue hors RAC.' : ''} Pension alimentaire versée : ${d.pension_versee}. ${d.dettes !== 'non' ? 'Dettes hors crédits : ' + d.dettes + '.' : ''}

ANALYSE DES ENCOURS
${d.nb_prets} prêt(s) consommation + ${d.nb_revolving} revolving + crédit auto : ${d.credit_auto}. Prêt immobilier : ${d.pret_immo_encours}. Part immobilière estimée dans MAF : ${d.part_immo}. Orientation montage : ${montageStr}. MAF : ${d.maf > 0 ? Number(d.maf).toLocaleString('fr') + ' €' : 'à préciser'}. Durée souhaitée : ${d.duree > 0 ? d.duree + ' mois' : 'à préciser'}. Trésorerie : ${d.tresorerie > 0 ? Number(d.tresorerie).toLocaleString('fr') + ' €' : 'aucune'} (${d.objet_tresorerie}).

COMPORTEMENT BANCAIRE
Rejets prélèvements : ${d.nb_rejets}. Rejet sur prêt immo : ${d.rejet_immo}. FICP : ${d.ficp}. FCC : ${d.fcc}. Surendettement : ${d.surendettement}. Prêt contentieux : ${d.contentieux}. Déchéance du terme : ${d.decheance}.

OBJECTIF CLIENT
${d.objectif}. ${d.tresorerie !== '0' ? 'Trésorerie demandée : ' + d.tresorerie + ' — objet : ' + d.objet_tresorerie + '.' : 'Pas de trésorerie demandée.'}

COHÉRENCE DU MONTAGE
Montage retenu : ${montageStr}. MAF : ${d.maf > 0 ? Number(d.maf).toLocaleString('fr') + ' €' : 'à préciser'}. Durée : ${d.duree > 0 ? d.duree + ' mois' : 'à préciser'}. TEAP post-RAC estimé : ${teap}%. RAV estimé : ${rav > 0 ? rav.toLocaleString('fr') + ' €/mois' : 'à préciser'}.

ÉLIGIBILITÉ PARTENAIRES
Éligibles : ${eligible}. Sous conditions : ${conditionnel}.

CONCLUSION
Dossier estimé ${verdictClass === 'vert' ? 'FINANÇABLE' : verdictClass === 'orange' ? 'À ÉTUDIER AVEC PRÉCAUTION' : 'NON FINANÇABLE EN L\'ÉTAT'}. ${verdictClass !== 'rouge' ? 'Recommandation prioritaire : ' + eligible + '.' : 'Lever les points bloquants avant dépôt.'}`;
}

function genChecklist(montages, d) {
  const groups = [];
  groups.push({
    cat: 'Identité & Foyer',
    items: [
      "Pièce d'identité en cours de validité (x2 si co-emprunteur)",
      'Justificatif de domicile de moins de 3 mois',
      d.nb_enfants > 0 ? 'Livret de famille / jugement garde alternée' : null,
      d.divorce === 'oui' ? 'Convention de divorce / jugement séparation' : null,
      d.nationalite === 'sejour' ? 'Titre de séjour valide (durée > durée du prêt)' : null,
    ].filter(Boolean)
  });

  groups.push({
    cat: 'Revenus',
    items: [
      '3 derniers bulletins de salaire',
      '2 derniers avis d\'imposition',
      d.contrat1 === 'cdd' ? 'Contrat de travail + attestation employeur (CDD)' : null,
      d.contrat1 === 'ae' || d.contrat1 === 'tns' ? '2 ou 3 derniers bilans / liasses fiscales' : null,
      d.contrat1 === 'retraite' ? 'Dernier relevé de pension de retraite' : null,
      d.pension_recue === 'oui' ? 'Jugement fixant la pension alimentaire reçue' : null,
    ].filter(Boolean)
  });

  groups.push({
    cat: 'Comptes bancaires',
    items: [
      '3 derniers relevés de tous les comptes courants',
      '3 derniers relevés des comptes avec prélèvements crédits',
      d.pret_immo_encours === 'conserver' ? 'Relevé compte avec prélèvement prêt immobilier conservé' : null,
    ].filter(Boolean)
  });

  groups.push({
    cat: 'Crédits à regrouper',
    items: [
      'Dernier relevé de situation de chaque crédit (CRD + mensualité)',
      d.credit_auto === 'oui' ? 'Contrat LOA/LLD ou TA crédit auto' : null,
      d.dettes !== 'non' ? 'Justificatif(s) dettes hors crédits (huissier / impôts)' : null,
    ].filter(Boolean)
  });

  if (montages.includes('LCC') || montages.includes('LS2')) {
    groups.push({
      cat: 'Bien immobilier (LCC/LS2)',
      items: [
        'Titre de propriété ou attestation notariale',
        'Taxe foncière la plus récente',
        'Estimation valeur du bien (agence ou notaire)',
        d.pret_immo_encours !== 'non' ? 'Tableau d\'amortissement du prêt immobilier' : null,
        d.rang_hypo === '2eme' ? 'Offre de prêt du 1er rang + TA à jour' : null,
      ].filter(Boolean)
    });
  }

  if (d.tresorerie && parseFloat(d.tresorerie) > 0) {
    const treso = parseFloat(d.tresorerie);
    const tItems = [];
    if (treso <= 10000) tItems.push('Attestation sur l\'honneur (motif + montant)');
    if (treso > 10000 && treso <= 25000) { tItems.push('Attestation client + explication en note de présentation'); }
    if (treso > 25000) {
      tItems.push('Attestation client signée');
      tItems.push('Devis daté et signé (ou bon de commande)');
    }
    if (d.objet_tresorerie === 'travaux_sans_permis') tItems.push('Devis travaux SANS mention de permis de construire');
    if (d.objet_tresorerie === 'vehicule') tItems.push('Bon de commande ou annonce véhicule datée');
    groups.push({ cat: 'Trésorerie', items: tItems });
  }

  return groups;
}

function toggleCheck(el) {
  el.classList.toggle('done');
  const cb = el.querySelector('.cb');
  cb.textContent = el.classList.contains('done') ? '✓' : '';
}

function copyNote() {
  const note = document.getElementById('note-analyste').innerText;
  navigator.clipboard.writeText(note).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = '✓ Copié !';
    setTimeout(() => btn.textContent = '📋 Copier', 2000);
  });
}

function exportPDF(partners, montages, d, teap, teav, rav) {
  const montageStr = montages.join(' + ') || 'PP';
  const now = new Date();
  const dateStr = now.toLocaleDateString('fr-FR');
  const timeStr = now.toLocaleTimeString('fr-FR', {hour:'2-digit',minute:'2-digit'});

  const statusColor = { eligible: '#16A34A', partiel: '#D97706', non: '#DC2626' };
  const statusLabel = { eligible: 'ÉLIGIBLE', partiel: 'SOUS CONDITIONS', non: 'KO' };
  const statusIcon  = { eligible: '✓', partiel: '⚠', non: '✗' };
  const ruleColor   = { ok: '#16A34A', warn: '#92400E', ko: '#DC2626' };
  const ruleDot     = { ok: '✓', warn: '⚠', ko: '✗' };

  const eligibles = partners.filter(p => p.statut === 'eligible').length;
  const partiels  = partners.filter(p => p.statut === 'partiel').length;
  const verdict   = eligibles >= 2 ? 'FINANÇABLE' : eligibles >= 1 || partiels >= 2 ? 'À ÉTUDIER' : 'NON FINANÇABLE';
  const verdictCol= eligibles >= 2 ? '#16A34A' : eligibles >= 1 || partiels >= 2 ? '#D97706' : '#DC2626';

  const partnerHTML = partners.map(p => `
    <div style="break-inside:avoid;background:#FFFFFF;border:1.5px solid ${statusColor[p.statut] || '#E2E8F0'};border-radius:10px;padding:16px 18px;margin-bottom:12px;">
      <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:10px;">
        <div style="font-size:16px;font-weight:700;color:#1E293B;">${p.nom}<\/div>
        <div style="font-size:11px;font-weight:700;padding:3px 12px;border-radius:20px;background:${statusColor[p.statut]}20;color:${statusColor[p.statut]};border:1px solid ${statusColor[p.statut]}50;font-family:monospace;letter-spacing:1px;">
          ${statusIcon[p.statut]} ${statusLabel[p.statut]}
        <\/div>
      <\/div>
      <div style="display:flex;flex-direction:column;gap:4px;">
        ${p.regles.map(r => `
          <div style="display:flex;gap:8px;align-items:flex-start;font-size:12px;color:${ruleColor[r.type] || '#64748B'};line-height:1.5;">
            <span style="flex-shrink:0;font-weight:700;">${ruleDot[r.type]}<\/span>
            <span>${r.text}<\/span>
          <\/div>
        `).join('')}
      <\/div>
    <\/div>
  `).join('');

  const html = `<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>Analyse RAC — ${dateStr}<\/title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
  body { font-family: 'Inter', sans-serif; background: #F8F9FC; color: #1E293B; margin: 0; padding: 0; -webkit-print-color-adjust: exact; print-color-adjust: exact; }
  @media print { body { background: white; } .no-print { display: none; } }
<\/style>
<\/head>
<body>
<div style="max-width:800px;margin:0 auto;padding:32px 28px;">

  <!-- HEADER -->
  <div style="display:flex;align-items:center;justify-content:space-between;padding-bottom:20px;border-bottom:2px solid #E2E8F0;margin-bottom:24px;">
    <div>
      <div style="font-size:10px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:#3B82F6;margin-bottom:4px;font-family:monospace;">OUTIL INTERNE · CONFIDENTIEL<\/div>
      <div style="font-size:24px;font-weight:700;color:#1E293B;">Analyse RAC<\/div>
      <div style="font-size:12px;color:#64748B;margin-top:2px;">Synthèse d'éligibilité partenaires<\/div>
    <\/div>
    <div style="text-align:right;">
      <div style="font-size:11px;color:#64748B;font-family:monospace;">${dateStr} · ${timeStr}<\/div>
      <div style="font-size:11px;color:#64748B;font-family:monospace;margin-top:2px;">Montage : ${montageStr}<\/div>
    <\/div>
  <\/div>

  <!-- VERDICT + KPIs -->
  <div style="background:#FFFFFF;border:1.5px solid ${verdictCol}40;border-radius:12px;padding:20px 24px;margin-bottom:20px;border-left:5px solid ${verdictCol};">
    <div style="font-size:20px;font-weight:700;color:${verdictCol};margin-bottom:12px;">${verdict}<\/div>
    <div style="display:grid;grid-template-columns:repeat(5,1fr);gap:12px;">
      ${[
        ['TEAV actuel', teav > 0 ? teav+'%' : 'N/A', teav > 90 ? '#DC2626' : teav > 70 ? '#D97706' : '#16A34A'],
        ['TEAP post-RAC', teap > 0 ? teap+'%' : 'N/A', teap > 50 ? '#DC2626' : teap > 45 ? '#D97706' : '#16A34A'],
        ['RAV estimé', rav > 0 ? rav.toLocaleString('fr')+' €' : 'N/A', rav < 700 ? '#DC2626' : rav < 1200 ? '#D97706' : '#16A34A'],
        ['MAF', d.maf > 0 ? Number(d.maf).toLocaleString('fr')+' €' : 'N/A', '#1E293B'],
        ['Durée', d.duree > 0 ? d.duree+' mois' : 'N/A', '#1E293B'],
      ].map(([lbl, val, col]) => `
        <div style="background:#F8F9FC;border-radius:8px;padding:12px;text-align:center;">
          <div style="font-size:18px;font-weight:700;color:${col};font-family:monospace;">${val}<\/div>
          <div style="font-size:9px;font-weight:600;letter-spacing:1px;text-transform:uppercase;color:#94A3B8;margin-top:3px;">${lbl}<\/div>
        <\/div>
      `).join('')}
    <\/div>
  <\/div>

  <!-- PARTENAIRES -->
  <div style="font-size:10px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:#94A3B8;margin-bottom:14px;display:flex;align-items:center;gap:8px;">
    ÉLIGIBILITÉ PAR PARTENAIRE
    <span style="flex:1;height:1px;background:#E2E8F0;display:block;"><\/span>
  <\/div>
  ${partnerHTML}

  <!-- FOOTER -->
  <div style="margin-top:28px;padding-top:16px;border-top:1px solid #E2E8F0;font-size:10px;color:#94A3B8;font-family:monospace;line-height:1.7;">
    Document généré automatiquement · Outil interne RAC · Usage conseiller uniquement<br>
    RGPD : aucune donnée nominative — variables anonymisées uniquement · ${dateStr}
  <\/div>

<\/div>
<script>window.print();<\/script>
<\/body>
<\/html>`;

  const blob = new Blob([html], {type: 'text/html'});
  const url  = URL.createObjectURL(blob);
  const win  = window.open(url, '_blank');
  setTimeout(() => URL.revokeObjectURL(url), 10000);
}

</script>
</body>
</html>
