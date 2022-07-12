
<template>

<div>

<!--  <div v-html= "myHtml"> </div>
<div v-text= "title"> </div>

<div v-if="showname">
  <p> {{ user.nombre }}</p>
</div>
<div v-else>
    <p> No se puede mostrar el Dato</p>
</div>

<hr>

  <ul>
    <li v-for="tarea in tareas">
      {{ tarea.titulo}}
    </li>
  </ul>


<input type="text" v-model="user.app">

<button type="button" v-on:click="saludar(user.app)"> Presioname </button>
-->

<input type="text" v-on:keyup.enter="typendEnter"></input>



</div>

</template>


<script>
  export default{
    data(){
      return{
        title:'Soy el titulo JS',
        user:{ nombre: 'ivan', app: 'Guerra'},
        myHtml: '<h3> Objeto HTML desde el script</h3>',
        showname: true,
        tareas:[{titulo:'Practica1'},{titulo:'Practica2'},{titulo:'Practica3'}]

      }
    },
    methods:{
      saludar(name){alert('Hello: '+ name)},
      typing(e){console.log(e.target.value)},
      typendEnter(e){console.log('Dio Enter')},

    }

  }
</script>


<style>

</style>
