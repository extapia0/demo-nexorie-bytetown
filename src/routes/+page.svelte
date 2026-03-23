<script lang="ts">
  const features = [
    'Custom AI companions tuned for creator brands and private communities.',
    'Fast onboarding flow with premium visuals, clear CTA hierarchy, and mobile-safe layouts.',
    'Flexible section system for product tiers, use cases, and showcase content.'
  ];

  const plans = [
    { name: 'OF Models', detail: 'Private fan engagement with signature persona flows.' },
    { name: 'Influencers', detail: 'On-brand assistants for outreach, drops, and gated content.' },
    { name: 'Live Dealer', detail: 'High-touch conversational flows for premium interactive experiences.' }
  ];

  const stats = [
    { value: '24/7', label: 'Always-on AI concierge' },
    { value: '3x', label: 'Faster launch-ready branded experiences' },
    { value: '0', label: 'Missing screenshot dependencies in production build' }
  ];
</script>

<svelte:head>
  <title>Nexorie Bytetown</title>
  <meta
    name="description"
    content="A polished Svelte landing page for Nexorie Bytetown with production-safe visuals for Vercel deploys."
  />
</svelte:head>

<div class="page-shell">
  <div class="orb orb-left" aria-hidden="true"></div>
  <div class="orb orb-right" aria-hidden="true"></div>

  <main class="page">
    <section class="hero card">
      <div class="hero-copy">
        <p class="eyebrow">Nexorie Bytetown</p>
        <h1>Unlock AI experiences that feel premium from the first screen.</h1>
        <p class="lede">
          A production-safe landing page with bold gradients, clear sections, and no missing local
          image dependencies.
        </p>

        <div class="actions">
          <a class="button primary" href="#plans">Explore solutions</a>
          <a class="button ghost" href="#contact">Book a walkthrough</a>
        </div>

        <div class="stats">
          {#each stats as stat}
            <article>
              <strong>{stat.value}</strong>
              <span>{stat.label}</span>
            </article>
          {/each}
        </div>
      </div>

      <div class="hero-art" aria-hidden="true">
        <div class="phone phone-large"></div>
        <div class="phone phone-small"></div>
      </div>
    </section>

    <section class="grid">
      <article class="card intro">
        <p class="eyebrow">Why it works</p>
        <h2>Built for sharp launches, not fragile screenshot placeholders.</h2>
        <ul>
          {#each features as feature}
            <li>{feature}</li>
          {/each}
        </ul>
      </article>

      <article class="card accent-panel">
        <p class="eyebrow">Design language</p>
        <h2>Dark-glass visuals, luminous gradients, and strong CTA rhythm.</h2>
        <p>
          The page keeps the futuristic direction of the original concept while relying only on
          code-driven visuals that compile cleanly on Vercel.
        </p>
      </article>
    </section>

    <section class="plans" id="plans">
      {#each plans as plan}
        <article class="card plan">
          <p class="eyebrow">{plan.name}</p>
          <h3>{plan.name} Experience</h3>
          <p>{plan.detail}</p>
          <span class="chip">Customizable</span>
        </article>
      {/each}
    </section>

    <section class="showcase card">
      <div>
        <p class="eyebrow">Customization</p>
        <h2>Shape voice, visuals, and conversion flow around each audience.</h2>
        <p>
          Adjust messaging, offer structure, and presentation style without changing the deployment
          model. The page remains static-friendly and adapter-vercel compatible.
        </p>
      </div>
      <div class="showcase-art" aria-hidden="true">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </section>

    <section class="contact card" id="contact">
      <div>
        <p class="eyebrow">Next step</p>
        <h2>Deploy-ready and linked to Vercel.</h2>
      </div>
      <a class="button primary" href="mailto:hello@nexorie.ai">Contact team</a>
    </section>
  </main>
</div>

<style>
  :global(html) {
    background: #090b16;
  }

  :global(body) {
    margin: 0;
    min-width: 320px;
    font-family: "Segoe UI", Aptos, sans-serif;
    color: #f5f7ff;
    background:
      radial-gradient(circle at 20% 0%, rgba(126, 110, 255, 0.28), transparent 28%),
      radial-gradient(circle at 100% 20%, rgba(58, 227, 255, 0.22), transparent 22%),
      linear-gradient(180deg, #151933 0%, #0d1124 44%, #090b16 100%);
  }

  :global(*) {
    box-sizing: border-box;
  }

  a {
    color: inherit;
    text-decoration: none;
  }

  h1,
  h2,
  h3,
  p,
  ul {
    margin: 0;
  }

  .page-shell {
    position: relative;
    overflow: clip;
    min-height: 100vh;
    padding: 24px;
  }

  .page {
    position: relative;
    z-index: 1;
    width: min(1180px, 100%);
    margin: 0 auto;
    display: grid;
    gap: 18px;
  }

  .card {
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 28px;
    background: rgba(13, 17, 36, 0.72);
    box-shadow: 0 24px 80px rgba(0, 0, 0, 0.28);
    backdrop-filter: blur(18px);
  }

  .hero,
  .showcase,
  .contact {
    display: grid;
    gap: 28px;
  }

  .hero {
    grid-template-columns: minmax(0, 1.1fr) minmax(320px, 0.9fr);
    padding: 44px;
    min-height: 640px;
  }

  .hero-copy,
  .intro,
  .accent-panel,
  .plan,
  .showcase,
  .contact {
    display: grid;
    gap: 20px;
  }

  .eyebrow {
    color: #96a1ff;
    font-size: 14px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
  }

  h1 {
    max-width: 700px;
    font-size: clamp(54px, 8vw, 92px);
    line-height: 0.95;
    letter-spacing: -0.06em;
    font-weight: 600;
  }

  h2 {
    font-size: clamp(34px, 5vw, 54px);
    line-height: 0.98;
    letter-spacing: -0.05em;
    font-weight: 600;
  }

  h3 {
    font-size: 28px;
    letter-spacing: -0.04em;
    font-weight: 600;
  }

  .lede,
  .intro li,
  .accent-panel p,
  .plan p,
  .showcase p {
    font-size: 18px;
    line-height: 1.6;
    color: rgba(245, 247, 255, 0.8);
  }

  .actions,
  .stats,
  .plans {
    display: flex;
    gap: 14px;
    flex-wrap: wrap;
  }

  .button {
    min-height: 48px;
    padding: 0 22px;
    border-radius: 999px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
  }

  .button.primary {
    color: #09101f;
    background: linear-gradient(135deg, #b8c3ff, #8af0ff);
  }

  .button.ghost {
    border: 1px solid rgba(255, 255, 255, 0.16);
    background: rgba(255, 255, 255, 0.04);
  }

  .stats article {
    min-width: 130px;
    padding: 16px 18px;
    border-radius: 18px;
    background: rgba(255, 255, 255, 0.04);
    border: 1px solid rgba(255, 255, 255, 0.08);
    display: grid;
    gap: 8px;
  }

  .stats strong {
    font-size: 32px;
    letter-spacing: -0.05em;
  }

  .stats span {
    color: rgba(245, 247, 255, 0.68);
    font-size: 14px;
    line-height: 1.4;
  }

  .hero-art {
    position: relative;
    min-height: 420px;
    border-radius: 24px;
    overflow: hidden;
    background:
      radial-gradient(circle at 50% 16%, rgba(166, 150, 255, 0.54), transparent 24%),
      radial-gradient(circle at 70% 74%, rgba(101, 232, 255, 0.42), transparent 18%),
      linear-gradient(160deg, rgba(255, 255, 255, 0.12), rgba(255, 255, 255, 0.02));
    border: 1px solid rgba(255, 255, 255, 0.08);
  }

  .phone {
    position: absolute;
    border-radius: 28px;
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.22), rgba(255, 255, 255, 0.02)),
      linear-gradient(180deg, #151933, #0c1022);
    border: 1px solid rgba(255, 255, 255, 0.12);
    box-shadow: 0 22px 44px rgba(0, 0, 0, 0.3);
  }

  .phone::before,
  .phone::after {
    content: '';
    position: absolute;
    left: 14px;
    right: 14px;
    border-radius: 16px;
  }

  .phone::before {
    top: 18px;
    height: 44%;
    background:
      radial-gradient(circle at 30% 30%, rgba(184, 195, 255, 0.82), transparent 34%),
      linear-gradient(135deg, rgba(140, 160, 255, 0.86), rgba(91, 242, 255, 0.3));
  }

  .phone::after {
    bottom: 18px;
    height: 26%;
    background: rgba(255, 255, 255, 0.06);
  }

  .phone-large {
    width: 240px;
    height: 460px;
    right: 18%;
    top: 54px;
    transform: rotate(-8deg);
  }

  .phone-small {
    width: 180px;
    height: 340px;
    right: 2%;
    top: 124px;
    transform: rotate(10deg);
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 18px;
  }

  .intro,
  .accent-panel,
  .plan {
    padding: 28px;
  }

  .intro ul {
    padding-left: 20px;
    display: grid;
    gap: 14px;
  }

  .accent-panel {
    background:
      radial-gradient(circle at top right, rgba(124, 114, 255, 0.25), transparent 30%),
      rgba(13, 17, 36, 0.72);
  }

  .plans {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 18px;
  }

  .chip {
    width: fit-content;
    padding: 8px 12px;
    border-radius: 999px;
    background: rgba(255, 255, 255, 0.06);
    border: 1px solid rgba(255, 255, 255, 0.08);
    color: #b8c3ff;
    font-size: 13px;
    text-transform: uppercase;
    letter-spacing: 0.08em;
  }

  .showcase {
    grid-template-columns: minmax(0, 1fr) 360px;
    align-items: center;
    padding: 32px;
  }

  .showcase-art {
    min-height: 280px;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
  }

  .showcase-art span {
    border-radius: 22px;
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.14), rgba(255, 255, 255, 0.03)),
      linear-gradient(180deg, #141935, #0c1023);
    border: 1px solid rgba(255, 255, 255, 0.08);
  }

  .showcase-art span:nth-child(2) {
    transform: translateY(28px);
  }

  .contact {
    grid-template-columns: 1fr auto;
    align-items: center;
    padding: 28px 32px;
  }

  .orb {
    position: absolute;
    border-radius: 50%;
    filter: blur(30px);
    opacity: 0.45;
    pointer-events: none;
  }

  .orb-left {
    left: -160px;
    top: 180px;
    width: 420px;
    height: 420px;
    background: rgba(116, 118, 255, 0.42);
  }

  .orb-right {
    right: -160px;
    top: 40px;
    width: 360px;
    height: 360px;
    background: rgba(97, 231, 255, 0.28);
  }

  @media (max-width: 980px) {
    .hero,
    .grid,
    .plans,
    .showcase,
    .contact {
      grid-template-columns: 1fr;
    }

    .hero {
      min-height: auto;
    }

    .hero-art {
      min-height: 360px;
    }
  }

  @media (max-width: 720px) {
    .page-shell {
      padding: 12px;
    }

    .hero,
    .intro,
    .accent-panel,
    .plan,
    .showcase,
    .contact {
      padding: 22px;
    }

    .phone-large {
      width: 190px;
      height: 360px;
      right: 16%;
    }

    .phone-small {
      width: 140px;
      height: 270px;
      right: 0;
    }
  }
</style>
