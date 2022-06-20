
<template>

<div>

<!--  <div v-html= "myHtml"> </div>-->
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



</div>

</template>


<script>
  export default{
    data(){
      return{
        title:'Soy el titulo JS',
        user:{ nombre: 'ivan', app: 'Guerra'},
        myHtml: '<h3> Objeto HTML desde el script</h3>',
        showname: false,
        tareas:[{titulo:'Practica1'},{titulo:'Practica2'},{titulo:'Practica3'}]

      }
    }
  }
</script>


<style>

</style>
