<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import DefaultNavbar from "../../../examples/navbars/NavbarDefault.vue";
import DefaultFooter from "../../../examples/footers/FooterDefault.vue";

//image
import bg0 from "@/assets/img/containers/wellcampimage1.png";
import logoflex1 from "@/assets/img/LogosFlexCamp/logo_flexcamp1.png"
import wavesWhite from "@/assets/img/waves-white.svg";

//dep
import Typed from "typed.js";

//sections
import Information from "./Sections/AboutInformation.vue";
import AboutTeam from "./Sections/AboutTeam.vue";
import Featuring from "./Sections/AboutFeaturing.vue";
import Newsletter from "./Sections/AboutNewsletter.vue";

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
    route: '/',
    label: 'Home',
    color: 'btn-info',
  }" transparent />
  <header class="bg-gradient-dark">
    <div class="page-header min-vh-75" :style="{ backgroundImage: `url(${bg0})` }">
      <span class="mask bg-gradient-dark opacity-6"></span>
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-8 text-center mx-auto my-auto">
            <!-- <h1 class="text-white">
              Work with an amazing <span class="text-white" id="typed"></span>
            </h1>
            <div id="typed-strings">
              <h1>team</h1>
              <h1>design</h1>
              <h1>tool</h1>
            </div> -->
            <h1 class="text-white">Acerca de</h1>
            <img :src="logoflex1" alt="" class="image-fluid" style="width: 22rem;">
            <p class="lead mb-4 text-white opacity-8">
              Flex Camp es un innovador spin-off de Biznet IT, creado en consorcio con Transporte Nuevo Mundo
              y con la representación estratégica de la compañía china Well Camp. Nos especializamos en el desarrollo,
              instalación y gestión de campamentos móviles ecológicos que combinan funcionalidad, rapidez y
              sostenibilidad.
              Nuestro enfoque está en ofrecer soluciones de alojamiento temporales que respetan el medio ambiente
              sin sacrificar la comodidad ni la eficiencia.
            </p>
            <p class="lead mb-4 text-white opacity-8">
              Nuestra misión en Flex Camp es transformar la manera en que se configuran y utilizan los espacios
              temporales
              para trabajo y vida. Nos comprometemos a proporcionar soluciones de campamento que no solo sean rápidas y
              flexibles,
              sino que también promuevan la sostenibilidad ambiental y mejoren la calidad de vida de sus usuarios.
            </p>
            <p class="lead mb-4 text-white opacity-8">
              En Flex Camp, aspiramos a ser líderes globales en soluciones de campamentos móviles ecológicos.
              Nuestra visión es expandir nuestra presencia a nivel mundial, ofreciendo productos que se destacan por su
              innovación,
              calidad y respeto por el planeta. Queremos establecer nuevos estándares en la industria, demostrando que
              es posible
              combinar la eficiencia operativa con el cuidado del medio ambiente.
            </p>
            
            <!-- <button type="submit" class="btn bg-white text-dark">
              Create Account
            </button>
            <h6 class="text-white mb-2 mt-5">Find us on</h6>
            <div class="d-flex justify-content-center">
              <a href="javascript:;"
                ><i class="fab fa-facebook text-lg text-white me-4"></i
              ></a>
              <a href="javascript:;"
                ><i class="fab fa-instagram text-lg text-white me-4"></i
              ></a>
              <a href="javascript:;"
                ><i class="fab fa-twitter text-lg text-white me-4"></i
              ></a>
              <a href="javascript:;"
                ><i class="fab fa-google-plus text-lg text-white"></i
              ></a>
            </div> -->
          </div>
        </div>
      </div>
    </div>
  </header>
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
              <h4 class="text-white">
                Innovación
              </h4>
              <p class="text-white text-md">
                Continuamente buscamos formas de mejorar y evolucionar nuestros productos y servicios.
              </p>
              <h4 class="text-white">
                Sostenibilidad
              </h4>
              <p class="text-white text-md">
                Compromiso con prácticas que apoyan la preservación del medio ambiente.
              </p>
              <h4 class="text-white">
                Calidad
              </h4>
              <p class="text-white text-md">
                Garantizamos la más alta calidad en todos nuestros campamentos, asegurando durabilidad y
                confort.
              </p>
              <h4 class="text-white">
                Responsabilidad Social
              </h4>
              <p class="text-white text-md">
                Nos esforzamos por tener un impacto positivo en las comunidades donde
                operamos.
              </p>
              <h5 class="text-white">
                Con Flex Camp, descubrirás que rapidez y ecología pueden ir de la mano, ofreciendo soluciones prácticas
                y
                sostenibles adaptadas a las necesidades modernas.
              </h5>
              
              

            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- <div class="card card-body shadow-xl mx-3 mx-md-4 mt-n6">
    <Information />
    <AboutTeam />
    <Featuring />
    <Newsletter />
  </div> -->
  <DefaultFooter />
</template>
