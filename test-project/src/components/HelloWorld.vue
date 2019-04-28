<template>
  <div class="hello">
  <h1>{{ msg }}</h1>
  <p>What is {{ num1 }} times {{ num2 }}?<span v-if="product">{{ product }}</span></p>
<button v-on:click="calculateProduct">Calculate</button>
  <h2>2 Things that are difficult in JavaScript</h2>
  <h3>{{ name }}</h3>
  <ol>
    <li>naming things</li>
    <li>recursion</li>
    <li>off-by-one errors</li>
  </ol>
  </div>
</template>

<script>
export default {
  name: 'hello',
  props: {
    msg: String
  },
  data () {
    return {
      name: 'Georgina',
      num1: 42,
      num2: 78,
      product: null
    }
  },
  methods: {
    calculateProduct: function(){
      this.product = this.num1 * this.num2;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ol {
  list-style-type: decimal;
  width: 40%;
  margin: auto;
}

li {
  display: list-item;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
