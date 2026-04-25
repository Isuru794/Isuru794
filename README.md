<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
      colors: {
        neon: '#00FFCC',
        dark: '#0D1117',
        darker: '#0A0A0F',
          },
      animation: {
        'glow': 'glow 2s ease-in-out infinite',
        'float': 'float 3s ease-in-out infinite',
        'spin-slow': 'spin 8s linear infinite',
        'pulse-fast': 'pulse 1.5s cubic-bezier(0.4, 0, 0.6, 1) infinite',
      },
      keyframes: {
        glow: {
          '0%, 100%': { textShadow: '0 0 20px rgba(0, 255, 204, 0.5)' },
          '50%': { textShadow: '0 0 40px rgba(0, 255, 204, 0.8)' },
        },
        float: {
          '0%, 100%': { transform: 'translateY(0px)' },
          '50%': { transform: 'translateY(-10px)' },
        },
      },
        },
      },
    }
  </script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Inter:wght@300;400;600;700&display=swap');
    * { font-family: 'Inter', sans-serif; }
    .orbitron { font-family: 'Orbitron', monospace; }
    .glow-text { animation: glow 2s ease-in-out infinite; }
    .float-animation { animation: float 3s ease-in-out infinite; }
    .bg-grid { background-image: linear-gradient(rgba(0, 255, 204, 0.05) 1px, transparent 1px), linear-gradient(90deg, rgba(0, 255, 204, 0.05) 1px, transparent 1px); background-size: 50px 50px; }
  </style>
</head>
<body class="bg-dark text-white">

