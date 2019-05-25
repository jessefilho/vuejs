<template>
    <b-card :no-body="true" footer-class="px-3 py-2">
          <b-card-body class="p-3 clearfix">
            <i class="fa fa-warning bg-warning p-3 font-2xl mr-3 float-left"></i>
            <div class="h6 text-warning mb-0 mt-2">$100.000.999,50</div>
            <div class="text-muted text-uppercase font-weight-bold font-xs">Rebut CA</div>
          </b-card-body>
          <div slot="footer">
            <b-link class="font-weight-bold font-xs btn-block text-muted" href="#">View More <i class="fa fa-angle-right float-right font-lg"></i></b-link>
          </div>
        </b-card>
</template>

<script>
    export default {
        name: "ChiffresRebutcaTotal"
    }
</script>

<style scoped>

</style>
