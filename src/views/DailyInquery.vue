<template>
  <app-layout>
    <div class="flex flex-col w-full bg-white">
      <InqueryForm />
      <div class="p-3 overflow-y-scroll">
        <div
          class="align-middle inline-block min-w-full overflow-hidden bg-white"
        >
          <table class="border divide-y divide-gray-200 relative w-full">
            <thead class="bg-gray-50">
              <tr>
                <th scope="col" class="tbl-head">Emp ID</th>
                <th scope="col" class="tbl-head">Date</th>
                <th scope="col" class="tbl-head">Floor</th>
                <th scope="col" class="tbl-head">Line</th>
                <th scope="col" class="tbl-head">Tag No</th>
                <th scope="col" class="tbl-head">Size</th>
                <th scope="col" class="tbl-head">Color</th>
                <th scope="col" class="tbl-head">Qty</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="punchData in tableDatas" :key="punchData.AutoID">
                <td
                  class="border px-6 py-1 whitespace-nowrap text-sm text-gray-500"
                >
                  {{ punchData.AutoID }}
                </td>
                <td
                  class="border px-6 py-1 whitespace-nowrap text-sm text-gray-500"
                >
                  {{ punchData.QCProductionDate }}
                </td>
                <td
                  class="border px-6 py-1 whitespace-nowrap text-sm text-gray-500"
                >
                  {{ punchData.Floor }}
                </td>
                <td
                  class="border px-6 py-1 whitespace-nowrap text-sm text-gray-500"
                >
                  {{ punchData.Line_No }}
                </td>
                <td
                  class="border px-6 py-1 whitespace-nowrap text-sm text-gray-500"
                >
                  {{ punchData.EmployeeID }}
                </td>
                <td
                  class="border px-6 py-1 whitespace-nowrap text-sm text-gray-500"
                >
                  {{ punchData.Size }}
                </td>
                <td
                  class="border px-6 py-1 whitespace-nowrap text-sm text-gray-500"
                >
                  {{ punchData.Color }}
                </td>
                <td
                  class="border px-6 py-1 whitespace-nowrap text-sm text-gray-500"
                >
                  {{ punchData.GoodQty }}
                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </app-layout>
</template>

<script>
import axios from "axios";
import InqueryForm from "@/components/InqueryForm";
import AppLayout from "@/layouts/Spotify";
export default {
  components: {
    InqueryForm,
    AppLayout,
  },
  data() {
    return {
      tableDatas: [],
    };
  },

  created() {
    axios.get("/data.json").then((res) => {
      this.tableDatas = res.data.data;
    });
  },
};
</script>