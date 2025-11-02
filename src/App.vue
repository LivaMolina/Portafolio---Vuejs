<!--funcionamiento de Vue composition Appi basica-->
<script setup>
//App.vue es un archivo raíz de nuestra aplicación y puede cargar archivos de javascript los puede ejecutar en forma de html y tb darle estilos
//puro javascript
//el setup lo que hace es que todo lo que pongamos dentro de las etiquetas script no hace falta importarlo
//directamente utilizando {{}} (doble llave o bigote) vamos a poder hacer que funcione en forma reactiva en vue
//const nombreApellido = 'Ivana Molina';

import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import Educacion from './components/EducacionComponente.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';
import ProyectosComponente from './components/ProyectosComponente.vue';
import HabilidadesComponente from './components/HabilidadesComponente.vue';
import InteresesComponente from './components/InteresesComponente.vue';
</script>
<!--template es una etiqueta-->
<!--html con herramientas de vue-->
<template>
  <!--dentro del template podemos usar html puro o javascript en forma reactiva-->
  <header id="top">
  <!--aquí utilizamos javascript-->
  <!--<h1>{{ nombreApellido }}</h1>-->
  <!--esto lo generaos con html, esto es html puro-->
  <!--<p> Bienvenido a Vue 3</p>-->


  <!-- Barra de Navegacion -->

     <NavBar />

   <!-- Componente Datos Personales -->
    <DatosPersonales/>
  </header>
  <main>
    <!--el estilo css de section se encuentra en base.css-->
    <section id="educacion"><h2>Educación - Cursos</h2>
    <!-- Componente Educación-->
    <Educacion />
    
    </section>
    <section id="experiencia"><h2>Experiencia</h2>
    <!-- Componente Experiencia -->
    <ExperienciaComponente />

    </section>
    <section id="proyectos"><h2>Proyectos</h2>
    <!-- Componente Proyectos -->
    <ProyectosComponente />
    
    </section>
    <section id="habilidades"><h2>Habilidades</h2>
    <!-- Componente Habilidades -->
    <HabilidadesComponente />
    </section>
    <section id="intereses"><h2>Intereses</h2>
    <!-- Componente Intereses -->
    <InteresesComponente />
    </section>
  </main>
   <footer>
        <a href="#top">Inicio</a>
        <p>© 2025 Ivana Molina - Portafolio web - tutorial UTN FRSR</p>
    </footer>
</template>
<!--código de css-->
<style scoped>
footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2rem;
    font-size: 1.3rem;
}
</style>
