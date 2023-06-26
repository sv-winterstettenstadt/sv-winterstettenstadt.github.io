<template>
  <header class="relative z-50 mx-auto py-2">
    <div
      class="relative max-w-7xl mx-auto flex justify-between items-center md:px-12 px-4"
    >
      <div class="h-16 w-16 md:h-24 md:w-24 rounded-xl">
        <a aria-label="Home" class="pointer-events-auto" href="/">
          <img
            src="/images/logo2.png"
            class="object-contain h-16 w-16 md:h-24 md:w-24"
            style="color: transparent"
          />
        </a>
      </div>
      <nav class="pointer-events-auto hidden md:block">
        <ul
          class="flex rounded-full text-gray-300 px-3 text-sm font-medium shadow-lg ring-1 ring-gray-300 backdrop-blur"
        >
          <li>
            <a class="relative block px-3 py-2 transition hover:text-green-600">
              Über uns
            </a>
          </li>
          <li>
            <a class="relative block px-3 py-2 transition hover:text-green-600">
              News
            </a>
          </li>
          <li>
            <a class="relative block px-3 py-2 transition hover:text-green-600">
              Mannschaften
            </a>
          </li>
          <li>
            <a class="relative block px-3 py-2 transition hover:text-green-600">
              Breitensport
              <!--              <span
                class="absolute inset-x-1 bottom-1 h-[2px] bg-gradient-to-r from-green-500/20 via-green-500 to-green-500/20 dark:from-teal-400/0 dark:via-teal-400/40 dark:to-teal-400/0"
              ></span>-->
            </a>
          </li>
          <li>
            <a class="relative block px-3 py-2 transition hover:text-green-600">
              Mitglied werden
            </a>
          </li>
        </ul>
      </nav>
      <div class="flex justify-end gap-2">
        <div class="pointer-events-auto md:hidden">
          <button
            class="flex items-center rounded-full px-6 text-sm font-medium shadow-lg ring-1 ring-gray-300 text-gray-300 backdrop-blur py-2 transition hover:text-green-600"
            type="button"
            aria-expanded="false"
          >
            Menü
            <svg
              viewBox="0 0 8 6"
              aria-hidden="true"
              class="ml-3 h-auto w-2 stroke-gray-300 group-hover:stroke-green-600"
            >
              <path
                d="M1.75 1.75 4 4.25l2.25-2.5"
                fill="none"
                stroke-width="1.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              ></path>
            </svg>
          </button>
        </div>
        <div class="pointer-events-auto hidden md:block">
          <ul
            class="flex rounded-full px-3 text-sm font-medium shadow-lg ring-1 ring-gray-300 text-gray-300 backdrop-blur"
          >
            <li>
              <a
                class="relative block px-3 py-2 transition hover:text-green-600"
              >
                Kontakt
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup></script>

<style scoped>
li,
a {
  cursor: pointer;
}
</style>
