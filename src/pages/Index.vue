<template>
  <q-page class="flex flex-center bg-grey-2">
    <!-- <img
      alt="Quasar logo"
      src="brasao.jpeg"
      style="width: 400px; height: 400px"
      class="rounded-borders"
    > -->
    <q-btn round>
      <q-avatar size="300px">
        <img src="brasao.jpeg" >
      </q-avatar>
    </q-btn>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'PageIndex'
})
</script>
