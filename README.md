# whoopchangnew

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Privacy Policy — Personal Health Tracker</title>
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,300;0,400;0,600;1,300&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --bg: #0e0e0e;
      --surface: #161616;
      --border: #2a2a2a;
      --accent: #c8f564;
      --text-primary: #f0ede6;
      --text-secondary: #888;
      --text-muted: #555;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      background: var(--bg);
      color: var(--text-primary);
      font-family: 'DM Sans', sans-serif;
      font-weight: 300;
      line-height: 1.75;
      min-height: 100vh;
    }

    /* Subtle grain overlay */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
      pointer-events: none;
      z-index: 0;
      opacity: 0.4;
    }

    .container {
      position: relative;
      z-index: 1;
      max-width: 740px;
      margin: 0 auto;
      padding: 80px 32px 120px;
    }

    /* Header */
    header {
      margin-bottom: 72px;
      padding-bottom: 40px;
      border-bottom: 1px solid var(--border);
    }

    .tag {
      display: inline-block;
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--accent);
      background: rgba(200, 245, 100, 0.08);
      border: 1px solid rgba(200, 245, 100, 0.2);
      padding: 4px 12px;
      border-radius: 2px;
      margin-bottom: 28px;
    }

    h1 {
      font-family: 'Fraunces', serif;
      font-size: clamp(2.2rem, 5vw, 3.2rem);
      font-weight: 300;
      line-height: 1.15;
      color: var(--text-primary);
      margin-bottom: 20px;
    }

    h1 em {
      font-style: italic;
      color: var(--accent);
    }

    .meta {
      font-size: 13px;
      color: var(--text-secondary);
      letter-spacing: 0.02em;
    }

    /* Sections */
    section {
      margin-bottom: 52px;
      opacity: 0;
      transform: translateY(16px);
      animation: fadeUp 0.5s ease forwards;
    }

    section:nth-child(1) { animation-delay: 0.1s; }
    section:nth-child(2) { animation-delay: 0.15s; }
    section:nth-child(3) { animation-delay: 0.2s; }
    section:nth-child(4) { animation-delay: 0.25s; }
    section:nth-child(5) { animation-delay: 0.3s; }
    section:nth-child(6) { animation-delay: 0.35s; }
    section:nth-child(7) { animation-delay: 0.4s; }
    section:nth-child(8) { animation-delay: 0.45s; }

    @keyframes fadeUp {
      to { opacity: 1; transform: translateY(0); }
    }

    h2 {
      font-family: 'Fraunces', serif;
      font-size: 1.15rem;
      font-weight: 400;
      color: var(--text-primary);
      margin-bottom: 14px;
      display: flex;
      align-items: center;
      gap: 12px;
    }

    h2::before {
      content: '';
      display: inline-block;
      width: 6px;
      height: 6px;
      background: var(--accent);
      border-radius: 50%;
      flex-shrink: 0;
    }

    p {
      font-size: 15px;
      color: #bbb;
      margin-bottom: 12px;
    }

    ul {
      list-style: none;
      padding: 0;
      margin: 8px 0 12px;
    }

    ul li {
      font-size: 15px;
      color: #bbb;
      padding: 6px 0 6px 20px;
      position: relative;
      border-bottom: 1px solid var(--border);
    }

    ul li:last-child { border-bottom: none; }

    ul li::before {
      content: '→';
      position: absolute;
      left: 0;
      color: var(--accent);
      font-size: 12px;
    }

    /* Callout box */
    .callout {
      background: var(--surface);
      border: 1px solid var(--border);
      border-left: 3px solid var(--accent);
      padding: 20px 24px;
      border-radius: 2px;
      margin: 16px 0;
    }

    .callout p {
      margin: 0;
      font-size: 14px;
    }

    /* Contact */
    .contact-box {
      background: var(--surface);
      border: 1px solid var(--border);
      padding: 28px 32px;
      border-radius: 4px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
      flex-wrap: wrap;
    }

    .contact-box span {
      font-size: 14px;
      color: var(--text-secondary);
    }

    .contact-box a {
      color: var(--accent);
      text-decoration: none;
      font-size: 14px;
      font-weight: 500;
      border-bottom: 1px solid rgba(200,245,100,0.3);
      padding-bottom: 1px;
      transition: border-color 0.2s;
    }

    .contact-box a:hover { border-color: var(--accent); }

    /* Footer */
    footer {
      margin-top: 80px;
      padding-top: 32px;
      border-top: 1px solid var(--border);
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 12px;
    }

    footer span {
      font-size: 12px;
      color: var(--text-muted);
      letter-spacing: 0.05em;
    }

    .dot { color: var(--accent); }
  </style>
