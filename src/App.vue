<template>
  <div id="app">
    <input v-model="chosen" type="color">
    <hr>
    <div class="column" v-bind:key="n" v-for="n in 20">
      <div class="demo" style="background-color: white" @dblclick="makeWhite" @mouseup="divClasses" v-bind:key="n" v-for="n in 20"><span hidden>{{ n }}</span></div>
    </div>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      'chosen': 'black'

    }
  },
  methods: {
    divClasses: function (event) {
      event.target.style.backgroundColor = this.chosen;
    },
    makeWhite: function (event) {
      event.target.style.backgroundColor = 'white';
    }
  },
  watch: {

  },
  computed: {

  }
}
</script>
<style>
  .column{
    float: left;
  }
  .demo {
    width: 15px;
    height: 15px;
    border: .5px solid black;
  }
</style>
