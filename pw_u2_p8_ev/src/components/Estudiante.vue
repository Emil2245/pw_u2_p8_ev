<template>
    <div class="container">
        <label for="id_nombre">Nombre:</label>
        <!-- Directiva v-model: input se vincula a la propiedad reactiva -->
        <!-- MVC: el modelo es el texto, y el controlador es el JS -->
        <!-- sale del input (V), (el texto)(M), va al JS y este actualiza el input (C) -->
        <input v-model="nuevoNombre" id="id_nombre" type="text">
        <label for="id_apellido">Apellido:</label>
        <input v-model="nuevoApellido" id="id_apellido" type="text">
        
        <label for="id_edad">Edad:</label>
        <input v-model="nuevaEdad" id="id_edad" type="number">
        
        <label for="id_genero">Genero:</label>
        <input v-model="nuevoGenero" id="id_genero" type="text">
        
        <label for="id_mascota">Mascota:</label>
        <input v-model="nuevaMascota" id="id_mascota" type="text">

        <button v-on:click="agregarEstudiante()">Agregar Estudiante</button>
        <p>
            {{ nuevoNombre }}
            {{ nuevoApellido }}
            {{ nuevoGenero }}
            {{ nuevaEdad }}
            {{ nuevaMascota }}

        </p>
        <ul>
            <li v-for="{ nombre, apellido, genero, edad, mascota } in lista" :key="nombre">{{ nombre }} - {{ apellido }} - {{ genero }} - {{ edad }} - {{ mascota }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            nuevoNombre: 'Emil',
            nuevoApellido: 'Verkade',
            nuevoGenero: 'Masculino',
            nuevaEdad: 23,
            nuevaMascota: 'clotilda la gallina',
            lista: [
                { nombre: 'Emil', apellido: 'Verkade', edad: 23, genero: 'Masculino', mascota: 'Cevichocho' },
                { nombre: 'Mat', apellido: 'Gomez', edad: 23, genero: 'Masculino', mascota: 'Cevichocho' },
                { nombre: 'Ren', apellido: 'Parra', edad: 23, genero: 'Masculino', mascota: 'Cevichocho' },
                { nombre: 'Kev', apellido: 'Andrade', edad: 23, genero: 'Masculino', mascota: 'Cevichocho' },
                { nombre: 'Jos', apellido: 'Teran', edad: 23, genero: 'Masculino', mascota: 'Cevichocho' },

            ],
        }
    },
    methods:{
        agregarEstudiante(){
            const nuevo={
                nombre: this.nuevoNombre,
                apellido: this.nuevoApellido,
                edad: this.nuevaEdad,
                genero: this.nuevoGenero,
                listaMascotas: this.nuevaListaMascotas,
            }
            this.lista.unshift(nuevo);
        }
    }

}
</script>

<style></style>