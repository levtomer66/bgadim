<template>
  <section class="container mt-5">
  <Card text="Elegant" image_src="https://carlgross.com/wp-content/uploads/2018/05/Business-Attire-600x600.jpg" />
  <Card text="Causal" image_src="https://i.pinimg.com/originals/32/d1/2e/32d12ecc86a0e26a64901bad3db3d2fc.jpg" />
  <Card text="Outfit" image_src="https://i.pinimg.com/originals/cb/7c/e8/cb7ce8f9856a2b1026cbd3b9ae158d29.jpg" />
  <img class="sub-button" src="https://www.pngkit.com/png/full/1-17622_white-subscribe-button-transparent.png" alt="" v-on:click="subscribe" />
  </section>
</template>

<style scoped>
 .mt-5 {
    margin-left: 15%;
  }
  .sub-button {
    position: absolute;
  top: 70%;
  left: 50%;
  margin: -25px 0 0 -25px;
    width: 190px;
    height: 100px;
    cursor: pointer;
  }

</style>

<script>
export default {
  data() {
    return {
    }
  },
  methods: {
    subscribe: function() {
      console.log("I did it!")
      // some code to filter users
    }

  }
}
</script>
