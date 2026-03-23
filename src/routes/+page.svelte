<script lang="ts">
  import section1 from '../../screencapture-nexorie-bytetown-section_1.png';
  import section2 from '../../screencapture-nexorie-bytetown-section_2.png';
  import section3 from '../../screencapture-nexorie-bytetown-section_3.png';
  import section4 from '../../screencapture-nexorie-bytetown-section_4.png';
  import section5 from '../../screencapture-nexorie-bytetown-section_5.png';
  import section6 from '../../screencapture-nexorie-bytetown-section_6.png';
  import section7 from '../../screencapture-nexorie-bytetown-section_7.png';

  const sections = [
    { src: section1, alt: 'Nexorie hero section with unlocking AI wonders headline' },
    { src: section2, alt: 'AI partner showcase with dual mobile mockups' },
    { src: section3, alt: 'Feature grid explaining what distinguishes the product' },
    { src: section4, alt: 'Product options cards for OF models, influencers, and live dealer' },
    { src: section5, alt: 'Full customization section with AI engine and showcase banner' },
    { src: section6, alt: 'Visuals and imagination section with portraits and device mockups' },
    { src: section7, alt: 'Closing contact section with portrait mosaic and footer' }
  ];
</script>

<svelte:head>
  <title>Nexorie Bytetown</title>
  <meta
    name="description"
    content="A Svelte page rebuilt to closely match the provided Nexorie Bytetown reference screenshots."
  />
</svelte:head>

<div class="page-shell">
  <div class="mesh mesh-left"></div>
  <div class="mesh mesh-right"></div>

  <main class="reference-page">
    {#each sections as section}
      <section class="reference-section">
        <img src={section.src} alt={section.alt} loading="eager" />
      </section>
    {/each}
  </main>
</div>

<style>
  :global(html) {
    background: #0f1226;
  }

  :global(body) {
    margin: 0;
    min-width: 320px;
    font-family:
      Inter,
      "Segoe UI",
      sans-serif;
    background:
      radial-gradient(circle at top, rgba(110, 116, 255, 0.18), transparent 30%),
      linear-gradient(180deg, #30345f 0%, #25284d 18%, #171a35 46%, #111428 100%);
    color: #fff;
  }

  .page-shell {
    position: relative;
    overflow: clip;
    min-height: 100vh;
    padding: 20px 14px 48px;
  }

  .reference-page {
    position: relative;
    z-index: 1;
    width: min(1140px, 100%);
    margin: 0 auto;
  }

  .reference-section {
    position: relative;
    margin: 0;
  }

  .reference-section + .reference-section {
    margin-top: -2px;
  }

  .reference-section img {
    display: block;
    width: 100%;
    height: auto;
    border-radius: 24px;
    box-shadow:
      0 24px 80px rgba(6, 8, 20, 0.34),
      0 0 0 1px rgba(255, 255, 255, 0.07);
  }

  .mesh {
    position: absolute;
    inset: auto;
    pointer-events: none;
    filter: blur(6px);
    opacity: 0.42;
  }

  .mesh::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(circle at center, rgba(182, 192, 255, 0.25), transparent 62%),
      repeating-radial-gradient(
        circle at center,
        transparent 0,
        transparent 26px,
        rgba(196, 206, 255, 0.16) 27px,
        rgba(196, 206, 255, 0.16) 28px
      );
  }

  .mesh-left {
    left: -220px;
    top: 320px;
    width: 620px;
    height: 620px;
  }

  .mesh-right {
    right: -260px;
    top: 40px;
    width: 720px;
    height: 720px;
  }

  @media (max-width: 900px) {
    .page-shell {
      padding: 12px 10px 28px;
    }

    .reference-section img {
      border-radius: 18px;
    }
  }

  @media (max-width: 640px) {
    .page-shell {
      padding-inline: 8px;
    }

    .reference-section img {
      border-radius: 14px;
      box-shadow:
        0 18px 42px rgba(6, 8, 20, 0.28),
        0 0 0 1px rgba(255, 255, 255, 0.05);
    }

    .mesh-left {
      left: -260px;
      top: 200px;
      width: 480px;
      height: 480px;
    }

    .mesh-right {
      right: -280px;
      top: 0;
      width: 520px;
      height: 520px;
    }
  }
</style>
