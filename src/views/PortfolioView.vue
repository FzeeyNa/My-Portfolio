<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <h4>Past Project Experience</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300">
            Explore the projects I've worked on so far</h4>
        </div>
      </header>

      <section>
        <div class="grid grid-cols-1 gap-4 pb-32 md:grid-cols-3 md:gap-3 xl:grid-cols-3 xl:gap-3 2xl:gap-5 fade-zoom-in">
          <div v-for="item in items" :key="item.id">
            <div
              class="item-card flex flex-col items-center gap-2 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-amber-50 md:gap-3 px-5 py-5 lg:px-5">
              <div class="flex w-full items-center justify-center">
                <img :src="item.imageUrl" :alt="item.name" loading="lazy"
                  class="drop-shadow-xl rounded-xl w-full h-auto object-cover" />
              </div>

              <div class="w-full flex flex-col gap-2 items-center text-sm md:text-base lg:text-lg">
                <div class="title-text font-medium text-secondary text-center">{{ item.name }}</div>

                <div class="w-full text-left text-[10px] text-[#c1c1c1] md:text-xs lg:text-sm">
                  {{ item.status }}
                </div>

                <div class="w-full mt-4 text-sm text-left text-amber-200">
                  {{ item.tech }}
                </div>

                <div class="w-full flex justify-end">
                  <div class="flex items-end gap-2 text-primary">
                    <a v-if="item.github" :href="item.github" target="_blank" rel="noreferrer"
                      title="View github repository" class="transition-all hover:text-accent">
                      <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24"
                        stroke-linecap="round" stroke-linejoin="round" height="16" width="16"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22">
                        </path>
                      </svg>
                    </a>

                    <a v-if="item.demo" :href="item.demo" target="_blank" rel="noreferrer"
                      title="View finished project" class="transition-all hover:text-accent">
                      <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24"
                        stroke-linecap="round" stroke-linejoin="round" height="18" width="18"
                        xmlns="http://www.w3.org/2000/svg">
                        <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                        <polyline points="15 3 21 3 21 9"></polyline>
                        <line x1="10" y1="14" x2="21" y2="3"></line>
                      </svg>
                    </a>
                  </div>
                </div>
              </div>

            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeTab: 1,
      items: [
        {
          id: 1,
          name: 'Personal Website',
          imageUrl: '/img/portofolio-1.png', 
          status: 'My personal website to show profile, skills, and try new technologies.',
          tech: 'VueJS 3, Tailwind',
          github: 'https://github.com/rakha-elctrnx/Portofolio-v2',
          demo: 'https://fazryal-portofolio.netlify.app/'
        },
        {
          id: 2,
          name: 'RFID-Based Attendance System',
          imageUrl: '/img/2.png',
          status: 'A web-based application that uses RFID technology to automate and simplify student attendance tracking.',
          tech: 'Laravel 9, Bootstrap',
          github: 'https://github.com/FzeeyNa/presensi',
          demo: 'https://presensi.vpstjkt.my.id/'
        },
        {
          id: 3,
          name: 'Website SMK Prestasi Prima Profile',
          imageUrl: '/img/3.png',
          status: 'A web application profile SMK Prestasi Prima with admin management.',
          tech: 'Laravel 9, Bootstrap',
          github: 'https://github.com/FzeeyNa/Web-SMK',
          demo: null
        },
        {
          id: 4,
          name: 'SIAKAD-SMK',
          imageUrl: '/img/4.png',
          status: 'A web-based application for managing student attendance in SMK Prestasi Prima.',
          tech: 'Laravel 9, Bootstrap',
          github: 'https://github.com/FzeeyNa/Siakad-SMK',
          demo: null
        },
        {
          id: 5,
          name: 'SPPIE-PP',
          imageUrl: '/img/5.png',
          status: 'A web-based application for managing student tuition payments at SMK Prestasi Prima, developed as a big project my school.',
          tech: 'Laravel 9, Tailwind',
          github: 'https://github.com/FzeeyNa/TugasBesar-PresmaSPP',
          demo: null
        },
        {
          id: 6,
          name: 'Finalis DINAMIK-19 Competitive Programming',
          imageUrl: '/img/6.png',
          status: 'Finalist in the DINAMIK-19 competition in the Competitive Programming category.',
          tech: 'Python',
          github: 'https://github.com/FzeeyNa/DINAMIK-19-COMPETITIVE-PROGRAMMING.git',
          demo: null
        },
        {
          id: 7,
          name: ' LKS SMK 2024 JT 2 Cyber Security',
          imageUrl: '/img/7.jpg',
          status: '2nd Honorable Mention Winner at the 2024 Provincial LKS SMK Competition, JT 2 - Cyber Security category.',
          tech: 'Kali Linux',
          github: null,
          demo: null
 }
      ]
    };
  }
};
</script>

<style>
.item-card:hover {
  transition: transform 0.3s ease;
  transform: translateY(-8px);
}
svg:hover {
  stroke: #ffdb70;
}
@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
.fade-zoom-in {
  animation: fadeZoomIn 1s ease-in-out;
}
</style>
