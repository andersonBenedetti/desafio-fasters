<template>
  <section id="contato" class="contato">
    <h1>Contato</h1>
    <div class="area-contato">
      <div class="info">
        <div class="fone">
          <p>Telefones</p>
          <span>+55 (11) 3088-0757</span>
          <p class="email">E-mail</p>
          <span>renee@reneetrajar.com.br</span>
        </div>
        <div>
          <p>Atendimento Personalizado</p>
          <button class="btn btn-info">Clique aqui!</button>
        </div>
      </div>
      <div class="area-msg">
        <input type="text" placeholder="Nome" />
        <input type="text" placeholder="E-mail" />
        <input class="msg" type="text" placeholder="Mensagem" />
        <button class="btn btn-msg">Enviar Mensagem</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContactCompany",
};
</script>

<style scoped>
.contato {
  max-width: 978px;
  margin: 50px auto 84px auto;
}

.contato h1 {
  display: flex;
  justify-content: center;
  font-family: "Cormorant";
  font-size: 38px;
  font-weight: 300;
  line-height: 46px;
  color: #1c86a4;
  position: relative;
}

.contato h1::after {
  content: "";
  position: absolute;
  width: 53px;
  height: 1px;
  background-color: #70b0c4;
  top: 50px;
}

.area-contato {
  display: flex;
  justify-content: space-between;
  margin-top: 40px;
}

.info {
  width: 280px;
  height: 273px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.info p {
  font-family: "Lato";
  font-weight: 300;
  font-size: 18px;
  line-height: 22px;
  text-transform: uppercase;
  color: #1c86a4;
  margin-bottom: 8px;
}

.info span {
  font-family: "Lato";
  font-weight: 300;
  font-size: 16px;
  line-height: 150.1%;
  color: #828282;
}

.email {
  margin-top: 17px;
}

.btn-info {
  width: 270px;
  background-color: transparent;
  font-family: "Lato";
  font-weight: 300;
  font-size: 18px;
  line-height: 22px;
  color: #014561;
  border: 1px solid #1c86a4;
  margin-top: 14px;
}

.area-msg {
  width: 600px;
  height: 273px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.area-msg input {
  width: 100%;
  height: 42px;
  border: 1px solid #1c86a4;
  border-radius: 3px;
}

.area-msg input::placeholder {
  color: #c4c4c4;
  padding-left: 14px;
}

.area-msg .msg {
  height: 77px;
}

.btn-msg {
  width: 100%;
}

@media screen and (max-width: 1200px) {
  .area-contato {
    flex-direction: column;
    padding: 22px;
  }

  .info {
    order: 2;
    margin: 0 auto;
    text-align: center;
    width: 100%;
  }

  .area-msg {
    order: 1;
    margin: 0 auto 44px auto;
  }

  .btn-info {
    margin: 0 auto;
  }
}

@media screen and (max-width: 700px) {
  .area-msg {
    width: 100%;
  }
}
</style>