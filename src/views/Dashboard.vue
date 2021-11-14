<template>
  <!--begin::Dashboard-->
  <div class="row gy-5 g-xl-8">
    <div class="col-xxl-4">
     <MixedWidget14 widget-classes="card-xxl-stretch mb-5 mb-xl-8"
        widget-color="#CBF0F4"/>
    </div>
  </div>

  <div class="row gy-5 gx-xl-8">
    <div class="col-xxl-4">
      <router-link to="/pricing"> Pricing </router-link>
      <router-link to="/request"> Request </router-link>
      <router-link to="/support"> Support </router-link>
      <router-link to="/billing"> Billing </router-link>
      <router-link to="/profile-main"> Profile </router-link>


    </div>
    <div class="col-xxl-8">

    </div>
  </div>

  <div class="row gy-5 g-xl-8">
    <div class="col-xxl-4">
    </div>
    <div class="col-xxl-4">
      <ListWidget6 widget-classes="card-xl-stretch mb-xl-8"></ListWidget6>
    </div>
    <div class="col-xxl-4">
      <ListWidget1 widget-classes="card-xxl-stretch mb-xl-3"></ListWidget1>
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
import ListWidget1 from "@/components/widgets/lists/Widget1.vue";
import ListWidget6 from "@/components/widgets/lists/Widget6.vue";
import MixedWidget14 from "@/components/widgets/mixed/Widget14.vue";
import { setCurrentPageTitle } from "@/core/helpers/breadcrumb";

export default defineComponent({
  name: "dashboard",
  components: {
    ListWidget1,
    ListWidget6,
    MixedWidget14
  },
  setup() {
    onMounted(() => {
      setCurrentPageTitle("Dashboard");
    });
  },
});
</script>
