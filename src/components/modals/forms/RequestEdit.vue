<template>
    <!--begin::Modal - New Target-->
    <div id="kt_modal_new_target" ref="newTargetModalRef" tabindex="-1" aria-hidden="true">
        <!--begin::Modal dialog-->
        <div class="modal-dialog modal-dialog-centered mw-650px">
            <!--begin::Modal content-->
            <div class="modal-content rounded">
                <!--begin::Modal header-->
                <div class="modal-header pb-0 border-0 justify-content-end">
                    <!--begin::Close-->
                    <div class="btn btn-sm btn-icon btn-active-color-primary" data-bs-dismiss="modal">
                        <span class="svg-icon svg-icon-1">
                            <inline-svg src="media/icons/duotune/arrows/arr061.svg" />
                        </span>
                    </div>
                    <!--end::Close-->
                </div>
                <!--begin::Modal header-->

                <!--begin::Modal body-->
                <div class="modal-body scroll-y px-10 px-lg-15 pt-0 pb-15">
                    <!--begin:Form-->
                    <el-form id="kt_modal_new_target_form" @submit.prevent="submit()" :model="targetData" :rules="rules"
                        ref="formRef" class="form">
                        <!--begin::Heading-->
                        <div class="mb-13 text-center">
                            <!--begin::Title-->
                            <h1 class="mb-3">Request Edit</h1>
                            <!--end::Title-->

                            <!--begin::Description-->
                            <div class="text-gray-400 fw-bold fs-5">
                                If you need more info, please check
                                <a href="#" class="fw-bolder link-primary">Modules</a>.
                            </div>
                            <!--end::Description-->
                        </div>
                        <!--end::Heading-->

                        <!--begin::Input group-->
                        <div class="d-flex flex-column mb-8 fv-row">
                            <!--begin::Label-->
                            <div class="row">
                                <div class="col-5 mt-3">
                                    <div class="form-check ">
                                        <input class="form-check-input" type="radio" value="True" name="ty"
                                            id="edittype1">
                                        <label class="custom-control-label" for="edittype1">Major Edit</label>
                                    </div> <br>
                                    <div class="form-check">
                                        <input class="form-check-input" type="radio" name="ty" value="False"
                                            id="edittype2">
                                        <label class="custom-control-label" for="edittype2">Minor Edit</label>
                                    </div> <br>
                                </div>
                                <div class="col-7 mt-3">
                                    <div class="col-md-6 fv-row">
                                        <label class="required fs-6 fw-bold mb-2">Website</label>

                                        <el-form-item prop="assign">
                                            <el-select v-model="targetData.assign" placeholder="Select a Website"
                                                name="assign" as="select">
                                                <el-option value="">Select Website</el-option>
                                                <el-option label="Karina Clark" value="1">Google</el-option>
                                                <el-option label="Robert Doe" value="2">Facebook</el-option>
                                                <el-option label="Niel Owen" value="3">lawda lassan</el-option>
                                                <el-option label="Olivia Wild" value="4">Olivia Wild</el-option>
                                                <el-option label="Sean Bean" value="5">Sean Bean</el-option>
                                            </el-select>
                                        </el-form-item>
                                    </div>
                                </div>
                                <!--end::Label-->
                            </div>
                            <!--end::Input group-->

                            <!--begin::Input group-->
                            <!--end::Input group-->

                            <!--begin::Input group-->
                            <div class="d-flex flex-column mb-8">
                                <label class="fs-6 fw-bold mb-2">
                                    <span class="required">Description</span>
                                    <i class="fas fa-exclamation-circle ms-2 fs-7" data-bs-toggle="tooltip"
                                        title="Specify a target priorty"></i>
                                </label>

                                <el-form-item prop="targetDetails">
                                    <el-input v-model="targetData.targetDetails" type="textarea" rows="3"
                                        name="targetDetails" placeholder="Type Target Details" />
                                </el-form-item>
                            </div>
                            <!--end::Input group-->

                            <!--begin::Input group-->
                            <!--end::Input group-->

                            <!--begin::Input group-->

                            <!--end::Input group-->

                            <!--begin::Input group-->
                            <!--end::Input group-->

                            <!--begin::Actions-->
                            <div class="text-center">
                                <!--begin::Button-->
                                <button :data-kt-indicator="loading ? 'on' : null" class="btn btn-lg btn-primary"
                                    type="submit">
                                    <span v-if="!loading" class="indicator-label">
                                        Submit
                                        <span class="svg-icon svg-icon-3 ms-2 me-0">
                                            <inline-svg src="icons/duotune/arrows/arr064.svg" />
                                        </span>
                                    </span>
                                    <span v-if="loading" class="indicator-progress">
                                        Please wait...
                                        <span class="spinner-border spinner-border-sm align-middle ms-2"></span>
                                    </span>
                                </button>
                                <!--end::Button-->
                            </div>
                            <!--end::Actions-->
                        </div>
                    </el-form>
                    <!--end:Form-->
                </div>
                <!--end::Modal body-->
            </div>
            <!--end::Modal content-->
        </div>
        <!--end::Modal dialog-->
    </div>
    <!--end::Modal - New Target-->
</template>

<style lang="scss">
    .el-select {
        width: 100%;
    }

    .el-date-editor.el-input,
    .el-date-editor.el-input__inner {
        width: 100%;
    }
</style>

<script lang="ts">
    import {
        defineComponent,
        ref
    } from "vue";
    import {
        hideModal
    } from "@/core/helpers/dom";
    import Swal from "sweetalert2/dist/sweetalert2.js";

    interface NewAddressData {
        targetTitle: string;
        assign: string;
        dueDate: string;
        targetDetails: string;
        tags: Array < string > ;
    }

    export default defineComponent({
        name: "new-target-modal",
        components: {},
        setup() {
            const formRef = ref < null | HTMLFormElement > (null);
            const newTargetModalRef = ref < null | HTMLElement > (null);
            const loading = ref < boolean > (false);

            const targetData = ref < NewAddressData > ({
                targetTitle: "",
                assign: "",
                dueDate: "",
                targetDetails: "",
                tags: ["important", "urgent"],
            });

            const rules = ref({
                targetTitle: [{
                    required: true,
                    message: "Please input Activity name",
                    trigger: "blur",
                }, ],
                assign: [{
                    required: true,
                    message: "Please select Activity zone",
                    trigger: "change",
                }, ],
                dueDate: [{
                    required: true,
                    message: "Please select Activity zone",
                    trigger: "change",
                }, ],
                tags: [{
                    required: true,
                    message: "Please select Activity zone",
                    trigger: "change",
                }, ],
            });

            const submit = () => {
                if (!formRef.value) {
                    return;
                }

                formRef.value.validate((valid) => {
                    if (valid) {
                        loading.value = true;

                        setTimeout(() => {
                            loading.value = false;

                            Swal.fire({
                                text: "Form has been successfully submitted!",
                                icon: "success",
                                buttonsStyling: false,
                                confirmButtonText: "Ok, got it!",
                                customClass: {
                                    confirmButton: "btn btn-primary",
                                },
                            }).then(() => {
                                hideModal(newTargetModalRef.value);
                            });
                        }, 2000);
                    } else {
                        Swal.fire({
                            text: "Sorry, looks like there are some errors detected, please try again.",
                            icon: "error",
                            buttonsStyling: false,
                            confirmButtonText: "Ok, got it!",
                            customClass: {
                                confirmButton: "btn btn-primary",
                            },
                        });
                        return false;
                    }
                });
            };

            return {
                targetData,
                submit,
                loading,
                formRef,
                rules,
                newTargetModalRef,
            };
        },
    });
</script>