<template>
  <div class="flex flex-col justify-between flex-none w-56 bg-gray-800">
    <div class="overflow-y-auto text-sm leading-relaxed hashtag-bar">
      <List />
      <!-- <button class="flex items-center text-gray-500 hover:text-gray-200">
        <Icon name="plus" class="w-5 h-5" />
        <h3 class="text-xs font-semibold tracking-wide">PPC Information</h3>
      </button>
      <ul class="px-2 py-3 pt-2">
        <li
          class="px-2 text-gray-200 rounded hover:text-gray-200 hover:bg-gray-900 bg-gray-750"
        >
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">general</span></a
          >
        </li>
        <li class="px-2 text-gray-200 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span>
            <span class="ml-2">core-dev</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">course</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">plugins</span></a
          >
        </li>
        <li class="px-2 text-gray-200 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">docs</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span>
            <span class="ml-2">showcase</span></a
          >
        </li>
        <li class="px-2 text-gray-200 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">help</span></a
          >
        </li>
      </ul>
      <button class="flex items-center text-gray-500 hover:text-gray-200">
        <Icon name="plus" class="w-5 h-5" />
        <h3 class="text-xs font-semibold tracking-wide">IE Information</h3>
      </button>
      <ul class="px-2 py-3 pt-2">
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span>
            <span class="ml-2">feedback</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">jobs</span></a
          >
        </li>
      </ul>
      <button class="flex items-center text-gray-500 hover:text-gray-200">
        <Icon name="plus" class="w-5 h-5" />
        <h3 class="text-xs font-semibold tracking-wide">Cutting Information</h3>
      </button>
      <ul class="px-2 py-3 pt-2">
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">design</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span>
            <span class="ml-2">development</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">random</span></a
          >
        </li>
      </ul>
      <button class="flex items-center text-gray-500 hover:text-gray-200">
        <Icon name="plus" class="w-5 h-5" />
        <h3 class="text-xs font-semibold tracking-wide">Reports</h3>
      </button>
      <ul class="px-2 py-3 pt-2">
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">design</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span>
            <span class="ml-2">development</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">random</span></a
          >
        </li>
      </ul>
      <button class="flex items-center text-gray-500 hover:text-gray-200">
        <Icon name="plus" class="w-5 h-5" />
        <h3 class="text-xs font-semibold tracking-wide">Daily Inquiries</h3>
      </button>
      <ul class="px-2 py-3 pt-2">
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">design</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span>
            <span class="ml-2">development</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">random</span></a
          >
        </li>
      </ul>
      <button class="flex items-center text-gray-500 hover:text-gray-200">
        <Icon name="plus" class="w-5 h-5" />
        <h3 class="text-xs font-semibold tracking-wide">SSL (Admin)</h3>
      </button>
      <ul class="px-2 py-3 pt-2">
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">design</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span>
            <span class="ml-2">development</span></a
          >
        </li>
        <li class="px-2 text-gray-500 hover:text-gray-200 hover:bg-gray-900">
          <a href="#" class="flex items-center"
            ><span class="text-xl">#</span> <span class="ml-2">random</span></a
          >
        </li>
      </ul> -->
    </div>
  </div>
</template>

<script>
// import Icon from "@/shared/Icon";
import List from "@/layouts/List";
export default {
  components: {
    // Icon,
    List,
  },
};
</script>
