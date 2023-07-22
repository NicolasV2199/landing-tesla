<template>
  <GlobalSection color="black" title="Model Y" subtitle="Starting at $40,240" subtitle2="After Federal Tax Credit">


    <template v-slot:footer>
      <a href="#"
        class="text-[14px] border-[#F4F4F4CC] border-2 bg-[#F4F4F4CC] backdrop-blur-sm rounded font-medium px-14 py-1.5 hover:bg-white hover:text-black transition-colors">
        Explore Inventory
      </a>
      <a href="#"
        class="text-white text-[14px] border-2 border-black/5 bg-black/50 rounded font-medium px-14 py-1.5 hover:bg-black transition-colors">
        Custom Order
      </a>
    </template>


    <template v-slot:background>
      <img src="/model-y.avif" alt="Model 3 tesla" class="h-full w-full object-cover object-center">
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