<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>yourname — Modern GitHub Page</title>
    <meta name="description" content="A sleek, modern personal site template for GitHub Pages. Neon gradients, glass cards, and dark mode." />

    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">

    <!-- Tailwind (CDN build for speed on GitHub Pages) -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
      tailwind.config = {
        theme: {
          extend: {
            fontFamily: { sans: ['Inter', 'ui-sans-serif', 'system-ui'] },
            dropShadow: {
              glow: '0 0 30px rgba(99,102,241,0.45)',
            },
            backgroundImage: {
              'grid': 'linear-gradient(rgba(255,255,255,0.06) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.06) 1px, transparent 1px)',
            },
          }
        },
        darkMode: 'class'
      }
    </script>
    <style>
      /* Subtle animated gradient blob */
      .blob {
        filter: blur(70px);
        animation: float 16s ease-in-out infinite;
      }
      @keyframes float {
        0%, 100% { transform: translate(0,0) scale(1); }
        50% { transform: translate(20px, -10px) scale(1.05); }
      }
    </style>
    <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Cdefs%3E%3ClinearGradient id='g' x1='0' y1='0' x2='1' y2='1'%3E%3Cstop stop-color='%236364F1'/%3E%3Cstop offset='1' stop-color='%230EA5E9'/%3E%3C/linearGradient%3E%3C/defs%3E%3Ccircle cx='50' cy='50' r='45' fill='url(%23g)'/%3E%3Ctext x='50' y='57' text-anchor='middle' font-family='Inter' font-size='45' fill='white'%3E%F0%9F%94%A5%3C/text%3E%3C/svg%3E">
  </head>
  <body class="bg-slate-950 text-slate-200 font-sans antialiased selection:bg-indigo-500/40">
    <!-- Decorative background -->
    <div aria-hidden="true" class="fixed inset-0 -z-10 overflow-hidden">
      <div class="absolute -top-40 -left-20 w-96 h-96 rounded-full bg-indigo-600/30 blob"></div>
      <div class="absolute top-40 -right-10 w-[28rem] h-[28rem] rounded-full bg-cyan-500/20 blob" style="animation-delay: -6s"></div>
      <div class="absolute inset-0 bg-grid bg-[size:40px_40px]"></div>
      <div class="absolute inset-0 bg-gradient-to-b from-transparent via-slate-950/40 to-slate-950"></div>
    </div>

    <!-- Header -->
    <header class="sticky top-0 z-50 backdrop-blur-xl bg-slate-950/60 border-b border-white/10">
      <div class="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
        <a href="#" class="text-lg font-bold tracking-tight">
          <span class="bg-gradient-to-r from-indigo-400 to-cyan-400 bg-clip-text text-transparent">yourname</span>
        </a>
        <nav class="hidden md:flex items-center gap-6 text-sm text-slate-300">
          <a class="hover:text-white transition" href="#projects">Projects</a>
          <a class="hover:text-white transition" href="#about">About</a>
          <a class="hover:text-white transition" href="#contact">Contact</a>
          <a class="hover:text-white transition" href="https://github.com/yourhandle" target="_blank" rel="noreferrer">GitHub</a>
        </nav>
        <div class="flex items-center gap-2">
          <button id="themeToggle" class="p-2 rounded-xl border border-white/10 hover:border-white/20 hover:bg-white/5 transition" aria-label="Toggle dark mode">
            <!-- moon/sun icon -->
            <svg id="iconMoon" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 24 24" fill="none" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M21 12.79A9 9 0 1111.21 3a7 7 0 109.79 9.79z"/></svg>
            <svg id="iconSun" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 hidden" viewBox="0 0 24 24" fill="none" stroke="currentColor"><circle cx="12" cy="12" r="4"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 2v2m0 16v2M2 12h2m16 0h2M4.93 4.93l1.41 1.41m11.32 11.32l1.41 1.41m0-14.14l-1.41 1.41M6.34 17.66l-1.41 1.41"/></svg>
          </button>
          <a href="#contact" class="hidden sm:inline-flex items-center gap-2 px-3 py-2 rounded-xl text-sm font-semibold bg-white/10 border border-white/10 hover:bg-white/15 hover:border-white/20 transition">
            <span>Contact</span>
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 24 24" fill="none" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17 8l4 4m0 0l-4 4m4-4H3"/></svg>
          </a>
        </div>
      </div>
    </header>

    <!-- Hero -->
    <section class="relative">
      <div class="max-w-6xl mx-auto px-4 pt-20 pb-16">
        <div class="grid md:grid-cols-2 items-center gap-10">
          <div>
            <p class="inline-flex items-center gap-2 text-xs uppercase tracking-widest text-slate-400/80 bg-white/5 border border-white/10 rounded-full px-3 py-1">
              <span class="h-1.5 w-1.5 rounded-full bg-emerald-400"></span>
              Open to collaborations
            </p>
            <h1 class="mt-4 text-4xl/tight sm:text-5xl/tight lg:text-6xl/tight font-extrabold">
              Build <span class="bg-gradient-to-r from-indigo-400 to-cyan-400 bg-clip-text text-transparent drop-shadow-glow">clean, modern</span> products that actually ship
            </h1>
            <p class="mt-5 text-slate-300/90 max-w-prose">
              I’m yourname — a builder focused on fast iteration and crisp UX. Here’s a curated slice of my work and experiments.
            </p>
            <div class="mt-8 flex flex-wrap items-center gap-3">
              <a href="#projects" class="inline-flex items-center gap-2 px-4 py-2 rounded-xl font-semibold bg-indigo-500/90 hover:bg-indigo-500 transition">
                View Projects
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 24 24" fill="none" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M5 12h14M12 5l7 7-7 7"/></svg>
              </a>
              <a href="https://github.com/yourhandle" target="_blank" rel="noreferrer" class="inline-flex items-center gap-2 px-4 py-2 rounded-xl border border-white/10 hover:border-white/20 bg-white/5 hover:bg-white/10 transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .5C5.73.5.98 5.24.98 11.5c0 4.85 3.14 8.96 7.49 10.41.55.11.75-.24.75-.53 0-.26-.01-1.13-.02-2.05-3.05.66-3.7-1.47-3.7-1.47-.5-1.26-1.22-1.6-1.22-1.6-.99-.68.08-.66.08-.66 1.1.08 1.67 1.13 1.67 1.13.98 1.67 2.57 1.19 3.2.91.1-.71.38-1.19.69-1.46-2.43-.28-4.99-1.22-4.99-5.45 0-1.2.43-2.18 1.13-2.95-.11-.28-.49-1.42.11-2.96 0 0 .92-.3 3.02 1.12.87-.24 1.8-.36 2.73-.36s1.86.12 2.73.36c2.1-1.42 3.02-1.12 3.02-1.12.59 1.54.22 2.68.11 2.96.7.77 1.13 1.75 1.13 2.95 0 4.24-2.57 5.17-5.01 5.44.39.34.74 1.01.74 2.03 0 1.46-.01 2.63-.01 2.99 0 .29.2.64.76.53 4.35-1.45 7.49-5.56 7.49-10.41C23.02 5.24 18.27.5 12 .5z"/></svg>
                GitHub
              </a>
            </div>
          </div>
          <div class="relative">
            <div class="absolute -inset-2 rounded-3xl bg-gradient-to-r from-indigo-500/40 to-cyan-500/40 blur-2xl -z-10"></div>
            <div class="rounded-3xl border border-white/10 bg-white/5 backdrop-blur-xl p-6">
              <div class="aspect-[4/3] rounded-2xl border border-white/10 bg-slate-900/60 flex items-center justify-center">
                <div class="text-center p-6">
                  <p class="text-sm text-slate-400">Feature highlight</p>
                  <h3 class="mt-2 text-xl font-bold">Neon Glass UI</h3>
                  <p class="mt-2 text-slate-300/90">Cards with layered gradients, tasteful blur, and hover motion. Clean, fast, and mobile-first.</p>
                </div>
              </div>
              <ul class="mt-5 grid grid-cols-2 gap-3 text-sm text-slate-300/90">
                <li class="flex items-center gap-2"><span class="h-1.5 w-1.5 rounded-full bg-emerald-400"></span>Dark mode</li>
                <li class="flex items-center gap-2"><span class="h-1.5 w-1.5 rounded-full bg-indigo-400"></span>Responsive</li>
                <li class="flex items-center gap-2"><span class="h-1.5 w-1.5 rounded-full bg-cyan-400"></span>Single-file</li>
                <li class="flex items-center gap-2"><span class="h-1.5 w-1.5 rounded-full bg-fuchsia-400"></span>Accessible</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects" class="py-16">
      <div class="max-w-6xl mx-auto px-4">
        <div class="flex items-end justify-between gap-4">
          <h2 class="text-2xl sm:text-3xl font-extrabold">Selected Projects</h2>
          <a href="https://github.com/yourhandle?tab=repositories" target="_blank" rel="noreferrer" class="text-sm text-slate-300 hover:text-white">See all →</a>
        </div>

        <div class="mt-8 grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <!-- Card -->
          <article class="group relative rounded-3xl border border-white/10 bg-white/5 backdrop-blur-xl p-5 hover:translate-y-[-2px] transition will-change-transform">
            <div class="absolute -inset-px rounded-3xl bg-gradient-to-r from-indigo-500/20 to-cyan-500/20 opacity-0 group-hover:opacity-100 transition -z-10"></div>
            <div class="flex items-center justify-between gap-3">
              <h3 class="text-lg font-semibold">Project One</h3>
              <span class="text-xs text-slate-400">TypeScript</span>
            </div>
            <p class="mt-2 text-sm text-slate-300/90">High-performance landing page generator with AI copy and components.</p>
            <div class="mt-4 flex items-center gap-3 text-sm">
              <a class="inline-flex items-center gap-1 px-3 py-1.5 rounded-lg bg-white/5 border border-white/10 hover:bg-white/10 transition" href="https://github.com/yourhandle/project-one" target="_blank" rel="noreferrer">Repo</a>
              <a class="inline-flex items-center gap-1 px-3 py-1.5 rounded-lg bg-white/5 border border-white/10 hover:bg-white/10 transition" href="#" target="_blank" rel="noreferrer">Live</a>
            </div>
          </article>

          <article class="group relative rounded-3xl border border-white/10 bg-white/5 backdrop-blur-xl p-5 hover:translate-y-[-2px] transition">
            <div class="absolute -inset-px rounded-3xl bg-gradient-to-r from-fuchsia-500/20 to-indigo-500/20 opacity-0 group-hover:opacity-100 transition -z-10"></div>
            <div class="flex items-center justify-between gap-3">
              <h3 class="text-lg font-semibold">Project Two</h3>
              <span class="text-xs text-slate-400">Python</span>
            </div>
            <p class="mt-2 text-sm text-slate-300/90">Telegram growth automations: capture, segment, and nurture in-chat.</p>
            <div class="mt-4 flex items-center gap-3 text-sm">
              <a class="inline-flex items-center gap-1 px-3 py-1.5 rounded-lg bg-white/5 border border-white/10 hover:bg-white/10 transition" href="https://github.com/yourhandle/project-two" target="_blank" rel="noreferrer">Repo</a>
              <a class="inline-flex items-center gap-1 px-3 py-1.5 rounded-lg bg-white/5 border border-white/10 hover:bg-white/10 transition" href="#" target="_blank" rel="noreferrer">Live</a>
            </div>
          </article>

          <article class="group relative rounded-3xl border border-white/10 bg-white/5 backdrop-blur-xl p-5 hover:translate-y-[-2px] transition">
            <div class="absolute -inset-px rounded-3xl bg-gradient-to-r from-emerald-500/20 to-cyan-500/20 opacity-0 group-hover:opacity-100 transition -z-10"></div>
            <div class="flex items-center justify-between gap-3">
              <h3 class="text-lg font-semibold">Project Three</h3>
              <span class="text-xs text-slate-400">Go</span>
            </div>
            <p class="mt-2 text-sm text-slate-300/90">Fast API boilerplate with auth, tests, and observability baked in.</p>
            <div class="mt-4 flex items-center gap-3 text-sm">
              <a class="inline-flex items-center gap-1 px-3 py-1.5 rounded-lg bg-white/5 border border-white/10 hover:bg-white/10 transition" href="https://github.com/yourhandle/project-three" target="_blank" rel="noreferrer">Repo</a>
              <a class="inline-flex items-center gap-1 px-3 py-1.5 rounded-lg bg-white/5 border border-white/10 hover:bg-white/10 transition" href="#" target="_blank" rel="noreferrer">Live</a>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- About -->
    <section id="about" class="py-16">
      <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-3 gap-10">
        <div class="md:col-span-1">
          <h2 class="text-2xl sm:text-3xl font-extrabold">About</h2>
          <p class="mt-2 text-slate-300/90">Short, punchy bio. What you build, your leverage, and what you’re looking for.</p>
        </div>
        <div class="md:col-span-2">
          <div class="rounded-3xl border border-white/10 bg-white/5 backdrop-blur-xl p-6">
            <ul class="grid sm:grid-cols-2 gap-4 text-sm text-slate-300/90">
              <li class="flex items-center gap-3"><span class="h-2 w-2 rounded-full bg-indigo-400"></span> Rapid prototyping & product strategy</li>
              <li class="flex items-center gap-3"><span class="h-2 w-2 rounded-full bg-cyan-400"></span> AI + automation systems</li>
              <li class="flex items-center gap-3"><span class="h-2 w-2 rounded-full bg-emerald-400"></span> Design systems & clean UX</li>
              <li class="flex items-center gap-3"><span class="h-2 w-2 rounded-full bg-fuchsia-400"></span> Performance-first web dev</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="py-16">
      <div class="max-w-6xl mx-auto px-4">
        <div class="rounded-3xl border border-white/10 bg-white/5 backdrop-blur-xl p-8">
          <div class="flex flex-col md:flex-row items-start md:items-center justify-between gap-6">
            <div>
              <h2 class="text-2xl sm:text-3xl font-extrabold">Let’s build</h2>
              <p class="mt-2 text-slate-300/90">For collabs, consulting, or intros, get in touch.</p>
            </div>
            <div class="flex flex-wrap items-center gap-3">
              <a href="mailto:you@example.com" class="inline-flex items-center gap-2 px-4 py-2 rounded-xl font-semibold bg-white/10 border border-white/10 hover:bg-white/15 hover:border-white/20 transition">Email</a>
              <a href="https://twitter.com/yourhandle" target="_blank" rel="noreferrer" class="inline-flex items-center gap-2 px-4 py-2 rounded-xl border border-white/10 hover:border-white/20 bg-white/5 hover:bg-white/10 transition">Twitter</a>
              <a href="https://www.linkedin.com/in/yourhandle/" target="_blank" rel="noreferrer" class="inline-flex items-center gap-2 px-4 py-2 rounded-xl border border-white/10 hover:border-white/20 bg-white/5 hover:bg-white/10 transition">LinkedIn</a>
            </div>
          </div>
        </div>
        <p class="mt-8 text-xs text-slate-400/80">© <span id="year"></span> yourname. Built with a single HTML file, Tailwind CDN, and taste.</p>
      </div>
    </section>

    <script>
      // Dark mode toggle with localStorage
      const toggle = document.getElementById('themeToggle');
      const iconMoon = document.getElementById('iconMoon');
      const iconSun = document.getElementById('iconSun');
      const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
      const stored = localStorage.getItem('theme');
      const root = document.documentElement;

      function setTheme(mode){
        if(mode === 'light'){ root.classList.remove('dark'); iconMoon.classList.remove('hidden'); iconSun.classList.add('hidden'); }
        else { root.classList.add('dark'); iconMoon.classList.add('hidden'); iconSun.classList.remove('hidden'); }
      }
      setTheme(stored || (prefersDark ? 'dark' : 'light'));
      toggle.addEventListener('click', () => {
        const next = root.classList.contains('dark') ? 'light' : 'dark';
        localStorage.setItem('theme', next);
        setTheme(next);
      });

      // Year
      document.getElementById('year').textContent = new Date().getFullYear();
    </script>
  </body>
</html>
