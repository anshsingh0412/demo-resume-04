 <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    html { scroll-behavior: smooth; }
    :root { --ring: 0 0% 100%; }
    .glass { backdrop-filter: blur(8px); background: rgba(255,255,255,0.6); }
    .dark .glass { background: rgba(17,24,39,0.6); }
    .shine {
      position: relative;
      overflow: hidden;
    }
    .shine::after{
      content:""; position:absolute; inset:-150% -150% auto auto; width:50%; height:300%;
      transform: rotate(25deg); background: linear-gradient(90deg, transparent, rgba(255,255,255,.2), transparent);
      animation: shine 4s linear infinite;
    }
    @keyframes shine{ 0%{ transform:translateX(-200%) rotate(25deg);} 100%{ transform:translateX(200%) rotate(25deg);} }
  </style>
</head>
<body class="bg-zinc-50 text-zinc-900 dark:bg-zinc-950 dark:text-zinc-100 font-[Inter]">

  <!-- Header -->
  <header class="fixed top-0 left-0 right-0 z-50">
    <div class="max-w-6xl mx-auto px-4">
      <div class="mt-4 flex items-center justify-between rounded-2xl glass border border-zinc-200/60 dark:border-zinc-800/60 p-2 shadow-lg">
        <a href="#home" class="flex items-center gap-3 px-2">
          <div class="h-10 w-10 rounded-xl bg-gradient-to-br from-indigo-500 via-sky-500 to-emerald-500"></div>
          <span class="font-semibold tracking-tight">Ansh Singh</span>
        </a>
        <nav class="hidden md:flex items-center gap-1">
          <a class="px-4 py-2 rounded-xl hover:bg-zinc-900 hover:text-white dark:hover:bg-white dark:hover:text-zinc-950 transition" href="#about">About</a>
          <a class="px-4 py-2 rounded-xl hover:bg-zinc-900 hover:text-white dark:hover:bg-white dark:hover:text-zinc-950 transition" href="#skills">Skills</a>
          <a class="px-4 py-2 rounded-xl hover:bg-zinc-900 hover:text-white dark:hover:bg-white dark:hover:text-zinc-950 transition" href="#projects">Projects</a>
          <a class="px-4 py-2 rounded-xl hover:bg-zinc-900 hover:text-white dark:hover:bg-white dark:hover:text-zinc-950 transition" href="#experience">Experience</a>
          <a class="px-4 py-2 rounded-xl hover:bg-zinc-900 hover:text-white dark:hover:bg-white dark:hover:text-zinc-950 transition" href="#achievements">Achievements</a>
        </nav>
        <div class="flex items-center gap-2">
          <a href="#projects" class="hidden sm:inline-flex items-center gap-2 px-4 py-2 rounded-xl bg-zinc-900 text-white dark:bg-white dark:text-zinc-950 hover:opacity-90 transition">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" viewBox="0 0 24 24" fill="currentColor"><path d="M4 4h16v2H4zM4 11h16v2H4zM4 18h16v2H4z"/></svg>
            View Work
          </a>
          <button id="themeToggle" class="p-2 rounded-xl border border-zinc-200 dark:border-zinc-800 hover:bg-zinc-100 dark:hover:bg-zinc-900" title="Toggle theme">
            <svg id="sun" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 hidden" viewBox="0 0 24 24" fill="currentColor"><path d="M6.76 4.84l-1.8-1.79-1.41 1.41 1.79 1.8 1.42-1.42zM1 13h3v-2H1v2zm10 10h2v-3h-2v3zM4.95 19.05l1.41 1.41 1.8-1.79-1.42-1.42-1.79 1.8zM20 11v2h3v-2h-3zm-3.76-6.16l1.42 1.42 1.79-1.8-1.41-1.41-1.8 1.79zM13 1h-2v3h2V1zm5.05 18.05l-1.8-1.79-1.42 1.42 1.79 1.8 1.43-1.43z"/><circle cx="12" cy="12" r="5"/></svg>
            <svg id="moon" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 24 24" fill="currentColor"><path d="M21.64 13A9 9 0 1111 2.36 7 7 0 1021.64 13z"/></svg>
          </button>
          <button class="md:hidden p-2 rounded-xl border border-zinc-200 dark:border-zinc-800" id="menuBtn" aria-label="Open menu">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 24 24" fill="currentColor"><path d="M4 6h16v2H4zM4 11h16v2H4zM4 16h16v2H4z"/></svg>
          </button>
        </div>
      </div>
      <div id="mobileMenu" class="md:hidden hidden mt-2 glass border border-zinc-200/60 dark:border-zinc-800/60 rounded-2xl p-2">
        <a class="block px-4 py-2 rounded-xl hover:bg-zinc-900 hover:text-white dark:hover:bg-white dark:hover:text-zinc-950" href="#about">About</a>
        <a class="block px-4 py-2 rounded-xl hover:bg-zinc-900 hover:text-white dark:hover:bg-white dark:hover:text-zinc-950" href="#skills">Skills</a>
        <a class="block px-4 py-2 rounded-xl hover:bg-zinc-900 hover:text-white dark:hover:bg-white dark:hover:text-zinc-950" href="#projects">Projects</a>
        <a class="block px-4 py-2 rounded-xl hover:bg-zinc-900 hover:text-white dark:hover:bg-white dark:hover:text-zinc-950" href="#experience">Experience</a>
        <a class="block px-4 py-2 rounded-xl hover:bg-zinc-900 hover:text-white dark:hover:bg-white dark:hover:text-zinc-950" href="#achievements">Achievements</a>
      </div>
    </div>
  </header>

  <!-- Hero -->
  <section id="home" class="relative pt-40 pb-24">
    <div class="absolute inset-0 -z-10">
      <div class="absolute inset-0 bg-gradient-to-br from-indigo-200 via-sky-100 to-emerald-200 opacity-40 dark:opacity-10"></div>
      <div class="absolute -top-24 -left-24 h-[28rem] w-[28rem] rounded-full blur-3xl bg-indigo-500/20"></div>
      <div class="absolute -bottom-24 -right-24 h-[28rem] w-[28rem] rounded-full blur-3xl bg-emerald-500/20"></div>
    </div>
    <div class="max-w-6xl mx-auto px-4">
      <div class="grid md:grid-cols-2 gap-10 items-center">
        <div>
          <p class="inline-flex items-center gap-2 text-xs font-medium px-3 py-1 rounded-full border border-zinc-200 dark:border-zinc-800">
            <span class="h-2 w-2 rounded-full bg-emerald-500"></span> Open to Work
          </p>
          <h1 class="mt-4 text-4xl sm:text-5xl font-extrabold tracking-tight leading-tight">Hi, I'm <span class="text-transparent bg-clip-text bg-gradient-to-r from-indigo-600 via-sky-600 to-emerald-600">Ansh Singh</span></h1>
          <p class="mt-4 text-zinc-600 dark:text-zinc-400">A passionate Front‑End Developer crafting fast, accessible and beautiful web experiences. I love building pixel‑perfect UIs and bringing ideas to life.</p>
          <div class="mt-6 flex flex-wrap gap-3">
            <a href="#projects" class="shine inline-flex items-center gap-2 px-5 py-3 rounded-2xl bg-zinc-900 text-white dark:bg-white dark:text-zinc-950 shadow-lg">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 24 24" fill="currentColor"><path d="M4 4h16v2H4zM4 11h16v2H4zM4 18h16v2H4z"/></svg>
              See Projects
            </a>
            <a href="mailto:youremail@example.com" class="inline-flex items-center gap-2 px-5 py-3 rounded-2xl border border-zinc-300 dark:border-zinc-700">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 24 24" fill="currentColor"><path d="M12 13L2 6.76V18a2 2 0 002 2h16a2 2 0 002-2V6.76L12 13z"/><path d="M22 6H2l10 7 10-7z"/></svg>
              Email
            </a>
            <a href="./Ansh_Singh_Resume.pdf" download class="inline-flex items-center gap-2 px-5 py-3 rounded-2xl border border-zinc-300 dark:border-zinc-700">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 24 24" fill="currentColor"><path d="M5 20h14v-2H5v2zM11 4v8.59L8.71 10.3 7.29 11.7 12 16.41l4.71-4.71-1.42-1.41L13 12.59V4h-2z"/></svg>
              Download CV
            </a>
          </div>
          <div class="mt-6 flex items-center gap-4 text-sm text-zinc-500 dark:text-zinc-400">
            <a href="#" class="hover:underline">GitHub</a>
            <a href="#" class="hover:underline">LinkedIn</a>
            <a href="#" class="hover:underline">Twitter</a>
          </div>
        </div>
        <div class="relative">
          <div class="absolute -inset-4 rounded-3xl bg-gradient-to-tr from-indigo-500/20 via-sky-500/20 to-emerald-500/20 blur-2xl"></div>
          <img src="https://images.unsplash.com/photo-1516387938699-a93567ec168e?q=80&w=1200&auto=format&fit=crop" alt="Profile" class="relative w-full rounded-3xl border border-zinc-200 dark:border-zinc-800 shadow-2xl" />
        </div>
      </div>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="py-20">
    <div class="max-w-6xl mx-auto px-4">
      <div class="grid md:grid-cols-3 gap-8 items-start">
        <div class="md:col-span-1">
          <h2 class="text-2xl font-bold">About</h2>
          <p class="mt-2 text-zinc-500">Who I am & what I do</p>
        </div>
        <div class="md:col-span-2 space-y-4">
          <p class="text-zinc-700 dark:text-zinc-300">I'm a front‑end developer focused on building delightful web apps with modern stacks. I enjoy working with React, Tailwind CSS and TypeScript, and I care about performance and accessibility.</p>
          <div class="grid sm:grid-cols-3 gap-4">
            <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800">
              <p class="text-3xl font-extrabold">2+</p>
              <p class="text-zinc-500">Years Experience</p>
            </div>
            <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800">
              <p class="text-3xl font-extrabold">15+</p>
              <p class="text-zinc-500">Projects</p>
            </div>
            <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800">
              <p class="text-3xl font-extrabold">5</p>
              <p class="text-zinc-500">Happy Clients</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Skills -->
  <section id="skills" class="py-20 bg-white/60 dark:bg-zinc-900/40">
    <div class="max-w-6xl mx-auto px-4">
      <div class="flex items-end justify-between">
        <div>
          <h2 class="text-2xl font-bold">Skills</h2>
          <p class="mt-2 text-zinc-500">Tech I work with</p>
        </div>
        <div class="text-sm text-zinc-500">Always learning 🚀</div>
      </div>
      <div class="mt-8 grid sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
        <!-- skill card -->
        <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">HTML & CSS</p>
          <p class="text-sm text-zinc-500">Semantic HTML, Flexbox, Grid, Animations</p>
        </div>
        <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">JavaScript / TypeScript</p>
          <p class="text-sm text-zinc-500">ES6+, Async, API Integration</p>
        </div>
        <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">React</p>
          <p class="text-sm text-zinc-500">Hooks, Context, SPA</p>
        </div>
        <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">Tailwind CSS</p>
          <p class="text-sm text-zinc-500">Utility‑first design</p>
        </div>
        <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">Node.js</p>
          <p class="text-sm text-zinc-500">Express, REST APIs</p>
        </div>
        <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">Git & GitHub</p>
          <p class="text-sm text-zinc-500">Version control, PRs</p>
        </div>
        <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">Figma</p>
          <p class="text-sm text-zinc-500">Wireframes, UI</p>
        </div>
        <div class="p-4 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">SEO & Performance</p>
          <p class="text-sm text-zinc-500">Lighthouse, Core Web Vitals</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects -->
  <section id="projects" class="py-20">
    <div class="max-w-6xl mx-auto px-4">
      <div class="flex items-end justify-between">
        <div>
          <h2 class="text-2xl font-bold">Projects</h2>
          <p class="mt-2 text-zinc-500">Things I've built</p>
        </div>
        <a href="https://github.com/" class="text-sm underline">All Projects →</a>
      </div>

      <div class="mt-8 grid md:grid-cols-2 gap-6">
        <!-- Project card 1 -->
        <article class="group relative overflow-hidden rounded-3xl border border-zinc-200 dark:border-zinc-800">
          <img class="h-56 w-full object-cover" src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?q=80&w=1200&auto=format&fit=crop" alt="Project" />
          <div class="p-5 bg-white dark:bg-zinc-900">
            <h3 class="font-semibold">Portfolio Website</h3>
            <p class="mt-1 text-sm text-zinc-500">A blazing fast personal site built with HTML, Tailwind and vanilla JS.</p>
            <div class="mt-3 flex gap-3 text-xs text-zinc-500">
              <span class="px-2 py-1 rounded-lg bg-zinc-100 dark:bg-zinc-800">HTML</span>
              <span class="px-2 py-1 rounded-lg bg-zinc-100 dark:bg-zinc-800">Tailwind</span>
              <span class="px-2 py-1 rounded-lg bg-zinc-100 dark:bg-zinc-800">JS</span>
            </div>
            <div class="mt-4 flex items-center gap-4 text-sm">
              <a href="#" class="inline-flex items-center gap-1 underline">Live</a>
              <a href="#" class="inline-flex items-center gap-1 underline">Code</a>
            </div>
          </div>
        </article>

        <!-- Project card 2 -->
        <article class="group relative overflow-hidden rounded-3xl border border-zinc-200 dark:border-zinc-800">
          <img class="h-56 w-full object-cover" src="https://images.unsplash.com/photo-1515879218367-8466d910aaa4?q=80&w=1200&auto=format&fit=crop" alt="Project" />
          <div class="p-5 bg-white dark:bg-zinc-900">
            <h3 class="font-semibold">Task Manager App</h3>
            <p class="mt-1 text-sm text-zinc-500">A simple tasks app with filters, persistence and keyboard shortcuts.</p>
            <div class="mt-3 flex gap-3 text-xs text-zinc-500">
              <span class="px-2 py-1 rounded-lg bg-zinc-100 dark:bg-zinc-800">React</span>
              <span class="px-2 py-1 rounded-lg bg-zinc-100 dark:bg-zinc-800">TypeScript</span>
              <span class="px-2 py-1 rounded-lg bg-zinc-100 dark:bg-zinc-800">Vite</span>
            </div>
            <div class="mt-4 flex items-center gap-4 text-sm">
              <a href="#" class="inline-flex items-center gap-1 underline">Live</a>
              <a href="#" class="inline-flex items-center gap-1 underline">Code</a>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>

  <!-- Experience -->
  <section id="experience" class="py-20 bg-white/60 dark:bg-zinc-900/40">
    <div class="max-w-6xl mx-auto px-4">
      <h2 class="text-2xl font-bold">Experience</h2>
      <p class="mt-2 text-zinc-500">Where I've worked</p>

      <div class="mt-8 space-y-6">
        <div class="rounded-2xl border border-zinc-200 dark:border-zinc-800 p-5">
          <div class="flex items-center justify-between gap-4">
            <div>
              <p class="font-semibold">Front‑End Developer — Freelance</p>
              <p class="text-sm text-zinc-500">Jan 2024 — Present</p>
            </div>
            <div class="text-sm text-zinc-500">Remote</div>
          </div>
          <ul class="mt-3 list-disc pl-5 text-sm text-zinc-600 dark:text-zinc-300 space-y-1">
            <li>Built landing pages and SPAs with React/Tailwind that score 95+ on Lighthouse.</li>
            <li>Collaborated with clients to refine UX and ship features faster.</li>
            <li>Set up CI workflows and automated deployments to Vercel & GitHub Pages.</li>
          </ul>
        </div>
        <div class="rounded-2xl border border-zinc-200 dark:border-zinc-800 p-5">
          <div class="flex items-center justify-between gap-4">
            <div>
              <p class="font-semibold">UI Designer — Part‑time</p>
              <p class="text-sm text-zinc-500">Jun 2023 — Dec 2023</p>
            </div>
            <div class="text-sm text-zinc-500">Lucknow, IN</div>
          </div>
          <ul class="mt-3 list-disc pl-5 text-sm text-zinc-600 dark:text-zinc-300 space-y-1">
            <li>Designed component library for a startup—reduced dev rework by 30%.</li>
            <li>Improved accessibility and color contrast across pages.</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- Achievements -->
  <section id="achievements" class="py-20">
    <div class="max-w-6xl mx-auto px-4">
      <h2 class="text-2xl font-bold">Achievements</h2>
      <p class="mt-2 text-zinc-500">Highlights I'm proud of</p>
      <div class="mt-8 grid md:grid-cols-3 gap-4">
        <div class="p-5 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">#1 Hackathon Winner</p>
          <p class="text-sm text-zinc-500">Built an AI‑powered UI kit in 24 hours.</p>
        </div>
        <div class="p-5 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">Open‑source Contributor</p>
          <p class="text-sm text-zinc-500">Contributed to popular Tailwind plugins.</p>
        </div>
        <div class="p-5 rounded-2xl border border-zinc-200 dark:border-zinc-800 bg-white dark:bg-zinc-900">
          <p class="font-semibold">100 Days of Code</p>
          <p class="text-sm text-zinc-500">Completed the challenge with daily commits.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer (No contact form) -->
  <footer class="py-10 border-t border-zinc-200 dark:border-zinc-800">
    <div class="max-w-6xl mx-auto px-4 flex flex-col sm:flex-row items-center justify-between gap-4">
      <p class="text-sm text-zinc-500">© <span id="year"></span> Ansh Singh. All rights reserved.</p>
      <div class="flex items-center gap-4 text-sm">
        <a href="#home" class="underline">Back to top</a>
        <a href="mailto:youremail@example.com" class="underline">Email</a>
        <a href="#" class="underline">GitHub</a>
        <a href="#" class="underline">LinkedIn</a>
      </div>
    </div>
  </footer>

  <script>
    // Year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Theme toggle
    const themeBtn = document.getElementById('themeToggle');
    const sun = document.getElementById('sun');
    const moon = document.getElementById('moon');
    const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
    const stored = localStorage.getItem('theme');
    if (stored === 'dark' || (!stored && prefersDark)) {
      document.documentElement.classList.add('dark');
      sun.classList.remove('hidden');
      moon.classList.add('hidden');
    }
    themeBtn.addEventListener('click', () => {
      const isDark = document.documentElement.classList.toggle('dark');
      localStorage.setItem('theme', isDark ? 'dark' : 'light');
      sun.classList.toggle('hidden');
      moon.classList.toggle('hidden');
    });

    // Mobile menu
    const menuBtn = document.getElementById('menuBtn');
    const mobileMenu = document.getElementById('mobileMenu');
    menuBtn.addEventListener('click', () => mobileMenu.classList.toggle('hidden'));

    // Close mobile menu on link click
    mobileMenu.querySelectorAll('a').forEach(a => a.addEventListener('click', () => mobileMenu.classList.add('hidden')));
  </script>
</body>
</html>
