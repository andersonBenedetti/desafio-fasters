<template>
  <footer>
    <div class="footer-container">
      <div>
        <div class="logo-footer">
          <img src="/img/logoFooter.png" alt="logo" />
        </div>
        <p class="cnpj">CNPJ:04.487.685/0001-01</p>
      </div>
      <div class="copyright">
        <span
          >Copyright: 2021 © Renee Trajar - Todos os direitos reservados.</span
        >
      </div>
    </div>
    <div class="seta" @click="scrollTop">
      <img src="/img/Vector3.png" alt="seta" />
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  methods: {
    scrollTop: function() {
      window.scrollTo(0, 0);
    },
  },
};
</script>

<style scoped>
footer {
  border-top: 1px solid #be9667;
  padding-top: 30px;
  padding-bottom: 38px;
  position: relative;
}

.footer-container {
  max-width: 978px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo-footer {
  height: 68.45px;
  width: 138.6px;
}

.logo-footer img {
  width: 100%;
}

.cnpj {
  color: #bdbdbd;
  font-family: "Poppins";
  font-weight: 300;
  font-size: 14px;
  line-height: 21px;
  margin-top: 16.56px;
}

.copyright {
  height: 106px;
  width: 426px;
  position: relative;
}

.copyright span {
  font-family: "Poppins";
  font-weight: 300;
  font-size: 14px;
  line-height: 21px;
  text-align: center;
  color: #4f4f4f;
  position: absolute;
  bottom: 1px;
}

.seta {
  width: 40px;
  height: 40px;
  box-shadow: 0 2.5px 6px #bdbdbd;
  border-radius: 4px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  right: 49px;
  bottom: 82px;
  cursor: pointer;
}

.seta img {
  height: 8px;
  width: 14px;
}

@media screen and (max-width: 900px) {
  .footer-container {
    flex-direction: column;
  }
  .copyright {
    height: 46px;
    width: 215px;
    margin-top: 25px;
  }
}
</style>