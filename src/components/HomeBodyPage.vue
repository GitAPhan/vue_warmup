<template>
  <div>
    <h1 @click="make_red">welcome to the page!!</h1>
    <div id="menu_cards">
      <menu-item
        v-for="item in items" :key="item['title']"
        :price="item['price']"
        :title="item['title']"
        :description="item['desc']"
        :image_src="item['image_src']"
      ></menu-item>
    </div>
    <page-footer
      logo="http://placeskull.com/100/100"
      logo_alt="random skull logo"
    ></page-footer>
  </div>
</template>

<script>
import MenuItem from "./MenuItem.vue";
import PageFooter from "./PageFooter.vue";
export default {
  name: "home-page-body",
  components: {
    MenuItem,
    PageFooter,
  },
  methods: {
    make_red() {
      document.body.style.backgroundColor = "red";
    },
  },
  data() {
    return {
      page_title: "Welcome to the page with many items!",
      items: [
        {
          image_src: "http://unsplash.it/300/150?random&gravity=center",
          title: "Item Title",
          desc: "this is a description",
          price: 10.5,
        },
        {
          image_src: "http://unsplash.it/301/150?random&gravity=center",
          title: "Item Title Two",
          desc: "this is a description",
          price: 13.5,
        },
        {
          image_src: "http://unsplash.it/300/151?random&gravity=center",
          title: "Item Title Three",
          desc: "this is a description",
          price: 15.5,
        },
        {
          image_src: "http://unsplash.it/301/151?random&gravity=center",
          title: "Item Title Four",
          desc: "this is a description",
          price: 17.5,
        },
      ],
    };
  },
};
</script>

<style scoped>
#menu_cards {
  display: grid;
  place-items: center;
  grid-auto-flow: column;
  column-gap: 10px;
  margin: 20px 0px;
}
</style>