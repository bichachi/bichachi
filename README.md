<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Stratosphere Shine | Jet Detailing Specialists</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Playfair+Display:wght@600&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg-dark: #050914;
      --bg-mid: #0e1630;
      --bg-light: #f3f5f9;
      --accent: #38bdf8;
      --accent-dark: #0ea5e9;
      --text-primary: #0b1224;
      --text-light: #ffffff;
      --card-shadow: rgba(5, 9, 20, 0.12);
      --radius-lg: 22px;
      --radius-md: 16px;
      --radius-sm: 10px;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: 'Montserrat', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
      color: var(--text-primary);
      background-color: var(--bg-light);
      line-height: 1.6;
    }

    h1, h2, h3 {
      font-family: 'Playfair Display', 'Times New Roman', serif;
      color: var(--text-primary);
      margin-top: 0;
    }

    p {
      margin-top: 0;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .hero {
      position: relative;
      min-height: 80vh;
      padding: 3rem clamp(1.5rem, 6vw, 6rem);
      color: var(--text-light);
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      background: linear-gradient(135deg, rgba(5, 9, 20, 0.85), rgba(5, 9, 20, 0.4)),
        url('https://images.unsplash.com/photo-1529074963764-98f45c47344b?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
    }

    .hero__overlay {
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at top left, rgba(56, 189, 248, 0.55), transparent 50%);
      pointer-events: none;
    }

    .hero > * {
      position: relative;
      z-index: 1;
    }

    .nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }

    .cta {
      padding: 0.75rem 1.5rem;
      border-radius: var(--radius-sm);
      border: 1px solid rgba(255, 255, 255, 0.5);
      font-weight: 600;
      backdrop-filter: blur(6px);
      transition: background-color 0.3s ease, border-color 0.3s ease;
    }

    .cta:hover {
      background-color: rgba(255, 255, 255, 0.2);
      border-color: rgba(255, 255, 255, 0.9);
    }

    .hero__content {
      max-width: 560px;
      padding: 3rem 0 6rem;
    }

    .hero__content h1 {
      font-size: clamp(2.5rem, 4vw + 1rem, 4.75rem);
      margin-bottom: 1rem;
      color: var(--text-light);
    }

    .hero__content p {
      font-size: 1.1rem;
      margin-bottom: 2rem;
      color: rgba(255, 255, 255, 0.85);
    }

    .hero__actions {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 0.85rem 1.8rem;
      border-radius: var(--radius-sm);
      font-weight: 600;
      transition: transform 0.2s ease, box-shadow 0.2s ease, background-color 0.2s ease;
      cursor: pointer;
    }

    .btn--primary {
      background: linear-gradient(135deg, var(--accent), var(--accent-dark));
      color: var(--text-light);
      box-shadow: 0 15px 30px rgba(56, 189, 248, 0.35);
    }

    .btn--primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 20px 40px rgba(56, 189, 248, 0.45);
    }

    .btn--secondary {
      background-color: rgba(255, 255, 255, 0.15);
      color: var(--text-light);
      border: 1px solid rgba(255, 255, 255, 0.35);
    }

    .btn--secondary:hover {
      background-color: rgba(255, 255, 255, 0.35);
    }

    .btn--ghost {
      border: 1px solid rgba(11, 18, 36, 0.15);
      color: var(--text-primary);
      background-color: transparent;
    }

    .btn--ghost:hover {
      border-color: rgba(11, 18, 36, 0.4);
      background-color: rgba(11, 18, 36, 0.05);
    }

    .section {
      padding: clamp(4rem, 8vw, 6rem) clamp(1.5rem, 6vw, 6rem);
      background-color: var(--bg-light);
    }

    .section--alt {
      background-color: #ffffff;
    }

    .section--dark {
      background: linear-gradient(145deg, var(--bg-dark), var(--bg-mid));
      color: var(--text-light);
    }

    .section__intro {
      max-width: 720px;
      margin-bottom: 3rem;
    }

    .section__intro h2 {
      font-size: clamp(2rem, 3vw + 1rem, 3.2rem);
    }

    .section__intro p {
      color: rgba(11, 18, 36, 0.7);
    }

    .section--dark .section__intro p {
      color: rgba(255, 255, 255, 0.75);
    }

    .section__intro--center {
      text-align: center;
      margin-left: auto;
      margin-right: auto;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 2rem;
    }

    .card {
      background-color: #ffffff;
      padding: 2rem;
      border-radius: var(--radius-lg);
      box-shadow: 0 25px 50px -25px var(--card-shadow);
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
    }

    .card ul {
      list-style: none;
      padding: 0;
      margin: 0;
      display: grid;
      gap: 0.75rem;
      color: rgba(11, 18, 36, 0.75);
    }

    .card__price {
      font-size: 1.8rem;
      font-weight: 700;
      color: var(--accent-dark);
      margin: 0;
    }

    .card--featured {
      background: linear-gradient(160deg, rgba(56, 189, 248, 0.15), rgba(14, 165, 233, 0.7));
      color: var(--text-primary);
      border: 1px solid rgba(14, 165, 233, 0.25);
    }

    .card--featured ul {
      color: rgba(11, 18, 36, 0.9);
    }

    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1.5rem;
    }

    .feature {
      background-color: rgba(14, 22, 48, 0.04);
      padding: 1.75rem;
      border-radius: var(--radius-md);
      border: 1px solid rgba(14, 22, 48, 0.08);
    }

    .timeline {
      list-style: none;
      margin: 0;
      padding: 0;
      display: grid;
      gap: 1.5rem;
    }

    .timeline li {
      display: grid;
      grid-template-columns: auto 1fr;
      gap: 1.5rem;
      align-items: start;
      background-color: #ffffff;
      padding: 1.5rem;
      border-radius: var(--radius-md);
      box-shadow: 0 10px 30px -20px var(--card-shadow);
    }

    .timeline__step {
      width: 42px;
      height: 42px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--accent), var(--accent-dark));
      color: var(--text-light);
      display: grid;
      place-items: center;
      font-weight: 700;
    }

    .section--dark .timeline li {
      background-color: rgba(11, 18, 36, 0.35);
      box-shadow: none;
    }

    .booking-form {
      background-color: rgba(11, 18, 36, 0.25);
      padding: clamp(2rem, 5vw, 3rem);
      border-radius: var(--radius-lg);
      box-shadow: 0 25px 50px -20px rgba(5, 9, 20, 0.45);
      backdrop-filter: blur(12px);
    }

    .form-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1.5rem;
    }

    label {
      font-weight: 600;
      display: grid;
      gap: 0.75rem;
      font-size: 0.95rem;
    }

    input,
    select,
    textarea {
      padding: 0.85rem 1rem;
      border-radius: var(--radius-sm);
      border: 1px solid rgba(255, 255, 255, 0.4);
      background-color: rgba(5, 9, 20, 0.35);
      color: var(--text-light);
      font-size: 1rem;
      font-family: inherit;
    }

    input::placeholder,
    textarea::placeholder {
      color: rgba(255, 255, 255, 0.6);
    }

    select {
      appearance: none;
      background-image: url('data:image/svg+xml,%3Csvg width="16" height="16" fill="white" xmlns="http://www.w3.org/2000/svg"%3E%3Cpath d="M4 6l4 4 4-4"/%3E%3C/svg%3E');
      background-repeat: no-repeat;
      background-position: right 1rem center;
    }

    input:focus,
    select:focus,
    textarea:focus {
      outline: 2px solid var(--accent);
      outline-offset: 2px;
    }

    textarea {
      resize: vertical;
    }

    .booking-form__notes {
      margin-top: 1.5rem;
    }

    .form-status {
      margin-top: 1rem;
      font-weight: 600;
      min-height: 1.5rem;
    }

    .section--dark .form-status {
      color: var(--text-light);
    }

    .footer {
      display: grid;
      gap: 1.5rem;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      padding: 3rem clamp(1.5rem, 6vw, 6rem);
      background-color: #02060f;
      color: rgba(255, 255, 255, 0.75);
    }

    .footer h3 {
      color: var(--text-light);
    }

    .footer__fineprint {
      grid-column: 1 / -1;
      font-size: 0.85rem;
      color: rgba(255, 255, 255, 0.55);
    }

    @media (max-width: 720px) {
      .hero {
        min-height: auto;
        padding-bottom: 4rem;
      }

      .hero__content {
        padding-bottom: 2rem;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        transition-duration: 0.01ms !important;
        animation-duration: 0.01ms !important;
      }
    }

    .booking-form.is-loading {
      opacity: 0.7;
      pointer-events: none;
    }

    .booking-form.is-loading .btn {
      cursor: progress;
    }
  </style>
