<template>
  <div >
  <b-card
    title="Sumas"
    tag="article"
    style="max-width: 30rem;"
    class="mb-4"
  >
    <b-card-text>
    
      <div class="border">
      </div>
      <hr>
      <input type="number" v-model="valueA"  class="form-control">

      <input type="number" v-model="valueB"  class="form-control">

      <hr>
      {{(valueA)+(valueB)}}

    </b-card-text>

  
  </b-card>
</div>
</template>

<script>
export default {
  name: 'Calculadora',
  props: {
    msg: String
  },
  data(){
    return{
      valueA: 0,
      valueB: 0,
    }
  },
  computed:{

  }
}
</script>

