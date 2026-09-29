/* STREAMING_CHUNK:Defining CSS variables and global reset styles... */
/* ==========================================================================
   1. CSS Variables & Reset
   ========================================================================== */
:root {
    /* 色彩計劃 (Luxury Nude, Charcoal & Gold) */
    --color-bg: #FAF8F5;
    --color-surface: #FFFFFF;
    --color-primary: #2B2927;
    --color-secondary: #8C827A;
    --color-accent: #C5A059;
    --color-accent-light: #F4EFE6;
    --color-border: #E8E2D9;
    --color-text-dark: #1A1918;
    --color-text-muted: #66605B;
    --color-white: #FFFFFF;

    /* 字體 */
    --font-serif: 'Cormorant Garamond', 'Noto Serif TC', Georgia, serif;
    --font-sans: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;

    /* 間距與邊框 radius */
    --radius-sm: 4px;
    --radius-md: 8px;
    --radius-lg: 16px;
    --transition-smooth: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    --shadow-subtle: 0 4px 20px rgba(0, 0, 0, 0.05);
    --shadow-hover: 0 10px 30px rgba(0, 0, 0, 0.1);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    background-color: var(--color-bg);
    color: var(--color-text-dark);
    font-family: var(--font-sans);
    line-height: 1.6;
    font-size: 16px;
    -webkit-font-smoothing: antialiased;
}

h1, h2, h3, h4, .logo {
    font-family: var(--font-serif);
    font-weight: 600;
    letter-spacing: 0.5px;
}

img {
    max-width: 100%;
    height: auto;
    display: block;
}

a {
    text-decoration: none;
    color: inherit;
    transition: var(--transition-smooth);
}

ul {
    list-style: none;
}

/* ==========================================================================
   2. Layout Helpers & Typography
   ========================================================================== */
/* STREAMING_CHUNK:Styling responsive container and utility classes... */
.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}

.section {
    padding: 80px 0;
}

.text-center { text-align: center; }
.max-w-700 { max-width: 700px; margin-left: auto; margin-right: auto; }

.section-tag {
    display: inline-block;
    font-size: 0.85rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--color-accent);
    margin-bottom: 8px;
    font-weight: 600;
}

.section-header h2 {
    font-size: 2.5rem;
    margin-bottom: 12px;
    color: var(--color-primary);
}

.section-header p {
    color: var(--color-text-muted);
    font-size: 1.1rem;
    margin-bottom: 40px;
}

/* ==========================================================================
   3. Buttons & Badges
   ========================================================================== */
/* STREAMING_CHUNK:Designing buttons and status badges... */
.btn {
    display: inline-block;
    padding: 14px 28px;
    border-radius: var(--radius-sm);
    font-size: 0.95rem;
    font-weight: 500;
    letter-spacing: 1px;
    cursor: pointer;
    text-align: center;
    border: 1px solid transparent;
    transition: var(--transition-smooth);
}

.btn-primary {
    background-color: var(--color-primary);
    color: var(--color-white);
}

.btn-primary:hover {
    background-color: var(--color-accent);
    color: var(--color-white);
}

.btn-outline {
    background-color: transparent;
    border-color: var(--color-primary);
    color: var(--color-primary);
}

.btn-outline:hover {
    background-color: var(--color-primary);
    color: var(--color-white);
}

.btn-sm {
    padding: 8px 16px;
    font-size: 0.85rem;
}

.btn-lg {
    padding: 16px 36px;
    font-size: 1.05rem;
}

.badge {
    display: inline-block;
    padding: 4px 10px;
    border-radius: 20px;
    font-size: 0.75rem;
    font-weight: 600;
    letter-spacing: 0.5px;
}

.badge-gold {
    background-color: var(--color-accent-light);
    color: var(--color-accent);
    border: 1px solid var(--color-accent);
}

.badge-niche {
    background-color: var(--color-primary);
    color: var(--color-white);
}

/* ==========================================================================
   4. Header & Navigation (Responsive Menu pure CSS)
   ========================================================================== */
/* STREAMING_CHUNK:Styling header and hamburger menu... */
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background-color: rgba(250, 248, 245, 0.95);
    backdrop-filter: blur(10px);
    z-index: 1000;
    border-bottom: 1px solid var(--color-border);
    padding: 18px 0;
}

.nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 1.8rem;
    color: var(--color-primary);
    font-weight: 600;
    letter-spacing: 2px;
}

.logo span {
    font-size: 0.9rem;
    color: var(--color-accent);
    font-family: var(--font-sans);
    letter-spacing: 3px;
    display: block;
    margin-top: -6px;
}

.nav-links {
    display: flex;
    gap: 30px;
}

.nav-links a {
    font-size: 0.95rem;
    color: var(--color-text-dark);
    font-weight: 500;
}

.nav-links a:hover {
    color: var(--color-accent);
}

/* 漢堡選單 (純 CSS) */
.menu-toggle {
    display: none;
}

.hamburger {
    display: none;
    flex-direction: column;
    gap: 5px;
    cursor: pointer;
}

.hamburger span {
    width: 25px;
    height: 2px;
    background-color: var(--color-primary);
    transition: var(--transition-smooth);
}

/* ==========================================================================
   5. Hero Section
   ========================================================================== */
/* STREAMING_CHUNK:Styling hero image banner and overlay... */
.hero {
    position: relative;
    height: 85vh;
    min-height: 550px;
    display: flex;
    align-items: center;
    overflow: hidden;
    margin-top: 60px;
}

.hero-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}

.hero-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.hero-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, rgba(250, 248, 245, 0.92) 0%, rgba(250, 248, 245, 0.4) 100%);
}

.hero-content {
    position: relative;
    z-index: 2;
    max-width: 600px;
}

.hero-subtitle {
    font-size: 0.85rem;
    letter-spacing: 3px;
    color: var(--color-accent);
    font-weight: 600;
}

.hero-title {
    font-size: 3.5rem;
    line-height: 1.15;
    margin: 12px 0 20px;
    color: var(--color-primary);
}

.hero-description {
    font-size: 1.1rem;
    color: var(--color-text-muted);
    margin-bottom: 30px;
}

.hero-actions {
    display: flex;
    gap: 15px;
}

/* ==========================================================================
   6. Scenario Section (按場合情境選香)
   ========================================================================== */
/* STREAMING_CHUNK:Styling usage scenario cards grid... */
.scenarios-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.scenario-card {
    background-color: var(--color-surface);
    border-radius: var(--radius-md);
    overflow: hidden;
    box-shadow: var(--shadow-subtle);
    border: 1px solid var(--color-border);
    transition: var(--transition-smooth);
}

.scenario-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-hover);
}

.card-img-wrapper {
    height: 220px;
    overflow: hidden;
}

.card-img-wrapper img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: var(--transition-smooth);
}

.scenario-card:hover .card-img-wrapper img {
    transform: scale(1.05);
}

.card-content {
    padding: 24px;
}

.card-content h3 {
    font-size: 1.4rem;
    margin-bottom: 10px;
    color: var(--color-primary);
}

.card-content p {
    font-size: 0.95rem;
    color: var(--color-text-muted);
    margin-bottom: 15px;
}

.tag-list {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
}

.tag-list li {
    font-size: 0.8rem;
    background-color: var(--color-bg);
    padding: 4px 10px;
    border-radius: 4px;
    color: var(--color-secondary);
}

/* ==========================================================================
   7. Pure CSS Fragrance Quiz Section
   ========================================================================== */
/* STREAMING_CHUNK:Implementing pure CSS quiz tab logic and styling... */
.quiz-section {
    background-color: var(--color-accent-light);
}

.quiz-wrapper {
    background: var(--color-surface);
    padding: 40px;
    border-radius: var(--radius-lg);
    border: 1px solid var(--color-border);
    box-shadow: var(--shadow-subtle);
}

/* 隱藏 Radio 狀態控制按鈕 */
.quiz-container > input[type="radio"] {
    display: none;
}

.quiz-steps-nav {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-bottom: 30px;
    border-bottom: 1px solid var(--color-border);
    padding-bottom: 15px;
}

.step-label {
    padding: 8px 16px;
    font-size: 0.9rem;
    color: var(--color-text-muted);
    cursor: pointer;
    border-radius: 20px;
    transition: var(--transition-smooth);
}

