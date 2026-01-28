<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MarketRoAlpha – Growth that Performs</title>

<style>
:root {
  --primary:#6366f1;
  --dark:#0f172a;
  --light:#f8fafc;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Inter, system-ui, sans-serif;
}

body {
  background: var(--light);
  color: var(--dark);
  line-height: 1.6;
}

section {
  padding: 90px 8%;
}

h1, h2 {
  font-weight: 800;
}

h2 {
  text-align: center;
  margin-bottom: 60px;
  font-size: 2.4rem;
}

/* ================= HERO ================= */
.hero {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  align-items: center;
  gap: 60px;
  position: relative;
  overflow: hidden;
}

.hero::before,
.hero::after {
  content: "";
  position: absolute;
  width: 420px;
  height: 420px;
  background: radial-gradient(circle, #c7d2fe, transparent 70%);
}

.hero::before { top: -120px; left: -120px; }
.hero::after { bottom: -140px; right: -140px; }

.hero-content {
  max-width: 720px;
  position: relative;
}

.hero small {
  color: var(--primary);
  font-weight: 700;
  letter-spacing: 1px;
}

.hero h1 {
  font-size: 3.8rem;
  margin: 12px 0;
}

.hero p {
  font-size: 1.25rem;
  margin-bottom: 24px;
  color: #334155;
}

.hero ul {
  list-style: none;
  margin-bottom: 36px;
}

.hero ul li {
  margin-bottom: 10px;
  font-weight: 600;
}

.hero ul li::before {
  content: "✓ ";
  color: var(--primary);
}

/* BUTTON */
.btn {
  padding: 16px 36px;
  background: linear-gradient(135deg, var(--primary), #4338ca);
  color: white;
  border-radius: 14px;
  font-weight: 700;
  border: none;
  cursor: pointer;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 20px 40px rgba(99,102,241,0.35);
}

/* HERO VISUALS */
.hero-visual {
  position: relative;
  height: 520px;
}

.kpi-card {
  position: absolute;
  background: white;
  padding: 22px 26px;
  border-radius: 18px;
  box-shadow: 0 25px 60px rgba(0,0,0,0.1);
  animation: float 6s ease-in-out infinite;
}

.kpi-card h3 {
  color: var(--primary);
  font-size: 1.6rem;
}

.kpi-card p {
  font-weight: 600;
  color: #475569;
}

.kpi-1 { top: 40px; left: 40px; }
.kpi-2 { top: 180px; right: 20px; animation-delay: 1s; }
.kpi-3 { bottom: 60px; left: 120px; animation-delay: 2s; }

.chart {
  position: absolute;
  bottom: 40px;
  right: 80px;
  width: 200px;
  height: 140px;
  display: flex;
  align-items: flex-end;
  gap: 14px;
}

.bar {
  width: 24px;
  border-radius: 8px;
  background: linear-gradient(180deg, var(--primary), #4338ca);
}

.bar:nth-child(1){ height: 40%; }
.bar:nth-child(2){ height: 65%; }
.bar:nth-child(3){ height: 90%; }
.bar:nth-child(4){ height: 70%; }

@keyframes float {
  0%,100% { transform: translateY(0); }
  50% { transform: translateY(-14px); }
}

/* ================= STATS ================= */
.stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px,1fr));
  gap: 24px;
  margin-top: 50px;
}

.stat {
  background: white;
  padding: 26px;
  border-radius: 18px;
  text-align: center;
  box-shadow: 0 16px 40px rgba(0,0,0,0.06);
}

.stat h3 {
  font-size: 2rem;
  color: var(--primary);
}

.stat p {
  font-weight: 600;
  color: #475569;
}

/* ================= GRID ================= */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 34px;
}

.card {
  background: white;
  border-radius: 22px;
  padding: 40px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.07);
}

.card h3 {
  margin-bottom: 12px;
  color: var(--primary);
}

/* ================= WHY ================= */
.why {
  background: linear-gradient(135deg, #eef2ff, #f0fdf4);
}

/* ================= FORM ================= */
form {
  max-width: 640px;
  margin: auto;
  background: white;
  padding: 44px;
  border-radius: 22px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.08);
}

input, select {
  width: 100%;
  padding: 14px;
  margin-bottom: 16px;
  border-radius: 10px;
  border: 1px solid #cbd5f5;
}

#successInline {
  display: none;
  text-align: center;
  color: #047857;
  font-weight: 600;
  margin-top: 20px;
}

/* ================= MODAL ================= */
.modal {
  position: fixed;
  inset: 0;
  background: rgba(15,23,42,0.7);
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  visibility: hidden;
  z-index: 9999;
}

.modal.active {
  opacity: 1;
  visibility: visible;
}

.modal-box {
  background: white;
  padding: 42px;
  border-radius: 20px;
  text-align: center;
  max-width: 420px;
}

/* ================= FOOTER ================= */
footer {
  background: var(--dark);
  color: white;
  text-align: center;
  padding: 30px;
}

