<template>
  <body>

    <Header />

    <Main />
  
    <Aside />

  </body>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'
import Aside from '@/components/Aside.vue'

export default defineComponent({
  name: 'Landing',

  components: {
    Header,
    Main,
    Aside
  }
  
});
</script>

<style scoped>

  body {
    width: 100vw;
    height: 100vh;
    display: grid;
    grid-template-areas: "h h"
                         "a m"
                         "a m";
    grid-template-columns: 20vw 1fr;
    grid-template-rows: 15vh 1fr;
  }

  header {
    grid-area: h;
  }

  main {
    grid-area: m;
  }

  aside {
    grid-area: a;
  }
  
</style>
