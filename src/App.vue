<template>
  <div id="app" class="row">
    <h2 class="titulo">{{titulo}}</h2> 
    <table-component v-for="(producto, key) in productos" :key="key" :columnas="columnas" :producto="producto" :estilo="estilos[key]" />
  </div>
</template>

<script>
import TableComponent from './components/tableComponent.vue'

export default {
  name: 'App',
  components: {
    TableComponent
  },
  data(){
    return{ 
      titulo:'Componentes vue cdn a vue cli - Carolina Perotti',
      estilos:[
        {
          "table-danger":true,
          "text-danger":true,
        },
        {
          "table-success":true,
          "text-success":true,
        },
        {
          "table-warning":true,
          "text-warning":true,
        }
      ],
      columnas:[
        {
          columna:'Tipo',
        },
        {
          columna:'Precio',
        },
      ],
      productos:[
        {
          tipo:'Carnes',
          variedades:[
            {
              nombre:'Vacio',
              precio: 1300,
            },
            {
              nombre:'Nalga',
              precio: 1400,
            },
            {
              nombre:'Costilla',
              precio: 1099,
            }
          ]  
        },
        {
          tipo:'Vegetales',
          variedades:[
            {
              nombre:'Cebollas',
              precio: 200,
            },
            {
              nombre:'Rucula',
              precio: 90,
            },
            {
              nombre:'Tomate',
              precio: 170,
            },
          ]
        },
        {
          tipo:'Bebidas',
          variedades:[
            {
              nombre:'Cerveza',
              precio:700
            },
            {
              nombre:'Vino',
              precio:800
            },
            {
              nombre:'Gin',
              precio:1800
            },
          ]
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
.titulo{
  margin-bottom: 30px;
}
</style>
