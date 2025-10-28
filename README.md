<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1.0" />
  <title>Mina Mamdouh – Automation Projects</title>
  <style>
    :root {
      --bg-dark: #0f1a2e;
      --card-dark: #1a2742;
      --panel-dark: #0f172a;
      --text-main: #ffffff;
      --text-dim: #94a3b8;
      --accent: #38bdf8;
      --accent-green: #10b981;
      --border-card: rgba(255,255,255,0.07);
      --border-panel: rgba(255,255,255,0.08);
      --radius-xl: 1.25rem;
      --radius-lg: 0.75rem;
      --whatsapp-green: #25D366;
    }

    * {
      box-sizing: border-box;
      -webkit-font-smoothing: antialiased;
      margin: 0;
      padding: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Inter", "Segoe UI", Roboto, "Cairo", sans-serif;
    }

    body {
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.5;
    }

    img {
      max-width: 100%;
      height: auto;
      display: block;
    }

    .wrapper {
      max-width: 1100px;
      margin: 0 auto;
      padding: 2rem 1.5rem 5rem;
    }

    /******** HEADER *********/
    header {
      display:flex;
      justify-content:space-between;
      align-items:flex-start;
      flex-wrap:wrap;
      gap:1rem;
      margin-bottom:2.5rem;
    }

    .left-head {
      display:flex;
      gap:.75rem;
      align-items:center;
    }

    .avatar {
      width:56px;
      height:56px;
      border-radius: var(--radius-lg);
      background:#1e293b;
      border:1px solid var(--border-card);
      display:flex;
      align-items:center;
      justify-content:center;
      font-weight:600;
      color:var(--text-main);
      font-size:.8rem;
    }

    .me-lines {
      display:flex;
      flex-direction:column;
      line-height:1.3;
    }

    .me-name {
      font-weight:600;
      font-size:1rem;
      color:var(--text-main);
      letter-spacing:-.02em;
    }
    .me-role {
      font-size:.8rem;
      color:var(--text-dim);
    }

    .right-head {
      display:flex;
      flex-direction:column;
      align-items:flex-end;
      gap:.75rem;
    }

    .head-cta-row {
      display:flex;
      flex-wrap:wrap;
      gap:.75rem;
      justify-content:flex-end;
    }

    .btn-wsp {
      background: var(--whatsapp-green);
      color:#000;
      font-weight:600;
      font-size:.9rem;
      border:0;
      border-radius:var(--radius-lg);
      padding:.7rem 1rem;
      text-decoration:none;
      line-height:1.2;
      box-shadow:0 10px 30px rgba(37,211,102,.35);
      white-space:nowrap;
    }

    .btn-mail {
      background:transparent;
      color:var(--text-main);
      border:1px solid var(--border-card);
      border-radius:var(--radius-lg);
      padding:.7rem 1rem;
      font-size:.9rem;
      font-weight:500;
      line-height:1.2;
      text-decoration:none;
      white-space:nowrap;
    }

    .lang-toggle-btn {
      background: transparent;
      border: 1px solid var(--border-card);
      border-radius: var(--radius-lg);
      color: var(--text-main);
      font-size: 0.8rem;
      line-height: 1.2;
      padding: .5rem .75rem;
      cursor: pointer;
      font-weight: 500;
      min-width: 70px;
      text-align: center;
    }

    /******** INTRO *********/
    .intro {
      margin-bottom:2rem;
      max-width:800px;
    }

    .intro h1 {
      font-size: clamp(1.5rem, 1vw + 1rem, 2rem);
      font-weight:600;
      color:var(--text-main);
      line-height:1.2;
      letter-spacing:-.03em;
      margin-bottom:1rem;
    }
    .intro h1 span {
      color:var(--accent);
    }

    .lead {
      color:var(--text-dim);
      font-size:1rem;
      line-height:1.5;
      margin-bottom:1.5rem;
    }

    .lead + .lead {
      margin-top:-.75rem;
    }

    /******** CATEGORY SECTIONS *********/
    .category-block {
      margin-bottom:3rem;
    }

    .cat-head {
      font-size: .9rem;
      font-weight:600;
      color:var(--text-main);
      margin-bottom:.75rem;
      letter-spacing:-.02em;
      display:flex;
      align-items:baseline;
      justify-content:space-between;
      flex-wrap:wrap;
      gap:.5rem;
    }

    .cat-note {
      font-size:.75rem;
      font-weight:500;
      color:var(--accent);
    }

    .projects-grid {
      display:grid;
      grid-template-columns:1fr;
      gap:1rem;
    }

    @media(min-width:768px){
      .projects-grid {
        grid-template-columns:repeat(2,1fr);
      }
    }

    .proj-card {
      background-color:var(--card-dark);
      border:1px solid var(--border-card);
      border-radius:var(--radius-xl);
      box-shadow:0 20px 60px rgba(0,0,0,.6);
      padding:1rem 1rem 1.25rem;
      display:grid;
      gap:.6rem;
    }

    .proj-topline {
      display:flex;
      justify-content:space-between;
      flex-wrap:wrap;
      gap:.5rem;
      align-items:flex-start;
    }

    .proj-name {
      font-size:.9rem;
      font-weight:600;
      color:var(--text-main);
      line-height:1.4;
      letter-spacing:-.02em;
    }

    .proj-pill {
      background:rgba(56,189,248,.15);
      color:var(--accent);
      border:1px solid rgba(56,189,248,.4);
      border-radius:999px;
      padding:.25rem .5rem;
      line-height:1.2;
      font-size:.7rem;
      font-weight:600;
      white-space:nowrap;
    }

    .proj-desc {
      font-size:.8rem;
      color:var(--text-dim);
      line-height:1.4;
    }

    .proj-meta {
      font-size:.75rem;
      color:var(--text-main);
      line-height:1.4;
    }
    .proj-meta-title {
      font-weight:600;
      color:var(--text-main);
    }

    ul.meta-list {
      padding-left:0;
      list-style:none;
      display:grid;
      gap:.3rem;
      margin-top:.4rem;
    }

    ul.meta-list li::before {
      content:"• ";
      color:var(--accent);
    }

    /******** FOOTER *********/
    footer {
      text-align:center;
      font-size:.7rem;
      color:var(--text-dim);
      border-top:1px solid var(--border-card);
      padding-top:2rem;
      margin-top:4rem;
    }

    footer .foot-name {
      font-weight:600;
      color:var(--text-main);
      letter-spacing:-.02em;
      margin-bottom:.5rem;
      font-size:.8rem;
    }

    /******** LANG HANDLING *********/
    .lang-en { display:block; }
    .lang-ar { display:none; }

    body[dir="rtl"] .lang-en { display:none; }
    body[dir="rtl"] .lang-ar { display:block; }

    /* rtl tweaks */
    body[dir="rtl"] header,
    body[dir="rtl"] .intro,
    body[dir="rtl"] .category-block,
    body[dir="rtl"] footer {
      direction: rtl;
    }

    body[dir="rtl"] .right-head { align-items:flex-start; }
    body[dir="rtl"] .head-cta-row { justify-content:flex-start; }

  </style>
