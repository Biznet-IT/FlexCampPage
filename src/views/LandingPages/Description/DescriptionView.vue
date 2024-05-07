<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import DefaultNavbar from "../../../examples/navbars/NavbarDefault.vue";
import DefaultFooter from "../../../examples/footers/FooterDefault.vue";
import DefaultInfoCard from "../../../examples/cards/infoCards/DefaultInfoCard.vue";

//image
import bg0 from "@/assets/img/containers/container2.png";
import wavesWhite from "@/assets/img/waves-white.svg";

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
  <div class="container-fluid mt-sm-5 border-radius-xl" :style="{
    background: 'linear-gradient(195deg, rgb(66, 66, 74), rgb(25, 25, 25))'
  }">
    <div class="page-header py-6 py-md-5 my-sm-3 mb-3 border-radius-xl" :style="{
    backgroundImage: `url(${wavesWhite})`
  }" loading="lazy">
      <span class="mask bg-gradient-dark"></span>
      <div class="container">
        <div class="row">
          <div class="d-flex justify-content-center p-5">
            <div class="col-lg-8 ms-lg-5 text-center">
              <h2 class="text-white pb-5">
                Gestión de Recursos y Logística en FlexCamp
              </h2>

              <h4 class="text-white pb-3">
                Manejo de Agua y Energía
              </h4>
              <p class="text-white text-md">
                En FlexCamp, la gestión eficiente del agua y la energía son pilares fundamentales de nuestros
                campamentos móviles.
                Nuestra aproximación al suministro de agua incluye sistemas avanzados que aseguran un uso óptimo de este
                recurso vital.
                Utilizamos tecnologías de tratamiento y reciclaje para manejar tanto las aguas grises (provenientes de
                duchas y lavabos)
                como las aguas negras (deshechos sanitarios), transformándolas en agua segura para otros usos no
                potables,
                lo que reduce significativamente el consumo total de agua.
              </p>
              <p class="text-white text-md">
                Para el suministro energético, EcoCamp implementa soluciones basadas en fuentes renovables. Contamos con
                instalaciones
                de paneles solares y opciones de energía eólica, que no solo proveen una fuente de energía sostenible y
                continua,
                sino que también minimizan la huella de carbono de las operaciones en el campamento.
              </p>

            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="container mt-sm-5">
    <div class="page-header py-6 py-md-5 my-sm-3 mb-3 border-radius-xl" :style="{
    backgroundImage:
      'url(https://raw.githubusercontent.com/creativetimofficial/public-assets/master/soft-ui-design-system/assets/img/desktop.jpg)'
  }" loading="lazy">
      <span class="mask bg-gradient-dark"></span>
      <div class="container">
        <div class="row">
          <div class="d-flex justify-content-center p-5">
            <div class="col-lg-8 ms-lg-5 text-center">
              <h4 class="text-white pb-3">
                Logística y Colaboración con Well Camp
              </h4>
              <p class="text-white text-md">
                FlexCamp trabaja en colaboración con Well Camp, una renombrada empresa china especializada en la
                construcción de estructuras modulares.
                Esta alianza estratégica nos permite acceder a innovaciones líderes en el sector y a materiales de alta
                calidad, garantizando la durabilidad y
                eficiencia de nuestros campamentos.
              </p>
              <p class="text-white text-md">
                Nuestra infraestructura logística se apoya en una red de bodegas en China, donde almacenamos
                pre-fabricados y otros materiales esenciales.
                Este sistema nos permite mantener un flujo constante de recursos, asegurando una rápida respuesta a las
                necesidades de nuestros clientes
                en cualquier parte del mundo. Nuestro completo sistema de importación y logística está diseñado para
                manejar eficientemente la cadena de suministro
                desde la producción hasta la instalación en sitio, lo que nos permite ejecutar proyectos a gran escala
                con tiempos de entrega optimizados.
              </p>
              <p class="text-white text-md">
                Con estas capacidades, EcoCamp se establece no solo como un proveedor de soluciones habitacionales
                temporales, sino como un socio logístico integral
                que garantiza la operatividad y sostenibilidad de los campamentos en cualquier entorno. Esta combinación
                de gestión responsable de recursos y
                logística avanzada nos posiciona como líderes en la industria de alojamientos temporales para
                sectores críticos.
              </p>

            </div>
          </div>
        </div>
      </div>

    </div>
  </div>

  <DefaultFooter />
</template>
