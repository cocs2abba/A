<p align="center">
  <svg width="600" height="150">
    <defs>
      <!-- Neon glow -->
      <filter id="neonGlow">
        <feGaussianBlur stdDeviation="3.5" result="blur"/>
        <feMerge>
          <feMergeNode in="blur"/>
          <feMergeNode in="SourceGraphic"/>
        </feMerge>
      </filter>

      <!-- Animated gradient -->
      <linearGradient id="cyberGrad" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="