</head>
<body>

  <div class="wrapper">

    <!-- HEADER -->
    <header>
      <div class="left-head">
        <div class="avatar">
          <div class="avatar">
  <img src="mina.jpeg" alt="Mina Mamdouh" style="width:100%;height:100%;object-fit:cover;object-position:center;">
</div>

        </div>
        <div class="me-lines">
          <div class="me-name">Mina Mamdouh</div>
          <div class="me-role lang-en">Automation / Monitoring / Data Ops/ web scrap</div>
          <div class="me-role lang-ar">Automation / Monitoring / Data Ops/ web scrap</div>
        </div>
      </div>

      <div class="right-head">
        <div class="head-cta-row">
          <a class="btn-wsp lang-en" href="https://wa.me/201276535995" target="_blank" rel="noopener noreferrer">WhatsApp</a>
          <a class="btn-wsp lang-ar" href="https://wa.me/201276535995" target="_blank" rel="noopener noreferrer">واتساب</a>

          <a class="btn-mail lang-en" href="mailto:gminamamdouh@gmail.com">Email me</a>
          <a class="btn-mail lang-ar" href="mailto:gminamamdouh@gmail.com">إيميل</a>
        </div>

        <button class="lang-toggle-btn" id="langToggle">العربية</button>
      </div>
    </header>

    <!-- INTRO -->
    <section class="intro">
      <h1 class="lang-en">
        Real automations I've shipped for ecommerce teams.<br/>
        <span>Dashboards, monitoring, alerts, no fluff.</span>
      </h1>
      <h1 class="lang-ar">
        شغل أوتوميشن حقيقي شغال مع ستورز فعلية.<br/>
        <span>ريبورتات، مراقبة، تنبيهات. مفيش كلام فاضي.</span>
      </h1>

      <p class="lead lang-en">
        Below are systems I actually built: revenue reporting, server monitoring,
        password rotation, ROAS tracking, low-stock alerts, order QA bots, and more.
        All built to remove manual work and catch problems before they lose money.
      </p>
      <p class="lead lang-ar">
        اللي تحت ده حاجات أنا عملتها فعلاً: ريبورت المبيعات، مراقبة السيرفر،
        تغيير الباسوردات تلقائي، تتبّع ROAS، تنبيه ستوك قليل، بوت بيشيّك الأوردرات.
        الهدف دايمًا: أقل شغل يدوي، وأسرع إنذار قبل الفلوس ما تروح.
      </p>

      <p class="lead lang-en">
        I work fast, directly with owners / marketing leads / ops. No agency drama.
      </p>
      <p class="lead lang-ar">
        بشتغل مباشرة مع صاحب البزنس أو الهيد بتاع الماركتينج / الأوبس. مافيش بيروقراطية.
      </p>
    </section>

    <!-- CATEGORY 1: Account & Balance -->
    <section class="category-block">
      <div class="cat-head">
        <div class="lang-en">Account & Balance</div>
        <div class="lang-ar">الحسابات والرصيد</div>

        <div class="cat-note lang-en">Spend / ROAS clarity</div>
        <div class="cat-note lang-ar">فلوسك رايحة فين؟</div>
      </div>

      <div class="projects-grid">
        <!-- Project: account manager sheet -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Automation account manager </div>
            <div class="proj-name lang-ar">شيت إدارة الحساب أوتوماتيك</div>
            <div class="proj-pill">Reporting</div>
          </div>

          <div class="proj-desc lang-en">
            Daily / Yesterday / This Month view of spend, revenue, ROAS for each client or store.
            Auto-updated Google Sheet. No manual copy from Ads Manager.
          </div>
          <div class="proj-desc lang-ar">
            شيت بيتحدث لوحده فيه أرقام النهارده / امبارح / الشهر ده:
            الصرف على الإعلانات، الإيراد، الـROAS لكل أكونت أو ستور.
            بدون ما حد يقعد يسحب أرقام من Ads Manager بإيده.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>Google Sheets API</li>
              <li>Meta Ads / TikTok Ads API</li>
              <li>Python automations</li>
              <li>N8N Workflows</li>
            </ul>
          </div>
        </div>

        <!-- Project: balance for Meta -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Automation balance for Meta</div>
            <div class="proj-name lang-ar">تنبيه رصيد الإعلانات (Meta)</div>
            <div class="proj-pill">Alert</div>
          </div>

          <div class="proj-desc lang-en">
            Tracks ad account balance / payment threshold and pings the team
            before ads stop. Prevents campaigns from pausing in the middle of the day.
          </div>
          <div class="proj-desc lang-ar">
            بيراقب رصيد حساب الإعلانات / الـthreshold
            ويبعت تنبيه للفريق قبل ما الإعلانات تتقفّل لوحدها.
            بيمنع توقف حملات شغالة.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>Meta Marketing API</li>
              <li>WhatsApp / Discord webhook</li>
              <li>Scheduled jobs</li>
              <li>N8N Workflows</li>

            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- CATEGORY 2: Security & Access -->
    <section class="category-block">
      <div class="cat-head">
        <div class="lang-en">Security & Access</div>
        <div class="lang-ar">الأمان و الوصول</div>

        <div class="cat-note lang-en">Stop sharing same password</div>
        <div class="cat-note lang-ar">مفيش باسوورد واحد عند كل الناس</div>
      </div>

      <div class="projects-grid">
        <!-- WP password rotation -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Auto-change password (WordPress)</div>
            <div class="proj-name lang-ar">تغيير باسورد أوتوماتيك (ووردبريس)</div>
            <div class="proj-pill">Security</div>
          </div>

          <div class="proj-desc lang-en">
            Rotates WordPress admin passwords on a schedule and sends the new secure login
            to the owner only. Team members get temporary access links, not the real password.
          </div>
          <div class="proj-desc lang-ar">
            بيغير باسورد الأدمن بتاع ووردبريس بمواعيد ثابتة،
            ويبعته للOwner بس. باقي الفريق بياخد لينكات دخول مؤقتة مش الباسورد الأصلي.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>WordPress REST API</li>
              <li>PHP hooks / Python scheduler</li>
              <li>Secure vault delivery</li>
              <li>Python automations</li>
            </ul>
          </div>
        </div>

        <!-- Laravel password rotation -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Auto-change password (Laravel)</div>
            <div class="proj-name lang-ar">تغيير باسورد أوتوماتيك (لارافيل)</div>
            <div class="proj-pill">Security</div>
          </div>

          <div class="proj-desc lang-en">
            Same logic for Laravel dashboards / admin panels.
            Reduces "ex-employee still has access" risk.
          </div>
          <div class="proj-desc lang-ar">
            نفس الفكرة على لوحات التحكم المبنية بـLaravel.
            الهدف: نقلل مخاطرة إن حد قديم لسه معاه أكسس.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>Laravel Auth / Tokens</li>
              <li>Cron / Scheduler</li>
              <li>Access logging</li>
              <li>Python automations</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- CATEGORY 3: Reports & Orders -->
    <section class="category-block">
      <div class="cat-head">
        <div class="lang-en">Reports & Orders</div>
        <div class="lang-ar">الريبورتات و الأوردرات</div>

        <div class="cat-note lang-en">Visibility + QA</div>
        <div class="cat-note lang-ar">كل حاجة تحت السيطرة</div>
      </div>

      <div class="projects-grid">
        <!-- Automation reports -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Automation reports</div>
            <div class="proj-name lang-ar">ريبورتات أوتوماتيك</div>
            <div class="proj-pill">Dashboard</div>
          </div>

          <div class="proj-desc lang-en">
            Generates PDF / screenshot summaries for sales, spend, ROAS, AOV,
            and sends them on a fixed schedule to management.
          </div>
          <div class="proj-desc lang-ar">
            بيولد تقرير جاهز (PDF أو صورة) فيه المبيعات، الصرف على الإعلانات،
            ROAS، متوسط قيمة الطلب. بيتبعت في مواعيد ثابتة للإدارة.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>Python reporting scripts</li>
              <li>Google Sheets / WooCommerce / Meta Ads APIs</li>
              <li>WhatsApp / Discord delivery</li>
            </ul>
          </div>
        </div>

        <!-- order test bot -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Automation order test bot</div>
            <div class="proj-name lang-ar">بوت فحص الأوردرات</div>
            <div class="proj-pill">QA</div>
          </div>

          <div class="proj-desc lang-en">
            Automatically places a dummy order / test order on the store to confirm:
            checkout works, payment works, confirmation flows work.
            Alerts if anything breaks.
          </div>
          <div class="proj-desc lang-ar">
            البوت بيعمل أوردر وهمي أوتوماتيك عشان يتأكد إن:
            الكارت شغال، الدفع شغال، الكونفرميشن شغال.
            لو في حاجة وقعت → تنبيه.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>WooCommerce / Shopify API</li>
              <li>Headless browser testing</li>
              <li>Python automations</li>
              <li>Alert webhook</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- CATEGORY 4: Sales & Monitoring -->
    <section class="category-block">
      <div class="cat-head">
        <div class="lang-en">Sales & Monitoring</div>
        <div class="lang-ar">المبيعات و المراقبة</div>

        <div class="cat-note lang-en">Live pulse of the business</div>
        <div class="cat-note lang-ar">نبض البزنس لحظي</div>
      </div>

      <div class="projects-grid">
        <!-- sales screen WP -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Automation sales screen (WordPress)</div>
            <div class="proj-name lang-ar">شاشة مبيعات لحظية (ووردبريس)</div>
            <div class="proj-pill">Live Dashboard</div>
          </div>

          <div class="proj-desc lang-en">
            Internal dashboard showing live orders, revenue, top SKUs
            for a WordPress/WooCommerce store. Designed for owners to keep open all day.
          </div>
          <div class="proj-desc lang-ar">
            داشبورد داخلية بتعرض المبيعات والمنتجات الأعلى بيع لحظيًا
            لستور WooCommerce. معمول عشان الأونر يسيبه مفتوح طول اليوم.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>WooCommerce API</li>
              <li>Python automations</li>
              <li>Auto-refresh</li>
            </ul>
          </div>
        </div>

        <!-- sales screen Laravel -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Automation sales screen (Laravel)</div>
            <div class="proj-name lang-ar">شاشة مبيعات لحظية (لارافيل)</div>
            <div class="proj-pill">Live Dashboard</div>
          </div>

          <div class="proj-desc lang-en">
            Same idea but for custom Laravel ecommerce / back-office systems.
            Pulls revenue, orders, conversion rate, and ROAS in near real-time.
          </div>
          <div class="proj-desc lang-ar">
            نفس الفكرة بس للستورز المبنية Laravel.
            يعرض الإيراد، عدد الأوردرات، الكونفرشن، والـROAS بشكل شبه لحظي.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>Laravel API / Queues</li>
              <li>Ad spend data merge</li>
              <li>Realtime push</li>
            </ul>
          </div>
        </div>

        <!-- server bot -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Automation server bot</div>
            <div class="proj-name lang-ar">بوت مراقبة السيرفرات</div>
            <div class="proj-pill">Monitoring</div>
          </div>

          <div class="proj-desc lang-en">
            Monitors all servers + Cloudflare rules + uptime.
            Sends alert when CPU is high, checkout is slow, or firewall is blocking legit traffic.
          </div>
          <div class="proj-desc lang-ar">
            بيراقب كل السيرفرات + Cloudflare rules + الـuptime.
            يبعت إنذار لو CPU عالي، الشيك آوت بطيء، أو Cloudflare بيخنق عميل حقيقي بالغلط.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>Cloudflare API</li>
              <li>Server health checks</li>
              <li>Discord / WhatsApp alerts</li>
              <li>Python automations</li>

            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- CATEGORY 5: Testing & Quality -->
    <section class="category-block">
      <div class="cat-head">
        <div class="lang-en">Testing & Quality</div>
        <div class="lang-ar">اختبار و جودة</div>

        <div class="cat-note lang-en">Catch broken stuff early</div>
        <div class="cat-note lang-ar">نلحق الغلط بدري</div>
      </div>

      <div class="projects-grid">
        <!-- site test bot -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Automation test site bot</div>
            <div class="proj-name lang-ar">بوت فحص الموقع</div>
            <div class="proj-pill">QA</div>
          </div>

          <div class="proj-desc lang-en">
            Bot that crawls categories, products, reviews, and images.
            Flags missing images, wrong price formats, broken product pages.
          </div>
          <div class="proj-desc lang-ar">
            بوت يلف على كل الأقسام والمنتجات والريفيوهات والصور.
            يعلّم لو في صور ناقصة، سعر بايظ، صفحة منتج مكسورة.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>Headless browser crawling</li>
              <li>WooCommerce / Laravel / Custom stores</li>
              <li>Auto QA report</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- CATEGORY 6: Alerts & Notifications -->
    <section class="category-block">
      <div class="cat-head">
        <div class="lang-en">Alerts & Notifications</div>
        <div class="lang-ar">تنبيهات و إنذارات</div>

        <div class="cat-note lang-en">You know first</div>
        <div class="cat-note lang-ar">إنت أول حد يعرف</div>
      </div>

      <div class="projects-grid">
        <!-- domain alert -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Automation alert – Domains</div>
            <div class="proj-name lang-ar">تنبيه الدومينات</div>
            <div class="proj-pill">Safety</div>
          </div>

          <div class="proj-desc lang-en">
            Watches domain status / DNS / SSL expiry and warns before something goes offline.
            No more “site is down because SSL expired”.
          </div>
          <div class="proj-desc lang-ar">
            بيراقب حالة الدومين / الـDNS / الـSSL ويبلغك قبل ما حاجة تقع.
            يعني مفيش بقى "الموقع واقع علشان الـSSL خلص".
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>DNS / SSL checks</li>
              <li>Domain registrar API</li>
              <li>Alert to WhatsApp / Discord</li>
              <li>N8N Workflows</li>

            </ul>
          </div>
        </div>

        <!-- server alert -->
        <div class="proj-card">
          <div class="proj-topline">
            <div class="proj-name lang-en">Automation alert – Servers</div>
            <div class="proj-name lang-ar">تنبيه السيرفرات</div>
            <div class="proj-pill">Infra</div>
          </div>

          <div class="proj-desc lang-en">
            CPU high? Memory leak? Disk almost full? Instant alert.
            The idea: you know before the store slows down and costs you sales.
          </div>
          <div class="proj-desc lang-ar">
            الـCPU مولع؟ الرام بتتهلك؟ الهارد فاضل فيه 2%؟ يجيلك إنذار فورًا.
            الفكرة: تعرف قبل ما الستور يهبّط ويضيع مبيعات.
          </div>

          <div class="proj-meta">
            <div class="proj-meta-title lang-en">Tech:</div>
            <div class="proj-meta-title lang-ar">التقنية:</div>
            <ul class="meta-list">
              <li>Server metrics polling</li>
              <li>Custom thresholds per client</li>
              <li>WhatsApp / Discord alert bots</li>
              <li>N8N Workflows</li>

            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- FOOTER -->
    <footer>
      <div class="foot-name">Mina Mamdouh</div>

      <div class="lang-en">I build automations for ecommerce teams.</div>
      <div class="lang-ar">ببني أوتوميشن لستورات الأونلاين.</div>

      <div style="margin-top:.5rem;">
        <span class="lang-en">Based in Egypt. Working remote.</span>
        <span class="lang-ar">في مصر. شغال ريموت.</span>
      </div>

      <div style="margin-top:.5rem;color:var(--text-dim);">
        WhatsApp: +20 127 653 5995 · gminamamdouh@gmail.com
      </div>
    </footer>

  </div><!-- /wrapper -->

<script>
  // language toggle logic
  const toggleBtn = document.getElementById('langToggle');
  let current = "en";

  function setLang(mode) {
    current = mode;
    if (mode === "ar") {
      document.documentElement.lang = "ar";
      document.body.setAttribute("dir", "rtl");
      toggleBtn.textContent = "English";
    } else {
      document.documentElement.lang = "en";
      document.body.setAttribute("dir", "ltr");
      toggleBtn.textContent = "العربية";
    }
  }

  // init English default
  setLang("en");

  toggleBtn.addEventListener("click", () => {
    setLang(current === "en" ? "ar" : "en");
  });
</script>

</body>
</html>
