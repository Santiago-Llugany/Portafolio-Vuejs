<script setup>
import icono1 from '/src/assets/chefman.svg';
import icono2 from '/src/assets/bike.svg';
import { ref } from 'vue';
const titulo = 'Desempledo :)';
const fecha = 'Desde Enero 2024';
const experiencias = ref([
    { id: 1, src: icono1, parrafo: 'Fui ayudante de cocina por un mes.' },
    { id: 2, src: icono2, parrafo: 'Tambien prove ser delivery ' },
]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experencia in experiencias" :key="experencia.id">
                <img class="imagen-svg" :src="experencia.src" width="45rem" :alt="experencia.parrafo">
                <p>{{ experencia.parrafo }}</p>
            </li>
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: var(--vt-c-indigo);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: coral;
}

.fecha {
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>
