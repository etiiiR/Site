<template>
    <div class="profile-page">
        <section class="section-profile-cover section-shaped my-0" style="">
            <div class="shape shape-style-1 shape-primary shape-skew alpha-4" style="background-image: linear-gradient(to right, #4facfe 0%, #00f2fe 100%);">
                
            </div>
        </section>
        <section class="section section-skew">
            <div class="container">
                <card shadow class="card-profile mt--300" no-body>
                    <div class="px-4">
                        <div class="row justify-content-center">
                            <div class="col-lg-3 order-lg-2">
                                <div class="card-profile-image">
                                    <a href="#">
                                        <img v-lazy="'img/theme/team-4-800x800.jpg'" class="rounded-circle">
                                    </a>
                                </div>
                            </div>
                            <div class="col-lg-4 order-lg-3 text-lg-right align-self-lg-center">
                                <div class="card-profile-actions py-4 mt-lg-0">
                                    <base-button type="info" size="sm" class="mr-4">Connect</base-button>
                                    <base-button type="default" size="sm" class="float-right">Contact ME</base-button>
                                </div>
                            </div>
                            <div class="col-lg-4 order-lg-1">
                                <div class="card-profile-stats d-flex justify-content-center">
                                    <div class="col-lg-4 order-lg-1">
                                <div class="card-profile-stats d-flex justify-content-center">
                                    <base-button type="primary" size="sm" class="float-left">LEBENSLAUF</base-button>
                                    <base-button type="danger" size="sm" class="float-left">KENNTNISSE</base-button>
                                    <base-button type="warning" size="sm" class="float-left">PROJEKTE</base-button>
                                </div>
                            </div>
                                </div>
                            </div>
                        </div>
                        <div class="text-center mt-5">
                            <h3>Etienne Roulet
                                <span class="font-weight-light">, 21</span>
                            </h3>
                            <div class="h6 font-weight-300"><i class="ni location_pin mr-2"></i>Computer Scientiest / Developer</div>
                            <div class="h6 mt-4"><i class="ni business_briefcase-24 mr-2"></i>Webdeveloper</div>
                            <div><i class="ni education_hat mr-2"></i>University of Computer Science</div>
                        </div>
                        <div class="mt-5 py-5 border-top text-center">
                            <div class="row justify-content-center">
                                <div class="col-lg-9">
                                    <fade-transition origin="center" mode="out-in" :duration="250">
                                     <router-view></router-view>
                                    </fade-transition>
                                     <base-button type="danger">Download my CV</base-button>
                                </div>
                            </div>
                        </div>
                    </div>
                </card>
            </div>
        </section>
    </div>
</template>
<script>
import { FadeTransition } from "vue2-transitions";

export default {
 components: {
    FadeTransition
  },
  methods: { 
      download_cv: function () {
             
          }
      }
  };
</script>
<style>
</style>

