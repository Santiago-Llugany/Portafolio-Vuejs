<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import EducacionComponente from './components/EducacionComponente.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';
import ProyectoComponente from './components/ProyectoComponente.vue';
import HabilidadesComponente from './components/HabilidadesComponente.vue';
import InteresesComponente from './components/InteresesComponente.vue';
import FondoBurbujas from './components/FondoBurbujas.vue';
</script>

<template>
 <div>
  <FondoBurbujas />
  <header id="top">
      <!--Barra de navegacion-->
      <NavBar />
      <!--Componente Datos Personales-->
      <DatosPersonales />
  </header>
  <main>
    <!--el estilo css de section se encuentra en base.css-->
    <section id="educacion"><h2>Educación - Cursos</h2>
    <EducacionComponente />
    </section>
    <section id="experiencia"><h2>Experiencia</h2>
    <ExperienciaComponente />
    </section>
    <section id="proyectos"><h2>Proyectos</h2>
    <ProyectoComponente />
    </section>
    <section id="habilidades"><h2>Habilidades</h2>
    <HabilidadesComponente />
    </section>
    <section id="intereses"><h2>Intereses</h2>
    <InteresesComponente />
    </section>
  </main>
  <footer>
        <a href="#top">Inicio</a>
        <p>2024 Santiago Llugany - Portafolio web - estudiante UTN FRSR</p>
  </footer>
 </div>
  
</template>

<style scoped>
a{
  color: rgb(43, 89, 226);
}
footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2rem;
    font-size: 1.3rem;
}
</style>
