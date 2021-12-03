<template>
  <div @click="make_purple" id="page_footer">
    <img :src="logo" :alt="logo_alt" />
    <img :src="logo" :alt="logo_alt" />
    <img :src="logo" :alt="logo_alt" />
    <img :src="logo" :alt="logo_alt" />
    <img :src="logo" :alt="logo_alt" />
    <img :src="logo" :alt="logo_alt" />
    <img :src="logo" :alt="logo_alt" />
  </div>
</template>

<script>
export default {
  name: "page-footer",
  props: {
    logo: String,
    logo_alt: String,
  },
  methods: {
    make_purple() {
      document.body.style.backgroundColor = "purple";
    },
  },
};
</script>

<style scoped>
#page_footer {
  width: 100%;
  background-color: black;
}
</style>