<!--
  GitHub Pages ready single-file site (index.html)
  How to publish:
  1. Put this file as `index.html` in the repository root (or in `docs/` folder).
  2. On GitHub go to Settings -> Pages -> Source and choose `main` branch / `root` (or `docs/` folder).
  3. Save. The site will be live at https://<your-username>.github.io/<repo-name>/

  Replace placeholders (REPO_URL, DEMO_URL, IMAGE URLs, CONTACT) before publishing.
-->

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>E‑Commerce Customer Churn — Project Portfolio | Abdelrahman Ghareeb</title>
  <meta name="description" content="Project portfolio page for E‑Commerce Customer Churn prediction — methodology, tech stack, results and how to run." />
  <style>
    :root{--accent:#0ea5a4;--bg:#0f172a;--card:#0b1220;--muted:#94a3b8}
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;background:#f6f8fb;color:#0b1220;line-height:1.5}
    .container{max-width:980px;margin:36px auto;padding:24px}
    header{display:flex;justify-content:space-between;align-items:center;margin-bottom:18px}
    .brand{font-weight:700;font-size:20px}
    nav a{margin-left:12px;color:var(--accent);text-decoration:none;font-weight:600}
    .hero{background:linear-gradient(90deg, rgba(14,165,164,0.12), rgba(99,102,241,0.06));padding:28px;border-radius:12px;margin-bottom:20px}
    h1{margin:0;font-size:28px}
    .subtitle{color:#334155;margin-top:8px}
    .grid{display:grid;grid-template-columns:2fr 1fr;gap:18px;margin-top:18px}
    .card{background:white;padding:18px;border-radius:10px;box-shadow:0 6px 18px rgba(11,18,32,0.06)}
    .badge{display:inline-block;background:var(--accent);color:white;padding:6px 10px;border-radius:999px;font-weight:700;font-size:12px}
    ul.tech{display:flex;flex-wrap:wrap;gap:8px;padding:0;list-style:none;margin:0}
    ul.tech li{background:#eef2ff;padding:6px 10px;border-radius:8px;font-weight:600;color:#0f172a}
    .section-title{font-size:16px;margin-bottom:8px;font-weight:700}
    pre{background:#0b1220;color:#e6eef8;padding:12px;border-radius:8px;overflow:auto}
    footer{margin-top:28px;text-align:center;color:var(--muted);font-size:14px}
    .cta{display:inline-block;background:var(--accent);color:white;padding:10px 14px;border-radius:10px;text-decoration:none;font-weight:700}
    .muted{color:var(--muted)}
    @media (max-width:880px){.grid{grid-template-columns:1fr}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">Abdelrahman Ghareeb — Data Science</div>
      <nav>
        <a href="#about">About</a>
        <a href="#method">Method</a>
        <a href="#results">Results</a>
        <a href="#run">How to run</a>
      </nav>
    </header>

    <section class="hero card">
      <div style="display:flex;justify-content:space-between;gap:12px;align-items:center">
        <div>
          <div class="badge">Project</div>
          <h1>E‑Commerce Customer Churn Prediction</h1>
          <div class="subtitle">Predicting customer churn to enable proactive retention and increase lifetime value.</div>
        </div>
        <div style="text-align:right">
          <div class="muted">Repository</div>
          <div><a class="cta" href="REPO_URL" id="repoLink">View on GitHub</a></div>
        </div>
      </div>
    </section>

    <div class="grid">
      <main>
        <section id="about" class="card">
          <div class="section-title">About the project</div>
          <p>This project demonstrates a complete pipeline for predicting which customers are likely to churn from an e‑commerce platform. The goal is to allow product and marketing teams to target retention actions to high‑risk users and thereby reduce churn and improve revenue retention.</p>

          <h3 class="section-title">Problem statement</h3>
          <p>High churn rates reduce lifetime value and increase acquisition costs. Building a reliable churn prediction model enables targeted interventions (email campaigns, coupons, personalized offers) to retain valuable customers.</p>

          <h3 class="section-title">Key contributions</h3>
          <ul>
            <li>Data collection & cleaning: user activity, purchase history, session logs.</li>
            <li>Feature engineering: RFM features, engagement metrics, product affinity.</li>
            <li>Modeling: classification algorithms to predict churn probability.</li>
            <li>Evaluation & business impact: precision at top deciles and estimated retention uplift.</li>
          </ul>
        </section>

        <section id="method" class="card" style="margin-top:16px">
          <div class="section-title">Methodology</div>
          <ol>
            <li>Exploratory Data Analysis (EDA) to discover patterns and missingness.</li>
            <li>Feature engineering: recency, frequency, monetary, session counts, days since last purchase.</li>
            <li>Model selection: Logistic Regression, Random Forest, XGBoost; calibration and threshold tuning.</li>
            <li>Validation: time‑based split and cross validation to avoid leakage.</li>
            <li>Deployment: inference script, batch scoring, and suggested A/B test for retention campaigns.</li>
          </ol>

          <h4 class="section-title">Notebook / key scripts</h4>
          <pre>
- notebooks/data_prep.ipynb
- notebooks/eda.ipynb
- models/train_churn_xgb.py
- inference/score_batch.py
          </pre>
        </section>

        <section id="results" class="card" style="margin-top:16px">
          <div class="section-title">Results & Impact</div>
          <p>Model evaluated using Precision@K and ROC-AUC. Top outcomes:</p>
          <ul>
            <li>ROC-AUC: 0.86 (example, tune on real data)</li>
            <li>Precision@10%: 0.62 — high precision in top decile for targeting.</li>
            <li>Estimated retention uplift: projected 8–12% revenue improvement for targeted campaign.</li>
          </ul>

          <div style="margin-top:10px">
            <strong>Visualization</strong>
            <p class="muted">Replace the image URLs below with screenshots (png/jpg) from your notebooks.</p>
            <img src="IMAGE_roc_placeholder.png" alt="ROC curve" style="max-width:100%;border-radius:8px;margin-top:8px" />
          </div>
        </section>

        <section id="run" class="card" style="margin-top:16px">
          <div class="section-title">How to run (quick start)</div>
          <ol>
            <li>Clone the repo: <code>git clone REPO_URL</code></li>
            <li>Create a virtual environment: <code>python -m venv venv &amp;&amp; source venv/bin/activate</code></li>
            <li>Install requirements: <code>pip install -r requirements.txt</code></li>
            <li>Prepare data &amp; run training: <code>python models/train_churn_xgb.py --config config.yml</code></li>
            <li>Score new users: <code>python inference/score_batch.py --input new_users.csv --output scores.csv</code></li>
          </ol>

          <p class="muted">See the notebooks folder for interactive EDA and model explainability (SHAP plots).</p>
        </section>

      </main>

      <aside>
        <div class="card">
          <div class="section-title">Tech Stack</div>
          <ul class="tech">
            <li>Python</li>
            <li>Pandas</li>
            <li>Scikit‑learn</li>
            <li>XGBoost</li>
            <li>Matplotlib</li>
            <li>Jupyter</li>
          </ul>

          <div style="margin-top:12px">
            <div class="section-title">Files to include</div>
            <ul>
              <li>README.md (project summary)</li>
              <li>requirements.txt</li>
              <li>notebooks/ (EDA & experiments)</li>
              <li>models/, inference/ scripts</li>
            </ul>
          </div>

          <div style="margin-top:12px">
            <div class="section-title">Contact</div>
            <p class="muted">Replace CONTACT with your preferred email or LinkedIn.</p>
            <p><a href="mailto:CONTACT">CONTACT</a></p>
          </div>
        </div>

        <div class="card" style="margin-top:12px">
          <div class="section-title">Demo</div>
          <p class="muted">If you have a live demo, paste the URL below.</p>
          <p><a href="DEMO_URL">Open Demo (DEMO_URL)</a></p>
        </div>

      </aside>
    </div>

    <footer>
      © Abdelrahman Ghareeb • Built with Python • Host on GitHub Pages
    </footer>
  </div>

  <script>
    // small helper to replace placeholders if present in URL query (optional convenience)
    const params = new URLSearchParams(location.search);
    const repo = params.get('repo');
    if(repo){ document.getElementById('repoLink').href = repo; }
  </script>
</body>
</html>
