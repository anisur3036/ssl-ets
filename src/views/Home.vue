<template>
  <app-layout>
    <HelloWorld></HelloWorld>
  </app-layout>
</template>

<script>
// @ is an alias to /src
import AppLayout from "@/layouts/Spotify";
import HelloWorld from "@/components/HelloWorld";
export default {
  components: {
    AppLayout,
    HelloWorld,
  },
};
</script>
