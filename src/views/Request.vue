<template>
  <!--begin::Dashboard-->
  <div class="row gy-5 g-xl-8">
    <div class="col-xxl-4">
    </div>
  </div>

  <div class="row gy-5 gx-xl-8">
    <div class="col-xxl-4">
        <RequestEdit />
    </div>
    <div class="col-xxl-8">
    </div>
  </div>

  <div class="row gy-5 g-xl-8">
    <div class="col-xxl-4">
        <TableWidget13 />
    </div>
    <div class="col-xxl-4">
    </div>
    <div class="col-xxl-4">
    </div>
  </div>

  <div class="row g-5 gx-xxl-8">
    <div class="col-xxl-4">
    </div>
    <div class="col-xxl-8">

    </div>
  </div>
  <!--end::Dashboard-->
</template>

<script lang="ts">
import { defineComponent, onMounted } from "vue";
import RequestEdit from "@/components/modals/forms/RequestEdit.vue";
import { setCurrentPageTitle } from "@/core/helpers/breadcrumb";
import TableWidget13 from "@/components/widgets/tables/Widget13.vue";

export default defineComponent({
  name: "dashboard",
  components: {
    RequestEdit,
    TableWidget13
  },
  setup() {
    onMounted(() => {
      setCurrentPageTitle("Dashboard");
    });
  },
});
</script>
