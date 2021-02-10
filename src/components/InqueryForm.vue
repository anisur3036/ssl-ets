<template>
  <div
    class="flex flex-col w-full bg-gray-50 p-2 space-y-3 border-b border-gray-300"
  >
    <div class="flex items-center justify-between">
      <div class="flex items-center">
        <div class="flex items-center">
          <input
            type="checkbox"
            class="p-0 pl-1 text-gray-600 border focus:ring-1 focus:ring-gray-600 rounded"
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
            :class="toggleDate ? null : 'opacity-50'"
            type="date"
            name="form"
            v-model="toDate"
            id="form"
            :disabled="toggleDate ? false : true"
          />
        </div>
        <div>-</div>
        <div class="flex items-center">
          <input
            class="p-0 pl-1 border rounded"
            :class="toggleDate ? null : 'opacity-50'"
            type="date"
            v-model="fromDate"
            name="form"
            id="form"
            :disabled="toggleDate ? false : true"
          />
        </div>
      </div>
    </div>
    <div class="flex items-center justify-between">
      <div class="flex items-center">
        <div class="flex items-center">
          <input
            type="checkbox"
            class="p-0 pl-1 text-gray-600 border focus:ring-1 focus:ring-gray-600 rounded"
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
            :class="toggleDateTime ? null : 'opacity-50'"
            type="datetime-local"
            name="form"
            v-model="toDateTime"
            id="form"
            :disabled="toggleDateTime ? false : true"
          />
        </div>
        <div>-</div>
        <div class="flex items-center">
          <input
            class="flex-1 p-0 pl-1 border rounded"
            :class="toggleDateTime ? null : 'opacity-50'"
            type="datetime-local"
            name="form"
            id="form"
            v-model="fromDateTime"
            :disabled="toggleDateTime ? false : true"
          />
        </div>
      </div>
      <div class="flex items-center justify-between">
        <button
          class="px-3 py-1 ml-5 text-sm text-blac bg-purple-300 rounded-md shadow"
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
    <div class="flex items-center space-x-2">
      <div class="flex items-center">
        <label class="font-semibold" for="sslno">SSL No: </label>
        <select
          class="ml-2 py-0 pl-3 pr-9 border border-gray-600 focus:ring-1 focus:ring-gray-600 rounded"
          name="sslno"
          id="sslno"
        >
          <option value="">Any SSL</option>
          <option value="">124</option>
          <option value="">125</option>
          <option value="">126</option>
        </select>
      </div>
      <div class="flex items-center">
        <label class="font-semibold" for="floor">Floor: </label>
        <select
          class="ml-2 py-0 pl-3 pr-9 border border-gray-600 focus:ring-1 focus:ring-gray-600 rounded"
          name="sslno"
          id="sslno"
        >
          <option value="">Any floor...</option>
          <option value="">Floor-1</option>
          <option value="">Floor-2</option>
        </select>
      </div>
      <div class="flex items-center">
        <label class="font-semibold" for="line">Line: </label>
        <select
          class="ml-2 py-0 pl-3 pr-9 border border-gray-600 focus:ring-1 focus:ring-gray-600 rounded"
          name="sslno"
          id="line"
        >
          <option value="">Any Line...</option>
          <option value="">Line-1</option>
          <option value="">Line-2</option>
        </select>
      </div>
    </div>
    <div class="flex items-center space-x-2">
      <div class="flex items-center">
        <label class="font-semibold" for="tagno">Tag No: </label>
        <input
          type="text"
          class="ml-2 py-0 w-1/2 pl-3 pr-9 border border-gray-600 focus:ring-1 focus:ring-gray-600 rounded"
        />
      </div>
      <div class="flex items-center">
        <label class="font-semibold" for="emp">Emp No: </label>
        <input
          type="text"
          class="ml-2 w-1/2 py-0 pl-3 pr-9 border border-gray-600 focus:ring-1 focus:ring-gray-600 rounded"
        />
      </div>
    </div>
  </div>
</template>
<script>
//import axios from "axios";
export default {
  data() {
    return {
      toggleDate: false,
      toggleDateTime: false,
      toDate: null,
      fromDate: null,
      toDateTime: null,
      fromDateTime: null,
    };
  },
  methods: {
    //
  },
};
</script>