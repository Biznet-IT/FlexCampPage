<script setup>
import DefaultCounterCard from "../../../examples/cards/counterCards/DefaultCounterCard.vue";
</script>

<template>
  <section class="pt-3 pb-4" id="count-stats">
    <div class="container">
      <div class="row">
        <div class="col-lg-9 z-index-2 border-radius-xl mx-auto py-3">
          <div class="row">
            <div class="col-md-3 position-relative">
              <DefaultCounterCard
                color="success"
                title="Pcs|40HQ"
                description=""
                :count="12"
                suffix=""
                :duration="3000"
                divider="vertical"
              />
            </div>
            <div class="col-md-3 position-relative">
              <DefaultCounterCard
                color="success"
                title="A prueba de Fuego"
                description=""
                :count="100"
                suffix="%"
                :duration="3000"
                divider="vertical"
              />
            </div>
            <div class="col-md-3">
              <DefaultCounterCard
                color="success"
                title="Plegable"
                description=""
                :count="100"
                suffix="%"
                :duration="3000"
                divider="vertical"
              />
            </div>
            <div class="col-md-3">
              <DefaultCounterCard
                color="success"
                title="A prueba de Agua"
                description=""
                :count="100"
                suffix="%"
                :duration="3000"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
