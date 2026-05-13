---
theme: default
title: BTO — Boil the Ocean
background: '#000'
class: text-white
highlighter: shiki
transition: slide-left
mdc: true
fonts:
  sans: 'DM Sans'
  serif: 'Playfair Display'
  mono: 'JetBrains Mono'
---

<style>
:root {
  --color-bg: #000000;
  --color-fg: #ffffff;
  --color-accent: #ffffff;
  --color-muted: #555555;
  --color-dim: #222222;
}

* { font-family: 'DM Sans', sans-serif; }

.slidev-layout {
  background: #000;
  color: #fff;
}

.num {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  background: #fff;
  color: #000;
  font-weight: 800;
  font-size: 1.2rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.tag {
  font-size: 0.65rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: #888;
  font-weight: 600;
}

.rule { border-top: 1px solid #333; margin: 1.5rem 0; }

.product-card {
  border: 1px solid #2a2a2a;
  padding: 1.5rem;
  border-radius: 2px;
}

.product-card h3 {
  font-size: 1.1rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.product-card .desc {
  font-size: 0.85rem;
  color: #aaa;
  line-height: 1.5;
}

.arrow-right {
  font-size: 1.4rem;
  color: #555;
  align-self: center;
}

.ecosystem-node {
  border: 1px solid #333;
  padding: 1rem 1.5rem;
  text-align: center;
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 0.05em;
}

.ecosystem-node.highlight {
  border-color: #fff;
  background: #fff;
  color: #000;
}

.stat-block {
  border-left: 2px solid #fff;
  padding-left: 1.2rem;
}

.stat-block .big {
  font-size: 2.5rem;
  font-weight: 800;
  line-height: 1;
}

.stat-block .label {
  font-size: 0.75rem;
  color: #888;
  letter-spacing: 0.12em;
  text-transform: uppercase;
}

.advisor-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1px;
  background: #222;
  border: 1px solid #222;
}

.advisor-cell {
  background: #000;
  padding: 1.2rem;
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
}

.advisor-cell .name {
  font-weight: 700;
  font-size: 0.9rem;
}

.advisor-cell .role {
  font-size: 0.75rem;
  color: #888;
}

.moat-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid #1a1a1a;
}

.moat-item .icon {
  font-size: 1.2rem;
  margin-top: 2px;
  min-width: 24px;
}

.moat-item .text h4 {
  font-size: 0.95rem;
  font-weight: 700;
  margin-bottom: 0.2rem;
}

.moat-item .text p {
  font-size: 0.8rem;
  color: #888;
  line-height: 1.5;
}

</style>


<div class="absolute inset-0 flex flex-col justify-between p-16">
  <div class="tag">Confidential · 2026</div>

  <div>
    <div style="font-size: 5rem; font-weight: 900; letter-spacing: -0.04em; line-height: 0.9;">
      Boil the<br/>Ocean.
    </div>
    <div class="rule" style="max-width: 200px; margin-top: 2rem;"/>
    <div style="font-size: 1rem; color: #888; margin-top: 1.5rem; max-width: 480px; line-height: 1.6;">
      A predictive intelligence platform that tells you what content wins — before production begins.
    </div>
  </div>

  <div style="display: flex; gap: 4rem; align-items: flex-end;">
    <div>
      <div class="tag">Company</div>
      <div style="font-weight: 600; margin-top: 0.3rem;">MRC Entertainment</div>
    </div>
    <div>
      <div class="tag">Stage</div>
      <div style="font-weight: 600; margin-top: 0.3rem;">Prototype</div>
    </div>
    <div>
      <div class="tag">Date</div>
      <div style="font-weight: 600; margin-top: 0.3rem;">2026</div>
    </div>
  </div>
</div>

---

<div class="p-12">
  <div class="tag" style="margin-bottom: 2rem;">The Problem</div>
  <div style="font-size: 2.2rem; font-weight: 800; letter-spacing: -0.02em; line-height: 1.1; max-width: 640px; margin-bottom: 3rem;">
    The entertainment supply chain is broken.
  </div>

  <div style="display: flex; align-items: center; gap: 1rem; flex-wrap: wrap;">
    <div class="ecosystem-node">
      Writer / Creator
    </div>
    <div class="arrow-right">→</div>
    <div class="ecosystem-node">
      Agent / Manager
    </div>
    <div class="arrow-right">→</div>
    <div class="ecosystem-node">
      Studio / Network
    </div>
    <div class="arrow-right">→</div>
    <div class="ecosystem-node">
      Greenlight
    </div>
    <div class="arrow-right">→</div>
    <div class="ecosystem-node">
      Production
    </div>
    <div class="arrow-right">→</div>
    <div class="ecosystem-node">
      Distribution
    </div>
    <div class="arrow-right">→</div>
    <div class="ecosystem-node highlight">
      Audience
    </div>
  </div>

  <div class="rule"/>

  <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 2rem; margin-top: 0.5rem;">
    <div>
      <div style="font-weight: 700; margin-bottom: 0.4rem;">No data at the top</div>
      <div style="font-size: 0.82rem; color: #888; line-height: 1.5;">Creators pitch blind. Executives buy on instinct. No feedback loop between audience outcome and greenlight decision.</div>
    </div>
    <div>
      <div style="font-weight: 700; margin-bottom: 0.4rem;">Access is everything</div>
      <div style="font-size: 0.82rem; color: #888; line-height: 1.5;">Gatekeepers decide who gets heard. Great material dies in inboxes. Relationships matter more than quality.</div>
    </div>
    <div>
      <div style="font-weight: 700; margin-bottom: 0.4rem;">Billions wasted annually</div>
      <div style="font-size: 0.82rem; color: #888; line-height: 1.5;">Studios greenlight on gut feel. Most projects underperform. The data to prevent this exists — it just isn't being used.</div>
    </div>
  </div>
</div>

---

<div class="p-12">
  <div class="tag" style="margin-bottom: 2rem;">The Vision</div>
  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center; height: 75%;">

    <div>
      <div style="font-size: 2rem; font-weight: 800; letter-spacing: -0.02em; line-height: 1.1; margin-bottom: 1.5rem;">
        From global content spend<br/>to one creator's screen.
      </div>
      <div style="font-size: 0.88rem; color: #aaa; line-height: 1.7;">
        Every year, studios and streamers spend hundreds of billions on content. Most of that decision-making is intuition. BTO brings the predictive intelligence of Wall Street quant desks to the greenlight table — starting with a single script, horror films, and the streamers who buy them.
      </div>
      <div class="rule" style="max-width: 200px;"/>
      <div style="font-size: 0.8rem; color: #666; font-style: italic;">
        → Think: zoom out to see the $300B global market. Zoom in and land on a YouTuber uploading their first screenplay.
      </div>
    </div>
    <div style="border: 1px solid #2a2a2a; aspect-ratio: 16/9; display: flex; align-items: center; justify-content: center; flex-direction: column; gap: 0.75rem; background: #0a0a0a;">
      <div style="font-size: 2rem;">▶</div>
      <div class="tag">Insert animation / video here</div>
      <div style="font-size: 0.75rem; color: #555; text-align: center; padding: 0 2rem; line-height: 1.5;">World → country → city → bedroom → laptop screen</div>
    </div>

  </div>
</div>

---

<div class="p-12">
  <div class="tag" style="margin-bottom: 2rem;">The Product</div>
  <div style="font-size: 2rem; font-weight: 800; letter-spacing: -0.02em; margin-bottom: 2.5rem;">Four products. One ecosystem.</div>

  <div style="display: grid; grid-template-columns: repeat(4, 1fr); gap: 1px; background: #1a1a1a; border: 1px solid #1a1a1a;">
    <div class="product-card" style="border: none; background: #000; border-right: 1px solid #1a1a1a;">
      <div class="num" style="margin-bottom: 1rem;">1</div>
      <h3>Nucleus</h3>
      <div class="desc">Executive insights + seeds for Creator Insights & Explorer. The scarce evaluation context elite film + TV leaders use.</div>
    </div>
    <div class="product-card" style="border: none; background: #000; border-right: 1px solid #1a1a1a;">
      <div class="num" style="margin-bottom: 1rem;">2</div>
      <h3>Creator Insights</h3>
      <div class="desc">Give creators the analytics and predictive power previously only available to studios. Discover the gatekeepers behind similar hits.</div>
    </div>
    <div class="product-card" style="border: none; background: #000; border-right: 1px solid #1a1a1a;">
      <div class="num" style="margin-bottom: 1rem;">3</div>
      <h3>Creator Explorer</h3>
      <div class="desc">Match creatives to decision-makers based on predictive performance. Creators connect to gatekeepers. Executives find emerging talent.</div>
    </div>
    <div class="product-card" style="border: none; background: #000;">
      <div class="num" style="margin-bottom: 1rem;">4</div>
      <h3>Marketplace</h3>
      <div class="desc">Commercial access to the most compelling material. Transform access to and for the best talent. Collapse the supply chain.</div>
    </div>
  </div>
</div>

---

<div class="p-12">
  <div class="tag" style="margin-bottom: 2rem;">Wedge Product</div>
  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 4rem;">

    <div>
      <div style="font-size: 2rem; font-weight: 800; letter-spacing: -0.02em; line-height: 1.1; margin-bottom: 1.5rem;">
        Start here:<br/>Horror scripts.<br/>Six platforms.
      </div>
      <div style="font-size: 0.88rem; color: #aaa; line-height: 1.7; margin-bottom: 1.5rem;">
        The BTO prototype ingests horror scripts and produces a full predictive analysis — taxonomy, comp sets, financial outcomes, and advisor-grade wisdom — for each major buyer.
      </div>
      <div style="display: flex; flex-direction: column; gap: 0.75rem;">
        <div style="display: flex; gap: 0.75rem; align-items: center;">
          <div style="width: 6px; height: 6px; background: #fff; border-radius: 50%;"></div>
          <div style="font-size: 0.85rem;">Netflix · Amazon · Apple</div>
        </div>
        <div style="display: flex; gap: 0.75rem; align-items: center;">
          <div style="width: 6px; height: 6px; background: #fff; border-radius: 50%;"></div>
          <div style="font-size: 0.85rem;">WB · Sony · Paramount</div>
        </div>
        <div style="display: flex; gap: 0.75rem; align-items: center;">
          <div style="width: 6px; height: 6px; background: #444; border-radius: 50%;"></div>
          <div style="font-size: 0.85rem; color: #666;">HBO · Peacock · Par+ (discuss)</div>
        </div>
      </div>
    </div>
    <div style="display: flex; flex-direction: column; gap: 0.75rem;">
      <div style="border: 1px solid #2a2a2a; aspect-ratio: 16/10; display: flex; align-items: center; justify-content: center; flex-direction: column; gap: 0.5rem; background: #050505;">
        <div style="font-size: 1.5rem;">💻</div>
        <div class="tag">Insert product demo / screen recording</div>
        <div style="font-size: 0.75rem; color: #555;">Laptop mockup scrolling through BTO output</div>
      </div>
      <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 0.5rem;">
        <div style="border: 1px solid #1a1a1a; padding: 0.75rem; font-size: 0.75rem; color: #888; text-align: center;">Taxonomy</div>
        <div style="border: 1px solid #1a1a1a; padding: 0.75rem; font-size: 0.75rem; color: #888; text-align: center;">Comp Sets</div>
        <div style="border: 1px solid #1a1a1a; padding: 0.75rem; font-size: 0.75rem; color: #888; text-align: center;">$ Outcomes</div>
      </div>
    </div>
  </div>
</div>

---

<div class="p-12">
  <div class="tag" style="margin-bottom: 2rem;">Early Customers</div>
  <div style="font-size: 2rem; font-weight: 800; letter-spacing: -0.02em; margin-bottom: 2.5rem;">Who we sell to first.</div>

  <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; margin-bottom: 2rem;">
    <div style="border: 1px solid #2a2a2a; padding: 1.5rem;">
      <div class="tag" style="margin-bottom: 0.75rem;">Buyer Type 1</div>
      <div style="font-weight: 700; font-size: 1rem; margin-bottom: 0.5rem;">Studio & Streamer Execs</div>
      <div style="font-size: 0.82rem; color: #888; line-height: 1.5;">Development and acquisition teams who currently greenlight on instinct. BTO gives them defensible data and faster comps.</div>
    </div>
    <div style="border: 1px solid #2a2a2a; padding: 1.5rem;">
      <div class="tag" style="margin-bottom: 0.75rem;">Buyer Type 2</div>
      <div style="font-weight: 700; font-size: 1rem; margin-bottom: 0.5rem;">Producers & Financiers</div>
      <div style="font-size: 0.82rem; color: #888; line-height: 1.5;">Independent producers and financiers who need to de-risk packages before attaching talent or committing capital.</div>
    </div>
    <div style="border: 1px solid #2a2a2a; padding: 1.5rem;">
      <div class="tag" style="margin-bottom: 0.75rem;">Buyer Type 3</div>
      <div style="font-weight: 700; font-size: 1rem; margin-bottom: 0.5rem;">Emerging Creators</div>
      <div style="font-size: 0.82rem; color: #888; line-height: 1.5;">Writers and directors with scripts who need to understand where they fit and how to get in front of the right buyer.</div>
    </div>
  </div>

  <div style="background: #0a0a0a; border: 1px solid #2a2a2a; padding: 1.25rem; display: flex; align-items: center; gap: 2rem;">
    <div style="font-size: 0.8rem; color: #666; text-transform: uppercase; letter-spacing: 0.1em; white-space: nowrap;">Add logos / names here →</div>
    <div style="display: flex; gap: 2rem; align-items: center; flex-wrap: wrap;">
      <div style="color: #444; font-size: 0.85rem; font-style: italic;">[ Partner / Customer 1 ]</div>
      <div style="color: #444; font-size: 0.85rem; font-style: italic;">[ Partner / Customer 2 ]</div>
      <div style="color: #444; font-size: 0.85rem; font-style: italic;">[ Partner / Customer 3 ]</div>
      <div style="color: #444; font-size: 0.85rem; font-style: italic;">[ Partner / Customer 4 ]</div>
    </div>
  </div>
</div>

---

<div class="p-12">
  <div class="tag" style="margin-bottom: 2rem;">Competitive Advantage</div>
  <div style="font-size: 2rem; font-weight: 800; letter-spacing: -0.02em; margin-bottom: 0.5rem;">What we need to become<br/>the #1 intelligence layer<br/>in entertainment.</div>

  <div class="rule" style="max-width: 300px;"/>

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0;">
    <div>
      <div class="moat-item">
        <div class="icon">◼</div>
        <div class="text">
          <h4>Proprietary Data Flywheel</h4>
          <p>Every script processed makes the model smarter. Comp sets get tighter. Predictions get sharper. Competitors can't replicate the training set.</p>
        </div>
      </div>
      <div class="moat-item">
        <div class="icon">◼</div>
        <div class="text">
          <h4>Advisor Network = Ground Truth</h4>
          <p>Our advisors are the gatekeepers. Their postmortem wisdom is baked into the model — not scraped from the internet.</p>
        </div>
      </div>
      <div class="moat-item">
        <div class="icon">◼</div>
        <div class="text">
          <h4>Full-Stack: Creator to Buyer</h4>
          <p>We own both sides of the market. That two-sided network is the moat. Each side makes the other more valuable.</p>
        </div>
      </div>
    </div>
    <div style="padding-left: 2.5rem; border-left: 1px solid #1a1a1a;">
      <div class="moat-item">
        <div class="icon">◼</div>
        <div class="text">
          <h4>MRC's 20-Year Film/TV Library</h4>
          <p>House of Cards, Knives Out, Ted Lasso. Real outcomes, real data, real comps — from titles that actually got made and distributed.</p>
        </div>
      </div>
      <div class="moat-item">
        <div class="icon">◼</div>
        <div class="text">
          <h4>Dollars-to-Views Translation</h4>
          <p>We map production spend to streaming viewership — a metric most studios still can't reliably calculate internally.</p>
        </div>
      </div>
      <div class="moat-item">
        <div class="icon">◼</div>
        <div class="text">
          <h4>Genre-Deep Before Going Wide</h4>
          <p>Horror first means we dominate a vertical before any competitor can react. Depth beats breadth at launch.</p>
        </div>
      </div>
    </div>
  </div>
</div>

---

<div class="p-12">
  <div class="tag" style="margin-bottom: 2rem;">The Product in Motion</div>
  <div style="font-size: 2rem; font-weight: 800; letter-spacing: -0.02em; margin-bottom: 2rem;">See it work.</div>

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem;">
    <div style="aspect-ratio: 16/9; border: 1px solid #2a2a2a; background: #050505; display: flex; align-items: center; justify-content: center; flex-direction: column; gap: 0.75rem; grid-column: span 2;">
      <div style="font-size: 2rem;">▶</div>
      <div class="tag">Insert primary demo video here</div>
      <div style="font-size: 0.75rem; color: #555;">Full product walkthrough · ~60–90 seconds</div>
    </div>
  </div>

  <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem; margin-top: 1rem;">
    <div style="border: 1px solid #1a1a1a; padding: 1rem; aspect-ratio: 16/9; display: flex; align-items: center; justify-content: center; flex-direction: column; gap: 0.4rem;">
      <div style="font-size: 1rem;">▶</div>
      <div style="font-size: 0.7rem; color: #555; text-align: center;">Script input → taxonomy output</div>
    </div>
    <div style="border: 1px solid #1a1a1a; padding: 1rem; aspect-ratio: 16/9; display: flex; align-items: center; justify-content: center; flex-direction: column; gap: 0.4rem;">
      <div style="font-size: 1rem;">▶</div>
      <div style="font-size: 0.7rem; color: #555; text-align: center;">Comp sets + financial model</div>
    </div>
    <div style="border: 1px solid #1a1a1a; padding: 1rem; aspect-ratio: 16/9; display: flex; align-items: center; justify-content: center; flex-direction: column; gap: 0.4rem;">
      <div style="font-size: 1rem;">▶</div>
      <div style="font-size: 0.7rem; color: #555; text-align: center;">Marketplace API demo</div>
    </div>
  </div>
</div>

---

<div class="p-12">
  <div class="tag" style="margin-bottom: 2rem;">The Team</div>
  <div style="font-size: 2rem; font-weight: 800; letter-spacing: -0.02em; margin-bottom: 2.5rem;">Built by insiders. Advised by the best.</div>

  <div style="margin-bottom: 1.5rem;">
    <div class="tag" style="margin-bottom: 1rem;">Core Team</div>
    <div style="display: grid; grid-template-columns: repeat(4, 1fr); gap: 1px; background: #1a1a1a; border: 1px solid #1a1a1a;">
      <div style="background: #000; padding: 1.25rem;">
        <div style="font-weight: 700; margin-bottom: 0.25rem;">[ Name ]</div>
        <div style="font-size: 0.78rem; color: #888;">[ Title / Background ]</div>
      </div>
      <div style="background: #000; padding: 1.25rem;">
        <div style="font-weight: 700; margin-bottom: 0.25rem;">[ Name ]</div>
        <div style="font-size: 0.78rem; color: #888;">[ Title / Background ]</div>
      </div>
      <div style="background: #000; padding: 1.25rem;">
        <div style="font-weight: 700; margin-bottom: 0.25rem;">[ Name ]</div>
        <div style="font-size: 0.78rem; color: #888;">[ Title / Background ]</div>
      </div>
      <div style="background: #000; padding: 1.25rem;">
        <div style="font-weight: 700; margin-bottom: 0.25rem;">[ Name ]</div>
        <div style="font-size: 0.78rem; color: #888;">[ Title / Background ]</div>
      </div>
    </div>
  </div>

  <div>
    <div class="tag" style="margin-bottom: 1rem;">Advisors</div>
    <div class="advisor-grid">
      <div class="advisor-cell"><div class="name">[ Advisor Name ]</div><div class="role">[ Studio / Network ]</div></div>
      <div class="advisor-cell"><div class="name">[ Advisor Name ]</div><div class="role">[ Studio / Network ]</div></div>
      <div class="advisor-cell"><div class="name">[ Advisor Name ]</div><div class="role">[ Studio / Network ]</div></div>
      <div class="advisor-cell"><div class="name">[ Advisor Name ]</div><div class="role">[ Studio / Network ]</div></div>
      <div class="advisor-cell"><div class="name">[ Advisor Name ]</div><div class="role">[ Studio / Network ]</div></div>
      <div class="advisor-cell"><div class="name">[ Advisor Name ]</div><div class="role">[ Studio / Network ]</div></div>
      <div class="advisor-cell"><div class="name">[ Advisor Name ]</div><div class="role">[ Studio / Network ]</div></div>
    </div>
  </div>
</div>
