<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Muhamad Naufal — Backend Developer</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
  <script src="https://code.iconify.design/3/3.1.0/iconify.min.js"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: { sans: ['Inter', 'sans-serif'] },
          colors: {
            surface: { DEFAULT: '#F4F2ED', dark: '#0C0C0C', card: '#EAE8E2' },
            ink: { DEFAULT: '#1C1C1C', light: '#78716C', faint: '#A8A29E' },
            accent: { DEFAULT: '#00BFFF', dim: '#0ea5e9' },
          },
          borderRadius: { '2xl': '1rem', '3xl': '1.5rem' },
        }
      }
    }
  </script>
  <style>
    ::selection { background: #00BFFF; color: #fff; }

    @keyframes revealUp {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes revealScale {
      from { opacity: 0; transform: scale(0.95); }
      to { opacity: 1; transform: scale(1); }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes slideLine {
      from { width: 0; }
      to { width: 100%; }
    }
    @keyframes pulse-dot {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.4; }
    }
    @keyframes countUp {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-8px); }
    }

    .anim-up { animation: revealUp 1.2s cubic-bezier(0.2,1,0.3,1) forwards; opacity: 0; }
    .anim-scale { animation: revealScale 1.4s cubic-bezier(0.2,1,0.3,1) forwards; opacity: 0; }
    .anim-fade { animation: fadeIn 1s ease-out forwards; opacity: 0; }
    .delay-1 { animation-delay: 0.15s; }
    .delay-2 { animation-delay: 0.3s; }
    .delay-3 { animation-delay: 0.45s; }
    .delay-4 { animation-delay: 0.6s; }
    .delay-5 { animation-delay: 0.75s; }
    .delay-6 { animation-delay: 0.9s; }
    .delay-7 { animation-delay: 1.05s; }
    .delay-8 { animation-delay: 1.2s; }

    .link-hover { position: relative; }
    .link-hover::after {
      content: ''; position: absolute; bottom: -2px; left: 0;
      height: 1px; width: 0; background: #00BFFF;
      transition: width 300ms ease-out;
    }
    .link-hover:hover::after { width: 100%; }

    .tech-row { transition: all 500ms ease-out; }
    .tech-row:hover { padding-left: 0.75rem; }
    .tech-row:hover .tech-label { color: #00BFFF; }

    .stat-card {
      transition: all 500ms cubic-bezier(0.22,1,0.36,1);
    }
    .stat-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 25px 50px -12px rgba(0,0,0,0.08);
    }

    .contact-link {
      transition: all 300ms ease-out;
    }
    .contact-link:hover {
      color: #00BFFF;
      transform: translateX(4px);
    }
    .contact-link:hover .contact-arrow {
      transform: translateX(4px);
      opacity: 1;
    }
    .contact-arrow {
      transition: all 300ms ease-out;
      opacity: 0;
      transform: translateX(-4px);
    }

    .status-dot {
      animation: pulse-dot 2s ease-in-out infinite;
    }

    .skill-tag {
      transition: all 300ms ease-out;
    }
    .skill-tag:hover {
      background: #1C1C1C;
      color: #F4F2ED;
      transform: translateY(-2px);
    }

    .scroll-indicator {
      animation: float 3s ease-in-out infinite;
    }
  </style>
</head>

