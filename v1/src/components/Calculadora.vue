<template>
  <div >
  <b-card
    title="CALCULADORA SIMPLE V1"
    tag="article"
    style="max-width: 30rem;"
    class="mb-4"
  >
    <b-card-text>
    
      <div class="border">
      </div>
      <hr>
<input type="number" :value="value0" @input="numberone = $event.target.value" class="form-control" >
<input type="number" :value="value1" @input="numbertwo = $event.target.value" class="form-control">
<button class="btn btn-danger w-100 mt-2" v-on:click="operacion()">Resolver</button>
<hr>
<p class="alert alert-danger">Suma: {{mensaje}}</p>
<p  class="alert alert-warning">Resta: {{mensaje2}}</p>
<p  class="alert alert-primary">Multiplicación: {{mensaje3}}</p>

    </b-card-text>

  
  </b-card>
</div>
</template>

<script>
export default {
  name: 'Calculadora',
  props: ['value0', 'value1'],
     data: function () {
        return {
            numberone: null,
            numbertwo: null,
            mensaje: null,
            mensaje2: null,
            mensaje3: null
        }
    },
    methods: {
        operacion() {
            this.mensaje = parseInt(this.numberone) +
                parseInt(this.numbertwo);
            this.mensaje2 = parseInt(this.numberone) -
                parseInt(this.numbertwo);
            this.mensaje3 = parseInt(this.numberone) *
                parseInt(this.numbertwo);
        }
    },
}
</script>

