<template>
  <div class="relative flex h-8 text-gray-800" style="-webkit-app-region: drag">
    <a
      class="flex items-center flex-none w-56 px-3 py-2 border-b border-purple-300 bg-gradient-to-b from-white to-gray-100"
      href="/"
    >
      <img class="w-6 h-6" src="@/assets/icon.png" alt="SSL Logo" />
      <div class="pl-2">Saiham Suits Ltd.</div>
    </a>
    <div
      class="flex items-center justify-between flex-1 px-4 border-b border-purple-300 bg-gradient-to-b from-white to-gray-100"
    >
      <div class="flex items-center">
        <div class="ml-2 text-sm text-gray-800">Select Menu Name</div>
        <div class="pl-3 ml-3 text-xs text-gray-800 border-l border-gray-600">
          Last Login User
        </div>
      </div>
      <div class="flex items-center">
        <a href="#" class="ml-4">
          <svg
            class="w-5 h-5 text-gray-600 hover:text-red-200"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            ></path>
          </svg>
        </a>
      </div>
    </div>
  </div>
</template>