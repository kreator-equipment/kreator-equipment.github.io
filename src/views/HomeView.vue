<template>
  <div class="kreator-landing">
    <!-- 1. HEADER NAVIGATION -->
    <header class="navbar">
      <div class="nav-brand">
        <img src="/kreator-logo.webp" alt="Kreator Logo" class="logo-k" />
      </div>
      <nav class="nav-links">
        <a href="#solutions">Solutions</a>
        <a href="#industries">Industries</a>
        <a href="#projects">Projects</a>
        <a href="#aftermarket">Aftermarket</a>
        <a href="#company">Company</a>
      </nav>
      <a href="#contact" class="btn-contact">Contact Us</a>
    </header>

    <!-- 2. HERO SECTION WITH SPECIFICATION OVERLAY -->
    <section id="hero" class="hero-section">
      <div class="hero-bg-overlay">
      <div class="hero-grid">
        <div class="hero-text">
          <h1>ENGINEERED<br />TO MOVE<br /><span class="accent-orange">INDUSTRY</span></h1>
          <p class="hero-subtitle">
            Custom conveyor systems and structures built for performance. Delivered turnkey.
          </p>
          <div class="hero-cta-group">
            <a href="#solutions" class="btn-orange">Explore Solutions</a>
            <a
              href="https://kreator-equipment.github.io/showroom"
              target="_blank"
              class="btn-outline-text"
              >View Our 3D Showroom</a
            >
          </div>
          <div class="scroll-indicator"><span class="arrow-down">↓</span> Scroll to Discover</div>
        </div>
        

        <!-- Interactive System Preview Card right of Hero image -->
        <div class="system-preview-card">
          <div class="card-header">
            <span class="spec-label">SYSTEM PREVIEW</span>
            <h3>{{ systemPreview[0].title }}</h3>
          </div>
          <div class="spec-table">
            <div class="spec-row">
              <span>{{ systemPreview[1].label }}</span><span class="spec-val">{{ systemPreview[1].value }}</span>
            </div>
            <div class="spec-row"><span>{{ systemPreview[2].label }}</span><span class="spec-val">{{ systemPreview[2].value }}</span></div>
            <div class="spec-row">
              <span>{{ systemPreview[3].label }}</span><span class="spec-val">{{ systemPreview[3].value }}</span>
            </div>
            <div class="spec-row"><span>{{ systemPreview[4].label }}</span><span class="spec-val">{{ systemPreview[4].value }}</span></div>
          </div>
          <a href="#projects" class="view-system-link">
            View Full System <span class="arrow">→</span>
          </a>
        </div>
      </div>
      </div>
      <!-- Industrial Sub-Hero Trust Badges -->
      <div class="trust-ribbon">
        <div class="ribbon-item"> Engineered for Performance</div>
        <div class="ribbon-item"> Built to Last</div>
        <div class="ribbon-item"> Installed with Precision</div>
        <div class="ribbon-item"> Supported for the Long Run</div>
      </div>
    </section>

