<template>
  <div class="flex flex-col w-full p-2 space-y-3 border-b border-gray-300">
    <div class="flex items-center justify-between">
      <div class="flex items-center">
        <div class="flex items-center">
          <input
            type="checkbox"
            class="p-0 pl-1 text-gray-600 border border-white focus:ring-1 focus:ring-gray-600 rounded"
            id="checkdate"
            v-model="toggleDate"
          />
          <label class="ml-1 mr-2 font-sans font-medium" for="checkdate"
            >Form</label
          >
        </div>
        <div class="flex items-center">
          <input
            class="p-0 pl-1 border rounded"
            :class="toggleDate ? null : 'opacity-5'"
            type="date"
            name="form"
            id="form"
            :disabled="toggleDate ? false : true"
          />
        </div>
        <div>-</div>
        <div class="flex items-center">
          <input
            class="p-0 pl-1 border rounded"
            :class="toggleDate ? null : 'opacity-5'"
            type="date"
            name="form"
            id="form"
            :disabled="toggleDate ? false : true"
          />
        </div>
      </div>
      <div class="flex items-center justify-between">
        <button
          class="px-3 py-1 ml-5 text-sm text-black bg-purple-300 rounded-md shadow"
        >
          Display
        </button>
        <button
          class="px-3 py-1 ml-5 text-sm text-white bg-red-600 rounded-md shadow"
        >
          Delete
        </button>
        <button
          class="px-3 py-1 ml-5 text-sm text-black bg-purple-300 rounded-md shadow"
        >
          Export
        </button>
      </div>
    </div>
    <div class="flex items-center">
      <div class="flex items-center">
        <input
          type="checkbox"
          class="rounded-sm"
          id="checkdatetime"
          v-model="toggleDateTime"
        />
        <label class="ml-1 mr-2 font-sans font-medium" for="checkdatetime"
          >Tag Time</label
        >
      </div>
      <div class="flex items-center">
        <input
          class="flex-1 p-0 pl-1 border rounded"
          :class="toggleDateTime ? null : 'opacity-5'"
          type="datetime-local"
          name="form"
          id="form"
          :disabled="toggleDateTime ? false : true"
        />
      </div>
      <div>-</div>
      <div class="flex items-center">
        <input
          class="flex-1 p-0 pl-1 border rounded"
          :class="toggleDateTime ? null : 'opacity-5'"
          type="datetime-local"
          name="form"
          id="form"
          :disabled="toggleDateTime ? false : true"
        />
      </div>
    </div>
    <div class="flex items-center">
      <div class="flex items-center">
        <input
          type="checkbox"
          class="rounded-sm"
          id="checkdatetime"
          v-model="toggleDateTime"
        />
        <label class="ml-1 mr-2 font-sans font-medium" for="checkdatetime"
          >Tag Time</label
        >
      </div>
      <div class="flex items-center">
        <input
          class="flex-1 p-0 pl-1 border rounded"
          :class="toggleDateTime ? null : 'opacity-5'"
          type="datetime-local"
          name="form"
          id="form"
          :disabled="toggleDateTime ? false : true"
        />
      </div>
      <div>-</div>
      <div class="flex items-center">
        <input
          class="flex-1 p-0 pl-1 border rounded"
          :class="toggleDateTime ? null : 'opacity-5'"
          type="datetime-local"
          name="form"
          id="form"
          :disabled="toggleDateTime ? false : true"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      toggleDate: false,
      toggleDateTime: false,
    };
  },
};
</script>

<style scoped>
.form-checkbox {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  -webkit-print-color-adjust: exact;
  color-adjust: exact;
  display: inline-block;
  vertical-align: middle;
  background-origin: border-box;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  flex-shrink: 0;
  height: 1em;
  width: 1em;
  color: #42d9e1;
  background-color: #fff;
  border-color: #e2e8f0;
  border-width: 1px;
  border-radius: 0.25rem;
}

.form-checkbox:checked {
  background-image: url("data:image/svg+xml,%3csvg viewBox='0 0 16 16' fill='white' xmlns='http://www.w3.org/2000/svg'%3e%3cpath d='M5.707 7.293a1 1 0 0 0-1.414 1.414l2 2a1 1 0 0 0 1.414 0l4-4a1 1 0 0 0-1.414-1.414L7 8.586 5.707 7.293z'/%3e%3c/svg%3e");
  border-color: transparent;
  background-color: currentColor;
  background-size: 100% 100%;
  background-position: center;
  background-repeat: no-repeat;
}
</style>