<template>
  <div class="relative flex h-10 text-white">
    <a
      class="flex items-center flex-none w-56 px-3 py-2 bg-gray-800 border-b border-gray-900"
      href="/"
    >
      <img class="w-6 h-6" src="@/assets/icon.png" alt="SSL Logo" />
      <div class="pl-2">Saiham Suits Ltd.</div>
    </a>
    <div
      class="flex items-center justify-between flex-1 px-4 bg-gray-800 border-b border-gray-900"
    >
      <div class="flex items-center">
        <div class="ml-2 text-sm text-white">Select Menu Name</div>
        <div class="pl-3 ml-3 text-xs text-gray-400 border-l border-gray-600">
          Last Login User
        </div>
      </div>
      <div class="flex items-center">
        <a href="#" class="ml-4">
          <form action="#" class="relative">
            <input
              placeholder="Search"
              class="px-2 py-1 text-xs text-gray-200 bg-gray-900 rounded"
            />
            <span class="absolute top-0 right-0 mr-1" style="top: 6px">
              <svg
                fill="currentColor"
                viewBox="0 0 24 24"
                width="24"
                height="24"
                class="w-4 h-4 text-gray-500 hover:text-gray-200"
              >
                <path
                  d="M16.32 14.9l5.39 5.4a1 1 0 0 1-1.42 1.4l-5.38-5.38a8 8 0 1 1 1.41-1.41zM10 16a6 6 0 1 0 0-12 6 6 0 0 0 0 12z"
                  class="heroicon-ui"
                ></path>
              </svg>
            </span>
          </form>
        </a>
        <a href="#" class="ml-4">
          <svg
            fill="currentColor"
            viewBox="0 0 24 24"
            width="24"
            height="24"
            class="w-6 h-6 text-gray-500 hover:text-gray-200"
          >
            <path
              d="M15.6 15.47A4.99 4.99 0 0 1 7 12a5 5 0 0 1 10 0v1.5a1.5 1.5 0 1 0 3 0V12a8 8 0 1 0-4.94 7.4 1 1 0 1 1 .77 1.84A10 10 0 1 1 22 12v1.5a3.5 3.5 0 0 1-6.4 1.97zM12 15a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"
              class="heroicon-ui"
            ></path>
          </svg>
        </a>
        <a href="#" class="ml-4">
          <svg
            fill="currentColor"
            viewBox="0 0 24 24"
            class="w-6 h-6 text-gray-500 hover:text-gray-200"
          >
            <g data-name="Layer 2">
              <g data-name="menu-arrow-circle">
                <rect
                  width="24"
                  height="24"
                  transform="rotate(180 12 12)"
                  opacity="0"
                ></rect>
                <path
                  d="M12 2a10 10 0 1 0 10 10A10 10 0 0 0 12 2zm0 16a1 1 0 1 1 1-1 1 1 0 0 1-1 1zm1-5.16V14a1 1 0 0 1-2 0v-2a1 1 0 0 1 1-1 1.5 1.5 0 1 0-1.5-1.5 1 1 0 0 1-2 0 3.5 3.5 0 1 1 4.5 3.34z"
                ></path>
              </g>
            </g>
          </svg>
        </a>
      </div>
    </div>
  </div>
</template>