<!-- 3. SOLUTIONS SECTION -->
    <section id="solutions" class="solutions-section">
      <div class="section-intro">
        <div class="intro-left-group">
          <h2>
            Complete Solutions.<br />Built Around <span class="accent-orange">Your Operation.</span>
          </h2>
          <p>
            We provide turnkey solutions to design, build, deliver, and install projects of any size. Backed by a dedicated team of designers, fabricators, transportation specialists, and field experts, we handle the heavy lifting so you don't have to.
          </p>
        </div>
        <div class="intro-right">
          <a href="#solutions" class="outline-action-btn">View All Solutions →</a>
        </div>
      </div>

      <div class="solutions-grid">
        <div class="solution-card" v-for="(sol, i) in solutions" :key="i">
          <div class="sol-icon">{{ sol.icon }}</div>
          <h3>{{ sol.title }}</h3>
          <p>{{ sol.desc }}</p>
        </div>
      </div>

      <!-- Stat Counters Grid Row -->
      <div class="metrics-row">
        <div class="metric-box" v-for="(stat, i) in stats" :key="i">
          <div class="metric-num">{{ stat.value }}</div>
          <div class="metric-label">{{ stat.label }}</div>
        </div>
      </div>
    </section>

    <!-- 4. INDUSTRIES SECTION -->
    <section id="industries" class="industries-section">
      <div class="section-intro">
        <h2>
          Built for the Industries<br />That Keep
          <span class="accent-orange">The World Moving.</span>
        </h2>
        <a href="#industries" class="outline-action-btn">View All Industries →</a>
      </div>

      <div class="industries-gallery">
        <div class="industry-thumb" v-for="(ind, i) in industries" :key="i">
          <div class="image-placeholder-box">
            <span class="play-overlay">👁</span>
          </div>
          <h4>{{ ind }}</h4>
        </div>
      </div>
    </section>

    <!-- 5. FEATURED CASE STUDY LAYER -->
    <section id="projects" class="case-study-section">
      <span class="section-tag">FEATURED PROJECT</span>
      <div class="case-study-grid">
        <div class="case-study-left">
          <h2>
            Complete Conveying System for a Leading
            <span class="accent-orange">Aggregate Producer</span>
          </h2>
          <p>
            A fully integrated solution including overland conveyors, stackers, and loadout systems
            designed for high capacity and maximum uptime.
          </p>
          <a href="#projects" class="outline-action-btn inline-btn">View Case Study →</a>
        </div>

        <div class="case-study-media">
          <div class="video-mock-container">
          </div>
          <div class="case-study-specs">
            <div class="spec-row">
              <span>Location</span><span class="spec-val">North America</span>
            </div>
            <div class="spec-row">
              <span>System Type</span><span class="spec-val">Overland Conveyor</span>
            </div>
            <div class="spec-row"><span>Length</span><span class="spec-val">1.2 km</span></div>
            <div class="spec-row"><span>Capacity</span><span class="spec-val">4,000 TPH</span></div>
          </div>
        </div>
      </div>
    </section>

    <!-- 6. ENTERPRISE TRUST LOGO BANNER -->
    <div class="logo-marquee-section">
      <p class="marquee-title">TRUSTED BY INDUSTRY LEADERS</p>
      <div class="logo-flex">
        <span>CATERPILLAR</span>
        <span>HOLCIM</span>
        <span>BHP</span>
        <span>ArcelorMittal</span>
        <span>thyssenkrupp</span>
        <span>pwc</span>
      </div>
    </div>

    <!-- 7. CLOSING CALL TO ACTION & CONTACT DETAILS -->
    <section id="contact" class="cta-contact-section">
      <div class="cta-grid">
        <div class="cta-left">
          <h2>Ready to Move Your<br />Operation <span class="accent-orange">Forward?</span></h2>
          <p>Let's build a solution that drives performance, efficiency, and long-term value.</p>
          <div class="cta-btn-row">
            <a href="mailto:info@kreator.com" class="btn-orange">Talk to an Expert</a>
            <button class="btn-outline-text">Request a Quote</button>
          </div>
        </div>

        <div class="contact-details-box">
          <div class="detail-item">
            <span class="detail-icon">📞</span>
            <div>
              <p class="label">PHONE</p>
              <p class="val">+1 (855) 573-2867</p>
            </div>
          </div>
          <div class="detail-item">
            <span class="detail-icon">✉</span>
            <div>
              <p class="label">EMAIL</p>
              <p class="val">info@kreator.com</p>
            </div>
          </div>
          <div class="detail-item">
            <span class="detail-icon">📍</span>
            <div>
              <p class="label">LOCATION</p>
              <p class="val">Ontario, Canada</p>
            </div>
          </div>
          <div class="detail-item">
            <span class="detail-icon">🌐</span>
            <div>
              <p class="label">GLOBAL SERVICE</p>
              <p class="val">24/7 Support</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 8. CORPORATE INDUSTRIAL FOOTER -->
    <footer ref="footerTarget" class="footer">
      <div class="footer-top">
        <div class="footer-brand-col">
          <img src="/kreator-logo.webp" alt="Kreator Logo" class="logo-k" />
        </div>
        <div class="footer-links-column">
          <h4>Solutions</h4>
          <a href="#">Conveyor Systems</a>
          <a href="#">Structures & Platforms</a>
          <a href="#">Logistics Solutions</a>
        </div>
        <div class="footer-links-column">
          <h4>Industries</h4>
          <a href="#">Aggregates</a>
          <a href="#">Industrial</a>
          <a href="#">Recycling</a>
        </div>
        <div class="footer-links-column">
          <h4>Company</h4>
          <a href="#">About Us</a>
          <a href="#">Our Team</a>
          <a href="#">Careers</a>
        </div>
        <div class="footer-links-column">
          <h4>Support</h4>
          <a href="#">Parts & Services</a>
          <a href="#">Request a Quote</a>
          <a href="#">Contact Us</a>
        </div>
      </div>
      <div class="footer-bottom">
        <p>© 2026 Kreator. All rights reserved.</p>
        <div class="footer-legal">
          <a href="#">Privacy Policy</a>
          <a href="#">Terms of Use</a>
        </div>
      </div>
      <!-- <div class="footer-agency-credit">
        <span class="agency-credit">Built by <a href="https://danielkaufman.dev" target="_blank">DKD Media</a></span>
      </div> -->
    </footer>
    <CreditBadge />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import CreditBadge from '../components/CreditBadge.vue'

