<script setup>
import icono1 from '/src/assets/laptop.ico';
import icono2 from '/src/assets/academica.svg';
import icono3 from '/src/assets/github_icon.svg';
import icono4 from '/src/assets/cellphone.svg';
import icono5 from '/src/assets/eficiente.svg';
import icono6 from '/src/assets/scrum.svg';

import { ref } from 'vue';
const titulo = 'Desarrollador Full Stack en formación';
const fecha = 'Desde Enero 2022 / Julio 2025';
const experiencias = ref([
    { id: 1, src: icono1, parrafo: 'Participé en el desarrollo de aplicaciones web integrando HTML, CSS, JavaScript y Vue.js, mejorando la experiencia de usuario y el rendimiento del sitio.' },
    { id: 2, src: icono2, parrafo: 'Colaboré en proyectos académicos y personales utilizando Python y Java, aplicando principios de programación orientada a objetos y bases de datos relacionales.' },
    { id: 3, src: icono3, parrafo: 'Gestioné versiones y control de código mediante Git y GitHub, optimizando el trabajo colaborativo en entornos de desarrollo.' },
    { id: 4, src: icono4, parrafo: 'Implementé diseños responsivos y accesibles, asegurando compatibilidad entre navegadores y dispositivos móviles.' },
    { id: 5, src: icono5, parrafo: 'Desarrollé scripts automatizados para tareas repetitivas en Python, reduciendo los tiempos de ejecución en un 30%.' },
    { id: 6, src: icono6, parrafo: 'Participé en prácticas de desarrollo ágil con metodologías SCRUM, favoreciendo la organización y entrega continua de resultados.' },
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

            <!-- <li class="item"><img class="imagen-svg" src="/src/assets/ventas.svg" width="45rem" alt="">
                <p>Lideré un equipo de 5 desarrolladores en la creación de una plataforma de comercio electrónico que incrementó las ventas en un 35% durante el primer año.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/ecomerce.svg" width="45rem" alt="">
                <p>Diseñé y desarrollé aplicaciones web utilizando Node.js, React y MongoDB, logrando reducir el tiempo de carga de las páginas en un 50%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/configuracion.svg" width="45rem" alt="">
                <p>Implementé soluciones de autenticación y autorización, mejorando la seguridad del sitio web y reduciendo los intentos de acceso no autorizado en un 20%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/uiux.svg" width="45rem" alt="">
                <p>Colaboré con diseñadores de UX/UI para crear interfaces de usuario atractivas y fáciles de usar, aumentando la satisfacción del cliente en un 15%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/watch.svg" width="45rem" alt="">
                <p>Automaticé procesos de despliegue continuo utilizando Jenkins y Docker, reduciendo los tiempos de despliegue en un 40%.</p>
            </li> -->
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: rgb(122, 91, 183);
}

.fecha {
    font-size: 1rem;
    color: rgb(134, 173, 200);
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