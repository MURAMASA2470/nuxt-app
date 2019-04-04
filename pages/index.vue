<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex
      xs12
      sm8
      md6
    >

    <btn-style-radio :items="items"></btn-style-radio>

    </v-flex>
  </v-layout>
</template>

<script>
import BtnStyleRadio from '~/components/btn-style-radio.vue'
import data from '~/static/items.json'

export default {
  components: {
    BtnStyleRadio
  }, 
  data() {
    return {
      items: data.items
    }
  }
}
</script>
