<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>

  <nav class="bg-white border-gray-200 dark:bg-gray-900">
    <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
      <a class="flex items-center">
        <img src="data:image/png;base64,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" class="h-8 mr-3" alt="bíó kvöld" />
        <span class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white">bíó kvöld</span>
      </a>
      <button data-collapse-toggle="navbar-default" type="button" class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="navbar-default" aria-expanded="false">
        <span class="sr-only">Open main menu</span>
        <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
          <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
        </svg>
      </button>
      <div class="hidden w-full md:block md:w-auto" id="navbar-default">
        <ul class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">

          <li>
            <RouterLink to="/home" class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Heima Síða</RouterLink>
          </li>

          <li>
            <RouterLink to="/about" class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Væntanlegt</RouterLink>
          </li>

          <li>
            <RouterLink to="/movies" class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Mismunandi Svæði</RouterLink>
          </li>

        </ul>
      </div>
    </div>
  </nav>

  <RouterView />
</template>

