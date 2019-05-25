<template>

  <!-- Single button triggers two b-collapse components -->
  <!--<b-button v-b-toggle.collapseA.collapseB variant="primary">-->
  <!--<i class="fa fa-lightbulb-o"></i>&nbsp;Montrer Calendrier-->
  <!--</b-button>-->
  <div>
    <b-row>

      <!--Single button triggers two b-collapse components-->
      <b-col col="6" sm="6" style="width: 262px; height: 55px; margin: 10px;">
        <b-button v-on:click="seen = !seen" variant="primary">
          <i class="fa fa-lightbulb-o" v-if="!seen">  Montrer Calendrier</i>
          <i class="fa fa-power-off" v-if="seen"> Cache Calendrier</i>

        </b-button>
      </b-col>
    </b-row >
    <b-card class="card-accent-info" header="Dates" v-if="seen">
      <m-d-datapicker-plugin> </m-d-datapicker-plugin>
    </b-card >
  </div>


</template>

<script>
  import MDDatapickerPlugin from './MdDatapickerPlugin'
  export default {
    name: "calendrier",

    components:{
      MDDatapickerPlugin
    },
    data(){
      return {
        seen:true,
        data_start:{
          title:"Depuis de"
        },
        data_end:{
          title:"Jusqu'à"
        }

      }
    }
  }
</script>

<style scoped>

</style>
