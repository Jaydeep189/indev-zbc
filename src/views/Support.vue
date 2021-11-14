<template>
  <!--begin::Dashboard-->
   <div class="row g-5 g-xl-8">
    <!--begin::Col-->
    <div class="col-xl-12">
      <MixedWidget15
      ></MixedWidget15>
    </div>
    <!--end::Col-->
    </div>
    <br>

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
import MixedWidget15 from "@/components/widgets/mixed/Widget15.vue";
import TableWidget13 from "@/components/widgets/tables/Widget13.vue";


import { setCurrentPageTitle } from "@/core/helpers/breadcrumb";
//import KTModalCard from "@/components/cards/Card.vue";

export default defineComponent({
  name: "dashboard",
  components: {
    MixedWidget15,
    TableWidget13
  //  KTModalCard
  },
  setup() {
    onMounted(() => {
      setCurrentPageTitle("Support");
     });
  },
});
</script>