<template>
    <form class="form form-login">
        <fieldset class="form__fieldset input">
            <input class="form__input" type="email" placeholder="Email">
            <label class="form__label">Email</label>
        </fieldset>

        <fieldset class="form__fieldset input">
            <input class="form__input" type="text" placeholder="Contraseña">
            <label class="form__label">Contraseña</label>
        </fieldset>

        <input type="submit" value="Acceder" class="btn btn-success btn-login">

        <router-link class="link-register" to="/register">
            ¿Aun no estas registrado?
        </router-link>
    </form>
</template>

<script scoped>
export default {
    name: 'Login'
}
</script>

<style scoped>

    .form-login {
        width: 100vw;
        height: 100vh;
        justify-content: center;
    }

    .btn-login {
        margin-top: 5vh;
    }

    .link-register {
        padding: 2vh;
    }

</style>