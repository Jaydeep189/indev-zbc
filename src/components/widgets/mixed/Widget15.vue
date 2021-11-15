<template>
    <!--begin::Mixed Widget 9-->
    <div :class="widgetClasses">
        <!--begin::Body-->
       <div class="row">
    <div class="col-lg-7 mb-lg-0 mb-4">
      <div class="card">
        <div class="card-body p-3">
          <div class="row">
            <div class="col-lg-6">
              <div class="d-flex flex-column h-100">
                <p class="text-sm mb-1 pt-2 text-bold">Developed by Zerobitcode</p>
                <h4 class="font-weight-bolder">Customer Dashboard</h4>
                <p class="mb-5">In Case of any query, you can visit our helpcenter</p>
                <a class="text-body text-sm font-weight-bold mb-0 icon-move-right mt-auto" target="_blank"
                  href="https://zerobitcode.com/help-center/">
                  Visit Helpcenter
                  <i class="fas fa-arrow-right text-sm ms-1" aria-hidden="true"></i>
                </a>
              </div>
            </div>
            <div class="col-lg-5 ms-auto text-center mt-5 mt-lg-0">
              <div class="border-radius-lg h-100">
                <div class="position-relative d-flex align-items-center justify-content-center h-100">
                  <img class="w-100 position-relative z-index-2 pt-4" src="media/svg/avatars/support.jpg">
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="col-lg-5">
      <div class="card h-100" >
        <div class="mask bg-gradient-dark overflow-hidden position-relative border-radius-xl bg-cover h-100"
          style="background-image: url('media/svg/avatars/learning.png '); border-radius: 10px; ">
          <span class="mask bg-gradient-dark"></span>
          <div class="card-body position-relative z-index-1 d-flex flex-column h-100 p-3">
            <h5 class="text-white font-weight-bolder mb-4 pt-2">Go On our Youtube Channel</h5>
            <p class="text-white">You can find tutorials about the website plans and the process of development.</p>
            <a class="text-white text-sm font-weight-bold mb-0 icon-move-right mt-auto" target="_blank"
              href="https://www.youtube.com/channel/UC9JDr7wIvwnMJLa5toI7Dvw">
              Open Now
              <i class="fas fa-arrow-right text-sm ms-1" aria-hidden="true"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="row mt-4">
    <div class="col-xl-4 col-sm-6 mb-xl-0 mb-4">
      <div class="card">
        <div class="card-body p-3">
          <div class="row">
            <div class="col-7">
              <div class="numbers">
                <p class="text-sm mb-0 text-capitalize font-weight-bold">Connect On WhatsApp</p>
                <h5 class="font-weight-bolder">8200466132</h5>
                <a class="text-grey text-sm font-weight-bold mb-0 icon-move-right mt-auto"
                  href="https://wa.me/+918200466132" target="_blank">
                  Connect Now
                </a>
                  <i class="fas fa-arrow-right text-sm ms-1" aria-hidden="true"></i>
              </div>
            </div>
            <div class="col-5 text-end my-auto">
              <div class="icon icon-shape text-center border-radius-md">
                <i class="fab fa-whatsapp fa-3x" style="color:green"></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="col-xl-4 col-sm-6 mb-xl-0 mb-4">
      <div class="card">
        <div class="card-body p-3">
          <div class="row">
            <div class="col-7">
              <div class="numbers">
                <p class="text-sm mb-0 text-capitalize font-weight-bold">Connect On Instagram</p>
                <h5 class="font-weight-bolder">@zerobitcode</h5>
                <a class="text-grey text-sm font-weight-bold mb-0 icon-move-right mt-auto" target="_blank"
                  href="https://www.instagram.com/zerobitcode/">
                  Connect Now
                  <i class="fas fa-arrow-right text-sm ms-1" aria-hidden="true"></i>
                </a>
              </div>
            </div>
            <div class="col-5 text-end my-auto">
              <div class="icon icon-shape text-center border-radius-md">
                <i class="fab fa-instagram fa-3x" style="color:#8a3ab9;"></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="col-xl-4 col-sm-6 mb-xl-0 mb-4">
      <div class="card">
        <div class="card-body p-3">
          <div class="row">
            <div class="col-7">
              <div class="numbers">
                <p class="text-sm mb-0 text-capitalize font-weight-bold">Email Us</p>
                <h5 class="font-weight-bolder">support@zerobitcode.com</h5>
                <a class="text-grey text-sm font-weight-bold mb-0 icon-move-right mt-auto"
                  href="mailto:support@zerobitcode.com">
                  Mail us
                  <i class="fas fa-arrow-right text-sm ms-1" aria-hidden="true"></i>
                </a>
              </div>
            </div>
            <div class="col-5 text-end my-auto">
              <div class="icon icon-shape text-center border-radius-md">
                <i class="fa fa-envelope fa-3x" style="color:#f1d592;"></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div>
            <!--end::Body-->
        </div>
        <!--end::Mixed Widget 9-->
</template>

<script lang="ts">
    import {
        defineComponent
    } from "vue";

    export default defineComponent({
        name: "widget-1",
        components: {},
        props: {
            widgetClasses: String,
            time: String,
            image: String,
            title: String,
            description: String,
        },
    });
</script>