</head>
<body>
  <header class="hero">
    <div class="hero__overlay"></div>
    <nav class="nav">
      <div class="logo">Stratosphere Shine</div>
      <a class="cta" href="#booking">Book Detailing</a>
    </nav>
    <div class="hero__content">
      <h1>Premium Jet Detailing Crafted for the Clouds</h1>
      <p>Elevate every flight with meticulous exterior and interior detailing delivered by aviation-certified specialists.</p>
      <div class="hero__actions">
        <a class="btn btn--primary" href="#packages">Explore Packages</a>
        <a class="btn btn--secondary" href="#booking">Schedule Service</a>
      </div>
    </div>
  </header>

  <main>
    <section class="section" id="packages">
      <div class="section__intro">
        <h2>Signature Detailing Packages</h2>
        <p>Each package is engineered around FAA-compliant products, hangar-safe processes, and the unique needs of business aviation.</p>
      </div>
      <div class="cards">
        <article class="card">
          <h3>Silver Ascend</h3>
          <p class="card__price">$1,150</p>
          <ul>
            <li>Exterior foam wash &amp; decontamination</li>
            <li>Drying with aviation-grade microfiber</li>
            <li>Brightwork spot polishing</li>
            <li>Cabin sanitization and vacuum</li>
          </ul>
          <a class="btn btn--ghost" href="#booking">Choose Silver</a>
        </article>
        <article class="card card--featured">
          <h3>Platinum Flightdeck</h3>
          <p class="card__price">$2,450</p>
          <ul>
            <li>Complete exterior polish &amp; sealant</li>
            <li>Engine nacelle deep clean</li>
            <li>Leather hydration &amp; stain treatment</li>
            <li>Cockpit glass anti-glare coating</li>
          </ul>
          <a class="btn btn--primary" href="#booking">Most Popular</a>
        </article>
        <article class="card">
          <h3>Elite Hangar Concierge</h3>
          <p class="card__price">$4,800</p>
          <ul>
            <li>Full surface correction &amp; graphene protectant</li>
            <li>Interior ozone purification &amp; detailing</li>
            <li>Brightwork restoration &amp; anti-corrosion</li>
            <li>On-board amenity restocking</li>
          </ul>
          <a class="btn btn--ghost" href="#booking">Choose Elite</a>
        </article>
      </div>
    </section>

    <section class="section section--alt" id="why-us">
      <div class="section__intro">
        <h2>Why Owners Choose Stratosphere Shine</h2>
        <p>We fuse luxury detailing with aviation maintenance discipline to protect paint systems, interior finishes, and mission readiness.</p>
      </div>
      <div class="features">
        <div class="feature">
          <h3>Certified Technicians</h3>
          <p>Our detailing crew is NATA Safety 1st certified and trained alongside maintenance teams for coordinated service visits.</p>
        </div>
        <div class="feature">
          <h3>Mobile Hangar Service</h3>
          <p>We dispatch to your preferred FBO or private hangar within 300 NM with self-contained power, water, and filtration.</p>
        </div>
        <div class="feature">
          <h3>Protective Chemistry</h3>
          <p>We select ceramic, graphene, and interior protectants engineered for aircraft substrates and proven in flight operations.</p>
        </div>
      </div>
    </section>

    <section class="section" id="process">
      <div class="section__intro">
        <h2>Detailing Flight Plan</h2>
        <p>From wheels down to cabin handover, our process keeps your aircraft immaculate and ready for passengers.</p>
      </div>
      <ol class="timeline">
        <li>
          <span class="timeline__step">1</span>
          <div>
            <h3>Arrival &amp; Inspection</h3>
            <p>We conduct a detailed walk-around with your crew, documenting paint condition, brightwork, and interior requests.</p>
          </div>
        </li>
        <li>
          <span class="timeline__step">2</span>
          <div>
            <h3>Exterior Rejuvenation</h3>
            <p>Foam wash, decontamination, polishing, and protectant application restore luster while respecting aircraft systems.</p>
          </div>
        </li>
        <li>
          <span class="timeline__step">3</span>
          <div>
            <h3>Cabin Detailing</h3>
            <p>Leather, textiles, stone, and brightwork receive tailored care with hypoallergenic, aviation-approved chemistry.</p>
          </div>
        </li>
        <li>
          <span class="timeline__step">4</span>
          <div>
            <h3>Final QA &amp; Departure Brief</h3>
            <p>We review every checklist item with your chief pilot, leaving the aircraft hangar-ready and passenger perfect.</p>
          </div>
        </li>
      </ol>
    </section>

    <section class="section section--dark" id="booking">
      <div class="section__intro section__intro--center">
        <h2>Schedule Your Detailing</h2>
        <p>Tell us about your aircraft and preferred service window. A concierge will confirm hangar logistics within one business hour.</p>
      </div>
      <form class="booking-form" aria-label="Jet detailing booking form">
        <div class="form-grid">
          <label>
            Contact Name
            <input type="text" name="name" placeholder="Captain Jordan Avery" required>
          </label>
          <label>
            Email
            <input type="email" name="email" placeholder="operations@flightdept.com" required>
          </label>
          <label>
            Phone
            <input type="tel" name="phone" placeholder="+1 (555) 012-3456" required>
          </label>
          <label>
            Aircraft Model
            <input type="text" name="aircraft" placeholder="Gulfstream G600" required>
          </label>
          <label>
            Preferred Date
            <input type="date" name="date" required>
          </label>
          <label>
            Preferred Time
            <input type="time" name="time" required>
          </label>
          <label>
            Hangar or FBO Location
            <input type="text" name="location" placeholder="Signature Flight Support - KTEB" required>
          </label>
          <label>
            Detailing Package
            <select name="package" required>
              <option value="" disabled selected>Select a package</option>
              <option value="silver">Silver Ascend</option>
              <option value="platinum">Platinum Flightdeck</option>
              <option value="elite">Elite Hangar Concierge</option>
            </select>
          </label>
        </div>
        <label class="booking-form__notes">
          Additional Notes
          <textarea name="notes" rows="4" placeholder="Request anti-icing boot conditioning and espresso bar restock."></textarea>
        </label>
        <button class="btn btn--primary" type="submit">Submit Booking Request</button>
        <p class="form-status" role="status" aria-live="polite"></p>
      </form>
    </section>
  </main>

  <footer class="footer">
    <div>
      <h3>Stratosphere Shine</h3>
      <p>FAA-compliant luxury jet detailing based in Teterboro, serving North American flight departments.</p>
    </div>
    <div>
      <p><strong>Operations:</strong> +1 (555) 987-6543</p>
      <p><strong>Email:</strong> concierge@stratosphereshine.aero</p>
    </div>
    <div class="footer__fineprint">
      <p>&copy; <span id="year"></span> Stratosphere Shine. All rights reserved.</p>
    </div>
  </footer>

  <script>
    const bookingForm = document.querySelector('.booking-form');
    const statusMessage = document.querySelector('.form-status');
    const yearEl = document.getElementById('year');

    if (yearEl) {
      yearEl.textContent = new Date().getFullYear();
    }

    const formatFormData = (formData) => {
      const entries = Array.from(formData.entries());
      return entries
        .map(([key, value]) => {
          if (!value) return null;
          const label = key
            .replace(/([A-Z])/g, ' $1')
            .replace(/^[a-z]/, (char) => char.toUpperCase());
          return `${label}: ${value}`;
        })
        .filter(Boolean)
        .join('\n');
    };

    const simulateNetworkRequest = () =>
      new Promise((resolve) => {
        setTimeout(resolve, 1200);
      });

    if (bookingForm) {
      bookingForm.addEventListener('submit', async (event) => {
        event.preventDefault();
        statusMessage.textContent = 'Submitting your request...';
        bookingForm.classList.add('is-loading');

        const formData = new FormData(bookingForm);
        const messageBody = formatFormData(formData);

        try {
          await simulateNetworkRequest();
          statusMessage.textContent = 'Request received! Our concierge team will reach out shortly to finalize your service window.';
          bookingForm.reset();
          console.groupCollapsed('Booking submission');
          console.log(messageBody);
          console.groupEnd();
        } catch (error) {
          statusMessage.textContent = 'There was an issue submitting your request. Please try again or call our operations line.';
          console.error(error);
        } finally {
          bookingForm.classList.remove('is-loading');
        }
      });
    }
  </script>
</body>
</html>
