<template>
  <!--begin::Toolbar-->
  <div class="card mb-5 mb-xl-8">
            <div class="card-body pt-15">
          <!--begin::Summary-->
          <div class="d-flex flex-center flex-column mb-5">
            <!--begin::Avatar-->
            <!--end::Avatar-->

            <!--begin::Name-->
            <a
              href="#"
              class="fs-3 text-gray-800 text-hover-primary fw-bolder mb-1"
            >
              MBS
            </a>
            <!--end::Name-->

            <!--begin::Position-->
            <div class="fs-5 fw-bold text-muted mb-6">ORDER ID: 123ASDF</div>
            <!--end::Position-->

            <!--begin::Info-->
            <div class="d-flex flex-wrap flex-center">
              <!--begin::Stats-->
              <div
                class="
                  border border-gray-300 border-dashed
                  rounded
                  py-3
                  px-3
                  mb-3
                "
              >
                <div class="fs-4 fw-bolder text-gray-700">
                  <span class="w-75px">70</span>
                  <span class="svg-icon svg-icon-3 svg-icon-success">
                  </span>
                </div>
                <div class="fw-bold text-muted">Price : </div>
              </div>
              <!--end::Stats-->
              <br>
              <!--begin::Stats-->
              <div
                class="
                  border border-gray-300 border-dashed
                  rounded
                  py-3
                  px-3
                  mx-4
                  mb-3
                "
              >
                <div class="fs-4 fw-bolder text-gray-700">
                  <span class="w-50px">130</span>
                  <span class="svg-icon svg-icon-3 svg-icon-danger">
                  </span>
                </div>
                <div class="fw-bold text-muted">Purchase Date: </div>
              </div>
              <!--end::Stats-->

              <!--begin::Stats--> <br>
              <div
                class="
                  border border-gray-300 border-dashed
                  rounded
                  py-3
                  px-3
                  mb-3
                "
              >
                <div class="fs-4 fw-bolder text-gray-700">
                  <span class="w-50px">500</span>
                  <span class="svg-icon svg-icon-3 svg-icon-success">
                  </span>
                </div>
                <div class="fw-bold text-muted">Renewal Date :</div>
              </div>
              <!--end::Stats-->
            </div>
            <!--end::Info-->
          </div>
          <!--end::Summary-->

          <!--begin::Details toggle-->
          <!--end::Details toggle-->
          <!--begin::Details content-->
          <!--end::Details content-->
        </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, onMounted } from "vue";
import { setCurrentPageBreadcrumbs } from "@/core/helpers/breadcrumb";

export default defineComponent({
  name: "projects",
  components: {
  },
  setup() {
    onMounted(() => {
      setCurrentPageBreadcrumbs("Projects", ["Pages", "Profile"]);
    });

    const users1 = [
      { name: "Emma Smith", src: "media/avatars/150-1.jpg" },
      { name: "Rudy Stone", src: "media/avatars/150-2.jpg" },
      { name: "Susan Redwood", initials: "S", state: "primary" },
    ];

    const users2 = [
      { name: "Alan Warden", initials: "A", state: "warning" },
      { name: "Brian Cox", src: "media/avatars/150-4.jpg" },
    ];

    const users3 = [
      { name: "Mad Masy", src: "media/avatars/150-1.jpg" },
      { name: "Cris Willson", src: "media/avatars/150-2.jpg" },
      { name: "Mike Garcie", initials: "M", state: "info" },
    ];

    const users4 = [
      { name: "Nich Warden", initials: "N", state: "warning" },
      { name: "Rob Otto", initials: "R", state: "success" },
    ];

    const users5 = [
      { name: "Francis Mitcham", src: "media/avatars/150-5.jpg" },
      { name: "Michelle Swanston", src: "media/avatars/150-13.jpg" },
      { name: "Susan Redwood", initials: "S", state: "primary" },
    ];

    const users6 = [
      { name: "Emma Smith", src: "media/avatars/150-1.jpg" },
      { name: "Rudy Stone", src: "media/avatars/150-2.jpg" },
      { name: "Susan Redwood", initials: "S", state: "primary" },
    ];

    const users7 = [
      { name: "Meloday Macy", src: "media/avatars/150-3.jpg" },
      { name: "Rabbin Watterman", initials: "S", state: "success" },
    ];

    const users8 = [
      { name: "Emma Smith", src: "media/avatars/150-1.jpg" },
      { name: "Rudy Stone", src: "media/avatars/150-2.jpg" },
      { name: "Susan Redwood", initials: "S", state: "primary" },
    ];

    const users9 = [
      { name: "Meloday Macy", src: "media/avatars/150-3.jpg" },
      { name: "Rabbin Watterman", initials: "S", state: "danger" },
    ];

    return {
      users1,
      users2,
      users3,
      users4,
      users5,
      users6,
      users7,
      users8,
      users9,
    };
  },
});
</script>
