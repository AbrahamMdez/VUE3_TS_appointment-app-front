<template>
  <form @submit.prevent="saveClient">
      <label>Nombre</label>
      <input type="text" v-model="newClient.name" placeholder="Nombre">
      <label>Apellidos</label>
      <input type="text" v-model="newClient.surname" placeholder="Apellidos">
      <label>Teléfono</label>
      <input type="number" v-model="newClient.phoneNumber" placeholder="Teléfono"> 
      <label>Correo Electrónico</label>
      <input type="email" v-model="newClient.email" placeholder="Correo electrónico">
      <label>NIF</label>
      <input type="text" v-model="newClient.nif" placeholder="NIF">
      <!-- <label>Contraseña</label>
      <input type="text" v-model="newClient.pass1" placeholder="Contraseña">
      <label>Repetir Contraseña</label>
      <input type="text" v-model="newClient.pass2" placeholder="Repetir contraseña"> -->
      <input type="submit" value="Crear">
  </form>
</template>

<script>
export default {
    data() {
        return {
            newClient: {
                name: '',
                surname: '',
                phoneNumber: '',
                email: '',
                nif: '',
                // pass1: '',
                // pass2: ''
            }
        }
    },
    methods: {
        saveClient() {
            this.axios.post('clients/create-client', this.newClient)
                .then(res =>{
                 this.newClient = res.data
                 console.log(res.data)
                 })
                .catch(err => console.error(err))
        }
    },
}
</script>

<style>

</style>