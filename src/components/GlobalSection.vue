<template>
  <section class="landing-section bg-black h-screen w-screen text-center relative overflow-hidden"
    :data-header-color="color">

    <div class="z-30 relative h-full flex flex-col">
      <header>
        <h2 :class="`text-${color} pt-32 text-[36px] font-medium`">{{ title }}</h2>
        <p :class="`text-${color} text-[14px]`">
          {{ subtitle }} <br>
          {{ subtitle2 }}
        </p>
      </header>

      <footer class="flex flex-col flex-grow justify-end pb-16">
        <div class="flex gap-x-6 justify-center">
          <slot name="footer"/>
        </div>
      </footer>
      <slot name="aditional-footer"/>
    </div>

    <div class="absolute top-0 bottom-0 h-full w-full z-10">
      <slot name="background"/>
    </div>
  </section>
</template>

<script>
export default {

  props: {
    color: {
      type: String,
      required: true,
      default: "white"
    },
    title: {
      type: String,
      required: true,
      default: ""
    },
    subtitle: {
      type: String,
      required: false,
      default: "",
    },
    subtitle2: {
      type: String,
      required: false,
      default: "",
    }
  }, 

}
</script>

<style></style>