<template>
  <q-page padding>
    <div class="row justify-center">
      <q-list bordered class="col-xs-10" v-for="(niver, index) in aniversarios" :key="index">
        <q-item-label header> {{ niver.mes }} - {{ niver.descricao }}</q-item-label>

        <q-item v-for="(pessoa, index) in niver.pessoas" :key="index" class="q-mb-sm" clickable v-ripple>
          <q-item-section avatar>
            <q-avatar color="primary" text-color="white" size="sm">
              {{ pessoa.dia }}
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label>{{ pessoa.nome }}</q-item-label>
            <!-- <q-item-label caption lines="1">{{ pessoa.dia }}</q-item-label> -->
          </q-item-section>

          <!-- <q-item-section side>
            <q-icon name="chat_bubble" color="grey" />
          </q-item-section> -->
        </q-item>
      </q-list>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import useNiver from 'src/constantes/nivers'

export default defineComponent({
  name: 'PageNiver',
  setup () {
    const { aniversarios } = useNiver()

    return {
      aniversarios
    }
  }
})
</script>
