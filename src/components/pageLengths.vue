<template lang="html">

  <section class="src-components-page-lengths">
    <b-card bg-variant="danger">
    <b-form-group
      label-cols-lg="3"
      label="Medidas de longitud"
      label-size="lg"
      label-class="font-weight-bold pt-0"
      class="mb-0"
    >
      <b-form-group
        label="Primer Valor:"
        label-for="n1"
        label-cols-sm="3"
        label-align-sm="right"
      >
        <b-form-input v-model="data1" type="number" id="n1"></b-form-input>
      </b-form-group>
      <b-form-group
        label="Conversion a:"
        label-cols-sm="3"
        label-align-sm="right"
        class="mb-0"
      >
        <b-form-group label="Por favor seleccione una opcion!">
          <b-form-radio-group
          id="radio-group-2"
          v-model="selected"
          name="radio-sub-component"
          >
          <b-form-radio id="kmToM"  value="1">Kilometros a Metros</b-form-radio>
           <b-form-radio id="mTokKm"  value="1">Metros a Kilometros</b-form-radio>
            <b-form-radio id="mToCm"  value="1">Metros a Centimetros</b-form-radio>
             <b-form-radio id="cmToM"  value="1">Centimetros a Metros</b-form-radio>
              <b-form-radio id="mToF"  value="1">Metros a pies</b-form-radio>
          </b-form-radio-group>
        </b-form-group>
        
        <hr>
        <b-button v-on:click="calcular1" variant="dark" size="lg" class="pt-2">Convertir a</b-button>
    </b-form-group>
    </b-form-group>
  </b-card>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-page-lengths',
    props: [],
    mounted () {

    },
    data () {
      return {
        selected: '',
        data1:''
        
       

        

      }
    },
    methods: {
      calcular1(){
       var elemento = document.getElementById("kmToM");
       var elemento1= document.getElementById("mTokKm");
       var elemento2 = document.getElementById("mToCm");
       var elemento3 = document.getElementById("cmToM");
       var elemento4 = document.getElementById("mToF");
       
        if (elemento.checked == true) {
         
          
          var obtenern= this.data1
          var equivalencia = 1000;
          var operacion =  (obtenern * equivalencia) 
          console.log(operacion );
          var res = (operacion + " Metros")
          alert(res);
          
          
         

        }
        else if (elemento1.checked == true)
        {
          var obtenern1=this.data1
          var equivalencia1 = 1000;
          var operacion1 = (obtenern1 / equivalencia1);
          console.log(operacion1);
          alert(operacion1 + " Kilometros");
         

        }
        else if (elemento2.checked == true)
        {
          var obtenern2=this.data1
          var equivalencia2 = 100;
          var operacion2 = (obtenern2 * equivalencia2);
          console.log(operacion2);
          alert(operacion2 + " Centimetros");
            
        }
        else if (elemento3.checked == true)
        {
          var obtenern3=this.data1
          var equivalencia3 = 100;
          var operacion3 = (obtenern3 / equivalencia3);
          console.log(operacion3);
          alert(operacion3 + " Metros");
         

        }
        else if (elemento4.checked == true)
        {
          var obtenern4=this.data1
          var equivalencia4 = 3.281;
          var operacion4 = (obtenern4 * equivalencia4);
          console.log(operacion4);
          alert(operacion4 + " Centimetros");
          

        }
        else {
          alert('Seleccione una opcion, por favor!')
        }

      }

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
.src-components-page-lengths {
  color: white;
}
</style>
