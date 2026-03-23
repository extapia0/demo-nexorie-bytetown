<script lang="ts">
  const assets = {
    logo: '/assets/nexorie/logo.svg',
    mesh: '/assets/nexorie/mesh-lines.svg',
    rings: '/assets/nexorie/rings.svg',
    engine: '/assets/nexorie/ai-engine.svg'
  };

  const navLinks = [
    { label: 'About us', href: '#about-us' },
    { label: 'Advantages', href: '#advantages' },
    { label: 'Product options', href: '#product-options' },
    { label: 'Platforms', href: '#platforms' }
  ];

  const advantageCards = [
    {
      title: 'The most advanced AI in the market',
      text: 'Discover our advanced AI technology with unmatched capabilities, intelligence, and adaptability.',
      kind: 'avatars'
    },
    {
      title: 'Stats Matter',
      text: 'Our expertise in marketing and the focus on the bottom line is what differentiates us from any other.',
      kind: 'chart'
    },
    {
      title: 'Never seen before AI abilities',
      text: 'Transform your experience with our AI that creates high-quality pictures, text, and voice messages, mimicking real conversations.',
      kind: 'toggle'
    },
    {
      title: 'Engage your audience everywhere',
      text: 'You do not have to choose, you can engage your audience anywhere, with the flexibility to operate on iOS, Android or web.',
      kind: 'platforms'
    }
  ];

  const productOptions = [
    {
      name: 'AI OF models',
      text: 'We are redefining personal entertainment with AI-powered models for a unique and engaging private experience.',
      copy: 'Dive into a world of unrivaled entertainment as our advanced algorithm adapts to the user preferences, while giving an opportunity to have a private chat with the OF model.',
      variant: 'of'
    },
    {
      name: 'AI IG influencers',
      text: 'Transform social media using artificial intelligence, offering a new way to connect with famous influencers.',
      copy: 'Imagine how influencers can adapt to any preference, making every interaction unique and different using our game changing AI.',
      variant: 'ig'
    },
    {
      name: 'AI live dealer',
      text: 'AI Live Dealer elevates online gaming by blending live casino thrills with advanced artificial intelligence.',
      copy: 'Players will enjoy personalised dealers, stunning live interactions and a real-time experience that will redefine the gaming user experience.',
      variant: 'dealer'
    }
  ];

  const visualPortraits = ['rose', 'pearl', 'mist', 'scarlet'];
  const mosaicColumns = [
    ['pearl', 'ginger', 'cocoa', 'midnight'],
    ['gold', 'berry', 'jade', 'ivory'],
    ['bronze', 'espresso', 'blush'],
    ['copper', 'ash', 'amber'],
    ['pearl', 'onyx', 'lavender'],
    ['midnight', 'cotton', 'bronze', 'cocoa']
  ];
</script>

<svelte:head>
  <title>Nexorie Bytetown</title>
  <meta
    name="description"
    content="Nexorie Bytetown full-page landing with dark futuristic visuals, product sections, and deploy-safe local assets."
  />
</svelte:head>