const systemPreview = ref([
  {
    title: 'Mining Conveyor System',
  },
  {
    label: 'System Type',
    value: 'Belt Conveyor',
  },
  {
    label: 'Lift Height',
    value: '18 m',
  },
  {
    label: 'Capacity',
    value: '3500 TPH',
  },
  {
    label: 'Speed',
    value: '1.2 m/s',
  },
])

const solutions = ref([
  {
    icon: '🏭',
    title: 'Conveyor Systems',
    desc: 'Custom engineered conveyor solutions for every application.',
  },
  {
    icon: '🏗️',
    title: 'Structures & Platforms',
    desc: 'Engineered support structures built to industry standards.',
  },
  {
    icon: '📦',
    title: 'Logistics Solutions',
    desc: 'Intelligent material handling and warehouse systems.',
  },
  {
    icon: '🔧',
    title: 'Installation Services',
    desc: 'Safe, efficient installation by experienced crews.',
  },
  {
    icon: '🎧',
    title: 'Aftermarket Support',
    desc: 'Parts, service and upgrades to maximize uptime.',
  },
])

const stats = ref([
  { value: '15+', label: 'Years of Experience' },
  { value: '2,000+', label: 'Systems Delivered' },
  { value: '99.9%', label: 'On-Time Delivery' },
  { value: '99%', label: 'Customer Satisfaction' },
])

const industries = ref([
  'Aggregates & Mining',
  'Industrial Manufacturing',
  'Recycling & Waste Management',
  'Industry Title 4',
  'Industry Title 5',
  'Industry Title 6',
])
</script>

<style scoped>
/* Mockup Styling Sync */
.kreator-landing {
  --bg-main: #0b0c0e;
  --bg-card: #13161a;
  --orange: #e65c00;
  --text-main: #ffffff;
  --text-muted: #8a929b;
  --border-color: rgba(255, 255, 255, 0.06);

  background-color: var(--bg-main);
  color: var(--text-main);
  font-family: 'Inter', sans-serif;
  min-height: 100vh;
  scroll-behavior: smooth;
}

/* 1. Header Styles */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem 4rem;
  background-color: rgba(11, 12, 14, 0.9);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--border-color);
  position: sticky;
  top: 0;
  z-index: 100;
}

.logo-k {
  padding: 0.2rem 0.6rem;
  border-radius: 3px;
  font-weight: 900;
  scale: 0.75;
  width: fit-content;
  height: fit-content;
}

.nav-links a {
  color: var(--text-muted);
  text-decoration: none;
  margin-right: 2rem;
  font-size: 0.9rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  transition: color 0.2s;
}

.nav-links a:hover {
  color: var(--text-main);
}

.btn-contact,
.btn-orange {
  background-color: var(--orange);
  color: white;
  padding: 0.75rem 1.5rem;
  text-decoration: none;
  font-weight: 700;
  border-radius: 4px;
  text-transform: uppercase;
  font-size: 0.85rem;
  transition: opacity 0.2s;
}
.btn-contact:hover,
.btn-orange:hover {
  opacity: 0.9;
}

/* 2. Hero Component Styles */
.hero-section {
  padding: 4rem;
  border-bottom: 1px solid var(--border-color);
  background-image: radial-gradient(circle at 60% 30%, rgba(230, 92, 0, 0.08), transparent 50%);
}
.hero-bg-overlay {
  background-image: url('/hero-bg.webp');
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
  width: 100%;
  height: 100%;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 4rem;
  align-items: center;
  min-height: 70vh;
}

h1 {
  font-size: 4.5rem;
  font-weight: 900;
  line-height: 1.05;
  letter-spacing: -2px;
  margin: 0 0 1.5rem 0;
}

.accent-orange {
  color: var(--orange);
}

.hero-subtitle {
  font-size: 1.25rem;
  color: var(--text-muted);
  max-width: 500px;
  margin-bottom: 2.5rem;
}

.hero-cta-group {
  display: flex;
  gap: 1.5rem;
  align-items: center;
  margin-bottom: 4rem;
}

