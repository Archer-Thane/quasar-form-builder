<template>
  <div>
    <div>
      {{ label }}: {{ inputData }} ({{ min }} تا {{ max }})
    </div>
    <q-slider
      v-model="inputData"
      :min="min"
      :max="max"
      :disable="disable"
      :readonly="readonly"
      @update:model-value="change($event)"
      @click="onClick"
    />
  </div>
</template>

<script>
import inputMixin from '../mixins/inputMixin'
export default {
  name: 'FormBuilderSlider',
  mixins: [inputMixin],
  props: {
    value: {
      default: 0,
      type: Number
    }
  },
  methods: {

  }
}
</script>

<style scoped>

</style>
