<template>

<div class="usuarioStyle">

    <h1> Componente USUARIO</h1>

    <ul>
        <li v-for="user in users">
        {{user.name}} - {{user.email}} <button v-on:click="deleteUser(user)">X</button>
        </li>
    </ul>

    <form v-on:submit.prevent="addUser">
    <input type="text" v-model="newUser.name" placeholder="Nombre del usuario:">
    <input type="email" v-model="newUser.email" placeholder="Correo:">
    <button type="submit">Agregar usuario</button> 

    </form>

</div>

</template>


<script>

export default{
    name:'users',
    data(){
        return{
            users:[{name:'ivan',email:'ivan@gmail.com',contacted:true},{name:'naomi',email:'naomi@gmail.com',contacted:false}],
            newUser:{}
        }
    },
    methods:{
        addUser(){ this.users.push(this.newUser); this.newUser= {}; },
        deleteUser(user){ this.users.splice(this.users.indexOf(user),1); },
    }
}

</script>


<style>
.usuarioStyle{ background: rgb(109, 175, 3); }

</style>
