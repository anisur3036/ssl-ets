<template>
  <div class="flex">
    <div class="flex absolute top-0 h-screen bg-gray-200">
      <!-- Sidebar -->
      <div class="flex">
        <!-- Backdrop -->
        <div
          :class="isOpen ? 'block' : 'hidden'"
          @click="isOpen = false"
          class="fixed z-20 inset-0 cursor-pointer bg-black opacity-50 transition-opacity lg:hidden"
        ></div>
        <!-- End Backdrop -->

        <div
          :class="
            isOpen ? 'translate-x-0 ease-out' : '-translate-x-full ease-in'
          "
          class="fixed z-30 inset-y-0 left-0 w-64 transition duration-300 transform bg-gray-800 overflow-y-auto lg:translate-x-0 lg:static lg:inset-0"
        >
          <div class="flex items-center justify-center mt-6">
            <div class="flex items-center">
              <img class="w-10 h-10" src="/img/SKCL-Logo.png" alt="SKCL" />

              <span class="text-white text-2xl mx-2 font-semibold"
                >Saiham Knit</span
              >
            </div>
          </div>

          <nav class="mt-10">
            <router-link
              class="flex items-center duration-200 mt-4 py-2 px-6 border-l-4"
              :class="[
                $route.name === 'Dashboard' ? activeClass : inactiveClass,
              ]"
              to="/dashboard"
            >
              <icon name="chart" />

              <span class="mx-4">Dashboard</span>
            </router-link>

            <router-link
              class="flex items-center duration-200 mt-4 py-2 px-6 border-l-4"
              :class="[
                $route.name === 'UIElements' ? activeClass : inactiveClass,
              ]"
              to="/ui-elements"
            >
              <svg
                class="h-5 w-5"
                viewBox="0 0 20 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M5 3C3.89543 3 3 3.89543 3 5V7C3 8.10457 3.89543 9 5 9H7C8.10457 9 9 8.10457 9 7V5C9 3.89543 8.10457 3 7 3H5Z"
                  fill="currentColor"
                />
                <path
                  d="M5 11C3.89543 11 3 11.8954 3 13V15C3 16.1046 3.89543 17 5 17H7C8.10457 17 9 16.1046 9 15V13C9 11.8954 8.10457 11 7 11H5Z"
                  fill="currentColor"
                />
                <path
                  d="M11 5C11 3.89543 11.8954 3 13 3H15C16.1046 3 17 3.89543 17 5V7C17 8.10457 16.1046 9 15 9H13C11.8954 9 11 8.10457 11 7V5Z"
                  fill="currentColor"
                />
                <path
                  d="M11 13C11 11.8954 11.8954 11 13 11H15C16.1046 11 17 11.8954 17 13V15C17 16.1046 16.1046 17 15 17H13C11.8954 17 11 16.1046 11 15V13Z"
                  fill="currentColor"
                />
              </svg>

              <span class="mx-4">UI Elements</span>
            </router-link>

            <router-link
              class="flex items-center duration-200 mt-4 py-2 px-6 border-l-4"
              :class="[$route.name === 'Tables' ? activeClass : inactiveClass]"
              to="/tables"
            >
              <svg
                class="h-5 w-5"
                viewBox="0 0 20 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7 3C6.44772 3 6 3.44772 6 4C6 4.55228 6.44772 5 7 5H13C13.5523 5 14 4.55228 14 4C14 3.44772 13.5523 3 13 3H7Z"
                  fill="currentColor"
                />
                <path
                  d="M4 7C4 6.44772 4.44772 6 5 6H15C15.5523 6 16 6.44772 16 7C16 7.55228 15.5523 8 15 8H5C4.44772 8 4 7.55228 4 7Z"
                  fill="currentColor"
                />
                <path
                  d="M2 11C2 9.89543 2.89543 9 4 9H16C17.1046 9 18 9.89543 18 11V15C18 16.1046 17.1046 17 16 17H4C2.89543 17 2 16.1046 2 15V11Z"
                  fill="currentColor"
                />
              </svg>

              <span class="mx-4">Tables</span>
            </router-link>

            <router-link
              class="flex items-center duration-200 mt-4 py-2 px-6 border-l-4"
              :class="[$route.name === 'Forms' ? activeClass : inactiveClass]"
              to="/forms"
            >
              <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
                <path
                  d="M17.414 2.586a2 2 0 00-2.828 0L7 10.172V13h2.828l7.586-7.586a2 2 0 000-2.828z"
                />
                <path
                  fill-rule="evenodd"
                  d="M2 6a2 2 0 012-2h4a1 1 0 010 2H4v10h10v-4a1 1 0 112 0v4a2 2 0 01-2 2H4a2 2 0 01-2-2V6z"
                  clip-rule="evenodd"
                />
              </svg>

              <span class="mx-4">Forms</span>
            </router-link>

            <router-link
              class="flex items-center duration-200 mt-4 py-2 px-6 border-l-4"
              :class="[$route.name === 'Cards' ? activeClass : inactiveClass]"
              to="/cards"
            >
              <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
                <path
                  d="M17.414 2.586a2 2 0 00-2.828 0L7 10.172V13h2.828l7.586-7.586a2 2 0 000-2.828z"
                />
                <path
                  fill-rule="evenodd"
                  d="M2 6a2 2 0 012-2h4a1 1 0 010 2H4v10h10v-4a1 1 0 112 0v4a2 2 0 01-2 2H4a2 2 0 01-2-2V6z"
                  clip-rule="evenodd"
                />
              </svg>

              <span class="mx-4">Cards</span>
            </router-link>

            <router-link
              class="flex items-center duration-200 mt-4 py-2 px-6 border-l-4"
              :class="[$route.name === 'Modal' ? activeClass : inactiveClass]"
              to="/modal"
            >
              <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
                <path
                  d="M3 4a1 1 0 011-1h12a1 1 0 011 1v2a1 1 0 01-1 1H4a1 1 0 01-1-1V4zM3 10a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H4a1 1 0 01-1-1v-6zM14 9a1 1 0 00-1 1v6a1 1 0 001 1h2a1 1 0 001-1v-6a1 1 0 00-1-1h-2z"
                />
              </svg>

              <span class="mx-4">Modal</span>
            </router-link>

            <router-link
              class="flex items-center duration-200 mt-4 py-2 px-6 border-l-4"
              :class="[$route.name === 'Blank' ? activeClass : inactiveClass]"
              to="/blank"
            >
              <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
                <path
                  d="M3 4a1 1 0 011-1h12a1 1 0 011 1v2a1 1 0 01-1 1H4a1 1 0 01-1-1V4zM3 10a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H4a1 1 0 01-1-1v-6zM14 9a1 1 0 00-1 1v6a1 1 0 001 1h2a1 1 0 001-1v-6a1 1 0 00-1-1h-2z"
                />
              </svg>

              <span class="mx-4">Blank</span>
            </router-link>
          </nav>
        </div>
      </div>
      <!-- End-Sidebar -->
    </div>
    <!-- Header -->
    <header
      class="flex justify-betweenitems-center py-2 px-6 bg-white border-b-2 border-indigo-400"
    >
      <div class="flex items-center" style="-webkit-app-region: no-drag">
        <button @click="isOpen = true" class="text-gray-500 focus:outline-none">
          <icon name="alt-menu" />
        </button>
      </div>

      <div class="flex items-center">
        <button class="flex mx-4 text-gray-600 focus:outline-none">
          <svg
            class="h-6 w-6"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M15 17H20L18.5951 15.5951C18.2141 15.2141 18 14.6973 18 14.1585V11C18 8.38757 16.3304 6.16509 14 5.34142V5C14 3.89543 13.1046 3 12 3C10.8954 3 10 3.89543 10 5V5.34142C7.66962 6.16509 6 8.38757 6 11V14.1585C6 14.6973 5.78595 15.2141 5.40493 15.5951L4 17H9M15 17V18C15 19.6569 13.6569 21 12 21C10.3431 21 9 19.6569 9 18V17M15 17H9"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </button>

        <div class="relative">
          <button
            @click="dropdownOpen = !dropdownOpen"
            class="relative z-10 block h-8 w-8 rounded-full overflow-hidden shadow focus:outline-none"
          >
            <img
              class="h-full w-full object-cover"
              src="https://images.unsplash.com/photo-1586083702768-190ae093d34d?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=296&q=80"
              alt="Your avatar"
            />
          </button>

          <div
            v-show="dropdownOpen"
            @click="dropdownOpen = false"
            class="fixed inset-0 h-full w-full z-10"
          ></div>

          <div
            v-show="dropdownOpen"
            class="absolute right-0 mt-2 py-2 w-48 bg-white rounded-md shadow-xl z-20"
          >
            <a
              href="#"
              class="block px-4 py-2 text-sm text-gray-700 hover:bg-indigo-600 hover:text-white"
              >Profile</a
            >
            <a
              href="#"
              class="block px-4 py-2 text-sm text-gray-700 hover:bg-indigo-600 hover:text-white"
              >Products</a
            >
            <router-link
              to="/"
              class="block px-4 py-2 text-sm text-gray-700 hover:bg-indigo-600 hover:text-white"
              >Log out</router-link
            >
          </div>
        </div>
      </div>
    </header>
    <!-- End-Header -->
    <!-- <main class="flex-1 lg:pl-64">
      <div class="overflow-x-hidden overflow-y-auto px-4 py-4">
        <slot />
      </div>
    </main> -->
  </div>
</template>

<script>
// import Header from '@/layouts/Header'
import Icon from "@/shared/Icon";
// import Sidebar from '@/layouts/Sidebar'
export default {
  data() {
    return {
      dropdownOpen: false,
      isOpen: false,
      activeClass: "bg-gray-600 bg-opacity-25 text-gray-100 border-gray-100",
      inactiveClass:
        "border-gray-900 text-gray-500 hover:bg-gray-600 hover:bg-opacity-25 hover:text-gray-100",
    };
  },
  components: {
    // Header,
    Icon,
  },
  methods: {
    sideBarClosed() {
      this.isOpen = false;
    },
    openSidebar() {
      this.isOpen = true;
    },
  },
};
</script>
