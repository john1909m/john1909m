<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1180 610" width="1180" height="610">
  <defs>
    <!-- Dark Mode Gradients -->
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#030712"/>
      <stop offset="100%" stop-color="#0F172A"/>
    </linearGradient>

    <radialGradient id="glow1" cx="20%" cy="30%" r="50%">
      <stop offset="0%" stop-color="#7C3AED" stop-opacity="0.15"/>
      <stop offset="100%" stop-color="#7C3AED" stop-opacity="0"/>
    </radialGradient>

    <radialGradient id="glow2" cx="80%" cy="70%" r="50%">
      <stop offset="0%" stop-color="#22D3EE" stop-opacity="0.1"/>
      <stop offset="100%" stop-color="#22D3EE" stop-opacity="0"/>
    </radialGradient>

    <radialGradient id="glow3" cx="50%" cy="50%" r="40%">
      <stop offset="0%" stop-color="#10B981" stop-opacity="0.08"/>
      <stop offset="100%" stop-color="#10B981" stop-opacity="0"/>
    </radialGradient>

    <linearGradient id="accentGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#7C3AED"/>
      <stop offset="50%" stop-color="#22D3EE"/>
      <stop offset="100%" stop-color="#10B981"/>
      <animate attributeName="x1" values="0%;100%;0%" dur="8s" repeatCount="indefinite"/>
      <animate attributeName="y1" values="0%;100%;0%" dur="8s" repeatCount="indefinite"/>
    </linearGradient>

    <linearGradient id="asciiGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#7C3AED"/>
      <stop offset="50%" stop-color="#22D3EE"/>
      <stop offset="100%" stop-color="#7C3AED"/>
      <animate attributeName="x1" values="0%;100%;0%" dur="6s" repeatCount="indefinite"/>
      <animate attributeName="y1" values="0%;100%;0%" dur="6s" repeatCount="indefinite"/>
    </linearGradient>

    <linearGradient id="borderGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="rgba(255,255,255,0)"/>
      <stop offset="30%" stop-color="rgba(255,255,255,0.08)"/>
      <stop offset="50%" stop-color="rgba(124,58,237,0.3)"/>
      <stop offset="70%" stop-color="rgba(34,211,238,0.3)"/>
      <stop offset="100%" stop-color="rgba(255,255,255,0)"/>
      <animate attributeName="x1" values="-100%;200%" dur="6s" repeatCount="indefinite"/>
    </linearGradient>

    <radialGradient id="particleGlow" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#22D3EE" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#22D3EE" stop-opacity="0"/>
    </radialGradient>

    <radialGradient id="pulseGlow" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#7C3AED" stop-opacity="0.3"/>
      <stop offset="100%" stop-color="#7C3AED" stop-opacity="0"/>
      <animate attributeName="r" values="30%;70%;30%" dur="3s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.3;0.1;0.3" dur="3s" repeatCount="indefinite"/>
    </radialGradient>

    <!-- Filters -->
    <filter id="glass" x="-10%" y="-10%" width="120%" height="120%">
      <feGaussianBlur in="SourceGraphic" stdDeviation="0.5"/>
      <feComponentTransfer>
        <feFuncA type="linear" slope="1.2"/>
      </feComponentTransfer>
    </filter>

    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <filter id="softGlow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="8"/>
    </filter>

    <filter id="noise">
      <feTurbulence type="fractalNoise" baseFrequency="0.8" numOctaves="3" stitchTiles="stitch"/>
      <feColorMatrix type="matrix" values="1 0 0 0 0 0 1 0 0 0 0 0 1 0 0 0 0 0 0.03 0"/>
    </filter>

    <!-- Clip Paths -->
    <clipPath id="roundedClip">
      <rect width="1180" height="610" rx="16"/>
    </clipPath>

    <clipPath id="leftPanel">
      <rect x="24" y="24" width="430" height="562" rx="12"/>
    </clipPath>

    <clipPath id="rightPanel">
      <rect x="474" y="24" width="682" height="562" rx="12"/>
    </clipPath>

    <!-- ASCII Art -->
    <style>
      .ascii-line {
        font-family: 'Courier New', monospace;
        font-size: 7px;
        fill: url(#asciiGrad);
        opacity: 0;
        animation: fadeIn 0.3s forwards;
        animation-delay: calc(var(--i) * 0.1s);
      }
      @keyframes fadeIn {
        to { opacity: 1; }
      }
      @keyframes blink {
        0%, 50% { opacity: 1; }
        51%, 100% { opacity: 0; }
      }
      @keyframes float {
        0%, 100% { transform: translateY(0); }
        50% { transform: translateY(-4px); }
      }
      @keyframes pulse {
        0%, 100% { opacity: 0.4; transform: scale(1); }
        50% { opacity: 0.8; transform: scale(1.05); }
      }
      @keyframes scanline {
        0% { transform: translateY(-100%); }
        100% { transform: translateY(200%); }
      }
      @keyframes shimmer {
        0% { transform: translateX(-100%) rotate(0deg); }
        100% { transform: translateX(100%) rotate(0deg); }
      }
      @keyframes typeCursor {
        0%, 50% { opacity: 1; }
        51%, 100% { opacity: 0; }
      }
      .cursor-blink {
        animation: blink 1s step-end infinite;
      }
      .typing-cursor {
        animation: typeCursor 1s step-end infinite;
      }
      .float-anim {
        animation: float 3s ease-in-out infinite;
      }
      .pulse-anim {
        animation: pulse 2s ease-in-out infinite;
      }
    </style>
  </defs>

  <!-- Background -->
  <g clip-path="url(#roundedClip)">
    <rect width="1180" height="610" fill="url(#bgGrad)"/>
    
    <!-- Glow Effects -->
    <rect width="1180" height="610" fill="url(#glow1)"/>
    <rect width="1180" height="610" fill="url(#glow2)"/>
    <rect width="1180" height="610" fill="url(#glow3)"/>

    <!-- Noise Texture -->
    <rect width="1180" height="610" filter="url(#noise)" opacity="0.5"/>

    <!-- Scanline -->
    <rect x="0" y="-100%" width="1180" height="2" fill="url(#asciiGrad)" opacity="0.05">
      <animate attributeName="y" values="-100%;200%" dur="4s" repeatCount="indefinite"/>
    </rect>

    <!-- Left Panel -->
    <rect x="24" y="24" width="430" height="562" rx="12" fill="#0F172A" opacity="0.8" stroke="rgba(255,255,255,0.06)" stroke-width="1.5"/>
    <rect x="24" y="24" width="430" height="562" rx="12" fill="url(#pulseGlow)" opacity="0.3"/>
    
    <!-- Border Shimmer -->
    <rect x="24" y="24" width="430" height="562" rx="12" fill="none" stroke="url(#borderGrad)" stroke-width="1.5">
      <animate attributeName="opacity" values="0.3;0.7;0.3" dur="4s" repeatCount="indefinite"/>
    </rect>

    <!-- Left Panel Content - ASCII Art -->
    <g transform="translate(50, 60)">
      <g class="float-anim">
        <!-- ASCII Art Lines -->
        <text x="0" y="20" class="ascii-line" style="--i:0;">    ██████╗ ███████╗██╗   ██╗███████╗██╗      ██████╗ ██████╗ ███████╗██████╗ </text>
        <text x="0" y="30" class="ascii-line" style="--i:1;">    ██╔══██╗██╔════╝██║   ██║██╔════╝██║     ██╔═══██╗██╔══██╗██╔════╝██╔══██╗</text>
        <text x="0" y="40" class="ascii-line" style="--i:2;">    ██████╔╝█████╗  ██║   ██║█████╗  ██║     ██║   ██║██████╔╝█████╗  ██████╔╝</text>
        <text x="0" y="50" class="ascii-line" style="--i:3;">    ██╔══██╗██╔══╝  ╚██╗ ██╔╝██╔══╝  ██║     ██║   ██║██╔══██╗██╔══╝  ██╔══██╗</text>
        <text x="0" y="60" class="ascii-line" style="--i:4;">    ██████╔╝███████╗ ╚████╔╝ ███████╗███████╗╚██████╔╝██║  ██║███████╗██║  ██║</text>
        <text x="0" y="70" class="ascii-line" style="--i:5;">    ╚═════╝ ╚══════╝  ╚═══╝  ╚══════╝╚══════╝ ╚═════╝ ╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝</text>
        
        <!-- Terminal cursor -->
        <rect x="140" y="80" width="8" height="8" fill="#22D3EE" opacity="0.8" class="cursor-blink"/>
      </g>
    </g>

    <!-- Right Panel -->
    <rect x="474" y="24" width="682" height="562" rx="12" fill="#0F172A" opacity="0.8" stroke="rgba(255,255,255,0.06)" stroke-width="1.5"/>
    <rect x="474" y="24" width="682" height="562" rx="12" fill="url(#pulseGlow)" opacity="0.2"/>
    
    <!-- Border Shimmer -->
    <rect x="474" y="24" width="682" height="562" rx="12" fill="none" stroke="url(#borderGrad)" stroke-width="1.5">
      <animate attributeName="opacity" values="0.3;0.7;0.3" dur="4s" repeatCount="indefinite"/>
    </rect>

    <!-- Right Panel Content -->
    <g transform="translate(510, 60)">
      <!-- Greeting -->
      <text x="0" y="20" font-family="system-ui, -apple-system, sans-serif" font-size="14" fill="#94A3B8" opacity="0.8">$ whoami</text>
      <text x="0" y="50" font-family="system-ui, -apple-system, sans-serif" font-size="28" font-weight="700" fill="#F8FAFC">Hi 👋 I'm John</text>
      
      <!-- Typing Text -->
      <g transform="translate(0, 80)">
        <text font-family="system-ui, -apple-system, sans-serif" font-size="18" fill="url(#accentGrad)" font-weight="500">
          <animate attributeName="opacity" values="0;1" dur="0.5s" fill="freeze"/>
          <tspan>
            <animate attributeName="text" values="|;S;So;Sof;Soft;Softw;Softwa;Softwar;Software;Software ;Software E;Software En;Software Eng;Software Engi;Software Engin;Software Engine;Software Engineer" dur="2s" fill="freeze" repeatCount="1"/>
          </tspan>
        </text>
        <rect x="0" y="0" width="2" height="22" fill="#22D3EE" class="typing-cursor">
          <animate attributeName="x" values="0;80;150;200;240;280;300;320;340;355;365;375;385;395;405;415;420" dur="2s" fill="freeze"/>
        </rect>
      </g>

      <!-- Info Items -->
      <g transform="translate(0, 130)" font-family="system-ui, -apple-system, sans-serif" font-size="13">
        <text x="0" y="0" fill="#94A3B8">
          <animate attributeName="opacity" values="0;1" dur="0.5s" begin="2.5s" fill="freeze"/>
          📍 Location : Egypt
        </text>
        <text x="0" y="25" fill="#94A3B8">
          <animate attributeName="opacity" values="0;1" dur="0.5s" begin="2.8s" fill="freeze"/>
          🎓 Education : Computer Engineering
        </text>
        <text x="0" y="50" fill="#94A3B8">
          <animate attributeName="opacity" values="0;1" dur="0.5s" begin="3.1s" fill="freeze"/>
          🔭 Current Focus : Backend Java Spring Boot
        </text>
        <text x="0" y="75" fill="#94A3B8">
          <animate attributeName="opacity" values="0;1" dur="0.5s" begin="3.4s" fill="freeze"/>
          🌐 Portfolio : https://portfolio-john-emil.vercel.app
        </text>
        <text x="0" y="100" fill="#94A3B8">
          <animate attributeName="opacity" values="0;1" dur="0.5s" begin="3.7s" fill="freeze"/>
          📧 Email : johnemil21@yahoo.com
        </text>
      </g>

      <!-- Skills Section -->
      <g transform="translate(0, 270)">
        <text x="0" y="0" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#94A3B8" letter-spacing="1">SKILLS</text>
        
        <!-- Skill Pills -->
        <g transform="translate(0, 20)">
          <rect x="0" y="0" width="75" height="32" rx="16" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.3)" stroke-width="1">
            <animate attributeName="width" values="75;82;75" dur="2s" repeatCount="indefinite"/>
          </rect>
          <text x="37.5" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#22D3EE" text-anchor="middle" font-weight="500">React</text>

          <rect x="85" y="0" width="95" height="32" rx="16" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.3)" stroke-width="1">
            <animate attributeName="width" values="95;102;95" dur="2.2s" repeatCount="indefinite"/>
          </rect>
          <text x="132.5" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#22D3EE" text-anchor="middle" font-weight="500">JavaScript</text>

          <rect x="190" y="0" width="70" height="32" rx="16" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.3)" stroke-width="1">
            <animate attributeName="width" values="70;77;70" dur="1.8s" repeatCount="indefinite"/>
          </rect>
          <text x="225" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#10B981" text-anchor="middle" font-weight="500">Tailwind</text>

          <rect x="270" y="0" width="60" height="32" rx="16" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.3)" stroke-width="1">
            <animate attributeName="width" values="60;67;60" dur="2.1s" repeatCount="indefinite"/>
          </rect>
          <text x="300" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#22D3EE" text-anchor="middle" font-weight="500">Java</text>

          <rect x="340" y="0" width="95" height="32" rx="16" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.3)" stroke-width="1">
            <animate attributeName="width" values="95;102;95" dur="2.3s" repeatCount="indefinite"/>
          </rect>
          <text x="387.5" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#22D3EE" text-anchor="middle" font-weight="500">Spring Boot</text>

          <rect x="445" y="0" width="50" height="32" rx="16" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.3)" stroke-width="1">
            <animate attributeName="width" values="50;57;50" dur="1.9s" repeatCount="indefinite"/>
          </rect>
          <text x="470" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#10B981" text-anchor="middle" font-weight="500">Vite</text>
        </g>

        <!-- Second Row -->
        <g transform="translate(0, 62)">
          <rect x="0" y="0" width="75" height="32" rx="16" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.3)" stroke-width="1">
            <animate attributeName="width" values="75;82;75" dur="2.4s" repeatCount="indefinite"/>
          </rect>
          <text x="37.5" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#22D3EE" text-anchor="middle" font-weight="500">Postgres</text>

          <rect x="85" y="0" width="40" height="32" rx="16" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.3)" stroke-width="1">
            <animate attributeName="width" values="40;47;40" dur="2.0s" repeatCount="indefinite"/>
          </rect>
          <text x="105" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#22D3EE" text-anchor="middle" font-weight="500">Git</text>

          <rect x="135" y="0" width="130" height="32" rx="16" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.3)" stroke-width="1">
            <animate attributeName="width" values="130;137;130" dur="2.5s" repeatCount="indefinite"/>
          </rect>
          <text x="200" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#10B981" text-anchor="middle" font-weight="500">Oracle Database</text>

          <rect x="275" y="0" width="85" height="32" rx="16" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.3)" stroke-width="1">
            <animate attributeName="width" values="85;92;85" dur="2.1s" repeatCount="indefinite"/>
          </rect>
          <text x="317.5" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#22D3EE" text-anchor="middle" font-weight="500">Swagger</text>

          <rect x="370" y="0" width="80" height="32" rx="16" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.3)" stroke-width="1">
            <animate attributeName="width" values="80;87;80" dur="2.2s" repeatCount="indefinite"/>
          </rect>
          <text x="410" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#22D3EE" text-anchor="middle" font-weight="500">Postman</text>
        </g>

        <!-- Third Row -->
        <g transform="translate(0, 104)">
          <rect x="0" y="0" width="95" height="32" rx="16" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.3)" stroke-width="1">
            <animate attributeName="width" values="95;102;95" dur="2.3s" repeatCount="indefinite"/>
          </rect>
          <text x="47.5" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#10B981" text-anchor="middle" font-weight="500">Claude Code</text>

          <rect x="105" y="0" width="65" height="32" rx="16" fill="rgba(124,58,237,0.15)" stroke="rgba(124,58,237,0.3)" stroke-width="1">
            <animate attributeName="width" values="65;72;65" dur="1.9s" repeatCount="indefinite"/>
          </rect>
          <text x="137.5" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#22D3EE" text-anchor="middle" font-weight="500">Cursor</text>

          <rect x="180" y="0" width="95" height="32" rx="16" fill="rgba(34,211,238,0.15)" stroke="rgba(34,211,238,0.3)" stroke-width="1">
            <animate attributeName="width" values="95;102;95" dur="2.4s" repeatCount="indefinite"/>
          </rect>
          <text x="227.5" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#22D3EE" text-anchor="middle" font-weight="500">Photoshop</text>

          <rect x="285" y="0" width="80" height="32" rx="16" fill="rgba(16,185,129,0.15)" stroke="rgba(16,185,129,0.3)" stroke-width="1">
            <animate attributeName="width" values="80;87;80" dur="2.0s" repeatCount="indefinite"/>
          </rect>
          <text x="325" y="21" font-family="system-ui, -apple-system, sans-serif" font-size="12" fill="#10B981" text-anchor="middle" font-weight="500">Illustrator</text>
        </g>
      </g>

      <!-- Social Icons -->
      <g transform="translate(0, 480)" font-family="system-ui, -apple-system, sans-serif">
        <text x="0" y="0" font-size="12" fill="#94A3B8" letter-spacing="1">CONNECT</text>
        
        <!-- GitHub Icon -->
        <g transform="translate(0, 20)" filter="url(#glow)">
          <circle cx="16" cy="16" r="16" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.1)" stroke-width="1.5">
            <animate attributeName="r" values="16;18;16" dur="2s" repeatCount="indefinite"/>
          </circle>
          <text x="16" y="21" font-size="14" fill="#F8FAFC" text-anchor="middle" font-weight="600">G</text>
        </g>

        <!-- LinkedIn Icon -->
        <g transform="translate(60, 20)" filter="url(#glow)">
          <circle cx="16" cy="16" r="16" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.1)" stroke-width="1.5">
            <animate attributeName="r" values="16;18;16" dur="2.2s" repeatCount="indefinite"/>
          </circle>
          <text x="16" y="21" font-size="14" fill="#F8FAFC" text-anchor="middle" font-weight="600">L</text>
        </g>

        <!-- Portfolio Icon -->
        <g transform="translate(120, 20)" filter="url(#glow)">
          <circle cx="16" cy="16" r="16" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.1)" stroke-width="1.5">
            <animate attributeName="r" values="16;18;16" dur="1.8s" repeatCount="indefinite"/>
          </circle>
          <text x="16" y="21" font-size="14" fill="#F8FAFC" text-anchor="middle" font-weight="600">P</text>
        </g>
      </g>
    </g>

    <!-- Floating Particles -->
    <circle cx="100" cy="100" r="2" fill="#22D3EE" opacity="0.6">
      <animate attributeName="cy" values="100;50;100" dur="6s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.6;0.2;0.6" dur="6s" repeatCount="indefinite"/>
    </circle>
    <circle cx="300" cy="400" r="1.5" fill="#7C3AED" opacity="0.5">
      <animate attributeName="cy" values="400;350;400" dur="5s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.5;0.1;0.5" dur="5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="600" cy="150" r="2" fill="#10B981" opacity="0.4">
      <animate attributeName="cy" values="150;100;150" dur="7s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.4;0.1;0.4" dur="7s" repeatCount="indefinite"/>
    </circle>
    <circle cx="900" cy="500" r="1.5" fill="#22D3EE" opacity="0.5">
      <animate attributeName="cy" values="500;450;500" dur="5.5s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.5;0.1;0.5" dur="5.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="1100" cy="200" r="2" fill="#7C3AED" opacity="0.4">
      <animate attributeName="cy" values="200;150;200" dur="6.5s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.4;0.1;0.4" dur="6.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="450" cy="300" r="1" fill="#10B981" opacity="0.3">
      <animate attributeName="cy" values="300;260;300" dur="4.5s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.3;0.05;0.3" dur="4.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="750" cy="350" r="1.5" fill="#22D3EE" opacity="0.4">
      <animate attributeName="cy" values="350;310;350" dur="5.8s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.4;0.1;0.4" dur="5.8s" repeatCount="indefinite"/>
    </circle>
    <circle cx="1050" cy="100" r="2" fill="#7C3AED" opacity="0.3">
      <animate attributeName="cy" values="100;60;100" dur="4.2s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.3;0.05;0.3" dur="4.2s" repeatCount="indefinite"/>
    </circle>

    <!-- Glass Reflection -->
    <rect x="24" y="24" width="430" height="562" rx="12" fill="url(#borderGrad)" opacity="0.03"/>
    <rect x="474" y="24" width="682" height="562" rx="12" fill="url(#borderGrad)" opacity="0.03"/>
  </g>
</svg>
