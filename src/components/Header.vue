<script setup>
import { ref } from 'vue';

const showMobileMenu = ref(false)

const closeMenu = () => {
  setTimeout(() => {
    showMobileMenu.value = !showMobileMenu.value
  }, 700)
}

</script>

<template>
  <div class="header">
    <nav class="shadow-xl">
      <!-- Desktop -->
      <div>
        <div class="mx-auto sm:px-5 xl:px-[54px] 2xl:px-[54px] bg-black">
          <div class="flex justify-between h-20">
            <div class="flex">
              <!-- logo -->
              <div class="logo flex items-center justify-between gap-3">
                <RouterLink :to="{ name: 'Home' }" class="ml-3">
                  <a href="https://flowbite.com/" class="flex items-center">
                    <div>
                      <img src="/img/logo2.png" class="h-[60px] mr-2 w-[60px]" alt="Logo" />
                    </div>
                    <div class="flex flex-col font-serif">
                      <span id="text-desktop"
                        class="self-center text-xl font-semibold whitespace-nowrap dark:text-white">Lira & Haine</span>
                      <span id="text-desktop"
                        class="self-center text-sm font-semibold whitespace-nowrap dark:text-white">Advocacia</span>
                    </div>
                  </a>
                </RouterLink>
              </div>
            </div>
            <!-- login -->
            <div class="hidden md:flex items-center">
              <a href="#home">
                <button
                  id="button-menu"
                  class="relative inline-flex items-center justify-start overflow-hidden transition-all border border-[#DCBD85] hover:border-white  rounded-full hover:bg-[#242424] group">
                  <span
                    class="w-0 h-0 rounded bg-[#DCBD85] absolute top-0 left-0 ease-out duration-500 transition-all group-hover:w-full group-hover:h-full -z-1"></span>
                  <span
                    class="text-white transition-colors duration-300 ease-in-out group-hover:text-white z-10">Home</span>
                </button>
              </a>
              <a href="#acting">
                <button
                  class="relative ml-3 inline-flex items-center justify-start overflow-hidden transition-all border border-[#DCBD85] hover:border-white rounded-full hover:bg-[#242424] group">
                  <span
                    class="w-0 h-0 rounded bg-[#DCBD85] absolute top-0 left-0 ease-out duration-500 transition-all group-hover:w-full group-hover:h-full -z-1"></span>
                  <span
                    class="text-white transition-colors duration-300 ease-in-out group-hover:text-white z-10">Atuação</span>
                </button>
              </a>
              <a href="#our-team">
                <button
                  class="relative ml-3 inline-flex items-center justify-start overflow-hidden transition-all border border-[#DCBD85] hover:border-white rounded-full hover:bg-[#242424] group">
                  <span
                    class="w-0 h-0 rounded bg-[#DCBD85] absolute top-0 left-0 ease-out duration-500 transition-all group-hover:w-full group-hover:h-full -z-1"></span>
                  <span class="text-white transition-colors duration-300 ease-in-out group-hover:text-white z-10">Nosso
                    Time</span>
                </button>
              </a>
              <a href="#about">
                <button
                  class="relative ml-3 inline-flex items-center justify-start overflow-hidden transition-all border border-[#DCBD85] hover:border-white rounded-full hover:bg-[#242424] group">
                  <span
                    class="w-0 h-0 rounded bg-[#DCBD85] absolute top-0 left-0 ease-out duration-500 transition-all group-hover:w-full group-hover:h-full -z-1"></span>
                  <span class="text-white transition-colors duration-300 ease-in-out group-hover:text-white z-10">Sobre
                    Nós</span>
                </button>
              </a>
              <a href="#contact">
                <button
                  class="relative ml-3 inline-flex items-center justify-start overflow-hidden transition-all border border-[#DCBD85] hover:border-white rounded-full hover:bg-[#242424] group">
                  <span
                    class="w-0 h-0 rounded bg-[#DCBD85] absolute top-0 left-0 ease-out duration-500 transition-all group-hover:w-full group-hover:h-full -z-1"></span>
                  <span
                    class="text-white transition-colors duration-300 ease-in-out group-hover:text-white z-10">Contatos</span>
                </button>
              </a>
            </div>
            <!-- button show mobile menu -->
            <div class="md:hidden flex items-center">
              <div class="px-5">
                <button @click="showMobileMenu = !showMobileMenu">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                    stroke="currentColor" class="w-6 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round"
                      d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                  </svg>
                </button>
              </div>

            </div>
          </div>
        </div>
      </div>
      <!-- menu mobile -->
      <div>
        <div class="md:hidden flex flex-col items-center bg-black px-10 py-10" :class="{ hidden: !showMobileMenu }">
          <a href="#home">
            <button
              class="relative inline-flex items-center justify-start overflow-hidden transition-all bg-transparent border border-[#DCBD85] rounded-full hover:bg-white group"
              @click="closeMenu">
              <span
                class="w-0 h-0 rounded bg-[#DCBD85] absolute top-0 left-0 ease-out duration-500 transition-all group-hover:w-full group-hover:h-full -z-1"></span>
              <span class="text-white transition-colors duration-300 ease-in-out group-hover:text-white z-10">Home</span>
            </button>
          </a>
          <a href="#acting">
            <button
              @click="closeMenu"
              class="relative xl:ml-3 inline-flex items-center justify-start overflow-hidden transition-all bg-transparent border border-[#DCBD85] rounded-full hover:bg-white group" id="button-menu">
              <span
                class="w-0 h-0 rounded bg-[#DCBD85] absolute top-0 left-0 ease-out duration-500 transition-all group-hover:w-full group-hover:h-full -z-1"></span>
              <span class="text-white transition-colors duration-300 ease-in-out group-hover:text-white z-10">Atuação</span>
            </button>
          </a>
          <a href="#our-team">
            <button
              @click="closeMenu"
              class="relative xl:ml-3 inline-flex items-center justify-start overflow-hidden transition-all bg-transparent border border-[#DCBD85] rounded-full hover:bg-white group" id="button-menu">
              <span
                class="w-0 h-0 rounded bg-[#DCBD85] absolute top-0 left-0 ease-out duration-500 transition-all group-hover:w-full group-hover:h-full -z-1"></span>
              <span class="text-white transition-colors duration-300 ease-in-out group-hover:text-white z-10">Nosso
                Time</span>
            </button>
          </a>
          <a href="#about">
            <button
              @click="closeMenu"
              class="relative xl:ml-3 inline-flex items-center justify-start overflow-hidden transition-all bg-transparent border border-[#DCBD85] rounded-full hover:bg-white group" id="button-menu">
              <span
                class="w-0 h-0 rounded bg-[#DCBD85] absolute top-0 left-0 ease-out duration-500 transition-all group-hover:w-full group-hover:h-full -z-1"></span>
              <span class="text-white transition-colors duration-300 ease-in-out group-hover:text-white z-10">Sobre
                Nós</span>
            </button>
          </a>
          <a href="#contact">
            <button
              @click="closeMenu"
              class="relative xl:ml-3 inline-flex items-center justify-start overflow-hidden transition-all bg-transparent border border-[#DCBD85] rounded-full hover:bg-white group" id="button-menu">
              <span
                class="w-0 h-0 rounded bg-[#DCBD85] absolute top-0 left-0 ease-out duration-500 transition-all group-hover:w-full group-hover:h-full -z-1"></span>
              <span
                class="text-white transition-colors duration-300 ease-in-out group-hover:text-white z-10">Contatos</span>
            </button>
          </a>
      </div>
    </div>
  </nav>
</div></template>

<style scoped>
  @media only screen and (max-width: 600px) {
  #button-menu {
    @apply mt-10;
  }
  /* #text-desktop {
    display: none;
  } */
}
</style>
