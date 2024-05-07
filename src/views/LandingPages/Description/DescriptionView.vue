<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import DefaultNavbar from "../../../examples/navbars/NavbarDefault.vue";
import DefaultFooter from "../../../examples/footers/FooterDefault.vue";
import DefaultInfoCard from "../../../examples/cards/infoCards/DefaultInfoCard.vue";

//image
import bg0 from "@/assets/img/containers/container2.png";

//dep
import Typed from "typed.js";

//sections
//import Information from "./Sections/AboutInformation.vue";
//import AboutTeam from "./Sections/AboutTeam.vue";
//import Featuring from "./Sections/AboutFeaturing.vue";
//import Newsletter from "./Sections/AboutNewsletter.vue";

const body = document.getElementsByTagName("body")[0];
//hooks
onMounted(() => {
  body.classList.add("about-us");
  body.classList.add("bg-gray-200");

  if (document.getElementById("typed")) {
    // eslint-disable-next-line no-unused-vars
    var typed = new Typed("#typed", {
      stringsElement: "#typed-strings",
      typeSpeed: 90,
      backSpeed: 90,
      backDelay: 200,
      startDelay: 500,
      loop: true,
    });
  }
});

onUnmounted(() => {
  body.classList.remove("about-us");
  body.classList.remove("bg-gray-200");
});
</script>
<template>
  <DefaultNavbar :action="{
    route: 'contactus',
    label: 'Contacto',
    color: 'btn-white',
  }" transparent />
  <header class="bg-gradient-dark">
    <div class="page-header min-vh-50" :style="{ backgroundImage: `url(${bg0})` }">
      <span class="mask bg-gradient-dark opacity-6"></span>
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-8 text-center mx-auto my-auto">
            <h1 class="text-white">
              Descripción del Servicio
            </h1>
            <p class="lead mb-4 text-white opacity-8">
              
            </p>
          </div>
        </div>
      </div>
    </div>
  </header>
  <div class="container">
    <div class="container p-5">
      <div class="row justify-content-center">
        <DefaultInfoCard icon="content_copy" title="Arriendo" description="FlexCamp ofrece una innovadora propuesta de arriendo de campamentos que no requiere permisos de
              construcción, facilitando así una instalación y despliegue extremadamente rápidos.
              Esta característica es crucial para proyectos que necesitan ponerse en marcha de manera inmediata,
              eliminando las demoras asociadas a la gestión de autorizaciones y permisos." />
        <DefaultInfoCard icon="flip_to_front" title="Impacto Ambiental" description="Nuestros campamentos están equipados con tecnología ecoamigable, incluyendo sistemas de energía renovable
              y soluciones eficientes para la gestión de agua y residuos.
              Al integrar estas tecnologías, FlexCamp no solo cumple con las necesidades operativas de nuestros
              clientes, sino que también asegura un impacto ambiental mínimo." />
      </div>
      <div class="row justify-content-center">
        <DefaultInfoCard icon="content_copy" title="Comodidad" description="Cada unidad de FlexCamp está diseñada para ofrecer confort y seguridad, garantizando que todos los
              ocupantes tengan un espacio adecuado para su bienestar y eficiencia laboral.
              La flexibilidad de nuestros servicios permite adaptar cada instalación a las especificaciones exactas de
              cada proyecto, asegurando que todas las necesidades estén cubiertas desde el primer día." />
        <DefaultInfoCard icon="flip_to_front" title="Rapidez" description="Con FlexCamp, las empresas pueden avanzar rápidamente en sus proyectos con la seguridad de que su
              infraestructura temporal es no solo funcional y rápida de desplegar, sino también sostenible
              y adaptada a las más estrictas normas de calidad y seguridad. EcoCamp es el aliado perfecto para proyectos
              que demandan rapidez, eficiencia y responsabilidad ambiental." />
      </div>
    </div>
  </div>

  <DefaultFooter />
</template>