<div class="page-shell">
  <img class="rings rings-top" src={assets.rings} alt="" aria-hidden="true" />

  <header class="site-nav">
    <a class="brand" href="#top" aria-label="Nexorie home">
      <img src={assets.logo} alt="Nexorie" />
    </a>
    <nav aria-label="Primary">
      {#each navLinks as link}
        <a href={link.href}>{link.label}</a>
      {/each}
    </nav>
    <a class="button button-light contact-button" href="#contact">Contact Us</a>
  </header>

  <main class="page-content">
    <section class="hero section" id="top">
      <div class="hero-glow" aria-hidden="true"></div>
      <h1>Unlocking<br />AI Wonders</h1>

      <div class="hero-visual" aria-hidden="true">
        <div class="hand-silhouette"></div>
        <div class="device hero-phone portrait rose">
          <div class="device-notch"></div>
          <div class="device-status"><span>9:41</span><span>4G</span></div>
          <div class="device-topbar">
            <span class="ghost-dot"></span>
            <strong>Matches</strong>
            <span class="ghost-dot thin"></span>
          </div>
          <div class="device-photo">
            <div class="device-copy">
              <h3>Camila, 21</h3>
              <p>I would be glad to meet a strong and intelligent man.</p>
            </div>
          </div>
          <div class="device-actions"><span>Chat</span><span class="active">Like</span><span>Save</span></div>
        </div>
      </div>

      <img class="mesh mesh-hero" src={assets.mesh} alt="" aria-hidden="true" />
    </section>

    <section class="partner section" id="about-us">
      <div class="section-copy">
        <h2>AI Partner, you haven&apos;t met <span>yet</span></h2>
        <p>Explore our groundbreaking app where your ideas come alive as virtual AI characters.</p>
        <p>We have created incredible characters that interact with you through images, voice and text, showcasing the latest technology.</p>
        <a class="button button-primary" href="#contact">Contact Us</a>
      </div>

      <div class="partner-stack" aria-hidden="true">
        <div class="partner-glow"></div>
        <div class="device chat-list">
          <div class="device-notch"></div>
          <div class="device-status"><span>9:41</span><span>5G</span></div>
          <div class="list-header"><strong>LOVAAI</strong><span class="login-pill">Log In</span></div>
          <div class="chat-items">
            <div><span class="avatar rose"></span><strong>Alexandra</strong></div>
            <div><span class="avatar gold"></span><strong>Camilla</strong></div>
            <div><span class="avatar berry"></span><strong>Maya</strong></div>
            <div><span class="avatar pearl"></span><strong>Barbara</strong></div>
            <div><span class="avatar copper"></span><strong>Ariel</strong></div>
          </div>
        </div>

        <div class="device chat-thread portrait cocoa">
          <div class="device-notch"></div>
          <div class="device-status"><span>9:41</span><span>5G</span></div>
          <div class="thread-header"><span class="ghost-dot"></span><div><strong>Maya</strong><small>Online</small></div></div>
          <div class="thread-body">
            <span class="bubble incoming">Hello, sweetie. How are you feeling today?</span>
            <span class="bubble outgoing">Hey! Today was a hard day at work...</span>
            <span class="bubble incoming">I get it. How would you like to relax?</span>
          </div>
          <div class="thread-input"><span>Message</span><span class="send"></span></div>
        </div>
      </div>
    </section>

    <section class="advantages section" id="advantages">
      <img class="rings rings-section" src={assets.rings} alt="" aria-hidden="true" />
      <div class="section-head center">
        <h2>What distinguishes our <span>product from others</span></h2>
      </div>
      <div class="adv-grid">
        <article class="adv-card adv-main">
          <div class="adv-copy">
            <h3>We create your dream product</h3>
            <p>Tailored to your desires, our product customization abilities bring your dream product to life, ensuring it reflects your uniqueness and desires.</p>
          </div>
          <div class="device-cluster" aria-hidden="true">
            <div class="mini-device tall portrait berry"></div>
            <div class="mini-device center portrait rose"></div>
            <div class="mini-device wide portrait midnight"></div>
          </div>
        </article>

        {#each advantageCards as card}
          <article class={`adv-card ${card.kind}`}>
            {#if card.kind === 'avatars'}
              <div class="avatar-row" aria-hidden="true">
                <span class="avatar berry"></span><span class="avatar espresso"></span><span class="avatar copper"></span><span class="avatar rose"></span><span class="avatar midnight"></span>
              </div>
            {/if}
            {#if card.kind === 'chart'}
              <div class="line-chart" aria-hidden="true"><span class="badge green">112%</span><span class="badge green high">98%</span></div>
            {/if}
            {#if card.kind === 'toggle'}
              <div class="toggle-panel" aria-hidden="true">
                <div><span>Voice messages</span><b></b></div>
                <div><span>Calls</span><b></b></div>
                <div><span>Video messages</span><b></b></div>
              </div>
            {/if}
            {#if card.kind === 'platforms'}
              <div class="platform-row" aria-hidden="true"><span>App</span><span>Play</span><span>Web</span></div>
            {/if}
            <h3>{card.title}</h3>
            <p>{card.text}</p>
          </article>
        {/each}
      </div>
    </section>

    <section class="products section" id="product-options">
      <div class="section-head">
        <h2>Choose your own version of the <span>product</span></h2>
        <p>You can choose not only different product logic and functionality but also stylistics.</p>
      </div>
      <div class="product-list">
        {#each productOptions as option}
          <article class="product-card">
            <div class="product-copy">
              <h3>{option.name}</h3>
              <p>{option.text}</p>
              <p>{option.copy}</p>
              <a class="button button-outline" href="#contact">Choose an option</a>
            </div>
            <div class={`product-art ${option.variant}`} aria-hidden="true">
              <div class="option-screen left"></div>
              <div class="option-screen center"></div>
              <div class="option-screen right"></div>
            </div>
          </article>
        {/each}
      </div>
    </section>

    <section class="visuals section" id="platforms">
      <div class="visual-grid">
        <div class="portrait-grid" aria-hidden="true">
          {#each visualPortraits as tone}
            <div class={`portrait-card portrait ${tone}`}></div>
          {/each}
        </div>
        <div class="visual-copy primary-copy">
          <h2>Stunning <span>visuals, powered by creativity</span></h2>
          <p>We create models from photos, giving virtual characters their own style. From lifelike portraits to imaginative creatures, experience the forefront of innovation.</p>
        </div>
        <div class="visual-copy secondary-copy">
          <h2>Your space, <span>your imagination</span></h2>
          <p>Choose from a mobile app, a web version, or integrated widgets for the latest advancements.</p>
          <p>Engage with characters, control actions, and tell your stories. Traditional boundaries vanish as we embrace limitless innovation.</p>
        </div>
        <div class="dashboard-stage" aria-hidden="true">
          <div class="device dashboard-phone portrait blush"></div>
          <div class="dashboard-screen"><div class="dashboard-toolbar"></div><div class="dashboard-content"></div></div>
        </div>
      </div>
    </section>

    <section class="customization section">
      <div class="section-head split">
        <h2>Full <span>customization</span></h2>
        <p>Tailored to your desires, our product customization abilities bring your dream product to life, ensuring it reflects your uniqueness and desires.</p>
      </div>
      <div class="custom-top">
        <article class="custom-card range-card">
          <strong>PRODUCT RANGE</strong>
          <div class="range-items"><span>Live Dealer</span><span>IG Influencers</span><span>OF Models</span></div>
          <div class="assist-pill">AI ASSISTANTS</div>
        </article>
        <div class="engine-wrap" aria-hidden="true"><img src={assets.engine} alt="" /></div>
        <article class="custom-card payment-card">
          <strong>PAYMENTS</strong>
          <div class="payment-grid">
            <span>Klarna</span><span>Visa</span><span>Mastercard</span><span>G Pay</span><span>Trustly</span><span>PayPal</span><span>Apple Pay</span><span>Stripe</span><span>Coinbase</span><span>Binance</span>
          </div>
        </article>
      </div>
      <article class="welcome-banner">
        <div class="banner-copy">
          <h2>Welcome to the <span>new reality</span></h2>
          <p>Leave a request for feedback and our manager will contact you as soon as possible.</p>
          <a class="button button-light" href="#contact">Contact Us</a>
        </div>
        <div class="banner-visual" aria-hidden="true">
          <div class="banner-portrait portrait berry"></div>
          <div class="device banner-phone portrait copper"></div>
        </div>
      </article>
    </section>

    <section class="final-cta section" id="contact">
      <img class="rings rings-footer" src={assets.rings} alt="" aria-hidden="true" />
      <div class="final-copy">
        <h2>Welcome to the new <span>reality</span></h2>
        <p>Leave a request for feedback and our manager will contact you as soon as possible.</p>
        <a class="button button-light" href="mailto:hello@nexorie.ai">Contact Us</a>
      </div>
      <div class="mosaic" aria-hidden="true">
        {#each mosaicColumns as column}
          <div class="mosaic-column">
            {#each column as tone}
              <div class={`mosaic-card portrait ${tone}`}></div>
            {/each}
          </div>
        {/each}
      </div>
    </section>
  </main>

  <footer class="site-footer">
    <div class="footer-top">
      <a class="brand brand-footer" href="#top" aria-label="Nexorie footer home"><img src={assets.logo} alt="Nexorie" /></a>
      <nav aria-label="Footer">
        {#each navLinks as link}
          <a href={link.href}>{link.label}</a>
        {/each}
      </nav>
    </div>
    <div class="footer-bottom">
      <p>Made by ByteTown</p>
      <div><a href="#top">Cookies Policy</a><a href="#top">Terms and conditions</a></div>
    </div>
  </footer>
</div>

<style>
  :global(html) {
    scroll-behavior: smooth;
    background: #121528;
  }

  :global(body) {
    margin: 0;
    min-width: 320px;
    color: #f8f7ff;
    font-family: "Segoe UI", Aptos, sans-serif;
    background:
      radial-gradient(circle at 50% 12%, rgba(136, 142, 255, 0.22), transparent 22%),
      linear-gradient(180deg, #343760 0%, #2e3158 18%, #1a1e39 44%, #111426 100%);
  }

  :global(*) {
    box-sizing: border-box;
  }

  a {
    color: inherit;
    text-decoration: none;
  }

  img {
    display: block;
    max-width: 100%;
  }

  h1,
  h2,
  h3,
  p {
    margin: 0;
  }

  .page-shell {
    position: relative;
    overflow: clip;
    min-height: 100vh;
    padding: 20px 20px 56px;
  }

  .rings {
    position: absolute;
    pointer-events: none;
    opacity: 0.45;
  }

  .rings-top {
    top: -60px;
    left: 50%;
    width: min(1500px, 112vw);
    transform: translateX(-50%);
  }

  .site-nav,
  .section,
  .site-footer {
    width: min(1480px, 100%);
    margin: 0 auto;
  }

  .site-nav {
    position: sticky;
    top: 16px;
    z-index: 20;
    min-height: 82px;
    padding: 14px 18px;
    border: 1px solid rgba(255, 255, 255, 0.12);
    border-radius: 24px;
    background: rgba(29, 33, 60, 0.82);
    backdrop-filter: blur(14px);
    display: grid;
    grid-template-columns: auto 1fr auto;
    align-items: center;
    gap: 24px;
  }

  .brand img {
    height: 38px;
    width: auto;
  }

  .site-nav nav,
  .footer-top nav,
  .footer-bottom div {
    display: flex;
    align-items: center;
    gap: 22px;
  }

  .site-nav nav {
    justify-content: center;
    flex-wrap: wrap;
  }

  .site-nav nav a,
  .footer-top nav a {
    color: rgba(255, 255, 255, 0.92);
    font-size: 17px;
    font-weight: 600;
  }

  .button {
    min-height: 52px;
    padding: 0 28px;
    border-radius: 18px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-size: 17px;
    font-weight: 700;
    border: 1px solid transparent;
  }

  .button-light {
    background: #ffffff;
    color: #242851;
  }

  .button-primary {
    background: linear-gradient(135deg, #6873ff 0%, #737cff 100%);
    color: #ffffff;
    box-shadow: 0 18px 40px rgba(79, 91, 255, 0.26);
  }

  .button-outline {
    width: fit-content;
    min-height: 42px;
    padding: 0 18px;
    border: 1px solid rgba(49, 61, 132, 0.5);
    color: #303873;
    background: transparent;
  }

  .contact-button {
    min-width: 178px;
  }

  .page-content {
    display: grid;
    gap: 112px;
    margin-top: 26px;
  }

  .section {
    position: relative;
  }

  .hero {
    min-height: 1180px;
    padding: 94px 24px 0;
    display: grid;
    justify-items: center;
    text-align: center;
  }

  .hero-glow {
    position: absolute;
    top: 180px;
    left: 50%;
    width: 760px;
    height: 760px;
    border-radius: 50%;
    transform: translateX(-50%);
    background: radial-gradient(circle, rgba(138, 148, 255, 0.45), rgba(138, 148, 255, 0) 68%);
    filter: blur(24px);
  }

  h1,
  h2 {
    font-weight: 700;
    line-height: 0.96;
    letter-spacing: -0.06em;
  }

  h1 {
    position: relative;
    z-index: 1;
    font-size: clamp(76px, 11vw, 160px);
  }

  h2 {
    font-size: clamp(54px, 7vw, 104px);
  }

  h2 span {
    color: rgba(164, 170, 214, 0.24);
  }

  .hero-visual {
    position: relative;
    z-index: 1;
    width: min(720px, 100%);
    margin-top: 26px;
    min-height: 720px;
  }

  .hand-silhouette {
    position: absolute;
    left: 50%;
    bottom: 34px;
    width: 380px;
    height: 500px;
    transform: translateX(-16%) rotate(8deg);
    border-radius: 160px 160px 100px 120px;
    background:
      linear-gradient(180deg, rgba(106, 63, 36, 0.2), rgba(16, 10, 11, 0.92)),
      radial-gradient(circle at 40% 30%, rgba(92, 55, 34, 0.6), transparent 45%);
    filter: blur(2px);
    opacity: 0.92;
  }

  .mesh {
    position: absolute;
    pointer-events: none;
    opacity: 0.55;
  }

  .mesh-hero {
    bottom: 10px;
    left: 50%;
    width: min(1760px, 124vw);
    transform: translateX(-50%);
  }

  .device {
    position: relative;
    border-radius: 42px;
    border: 1px solid rgba(255, 255, 255, 0.12);
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0.02)),
      linear-gradient(180deg, #121521, #0c0f1a);
    box-shadow:
      0 24px 80px rgba(0, 0, 0, 0.42),
      inset 0 1px 0 rgba(255, 255, 255, 0.08);
    overflow: hidden;
  }

  .device::after {
    content: '';
    position: absolute;
    inset: 8px;
    border-radius: 34px;
    border: 1px solid rgba(255, 255, 255, 0.06);
    pointer-events: none;
  }

  .hero-phone {
    width: 320px;
    height: 620px;
    margin: 0 auto;
  }

  .device-notch {
    position: absolute;
    top: 14px;
    left: 50%;
    width: 118px;
    height: 24px;
    transform: translateX(-50%);
    border-radius: 20px;
    background: rgba(5, 6, 10, 0.92);
    z-index: 2;
  }

  .device-status,
  .device-topbar,
  .device-actions,
  .thread-input,
  .list-header,
  .thread-header {
    position: relative;
    z-index: 1;
    display: flex;
    align-items: center;
  }

  .device-status {
    justify-content: space-between;
    padding: 20px 24px 0;
    font-size: 15px;
    font-weight: 700;
  }

  .device-topbar {
    justify-content: space-between;
    padding: 18px 22px 0;
  }

  .ghost-dot {
    width: 40px;
    height: 40px;
    border-radius: 14px;
    background: rgba(255, 255, 255, 0.12);
  }

  .ghost-dot.thin {
    width: 26px;
  }

  .device-photo {
    position: absolute;
    inset: 98px 18px 104px;
    border-radius: 26px;
    background:
      linear-gradient(180deg, rgba(0, 0, 0, 0.05), rgba(0, 0, 0, 0.44)),
      radial-gradient(circle at 50% 18%, rgba(251, 240, 211, 0.62), transparent 18%),
      radial-gradient(circle at 48% 48%, rgba(247, 204, 174, 0.38), transparent 24%),
      linear-gradient(180deg, rgba(25, 21, 32, 0) 0%, rgba(12, 12, 18, 0.44) 100%);
  }

  .device-copy {
    position: absolute;
    left: 16px;
    right: 16px;
    bottom: 20px;
    display: grid;
    gap: 8px;
    text-align: left;
  }

  .device-copy h3,
  .adv-card h3,
  .product-card h3 {
    font-size: clamp(26px, 2vw, 38px);
    line-height: 1.04;
    letter-spacing: -0.04em;
    font-weight: 700;
  }

  .device-copy p,
  .section-copy p,
  .adv-card p,
  .product-card p,
  .visual-copy p,
  .section-head p,
  .banner-copy p,
  .final-copy p {
    font-size: clamp(18px, 1.6vw, 22px);
    line-height: 1.25;
    color: rgba(244, 244, 255, 0.82);
  }

  .device-actions {
    position: absolute;
    left: 18px;
    right: 18px;
    bottom: 22px;
    min-height: 64px;
    justify-content: space-between;
    padding: 0 18px;
    border-radius: 22px;
    background: rgba(255, 255, 255, 0.1);
    color: rgba(255, 255, 255, 0.78);
    font-size: 14px;
  }

  .device-actions .active {
    width: 62px;
    height: 62px;
    border-radius: 20px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    color: #ffffff;
    background: linear-gradient(180deg, #d77dff, #6a48ff);
  }

  .section-copy {
    max-width: 640px;
    display: grid;
    gap: 22px;
  }

  .partner {
    display: grid;
    grid-template-columns: minmax(320px, 0.88fr) minmax(320px, 1fr);
    gap: 48px;
    align-items: center;
  }

  .partner-stack {
    position: relative;
    min-height: 640px;
  }

  .partner-glow {
    position: absolute;
    inset: 70px 80px 80px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(136, 144, 255, 0.38), rgba(136, 144, 255, 0) 68%);
    filter: blur(20px);
  }

  .chat-list,
  .chat-thread {
    position: absolute;
    width: 330px;
    height: 560px;
  }

  .chat-list {
    right: 150px;
    top: 24px;
  }

  .chat-thread {
    right: 8px;
    top: 108px;
  }

  .list-header,
  .thread-header {
    justify-content: space-between;
    padding: 40px 20px 16px;
  }

  .list-header strong {
    font-size: 28px;
  }

  .login-pill {
    padding: 10px 14px;
    border-radius: 14px;
    background: rgba(255, 255, 255, 0.16);
    font-size: 14px;
    font-weight: 700;
  }

  .chat-items {
    display: grid;
    gap: 12px;
    padding: 10px 18px;
  }

  .chat-items div {
    min-height: 58px;
    padding: 0 14px;
    border-radius: 16px;
    display: flex;
    align-items: center;
    gap: 12px;
    background: rgba(255, 255, 255, 0.08);
  }

  .avatar {
    width: 58px;
    height: 58px;
    border-radius: 50%;
    display: inline-block;
    border: 2px solid rgba(255, 255, 255, 0.7);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.24);
  }

  .thread-header small {
    display: block;
    color: rgba(255, 255, 255, 0.65);
  }

  .thread-body {
    display: grid;
    gap: 14px;
    padding: 180px 14px 0;
  }

  .bubble {
    max-width: 84%;
    padding: 14px 16px;
    border-radius: 18px;
    font-size: 15px;
    line-height: 1.35;
  }

  .incoming {
    background: #e9d4ff;
    color: #1f1830;
  }

  .outgoing {
    margin-left: auto;
    background: rgba(108, 88, 63, 0.66);
    color: #fff5eb;
  }

  .thread-input {
    position: absolute;
    left: 16px;
    right: 16px;
    bottom: 18px;
    min-height: 58px;
    padding: 0 0 0 16px;
    justify-content: space-between;
    border-radius: 18px;
    background: rgba(16, 11, 9, 0.48);
    color: rgba(255, 255, 255, 0.64);
  }

  .send {
    width: 54px;
    height: 54px;
    border-radius: 16px;
    background: linear-gradient(180deg, #ca73ff, #6d48ff);
  }

  .section-head {
    max-width: 920px;
    display: grid;
    gap: 16px;
  }

  .section-head.center {
    margin: 0 auto 28px;
    text-align: center;
    justify-items: center;
  }

  .advantages {
    padding-top: 20px;
  }

  .rings-section {
    top: -120px;
    left: 50%;
    width: min(1460px, 108vw);
    transform: translateX(-50%);
  }

  .adv-grid {
    position: relative;
    z-index: 1;
    display: grid;
    grid-template-columns: 1.6fr 1fr 1fr;
    gap: 18px;
  }

  .adv-card {
    min-height: 320px;
    padding: 28px;
    border-radius: 30px;
    background: rgba(53, 57, 100, 0.86);
    border: 1px solid rgba(255, 255, 255, 0.08);
    display: grid;
    align-content: start;
    gap: 18px;
    box-shadow: 0 22px 60px rgba(0, 0, 0, 0.2);
  }

  .adv-main {
    grid-row: span 2;
    background: linear-gradient(180deg, #90a4ff 0%, #7480d2 100%);
  }

  .adv-main p,
  .adv-main h3 {
    color: #ffffff;
  }

  .device-cluster {
    position: relative;
    min-height: 420px;
    margin-top: auto;
  }

  .mini-device {
    position: absolute;
    bottom: -18px;
    border-radius: 24px;
    border: 1px solid rgba(255, 255, 255, 0.14);
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.14), rgba(255, 255, 255, 0.02)),
      linear-gradient(180deg, #121521, #090b14);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.28);
  }

  .mini-device.tall {
    left: 40px;
    width: 180px;
    height: 320px;
  }

  .mini-device.center {
    left: 210px;
    width: 210px;
    height: 390px;
    z-index: 2;
  }

  .mini-device.wide {
    right: 34px;
    width: 260px;
    height: 320px;
  }

  .avatar-row,
  .platform-row {
    display: flex;
    align-items: center;
    gap: 10px;
    flex-wrap: wrap;
  }

  .line-chart {
    position: relative;
    min-height: 122px;
    border-radius: 22px;
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0)),
      linear-gradient(135deg, rgba(157, 131, 255, 0.46), rgba(128, 132, 255, 0.08));
    overflow: hidden;
  }

  .line-chart::before {
    content: '';
    position: absolute;
    inset: 24px 20px 20px;
    border-top: 4px solid #998ef5;
    border-right: 4px solid #998ef5;
    border-radius: 90px;
    transform: skewX(-18deg);
    opacity: 0.95;
  }

  .badge {
    position: absolute;
    top: 54px;
    left: 42px;
    padding: 8px 12px;
    border-radius: 14px;
    background: rgba(11, 14, 18, 0.88);
    color: #fff;
    font-size: 14px;
    font-weight: 700;
  }

  .badge.green::before {
    content: '▲';
    margin-right: 6px;
    color: #4ce48a;
  }

  .badge.high {
    top: 22px;
    left: auto;
    right: 30px;
  }

  .toggle-panel {
    display: grid;
    gap: 10px;
    padding: 14px;
    border-radius: 22px;
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0.02)),
      rgba(63, 66, 118, 0.52);
  }

  .toggle-panel div {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
  }

  .toggle-panel b {
    width: 44px;
    height: 24px;
    border-radius: 999px;
    background: linear-gradient(90deg, #3ccb7c 0%, #6df3a4 100%);
  }

  .platform-row span {
    min-width: 82px;
    min-height: 68px;
    padding: 0 14px;
    border-radius: 22px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
    font-weight: 700;
    background: rgba(255, 255, 255, 0.1);
  }

  .products {
    display: grid;
    gap: 26px;
  }

  .product-list {
    display: grid;
    gap: 30px;
  }

  .product-card {
    min-height: 430px;
    padding: 42px 40px;
    border-radius: 38px;
    background: rgba(255, 255, 255, 0.96);
    color: #26305f;
    display: grid;
    grid-template-columns: minmax(300px, 0.86fr) minmax(320px, 1fr);
    gap: 28px;
    overflow: hidden;
    box-shadow: 0 24px 60px rgba(0, 0, 0, 0.18);
  }

  .product-copy {
    display: grid;
    align-content: start;
    gap: 18px;
  }

  .product-copy p {
    color: rgba(48, 56, 115, 0.88);
  }

  .product-art {
    position: relative;
    min-height: 320px;
  }

  .option-screen {
    position: absolute;
    bottom: -24px;
    width: 200px;
    border-radius: 28px;
    border: 1px solid rgba(27, 34, 72, 0.16);
    box-shadow: 0 18px 36px rgba(26, 29, 64, 0.14);
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.24), rgba(255, 255, 255, 0)),
      linear-gradient(180deg, #ffffff, #eef1ff);
  }

  .option-screen.left {
    left: 48px;
    width: 190px;
    height: 320px;
  }

  .option-screen.center {
    left: 210px;
    width: 230px;
    height: 390px;
    z-index: 2;
  }

  .option-screen.right {
    right: 24px;
    width: 220px;
    height: 340px;
  }

  .of .option-screen {
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.22), rgba(255, 255, 255, 0)),
      linear-gradient(180deg, #fff7f7, #edf2ff);
  }

  .ig .option-screen {
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.22), rgba(255, 255, 255, 0)),
      linear-gradient(180deg, #131720, #2a3048);
  }

  .dealer .option-screen {
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.22), rgba(255, 255, 255, 0)),
      linear-gradient(180deg, #15171f, #2c2536);
  }

  .visual-grid {
    display: grid;
    grid-template-columns: 420px 1fr;
    gap: 34px 56px;
    align-items: start;
  }

  .portrait-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 14px;
  }

  .portrait-card {
    min-height: 250px;
    border-radius: 28px;
    border: 1px solid rgba(255, 255, 255, 0.12);
    box-shadow: 0 20px 50px rgba(0, 0, 0, 0.18);
  }

  .visual-copy {
    display: grid;
    gap: 18px;
  }

  .primary-copy {
    align-self: center;
  }

  .dashboard-stage {
    position: relative;
    grid-column: 2;
    min-height: 430px;
  }

  .dashboard-screen {
    position: absolute;
    right: 0;
    bottom: 0;
    width: min(780px, 100%);
    height: 360px;
    border-radius: 34px;
    border: 1px solid rgba(255, 255, 255, 0.12);
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.12), rgba(255, 255, 255, 0.02)),
      linear-gradient(180deg, #eef1fb, #d7ddf4);
    box-shadow: 0 24px 64px rgba(0, 0, 0, 0.22);
  }

  .dashboard-toolbar {
    height: 48px;
    margin: 16px 18px 0;
    border-radius: 14px;
    background: rgba(255, 255, 255, 0.9);
  }

  .dashboard-content {
    position: absolute;
    left: 18px;
    right: 18px;
    top: 82px;
    bottom: 18px;
    border-radius: 22px;
    background:
      linear-gradient(180deg, rgba(126, 132, 255, 0.14), rgba(248, 122, 162, 0.12)),
      rgba(255, 255, 255, 0.84);
  }

  .dashboard-phone {
    position: absolute;
    left: 22px;
    bottom: -4px;
    width: 168px;
    height: 320px;
    z-index: 2;
  }

  .customization {
    display: grid;
    gap: 28px;
  }

  .section-head.split {
    max-width: none;
    grid-template-columns: minmax(320px, 1fr) minmax(320px, 0.92fr);
    align-items: start;
  }

  .custom-top {
    display: grid;
    grid-template-columns: minmax(260px, 1fr) auto minmax(260px, 1fr);
    gap: 26px;
    align-items: center;
  }

  .custom-card {
    min-height: 260px;
    padding: 24px 26px;
    border-radius: 34px;
    background:
      linear-gradient(180deg, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0.02)),
      rgba(72, 77, 129, 0.56);
    border: 1px solid rgba(255, 255, 255, 0.08);
    display: grid;
    gap: 18px;
    box-shadow: 0 20px 48px rgba(0, 0, 0, 0.18);
  }

  .custom-card strong {
    font-size: 22px;
    text-align: center;
  }

  .range-items {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 12px;
  }

  .range-items span,
  .payment-grid span,
  .assist-pill {
    min-height: 54px;
    padding: 0 14px;
    border-radius: 16px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    font-weight: 700;
    background: rgba(255, 255, 255, 0.92);
    color: #343d76;
  }

  .assist-pill {
    width: fit-content;
    margin: auto;
    padding-inline: 18px;
    background: rgba(238, 241, 255, 0.94);
  }

  .engine-wrap {
    position: relative;
    display: grid;
    place-items: center;
  }

  .engine-wrap::before,
  .engine-wrap::after {
    content: '';
    position: absolute;
    top: 50%;
    width: 180px;
    height: 2px;
    transform: translateY(-50%);
    background: linear-gradient(90deg, rgba(255, 255, 255, 0.2), rgba(255, 255, 255, 0.7));
  }

  .engine-wrap::before {
    right: 100%;
    margin-right: 18px;
  }

  .engine-wrap::after {
    left: 100%;
    margin-left: 18px;
  }

  .payment-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 12px;
  }

  .welcome-banner {
    min-height: 540px;
    padding: 40px 46px;
    border-radius: 40px;
    display: grid;
    grid-template-columns: minmax(320px, 0.76fr) minmax(320px, 1fr);
    gap: 30px;
    overflow: hidden;
    background:
      linear-gradient(180deg, rgba(154, 165, 255, 0.14), rgba(110, 88, 255, 0.1)),
      rgba(70, 74, 122, 0.56);
    border: 1px solid rgba(255, 255, 255, 0.08);
    box-shadow: 0 22px 68px rgba(0, 0, 0, 0.22);
  }

  .banner-copy {
    position: relative;
    z-index: 1;
    display: grid;
    align-content: center;
    gap: 18px;
  }

  .banner-visual {
    position: relative;
    min-height: 430px;
  }

  .banner-portrait {
    position: absolute;
    inset: 0 0 0 40px;
    border-radius: 34px;
    opacity: 0.96;
  }

  .banner-phone {
    position: absolute;
    right: 28px;
    bottom: -12px;
    width: 200px;
    height: 390px;
  }

  .final-cta {
    padding-top: 28px;
    display: grid;
    justify-items: center;
    text-align: center;
  }

  .rings-footer {
    top: -120px;
    left: 50%;
    width: min(1500px, 110vw);
    transform: translateX(-50%);
  }

  .final-copy {
    position: relative;
    z-index: 1;
    max-width: 940px;
    display: grid;
    justify-items: center;
    gap: 20px;
  }

  .mosaic {
    position: relative;
    z-index: 1;
    width: 100%;
    margin-top: 36px;
    display: grid;
    grid-template-columns: repeat(6, minmax(0, 1fr));
    gap: 18px;
    align-items: end;
  }

  .mosaic-column {
    display: grid;
    gap: 18px;
    align-content: end;
  }

  .mosaic-card {
    min-height: 180px;
    border-radius: 28px;
    border: 1px solid rgba(255, 255, 255, 0.12);
    box-shadow: 0 18px 42px rgba(0, 0, 0, 0.16);
  }

  .site-footer {
    margin-top: 28px;
    padding-top: 28px;
    border-top: 1px solid rgba(255, 255, 255, 0.16);
    display: grid;
    gap: 26px;
  }

  .footer-top,
  .footer-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
  }

  .footer-top {
    flex-wrap: wrap;
  }

  .footer-bottom {
    color: rgba(255, 255, 255, 0.86);
    font-size: 16px;
  }

  .brand-footer img {
    height: 32px;
  }

  .portrait.rose,
  .avatar.rose {
    background:
      radial-gradient(circle at 50% 28%, rgba(255, 227, 190, 0.82), transparent 18%),
      radial-gradient(circle at 50% 54%, rgba(224, 174, 158, 0.54), transparent 24%),
      linear-gradient(180deg, #3c2f44 0%, #18131c 100%);
  }

  .portrait.cocoa,
  .avatar.cocoa {
    background:
      radial-gradient(circle at 48% 26%, rgba(214, 176, 142, 0.82), transparent 16%),
      radial-gradient(circle at 50% 54%, rgba(101, 61, 45, 0.56), transparent 26%),
      linear-gradient(180deg, #34211f 0%, #111117 100%);
  }

  .portrait.berry,
  .avatar.berry {
    background:
      radial-gradient(circle at 52% 22%, rgba(239, 213, 192, 0.82), transparent 16%),
      radial-gradient(circle at 48% 54%, rgba(181, 76, 112, 0.54), transparent 25%),
      linear-gradient(180deg, #45263a 0%, #12131d 100%);
  }

  .portrait.pearl,
  .avatar.pearl {
    background:
      radial-gradient(circle at 48% 24%, rgba(255, 234, 217, 0.88), transparent 17%),
      radial-gradient(circle at 50% 54%, rgba(195, 160, 145, 0.48), transparent 24%),
      linear-gradient(180deg, #5a4d50 0%, #1b1820 100%);
  }

  .portrait.scarlet,
  .avatar.scarlet {
    background:
      radial-gradient(circle at 50% 24%, rgba(255, 238, 226, 0.82), transparent 17%),
      radial-gradient(circle at 54% 58%, rgba(209, 75, 64, 0.6), transparent 26%),
      linear-gradient(180deg, #4e2635 0%, #1c1a24 100%);
  }

  .portrait.mist,
  .avatar.mist {
    background:
      radial-gradient(circle at 50% 22%, rgba(255, 234, 220, 0.84), transparent 17%),
      radial-gradient(circle at 50% 56%, rgba(129, 189, 235, 0.48), transparent 25%),
      linear-gradient(180deg, #495b6a 0%, #171a23 100%);
  }

  .portrait.midnight,
  .avatar.midnight {
    background:
      radial-gradient(circle at 50% 24%, rgba(229, 200, 188, 0.82), transparent 17%),
      radial-gradient(circle at 50% 58%, rgba(68, 82, 179, 0.54), transparent 26%),
      linear-gradient(180deg, #242842 0%, #10131d 100%);
  }

  .portrait.gold,
  .avatar.gold {
    background:
      radial-gradient(circle at 50% 22%, rgba(251, 229, 191, 0.88), transparent 17%),
      radial-gradient(circle at 48% 58%, rgba(210, 162, 82, 0.52), transparent 26%),
      linear-gradient(180deg, #5f4728 0%, #1c1a1a 100%);
  }

  .portrait.espresso,
  .avatar.espresso {
    background:
      radial-gradient(circle at 48% 23%, rgba(214, 173, 145, 0.82), transparent 17%),
      radial-gradient(circle at 52% 58%, rgba(103, 68, 47, 0.58), transparent 26%),
      linear-gradient(180deg, #49362d 0%, #17161b 100%);
  }

  .portrait.copper,
  .avatar.copper {
    background:
      radial-gradient(circle at 50% 22%, rgba(241, 214, 197, 0.86), transparent 16%),
      radial-gradient(circle at 50% 58%, rgba(196, 103, 70, 0.5), transparent 25%),
      linear-gradient(180deg, #5c3328 0%, #191a22 100%);
  }

  .portrait.ivory,
  .avatar.ivory {
    background:
      radial-gradient(circle at 50% 22%, rgba(255, 235, 219, 0.9), transparent 16%),
      radial-gradient(circle at 48% 58%, rgba(207, 187, 157, 0.46), transparent 25%),
      linear-gradient(180deg, #8c7f77 0%, #20202a 100%);
  }

  .portrait.amber,
  .avatar.amber {
    background:
      radial-gradient(circle at 48% 23%, rgba(255, 232, 211, 0.82), transparent 16%),
      radial-gradient(circle at 54% 58%, rgba(217, 126, 65, 0.56), transparent 26%),
      linear-gradient(180deg, #6c4630 0%, #1c1b23 100%);
  }

  .portrait.onyx,
  .avatar.onyx {
    background:
      radial-gradient(circle at 50% 23%, rgba(212, 175, 158, 0.78), transparent 16%),
      radial-gradient(circle at 50% 58%, rgba(44, 44, 50, 0.52), transparent 25%),
      linear-gradient(180deg, #27242d 0%, #111118 100%);
  }

  .portrait.ginger,
  .avatar.ginger {
    background:
      radial-gradient(circle at 48% 22%, rgba(255, 227, 208, 0.84), transparent 17%),
      radial-gradient(circle at 52% 56%, rgba(214, 116, 68, 0.56), transparent 26%),
      linear-gradient(180deg, #7a422f 0%, #1b1820 100%);
  }

  .portrait.jade,
  .avatar.jade {
    background:
      radial-gradient(circle at 48% 22%, rgba(255, 232, 219, 0.82), transparent 16%),
      radial-gradient(circle at 52% 58%, rgba(83, 170, 146, 0.5), transparent 26%),
      linear-gradient(180deg, #31584d 0%, #17181e 100%);
  }

  .portrait.bronze,
  .avatar.bronze {
    background:
      radial-gradient(circle at 50% 22%, rgba(255, 232, 204, 0.84), transparent 17%),
      radial-gradient(circle at 48% 57%, rgba(173, 122, 84, 0.54), transparent 26%),
      linear-gradient(180deg, #62473b 0%, #1b1820 100%);
  }

  .portrait.ash,
  .avatar.ash {
    background:
      radial-gradient(circle at 48% 22%, rgba(249, 232, 219, 0.84), transparent 16%),
      radial-gradient(circle at 52% 57%, rgba(160, 145, 154, 0.46), transparent 24%),
      linear-gradient(180deg, #5f5b66 0%, #1b1b23 100%);
  }

  .portrait.blush,
  .avatar.blush {
    background:
      radial-gradient(circle at 50% 22%, rgba(255, 236, 228, 0.9), transparent 16%),
      radial-gradient(circle at 48% 58%, rgba(239, 157, 146, 0.46), transparent 24%),
      linear-gradient(180deg, #87666b 0%, #1f1f26 100%);
  }

  .portrait.cotton,
  .avatar.cotton {
    background:
      radial-gradient(circle at 50% 23%, rgba(255, 237, 223, 0.88), transparent 16%),
      radial-gradient(circle at 48% 58%, rgba(212, 195, 180, 0.42), transparent 24%),
      linear-gradient(180deg, #92847e 0%, #20212a 100%);
  }

  @media (max-width: 1200px) {
    .site-nav {
      grid-template-columns: 1fr auto;
    }

    .site-nav nav {
      display: none;
    }

    .partner,
    .product-card,
    .welcome-banner,
    .section-head.split,
    .custom-top,
    .visual-grid {
      grid-template-columns: 1fr;
    }

    .adv-grid {
      grid-template-columns: 1fr 1fr;
    }

    .adv-main {
      grid-column: 1 / -1;
      grid-row: auto;
    }

    .dashboard-stage {
      grid-column: auto;
    }

    .engine-wrap::before,
    .engine-wrap::after {
      display: none;
    }

    .mosaic {
      grid-template-columns: repeat(3, minmax(0, 1fr));
    }
  }

  @media (max-width: 820px) {
    .page-shell {
      padding: 10px 10px 34px;
    }

    .site-nav {
      min-height: 64px;
      padding: 10px 12px;
      border-radius: 18px;
    }

    .brand img {
      height: 24px;
    }

    .contact-button {
      min-width: 92px;
      min-height: 34px;
      padding: 0 14px;
      border-radius: 10px;
      font-size: 12px;
    }

    .page-content {
      gap: 72px;
      margin-top: 14px;
    }

    .hero {
      min-height: 700px;
      padding: 24px 14px 0;
    }

    h1 {
      font-size: clamp(60px, 14vw, 86px);
    }

    h2 {
      font-size: clamp(42px, 9vw, 68px);
    }

    .hero-visual {
      min-height: 450px;
    }

    .hero-phone {
      width: 210px;
      height: 404px;
    }

    .hand-silhouette {
      width: 230px;
      height: 320px;
      bottom: 10px;
    }

    .device-notch {
      width: 84px;
      height: 18px;
    }

    .device-status {
      padding: 18px 18px 0;
      font-size: 11px;
    }

    .device-topbar {
      padding: 12px 14px 0;
    }

    .ghost-dot {
      width: 28px;
      height: 28px;
      border-radius: 10px;
    }

    .device-photo {
      inset: 74px 12px 74px;
      border-radius: 18px;
    }

    .device-copy h3,
    .adv-card h3,
    .product-card h3 {
      font-size: 24px;
    }

    .device-copy p,
    .section-copy p,
    .adv-card p,
    .product-card p,
    .visual-copy p,
    .section-head p,
    .banner-copy p,
    .final-copy p {
      font-size: 16px;
    }

    .device-actions {
      left: 12px;
      right: 12px;
      bottom: 14px;
      min-height: 46px;
      padding: 0 12px;
      font-size: 11px;
    }

    .device-actions .active {
      width: 44px;
      height: 44px;
      border-radius: 14px;
    }

    .partner-stack {
      min-height: 480px;
    }

    .chat-list,
    .chat-thread {
      width: 210px;
      height: 360px;
      border-radius: 28px;
    }

    .chat-list {
      right: 98px;
      top: 22px;
    }

    .chat-thread {
      right: 0;
      top: 76px;
    }

    .list-header,
    .thread-header {
      padding: 28px 12px 12px;
    }

    .list-header strong {
      font-size: 18px;
    }

    .login-pill {
      padding: 7px 10px;
      font-size: 10px;
    }

    .chat-items {
      gap: 8px;
      padding: 8px 10px;
    }

    .chat-items div {
      min-height: 40px;
      padding: 0 10px;
      border-radius: 12px;
      font-size: 11px;
    }

    .avatar {
      width: 34px;
      height: 34px;
    }

    .thread-body {
      gap: 8px;
      padding: 112px 10px 0;
    }

    .bubble {
      padding: 10px 12px;
      border-radius: 14px;
      font-size: 11px;
    }

    .thread-input {
      left: 10px;
      right: 10px;
      bottom: 12px;
      min-height: 42px;
      border-radius: 14px;
      font-size: 11px;
    }

    .send {
      width: 38px;
      height: 38px;
      border-radius: 12px;
    }

    .adv-grid,
    .payment-grid,
    .mosaic {
      grid-template-columns: 1fr;
    }

    .adv-card,
    .product-card,
    .custom-card,
    .welcome-banner {
      border-radius: 24px;
    }

    .adv-card {
      min-height: auto;
      padding: 20px;
    }

    .device-cluster {
      min-height: 230px;
    }

    .mini-device.tall {
      left: 12px;
      width: 100px;
      height: 170px;
    }

    .mini-device.center {
      left: 106px;
      width: 120px;
      height: 220px;
    }

    .mini-device.wide {
      right: 8px;
      width: 136px;
      height: 180px;
    }

    .product-card {
      min-height: auto;
      padding: 22px;
    }

    .product-art {
      min-height: 220px;
    }

    .option-screen.left {
      left: 8px;
      width: 96px;
      height: 160px;
    }

    .option-screen.center {
      left: 84px;
      width: 116px;
      height: 214px;
    }

    .option-screen.right {
      right: 4px;
      width: 106px;
      height: 170px;
    }

    .visual-grid {
      gap: 24px;
    }

    .portrait-grid {
      max-width: 320px;
    }

    .portrait-card {
      min-height: 136px;
      border-radius: 18px;
    }

    .dashboard-stage {
      min-height: 240px;
    }

    .dashboard-screen {
      height: 180px;
      border-radius: 20px;
    }

    .dashboard-phone {
      width: 92px;
      height: 178px;
    }

    .custom-top {
      gap: 18px;
    }

    .custom-card {
      min-height: auto;
      padding: 18px;
    }

    .range-items {
      grid-template-columns: 1fr;
    }

    .payment-grid {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .welcome-banner {
      min-height: auto;
      padding: 24px;
    }

    .banner-visual {
      min-height: 280px;
    }

    .banner-portrait {
      inset: 0;
      border-radius: 20px;
    }

    .banner-phone {
      right: 10px;
      width: 130px;
      height: 250px;
    }

    .final-cta {
      overflow: hidden;
    }

    .mosaic {
      gap: 10px;
    }

    .mosaic-column {
      display: contents;
    }

    .mosaic-card {
      min-height: 120px;
      border-radius: 18px;
    }

    .footer-top,
    .footer-bottom,
    .footer-bottom div {
      display: grid;
      gap: 12px;
      justify-content: start;
    }

    .footer-top nav {
      flex-wrap: wrap;
      gap: 12px 18px;
    }

    .footer-bottom {
      font-size: 14px;
    }
  }
</style>
