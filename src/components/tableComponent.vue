<template>
    <div class="col">
        <h4>{{producto.tipo}}</h4>
        <table :class='estilo' class="table table-bordered">
            <thead>
                <tr>
                    <th v-for='(columna, key) in columnas' :key='key'>{{columna.columna}}
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr v-for='(variedad, key) in producto.variedades' :key='key'>
                    <td>{{variedad.nombre}}</td>
                    <td>$ {{variedad.precio}}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
    export default {
        name:'tableComponent',
        props:{
            columnas: Array,
            producto: Object,
            estilo: Object,
        },
    }
</script>

<style scoped>

</style>