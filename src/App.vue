<template>
  <div class="container bg-gray-200 m-auto p-40 min-h-screen">
    <radio-button :type="type" :title="title" :options="options" v-model:choice="choice" />
    <div class="mx-auto max-w-sm p-2 rounded bg-indigo-700 text-white text-center">
      <span>Selecionado: {{ choice }}</span>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import RadioButton from './components/RadioButton.vue'
export default {
  components: { RadioButton },
  setup () {
    // DATA
    const type = ref('col') // row or col
    const title = ref('Make the right choice:')
    const options = ref([
      { text: 'Best choice', value: 'best' },
      { text: 'First choice', value: 'first' },
      { text: 'Second choice', value: 'second' },
      { text: 'Thirde choice', value: 'third' },
      { text: 'Fourth choice', value: 'fourth' },
      { text: 'Choice Five with a longer title', value: 'five' },
    ])
    const choice = ref('best')

    return { type, title, options, choice }
  }
}
</script>

<style>

</style>
