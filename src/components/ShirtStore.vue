<template>
  <section id="camisaria" class="camisaria">
    <div class="container">
      <div class="image">
        <img src="/img/101.png" alt="foto" />
      </div>
      <div class="infos">
        <div class="title">
          <h1>Camisaria</h1>
          <span>confeccionadas artesanalmente</span>
        </div>
        <div class="colunas">
          <div class="coluna1">
            <span>100% Algodão</span>
            <span>Monograma</span>
            <span>Slim</span>
          </div>
          <div class="coluna2">
            <span>Nacionais e Importadas </span>
            <span>Tradicionais e Esportivas</span>
            <span>Casamentos</span>
          </div>
        </div>
        <ButtonComponent title="Quero um orçamento" />
      </div>
    </div>
  </section>
</template>

<script>
import ButtonComponent from "@/components/ButtonComponent";
export default {
  name: "ShirtStore",
  components: {
    ButtonComponent,
  },
};
</script>

<style scoped>
.camisaria {
  display: flex;
  justify-content: center;
  margin-top: 100px;
  margin-bottom: 100px;
}

.container {
  width: 1111px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.image {
  max-width: 540px;
  max-height: 488px;
  position: relative;
}

.image::before {
  content: "";
  position: absolute;
  border: 1px solid #1c86a4;
  height: 464px;
  width: 550px;
  top: 10px;
  right: -12px;
}

.image img {
  width: 100%;
  z-index: 2;
}

.infos {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 290px;
  width: 468px;
  position: relative;
}

.infos::before {
  content: "";
  position: absolute;
  border: 1px solid #e5e5e5;
  width: 662px;
  height: 385px;
  top: -40px;
  right: -35px;
  z-index: -1;
}

.title h1 {
  font-family: "Cormorant";
  font-weight: 300;
  font-size: 62px;
  line-height: 75px;
  text-transform: uppercase;
  color: #014561;
}

.title span {
  font-weight: 400;
  font-size: 16px;
  line-height: 19px;
  text-transform: uppercase;
  color: #c4c4c4;
  position: relative;
  margin-left: 20px;
}

.title span::before {
  content: "";
  position: absolute;
  width: 15px;
  height: 1px;
  background-color: #be9667;
  left: -20px;
  top: 10px;
}

.colunas {
  font-family: "Cormorant";
  font-style: italic;
  font-weight: 400;
  font-size: 24px;
  line-height: 29px;
  color: #727272;
  display: flex;
  justify-content: space-between;
}

.colunas span {
  position: relative;
  margin-left: 35px;
}

.colunas span::before {
  content: "";
  position: absolute;
  width: 5px;
  height: 5px;
  border-radius: 50%;
  background-color: #727272;
  left: -20px;
  top: 13px;
}

.coluna1 {
  height: 87px;
  width: 152px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.coluna2 {
  height: 87px;
  width: 248px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.infos button {
  width: 330px;
}

@media screen and (max-width: 1200px) {
  .container {
    flex-direction: column;
    padding: 22px;
    width: 100%;
  }

  .infos::before {
    content: none;
  }

  .infos {
    margin-top: 20px;
    order: 2;
    height: 366px;
    width: 100%;
  }

  .image {
    order: 1;
  }

  .colunas span {
    margin-left: none;
  }

  .colunas {
    flex-direction: column;
  }
  .infos button {
    width: 100%;
  }

  .title h1 {
    font-size: 50px;
  }
}
@media screen and (max-width: 600px) {
  .image {
    height: 294px;
    width: 330px;
  }

  .image::before {
    height: 282px;
    width: 352px;
  }
}
</style>