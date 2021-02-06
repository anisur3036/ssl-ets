<template>
  <div class="flex flex-col flex-1 h-screen min-h-screen">
    <!-- Header -->
    <app-header></app-header>
    <!-- End-Header -->
    <div class="flex flex-1 overflow-y-hidden">
      <!-- Sidebar -->
      <app-sidebar></app-sidebar>
      <!-- end-sidebar -->
      <slot />
    </div>
  </div>
</template>
<script>
import AppSidebar from "./AppSidebar";
import AppHeader from "./AppHeader";
export default {
  components: {
    AppHeader,
    AppSidebar,
  },
};
</script>
