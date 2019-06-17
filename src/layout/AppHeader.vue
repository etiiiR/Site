<template>
    <header class="header-global">
        <base-nav class="navbar-main" transparent type="" effect="light" expand>
            <router-link slot="brand" class="navbar-brand mr-lg-5" to="/">
                <img src="img/brand/logo.png" style="width: 250px; height:auto" alt="logo">
            </router-link>

            <div class="row" slot="content-header" slot-scope="{closeMenu}">
                <div class="col-6 collapse-brand">
                    <a href="https://demos.creative-tim.com/vue-argon-design-system/documentation/">
                        <img src="img/brand/blue.png">
                    </a>
                </div>
                <div class="col-6 collapse-close">
                    <close-button @click="closeMenu"></close-button>
                </div>
            </div>

            <ul class="navbar-nav navbar-nav-hover align-items-lg-center">
                <base-dropdown class="nav-item" menu-classes="dropdown-menu-xl">
                    <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
                        <i class="ni ni-ui-04 d-lg-none"></i>
                        <span class="nav-link-inner--text">Components</span>
                    </a>
                    <div class="dropdown-menu-inner">
                        <a 
                         @click="router(event='route_1')"
                           class="media d-flex align-items-center">
                            <div class="icon icon-shape bg-gradient-primary rounded-circle text-white">
                                <i class="ni ni-spaceship"></i>
                            </div>
                            <div class="media-body ml-3">
                                <h6 class="heading text-primary mb-md-1">Portfolio</h6>
                                <p class="description d-none d-md-inline-block mb-0">Hier geht es zu dem Portfolio von Etienne Roulet.</p>
                            </div>
                        </a>
                        <a @click="router(event='route_2')" 
                           class="media d-flex align-items-center">
                            <div class="icon icon-shape bg-gradient-warning rounded-circle text-white">
                                <i class="ni ni-ui-04"></i>
                            </div>
                            <div class="media-body ml-3">
                                <h5 class="heading text-warning mb-md-1">Dashboard</h5>
                                <p class="description d-none d-md-inline-block mb-0">Das Dashboard ist nur für Administatoren erreichbar.</p>
                            </div>
                        </a>
                    </div>
                </base-dropdown>
                <base-dropdown tag="li" class="nav-item">
                    <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
                        <i class="ni ni-collection d-lg-none"></i>
                        <span class="nav-link-inner--text">Pages</span>
                    </a>
                    <router-link to="/landing" class="dropdown-item">Landing</router-link>
                    <router-link to="/profile" class="dropdown-item">Profile</router-link>
                    <router-link to="/login" class="dropdown-item">Login</router-link>
                    <router-link to="/register" class="dropdown-item">Register</router-link>
                </base-dropdown>
            </ul>
            <ul class="navbar-nav align-items-lg-center ml-lg-auto">
                <li class="nav-item">
                    <a class="nav-link nav-link-icon" href="https://www.facebook.com/creativetim" target="_blank" rel="noopener"
                       data-toggle="tooltip" title="Like us on Facebook">
                        <i class="fa fa-facebook-square"></i>
                        <span class="nav-link-inner--text d-lg-none">Facebook</span>
                    </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link nav-link-icon" href="https://www.instagram.com/creativetimofficial"
                       target="_blank" rel="noopener" data-toggle="tooltip" title="Follow us on Instagram">
                        <i class="fa fa-instagram"></i>
                        <span class="nav-link-inner--text d-lg-none">Instagram</span>
                    </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link nav-link-icon" href="https://twitter.com/creativetim" target="_blank" rel="noopener"
                       data-toggle="tooltip" title="Follow us on Twitter">
                        <i class="fa fa-twitter-square"></i>
                        <span class="nav-link-inner--text d-lg-none">Twitter</span>
                    </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link nav-link-icon" href="https://github.com/creativetimofficial/vue-argon-design-system"
                       target="_blank" rel="noopener" data-toggle="tooltip" title="Star us on Github">
                        <i class="fa fa-github"></i>
                        <span class="nav-link-inner--text d-lg-none">Github</span>
                    </a>
                </li>
            </ul>
        </base-nav>
    </header>
</template>
<script>
import BaseNav from "@/components/BaseNav";
import BaseDropdown from "@/components/BaseDropdown";
import CloseButton from "@/components/CloseButton";

export default {
  components: {
    BaseNav,
    CloseButton,
    BaseDropdown
  },
  methods: { 
      router: function (event) {
          if (event === 'route_1') {
              this.$router.push('profile')
          } else if (event === 'route_2') {
              this.$router.push('dashboard')
          }
      }
  }
};
</script>
<style>
</style>
