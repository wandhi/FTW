<template>
  <div>
  
  <base-nav
    container-classes="container-fluid"
    class="navbar-top navbar-expand"
    :class="{'navbar-dark': type === 'default'}"
  >
  <b-row style="display:flex;flex-direction:row">
    <b-col>
    <img src="img/icons/sidebar/titleicon.png" style="margin-right:15px;width:12px;height:12px;object-fit:content"/>
    <a href="#" aria-current="page" style="color:#0036A0;font-size:12px;margin-top:24px" class="h4 mb-0  text-uppercase d-none d-lg-inline-block active router-link-active"> {{$route.name}} </a>
    </b-col>
  </b-row>
    <!-- Navbar links -->
   
  </base-nav>
  </div>
  
</template>
<script>
import { CollapseTransition } from 'vue2-transitions';
import { BaseNav, Modal } from '@/components';

export default {
  components: {
    CollapseTransition,
    BaseNav,
    Modal
  },
  props: {
    type: {
      type: String,
      default: 'default', // default|light
      description: 'Look of the dashboard navbar. Default (Green) or light (gray)'
    }
  },
  computed: {
    routeName() {
      const { name } = this.$route;
      return this.capitalizeFirstLetter(name);
    }
  },
  data() {
    return {
      activeNotifications: false,
      showMenu: false,
      searchModalVisible: false,
      searchQuery: ''
    };
  },
  methods: {
    capitalizeFirstLetter(string) {
      return string.charAt(0).toUpperCase() + string.slice(1);
    },
    toggleNotificationDropDown() {
      this.activeNotifications = !this.activeNotifications;
    },
    closeDropDown() {
      this.activeNotifications = false;
    }
  }
};
</script>
<style >
.navbar-vertical{
  box-shadow: none!important;
}
</style>
