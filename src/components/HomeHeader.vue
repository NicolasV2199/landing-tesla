<template>
  <div class="fixed top-0 z-40 w-full">
    <TopBar />
    <side-bar ref="homeSidebar"/>
    <header id="home-header" class="py-2 px-8 flex items-center w-full justify-between z-40 text-white">
  
  
      <div class="flex flex-grow basis-0">
        <a href="./">
          <MainLogo />
        </a>
      </div>
  
      <nav>
        <ul
          class="flex text-[14px] [&>li>a]:transition-colors [&>li>a]:duration-500 [&>li>a]:text-current [&>li>a]:font-medium 
            [&>li>a]:px-2 [&>li>a]:py-2 [&>li>a]:hidden [&>li>a]:xl:inline-block">
          <li><a href="#">Model S</a></li>
          <li><a href="#">Model 3</a></li>
          <li><a href="#">Model X</a></li>
          <li><a href="#">Model Y</a></li>
          <li><a href="#">Solar Roof</a></li>
          <li><a href="#">Solar Panels</a></li>
          <li><a href="#">Powerwall</a></li>
        </ul>
      </nav>
  
      <nav class="flex flex-grow justify-end basis-0">
        <ul
          class="flex text-[14px] [&>li>a]:transition-colors [&>li>a]:duration-500 [&>li>a]:text-current [&>li>a]:font-medium 
          [&>li>a]:px-4 [&>li>a]:py-2">
          <li><a href="#" class="hidden xl:inline-block">Shop</a></li>
          <li><a href="#" class="hidden xl:inline-block">Account</a></li>
          <li><a href="#" class="inline-block" @click="openMenu">Menu</a></li>
        </ul>
      </nav>
  
      <div id="menu-backdrop" class="absolute bg-black/5 backdrop-blur-lg rounded 
          translate-x-[var(--left)] translate-y-[var(--top)]
          top-0 left-0
          w-[var(--width)] h-[var(--height)]
          transition-all duration-300 ease-in-out opacity-0 -z-10">
      </div>
    </header>
  </div>
</template>

<script>
import SideBar from '@/SideBar.vue';

import MainLogo from './MainLogo.vue'
import TopBar from './TopBar.vue';
export default {

  components: {
    MainLogo,
    TopBar,
    SideBar
  },

  data() {
    return {

    }
  },

  methods: {

    openMenu(){
      this.$refs.homeSidebar.openSidebar();
    },

    adaptScroll() {
      const header = document.querySelector('#home-header');

      const observerOptions = {
        root: null, //defaults to viewport
        rootMargin: '0px', //As soon as you see the element
        threshold: 0.9, //View percent of the element
      }

      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          const { isIntersecting } = entry;
          if (isIntersecting) {
            const color = entry.target.getAttribute('data-header-color');
            header.style.color = color;
          }
        })
      }, observerOptions);

      const sections = document.querySelectorAll('.landing-section');
      sections.forEach((section) => observer.observe(section));

    },

    smoothItemChange() {
      const listItem = document.querySelectorAll("#home-header li");
      const menuBackdrop = document.querySelector("#menu-backdrop");

      listItem.forEach((item) => {
        item.addEventListener("mouseenter", () => {
          const { left, top, width, height } = item.getBoundingClientRect(); //Gives all the information of the element
          menuBackdrop.style.setProperty("--left", `${left}px`);
          menuBackdrop.style.setProperty("--top", `${top}px`);
          menuBackdrop.style.setProperty("--width", `${width}px`);
          menuBackdrop.style.setProperty("--height", `${height}px`);
          menuBackdrop.style.opacity = "1";
          menuBackdrop.style.visibility = "visible";
        })

        item.addEventListener("mouseleave", () => {
          menuBackdrop.style.opacity = "0";
          menuBackdrop.style.visibility = "hidden";
        })
      })
    }

  },

  mounted() {
    this.adaptScroll();
    this.smoothItemChange();
  }

}

</script>

<style></style>