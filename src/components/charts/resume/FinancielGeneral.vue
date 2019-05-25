<template>

  <b-row>
    <b-col sm="12">
      <h4 id="financielGeneral" class="card-title mb-0">Vue Global</h4>
      <div class="small text-muted">November 2019</div>
      <highcharts :options="chartOptions"></highcharts>
    </b-col>
  </b-row>
</template>

<script>
  //Implement hightCharts
  //https://github.com/highcharts/highcharts-vue#implementing-stockchart-and-mapchart
  import {Chart} from 'highcharts-vue'
  import Highcharts from 'highcharts'
  import stockInit from 'highcharts/modules/stock'
  stockInit(Highcharts)
  // import exportingInit from 'highcharts/modules/exporting'
  // exportingInit(Highcharts)

  //import * as cont from './container'


  export default {
    name: "FinancielGeneral",
    components:{
      Chart

    },created() { // load data here
      // let recaptchaScript = document.createElement('script')
      // recaptchaScript.setAttribute('src', 'https://www.google.com/recaptcha/api.js')
      // document.head.appendChild(recaptchaScript)

    }
    ,data(){
      return {
        chartOptions: {
          chart: {
            type: 'bar',
            color:['#60d85e', '#a49d0f', '#bc1516']
          },

          title: {
            text: 'Historic World Population by Region'
          },
          xAxis: {
            categories: ['1','2','3'],
            title: {
              text: null
            }
          },
          yAxis: {
            min: 0,

            title: {
              text: 'Total fruit consumption'
            }
          },
          tooltip: {
            valueSuffix: ' millions'
          },
          plotOptions: {
            series:{
              pointWidth:10 // width of bars

            },
            bar: {
              dataLabels: {
                enabled: true
              }
            }
          },
          legend: {
            layout: 'vertical',
            align: 'right',
            verticalAlign: 'top',
            x: -40,
            y: 80,
            floating: true,
            borderWidth: 1,
            backgroundColor: ((Highcharts.theme && Highcharts.theme.legendBackgroundColor) || '#FFFFFF'),
            shadow: true
          },
          credits: {
            enabled: false
          },
          series:// to do a json on REST API to return the follow structure
            [{
            name: 'CA',
            data: [1825, 31, 635, 203, 2]
          }, {
            name: 'M',
            data: [133, 156, 947, 408, 6]
          }, {
            name: 'R',
            data: [814, 841, 3714, 727, 31]
          }]

        }
      }
    }

  }
</script>

<style scoped>

</style>
