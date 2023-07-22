<template>
  <GlobalSection color="white" title="Experience Tesla" subtitle="Schedule a Demo Drive Today">


    <template v-slot:footer>
      <a href="#"
        class="text-white text-[14px] border-[3px] border-white bg-white/5 backdrop-blur-sm rounded font-medium px-14 py-2 hover:bg-white hover:text-black transition-colors">
        Demo Drive
      </a>
    </template>


    <template v-slot:background>
      <video class="object-center object-cover h-full w-full" autoplay muted loop src="/video-landing.webm"></video>
    </template>


  </GlobalSection>










  <!-- <section class="landing-section bg-black h-screen w-screen text-center relative overflow-hidden"
    data-header-color="white">

    <div class="z-30 relative h-full flex flex-col">
      <header>
        <h2 class="text-white pt-40 text-[40px] font-medium">Experience Tesla</h2>
        <p class="text-white text-sm">Schedule a Demo Drive Today</p>
      </header>

      <footer class="flex flex-col flex-grow justify-end pb-20">
        <div>

        </div>
      </footer>
    </div>

    <div class="absolute top-0 bottom-0 h-full w-full z-10">

    </div>
  </section> -->
</template>

<script>
import GlobalSection from './GlobalSection.vue'

export default {
  components:{
    GlobalSection,
  }
}
</script>

<style></style>