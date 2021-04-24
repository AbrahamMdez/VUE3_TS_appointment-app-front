<template>
    <form class="form form-register">
        <fieldset class="form__fieldset input">
            <input class="form__input" type="text" placeholder="Nombre">
            <label class="form__label">Nombre</label>
        </fieldset>
        
        <fieldset class="form__fieldset input">
            <input class="form__input" type="text" placeholder="Apellidos">
            <label class="form__label">Apellidos</label>
        </fieldset>

        <fieldset class="form__fieldset input">
            <input class="form__input" type="email" placeholder="Email">
            <label class="form__label">Email</label>
        </fieldset>

        <fieldset class="form__fieldset input">
            <input class="form__input" type="text" placeholder="Contraseña">
            <label class="form__label">Contraseña</label>
        </fieldset>

        <fieldset class="form__fieldset input">
            <input class="form__input" type="text" placeholder="Repetir contraseña">
            <label class="form__label">Repite contraseña</label>
        </fieldset>

        <input class="btn btn-success btn-register" type="submit" value="Registrarse">

        <router-link class="link-login" to="/login">
            Volver a acceder
        </router-link>
    </form>
</template>

<script>
export default {
    name: 'Register'
}
</script>

<style scoped>

    .form-register {
        width: 100vw;
        height: 100vh;
        justify-content: center;
    }

    .btn-register {
        margin-top: 5vh;
    }

    .link-login {
        padding: 2vh;
    }

</style>