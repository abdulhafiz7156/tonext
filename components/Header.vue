<template>
  <header class="bg-custom text-white p-4">
    <div class="container mx-auto flex items-center justify-between">
      <div class="flex items-center space-x-4">
        <div class="text-xl font-bold">
          <img src="/images/logo.png" alt="Logo">
        </div>

        <!-- Language Editor Component -->
        <!-- Language Editor Component -->
        <div class="hidden md:flex relative">
          <button @click="toggleDropdown" class="language-editor flex items-center">
            <img src="/images/globe.png" alt="Globe" class="w-4 h-4 mr-2" />
            {{ formatLanguage(selectedLanguage) }}
          </button>
          <div
              v-if="isDropdownOpen"
              class="absolute right-0 text-white rounded-lg shadow-lg mt-12 min-w-max"
          >
            <div
                v-if="selectedLanguage !== 'eng'"
                class="language-option"
                @click="selectLanguage('eng')"
            >
              <img src="/images/globe.png" alt="Globe" class="w-4 h-4 mr-2" /> Eng
            </div>
            <div
                v-if="selectedLanguage !== 'ru'"
                class="language-option"
                @click="selectLanguage('ru')"
            >
              <img src="/images/globe.png" alt="Globe" class="w-4 h-4 mr-2" /> Ru
            </div>
          </div>
        </div>
      </div>

      <nav class="hidden md:flex justify-center flex-grow">
        <ul class="flex space-x-4">
          <li><a href="#" class="hover:underline">Главная</a></li>
          <li><a href="#" class="hover:underline">Faq</a></li>
          <li><a href="#" class="hover:underline">Как начать?</a></li>
          <li><a href="#" class="hover:underline">Smart-contract</a></li>
          <li><a href="#" class="hover:underline">Калькулятор</a></li>
        </ul>
      </nav>

      <div class="hidden md:flex header__buttons items-center space-x-4">
        <button class="bg-blue-500 p-2 rounded">1 TON - $4.89</button>
        <button class="bg-blue-500 p-2 rounded flex"><img src="/images/ton-logo.png" alt=""> Connect wallet</button>
      </div>
      <div class="flex md:hidden">
        <button @click="toggleMenu" class="p-2 header__menu-burger">
          <img src="/images/menu-burger.png" alt="">
        </button>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div
        :style="{ top: isMenuOpen ? '72px' : '-100%', height: '100vh' }"
        class="fixed left-0 right-0 z-50 bg-custom-menu-burger p-4 md:hidden transition-all duration-1000 ease-in-out"
    >
      <div class="flex items-center justify-between mb-4">
        <div class="flex items-center space-x-2">
          <span class="text-gray-400">Menu</span>
        </div>
        <img src="/images/logo.png" alt="Logo" class="h-6">
        <button @click="toggleMenu" class="p-2 header__close-button">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>

      <nav class="bg-custom rounded-lg p-6">
        <ul class="space-y-4 text-center text-lg ul-li-border-custom-border">
          <li class="border-b pb-5"><a href="#" class="hover:underline">Главная</a></li>
          <li class="border-b pb-5"><a href="#" class="hover:underline">Faq</a></li>
          <li class="border-b pb-5"><a href="#" class="hover:underline">Как начать?</a></li>
          <li class="border-b pb-5"><a href="#" class="hover:underline">Smart-contract</a></li>
          <li class="border-b pb-5"><a href="#" class="hover:underline">Калькулятор</a></li>
        </ul>

        <div class="flex flex-col mt-4 space-y-4 header__buttons">
          <!-- Button Connect Wallet -->
          <button class="bg-blue-500 p-2 rounded flex items-center justify-center button-bg-color">
            <img src="/images/ton-logo.png" alt="TON Logo" class="mr-2" /> Connect wallet
          </button>

          <!-- Button 1 TON -->
          <div class="flex justify-between items-center">
            <button class="bg-blue-500 p-2 rounded">1 TON - $4.89</button>

            <!-- Language Editor Inside Mobile Menu -->
            <div class="relative">
              <button @click="toggleDropdown" class="language-editor flex items-center">
                <img src="/images/globe.png" alt="Globe" class="w-4 h-4 mr-2" />
                {{ formatLanguage(selectedLanguage) }}
              </button>
              <div v-if="isDropdownOpen" class="absolute right-0 bg-custom text-white rounded-lg shadow-lg">
                <div
                    v-if="selectedLanguage !== 'eng'"
                    class="language-option"
                    @click="selectLanguage('eng')"
                >
                  <img src="/images/globe.png" alt="Globe" class="w-4 h-4 mr-2" /> Eng
                </div>
                <div
                    v-if="selectedLanguage !== 'ru'"
                    class="language-option"
                    @click="selectLanguage('ru')"
                >
                  <img src="/images/globe.png" alt="Globe" class="w-4 h-4 mr-2" /> Ru
                </div>
              </div>
            </div>
          </div>
        </div>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);
const isDropdownOpen = ref(false);
const selectedLanguage = ref('eng');

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value;
}

function toggleDropdown() {
  isDropdownOpen.value = !isDropdownOpen.value;
}

function selectLanguage(language) {
  selectedLanguage.value = language;
  isDropdownOpen.value = false; // Close dropdown after selection
  // Add logic to handle language change here
}

function formatLanguage(language) {
  return language === 'eng' ? 'Eng' : 'Ru';
}
</script>

<style scoped>
.bg-custom {
  background-color: #12172D;
}

.bg-custom-menu-burger {
  background: #12182E;
  border: 1px solid #25305B;
  border-radius: 21px 21px 0px 0px;
}

.header__buttons button {
  background-color: var(--button-bg-color);
  border-radius: var(--button-radius);
  height: 40px;
  padding: 10px 22px;
}

.header__buttons button img {
  margin-right: 5px;
}

.header__buttons button:first-child {
  background: #252F59;
}

.language-editor {
  display: flex;
  align-items: center;
  border-radius: var(--button-radius);
  background-color: #252F59;
  overflow: hidden;
  cursor: pointer;
  padding: 10px 20px;
  width: 90px;
  display: flex;
  justify-content: space-between;
}

.language-option {
  color: white;
  padding: 10px 20px;
  width: 90px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: var(--button-radius);
  background-color: #252F59;
}


.language-option:not(:last-child) {
  border-bottom: 1px solid #ffffff;
}

.language-option:hover,
.language-option.active {
  background-color: #1d2a4a;
}

.transition-all {
  transition: all 1s;
}

.ul-li-border-custom-border li {
  border-color: #25305B;
}

.ul-li-border-custom-border li:last-child {
  border-bottom: none;
  margin-bottom: 50px;
}

.header__menu-burger {
  background: #252F59;
  border: 1px solid #475489;
  width: 73px;
  height: 45px;
  border-radius: 999px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.header__close-button {
  background: #70758E0F;
  border-radius: 50%;
}
</style>
