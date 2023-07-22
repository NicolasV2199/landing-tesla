<template>
  <div class=" bg-gray-600/50 font-[Poppins] w-full h-screen top-0 left-0 right-0 backdrop-blur-sm" v-show="isOpen"
    @click="closeSidebar">
  </div>

  <aside
    :class="`${isOpen ? 'w-64' : 'w-0'} bg-slate-50 h-screen fixed top-0 right-0 overflow-y-scroll transition-all duration-500 ease-in-out`">
    <div v-show="isOpen">
      <button class="absolute right-5 top-5" @click="closeSidebar">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
          class="w-5 h-5">
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>

      <nav class="mt-6 p-8">
        <ul
          class="text-[14px] font-medium [&>li]:py-1.5 [&>li]:px-2 [&>li]:my-2 [&>li]:rounded-sm [&>li]:cursor-pointer [&>li]:transition-colors [&>li]:duration-500">
          <li class="hover:bg-slate-200 lg:hidden"><a href="#">Model X</a></li>
          <li class="hover:bg-slate-200 lg:hidden"><a href="#">Model 3</a></li>
          <li class="hover:bg-slate-200 lg:hidden"><a href="#">Model Y</a></li>
          <li class="hover:bg-slate-200 lg:hidden"><a href="#">Solar Roof</a></li>
          <li class="hover:bg-slate-200 lg:hidden"><a href="#">Solar Panels</a></li>
          <li class="hover:bg-slate-200 lg:hidden"><a href="#">Powerwall</a></li>
          <li class="hover:bg-slate-200"><a href="#">Existing Inventory</a></li>
          <li class="hover:bg-slate-200"><a href="#">Used Inventory</a></li>
          <li class="hover:bg-slate-200"><a href="#">Demo Drive</a></li>
          <li class="hover:bg-slate-200"><a href="#">Insurance</a></li>
          <li class="hover:bg-slate-200"><a href="#">Fleet</a></li>
          <li class="hover:bg-slate-200"><a href="#">Comercial Energy</a></li>
          <li class="hover:bg-slate-200"><a href="#">Utilities</a></li>
          <li class="hover:bg-slate-200"><a href="#">Charging</a></li>
          <li class="hover:bg-slate-200"><a href="#">Careers</a></li>
          <li class="hover:bg-slate-200"><a href="#">Find Us</a></li>
          <li class="hover:bg-slate-200"><a href="#">Events</a></li>
          <li class="hover:bg-slate-200"><a href="#">Suport</a></li>
          <li class="hover:bg-slate-200"><a href="#">Investor Relations</a></li>
          <li class="hover:bg-slate-200"><a href="#">Shop</a></li>
          <li class="hover:bg-slate-200"><a href="#">Acount</a></li>

          <li class="hover:bg-slate-200">
            <a href="#" class="flex justify-between">More
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                stroke="currentColor" class="w-3 h-3 self-center">
                <path stroke-linecap="round" stroke-linejoin="round" d="M8.25 4.5l7.5 7.5-7.5 7.5" />
              </svg>
            </a>
          </li>
          <li class="hover:bg-slate-200">
            <a href="#">
              <div class="flex align-middle">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                  stroke="currentColor" class="w-6 h-6">
                  <path stroke-linecap="round" stroke-linejoin="round"
                    d="M12 21a9.004 9.004 0 008.716-6.747M12 21a9.004 9.004 0 01-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 017.843 4.582M12 3a8.997 8.997 0 00-7.843 4.582m15.686 0A11.953 11.953 0 0112 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0121 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0112 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 013 12c0-1.605.42-3.113 1.157-4.418" />
                </svg>
                <span class="self-center ml-3">United States <br> <span class="font-light text-[12px] hover:underline">English</span></span>
              </div>
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </aside>
</template>

<script>
export default {

  data() {
    return {
      isOpen: false,
    }
  },


  methods: {
    openSidebar() {
      this.isOpen = true;
    },
    closeSidebar() {
      this.isOpen = false;
    },
  }


}
</script>
