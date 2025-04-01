<template>
  <div class="navbar">
    <TopNavbar />
    <BottomNavbar />
  </div>
</template>

<script lang="ts">
import TopNavbar from "./NavbarComponents/TopBar.vue";
import BottomNavbar from "./NavbarComponents/BottomBar.vue";

export default {
    components: {
        TopNavbar,
        BottomNavbar
    }
}
</script>

<style>

</style>