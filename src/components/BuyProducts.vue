<template>
  <section class="products">
    <div class="container">
      <div class="infos">
        <div class="title">
          <h1>Condição Imperdível</h1>
        </div>
        <div class="compre">
          <h2>Compre hoje e garanta:</h2>
          <p>12% de desconto e pagamento em até <span>3x sem juros;</span></p>
          <p>
            Até <span>10 meses</span> para confeccionar sua roupa. Não se
            preocupe se suas medidas aumentaram ou diminuíram, estará sempre
            elegante;
          </p>
          <p>Condição muito especial por <span>tempo limitado;</span></p>
          <p>
            Poder presentear alguém com uma roupa de alta costura,
            <span>exclusiva.</span>
          </p>
        </div>
        <div>
          <ButtonComponent
            title="Garanta essa condição especial!"
            bgColor="#be9667"
          />
        </div>
      </div>
      <div class="img-product">
        <img src="/img/anzug.png" alt="produto" />
      </div>
    </div>
  </section>
</template>

<script>
import ButtonComponent from "@/components/ButtonComponent";
export default {
  name: "BuyProducts",
  components: {
    ButtonComponent,
  },
};
</script>

<style scoped>
.products {
  display: flex;
  justify-content: center;
  background-color: #042e40;
  width: 100%;
}

.banner {
  width: 100%;
}

.container {
  max-width: 1032px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.infos {
  max-width: 650px;
  height: 474px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.title h1 {
  font-family: "Cormorant";
  font-weight: 400;
  font-size: 53px;
  line-height: 64px;
  text-transform: uppercase;
  color: #be9667;
}

.compre h2 {
  font-family: "Cormorant";
  font-style: italic;
  font-weight: 400;
  font-size: 30px;
  line-height: 36px;
  color: #be9667;
}

.compre p {
  font-size: 22px;
  line-height: 26px;
  color: #c4c4c4;
  margin-left: 20px;
  margin-top: 23px;
  position: relative;
}

.compre p::before {
  content: "";
  position: absolute;
  width: 15px;
  height: 1px;
  background-color: #be9667;
  left: -20px;
  top: 12px;
}

.compre span {
  font-weight: 400;
}

.btn-compre {
  height: 55px;
  width: 330px;
  border-radius: 2px;
  background-color: #be9667;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  color: #e0e0e0;
  border: none;
}

.img-product {
  max-width: 330px;
  max-height: 517px;
}

.img-product img {
  width: 100%;
  height: 100%;
}

@media screen and (max-width: 900px) {
  .img-product {
    display: none;
  }

  .products {
    height: 780px;
  }

  .container {
    padding-left: 23px;
    padding-right: 23px;
    align-items: center;
  }
  .btn-compre {
    margin: 0 auto;
    margin-top: 10px;
  }
}
</style>