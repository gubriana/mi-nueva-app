<template>
        <div id = "app">
            <h1 v-if = "encabezado_paises_si">Estos son los paises a los que {{ nombre }} quiere viajar</h1>
            <ul>
                <li v-for = "(paisessi, i) in lista_paises_si" v-bind:key="i" >{{paisessi}}</li>
            </ul>
            <h1 v-if= "encabezado_paises_no">Estos son los paises a los que {{ nombre }} no íria</h1>
            <ul>
                <li v-for = "(paisesno, i) in lista_paises_no" v-bind:key="i" >{{paisesno}}</li>
            </ul>
        </div>
</template>

<script>
export default {
  name: 'GLista',
  data:function() {
    return{
      nombre: "Gabriela",
      encabezado_paises_si: true,
      encabezado_paises_no: true,
      lista_paises_si: ['Japón', 'Islandia', 'Noruega', 'Suecia', 'Turquia', 'India'],
      lista_paises_no: ['Estados unidos', 'Perú', 'China', 'Francia']
    }
  }  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
