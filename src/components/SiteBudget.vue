<template>
  <section class="banner">
    <img src="/img/Banner31.png" alt="Banner" />
    <div class="alfaiate-topo">
      <div class="content">
        <div class="descricao">
          <p>Elegante é ter um</p>
          <h1>Alfaiate</h1>
          <p class="chamar">para chamar de seu.</p>
        </div>
        <div>
          <div class="compre">
            <p>
              COMPRE HOJE, <span>PAGUE EM ATÉ 3X COM 12% DE DESCONTO</span> E
              TENHA 10 MESES PARA CONFECCIONAR!
            </p>
          </div>
          <ButtonComponent title="Faça já um Orçamento" link="#" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ButtonComponent from "@/components/ButtonComponent";
export default {
  name: "SiteBudget",
  components: {
    ButtonComponent,
  },
};
</script>

<style scoped>
.banner {
  position: relative;
  width: 100%;
  height: 100%;
}

img {
  width: 100%;
  height: 100%;
}

.alfaiate-topo {
  position: absolute;
  top: 111px;
  width: 100%;
  height: 100%;
  margin-bottom: 114px;
}

.content {
  display: flex;
  height: 630px;
  flex-direction: column;
  justify-content: space-around;
  margin-left: 98px;
}

.descricao {
  width: 404.18px;
  left: 103.98px;
}

.descricao p {
  font-family: "Playfair Display";
  font-style: italic;
  font-weight: 400;
  font-size: 32.5627px;
  line-height: 43px;
  color: #be9667;
}

.descricao h1 {
  color: rgba(2, 75, 104, 0.68);
  font-family: "Playfair Display";
  font-style: normal;
  font-weight: 400;
  font-size: 90.0346px;
  line-height: 120px;
  text-transform: uppercase;
}

.descricao .chamar {
  margin-left: 116px;
}

.compre {
  max-width: 438px;
  max-height: 93px;
  color: #e5e5e5;
  margin-bottom: 25px;
}

.compre p {
  font-family: "Lato";
  font-style: normal;
  font-weight: 300;
  font-size: 24px;
  line-height: 131%;
  text-transform: uppercase;
}

.compre span {
  font-weight: 400;
}

@media screen and (max-width: 1300px) {
  img {
    height: 735px;
  }
}

@media screen and (max-width: 500px) {
  .descricao {
    margin-bottom: 20px;
    width: 100%;
  }

  .descricao p {
    font-size: 26px;
    line-height: 34.6px;
  }

  .descricao h1 {
    font-size: 72px;
    line-height: 95.9px;
  }

  .descricao .chamar {
    margin-left: 90px;
  }

  .compre {
    margin-bottom: 60px;
  }

  .compre p {
    font-size: 22px;
    line-height: 31.24px;
  }

  .content {
    margin-left: 0;
    padding: 22px;
  }
}

@media screen and (max-width: 400px) {
  .content {
    padding: 10px;
  }
  .descricao h1 {
    font-size: 50px;
    line-height: 50px;
  }
  .descricao p {
    font-size: 20px;
  }
  .compre p {
    font-size: 16px;
  }
  .content {
    height: auto;
  }
  img {
    height: 70vh;
  }
}
</style>