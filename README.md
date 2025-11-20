<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="description" content="Transparencia: desglose de inversión de StreetBall Andaluz, financiado 100% con capital propio." />
  <title>Inversión Responsable - StreetBall Andaluz</title>
  <style>
    :root{
      --bg: #f8f9fa;
      --card: #fff;
      --text: #1f2937;
      --muted: #6b7280;
      --accent: #f97316;
      --accent-2: #fb923c;
      --accent-3: #fdba74;
      --track: #e5e7eb;
      --rounded: 12px;
      --shadow: 0 4px 12px rgba(0,0,0,0.08);
      --max-width: 820px;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      background:var(--bg);
      color:var(--text);
      line-height:1.5;
      padding:20px;
    }
    .container{
      max-width:var(--max-width);
      margin:0 auto;
      background:var(--card);
      padding:36px;
      border-radius:var(--rounded);
      box-shadow:var(--shadow);
    }
    header{
      text-align:center;
      margin-bottom:8px;
    }
    h1{
      margin:0;
      font-size:2.1rem;
      color:var(--accent);
    }
    .subtitle{
      color:var(--muted);
      margin-top:8px;
      font-size:1rem;
    }
    .investment-total{
      text-align:center;
      margin:28px 0;
    }
    .total-amount{
      font-size:3rem;
      font-weight:700;
      color:var(--accent);
      line-height:1;
    }
    .total-label{
      color:var(--muted);
      font-size:0.95rem;
    }
    .investment-breakdown{
      margin-top:20px;
      display:grid;
      gap:18px;
    }
    .item{
      display:block;
    }
    .item-header{
      display:flex;
      justify-content:space-between;
      align-items:center;
      margin-bottom:8px;
      font-weight:600;
    }
    .progress-track{
      height:28px;
      background:var(--track);
      border-radius:999px;
      overflow:hidden;
      position:relative;
    }
    .progress-bar{
      height:100%;
      display:flex;
      align-items:center;
      justify-content:flex-end;
      padding-right:10px;
      color:#fff;
      font-weight:700;
      font-size:0.85rem;
      white-space:nowrap;
      transition:width 600ms ease;
    }
    .bar-1{ background:var(--accent); }
    .bar-2{ background:var(--accent-2); }
    .bar-3{ background:var(--accent-3); }
    .bar-zero{ background:#d1d5db; color:#374151; justify-content:flex-start; padding-left:10px; }
    .investment-note{
      margin-top:26px;
      padding-top:18px;
      border-top:1px solid #eee;
      color:var(--muted);
      font-style:italic;
      text-align:center;
    }

    @media (max-width:600px){
      .container{ padding:20px; }
      h1{ font-size:1.6rem; }
      .total-amount{ font-size:2.2rem; }
      .progress-track{ height:22px; }
    }

    /* Focus styles for keyboard users */
    .item:focus-within .item-header{ outline:2px solid rgba(249,115,22,0.18); border-radius:8px; }
  </style>
</head>
<body>
  <div class="container" role="region" aria-labelledby="page-title">
    <header>
      <h1 id="page-title">Inversión responsable</h1>
      <p class="subtitle">Financiado 100% con capital propio. Transparencia y compromiso.</p>
    </header>

    <main>
      <div class="investment-total" aria-live="polite">
        <div id="totalAmount" class="total-amount" aria-hidden="true">120 €</div>
        <div class="total-label">Total invertido</div>
      </div>

      <section class="investment-breakdown" aria-label="Desglose de inversión">
        <div class="item" data-amount="60">
          <div class="item-header">
            <span>Material deportivo</span>
            <span class="amount" aria-hidden="true">60 €</span>
          </div>
          <div class="progress-track" role="group" aria-label="Porcentaje invertido en material deportivo">
            <div class="progress-bar bar-1" role="progressbar" aria-valuemin="0" aria-valuemax="100" aria-valuenow="50" style="width:50%;">50%</div>
          </div>
        </div>

        <div class="item" data-amount="40">
          <div class="item-header">
            <span>Organización logística</span>
            <span class="amount" aria-hidden="true">40 €</span>
          </div>
          <div class="progress-track" role="group" aria-label="Porcentaje invertido en organización logística">
            <div class="progress-bar bar-2" role="progressbar" aria-valuemin="0" aria-valuemax="100" aria-valuenow="33" style="width:33%;">33%</div>
          </div>
        </div>

        <div class="item" data-amount="20">
          <div class="item-header">
            <span>Publicidad</span>
            <span class="amount" aria-hidden="true">20 €</span>
          </div>
          <div class="progress-track" role="group" aria-label="Porcentaje invertido en publicidad">
            <div class="progress-bar bar-3" role="progressbar" aria-valuemin="0" aria-valuemax="100" aria-valuenow="17" style="width:17%;">17%</div>
          </div>
        </div>

        <div class="item" data-amount="0">
          <div class="item-header">
            <span>Alquiler de instalaciones</span>
            <span class="amount" aria-hidden="true">0 €</span>
          </div>
          <div class="progress-track" role="group" aria-label="Porcentaje invertido en alquiler de instalaciones">
            <div class="progress-bar bar-zero" role="progressbar" aria-valuemin="0" aria-valuemax="100" aria-valuenow="0" style="width:0%;">0%</div>
          </div>
        </div>
      </section>

      <p class="investment-note">
        Este modelo de inversión reducida nos permite ofrecer eventos de calidad de forma sostenible.
      </p>
    </main>
  </div>

  <script>
    (function(){
      const fmt = new Intl.NumberFormat('es-ES', { style: 'currency', currency: 'EUR', maximumFractionDigits: 0 });
      const items = Array.from(document.querySelectorAll('.item'));
      const totalAmountEl = document.getElementById('totalAmount');

      const amounts = items.map(it => {
        const raw = it.dataset.amount || '0';
        const value = Number(raw);
        return Number.isFinite(value) ? value : 0;
      });
      const total = amounts.reduce((s,v) => s+v, 0);
      totalAmountEl.textContent = fmt.format(total);

      items.forEach((it, idx) => {
        const amt = amounts[idx];
        const bar = it.querySelector('.progress-bar');
        const amountLabel = it.querySelector('.amount');
        if (amountLabel) amountLabel.textContent = fmt.format(amt);
        if (total <= 0){
          if (bar){
            bar.style.width = '0%';
            bar.textContent = '0%';
            bar.setAttribute('aria-valuenow','0');
            bar.classList.remove('bar-1','bar-2','bar-3');
            bar.classList.add('bar-zero');
          }
        } else {
          const pctRaw = (amt / total) * 100;
          const pct = Math.round(pctRaw);
          if (bar){
            bar.style.width = pct + '%';
            bar.textContent = pct + '%';
            bar.setAttribute('aria-valuenow', String(pct));
            if (amt === 0){
              bar.classList.remove('bar-1','bar-2','bar-3');
              bar.classList.add('bar-zero');
              bar.style.width = '0%';
              bar.textContent = '0%';
            }
          }
        }
      });

      window.updateInvestmentBreakdown = function(){ location.reload(); };
    })();
  </script>
</body>
</html>
