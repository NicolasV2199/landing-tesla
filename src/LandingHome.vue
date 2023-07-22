<template>
  <HomeHeader />

  <main class="snap-y snap-mandatory relative w-full h-screen overflow-y-auto scroll overflow-x-hidden">
    <div class="snap-center">
      <InitialSection />
    </div>

    <div class="snap-center">
      <ModelThreeSection />
    </div>

    <div class="snap-center">
      <ModelYSection />
    </div>

    <div class="snap-center">
      <ModelSSection />
    </div>

    <div class="snap-center">
      <ModelXSection />
    </div>

    <div class="snap-center">
      <SolarPanelsSection />
    </div>

    <div class="snap-center">
      <SolarRoofSection />
    </div>

    <div class="snap-center">
      <PowerWallSection />
    </div>

    <div class="snap-center">
      <AccessoriesSection />
    </div>

  </main>
</template>

<script>
import HomeHeader from './components/HomeHeader.vue'
import InitialSection from './components/InitialSection.vue';
import ModelThreeSection from './components/ModelThreeSection.vue';
import ModelYSection from './components/ModelYSection.vue';
import ModelSSection from './components/ModelSSection.vue';
import ModelXSection from './components/ModelXSection.vue';
import SolarPanelsSection from './components/SolarPanelsSection.vue';
import SolarRoofSection from './components/SolarRoofSection.vue';
import PowerWallSection from './components/PowerWallSection.vue';
import AccessoriesSection from './components/AccessoriesSection.vue';
export default {

  metadata: {
    title: 'Titulo de prueba'
  },

  components: {
    HomeHeader,
    InitialSection,
    ModelThreeSection,
    ModelYSection,
    ModelSSection,
    ModelXSection,
    SolarPanelsSection,
    SolarRoofSection,
    PowerWallSection,
    AccessoriesSection,
  },



}
</script>

<style></style>