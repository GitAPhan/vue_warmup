<template>
  <div class="menu_card" v-if="price < 100 && price > 1">
    <img :src="image_src" alt="some food" />
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
    <h5>{{ price }}</h5>
  </div>
</template>

<script>
export default {
  name: "menu-item",
  mounted() {
    // alert("the menu item has been injected onto the page");
    document.body.style.backgroundColor = "orange";
  },

  props: {
    image_src: String,
    title: String,
    description: String,
    price: Number,
  },
};
</script>

<style scoped>
.menu_card {
  max-width: 300px;
  border-radius: 25px;
  border: black 1px solid;
  overflow: hidden;
}

.menu_card > img {
  padding: 10px;
  max-width: 90%;
}
</style>