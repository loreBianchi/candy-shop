<template>
  <div class="textlockup">
    <div class="grid-container">
      <div class="main-offer"></div>
      <div class="second-offer"></div>
      <div class="third-offer"></div>
      <div class="fouth-offer"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/variables";

.textlockup {
  height: 80vh;
  width: 100%;
}
.grid-container {
  height: 100%;
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
  grid-template-rows: 1fr 0.9fr 1.1fr;
  gap: 1px 1px;
  grid-template-areas: "main-offer main-offer main-offer main-offer second-offer second-offer" "main-offer main-offer main-offer main-offer third-offer third-offer" "fouth-offer fouth-offer fouth-offer fouth-offer fouth-offer fouth-offer";
}

.main-offer { 
  grid-area: main-offer;
  background: lightgrey;
}

.second-offer { 
  grid-area: second-offer;
  background: lightgoldenrodyellow;
}

.third-offer { grid-area: third-offer; }

.fouth-offer { grid-area: fouth-offer; }

/* For presentation only, no need to copy the code below */
.grid-container * { 
  border: 1px solid $brand-primary;
  position: relative;
  padding: 16px;
}

.grid-container *:after { 
  content:attr(class);
  position: absolute;
  top: 0;
  left: 0;
}
</style>
