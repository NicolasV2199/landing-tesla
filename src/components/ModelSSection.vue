<template>
  <GlobalSection color="black" title="Model S" subtitle="Explore Inventory">


    <template v-slot:footer>
      <a href="#"
        class="text-[14px] border-[#d8d6d6] border-2 bg-[#d8d6d6] backdrop-blur-sm rounded font-medium px-14 py-1.5 hover:bg-white hover:text-black transition-colors">
        Custom Order
      </a>
      <a href="#"
        class="text-white text-[14px] border-2 border-black/5 bg-black/50 rounded font-medium px-14 py-1.5 hover:bg-black transition-colors">
        Demo Drive
      </a>
    </template>


    <template v-slot:background>
      <img src="/model-s.avif" alt="Model 3 tesla" class="h-full w-full object-cover object-center">
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