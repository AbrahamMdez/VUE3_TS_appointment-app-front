<template>
    <aside>
        <router-link to="/">
            <i class="fab fa-elementor"></i>
        </router-link>
    </aside>
</template>

<script>
export default {
    name: 'Aside'
}
</script>

<style scoped>

    aside {
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