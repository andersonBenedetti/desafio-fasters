<template>
  <section class="selos">
    <ListComponents
      image="Vector"
      title="Qualidade"
      text="Camisaria e Alfaiataria 100% artesanal."
    />
    <ListComponents
      class="confianca"
      image="Vector1"
      title="Confiança"
      text="Atendimento personalizado no escritório ou residência."
    />
    <ListComponents
      image="Vector2"
      title="Experiência"
      text="Tradição e modernidade proporcionando elegância."
    />
  </section>
</template>

<script>
import ListComponents from "./ListComponents";
export default {
  name: "SelosComponents",
  components: {
    ListComponents,
  },
};
</script>

<style scoped>
.selos {
  display: flex;
  justify-content: space-around;
  margin-top: 52.29px;
  margin-bottom: 50px;
}

.confianca {
  position: relative;
}

.confianca::after {
  content: "";
  position: absolute;
  width: 1px;
  height: 57px;
  background-color: #cccccc;
  bottom: 1px;
  left: 420px;
}
.confianca::before {
  content: "";
  position: absolute;
  width: 0.5px;
  height: 57px;
  background-color: #cccccc;
  bottom: 1px;
  right: 420px;
}
@media screen and (max-width: 1200px) {
  .confianca::after {
    content: none;
  }

  .confianca::before {
    content: none;
  }

  .selos {
    margin-top: 100px;
  }
}
@media screen and (max-width: 1200px) {
  .selos {
    display: none;
  }
}
</style>