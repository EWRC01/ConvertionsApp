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
        <b-form-input type="number" id="n1"></b-form-input>
      </b-form-group>

      <b-form-group
        label="Segundo valor:"
        label-for="n2"
        label-cols-sm="3"
        label-align-sm="right"
      >
        <b-form-input type="number" id="n2"></b-form-input>
      </b-form-group>
      <b-form-group
        label="Conversion a:"
        label-cols-sm="3"
        label-align-sm="right"
        class="mb-0"
        v-slot="{ ariaDescribedby }"
      >
        <b-form-radio-group
          class="pt-2"
          :options="['Metros a Kilometros', 'Kilometros a Metros', 'Centimetros a Metros', 'Metros a Centimetros']"
          :aria-describedby="ariaDescribedby"
        ></b-form-radio-group>
        <hr>
        <b-button variant="dark" size="lg" class="pt-2">Convertir a</b-button>
        <hr>
        <b-form-group
        label="Respuesta: "
        
        ></b-form-group>
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

      }
    },
    methods: {

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
