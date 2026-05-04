<script setup>
const projects = [
  {
    id: 1,
    title: 'KosKita',
    category: 'Management System',
    tech: ['Laravel 11', 'React 19', 'Tailwind v4'],
    link: '#'
  },
  {
    id: 2,
    title: 'LibroModern',
    category: 'Digital Library',
    tech: ['React', 'Google Apps Script'],
    link: '#'
  },
  {
    id: 3,
    title: 'DompetKu AI',
    category: 'Financial Tracker',
    tech: ['Vue', 'AI Advisory'],
    link: '#'
  },
  {
    id: 4,
    title: 'TypeLab Arena',
    category: 'Web Platform',
    tech: ['React 19', 'Vite 8'],
    link: '#'
  }
]
</script>

<template>
  <section id="portfolio" class="py-32 px-6 bg-white font-poppins">
    <div class="max-w-7xl mx-auto">

      <!-- Section Header -->
      <div class="flex flex-col md:flex-row md:items-end justify-between mb-20 gap-8">
        <div class="max-w-2xl">
          <h2 class="text-[10px] font-bold uppercase tracking-[0.5em] text-[#8B5CF6] mb-6">Selected Works</h2>
          <h3 class="text-5xl md:text-7xl font-bold tracking-tighter text-[#1A1A1A] leading-[0.9]">
            Recent<br />Projects.
          </h3>
        </div>
        <p class="max-w-xs text-zinc-500 font-light text-lg">
          Koleksi sistem web kompleks dengan standar industri untuk kebutuhan akademik.
        </p>
      </div>

      <!-- Portfolio Grid -->
      <div class="grid md:grid-cols-2 gap-x-12 gap-y-24">
        <div
          v-for="(project, index) in projects"
          :key="project.id"
          :class="['group cursor-pointer', index % 2 !== 0 ? 'md:mt-24' : '']"
        >
          <!-- Project Image Placeholder -->
          <div class="relative aspect-video bg-zinc-100 rounded-[2rem] overflow-hidden mb-8 transition-all duration-500 group-hover:shadow-2xl group-hover:shadow-purple-500/10 border border-zinc-100">
            <div class="absolute inset-0 bg-gradient-to-br from-[#8B5CF6]/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity"></div>
            <!-- Simbol panah muncul saat hover -->
            <div class="absolute top-6 right-6 w-12 h-12 bg-white rounded-full flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all transform translate-y-2 group-hover:translate-y-0">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="#1A1A1A" class="w-5 h-5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25" />
              </svg>
            </div>
          </div>

          <!-- Project Info -->
          <div class="px-2">
            <div class="flex items-center gap-3 mb-4">
              <span class="text-[10px] font-bold uppercase tracking-widest text-[#8B5CF6] bg-purple-50 px-3 py-1 rounded-full">
                {{ project.category }}
              </span>
            </div>
            <h4 class="text-3xl font-bold text-[#1A1A1A] mb-4 tracking-tight group-hover:text-[#8B5CF6] transition-colors">
              {{ project.title }}
            </h4>

            <!-- Tech Badges -->
            <div class="flex flex-wrap gap-2">
              <span
                v-for="t in project.tech"
                :key="t"
                class="text-[11px] font-medium text-zinc-400 border border-zinc-100 px-3 py-1 rounded-md"
              >
                {{ t }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
