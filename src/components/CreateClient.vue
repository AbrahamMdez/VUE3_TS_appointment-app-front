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
      
    <input type="submit" value="Crear">
  </form>
</template>

<script>
export default {
    name: 'CreateClient',

    data() {
        return {
            newClient: {
                name: '',
                surname: '',
                phoneNumber: '',
                email: '',
                nif: ''
            }
        }
    },
    
    methods: {
        saveClient() {
            this.axios.post('clients/create-client', this.newClient)
                .then( res => {
                    this.newClient = res.data
                    console.log(res.data)
                })

                .catch( err => console.error(err));
        }
    }
}
</script>

<style scoped>

</style>