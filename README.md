<p align="center">
  <svg width="500" height="150">
    <defs>
      <!-- Neon glow -->
      <filter id="neonGlow">
        <feGaussianBlur stdDeviation="4" result="coloredBlur"/>
        <feMerge>
          <feMergeNode in="coloredBlur"/>
          <feMergeNode in="SourceGraphic"/>
        </feMerge>
      </filter>

      <!-- Gradient -->
      <linearGradient id="cyberGrad" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" style="stop-color:#00eaff;" />
        <stop offset="50%" style="
