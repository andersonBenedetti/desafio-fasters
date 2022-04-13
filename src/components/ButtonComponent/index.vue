<template>
    <div>
      <a :href="link" class="button" target="_self" :style="{backgroundColor: bgColor, color: color}">{{title}}</a>
    </div>
</template>

<script>
export default {
  name: "ButtonComponent",
  props: ["title", "bgColor", "color", "link"]
};
</script>

<style scoped>
.button {
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: Lato;
  font-size: 18px;
  font-weight: 300;
  line-height: 22px;
  letter-spacing: 0em;
  height: 50px;
  width: 297px;
  left: 0px;
  top: 0px;
  border-radius: 2px;
  background: #014561;
  color: #e5e5e5;
  cursor: pointer;
  border: none;
  text-decoration: none;
  transition: all 0.2s ease 0s;
}
.button:hover {
  transform: scale(1.1);
}
</style>