<template>
    <footer>
        <nav>
            <ul>
                <li>
                    <router-link to="/">
                        <i class="fas fa-bars"></i>
                    </router-link>
                </li>

                <li>
                    <i class="far fa-calendar"></i>
                </li>

                <li>
                    <i class="fas fa-users"></i>
                </li>

                <li>
                    <i class="far fa-clock"></i>
                </li>
            </ul>
        </nav>
    </footer>
</template>

<script>
export default {
    name: 'Footer'

}
</script>

<style scoped>

    footer {
        height: 10vh;
        width: 100vw;
        position: absolute;
        bottom: 0;
    }

    footer nav {
        height: inherit;
        width: inherit;
    }

    footer nav ul {
        height: inherit;
        width: inherit;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    footer nav ul li {
        font-size: 1.5rem;
        color: var(--color-icons);
    }

</style>