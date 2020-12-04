<template>
  <q-layout row inline view="lHh Lpr lFf">
    <q-header elevated class="bg-brown-13">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title>
          BSC - Planejamento Estratégico
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-brown-2"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Menu
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>
    <q-page-container>
    <q-stepper
      v-model="step"
      ref="stepper"
      color="primary"
      header-nav
      animated
    >
      <q-step
        :name="1"
        title="Financeiro"
        icon="create_new_folder"
        >
        <VueSvgGauge
        style="width: 300px"
        v-for="gauge in valoresFinanceiro"
        :key="gauge.value"
         v-bind="gauge.value"
        :value="gauge.value"
        :title="gauge.title"
        :separator-step="gauge.separatorStep"
        >
        </VueSvgGauge>
       <!-- <VGauges>
        </VGauges> -->

      </q-step>

      <q-step
        :name="2"
        title="Cliente"
        icon="create_new_folder"
      >
        <div class="row inline justify-center">
       <div
       class="q-pa-md"
       v-for="gauge in valoresCliente"
       :key="gauge.value"
       v-bind="gauge.value"
       >
        <!-- <Gauges
        :value="gauge.value"
        :title="gauge.title"
        ></Gauges> -->
        <VueSvgGauge
        class="col"
        :value="gauge.value"
        :title="gauge.title"
        :separator-step="gauge.separatorStep"
        >
        </VueSvgGauge>
       </div >
       <!-- <VGauges>
        </VGauges> -->

    </div>
      </q-step>

      <q-step
        :name="3"
        title="Processos Internos"
        icon="add_comment"
      >
        <div class="row inline justify-center ">
       <div
       class="q-pa-md itens-end"
       v-for="gauge in valoresProcessos"
       :key="gauge.value"
       v-bind="gauge.value"
       >
        <!-- <Gauges
        :value="gauge.value"
        :title="gauge.title"
        ></Gauges> -->
        <VueSvgGauge
        class="col itens-end"
        :value="gauge.value"
        :title="gauge.title"
        :separator-step="gauge.separatorStep"
        >
        </VueSvgGauge>
       </div >
       <!-- <VGauges>
        </VGauges> -->

    </div>
      </q-step>
      <q-step
        :name="4"
        title="Aprendizado e Crescimento"
        icon="add_comment"
      >
       <div
       style="width: 300px"
       v-for="gauge in valoresAprendizado"
       :key="gauge.value"
       v-bind="gauge.value"
       >
        <!-- <Gauges
        :value="gauge.value"
        :title="gauge.title"
        ></Gauges> -->
        <VueSvgGauge
        :value="gauge.value"
        :title="gauge.title"
        :separator-step="gauge.separatorStep"
        >
        </VueSvgGauge>
       </div >
       <!-- <VGauges>
        </VGauges> -->
      </q-step>

      <!-- <template v-slot:navigation>
        <q-stepper-navigation>
          <q-btn @click="$refs.stepper.next()" color="primary" :label="step === 3 ? 'Finish' : 'Continue'" />
          <q-btn v-if="step > 1" flat color="primary" @click="$refs.stepper.previous()" label="Back" class="q-ml-sm" />
        </q-stepper-navigation>
      </template> -->
    </q-stepper>
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'
// import Gauges from 'components/Gauges.vue'
// import VGauges from 'components/Gauge.vue'
import VueSvgGauge from 'components/VueSvgGauge.vue'

const linksData = [
  {
    title: 'Dashboard',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  }
]

export default {
  name: 'MainLayout',
  components: { EssentialLink, VueSvgGauge },
  data () {
    return {
      valoresFinanceiro: [
        {
          value: 30,
          title: 'Geração de novas fontes de financiamento',
          separatorStep: 60
        },
        {
          value: 35,
          title: '% do orçado versus realizado',
          separatorStep: 100
        }
      ],
      valoresCliente: [
        {
          value: 45,
          title: 'Satisfação com os Serviços Públicos Prestados',
          separatorStep: 75
        },
        {
          value: 45,
          title: 'Oportunidade e Responsabilidade Solidária',
          separatorStep: 60
        },
        {
          value: 20,
          title: 'Priorização da infraestrutura urbana',
          separatorStep: 60
        },
        {
          value: 50,
          title: 'Referência e qualidade de vida',
          separatorStep: 50
        },
        {
          value: 10,
          title: 'Promoção do cidadão',
          separatorStep: 50
        }
      ],
      valoresProcessos: [
        {
          value: 25,
          title: 'Desenvolvimento de políticas públicas',
          separatorStep: 100
        },
        {
          value: 80,
          title: 'Promover a urbanização',
          separatorStep: 100
        },
        {
          value: 25,
          title: 'Promover o acesso às condições de cidadania',
          separatorStep: 60
        }
      ],
      valoresAprendizado: [
        {
          value: 20,
          title: 'Desenvolvimento dos servidores municipais',
          separatorStep: 70
        }
      ],
      leftDrawerOpen: false,
      essentialLinks: linksData,
      step: 1
    }
  }
}
</script>
<style scoped>

</style>
