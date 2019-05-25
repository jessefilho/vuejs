<template>
  <div>
    <h6>Depuis de:</h6>
    <date-picker v-model="date" :config="options" aria-placeholder="asdeae"></date-picker>
  <p>{{date}}</p>
  </div>


</template>

<script>



  import datePicker from 'vue-bootstrap-datetimepicker';
  import 'bootstrap/dist/css/bootstrap.css';
  import 'pc-bootstrap4-datetimepicker/build/css/bootstrap-datetimepicker.css';
  //Vue.use(datePicker);

  export default {
    name: "plugindatapickerBootstrap",
    components:{
      datePicker
    },
    data() {
      return {
        date: null,
        options: {
          // https://momentjs.com/docs/#/displaying/
          format: 'DD/MM/YYYY',
          useCurrent: false,
          showClear: true,
          showClose: true
        }
      }
    },
  }
</script>

<style>

</style>