/* 根據不同的 checked 項目動態切換步驟頁面 (Pure CSS) */
#step1:checked ~ .quiz-steps-nav .step1-label,
#step2:checked ~ .quiz-steps-nav .step2-label,
#step3:checked ~ .quiz-steps-nav .step3-label {
    background-color: var(--color-primary);
    color: var(--color-white);
}

.quiz-content {
    display: none;
    animation: fadeIn 0.4s ease;
}

#step1:checked ~ .step1-content,
#step2:checked ~ .step2-content,
#step3:checked ~ .step3-content {
    display: block;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}

.options-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin: 25px 0;
}

.option-card {
    border: 1px solid var(--color-border);
    padding: 20px;
    border-radius: var(--radius-md);
    cursor: pointer;
    transition: var(--transition-smooth);
    display: flex;
    flex-direction: column;
}

.option-card:hover {
    border-color: var(--color-accent);
    background-color: var(--color-bg);
}

.option-card input {
    margin-bottom: 10px;
}

.option-title {
    font-weight: 600;
    margin-bottom: 5px;
    color: var(--color-primary);
}

.option-desc {
    font-size: 0.85rem;
    color: var(--color-text-muted);
}

.quiz-next {
    margin-top: 25px;
    text-align: right;
}

.flex-between {
    display: flex;
    justify-content: space-between;
}

.result-box {
    padding: 20px 0;
}

.result-img {
    width: 180px;
    height: 180px;
    object-fit: cover;
    margin: 20px auto;
    border-radius: 50%;
    border: 3px solid var(--color-accent);
}

.result-actions {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 20px;
}

/* ==========================================================================
   8. Perfumes Showcase Cards Section
   ========================================================================== */
/* STREAMING_CHUNK:Styling perfume showcase cards and performance progress bars... */
.perfumes-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 30px;
}

.perfume-card {
    background-color: var(--color-surface);
    border-radius: var(--radius-md);
    border: 1px solid var(--color-border);
    overflow: hidden;
    position: relative;
    display: flex;
    flex-direction: column;
    box-shadow: var(--shadow-subtle);
    transition: var(--transition-smooth);
}

.perfume-card:hover {
    box-shadow: var(--shadow-hover);
}

.perfume-badge-group {
    position: absolute;
    top: 15px;
    left: 15px;
    z-index: 5;
}

.perfume-img-container {
    height: 300px;
    background-color: var(--color-bg);
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
}

.perfume-img-container img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: var(--transition-smooth);
}

.perfume-card:hover .perfume-img-container img {
    transform: scale(1.03);
}

.perfume-details {
    padding: 25px;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
}

.perfume-brand {
    font-size: 0.75rem;
    letter-spacing: 2px;
    color: var(--color-secondary);
}

.perfume-title {
    font-size: 1.5rem;
    color: var(--color-primary);
    margin: 4px 0;
}

.perfume-type {
    font-size: 0.85rem;
    color: var(--color-text-muted);
    margin-bottom: 15px;
}

/* 前中後調金字塔 */
.notes-pyramid {
    background-color: var(--color-bg);
    padding: 12px 15px;
    border-radius: var(--radius-sm);
    font-size: 0.82rem;
    margin-bottom: 20px;
}

.note-item {
    margin-bottom: 4px;
    color: var(--color-text-dark);
}

.note-item:last-child {
    margin-bottom: 0;
}

/* 持香與擴香進度條指標 */
.performance-metrics {
    margin-bottom: 20px;
}

.metric-row {
    margin-bottom: 10px;
}

.metric-name {
    font-size: 0.8rem;
    color: var(--color-text-muted);
    display: block;
    margin-bottom: 3px;
}

.progress-bar {
    height: 6px;
    background-color: var(--color-border);
    border-radius: 3px;
    overflow: hidden;
    margin-bottom: 3px;
}

.progress-fill {
    height: 100%;
    background-color: var(--color-accent);
    border-radius: 3px;
}

.metric-value {
    font-size: 0.75rem;
    color: var(--color-primary);
    font-weight: 600;
}

.perfume-footer {
    margin-top: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 15px;
    border-top: 1px solid var(--color-border);
}