/* MOBILE */
@media(max-width:900px){
  .hero {
    grid-template-columns: 1fr;
    text-align: center;
  }
  .hero-visual {
    display: none;
  }
}
</style>
</head>

<body>

<!-- HERO -->
<section class="hero">
  <div class="hero-content">
    <small>🚀 Performance-Driven Growth for Ambitious Brands</small>
    <h1>MarketRoAlpha</h1>
    <p><strong>Growth that Performs.</strong><br>
    We build predictable, scalable and profitable marketing systems — not random campaigns.</p>

    <ul>
      <li>ROI-focused paid acquisition</li>
      <li>Funnels & automation that convert</li>
      <li>Decisions powered by clean data</li>
    </ul>

    <a href="#contact" class="btn">Book Your Personalised Consultation</a>

    <div class="stats">
      <div class="stat"><h3>50+</h3><p>Funnels Built</p></div>
      <div class="stat"><h3>₹10Cr+</h3><p>Revenue Influenced</p></div>
      <div class="stat"><h3>7+</h3><p>Industries Scaled</p></div>
    </div>
  </div>

  <div class="hero-visual">
    <div class="kpi-card kpi-1"><h3>4.2x</h3><p>ROAS</p></div>
    <div class="kpi-card kpi-2"><h3>-38%</h3><p>CAC Reduced</p></div>
    <div class="kpi-card kpi-3"><h3>₹1.6Cr</h3><p>Monthly Revenue</p></div>

    <div class="chart">
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section>
  <h2>Our Marketing Services</h2>
  <div class="grid">
    <div class="card"><h3>Performance Marketing</h3>ROI-focused paid media across Google, Meta & more.</div>
    <div class="card"><h3>Conversion Rate Optimization</h3>Funnels & landing pages that convert clicks into revenue.</div>
    <div class="card"><h3>Growth Funnels</h3>End-to-end acquisition, activation & retention journeys.</div>
    <div class="card"><h3>CRM & Automation</h3>Lifecycle automation to improve LTV & retention.</div>
    <div class="card"><h3>Analytics & Attribution</h3>UTM frameworks & decision-ready dashboards.</div>
    <div class="card"><h3>Growth Consulting</h3>Founder-level strategic guidance for scale.</div>
  </div>
</section>

<!-- WHY US -->
<section class="why">
  <h2>Why Choose MarketRoAlpha</h2>
  <div class="grid">
    <div class="card"><h3>Revenue First</h3>We optimize for profit, not vanity metrics.</div>
    <div class="card"><h3>Data-Led Execution</h3>Every move backed by insights.</div>
    <div class="card"><h3>Fast Iteration</h3>Test, learn and scale quickly.</div>
    <div class="card"><h3>Full Transparency</h3>No black boxes. Ever.</div>
    <div class="card"><h3>Founder Mindset</h3>We think like owners.</div>
    <div class="card"><h3>Scalable Systems</h3>Built to grow with you.</div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <h2>Book Your Personalised Consultation</h2>

  <form id="leadForm">
    <input name="company" placeholder="Company Name" required>
    <input name="mobile" placeholder="Mobile Number" required>
    <input name="email" placeholder="Email Address" required>

    <select name="service" required>
      <option value="">Select Service</option>
      <option>Performance Marketing</option>
      <option>Funnels & CRO</option>
      <option>CRM & Automation</option>
      <option>Analytics & Attribution</option>
      <option>Growth Consulting</option>
    </select>

    <input type="hidden" name="utm_source">
    <input type="hidden" name="utm_medium">
    <input type="hidden" name="utm_campaign">

    <button class="btn" type="submit">Submit</button>
    <p id="successInline">✅ Form has been submitted successfully. Our team will contact you shortly.</p>
  </form>
</section>

<footer>
  <p>📞 +91 9729242050 | ✉️ vbhardwaj@marketroalpha.com</p>
</footer>

<div class="modal" id="successModal">
  <div class="modal-box">
    <h3>🎉 Thank You!</h3>
    <p>Form has been submitted successfully.<br>Our team will contact you shortly.</p>
    <br>
    <button class="btn" onclick="closeModal()">Close</button>
  </div>
</div>

<script>
const params = new URLSearchParams(window.location.search);
["utm_source","utm_medium","utm_campaign"].forEach(p => {
  const field = document.querySelector(`[name="${p}"]`);
  if (field) field.value = params.get(p) || "";
});

document.getElementById("leadForm").addEventListener("submit", function(e) {
  e.preventDefault();
  const form = this;
  const formData = new FormData(form);

  fetch("https://script.google.com/macros/s/AKfycbwUHkNaljAnnKyk7UXn6EKhqvBQuNROEURjhcvdE0Cz9cgrmAB53pd1E2gHwjqHzjlzAA/exec", {
    method: "POST",
    body: formData
  });

  document.getElementById("successInline").style.display = "block";
  document.getElementById("successModal").classList.add("active");
  form.reset();
});

function closeModal() {
  document.getElementById("successModal").classList.remove("active");
}
</script>

</body>
</html>

