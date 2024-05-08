<script setup>
import RotatingCard from "../../../examples/cards/rotatingCards/RotatingCard.vue";
import RotatingCardFront from "../../../examples/cards/rotatingCards/RotatingCardFront.vue";
import RotatingCardBack from "../../../examples/cards/rotatingCards/RotatingCardBack.vue";
import DefaultInfoCard from "../../../examples/cards/infoCards/DefaultInfoCard.vue";
</script>
<template>
  <section class="my-5 py-5">
    <div class="container" >
      <div class="row align-items-center">
        <div class="col-lg-4 ms-auto me-auto p-lg-4 mt-lg-0 mt-4">
          <RotatingCard>
            <RotatingCardFront
              image="https://images.unsplash.com/photo-1569683795645-b62e50fbf103?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80"
              icon="touch_app" title="Explora nuestros Productos" description="Hay una amplia variedad para elegir." />

            <RotatingCardBack
              image="https://images.unsplash.com/photo-1498889444388-e67ea62c464b?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1365&q=80"
              title="Descubre Más"
              description="Nuestros productos incluyen Casas de Container, Oficinas de Container, estructuras de metal y más."
              :action="[
                {
                  route: './',
                  label: 'Productos',
                },
              ]" />
          </RotatingCard>
        </div>
        <div class="col-lg-6 ms-auto">
          <div class="row justify-content-start">
            <div class="card m-3" style="width: 18rem;">
              <img src="src\assets\img\containers\container-shop.png" class="card-img-top" alt="...">
              <div class="card-body">
                <p class="card-text">Containers para Tiendas</p>
              </div>
            </div>
            <div class="card m-3" style="width: 18rem;">
              <img src="src\assets\img\containers\container-office.png" class="card-img-top" alt="...">
              <div class="card-body">
                <p class="card-text">Containers para Tiendas</p>
              </div>
            </div>
            <div class="card m-3" style="width: 18rem;">
              <img src="src\assets\img\containers\container-storage.png" class="card-img-top" alt="...">
              <div class="card-body">
                <p class="card-text">Containers para Tiendas</p>
              </div>
            </div>
            <!-- <DefaultInfoCard
            image="container-camp.png"
              icon="content_copy"
              title="Shop"
              description="Built by developers for developers. Check the foundation and
                  you will find everything inside our documentation."
            />
            <DefaultInfoCard
              icon="flip_to_front"
              title="Office"
              description="The world’s most popular front-end open source toolkit,
                  featuring Sass variables and mixins."
            />
            <DefaultInfoCard
              icon="flip_to_front"
              title="Storage"
              description="The world’s most popular front-end open source toolkit,
                  featuring Sass variables and mixins."
            /> -->
          </div>

        </div>
      </div>
    </div>
  </section>
</template>
