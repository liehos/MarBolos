<template>
  <q-page>
  <div class="q-pt-md">

    <q-carousel
      animated
      swipeable
      transition-next="slide-left"
      v-model="slide"
      arrows
      navigation
      infinite
      autoplay="true"
      draggable="false"
      height="32rem"
    >
      <q-carousel-slide
      :name="1"
      img-src="image1.jpeg"
      />
      <q-carousel-slide
      :name="2"
      img-src="image2.jpeg" />
      <q-carousel-slide
      :name="3"
      img-src="image3.jpeg" />
      <q-carousel-slide
      :name="4"
      img-src="image4.jpeg" />
    </q-carousel>
  </div>

  <div>
    <div class="row">
      <div class="col">
    <q-btn
      unelevated
      rounded
      color="primary"
      label="Faça já a sua encomenda"
      to="/contact"
      class="q-ma-md text=center"
      />
      </div>
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
