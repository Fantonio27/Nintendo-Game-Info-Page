<template>
  <div class="top-bar row">
    <div class="left-side row">
      <div class="logo-container row">
        <svg
          viewBox="0 0 97 24"
          xmlns="http://www.w3.org/2000/svg"
          width="69"
          role="presentation"
          alt=""
          data-testid="NintendoRacetrackLogoIcon"
          size="69"
          color="white"
        >
          <path
            d="M17.945 14.157l-4.85-7.838H9.609V17.59h3.486V9.752l4.85 7.838h3.456V6.32h-3.486l.03 7.837zm27.554-4.04V8.993H43.68v-1.52h-3.395v1.52h-1.849v1.124h1.85v7.473h3.394v-7.473h1.82zM23.341 17.56h3.364v-7.474h-3.364v7.474zm0-8.932h3.395V6.319H23.34v2.309zm59.17.942c-2.728 0-4.941 1.883-4.941 4.192s2.213 4.193 4.94 4.193c2.729 0 4.942-1.884 4.942-4.193 0-2.309-2.213-4.192-4.941-4.192zm1.364 5.772c0 1.185-.698 1.67-1.364 1.67-.667 0-1.395-.485-1.395-1.67v-3.16c0-1.184.697-1.67 1.395-1.67.666 0 1.364.486 1.364 1.67v3.16zm-10.73-4.891c-.547-.304-1.123-.608-1.91-.669-2.426-.212-4.305 1.945-4.305 3.92 0 2.612 2 3.554 2.304 3.706 1.152.516 2.607.547 3.88-.274v.426h3.334V6.32h-3.334c.03 0 .03 2.4.03 4.13zm.03 3.342v1.336c0 1.155-.789 1.458-1.334 1.458-.546 0-1.334-.303-1.334-1.458v-2.673c0-1.155.788-1.458 1.334-1.458.515 0 1.333.303 1.333 1.458v1.337zM34.616 9.752c-1.122.03-2.031.516-2.698 1.124v-.79h-3.365v7.474h3.365v-4.922c0-.638.697-1.367 1.607-1.367.909 0 1.546.73 1.546 1.367v4.922h3.364v-4.071c0-2.947-2.546-3.798-3.82-3.737zm27.433 0a4.075 4.075 0 0 0-2.698 1.124v-.79h-3.365v7.474h3.365v-4.922c0-.638.697-1.367 1.606-1.367.91 0 1.546.73 1.546 1.367v4.922h3.365v-4.071c0-2.947-2.546-3.798-3.82-3.737zm-7.063 4.101c0-2.309-2.243-4.253-4.971-4.253-2.759 0-4.972 1.884-4.972 4.193 0 2.308 2.213 4.192 4.972 4.192 2.273 0 4.213-1.306 4.789-3.068H51.44v.455c0 1.367-.91 1.671-1.394 1.671-.515 0-1.425-.304-1.425-1.67v-1.55l6.366.03zm-6.123-2.643a1.391 1.391 0 0 1 1.182-.668c.455 0 .91.213 1.182.668.212.365.212.82.212 1.458H48.62c0-.637.03-1.063.243-1.458zm39.921-3.493c0-.365-.272-.547-.818-.547h-.758v1.914h.455v-.79h.242l.364.79h.515l-.424-.851c.273-.091.424-.273.424-.516zm-.879.273h-.242v-.547h.212c.273 0 .424.091.424.274 0 .212-.12.273-.394.273zm.03-1.58c-.94 0-1.727.79-1.727 1.732s.788 1.732 1.728 1.732 1.727-.79 1.727-1.732a1.73 1.73 0 0 0-1.727-1.732zm0 3.13a1.413 1.413 0 0 1-1.394-1.398c0-.76.637-1.398 1.395-1.398.757 0 1.394.638 1.394 1.398 0 .76-.637 1.397-1.394 1.397zM84.148 0H12.64C5.062-.03 0 5.438 0 11.97c0 6.53 5.062 11.939 12.67 11.939h71.508c7.608 0 12.67-5.408 12.67-11.94C96.818 5.44 91.726 0 84.148 0zm-.03 20.993H12.671c-6.033.03-9.7-4.041-9.7-9.023 0-4.983 3.698-8.993 9.7-9.023h71.446c6.002 0 9.7 4.04 9.7 9.023 0 4.982-3.668 9.023-9.7 9.023z"
            fill="currentColor"
          ></path>
        </svg>
      </div>
      <div class="container row">
        <div class="row" v-for="({ icon, label, style}, index) in leftItems" :key="index">
          <Icon :icon="icon" class="icon" :style="{'font-size': style}"/>
          <p>{{ label }}</p>
        </div>
      </div>
    </div>

    <div class="right-side row">
      <div v-for="({icon, image, label}, index) in rightItems" :key="index" class="row">
        <Icon v-if="index != rightItems.length - 1" :icon="icon" class="icon"/>
        <img src="./FlagUsaIconRegionSelect.webp" alt="us-flag" v-else>
        <p v-if="label">{{ label }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      leftItems: [
        {
          icon: "line-md:compass",
          label: "Explore",
        },
        {
          icon: "streamline:shopping-bag-hand-bag-2-solid",
          label: "Shop",
          style: "16px !important"
        },
        {
          icon: "fluent:shield-question-32-filled",
          label: "Support",
        },
      ],
      rightItems: [
        {
          icon: "material-symbols:search-rounded",
          label: "Search",
        },
        {
          icon: "mdi:heart",
          label: "",
        },
        {
          icon: "tdesign:cart-filled",
          label: "",
        },
        {
          icon: "",
          label: "Log in / Sign up",
        },
        {
          image: "./FlagUsaIconRegionSelect.webp",
          label: "",
        },
      ],
    };
  },
};
</script>

<style></style>
