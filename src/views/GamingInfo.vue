<template>
  <div>
    <Product />
    <GameDescription />
    <OtherInformation />
    <GameDetails />
    <Features />
    <MoreLikeThis />
    <Disclaimer />
  </div>
</template>

<script lang="ts">
import Product from "../components/GamingInfoComponents/Product.vue";
import GameDescription from "../components/GamingInfoComponents/GameDescription.vue";
import OtherInformation from "../components/GamingInfoComponents/OtherInformation.vue";
import GameDetails from "../components/GamingInfoComponents/GameDetails.vue";
import Features from "../components/GamingInfoComponents/Features.vue";
import MoreLikeThis from "../components/GamingInfoComponents/MoreLikeThis.vue";
import Disclaimer from "../components/GamingInfoComponents/Disclaimer.vue";

export default {
  components: {
    Disclaimer,
    Features,
    GameDescription,
    GameDetails,
    MoreLikeThis,
    OtherInformation,
    Product,
  },
};
</script>
