<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>

    <radio-group :items="items"></radio-group>

    </v-flex>
  </v-layout>
</template>

<script>
import RadioGroup from '~/components/radio-group.vue'
import data from '~/static/items.json'

export default {
  components: {
    RadioGroup
  }, 
  data() {
    return {
      items: data.items
    }
  }
}
</script>
