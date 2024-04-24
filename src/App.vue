<template>

  <LitsBootstrapNavbar :options="opt" class="navbar-expand-lg navbar-dark bg-primary sticky-top"></LitsBootstrapNavbar>

  <RouterView />

  <LitsSimpleFooter :options="footerOptions"></LitsSimpleFooter>

</template>

<script lang="ts">
import { ref } from 'vue';
import { LitsBootstrapNavbar, LitsProfileNavbar, LitsSimpleFooter } from './components/elements';


export default {

  components: {
    LitsBootstrapNavbar,
    LitsProfileNavbar,
    LitsSimpleFooter
  },

  setup(){

    const opt = ref({
      container: "container",
      title: "Vue Elements",
      links : [
        {
          text: 'Home',
          to: '/'
        },
        {
          text: 'About us',
          to: '/about'
        },
      ],
    });

    const footerOptions = ref({
      title : "Vue Elements"
    });

    return {
      opt,
      footerOptions,
    };

  },

}
</script>