<div class="max-w-5xl mx-auto p-6 space-y-8">

  <!-- About Me Section - TOP -->
  <div class="bg-gradient-to-br from-darker to-dark rounded-2xl border border-neon/20 p-8 shadow-2xl backdrop-blur-sm bg-grid">
    <div class="flex flex-col md:flex-row gap-8 items-start">
      
      <!-- Avatar + 3D Badge -->
      <div class="relative float-animation">
        <div class="w-32 h-32 rounded-full bg-gradient-to-br from-neon to-purple-600 p-1">
          <div class="w-full h-full rounded-full bg-dark flex items-center justify-center text-6xl font-bold orbitron text-neon">
            IS
          </div>
        </div>
        <div class="absolute -bottom-2 -right-2 bg-neon text-dark text-xs font-bold px-2 py-1 rounded-full">
          3D DEV
        </div>
      </div>

      <!-- About Me Content -->
      <div class="flex-1 space-y-4">
        <div class="flex items-center gap-3 flex-wrap">
          <h1 class="text-5xl font-bold orbitron bg-gradient-to-r from-neon to-blue-500 bg-clip-text text-transparent">
            Isuru Sumedha
          </h1>
          <span class="px-3 py-1 bg-neon/10 border border-neon/30 rounded-full text-neon text-sm font-mono">
            Fullstack Dev
          </span>
        </div>

        <div class="text-gray-300 text-lg leading-relaxed space-y-3">
          <p class="flex items-center gap-2">
            <span class="text-neon">✦</span> 
            <span class="orbitron text-neon">SE Undergraduate</span> 
            <span class="text-gray-500">|</span> 
            <span>University of Sri Lanka</span>
          </p>
          <p class="flex items-center gap-2">
            <span class="text-neon">✦</span> 
            Currently building <span class="text-neon font-semibold">Fullstack Apps</span> & 
            <span class="text-neon font-semibold">3D Web Experiences</span>
          </p>
          <p class="flex items-center gap-2">
            <span class="text-neon">✦</span> 
            Passionate about <span class="text-neon">Creative Coding</span> | 
            <span class="text-neon">WebGL</span> | 
            <span class="text-neon">System Design</span>
          </p>
          <p class="flex items-center gap-2">
            <span class="text-neon">✦</span> 
            Open for collaborations & innovative projects
          </p>
        </div>

        <!-- Quick Action Badges -->
        <div class="flex gap-3 pt-3 flex-wrap">
          <a href="#" class="px-4 py-2 bg-neon/10 border border-neon rounded-lg text-neon hover:bg-neon hover:text-dark transition-all duration-300 flex items-center gap-2">
            📄 Resume
          </a>
          <a href="#" class="px-4 py-2 bg-dark border border-gray-700 rounded-lg text-gray-300 hover:border-neon hover:text-neon transition-all duration-300 flex items-center gap-2">
            💼 Portfolio
          </a>
          <a href="#" class="px-4 py-2 bg-dark border border-gray-700 rounded-lg text-gray-300 hover:border-neon hover:text-neon transition-all duration-300 flex items-center gap-2">
            📧 Contact
          </a>
        </div>
      </div>
    </div>
  </div>

  <!-- Typing Animation Banner -->
  <div class="bg-dark/50 rounded-xl p-6 text-center border border-neon/20">
    <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=600&size=28&duration=3000&pause=500&color=00FFCC&center=true&vCenter=true&width=800&lines=Fullstack+Developer;3D+Web+Enthusiast;MERN+%7C+Next.js+%7C+Three.js;Creative+Problem+Solver" alt="Typing SVG" class="mx-auto" />
  </div>

  <!-- 3D Stats Row -->
  <div class="grid md:grid-cols-2 gap-6">
    <div class="bg-darker rounded-xl p-4 border border-neon/20 hover:border-neon/50 transition-all duration-300 hover:scale-105">
      <img src="https://github-readme-stats.vercel.app/api?username=IsuruSumedha&show_icons=true&theme=radical&hide_border=true&bg_color=0D1117&title_color=00FFCC&icon_color=00FFCC&ring_color=00FFCC&text_color=AAAAAA" class="w-full" />
    </div>
    <div class="bg-darker rounded-xl p-4 border border-neon/20 hover:border-neon/50 transition-all duration-300 hover:scale-105">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=IsuruSumedha&layout=compact&theme=radical&hide_border=true&bg_color=0D1117&title_color=00FFCC&text_color=AAAAAA" class="w-full" />
    </div>
  </div>

  <!-- 3D Tech Stack (Animated Cards) -->
  <div class="bg-darker rounded-xl p-6 border border-neon/20">
    <h2 class="text-2xl font-bold orbitron text-neon mb-6 text-center animate-pulse-fast">
      ⚡ 3D Tech Universe
    </h2>
    <div class="grid grid-cols-3 md:grid-cols-6 gap-4">
      {[
        ['react', 'React', '#61DAFB'],
        ['nodejs', 'Node.js', '#339933'],
        ['nextjs', 'Next.js', '#000000'],
        ['typescript', 'TypeScript', '#3178C6'],
        ['threejs', 'Three.js', '#000000'],
        ['tailwind', 'Tailwind', '#06B6D4'],
        ['mongodb', 'MongoDB', '#47A248'],
        ['postgresql', 'PostgreSQL', '#4169E1'],
        ['docker', 'Docker', '#2496ED'],
        ['git', 'Git', '#F05032'],
        ['vscode', 'VS Code', '#007ACC'],
        ['figma', 'Figma', '#F24E1E']
      ].map(([icon, name, color]) => `
        <div class="group bg-dark rounded-lg p-4 text-center hover:bg-neon/10 transition-all duration-300 hover:scale-110 cursor-pointer border border-gray-800 hover:border-neon">
          <img src="https://skillicons.dev/icons?i=${icon}" class="w-12 mx-auto mb-2" />
          <p class="text-sm text-gray-400 group-hover:text-neon transition-colors">${name}</p>
        </div>
      `).join('')}
    </div>
  </div>

  <!-- 3D Contribution Snake (Animated) -->
  <div class="bg-darker rounded-xl p-4 border border-neon/20">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/IsuruSumedha/IsuruSumedha/output/github-contribution-grid-snake-dark.svg" />
      <img alt="GitHub Snake Animation" src="https://raw.githubusercontent.com/IsuruSumedha/IsuruSumedha/output/github-contribution-grid-snake-dark.svg" class="w-full" />
    </picture>
  </div>

  <!-- 3D Activity Graph -->
  <div class="bg-darker rounded-xl p-4 border border-neon/20">
    <img src="https://github-readme-activity-graph.vercel.app/graph?username=IsuruSumedha&bg_color=0D1117&color=00FFCC&line=00FFCC&point=FFFFFF&area=true&hide_border=true&radius=8" class="w-full" />
  </div>

  <!-- Current Focus with 3D Hover -->
  <div class="grid md:grid-cols-3 gap-6">
    <div class="bg-gradient-to-br from-neon/10 to-transparent rounded-xl p-5 border border-neon/20 hover:border-neon transition-all duration-300 hover:translate-y-[-5px]">
      <div class="text-3xl mb-3">🔭</div>
      <h3 class="text-xl font-bold text-neon mb-2">Currently Building</h3>
      <p class="text-gray-400">Fullstack SaaS platform with Next.js + Three.js 3D dashboards</p>
    </div>
    <div class="bg-gradient-to-br from-neon/10 to-transparent rounded-xl p-5 border border-neon/20 hover:border-neon transition-all duration-300 hover:translate-y-[-5px]">
      <div class="text-3xl mb-3">🌱</div>
      <h3 class="text-xl font-bold text-neon mb-2">Learning</h3>
      <p class="text-gray-400">WebGL Shaders, System Design, AWS Architecture</p>
    </div>
    <div class="bg-gradient-to-br from-neon/10 to-transparent rounded-xl p-5 border border-neon/20 hover:border-neon transition-all duration-300 hover:translate-y-[-5px]">
      <div class="text-3xl mb-3">🤝</div>
      <h3 class="text-xl font-bold text-neon mb-2">Open To</h3>
      <p class="text-gray-400">3D web projects, Hackathons, Creative collaborations</p>
    </div>
  </div>

  <!-- Connect Section -->
  <div class="bg-darker rounded-xl p-6 text-center border border-neon/20">
    <h2 class="text-2xl font-bold orbitron text-neon mb-6">🌐 Connect in 3D Space</h2>
    <div class="flex justify-center gap-4 flex-wrap">
      <a href="#" class="group relative px-6 py-3 bg-dark rounded-lg border border-neon/30 hover:bg-neon transition-all duration-300">
        <span class="text-neon group-hover:text-dark font-semibold">💼 LinkedIn</span>
      </a>
      <a href="#" class="group relative px-6 py-3 bg-dark rounded-lg border border-neon/30 hover:bg-neon transition-all duration-300">
        <span class="text-neon group-hover:text-dark font-semibold">🐦 Twitter</span>
      </a>
      <a href="#" class="group relative px-6 py-3 bg-dark rounded-lg border border-neon/30 hover:bg-neon transition-all duration-300">
        <span class="text-neon group-hover:text-dark font-semibold">💻 GitHub</span>
      </a>
      <a href="#" class="group relative px-6 py-3 bg-dark rounded-lg border border-neon/30 hover:bg-neon transition-all duration-300">
        <span class="text-neon group-hover:text-dark font-semibold">📧 Email</span>
      </a>
    </div>
  </div>

  <!-- Footer -->
  <div class="text-center pt-6 border-t border-gray-800">
    <div class="flex justify-center items-center gap-4 text-sm text-gray-500">
      <span>✦ 3D Animated Profile ✦</span>
      <span>⚡ Powered by Tailwind CSS</span>
      <span>
        <img src="https://komarev.com/ghpvc/?username=IsuruSumedha&style=flat-square&color=00FFCC" class="inline" />
      </span>
    </div>
  </div>

</div>

</body>
</html>