</head>
<body>
  <div class="container">

    <header>
      <div class="tag">Legal Document</div>
      <h1>Privacy <em>Policy</em></h1>
      <p class="meta">Personal Health Tracker &nbsp;<span class="dot">·</span>&nbsp; Last updated: March 29, 2026</p>
    </header>

    <section>
      <h2>Overview</h2>
      <p>This Privacy Policy explains how Personal Health Tracker ("the App", "we", "us") collects, uses, and protects your personal health data when you connect your WHOOP account. This is a personal-use application and your data is never shared, sold, or used for commercial purposes.</p>
      <div class="callout">
        <p>This app is a personal tool for accessing your own WHOOP data. Only you have access to your information.</p>
      </div>
    </section>

    <section>
      <h2>Data We Access</h2>
      <p>With your explicit authorization via WHOOP's OAuth 2.0 flow, the App may access the following data from your WHOOP account:</p>
      <ul>
        <li>Recovery scores, HRV, and resting heart rate</li>
        <li>Daily strain scores and physiological cycles</li>
        <li>Sleep performance data (duration, stages, disturbances)</li>
        <li>Workout detection data (type, effort, heart rate zones)</li>
        <li>Basic profile information (name, email)</li>
      </ul>
    </section>

    <section>
      <h2>How We Use Your Data</h2>
      <p>Your WHOOP data is used solely for the following purposes:</p>
      <ul>
        <li>Displaying your personal health metrics in a readable format</li>
        <li>Analyzing recovery and training trends over time</li>
        <li>Generating personal performance insights</li>
        <li>Exporting data for your own personal records</li>
      </ul>
      <p>We do <strong style="color: var(--text-primary);">not</strong> use your data for advertising, profiling, or any commercial purpose.</p>
    </section>

    <section>
      <h2>Data Storage & Security</h2>
      <p>Your access credentials (OAuth tokens) are stored locally on your personal device and are never transmitted to any third-party server. Health data retrieved from WHOOP is processed locally and is not stored in any external database.</p>
      <div class="callout">
        <p>All API calls are made server-side. Your Client Secret and Access Tokens are never exposed in any client-facing interface.</p>
      </div>
    </section>

    <section>
      <h2>Data Sharing</h2>
      <p>We do not sell, trade, rent, or otherwise share your personal health information with any third parties. Your data is accessed solely through the official WHOOP API and remains under your control at all times.</p>
    </section>

    <section>
      <h2>Your Rights & Control</h2>
      <p>You retain full control over your data at all times:</p>
      <ul>
        <li>Revoke app access at any time from your WHOOP account settings</li>
        <li>Request deletion of any locally stored data</li>
        <li>Disconnect the integration without any data retention</li>
        <li>Review what scopes the app has requested before authorizing</li>
      </ul>
    </section>

    <section>
      <h2>Third-Party Services</h2>
      <p>This app integrates exclusively with the WHOOP Developer API. Your use of WHOOP's platform is also subject to <a href="https://www.whoop.com/privacy/" target="_blank" style="color: var(--accent); text-decoration: none; border-bottom: 1px solid rgba(200,245,100,0.3);">WHOOP's own Privacy Policy</a>. We have no control over WHOOP's data practices.</p>
    </section>

    <section>
      <h2>Changes to This Policy</h2>
      <p>Any material changes to this Privacy Policy will be reflected with an updated date at the top of this page. Continued use of the App after changes constitutes your acceptance of the revised policy.</p>
    </section>

    <section>
      <h2>Contact</h2>
      <div class="contact-box">
        <span>Questions about this Privacy Policy?</span>
        <a href="mailto:your@email.com">your@email.com</a>
      </div>
    </section>

    <footer>
      <span>Personal Health Tracker <span class="dot">·</span> Privacy Policy</span>
      <span>© 2026 — All rights reserved</span>
    </footer>

  </div>
</body>
</html>
