<!-- Cyberpunk SVG logo for N1H4D -->
<svg width="100%" height="200" viewBox="0 0 600 200"
     xmlns="http://www.w3.org/2000/svg"
     role="img" aria-labelledby="title desc">
  <title id="title">N1H4D Cyberpunk Logo</title>
  <desc id="desc">Animated neon cyberpunk logo for N1H4D</desc>

  <defs>
    <!-- Background gradient -->
    <linearGradient id="bgGradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#020617"/>
      <stop offset="50%" stop-color="#020024"/>
      <stop offset="100%" stop-color="#0f172a"/>
    </linearGradient>

    <!-- Neon text gradient -->
    <linearGradient id="textGradient" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#22d3ee"/>
      <stop offset="50%" stop-color="#a855f7"/>
      <stop offset="100%" stop-color="#f97316"/>
    </linearGradient>

    <!-- Glow filter -->
    <filter id="neonGlow">
      <feGaussianBlur stdDeviation="4" result="blur" />
      <feColorMatrix in="blur" type="matrix"
        values="0 0 0 0 0
                0 0 0 0 1
                0 0 0 0 1
                0 0 0 0.8 0" />
      <feMerge>
        <feMergeNode />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <!-- Scanline mask -->
    <pattern id="scanlines" width="4" height="4" patternUnits="userSpaceOnUse">
      <rect x="0" y="0" width="4" height="2" fill="#000000" opacity="0.4" />
      <rect x="0" y="2" width="4" height="2" fill="#000000" opacity="0" />
    </pattern>
  </defs>

  <style>
    /* Base styling */
    .logo-bg {
      stroke: #22d3ee;
      stroke-width: 2;
      rx: 18;
      ry: 18;
    }

    .border-glow {
      stroke: #22d3ee;
      stroke-width: 2;
      opacity: 0.7;
      filter: url(#neonGlow);
      animation: borderPulse 3s ease-in-out infinite alternate;
    }

    text {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
                   Roboto, sans-serif;
      text-transform: uppercase;
      letter-spacing: 0.6em;
      dominant-baseline: middle;
      text-anchor: middle;
    }

    #text-base {
      fill: none;
      stroke: url(#textGradient);
      stroke-width: 2.5;
      paint-order: stroke;
      stroke-linejoin: round;
      animation: strokeDash 6s linear infinite;
      stroke-dasharray: 500;
      stroke-dashoffset: 500;
    }

    #text-fill {
      fill: url(#textGradient);
      opacity: 0.9;
      animation: flicker 4s infinite;
    }

    /* Offset layers for glitch effect */
    #text-glitch-1,
    #text-glitch-2 {
      fill: none;
      stroke-width: 2.5;
      mix-blend-mode: screen;
    }

    #text-glitch-1 {
      stroke: #f97316;
      animation: glitch1 2.2s infinite;
    }

    #text-glitch-2 {
      stroke: #22d3ee;
      animation: glitch2 1.7s infinite;
    }

    /* Scanline overlay */
    .scan-overlay {
      fill: url(#scanlines);
      animation: scanMove 5s linear infinite;
      pointer-events: none;
    }

    /* Keyframes */
    @keyframes borderPulse {
      0%   { opacity: 0.2; }
      100% { opacity: 0.8; }
    }

    @keyframes strokeDash {
      0%   { stroke-dashoffset: 500; }
      40%  { stroke-dashoffset: 0; }
      100% { stroke-dashoffset: 0; }
    }

    @keyframes flicker {
      0%, 18%, 22%, 25%, 53%, 57%, 100% {
        opacity: 0.95;
      }
      19%, 21%, 24%, 55% {
        opacity: 0.3;
      }
    }

    @keyframes glitch1 {
      0%   { transform: translate(0, 0); opacity: 0.0; }
      5%   { transform: translate(-2px, -1px); opacity: 0.9; }
      10%  { transform: translate(1px, 1px); opacity: 0.4; }
      15%  { transform: translate(-1px, 2px); opacity: 0.8; }
      20%  { transform: translate(0, 0); opacity: 0.0; }
      100% { transform: translate(0, 0); opacity: 0.0; }
    }

    @keyframes glitch2 {
      0%   { transform: translate(0, 0); opacity: 0.0; }
      5%   { transform: translate(2px, 1px); opacity: 0.8; }
      9%   { transform: translate(-1px, -2px); opacity: 0.4; }
      14%  { transform: translate(1px, -1px); opacity: 0.9; }
      20%  { transform: translate(0, 0); opacity: 0.0; }
      100% { transform: translate(0, 0); opacity: 0.0; }
    }

    @keyframes scanMove {
      0%   { transform: translateY(-200px); opacity: 0.0; }
      10%  { opacity: 0.25; }
      50%  { transform: translateY(0px); opacity: 0.15; }
      90%  { opacity: 0.25; }
      100% { transform: translateY(200px); opacity: 0.0; }
    }
  </style>

  <!-- Background card -->
  <rect x="10" y="10" width="580" height="180"
        fill="url(#bgGradient)" class="logo-bg" />
  <rect x="10" y="10" width="580" height="180"
        fill="none" class="border-glow" />

  <!-- Subtle inner border lines -->
  <line x1="40" y1="40" x2="560" y2="40"
        stroke="#22d3ee" stroke-width="1" opacity="0.2" />
  <line x1="40" y1="160" x2="560" y2="160"
        stroke="#a855f7" stroke-width="1" opacity="0.2" />

  <!-- Main text + glitch layers -->
  <g transform="translate(0, 5)">
    <text id="text-base" x="50%" y="50%">N1H4D</text>
    <text id="text-fill" x="50%" y="50%">N1H4D</text>
    <text id="text-glitch-1" x="50%" y="50%">N1H4D</text>
    <text id="text-glitch-2" x="50%" y="50%">N1H4D</text>
  </g>

  <!-- Scanline overlay -->
  <rect class="scan-overlay" x="10" y="10" width="580" height="180" />
</svg>
