<template>
  <body>

    <header>
      Header
    </header>

    <main>
      Main
    </main>
  
    <aside>
      <router-link to="/">
        <i class="fab fa-elementor"></i>
      </router-link>
    </aside>

  </body>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Main'
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
    height: 15vh;
    background-color: var(--cuarternary-color);
  }

  main {
    background-color: var(--quintinary-color);
    grid-area: m;
    height: 85vh;
    width: 80vw;
  }

  aside {
    grid-area: a;
    background-color: var(--cuarternary-color);
    height: 85vh;
    width: 20vw;
  }

  aside i {
    padding: 6vh;
    font-size: 2rem;
    color: var(--color-icons);
  }
  
</style>
