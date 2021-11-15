<template>
  <!--begin::Dashboard-->
  <br>
  <div class="row gy-5 g-xl-8">
        <h2 style="padding-left:20px"> Website Plans </h2>
    </div>
  <br>
  <div class="row gy-5 gx-xl-8">
     <div class="col-md-6 col-xl-4">  
      <KTCard
        status="Overdue"
        :progress="10"
        status-data-badge-color="badge-light-danger"
        icon="media/svg/brand-logos/treva.svg"
        title="Aviasales App"
        date="May 10, 2021"
        budget="$36,400.00"
        :users="users8"
      ></KTCard>
    </div>
     <div class="col-md-6 col-xl-4">  
      <KTCard
        status="Overdue"
        :progress="10"
        status-data-badge-color="badge-light-danger"
        icon="media/svg/brand-logos/treva.svg"
        title="Aviasales App"
        date="May 10, 2021"
        budget="$36,400.00"
        :users="users8"
      ></KTCard>
    </div>
      <div class="col-md-6 col-xl-4">  
      <KTCard
        status="Overdue"
        :progress="10"
        status-data-badge-color="badge-light-danger"
        icon="media/svg/brand-logos/treva.svg"
        title="Aviasales App"
        date="May 10, 2021"
        budget="$36,400.00"
        :users="users8"
      ></KTCard>
    </div>
      <div class="col-md-6 col-xl-4">  
      <KTCard
        status="Overdue"
        :progress="10"
        status-data-badge-color="badge-light-danger"
        icon="media/svg/brand-logos/treva.svg"
        title="Aviasales App"
        date="May 10, 2021"
        budget="$36,400.00"
        :users="users8"
      ></KTCard>
    </div>
    <div class="col-xxl-8">
    </div>
  </div>
<br>
  <div class="row gy-5 gx-xl-8">
     <div class="row gy-5 g-xl-8">
        <h2 style="padding-left:20px"> Module Plans </h2>
    </div>
    <br>
     <div class="col-md-6 col-xl-4">  
      <KTCard
        status="Overdue"
        :progress="10"
        status-data-badge-color="badge-light-danger"
        icon="media/svg/brand-logos/treva.svg"
        title="Aviasales App"
        date="May 10, 2021"
        budget="$36,400.00"
        :users="users8"
      ></KTCard>
    </div>
    <div class="col-md-6 col-xl-4">  
      <KTCard
        status="Overdue"
        :progress="10"
        status-data-badge-color="badge-light-danger"
        icon="media/svg/brand-logos/treva.svg"
        title="Aviasales App"
        date="May 10, 2021"
        budget="$36,400.00"
        :users="users8"
      ></KTCard>
    </div>
    <div class="col-md-6 col-xl-4">  
      <KTCard
        status="Overdue"
        :progress="10"
        status-data-badge-color="badge-light-danger"
        icon="media/svg/brand-logos/treva.svg"
        title="Aviasales App"
        date="May 10, 2021"
        budget="$36,400.00"
        :users="users8"
      ></KTCard>
    </div>
    <div class="col-md-6 col-xl-4">  
      <KTCard
        status="Overdue"
        :progress="10"
        status-data-badge-color="badge-light-danger"
        icon="media/svg/brand-logos/treva.svg"
        title="Aviasales App"
        date="May 10, 2021"
        budget="$36,400.00"
        :users="users8"
      ></KTCard>
    </div>
    <div class="col-xxl-8">
     <div class="col-md-6 col-xl-4"> 
    </div>
    </div>
  </div>
<br>
  <div class="row gy-5 g-xl-8">
    <div class="col-xxl-4">
      <Invoices card-classes="mb-6 mb-xl-9"></Invoices>
    </div>
    <div class="col-xxl-4">
      <Invoices card-classes="mb-6 mb-xl-9"></Invoices>
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
import KTCard from "@/components/cards/Card1.vue";
import Invoices from "@/components/customers/cards/overview/Invoices.vue";

import { setCurrentPageTitle } from "@/core/helpers/breadcrumb";

export default defineComponent({
  name: "dashboard",
  components: {
    Invoices,
    KTCard
  },
  setup() {
    onMounted(() => {
      setCurrentPageTitle("Billing");
    });
  },
});
</script>
