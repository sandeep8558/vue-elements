<template>

    <header>
      <LitsBootstrapNavbar :options="opt"></LitsBootstrapNavbar>
    </header>


  <RouterView />
</template>

<script lang="ts">
import { ref } from 'vue';
import { LitsBootstrapNavbar } from './components/elements';


export default {

  components: {
    LitsBootstrapNavbar,
  },

  setup(){

    const opt = ref({
      container: "container",
      navMode: "navbar-dark",
      navBg : "bg-dark",
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