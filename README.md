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
        <stop offset="0%">
          <animate attributeName="stop-color"
                   values="#00eaff; #ff00f7; #fcee0c; #00eaff"
                   dur="6s" repeatCount="indefinite"/>
        </stop>
        <stop offset="100%">
          <animate attributeName="stop-color"
                   values="#ff00f7; #fcee0c; #00eaff; #ff00f7"
                   dur="6s" repeatCount="indefinite"/>
        </stop>
      </linearGradient>

      <!-- Glitch effect -->
      <filter id="glitch">
        <feTurbulence type="fractalNoise" baseFrequency="0.02" numOctaves="2" result="noise"/>
        <feDisplacementMap in="SourceGraphic" in2="noise" scale="5">
          <animate attributeName="scale"
                   values="3;8;2;6;3"
                   dur="1.2s"
                   repeatCount="indefinite"/>
        </feDisplacementMap>
      </filter>
    </defs>

    <!-- Main neon text -->
    <text x="50%" y="50%" dominant-baseline="middle"
          text-anchor="middle"
          font-size="64"
          font-family="Orbitron, monospace"
          fill="url(#cyberGrad)"
          filter="url(#neonGlow)"
          letter-spacing="10">
      N1H4D
      <animate attributeName="opacity"
               values="1;0.95;1;0.97;1"
               dur="1.8s"
               repeatCount="indefinite"/>
    </text>

    <!-- Glitch overlay -->
    <text x="50%" y="50%" dominant-baseline="middle"
          text-anchor="middle"
          font-size="64"
          font-family="Orbitron, monospace"
          fill="#00eaff"
          filter="url(#glitch)"
          letter-spacing="10"
          opacity="0.35">
      N1H4D
    </text>
  </svg>
</p>