<body class="bg-surface font-sans text-ink antialiased">

  <!-- ═══════════════════════ NAV ═══════════════════════ -->
  <nav class="fixed top-0 left-0 right-0 z-50 anim-fade" id="nav">
    <div class="max-w-[1800px] mx-auto px-6 md:px-12 py-5 flex items-center justify-between">
      <a href="#" class="text-sm font-semibold tracking-[0.2em] uppercase text-ink">
        MN<span class="text-accent">.</span>
      </a>
      <div class="hidden md:flex items-center gap-8">
        <a href="#about" class="text-[11px] font-semibold tracking-[0.2em] uppercase text-ink-light hover:text-accent transition-colors duration-300">About</a>
        <a href="#tech" class="text-[11px] font-semibold tracking-[0.2em] uppercase text-ink-light hover:text-accent transition-colors duration-300">Stack</a>
        <a href="#stats" class="text-[11px] font-semibold tracking-[0.2em] uppercase text-ink-light hover:text-accent transition-colors duration-300">Stats</a>
        <a href="#contact" class="text-[11px] font-semibold tracking-[0.2em] uppercase text-ink-light hover:text-accent transition-colors duration-300">Contact</a>
      </div>
      <div class="flex items-center gap-2">
        <span class="status-dot w-2 h-2 rounded-full bg-emerald-500 inline-block"></span>
        <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-light">Open to Work</span>
      </div>
    </div>
  </nav>

  <!-- ═══════════════════════ HERO ═══════════════════════ -->
  <section class="min-h-screen flex flex-col justify-center items-center relative px-6 md:px-12">
    <!-- Subtle grid background -->
    <div class="absolute inset-0 opacity-[0.03]" style="background-image: linear-gradient(#1C1C1C 1px, transparent 1px), linear-gradient(90deg, #1C1C1C 1px, transparent 1px); background-size: 60px 60px;"></div>

    <div class="text-center relative z-10">
      <!-- Label -->
      <div class="anim-up delay-1 mb-8">
        <span class="inline-flex items-center gap-2 text-[10px] font-bold tracking-[0.3em] uppercase text-ink-light border border-ink/10 rounded-full px-5 py-2.5">
          <span class="iconify" data-icon="lucide:map-pin" data-width="12"></span>
          Karawang, Indonesia
        </span>
      </div>

      <!-- Name -->
      <h1 class="anim-up delay-2 text-[15vw] md:text-[11rem] font-semibold leading-[0.85] tracking-[-0.05em] uppercase text-ink">
        Naufal
      </h1>

      <!-- Role -->
      <div class="anim-up delay-3 mt-6 md:mt-8">
        <p class="text-sm md:text-base font-light text-ink-light tracking-wide">
          Backend Developer · Laravel Enthusiast · Clean Code Advocate
        </p>
      </div>

      <!-- CTA -->
      <div class="anim-up delay-4 mt-10 flex flex-col sm:flex-row items-center justify-center gap-4">
        <a href="#contact" class="group inline-flex items-center gap-3 bg-ink text-surface text-[10px] font-bold tracking-[0.25em] uppercase px-8 py-4 rounded-full hover:bg-accent transition-colors duration-300">
          Get in Touch
          <span class="iconify transition-transform duration-300 group-hover:translate-x-1" data-icon="lucide:arrow-right" data-width="14"></span>
        </a>
        <a href="#about" class="inline-flex items-center gap-3 text-[10px] font-bold tracking-[0.25em] uppercase text-ink-light hover:text-accent transition-colors duration-300 px-8 py-4">
          Learn More
          <span class="iconify" data-icon="lucide:arrow-down" data-width="14"></span>
        </a>
      </div>
    </div>

    <!-- Scroll indicator -->
    <div class="absolute bottom-12 left-1/2 -translate-x-1/2 scroll-indicator anim-fade delay-7">
      <div class="w-px h-12 bg-gradient-to-b from-transparent to-ink/20"></div>
    </div>
  </section>

  <!-- ═══════════════════════ ABOUT ═══════════════════════ -->
  <section id="about" class="py-32 md:py-48 px-6 md:px-12">
    <div class="max-w-[672px] mx-auto">
      <!-- Section label -->
      <div class="anim-up">
        <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-accent">01 — About</span>
      </div>

      <!-- Divider -->
      <div class="mt-6 mb-10 h-px bg-ink/10 anim-fade delay-1" style="animation: slideLine 1.5s cubic-bezier(0.22,1,0.36,1) forwards; width: 0; animation-delay: 0.3s;"></div>

      <!-- Content -->
      <p class="anim-up delay-2 text-lg md:text-xl font-light leading-relaxed text-ink/80">
        Saya adalah backend developer yang fokus membangun aplikasi web skalabel dengan <strong class="font-semibold text-ink">Laravel</strong>. Percaya bahwa kode yang bersih adalah fondasi dari produk yang bertahan lama.
      </p>
      <p class="anim-up delay-3 mt-6 text-lg md:text-xl font-light leading-relaxed text-ink/80">
        Saat ini mendalami <strong class="font-semibold text-ink">Filament</strong>, API design, dan TailwindCSS. Setiap hari adalah kesempatan untuk menulis kode yang lebih baik dari kemarin.
      </p>

      <!-- Quick facts -->
      <div class="anim-up delay-4 mt-12 grid grid-cols-2 gap-6">
        <div class="border-t border-ink/10 pt-5">
          <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Focus</span>
          <p class="mt-2 text-sm font-medium text-ink">Backend & API</p>
        </div>
        <div class="border-t border-ink/10 pt-5">
          <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Experience</span>
          <p class="mt-2 text-sm font-medium text-ink">Laravel Ecosystem</p>
        </div>
        <div class="border-t border-ink/10 pt-5">
          <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Learning</span>
          <p class="mt-2 text-sm font-medium text-ink">Filament · React</p>
        </div>
        <div class="border-t border-ink/10 pt-5">
          <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Principle</span>
          <p class="mt-2 text-sm font-medium text-ink">Clean Code First</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════════════════════ TECH STACK ═══════════════════════ -->
  <section id="tech" class="py-32 md:py-48 px-6 md:px-12 bg-surface-card">
    <div class="max-w-[1200px] mx-auto">
      <!-- Section label -->
      <div class="anim-up">
        <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-accent">02 — Tech Stack</span>
      </div>
      <div class="mt-6 mb-16 h-px bg-ink/10 anim-fade delay-1" style="animation: slideLine 1.5s cubic-bezier(0.22,1,0.36,1) forwards; width: 0; animation-delay: 0.3s;"></div>

      <div class="grid md:grid-cols-2 gap-16 md:gap-24">

        <!-- Left: Categories -->
        <div class="space-y-10">
          <!-- Core -->
          <div class="anim-up delay-2">
            <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Core</span>
            <div class="mt-4 flex flex-wrap gap-2">
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">PHP</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">Laravel</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">CodeIgniter</span>
            </div>
          </div>

          <!-- Frontend -->
          <div class="anim-up delay-3">
            <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Frontend</span>
            <div class="mt-4 flex flex-wrap gap-2">
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">JavaScript</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">HTML</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">CSS</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">Bootstrap</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">TailwindCSS</span>
            </div>
          </div>

          <!-- Database & Tools -->
          <div class="anim-up delay-4">
            <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Database & Tools</span>
            <div class="mt-4 flex flex-wrap gap-2">
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">MySQL</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">Firebase</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">Postman</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">Git</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-surface rounded-full border border-ink/5 cursor-default">GitHub</span>
            </div>
          </div>

          <!-- Learning -->
          <div class="anim-up delay-5">
            <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Currently Learning</span>
            <div class="mt-4 flex flex-wrap gap-2">
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-accent/10 text-accent rounded-full border border-accent/20 cursor-default">Filament</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-accent/10 text-accent rounded-full border border-accent/20 cursor-default">React</span>
              <span class="skill-tag px-4 py-2 text-xs font-medium bg-accent/10 text-accent rounded-full border border-accent/20 cursor-default">Node.js</span>
            </div>
          </div>
        </div>

        <!-- Right: Philosophy -->
        <div class="anim-up delay-3 flex flex-col justify-center">
          <div class="border-l-2 border-accent/30 pl-8">
            <p class="text-2xl md:text-3xl font-light leading-snug text-ink/80">
              "Saya tidak hanya menulis kode yang <em class="font-medium text-ink not-italic">berfungsi</em>, tapi kode yang <em class="font-medium text-ink not-italic">dapat dibaca</em> oleh manusia."
            </p>
          </div>
          <div class="mt-10 space-y-4">
            <div class="flex items-start gap-4">
              <span class="mt-1 flex-shrink-0 w-8 h-8 rounded-full bg-ink/5 flex items-center justify-center">
                <span class="iconify text-ink-light" data-icon="lucide:check" data-width="14"></span>
              </span>
              <div>
                <p class="text-sm font-semibold text-ink">SOLID Principles</p>
                <p class="text-sm font-light text-ink-light">Arsitektur yang mudah di-maintain</p>
              </div>
            </div>
            <div class="flex items-start gap-4">
              <span class="mt-1 flex-shrink-0 w-8 h-8 rounded-full bg-ink/5 flex items-center justify-center">
                <span class="iconify text-ink-light" data-icon="lucide:check" data-width="14"></span>
              </span>
              <div>
                <p class="text-sm font-semibold text-ink">RESTful API Design</p>
                <p class="text-sm font-light text-ink-light">Endpoint yang konsisten & terdokumentasi</p>
              </div>
            </div>
            <div class="flex items-start gap-4">
              <span class="mt-1 flex-shrink-0 w-8 h-8 rounded-full bg-ink/5 flex items-center justify-center">
                <span class="iconify text-ink-light" data-icon="lucide:check" data-width="14"></span>
              </span>
              <div>
                <p class="text-sm font-semibold text-ink">Version Control</p>
                <p class="text-sm font-light text-ink-light">Git workflow yang terstruktur</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════════════════════ STATS ═══════════════════════ -->
  <section id="stats" class="py-32 md:py-48 px-6 md:px-12">
    <div class="max-w-[1200px] mx-auto">
      <!-- Section label -->
      <div class="anim-up">
        <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-accent">03 — GitHub Stats</span>
      </div>
      <div class="mt-6 mb-16 h-px bg-ink/10 anim-fade delay-1" style="animation: slideLine 1.5s cubic-bezier(0.22,1,0.36,1) forwards; width: 0; animation-delay: 0.3s;"></div>

      <!-- GitHub Cards -->
      <div class="anim-scale delay-2 flex flex-col md:flex-row gap-6">
        <div class="stat-card flex-1 bg-surface-card rounded-2xl p-6 border border-ink/5">
          <img src="https://github-readme-stats.vercel.app/api?username=muhamad-naufal-666&show_icons=true&theme=default&hide_border=true&hide_title=true&bg_color=transparent&title_color=1C1C1C&icon_color=00BFFF&text_color=78716C" alt="GitHub Stats" class="w-full" />
        </div>
        <div class="stat-card flex-1 bg-surface-card rounded-2xl p-6 border border-ink/5">
          <img src="https://github-readme-streak-stats.herokuapp.com?user=muhamad-naufal-666&theme=default&hide_border=true&hide_title=true&background=transparent&stroke=rgba(28,28,28,0.1)&ring=rgba(28,28,28,0.05)&fire=00BFFF&currStreakLabel=1C1C1C&sideLabels=78716C&currStreakNum=1C1C1C&sideNums=1C1C1C&dates=78716C" alt="Streak Stats" class="w-full" />
        </div>
      </div>

      <!-- Mini metrics -->
      <div class="mt-8 grid grid-cols-2 md:grid-cols-4 gap-4">
        <div class="stat-card bg-surface-card rounded-2xl p-6 border border-ink/5 text-center">
          <p class="text-3xl font-semibold text-ink tracking-tight">Laravel</p>
          <p class="mt-1 text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Primary Stack</p>
        </div>
        <div class="stat-card bg-surface-card rounded-2xl p-6 border border-ink/5 text-center">
          <p class="text-3xl font-semibold text-ink tracking-tight">REST</p>
          <p class="mt-1 text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">API Design</p>
        </div>
        <div class="stat-card bg-surface-card rounded-2xl p-6 border border-ink/5 text-center">
          <p class="text-3xl font-semibold text-ink tracking-tight">Clean</p>
          <p class="mt-1 text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Code Style</p>
        </div>
        <div class="stat-card bg-surface-card rounded-2xl p-6 border border-ink/5 text-center">
          <p class="text-3xl font-semibold text-accent tracking-tight">∞</p>
          <p class="mt-1 text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">Willing to Learn</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════════════════════ CONTACT ═══════════════════════ -->
  <section id="contact" class="py-32 md:py-48 px-6 md:px-12 bg-surface-card">
    <div class="max-w-[672px] mx-auto text-center">
      <!-- Section label -->
      <div class="anim-up">
        <span class="text-[10px] font-bold tracking-[0.3em] uppercase text-accent">04 — Contact</span>
      </div>
      <div class="mt-6 mb-12 h-px bg-ink/10 mx-auto max-w-[200px] anim-fade delay-1" style="animation: slideLine 1.5s cubic-bezier(0.22,1,0.36,1) forwards; width: 0; animation-delay: 0.3s;"></div>

      <h2 class="anim-up delay-2 text-4xl md:text-6xl font-medium tracking-[-0.025em] leading-[1.1] text-ink">
        Let's Build<br />Something Together
      </h2>
      <p class="anim-up delay-3 mt-6 text-base font-light text-ink-light leading-relaxed max-w-md mx-auto">
        Punya proyek menarik atau ingin berdiskusi? Saya selalu terbuka untuk peluang baru.
      </p>

      <!-- Contact Links -->
      <div class="anim-up delay-4 mt-12 flex flex-col items-center gap-5">
        <a href="mailto:naufal.mhmd1106@gmail.com" class="contact-link group flex items-center gap-4 text-ink">
          <span class="w-12 h-12 rounded-full bg-surface flex items-center justify-center border border-ink/5 group-hover:bg-ink group-hover:text-surface transition-all duration-300">
            <span class="iconify" data-icon="lucide:mail" data-width="18"></span>
          </span>
          <div class="text-left">
            <p class="text-sm font-medium">Email</p>
            <p class="text-xs text-ink-light">naufal.mhmd1106@gmail.com</p>
          </div>
          <span class="contact-arrow iconify ml-4" data-icon="lucide:arrow-right" data-width="16"></span>
        </a>

        <a href="https://wa.me/6281573635413" target="_blank" class="contact-link group flex items-center gap-4 text-ink">
          <span class="w-12 h-12 rounded-full bg-surface flex items-center justify-center border border-ink/5 group-hover:bg-ink group-hover:text-surface transition-all duration-300">
            <span class="iconify" data-icon="lucide:message-circle" data-width="18"></span>
          </span>
          <div class="text-left">
            <p class="text-sm font-medium">WhatsApp</p>
            <p class="text-xs text-ink-light">+62 815-7363-5413</p>
          </div>
          <span class="contact-arrow iconify ml-4" data-icon="lucide:arrow-right" data-width="16"></span>
        </a>

        <a href="https://www.linkedin.com/in/usernameanda/" target="_blank" class="contact-link group flex items-center gap-4 text-ink">
          <span class="w-12 h-12 rounded-full bg-surface flex items-center justify-center border border-ink/5 group-hover:bg-ink group-hover:text-surface transition-all duration-300">
            <span class="iconify" data-icon="lucide:linkedin" data-width="18"></span>
          </span>
          <div class="text-left">
            <p class="text-sm font-medium">LinkedIn</p>
            <p class="text-xs text-ink-light">Muhamad Naufal</p>
          </div>
          <span class="contact-arrow iconify ml-4" data-icon="lucide:arrow-right" data-width="16"></span>
        </a>

        <a href="https://github.com/muhamad-naufal-666" target="_blank" class="contact-link group flex items-center gap-4 text-ink">
          <span class="w-12 h-12 rounded-full bg-surface flex items-center justify-center border border-ink/5 group-hover:bg-ink group-hover:text-surface transition-all duration-300">
            <span class="iconify" data-icon="lucide:github" data-width="18"></span>
          </span>
          <div class="text-left">
            <p class="text-sm font-medium">GitHub</p>
            <p class="text-xs text-ink-light">muhamad-naufal-666</p>
          </div>
          <span class="contact-arrow iconify ml-4" data-icon="lucide:arrow-right" data-width="16"></span>
        </a>
      </div>
    </div>
  </section>

  <!-- ═══════════════════════ FOOTER ═══════════════════════ -->
  <footer class="py-12 px-6 md:px-12 border-t border-ink/5">
    <div class="max-w-[1800px] mx-auto flex flex-col md:flex-row items-center justify-between gap-4">
      <p class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">
        © 2025 Muhamad Naufal
      </p>
      <p class="text-[10px] font-bold tracking-[0.3em] uppercase text-ink-faint">
        Consistency beats talent — keep coding.
      </p>
    </div>
  </footer>

  <!-- ═══════════════════════ SCRIPTS ═══════════════════════ -->
  <script>
    // Nav background on scroll
    const nav = document.getElementById('nav');
    let lastScroll = 0;

    window.addEventListener('scroll', () => {
      const currentScroll = window.scrollY;
      if (currentScroll > 80) {
        nav.style.background = 'rgba(244, 242, 237, 0.85)';
        nav.style.backdropFilter = 'blur(12px)';
        nav.style.borderBottom = '1px solid rgba(28, 28, 28, 0.05)';
      } else {
        nav.style.background = 'transparent';
        nav.style.backdropFilter = 'none';
        nav.style.borderBottom = 'none';
      }
      lastScroll = currentScroll;
    });

    // Intersection Observer for scroll animations
    const observerOptions = {
      threshold: 0.15,
      rootMargin: '0px 0px -60px 0px'
    };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.animationPlayState = 'running';
          observer.unobserve(entry.target);
        }
      });
    }, observerOptions);

    // Observe all animated elements (except hero — those play immediately)
    document.querySelectorAll('#about .anim-up, #about .anim-fade, #tech .anim-up, #tech .anim-scale, #tech .anim-fade, #stats .anim-up, #stats .anim-scale, #stats .anim-fade, #contact .anim-up, #contact .anim-fade').forEach(el => {
      el.style.animationPlayState = 'paused';
      observer.observe(el);
    });

    // Smooth scroll for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
      });
    });
  </script>

</body>
</html>
