<template>
    <form @submit.prevent="">
        <label>Email</label>
        <input type="email" placeholder="Email">

        <label>Contraseña</label>
        <input type="text" placeholder="Contraseña">

        <input type="submit" value="Acceder">
    </form>
</template>

<script>
export default {
    name: 'Login',

    data() {
        return {
            
        }
    },

}
</script>

<style>

</style>