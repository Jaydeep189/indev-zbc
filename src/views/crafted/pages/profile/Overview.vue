<template>
      <div class="row my-3">
        <div class="col-12 col-xl-8">
            <div class="card mb-4">
                <div class="card-header pb-0 p-3">
                    <div class="row">
                        <div class="col d-flex align-items-center">
                            <h6 class="mb-0">Profile Information</h6>
                        </div>
                        <!--<div class="col-md-4 text-right">
                            <a href="javascript:;"><i class="fas fa-user-edit text-secondary text-sm" data-bs-toggle="tooltip" data-bs-placement="top" title="Edit Profile"></i></a>
                        </div>-->
                    </div>
                </div>
                <div class="card-body p-3">
                    <p class="text-sm">
                        Mera Brand Store
                    </p>
                    <hr class="horizontal gray-light my-4" />
                    <ul class="list-group">
                        <li class="list-group-item border-0 ps-0 pt-0 text-sm"><strong class="text-dark">Full
                                Name:</strong> &nbsp;Naam me kya Rakha hai</li>
                        <li class="list-group-item border-0 ps-0 text-sm"><strong class="text-dark">Mobile:</strong>
                            &nbsp; 9548512366</li>
                        <li class="list-group-item border-0 ps-0 text-sm"><strong class="text-dark">Email:</strong>
                            &nbsp; google@gmail.com</li>
                        <li class="list-group-item border-0 ps-0 text-sm"><strong class="text-dark">Address:</strong>
                            &nbsp; Bhagwan ke Pass</li>
                        <li class="list-group-item border-0 ps-0 text-sm"><strong class="text-dark">Pincode:</strong>
                            &nbsp; 10001</li>

                    </ul>
                </div>
            </div>
        </div>


        <div class="col-12 col-xl-4">
            <div class="card mb-4">
                <div class="card-header pb-0 p-3">
                    <h6 class="mb-0">Platform Settings</h6>
                </div>
                <div class="card-body p-3">
                    <h6 class="text-uppercase text-body text-xs font-weight-bolder">Account</h6>
                    <form enctype='multipart/form-data' method='post' name='form1'><input type="hidden" name="csrfmiddlewaretoken" value="ThmodwZWt4lq0LC5jer8cMfbe4ICJsFiR5oiPfjdFUFF7mtv27GvGNXH8ph4RrJQ">
                        <ul class="list-group">
                            <li class="list-group-item border-0 px-0">
                                <div class="form-check form-switch ps-0">

                                    <input class="form-check-input ms-auto" onclick="function1();" data-toggle="toggle"
                                        name="notil" value="True" type="checkbox" id="flexSwitchCheckDefault"
                                         checked  />
                                    <label class="form-check-label text-body ms-3 text-truncate w-80 mb-0"
                                        for="flexSwitchCheckDefault">Email me renewal reminders</label>
                                </div>
                            </li>
                            <li class="list-group-item border-0 px-0">
                                <div class="form-check form-switch ps-0">
                                    <input class="form-check-input ms-auto" onclick="function1();" name="newsl"
                                        value="True" type="checkbox" id="flexSwitchCheckDefault1"
                                         />
                                    <label class="form-check-label text-body ms-3 text-truncate w-80 mb-0"
                                        for="flexSwitchCheckDefault1">Email me Offers & More.</label>
                                </div>
                            </li>

                        </ul>
                    </form>
                </div>
                </div>
            </div>
        </div>
</template>

<script lang="ts">
import { defineComponent, onMounted } from "vue";
import { setCurrentPageBreadcrumbs } from "@/core/helpers/breadcrumb";

export default defineComponent({
  name: "overview",
  components: {

  },
  setup() {
    onMounted(() => {
      setCurrentPageBreadcrumbs("Overview", ["Pages", "Profile"]);
    });
  },
});
</script>
