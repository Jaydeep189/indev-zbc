<template>
  <!--begin::Dashboard-->
  <div class="row gy-5 gx-xl-8">
    <div class="col-xxl-4">
    </div>
    <div class="col-xxl-8">
      <UpgradePlan />
    </div>
  </div>

  <div class="row gy-5 g-xl-8">
    <div class="col-xxl-4">
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
import { setCurrentPageTitle } from "@/core/helpers/breadcrumb";
//import KTModalCard from "@/components/cards/Card.vue";
import UpgradePlan from "@/components/modals/general/UpgradePlanModal.vue"

export default defineComponent({
  name: "dashboard",
  components: {
    UpgradePlan,
  //  KTModalCard
  },
  setup() {
    onMounted(() => {
      setCurrentPageTitle("Pricing");
     });
  },
});
</script>