.btn-video {
  background: none;
  border: none;
  color: var(--text-main);
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.play-icon {
  border: 1px solid var(--text-muted);
  padding: 0.4rem 0.6rem;
  border-radius: 50%;
  font-size: 0.75rem;
}

.scroll-indicator {
  color: var(--text-muted);
  font-size: 0.85rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

/* System Specifications Overlay Box */
.system-preview-card {
  align-self: end;
  background-color: var(--bg-card);
  border: 1px solid var(--border-color);
  padding: 2rem;
  border-radius: 6px;
}

.spec-label {
  color: var(--text-muted);
  font-size: 0.75rem;
  font-family: monospace;
}

.system-preview-card h3 {
  margin: 0.25rem 0 1.5rem 0;
  font-size: 1.25rem;
}

.spec-table {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.spec-row {
  display: flex;
  justify-content: space-between;
  font-size: 0.9rem;
  color: var(--text-muted);
  border-bottom: 1px solid rgba(255, 255, 255, 0.03);
  padding-bottom: 0.5rem;
}

.spec-val {
  color: var(--text-main);
  font-weight: 600;
}

.view-system-link {
  color: var(--orange);
  text-decoration: none;
  font-size: 0.9rem;
  font-weight: 700;
}

.trust-ribbon {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  border-top: 1px solid var(--border-color);
  padding-top: 2.5rem;
  margin-top: 2rem;
}

.ribbon-item {
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--text-muted);
  text-align: center;
}
/* 3. Solutions Section Styles */
 .industries-section {
  padding: 6rem 4rem;
}
.solutions-section,
.case-study-section {
  padding: 6rem 4rem;
  border-bottom: 1px solid var(--border-color);
}
.section-intro {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 4rem;
}

.section-intro h2 {
  font-size: 2.5rem;
  font-weight: 800;
  line-height: 1.1;
  margin: 0;
}

.intro-left {
  max-width: 450px;
}
.intro-left-group h2 {
  margin-bottom: 0.5rem;
}
.intro-left-group p {
  color: var(--text-muted);
  line-height: 1.5;
  max-width: 70%;
  margin: 0;
}
.intro-right {
  align-items: center;
}
.outline-action-btn {
  border: 1px solid var(--border-color);
  color: var(--text-main);
  padding: 0.75rem 1.5rem;
  border-radius: 4px;
  text-decoration: none;
  font-size: 0.85rem;
  font-weight: 600;
  text-wrap: nowrap;
}
.outline-action-btn:hover {
  border-color: var(--orange);
}
.solutions-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 1.5rem;
  margin-bottom: 6rem;
}
.solution-card {
  background-color: var(--bg-card);
  border: 1px solid var(--border-color);
  padding: 2rem 1.5rem;
  border-radius: 4px;
}
.sol-icon {
  font-size: 1.75rem;
  margin-bottom: 1.5rem;
}
.solution-card h3 {
  font-size: 1.1rem;
  margin: 0 0 0.75rem 0;
}
.solution-card p {
  color: var(--text-muted);
  font-size: 0.85rem;
  line-height: 1.5;
  margin: 0;
}
.metrics-row {
  display: grid;
  justify-items: center;
  grid-template-columns: repeat(4, 1fr);
  border-top: 1px solid var(--border-color);
  padding-top: 4rem;
}

.metric-num {
  font-size: 3.5rem;
  font-weight: 900;
  color: var(--orange);
  line-height: 1;
  text-align: center;
}
.metric-label {
  color: var(--text-muted);
  font-size: 0.85rem;
  margin-top: 0.5rem;
  text-transform: uppercase;
  text-align: center;
}

/* 4. Industries Section Styles */
.industries-gallery {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 1rem;
}

.industry-thumb h4 {
  font-size: 0.95rem;
  margin: 0.75rem 0 0 0;
  font-weight: 600;
}

.image-placeholder-box {
  background-color: #1a1d23;
  height: 180px;
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.play-overlay {
  opacity: 0;
  transition: opacity 0.2s;
  color: var(--orange);
  font-size: 1.5rem;
}
.image-placeholder-box:hover .play-overlay {
  opacity: 1;
}

/* 5. Case Study Component Layout */
.section-tag {
  color: var(--orange);
  font-family: monospace;
  font-size: 0.8rem;
  font-weight: 700;
}

.case-study-grid {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  gap: 4rem;
  margin-top: 1rem;
}

.case-study-left h2 {
  font-size: 2.5rem;
  font-weight: 800;
  margin: 0 0 1.5rem 0;
}
.case-study-left p {
  color: var(--text-muted);
  line-height: 1.6;
  margin-bottom: 2.5rem;
}
.inline-btn {
  display: inline-block;
}

.video-mock-container {
  background-color: #1f232b;
  height: 26rem;
  border-radius: 4px;
  margin-bottom: 1.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* 6. Logo Marquee Block */
.logo-marquee-section {
  padding: 4rem;
  border-bottom: 1px solid var(--border-color);
  text-align: center;
}

.marquee-title {
  font-size: 0.8rem;
  color: var(--text-muted);
  font-weight: 700;
  letter-spacing: 2px;
  margin-bottom: 2rem;
}

.logo-flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
  opacity: 0.4;
  font-weight: 800;
  font-size: 1.25rem;
}

/* 7. Call To Action Form Section */
.cta-contact-section {
  padding: 6rem 4rem;
  background-color: #0e1013;
}
.cta-grid {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 4rem;
}
.cta-left h2 {
  font-size: 3rem;
  font-weight: 900;
  margin: 0 0 1rem 0;
}
.cta-left p {
  color: var(--text-muted);
  margin-bottom: 3rem;
}
.cta-btn-row {
  display: flex;
  gap: 1.5rem;
}

.btn-outline-text {
  background: none;
  border: 1px solid var(--border-color);
  color: white;
  padding: 0.75rem 1.5rem;
  border-radius: 4px;
  cursor: pointer;
  text-decoration: none;
}

.contact-details-box {
  background-color: var(--bg-card);
  padding: 2.5rem;
  border-radius: 6px;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.detail-item {
  display: flex;
  gap: 1rem;
  align-items: center;
}
.detail-icon {
  font-size: 1.5rem;
  color: var(--orange);
}
.detail-item .label {
  font-size: 0.7rem;
  color: var(--text-muted);
  margin: 0;
  font-family: monospace;
}
.detail-item .val {
  font-size: 1rem;
  font-weight: 600;
  margin: 0;
}

/* 8. Corporate Footer Structure */
.footer {
  padding: 6rem 4rem 2rem 4rem;
  background-color: var(--bg-main);
  border-top: 1px solid var(--border-color);
}
.footer-top {
  display: grid;
  grid-template-columns: 1.5fr repeat(4, 1fr);
  gap: 2rem;
  margin-bottom: 4rem;
}
.footer-brand-col {
  margin: auto;
}
.footer-links-column h4 {
  font-size: 0.95rem;
  margin-bottom: 1.5rem;
}
.footer-links-column a {
  display: block;
  color: var(--text-muted);
  text-decoration: none;
  margin-bottom: 0.75rem;
  font-size: 0.9rem;
}
.footer-links-column a:hover {
  color: var(--text-main);
}

.footer-bottom {
  display: flex;
  justify-content: space-between;
  border-top: 1px solid rgba(255, 255, 255, 0.02);
  padding-top: 2rem;
  color: rgba(255, 255, 255, 0.2);
  font-size: 0.85rem;
}
.footer-legal a {
  color: rgba(255, 255, 255, 0.2);
  text-decoration: none;
  margin-left: 1.5rem;
  margin-bottom: 1.5rem;
}
.footer-agency-credit {
  display: flex;
  justify-content: flex-end;
  margin: 0.5rem;
}
.agency-credit {
  color: rgba(255, 255, 255, 0.2);
  font-size: 0.85rem;
  margin-right: 1.5rem;
}
.agency-credit a {
  color: rgba(255, 255, 255, 0.4);
  text-decoration: none;
  transition: color 0.2s ease;
}
.agency-credit a:hover {
  color: var(--orange);
}

/* Fully Scalable Breakpoint Fallbacks */
@media (max-width: 1200px) {
  .solutions-grid {
    grid-template-columns: repeat(3, 1fr);
  }
  .industries-gallery {
    grid-template-columns: repeat(3, 1fr);
  }
}
@media (max-width: 768px) {
  .hero-grid,
  .cta-grid,
  .case-study-grid,
  .footer-top {
    grid-template-columns: 1fr;
    gap: 2.5rem;
  }
  .navbar {
    padding: 1.5rem 2rem;
  }
  .hero-section,
  .solutions-section,
  .industries-section,
  .case-study-section,
  .cta-contact-section {
    padding: 4rem 2rem;
  }
  h1 {
    font-size: 3rem;
  }
  .solutions-grid,
  .industries-gallery,
  .trust-ribbon,
  .metrics-row {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}
</style>
