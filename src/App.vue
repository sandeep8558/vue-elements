<template>

  <LitsBootstrapNavbar :options="opt" class="navbar-expand-lg navbar-dark bg-primary sticky-top mb-5"></LitsBootstrapNavbar>

  <LitsProfileNavbar class="sticky-top p-2 navbar-expand navbar-light bg-white mb-10"></LitsProfileNavbar>

  <div style="height: 200vh;">Hello</div>

  <RouterView />

</template>

<script lang="ts">
import { ref } from 'vue';
import { LitsBootstrapNavbar, LitsProfileNavbar } from './components/elements';


export default {

  components: {
    LitsBootstrapNavbar,
    LitsProfileNavbar
  },

  setup(){

    const opt = ref({
      container: "container",
      title: "Sandy Rato",
      links : [
        {
          text: 'Home',
          to: '/'
        },
        {
          text: 'About us',
          to: '/about'
        },
        {
          text: 'Links',
          dropdown: [
            {
              text: 'Home',
              to: '/'
            },
            {
              text: 'About us',
              to: '/about'
            },
          ]
        },
      ],
    });

    return {
      opt,
    };

  },

}
</script>