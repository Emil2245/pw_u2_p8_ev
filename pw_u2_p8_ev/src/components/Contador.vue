<template>
    <div class="container">
        <h1>Contador</h1>
        <div class="doble_fila">
            <div>
                <p>{{ numero }}<sup>2</sup>={{ calcularCuadrado() }}</p>
                <p>{{ numero }}<sup>2</sup>={{ calcularCuadrado() }}</p>
                <p>{{ numero }}<sup>2</sup>={{ calcularCuadrado() }}</p>
                <p>{{ numero }}<sup>2</sup>={{ calcularCuadrado() }}</p>
                <p>{{ numero }}<sup>2</sup>={{ calcularCuadrado() }}</p>

            </div>
            <div>
                <p>{{ numero }}<sup>2</sup>={{ calCuadrado }}</p>
                <p>{{ numero }}<sup>2</sup>={{ calCuadrado }}</p>
                <p>{{ numero }}<sup>2</sup>={{ calCuadrado }}</p>
                <p>{{ numero }}<sup>2</sup>={{ calCuadrado }}</p>
                <p>{{ numero }}<sup>2</sup>={{ calCuadrado }}</p>

            </div>
        </div>
        <div>
            <button v-on:click="incrementar()">+1</button>
            <button v-on:click="decrementar()">-1</button>
        </div>
        <!-- <p>{{ numero }}<sup>2</sup>={{calc}}</p> -->

        <!-- representacion declarativa -->
        <p>
            1+1
        </p>
        <p>
            {{ 1 + 1 }}
        </p>
        <p>
            {{ false ? 'hola' : 'Joel, porque es falso' }}
        </p>

        <!-- Prog. reactiva, observa cambios en los componentes y permite realizar cambios de manera reactiva -->
        <!-- Option API data -->
        <p>
            {{ numero + 66 }}
        </p>
        <p>{{ joel }}</p>
        <p>{{ usr }}</p>
        <p>{{ arreglo }}</p>

    </div>
</template>

<script>
export default {
    // option Api data()
    data() {
        return {
            numero: 5,
            nombre: 'Emil Verkade',
            joel: false,
            usr: {
                nombre: 'Emil',
                edad: 23,
                genero: 'M'
            },
            arreglo: ['blanc', 'jaune', 'rouge'],
            calc: () => numero ** 2
        };
    },
    methods: {
        calcularCuadrado() {
            console.log('entra al metodo');
            return this.numero ** 2;
        },
        incrementar(){
            this.numero++;

        },
        decrementar(){
            this.numero--;
        }
    },
    // propiedades computadas: es una ESPECIE de metodo, no es un METODO, guarda propiedades en cache, como ejecucion de metodos
    // en lugar de calcularlo, deuvleve el valor
    //  siempre y cuando no cambie el cuerpo o el resultado de la propiedad computada
    computed: {
        calCuadrado() {
            console.log('prop computada');
            return this.numero ** 2;
        }
    },
    // directivas permiten gestionar eventos en la pagina web
    // comienzan con v-
}
</script>

<style>
.doble_fila {
    display: grid;
    justify-content: center;
    align-content: center;
    grid-template-columns: 100px 100px;
}
</style>
