<template>
    <div class="container">
        <label for="id_nombre">Nombre:</label>
        <!-- Directiva v-model: input se vincula a la propiedad reactiva -->
        <!-- MVC: el modelo es el texto, y el controlador es el JS -->
        <!-- sale del input (V), (el texto)(M), va al JS y este actualiza el input (C) -->
        <input v-model="nuevoNombre" id="id_nombre" type="text">
        <label for="id_apellido">Apellido:</label>
        <input v-model="nuevoApellido" id="id_apellido" type="text">
        <button v-on:click="agregarEstudiante()">Agregar Estudiante</button>
        <p>
            {{ nuevoNombre }}
            {{ nuevoApellido }}

        </p>
        <ul>
            <li v-for="{ nombre, apellido } in lista" :key="nombre">{{ nombre }} - {{ apellido }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            nuevoNombre: 'Emil',
            nuevoApellido: 'Verkade',
            lista: [
                { nombre: 'Emil', apellido: 'Verkade' },
                { nombre: 'Mat', apellido: 'Gomez' },
                { nombre: 'Ren', apellido: 'Parra' },
                { nombre: 'Kev', apellido: 'Andrade' },
                { nombre: 'Jos', apellido: 'Teran' },

            ],
        }
    },
    methods:{
        agregarEstudiante(){
            const nuevo={
                nombre: this.nuevoNombre,
                apellido: this.nuevoApellido
            }
            this.lista.unshift(nuevo);
        }
    }

}
</script>

<style></style>