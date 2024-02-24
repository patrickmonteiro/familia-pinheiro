<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>
          Família Pinheiro
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-footer elevated>
      <!-- <q-toolbar> -->
        <q-tabs
          v-model="tab"
          inline-label
          class="bg-primary text-white shadow-2"
        >
          <q-route-tab
            name="home"
            icon="home"
            label="Home"
            to="/"
            exact
          />
          <q-route-tab
            name="Aniversários"
            icon="cake"
            label="niver"
            to="/niver"
            exact
          />
        </q-tabs>
      <!-- </q-toolbar> -->
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref, onMounted } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
  },

  setup () {
    const tab = ref('')

    onMounted(() => {
      // Solução para recarregar Safari quando não encontrar arquivos JS
      window.addEventListener('error', (e) => {
        const srcError = e.target.src
        if (srcError.includes('/js/')) {
          window.location.reload()
        }
      }, true)
    })
    return {
      tab
    }
  }
})
</script>
