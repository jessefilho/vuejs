<template>
  <b-row>
    <b-col col="6" sm="6">
    <h6>Depuis de:</h6>
      <md-datepicker v-model="selectedDateStart" md-immediately md-open-on-focus=false ></md-datepicker>
    </b-col>
    <b-col col="6" sm="6">
    <h6>Jusqu'à:</h6>
    <md-datepicker v-model="selectedDateEnd" md-immediately md-open-on-focus=false ></md-datepicker>
    </b-col>
  </b-row>
</template>

<script>

  import VueMaterial from 'vue-material'
  import 'vue-material/dist/vue-material.min.css'
  import 'vue-material/dist/theme/default.css'
  export default {
    name: "mddatapickerplugin",
    components:{
      VueMaterial
    },

    data(){
      return {
        selectedDateEnd: new Date(),
        selectedDateStart: null

      }
    }
  }
</script>

<style>

</style>
