<template>
  <app-layout>
    <div class="flex flex-col">
      <InqueryForm />
      <div class="p-3 overflow-y-scroll"></div>
    </div>
  </app-layout>
</template>

<script>
import InqueryForm from "@/components/InqueryForm";
import AppLayout from "@/layouts/Spotify";
export default {
  components: {
    InqueryForm,
    AppLayout,
  },
};
</script>