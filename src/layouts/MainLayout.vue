<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          <q-tabs
            v-model="tab"
          >
          <q-route-tab
          name="mails"
          icon="mail"
          to='/'
            />
          <q-route-tab
          name="alarms"
          icon="alarm"
          to='/gallery'

          />
          <q-route-tab
          name="movies"
          icon="movie"
          to='/contact'
          />
          </q-tabs>
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'
import { VueDevToolsLabels } from '@intlify/vue-devtools'

const linksList = [
  {
    title: 'Login',
    icon: 'login',
    link: 'https://quasar.dev'
  }
]

// const { a } = Vue

// const app = Vue.createApp({
//   setup () {
//     return {
//       tab: a("mails")
//     }
//   }
// })

// app.use(Quasar, { config: {} })
// app.mount('#q-app')

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
