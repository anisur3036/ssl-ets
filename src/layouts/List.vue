<template>
  <ul class="overflow-hidden bg-gray-200">
    <li
      class="relative text-gray-800 border-t border-gray-400 cursor-pointer"
      v-for="(item, index) in list"
      :key="'item' + index"
    >
      <!-- font awesome icon with a rotating animation -->
      <Icon
        name="chevron_right"
        class="w-5 h-5 text-gray-400 icon"
        :class="{ open: item.open }"
      />
      <!-- The list title with the click event for toggling the open status -->
      <div class="py-3 title" @click="item.open = !item.open">
        {{ item.title }}
      </div>
      <!-- renders the ListItem Component for each list element -->
      <ListItem :list="item" />
    </li>
  </ul>
</template>

<script>
import ListItem from "./ListItem";
import Icon from "@/shared/Icon";
export default {
  data: () => {
    return {
      list: [
        {
          title: "PPC Information",
          open: false,
          sublist: [
            "SSL Information",
            "Target Setting Cutting",
            "Target Setting Sewing",
            "Target Setting Finishing",
          ],
        },
        {
          title: "IE Information",
          open: false,
          sublist: [
            "Rework Code",
            "Work Settings",
            "Basic Operations",
            "SSL Bulletin",
          ],
        },
        {
          title: "Cutting Information",
          open: false,
          sublist: [
            "Lay Chart Information",
            "Making Bdl Qty",
            "Tag Assign (Cutting)",
            "Tag Change Query",
          ],
        },
        {
          title: "Daily Inquiries",
          open: false,
          sublist: ["Daily Production Report", "Cutting Production Report"],
        },
        {
          title: "Reports",
          open: false,
          sublist: ["Tag Change Query", "Personnel Info"],
        },
        {
          title: "SSL (Admin)",
          open: false,
          sublist: ["Admin Action 1", "Admin Action 2"],
        },
      ],
    };
  },
  components: {
    ListItem,
    Icon,
  },
};
</script>

<style lang="scss" scoped>
.icon {
  position: absolute;
  top: 14px;
  right: 10px;
  transition: transform 0.5s ease-in-out;
  &.open {
    transform: rotateZ(90deg);
  }
}
.title {
  padding: 10px 0;
  text-indent: 20px;
}
</style>