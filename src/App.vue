<template>
  <div id="app">
    <v-container>
      <v-row>
        <v-col> <canvas class="pixi" /> </v-col>
        <v-col> 333</v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  mounted() {
    var scriptBody = document.getElementById("app");

    const cdnPixi = document.createElement("script");
    cdnPixi.setAttribute(
      "src",
      "https://cdnjs.cloudflare.com/ajax/libs/pixi.js/5.2.0/pixi.min.js"
    );
    cdnPixi.async = true;
    scriptBody.insertAdjacentElement("afterend", cdnPixi);

    const cdnGsap = document.createElement("script");
    cdnGsap.setAttribute(
      "src",
      "https://cdnjs.cloudflare.com/ajax/libs/gsap/3.0.5/gsap.min.js"
    );
    cdnGsap.async = true;
    scriptBody.insertAdjacentElement("afterend", cdnGsap);

    const cdnPixiFilters = document.createElement("script");
    cdnPixiFilters.setAttribute(
      "src",
      "https://cdn.jsdelivr.net/npm/pixi-filters@3.0.3/dist/pixi-filters.js"
    );
    cdnPixiFilters.async = true;
    scriptBody.insertAdjacentElement("afterend", cdnPixiFilters);

    const glitch = document.createElement("script");
    glitch.setAttribute("src", "glitch.js");
    glitch.async = true;
    scriptBody.insertAdjacentElement("afterend", glitch);
  },
  name: "App",
  /*
  components: {
    HelloWorld
  },
*/
  data: () => ({
    //
  }),
};
</script>

<style lang="scss">
body {
  background-color: black;
}
#app {
  margin-top: 10%;
}
.pixi {
  width: 100%;
}
</style>
