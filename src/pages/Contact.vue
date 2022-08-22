<template>
  <q-page>
    <div class="q-pa-md">
    <div class="q-gutter-md" style="max-width: 300px">
    <q-input
    rounded
    outlined
    v-model="text"
    label="Name" />
    <q-input
    rounded
    v-model="date"
    outlined
    type="date"
    label="Data de entrega da encomenda" />
    <q-input
    rounded
    outlined
    v-model="text"
    label="Quer escrever algo no bolo?" />
    <q-input
    rounded
    v-model.number="tel"
    outlined type="tel"
    label="Telephone number" />
    <q-input
      rounded
      v-model="text"
      outlined
      type="textarea"
      label="Descrição do bolo (opcional)"
    />
      <q-input
        @update:model-value="val => { file = val[0] }"
        outlined
        rounded
        type="file"
        hint="Native file"
      />
    </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Contact'
})
</script>
