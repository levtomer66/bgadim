<template>
  <div class="card" v-on:click="card_click" v-bind:class="{card_selected: isCardSelected}" >
    <img v-bind:src="image_src" alt="Avatar" style="width:100%">
      <div class="text">
        <h4 class="centered">{{ text }}</h4>
      </div>
  </div>
</template>


<style>

.card {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 30%;
  border-radius: 5px;
  margin-left: 20px;
}

.card_selected {
  outline-style: auto;
  outline-color: steelblue;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
  /* width: 33%; */
}

img {
  border-radius: 5px 5px 0 0;
  height: 350px;
}

.centered {
  position: absolute;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -50%);
}

h4.centered {
  font-size: 5.5rem;
  color: white;
  opacity: 0.75;
  font-weight: 200;
}

.card:hover h4 {
  font-size: 5.5rem;
  color: white;
  opacity: 0.85;
  font-weight: 400;
  -webkit-transition: all 0.2s ease;
  -moz-transition: all 0.2s ease;
  -o-transition: all 0.2s ease;
  -ms-transition: all 0.2s ease;
}
.text {
  padding: 2px 16px;
}

.card_selected .text {
  padding: 2px 16px;
  background-color: steelblue;
}
</style>

<script>
export default {
  data() {
    return {
      isCardSelected: false,
      greeting: '',
    }
  },
  props: [ 'text', 'image_src' ],
  methods: {
    card_click: function() {
      this.isCardSelected = !this.isCardSelected;
      // some code to filter users
    }

  }
}
</script>
