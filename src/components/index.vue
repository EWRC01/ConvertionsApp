<template class="generalTemplate" lang="html">

  <section class="src-components-index">
    
      <!--Agregar titulo-->
    <section class="divIcon">
   <p class="h1 mb-2">Medidas de conversion <b-icon icon="calculator-fill"></b-icon></p>
   </section>
      <!--Implementacion de la primera pagina-->
      <div class="page1Lengths">
        <Page1/>
        </div>
  </section>
 
</template>

<script lang="js">
import Page1 from './pageLengths.vue';

  export default  {
    name: 'src-components-index',
    components:{
      Page1

    },
    props: [],
    mounted () {

    },
    data () {
      return {

      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
.src-components-index {
  color: black;
}
.divIcon {
  color: white;
  margin: 0;
  padding: 10px;
}

</style>
