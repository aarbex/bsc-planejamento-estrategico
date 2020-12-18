<template>
    <q-layout view="hHh Lpr lff">
    <q-header elevated class="bg-brown-13">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
        <q-icon
        name="menu"
        @click="leftDrawerOpen = !leftDrawerOpen"
        style="font-size: 1.5em;"
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
          class="text-brown"
        >
          Menu
        </q-item-label>
        <EssentialLink
        class="text-brown"
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>
    <q-page-container>
    <b-card>
      <b-tabs
      brown
      pills
      fill
      card
      title-item-class="text-danger"
      active-nav-item-class="font-weight-bold text-uppercase text-white bg-brown"
      active-tab-class="font-weight-bold text-brown"
      content-class="mt-3">
        <b-tab no-body title="Financeiro" title-link-class="text-brown">
           <b-container display="flexbox">
            <b-row cols="3">
                <b-col
                align-self="end"
                v-for="gauge in valoresFinanceiro"
        :key="gauge.value"
         v-bind="gauge.value"
                >
          <VueSvgGauge
        :value="gauge.value"
        :title="gauge.title"
        :separator-step="gauge.separatorStep"
        >
        </VueSvgGauge>
        </b-col>
        </b-row>
          </b-container>
        </b-tab>
        <b-tab no-body title="Cliente" title-link-class="text-brown">
          <b-container display="flexbox">
            <b-row cols="3">
                <b-col
                align-self="end"
                v-for="gauge in valoresCliente"
        :key="gauge.value"
        v-bind="gauge.value"
                >
      <VueSvgGauge
        :value="gauge.value"
        :title="gauge.title"
        :separator-step="gauge.separatorStep"
        >
        </VueSvgGauge>
        </b-col>
        </b-row>
          </b-container>
        </b-tab>
        <b-tab no-body title="Processos Internos" title-link-class="text-brown">
          <b-container display="flexbox">
            <b-row cols="3">
                <b-col
                align-self="end"
                v-for="gauge in valoresProcessos"
                    :key="gauge.value"
                    v-bind="gauge.value"
                >
                  <VueSvgGauge
                    :value="gauge.value"
                    :title="gauge.title"
                    :separator-step="gauge.separatorStep"
                    >
                    </VueSvgGauge>
                </b-col>
        </b-row>
          </b-container>
        </b-tab>
        <b-tab no-body title="Aprendizado" title-link-class="text-brown">
          <b-container display="flexbox">
            <b-row cols="3">
                <b-col
                align-self="end"
                v-for="gauge in valoresAprendizado"
       :key="gauge.value"
       v-bind="gauge.value"
                >
        <VueSvgGauge
        :value="gauge.value"
        :title="gauge.title"
        :separator-step="gauge.separatorStep"
        >
        </VueSvgGauge>
        </b-col>
        </b-row>
          </b-container>
        </b-tab>
      </b-tabs>
    </b-card>
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
    caption: 'Acompanhamento de metas',
    icon: 'leaderboard',
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
<style scoped>{

 }
</style>
