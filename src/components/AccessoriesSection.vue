<template>
  <GlobalSection color="black" title="Accessories">


    <template v-slot:footer>
      <div class="w-screen">
        <a href="#"
          class="text-[14px] border-[#d8d6d6] border-2 bg-[#d8d6d6] backdrop-blur-sm rounded font-medium px-14 py-1.5 hover:bg-white hover:text-black transition-colors">
          Shop Now
        </a>
      </div>
    </template>


    <template v-slot:aditional-footer>
      <nav class="pb-3">
        <ul class="text-gray-300 flex text-[12px] [&>li]:font-medium [&>li]:px-2 [&>li]:py-2 justify-center">
          <li>Tesla &copy; 2023</li>
          <li>Privacy & Legal</li>
          <li>Vehicle Recalls</li>
          <li>Contact</li>
          <li>News</li>
          <li>Get Updates</li>
          <li>Locations</li>
        </ul>
      </nav>
    </template>


    <template v-slot:background>
      <img src="/accessories.avif" alt="Model 3 tesla" class="h-full w-full object-cover object-center">
    </template>


  </GlobalSection>
</template>

<script>
import GlobalSection from './GlobalSection.vue'

export default {

  components: {
    GlobalSection,
  }

}
</script>

<style></style>