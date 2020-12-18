<template>
    <b-container class="p-5" >
        <b-row>
            <b-col class="text-center">
              <h6>{{title}}</h6>
            </b-col>
        </b-row>
        <b-row>
       <b-col>
          <VueSvgGauge
        :start-angle="-90"
        :end-angle="90"
        :value= "value"
        :separator-step= "separatorStep"
        :separator-thickness= "2"
        :min="0"
        :max="100"
        :gauge-color="[{ offset: 0, color: '#C62424'}, { offset: 45, color: '#E0A800'}, { offset: 100, color: '#42B983'}]"
        :scale-interval="0.1"
        >
        </VueSvgGauge>
       </b-col>
        </b-row>
    </b-container>
</template>

<script>
import { VueSvgGauge } from 'vue-svg-gauge'
export default {
  names: VueSvgGauge,
  components: {
    VueSvgGauge
  },
  props: {
    value: {
      type: Number,
      requires: true
    },
    title: {
      type: String,
      requires: true
    },
    separatorStep: {
      type: Number,
      requires: true
    }
  }
}
</script>

<style>
  .card-gauge{
    padding: 5px;
  }
</style>
