<template>
  <div class="flex flex-col justify-between flex-none w-56 bg-gray-200">
    <div class="overflow-y-auto text-sm leading-relaxed hashtag-bar">
      <List />
    </div>
  </div>
</template>

<script>
// import Icon from "@/shared/Icon";
import List from "@/layouts/List";
export default {
  components: {
    List,
  },
};
</script>
