<template>
  <div>
    <Navbar />
    <GamingInfo />
    <Footer />
  </div>
</template>

<script>
import Footer from "./components/common/Footer.vue";
import Navbar from "./components/common/Navbar.vue";
import Sidebar from "./components/common/Sidebar.vue";
import GamingInfo from "./views/GamingInfo.vue";

export default {
  components: { Navbar, Sidebar, Footer, GamingInfo},
};
</script>

<style></style>
