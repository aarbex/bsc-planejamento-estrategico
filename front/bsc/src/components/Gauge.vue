<template>
  <div class="q-pa-md column flex-center">
        <div><h5>{{title}}</h5></div>
        <VueGauge
        :refid="'type-unique-id'"
        :options="{'needleValue':85,
                    'arcDelimiters':[10,36,78],
                    'hasNeedle':false}"
        >
        </VueGauge>
       </div>
</template>

<script>
import VueGauge from 'vue-gauge'

export default {
  names: 'VGauges',
  components: { VueGauge },
  props: {
    value: {
      type: Number,
      requires: true
    },
    title: {
      type: String,
      requires: true
    }
  }
}
</script>

<style>

</style>
