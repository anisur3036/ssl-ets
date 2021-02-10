<template>
  <app-layout>
    <div class="flex flex-col w-full bg-white">
      <InqueryForm />
      <div class="p-3 overflow-y-scroll">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis,
        reprehenderit voluptatem necessitatibus repellat excepturi culpa
        nesciunt eum laborum distinctio repellendus, harum sapiente quam
        dignissimos beatae pariatur. Animi in rem nostrum?
      </div>
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