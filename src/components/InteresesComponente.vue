<script setup>
import { ref } from 'vue';
//import FondoLava from './FondoLava.vue';
//Este es un arreglo con ref para que se pueda reactivar el cambio de los intereses
const intereses = ref([
    'Me apasiona el desarrollo de software y todo lo que tenga que ver con crear, aprender y mejorar. Disfruto los desafíos que me hacen pensar de forma diferente y me motivan a seguir creciendo.',
    'Valoro el trabajo en equipo y los proyectos que desafían mi pensamiento lógico y mi creatividad.',
    'Me fascina sumergirme en el mundo del código, explorar nuevos lenguajes y descubrir cómo la tecnología puede transformar ideas en realidad. Cada línea de código es para mí una pequeña chispa que conecta lógica y posibilidad.',
    'En mis momentos libres me encanta pasar tiempo con mi familia, compartir mates con amigos y disfrutar del aire libre. Me inspira la naturaleza, los paisajes lindos, la natación y los pequeños momentos que equilibran la rutina y me llenan de energía.'
]);
</script>

<template>
    <div class="intereses-contenedor">
       <!--<FondoLava />-->
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
    <!-- <div class="intereses-contenedor">
        <ul class="contenedor-lista">
            <li class="item">
                Desarrollo de Software de Código Abierto: Contribuyo a proyectos en GitHub, colaborando con otros
                desarrolladores para mejorar herramientas y librerías populares.
            </li>
            <li class="item">
                Deportes al Aire Libre: Disfruto del senderismo y el ciclismo de montaña, actividades que practico
                regularmente para mantener un equilibrio entre el trabajo y la vida personal.
            </li>
            <li class="item">
                Tecnología de Innovación: Me apasiona explorar nuevas tendencias tecnológicas como la inteligencia
                artificial y el desarrollo de aplicaciones móviles.
            </li>
            <li class="item">
                Fotografía: Practico la fotografía como un hobby, lo que me ayuda a mantener una perspectiva creativa
                tanto en mi vida profesional como personal.
            </li>
        </ul>
    </div> -->
</template>

<style scoped>

   .intereses-contenedor {
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 100%;
    padding: 2rem;
    background-image: url('@/assets/fondonaturaleza.jpg'); /* ruta del fondo */
    background-size: cover;        /* ocupa todo el contenedor */
    background-position: center;   /* centrado */
    background-attachment: fixed;  /* se mantiene fijo al hacer scroll */
    border-radius: 16px;           /* opcional: esquinas redondeadas */
    /*display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;*/
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.1rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
    
}

.item {
    margin-bottom: 1rem;
}
</style>