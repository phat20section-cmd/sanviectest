<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kĩ Năng Săn Việc - Ebook</title>
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&family=Be+Vietnam+Pro:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --orange: #F47820;
    --orange-dark: #E06510;
    --orange-light: #FF9A45;
    --cream: #FDF5EC;
    --cream-dark: #F5EAD8;
    --dark: #1A1A1A;
    --text: #3D3D3D;
    --text-light: #6B6B6B;
    --white: #FFFFFF;
    --green: #2ECC71;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Be Vietnam Pro', sans-serif;
    background: var(--cream);
    color: var(--dark);
    overflow-x: hidden;
  }

  /* ===== HERO ===== */
  .hero {
    background: var(--orange);
    position: relative;
    overflow: hidden;
    padding: 60px 24px 0;
    text-align: center;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 280px; height: 280px;
    background: var(--orange-dark);
    border-radius: 50%;
    opacity: 0.6;
  }

  .hero::after {
    content: '';
    position: absolute;
    top: 40px; right: -40px;
    width: 160px; height: 160px;
    background: var(--orange-light);
    border-radius: 50%;
    opacity: 0.5;
  }

  .badge {
    display: inline-block;
    background: var(--orange-dark);
    color: var(--white);
    font-family: 'Nunito', sans-serif;
    font-weight: 800;
    font-size: 13px;
    letter-spacing: 2px;
    padding: 6px 18px;
    border-radius: 6px;
    margin-bottom: 24px;
    position: relative;
    z-index: 1;
  }

  .hero-title {
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: clamp(52px, 12vw, 88px);
    line-height: 1;
    color: var(--white);
    text-transform: uppercase;
    position: relative;
    z-index: 1;
    margin-bottom: 16px;
    letter-spacing: -1px;
  }

  .hero-divider {
    width: 120px;
    height: 3px;
    background: var(--white);
    opacity: 0.6;
    margin: 0 auto 20px;
    position: relative;
    z-index: 1;
  }

  .hero-tagline {
    font-family: 'Nunito', sans-serif;
    font-weight: 700;
    font-size: clamp(13px, 3vw, 16px);
    color: var(--white);
    letter-spacing: 2px;
    text-transform: uppercase;
    opacity: 0.9;
    position: relative;
    z-index: 1;
    margin-bottom: 12px;
  }

  .hero-sub {
    font-size: 15px;
    color: rgba(255,255,255,0.85);
    max-width: 340px;
    margin: 0 auto 32px;
    line-height: 1.6;
    position: relative;
    z-index: 1;
  }

  .cta-main {
    display: inline-block;
    background: var(--white);
    color: var(--orange);
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: 16px;
    padding: 16px 40px;
    border-radius: 50px;
    text-decoration: none;
    letter-spacing: 0.5px;
    margin-bottom: 40px;
    position: relative;
    z-index: 1;
    box-shadow: 0 8px 24px rgba(0,0,0,0.15);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .cta-main:hover { transform: translateY(-2px); box-shadow: 0 12px 32px rgba(0,0,0,0.2); }

  .hero-price-note {
    font-size: 13px;
    color: rgba(255,255,255,0.75);
    margin-bottom: 40px;
    position: relative;
    z-index: 1;
  }

  .hero-illustration {
    position: relative;
    z-index: 1;
    background: var(--cream);
    border-radius: 24px 24px 0 0;
    padding: 40px 20px 0;
    margin: 0 -24px;
  }

  .illustration-svg {
    max-width: 320px;
    margin: 0 auto;
    display: block;
  }

  /* ===== PAIN SECTION ===== */
  .section {
    padding: 64px 24px;
    max-width: 600px;
    margin: 0 auto;
  }

  .section-badge {
    display: inline-block;
    background: var(--orange);
    color: var(--white);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 2px;
    padding: 5px 14px;
    border-radius: 20px;
    margin-bottom: 16px;
    text-transform: uppercase;
  }

  .section-title {
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: clamp(26px, 6vw, 36px);
    line-height: 1.2;
    margin-bottom: 8px;
    color: var(--dark);
  }

  .section-sub {
    font-size: 15px;
    color: var(--text-light);
    margin-bottom: 36px;
    line-height: 1.6;
  }

  /* Pain cards */
  .pain-grid {
    display: grid;
    gap: 14px;
  }

  .pain-card {
    background: var(--white);
    border-radius: 16px;
    padding: 20px;
    display: flex;
    align-items: flex-start;
    gap: 16px;
    box-shadow: 0 2px 12px rgba(0,0,0,0.06);
    border-left: 4px solid var(--orange);
    transition: transform 0.2s;
  }
  .pain-card:hover { transform: translateX(4px); }

  .pain-icon {
    font-size: 28px;
    flex-shrink: 0;
    margin-top: 2px;
  }

  .pain-text {
    font-size: 15px;
    line-height: 1.5;
    color: var(--text);
    font-weight: 500;
  }

  .pain-text strong {
    color: var(--orange-dark);
    display: block;
    font-size: 16px;
    margin-bottom: 4px;
  }

  /* ===== SOLUTION SECTION ===== */
  .solution-section {
    background: var(--orange);
    padding: 64px 24px;
    position: relative;
    overflow: hidden;
  }

  .solution-section::before {
    content: '';
    position: absolute;
    bottom: -60px; right: -60px;
    width: 200px; height: 200px;
    background: var(--orange-dark);
    border-radius: 50%;
    opacity: 0.4;
  }

  .solution-inner {
    max-width: 600px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }

  .solution-section .section-badge {
    background: rgba(255,255,255,0.25);
    color: var(--white);
  }

  .solution-section .section-title {
    color: var(--white);
  }

  .solution-section .section-sub {
    color: rgba(255,255,255,0.8);
  }

  .checklist {
    display: grid;
    gap: 14px;
  }

  .check-item {
    background: rgba(255,255,255,0.15);
    backdrop-filter: blur(4px);
    border-radius: 14px;
    padding: 16px 20px;
    display: flex;
    align-items: flex-start;
    gap: 14px;
    border: 1px solid rgba(255,255,255,0.2);
  }

  .check-icon {
    width: 28px; height: 28px;
    background: var(--white);
    color: var(--orange);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 14px;
    font-weight: 900;
    flex-shrink: 0;
    margin-top: 1px;
  }

  .check-text {
    color: var(--white);
    font-size: 15px;
    line-height: 1.5;
    font-weight: 500;
  }

  .check-text strong {
    display: block;
    font-size: 16px;
    font-weight: 700;
    margin-bottom: 2px;
  }

  /* ===== CONTENT SECTION ===== */
  .content-section {
    background: var(--cream);
    padding: 64px 24px;
  }

  .content-inner {
    max-width: 600px;
    margin: 0 auto;
  }

  .chapters {
    display: grid;
    gap: 12px;
  }

  .chapter-card {
    background: var(--white);
    border-radius: 14px;
    padding: 18px 20px;
    display: flex;
    gap: 16px;
    align-items: flex-start;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    transition: box-shadow 0.2s;
  }
  .chapter-card:hover { box-shadow: 0 4px 16px rgba(244,120,32,0.15); }

  .chapter-num {
    width: 36px; height: 36px;
    background: var(--orange);
    color: var(--white);
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: 15px;
    flex-shrink: 0;
  }

  .chapter-info {}
  .chapter-title {
    font-weight: 700;
    font-size: 15px;
    color: var(--dark);
    margin-bottom: 3px;
  }
  .chapter-desc {
    font-size: 13px;
    color: var(--text-light);
    line-height: 1.4;
  }

  .bonus-card {
    background: linear-gradient(135deg, var(--orange), var(--orange-dark));
    border-radius: 14px;
    padding: 18px 20px;
    display: flex;
    gap: 16px;
    align-items: center;
  }

  .bonus-icon {
    font-size: 32px;
  }

  .bonus-text .chapter-title { color: var(--white); }
  .bonus-text .chapter-desc { color: rgba(255,255,255,0.8); }

  /* ===== DIFF SECTION ===== */
  .diff-section {
    background: var(--cream-dark);
    padding: 64px 24px;
  }

  .diff-inner { max-width: 600px; margin: 0 auto; }

  .compare-box {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
    margin-bottom: 32px;
  }

  .compare-card {
    border-radius: 16px;
    padding: 20px;
  }

  .compare-card.bad {
    background: #fff0eb;
    border: 2px solid #ffcbb0;
  }

  .compare-card.good {
    background: var(--orange);
    border: 2px solid var(--orange-dark);
  }

  .compare-label {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .compare-card.bad .compare-label { color: #cc5500; }
  .compare-card.good .compare-label { color: rgba(255,255,255,0.8); }

  .compare-text {
    font-size: 14px;
    line-height: 1.6;
    font-weight: 500;
  }
  .compare-card.bad .compare-text { color: var(--text); }
  .compare-card.good .compare-text { color: var(--white); }

  .diff-points {
    display: grid;
    gap: 12px;
  }

  .diff-point {
    background: var(--white);
    border-radius: 14px;
    padding: 16px 20px;
    display: flex;
    gap: 14px;
    align-items: center;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  }

  .diff-emoji { font-size: 24px; }

  .diff-txt {
    font-size: 14px;
    line-height: 1.5;
    color: var(--text);
    font-weight: 500;
  }

  /* ===== AUTHOR SECTION ===== */
  .author-section {
    background: var(--white);
    padding: 64px 24px;
  }

  .author-inner { max-width: 600px; margin: 0 auto; }

  .author-card {
    background: var(--cream);
    border-radius: 24px;
    padding: 32px 24px;
    text-align: center;
  }

  .author-avatar {
    width: 90px; height: 90px;
    background: var(--orange);
    border-radius: 50%;
    margin: 0 auto 16px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 36px;
    border: 4px solid var(--white);
    box-shadow: 0 4px 16px rgba(244,120,32,0.3);
  }

  .author-name {
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: 24px;
    color: var(--dark);
    margin-bottom: 4px;
  }

  .author-handle {
    font-size: 14px;
    color: var(--orange);
    font-weight: 600;
    margin-bottom: 16px;
  }

  .author-stats {
    display: flex;
    justify-content: center;
    gap: 24px;
    margin-bottom: 20px;
  }

  .stat {
    text-align: center;
  }

  .stat-num {
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: 22px;
    color: var(--orange);
    display: block;
  }

  .stat-label {
    font-size: 12px;
    color: var(--text-light);
  }

  .author-quote {
    background: var(--white);
    border-radius: 16px;
    padding: 20px;
    font-size: 15px;
    line-height: 1.7;
    color: var(--text);
    font-style: italic;
    border-left: 4px solid var(--orange);
    text-align: left;
    position: relative;
  }

  .quote-mark {
    font-size: 48px;
    color: var(--orange);
    opacity: 0.3;
    line-height: 0;
    position: absolute;
    top: 28px; left: 12px;
    font-family: Georgia, serif;
  }

  /* ===== CTA FINAL ===== */
  .cta-section {
    background: var(--orange);
    padding: 72px 24px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .cta-section::before {
    content: '';
    position: absolute;
    top: -80px; left: -80px;
    width: 240px; height: 240px;
    background: var(--orange-dark);
    border-radius: 50%;
    opacity: 0.5;
  }

  .cta-section::after {
    content: '';
    position: absolute;
    bottom: -60px; right: -60px;
    width: 180px; height: 180px;
    background: var(--orange-light);
    border-radius: 50%;
    opacity: 0.4;
  }

  .cta-inner {
    max-width: 480px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }

  .cta-title {
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: clamp(28px, 7vw, 42px);
    color: var(--white);
    line-height: 1.2;
    margin-bottom: 12px;
  }

  .cta-sub {
    font-size: 16px;
    color: rgba(255,255,255,0.85);
    margin-bottom: 32px;
    line-height: 1.6;
  }

  .price-tag {
    display: inline-block;
    background: rgba(255,255,255,0.2);
    border: 2px solid rgba(255,255,255,0.4);
    border-radius: 50px;
    padding: 10px 28px;
    color: var(--white);
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: 22px;
    margin-bottom: 24px;
  }

  .price-note {
    font-size: 13px;
    color: rgba(255,255,255,0.7);
    margin-bottom: 24px;
  }

  .cta-btn {
    display: block;
    background: var(--white);
    color: var(--orange);
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: 18px;
    padding: 20px 40px;
    border-radius: 50px;
    text-decoration: none;
    letter-spacing: 0.5px;
    margin-bottom: 16px;
    box-shadow: 0 8px 32px rgba(0,0,0,0.2);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .cta-btn:hover { transform: translateY(-3px); box-shadow: 0 14px 40px rgba(0,0,0,0.25); }

  .cta-guarantee {
    font-size: 13px;
    color: rgba(255,255,255,0.75);
    margin-bottom: 6px;
  }

  .cta-email {
    font-size: 13px;
    color: rgba(255,255,255,0.9);
    font-weight: 600;
  }

  /* ===== FOOTER ===== */
  .footer {
    background: var(--dark);
    padding: 24px;
    text-align: center;
    font-size: 13px;
    color: rgba(255,255,255,0.4);
  }

  .footer span { color: var(--orange); }

  /* ===== STICKY CTA ===== */
  .sticky-cta {
    position: fixed;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 100;
    display: none;
  }

  .sticky-cta a {
    display: inline-block;
    background: var(--orange);
    color: var(--white);
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: 15px;
    padding: 14px 32px;
    border-radius: 50px;
    text-decoration: none;
    box-shadow: 0 8px 24px rgba(244,120,32,0.5);
    white-space: nowrap;
    transition: transform 0.2s;
  }
  .sticky-cta a:hover { transform: scale(1.03); }

  @media(min-width: 480px) {
    .sticky-cta { display: block; }
  }

  /* Animations */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .hero-title { animation: fadeUp 0.6s ease both; }
  .hero-tagline { animation: fadeUp 0.6s 0.1s ease both; }
  .hero-sub { animation: fadeUp 0.6s 0.2s ease both; }
  .cta-main { animation: fadeUp 0.6s 0.3s ease both; }
</style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <div class="badge">📘 EBOOK</div>
  <h1 class="hero-title">KĨ NĂNG<br>SĂN VIỆC</h1>
  <div class="hero-divider"></div>
  <p class="hero-tagline">CV Chuẩn · Phỏng Vấn Chất · Offer Ngon</p>
  <p class="hero-sub">Bạn không thiếu năng lực. Bạn chỉ chưa biết cách <strong>thể hiện đúng cách.</strong></p>
  <a href="#cta" class="cta-main">📩 SỞ HỮU NGAY — Chỉ 79K</a>
  <p class="hero-price-note">Bằng 1 ly trà sữa ☕ — dùng cả đời 🔥</p>
  <div class="hero-illustration">
    <!-- SVG Illustration giống bìa ebook -->
    <svg class="illustration-svg" viewBox="0 0 320 220" fill="none" xmlns="http://www.w3.org/2000/svg">
      <!-- Laptop -->
      <rect x="105" y="130" width="110" height="68" rx="8" fill="#E8E0D4" stroke="#333" stroke-width="2.5"/>
      <rect x="112" y="137" width="96" height="52" rx="4" fill="#fff" stroke="#333" stroke-width="1.5"/>
      <ellipse cx="160" cy="200" rx="14" ry="4" fill="#C8B89A"/>
      <rect x="90" y="197" width="140" height="6" rx="3" fill="#D4C5B0" stroke="#333" stroke-width="1.5"/>
      <!-- Laptop screen lines -->
      <rect x="120" y="144" width="60" height="3" rx="1.5" fill="#F47820" opacity="0.5"/>
      <rect x="120" y="151" width="45" height="2" rx="1" fill="#ccc"/>
      <rect x="120" y="157" width="50" height="2" rx="1" fill="#ccc"/>
      <!-- Spark -->
      <path d="M155 128 L158 120 L161 128 L169 131 L161 134 L158 142 L155 134 L147 131 Z" fill="#F47820" stroke="#E06510" stroke-width="1"/>
      <!-- Person Left -->
      <circle cx="72" cy="88" r="22" fill="#F47820" stroke="#333" stroke-width="2"/>
      <circle cx="72" cy="88" r="14" fill="#FFDBB0" stroke="#333" stroke-width="2"/>
      <ellipse cx="72" cy="108" rx="28" ry="18" fill="#F47820" stroke="#333" stroke-width="2"/>
      <!-- left arm raised -->
      <path d="M94 95 Q108 78 104 68" stroke="#F47820" stroke-width="10" stroke-linecap="round" fill="none"/>
      <circle cx="103" cy="66" r="8" fill="#FFDBB0" stroke="#333" stroke-width="2"/>
      <!-- left arm resting -->
      <path d="M50 105 Q36 118 42 128" stroke="#F47820" stroke-width="10" stroke-linecap="round" fill="none"/>
      <circle cx="43" cy="130" r="8" fill="#FFDBB0" stroke="#333" stroke-width="2"/>
      <!-- Speech bubble left -->
      <rect x="26" y="42" width="60" height="34" rx="10" fill="#fff" stroke="#333" stroke-width="2"/>
      <path d="M56 76 L52 86 L62 76" fill="#fff" stroke="#333" stroke-width="2" stroke-linejoin="round"/>
      <rect x="33" y="51" width="40" height="3" rx="1.5" fill="#ccc"/>
      <rect x="33" y="58" width="32" height="3" rx="1.5" fill="#ccc"/>
      <rect x="33" y="65" width="36" height="3" rx="1.5" fill="#ccc"/>
      <!-- Person Right -->
      <circle cx="248" cy="88" r="22" fill="#F47820" stroke="#333" stroke-width="2"/>
      <circle cx="248" cy="88" r="14" fill="#FFDBB0" stroke="#333" stroke-width="2"/>
      <!-- Hair right person -->
      <path d="M234 80 Q248 68 262 80" stroke="#222" stroke-width="6" stroke-linecap="round" fill="none"/>
      <path d="M262 80 Q268 90 265 100" stroke="#222" stroke-width="5" stroke-linecap="round" fill="none"/>
      <ellipse cx="248" cy="108" rx="28" ry="18" fill="#F47820" stroke="#333" stroke-width="2"/>
      <!-- right arm left -->
      <path d="M226 105 Q218 118 224 128" stroke="#F47820" stroke-width="10" stroke-linecap="round" fill="none"/>
      <circle cx="225" cy="130" r="8" fill="#FFDBB0" stroke="#333" stroke-width="2"/>
      <!-- right arm right -->
      <path d="M270 105 Q280 118 276 128" stroke="#F47820" stroke-width="10" stroke-linecap="round" fill="none"/>
      <circle cx="275" cy="130" r="8" fill="#FFDBB0" stroke="#333" stroke-width="2"/>
      <!-- Speech bubble right (orange) -->
      <rect x="232" y="42" width="60" height="34" rx="10" fill="#F47820" stroke="#333" stroke-width="2"/>
      <path d="M252 76 L248 86 L258 76" fill="#F47820" stroke="#333" stroke-width="2" stroke-linejoin="round"/>
      <rect x="239" y="51" width="40" height="3" rx="1.5" fill="rgba(255,255,255,0.6)"/>
      <rect x="239" y="58" width="32" height="3" rx="1.5" fill="rgba(255,255,255,0.6)"/>
      <rect x="239" y="65" width="36" height="3" rx="1.5" fill="rgba(255,255,255,0.6)"/>
    </svg>
  </div>
</section>

<!-- PAIN POINTS -->
<section style="background:var(--cream); padding: 64px 24px;">
  <div style="max-width:600px; margin:0 auto;">
    <span class="section-badge">😅 PAIN POINTS</span>
    <h2 class="section-title">Bạn có đang mắc kẹt ở đây không?</h2>
    <p class="section-sub">Nếu gật đầu với bất kỳ điều nào dưới đây — ebook này viết cho bạn đấy.</p>
    <div class="pain-grid">
      <div class="pain-card">
        <div class="pain-icon">📨</div>
        <div class="pain-text">
          <strong>CV gửi mãi không ai gọi lại</strong>
          Bạn apply hàng chục công ty nhưng chỉ nhận được... tiếng im lặng.
        </div>
      </div>
      <div class="pain-card">
        <div class="pain-icon">😬</div>
        <div class="pain-text">
          <strong>Phỏng vấn ấp úng, nhạt như nước ốc</strong>
          Trả lời y chang 100 ứng viên khác, không có gì đáng nhớ.
        </div>
      </div>
      <div class="pain-card">
        <div class="pain-icon">🤷</div>
        <div class="pain-text">
          <strong>Không biết mình có gì để viết vào CV</strong>
          Nhìn tờ CV trắng trơn mà không biết bắt đầu từ đâu.
        </div>
      </div>
      <div class="pain-card">
        <div class="pain-icon">😰</div>
        <div class="pain-text">
          <strong>Sợ bị hỏi điểm yếu, lương, lý do nghỉ việc</strong>
          Những câu hỏi tưởng đơn giản mà làm bạn toát mồ hôi lạnh.
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SOLUTION -->
<section class="solution-section">
  <div class="solution-inner">
    <span class="section-badge">✅ SAU KHI ĐỌC EBOOK NÀY</span>
    <h2 class="section-title" style="color:white">Bạn sẽ làm được những điều này</h2>
    <p class="section-sub">Không phải lý thuyết suông — đây là những kỹ năng bạn áp dụng được ngay.</p>
    <div class="checklist">
      <div class="check-item">
        <div class="check-icon">✓</div>
        <div class="check-text"><strong>Khai phá "thành tựu ngầm" của bản thân</strong>Những thứ bạn tưởng bình thường lại là bằng chứng rõ nhất cho năng lực của bạn.</div>
      </div>
      <div class="check-item">
        <div class="check-icon">✓</div>
        <div class="check-text"><strong>Viết CV có số má bằng công thức XYZ của Google</strong>Không còn viết CV như liệt kê đầu việc. Mỗi dòng đều có kết quả đo lường được.</div>
      </div>
      <div class="check-item">
        <div class="check-icon">✓</div>
        <div class="check-text"><strong>Phỏng vấn tự tin với SHOW DON'T TELL & STAR</strong>Để nhà tuyển dụng tự kết luận bạn giỏi — thay vì bạn tự khen mình.</div>
      </div>
      <div class="check-item">
        <div class="check-icon">✓</div>
        <div class="check-text"><strong>Nhận diện công ty bất ổn trước khi ký hợp đồng</strong>Những dấu hiệu đỏ mà nhà tuyển dụng sẽ không bao giờ chủ động nói.</div>
      </div>
      <div class="check-item">
        <div class="check-icon">✓</div>
        <div class="check-text"><strong>Có bộ Prompt AI thực chiến đầy đủ</strong>Để viết CV, luyện phỏng vấn và research công ty — tiết kiệm hàng giờ đồng hồ.</div>
      </div>
      <div class="check-item">
        <div class="check-icon">✓</div>
        <div class="check-text"><strong>Thử việc đúng cách để không phải thử việc lại</strong>Chiến lược 60 ngày đầu để được giữ lại và tạo dấu ấn thực sự.</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTENT -->
<section class="content-section">
  <div class="content-inner">
    <span class="section-badge">📖 NỘI DUNG</span>
    <h2 class="section-title">90+ trang kiến thức thực chiến</h2>
    <p class="section-sub" style="margin-bottom:28px">Cấu trúc rõ ràng từ A–Z — từ khai phá bản thân đến vượt qua thử việc.</p>
    <div class="chapters">
      <div class="chapter-card">
        <div class="chapter-num">1</div>
        <div class="chapter-info">
          <div class="chapter-title">Khai Phá Tiềm Năng Bản Thân</div>
          <div class="chapter-desc">Template bản đồ năng lực · Cách lấp đầy khoảng trống kỹ năng</div>
        </div>
      </div>
      <div class="chapter-card">
        <div class="chapter-num">2</div>
        <div class="chapter-info">
          <div class="chapter-title">Viết CV Chỉ Là Chuyện Nhỏ</div>
          <div class="chapter-desc">Công thức XYZ · Chọn template chuẩn · Prompt AI viết CV</div>
        </div>
      </div>
      <div class="chapter-card">
        <div class="chapter-num">3</div>
        <div class="chapter-info">
          <div class="chapter-title">Trả Lời Phỏng Vấn Chuyên Nghiệp</div>
          <div class="chapter-desc">SHOW DON'T TELL · Mô hình STAR · Checklist buổi phỏng vấn</div>
        </div>
      </div>
      <div class="chapter-card">
        <div class="chapter-num">4</div>
        <div class="chapter-info">
          <div class="chapter-title">10 Mẫu Email Quan Trọng</div>
          <div class="chapter-desc">Xin việc · Cảm ơn · Hỏi kết quả · Nhận offer · Từ chối offer</div>
        </div>
      </div>
      <div class="chapter-card">
        <div class="chapter-num">5</div>
        <div class="chapter-info">
          <div class="chapter-title">Điều Công Ty Sẽ Không Nói Với Bạn</div>
          <div class="chapter-desc">Dấu hiệu công ty bất ổn · Cách đọc offer letter · Network đúng cách</div>
        </div>
      </div>
      <div class="chapter-card">
        <div class="chapter-num">6</div>
        <div class="chapter-info">
          <div class="chapter-title">Thử Việc Đúng Để Không Phải Thử Việc Lại</div>
          <div class="chapter-desc">Mindset · Tuần đầu tiên · Tạo dấu ấn có chiến lược · Checklist thử việc</div>
        </div>
      </div>
      <div class="bonus-card">
        <div class="bonus-icon">🤖</div>
        <div class="bonus-text">
          <div class="chapter-title">BONUS: Bộ Prompt AI Săn Việc Đầy Đủ</div>
          <div class="chapter-desc">Toàn bộ prompts để viết CV · luyện phỏng vấn · research công ty</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- DIFF -->
<section class="diff-section">
  <div class="diff-inner">
    <span class="section-badge">💡 ĐIỂM KHÁC BIỆT</span>
    <h2 class="section-title">Đây không phải ebook CV bình thường</h2>
    <p class="section-sub" style="margin-bottom:24px">Ebook khác cho bạn bài giải mẫu. Ebook này giúp bạn tìm ra bài giải của chính mình.</p>
    <div class="compare-box">
      <div class="compare-card bad">
        <div class="compare-label">❌ Ebook thường</div>
        <div class="compare-text">Cho bạn template đẹp để điền vào — nhưng không giúp bạn biết điền gì.</div>
      </div>
      <div class="compare-card good">
        <div class="compare-label">✅ Ebook này</div>
        <div class="compare-text">Giúp bạn khai phá những gì bạn đã có và trình bày chúng thuyết phục nhất.</div>
      </div>
    </div>
    <div class="diff-points">
      <div class="diff-point">
        <div class="diff-emoji">🎯</div>
        <div class="diff-txt">Viết từ kinh nghiệm thực tế — không phải lý thuyết sách giáo khoa</div>
      </div>
      <div class="diff-point">
        <div class="diff-emoji">💔</div>
        <div class="diff-txt">Tác giả từng bị từ chối nhiều lần — thực sự hiểu nỗi đau của bạn</div>
      </div>
      <div class="diff-point">
        <div class="diff-emoji">📝</div>
        <div class="diff-txt">Ví dụ cụ thể cho nhiều ngành: Marketing, Sales, Content, Gia sư, Bán hàng online...</div>
      </div>
      <div class="diff-point">
        <div class="diff-emoji">🤖</div>
        <div class="diff-txt">Tích hợp AI tools giúp tiết kiệm thời gian tối đa trong mọi bước</div>
      </div>
    </div>
  </div>
</section>

<!-- AUTHOR -->
<section class="author-section">
  <div class="author-inner">
    <span class="section-badge">👤 TÁC GIẢ</span>
    <h2 class="section-title" style="margin-bottom:24px">Người đứng sau cuốn ebook</h2>
    <div class="author-card">
      <div class="author-avatar">🧑‍💻</div>
      <div class="author-name">ThePhat</div>
      <div class="author-handle">@withthephat</div>
      <div class="author-stats">
        <div class="stat"><span class="stat-num">30K+</span><span class="stat-label">IG Followers</span></div>
        <div class="stat"><span class="stat-num">50K+</span><span class="stat-label">FB Followers</span></div>
        <div class="stat"><span class="stat-num">90+</span><span class="stat-label">Trang nội dung</span></div>
      </div>
      <div class="author-quote">
        <span class="quote-mark">"</span>
        <span style="padding-left: 20px; display: block;">Mình cũng từng gửi CV méo, CV đen thui và bị từ chối nhiều lần. Mình hiểu cảm giác đó. Và mình đã tìm ra cách vượt qua — rồi viết lại tất cả vào đây để bạn không cần mò mẫm như mình.</span>
      </div>
    </div>
  </div>
</section>

<!-- CTA FINAL -->
<section class="cta-section" id="cta">
  <div class="cta-inner">
    <div class="badge" style="margin-bottom:20px; background: rgba(255,255,255,0.2); color: white;">🔥 LẤY NGAY HÔM NAY</div>
    <h2 class="cta-title">Sẵn sàng săn được công việc xứng đáng chưa?</h2>
    <p class="cta-sub">Đầu tư một lần — dùng mãi cho cả hành trình sự nghiệp</p>
    <div class="price-tag">Chỉ 79.000đ</div>
    <p class="price-note">☕ Bằng 1 ly cà phê Starbucks — nhưng đổi lại cả sự nghiệp</p>
    <a href="mailto:work@withthephat.com" class="cta-btn">📩 TÔI MUỐN SỞ HỮU NGAY</a>
    <p class="cta-guarantee">💬 Không hài lòng? Liên hệ tác giả trực tiếp</p>
    <p class="cta-email">work@withthephat.com</p>
  </div>
</section>

<!-- FOOTER -->
<footer class="footer">
  <p>Made with ❤️ by <span>@withthephat</span> · Kĩ Năng Săn Việc 2025</p>
</footer>

<!-- Sticky CTA -->
<div class="sticky-cta">
  <a href="#cta">📩 SỞ HỮU NGAY — 79K</a>
</div>

</body>
</html>