.price {
    font-size: 1.25rem;
    font-weight: 600;
    color: var(--color-primary);
    font-family: var(--font-serif);
}

/* ==========================================================================
   9. Discovery Set Section
   ========================================================================== */
/* STREAMING_CHUNK:Styling discovery trial set promo box... */
.discovery-section {
    background-color: var(--color-accent-light);
}

.discovery-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 50px;
    align-items: center;
}

.discovery-img-wrapper {
    border-radius: var(--radius-lg);
    overflow: hidden;
    box-shadow: var(--shadow-hover);
}

.discovery-content h2 {
    font-size: 2.2rem;
    margin: 10px 0 15px;
}

.benefit-list {
    margin: 25px 0;
}

.benefit-list li {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    margin-bottom: 12px;
    font-size: 0.95rem;
}

.benefit-icon {
    color: var(--color-accent);
    font-weight: bold;
}

.discovery-price-box {
    display: flex;
    align-items: center;
    gap: 15px;
    margin-bottom: 25px;
}

.old-price {
    text-decoration: line-through;
    color: var(--color-text-muted);
}

.new-price {
    font-size: 2rem;
    font-weight: 600;
    color: var(--color-primary);
    font-family: var(--font-serif);
}

.tag-free-ship {
    background-color: var(--color-primary);
    color: var(--color-white);
    font-size: 0.75rem;
    padding: 3px 8px;
    border-radius: 4px;
}

/* ==========================================================================
   10. Brand Philosophy & Footer
   ========================================================================== */
/* STREAMING_CHUNK:Styling brand story and responsive footer... */
.about-section {
    background-color: var(--color-surface);
}

.footer {
    background-color: var(--color-primary);
    color: var(--color-white);
    padding: 60px 0 20px;
}

.footer-grid {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr 2fr;
    gap: 40px;
    margin-bottom: 40px;
}

.footer .logo {
    color: var(--color-white);
}

.footer-brand p {
    font-size: 0.85rem;
    color: var(--color-secondary);
    margin-top: 15px;
}

.footer-links h4, .footer-newsletter h4 {
    font-size: 1rem;
    margin-bottom: 15px;
    color: var(--color-accent-light);
}

.footer-links ul li {
    margin-bottom: 8px;
}

.footer-links a {
    color: var(--color-secondary);
    font-size: 0.85rem;
}

.footer-links a:hover {
    color: var(--color-white);
}

.footer-newsletter p {
    font-size: 0.85rem;
    color: var(--color-secondary);
    margin-bottom: 15px;
}

.newsletter-form {
    display: flex;
    gap: 10px;
}

.newsletter-form input {
    padding: 10px;
    border-radius: var(--radius-sm);
    border: 1px solid #444;
    background-color: #383533;
    color: var(--color-white);
    flex-grow: 1;
    font-size: 0.85rem;
}

.footer-bottom {
    border-top: 1px solid #383533;
    padding-top: 20px;
    font-size: 0.8rem;
    color: var(--color-secondary);
}

/* ==========================================================================
   11. Media Queries (Mobile & Tablet Responsiveness)
   ========================================================================== */
/* STREAMING_CHUNK:Adding media queries for tablet and mobile devices... */
@media (max-width: 992px) {
    .hero-title {
        font-size: 2.8rem;
    }

    .discovery-grid {
        grid-template-columns: 1fr;
    }

    .footer-grid {
        grid-template-columns: 1fr 1fr;
    }
}

@media (max-width: 768px) {
    .hamburger {
        display: flex;
    }

    .nav-links {
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background-color: var(--color-surface);
        flex-direction: column;
        padding: 20px;
        gap: 15px;
        border-bottom: 1px solid var(--color-border);
        display: none;
    }

    /* 漢堡開關 (純 CSS) */
    .menu-toggle:checked ~ .nav-links {
        display: flex;
    }

    .hero {
        height: auto;
        padding: 80px 0;
    }

    .hero-title {
        font-size: 2.2rem;
    }

    .hero-actions {
        flex-direction: column;
    }

    .quiz-steps-nav {
        flex-direction: column;
        align-items: center;
    }

    .footer-grid {
        grid-template-columns: 1fr;
    }
}