<template>
  <section class="lista">
    <div class="logo">
      <img :src="`/img/${image}.png`" alt="Vector" />
    </div>
    <p class="title">{{ title }}</p>
    <p class="text">{{ text }}</p>
  </section>
</template>

<script>
export default {
  name: "ListComponents",
  props: ["image", "title", "text"],
};
</script>

<style scoped>
.lista {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.logo {
  width: 36px;
  height: 36px;
}

.logo img {
  display: block;
  width: 100%;
  height: 100%;
}

.title {
  margin-bottom: 5px;
  margin-top: 14.7px;
  font-family: "Cormorant";
  font-weight: 600;
  font-size: 24px;
  line-height: 29px;
  text-align: center;
  text-transform: uppercase;
  color: #1c86a4;
}

.text {
  font-family: "Lato";
  font-weight: 300;
  font-size: 14px;
  line-height: 17px;
  color: #727272;
}
</style>