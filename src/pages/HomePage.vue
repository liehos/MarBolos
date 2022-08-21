<template>
  <q-page>
  <div class="q-pt-md">

    <q-carousel
      animated
      transition-next="slide-left"
      v-model="slide"
      arrows
      navigation
      infinite
      autoplay="true"
      draggable="false"
    >
      <q-carousel-slide :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg" />
      <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg" />
      <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg" />
      <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg" />
    </q-carousel>
  </div>

  <div>
    <div class="row">
      <div class="col-2"></div>
      <div class="col-8">
    <q-btn
      unelevated
      rounded
      color="primary"
      label="Faça já a sua encomenda"
      class="q-ma-md text=center"
      />
      </div>

  <div class="col-2"></div>
  </div>
</div>

  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import { ref } from 'vue'

export default defineComponent({
  name: 'HomePage',
  setup () {
    return {
      slide: ref(1)
    }
  }
})

</script>
