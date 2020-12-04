<template>
  <div class="q-pa-md column flex-center">
        <div><h5>{{title}}</h5></div>
        <VGauge
        :value="value"
        unit="%"
        >
        </VGauge>
       </div>
</template>

<script>
import VGauge from 'vgauge'

export default {
  names: 'Gauges',
  components: { VGauge },
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
