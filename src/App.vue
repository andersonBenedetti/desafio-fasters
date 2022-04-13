<template>
  <div id="app">
    <HeaderComponent />
    <SiteBudget />
    <ScheduleRenee />
    <ClientCompany />
    <SelosComponents />
    <BuyProducts />
    <ShirtStore />
    <TailorShop />
    <CustomerTestimonials />
    <ContactCompany />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "@/components/HeaderComponent";
import SiteBudget from "@/components/SiteBudget.vue";
import ScheduleRenee from "@/components/ScheduleRenee.vue";
import ClientCompany from "@/components/ClientCompany.vue";
import SelosComponents from "@/components/SelosComponents";
import BuyProducts from "@/components/BuyProducts.vue";
import ShirtStore from "@/components/ShirtStore.vue";
import TailorShop from "@/components/TailorShop.vue";
import CustomerTestimonials from "@/components/CustomerTestimonials.vue";
import ContactCompany from "@/components/ContactCompany.vue";
import FooterComponent from "@/components/FooterComponent.vue";

export default {
  components: {
    HeaderComponent,
    SiteBudget,
    ScheduleRenee,
    ClientCompany,
    SelosComponents,
    BuyProducts,
    ShirtStore,
    TailorShop,
    CustomerTestimonials,
    ContactCompany,
    FooterComponent,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}

body,
ul,
h1,
h2,
p {
  padding: 0;
  margin: 0;
}

ul {
  list-style: none;
}

a {
  text-decoration: none;
}

img {
  display: block;
  max-width: 100%;
}

.btn {
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
}

html {
  scroll-behavior: smooth;
}
</style>
