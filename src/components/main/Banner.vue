<template>
  <div class="banner">
    <v-img :src="imgSrc" min-height="300"></v-img>
    <div class="main-copy">
      <p class="copy">WELCOM TO</p>
      <p class="copy big-font">NIGHT SLEEP</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Banner",
  data() {
    return {
      imgSrc:
        "https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/macbook-accessories-1585767118.jpg"
    };
  }
};
</script>

<style lang="scss" scoped>
.banner {
  display: flex;
  flex-flow: row;
  justify-content: center;
  align-items: center;
}

.main-copy {
  position: absolute;

  p {
    font-size: 50px;
    color: white;
    margin: 0;
    text-align: center;
    font-weight: 300;
  }
  .big-font {
    font-weight: 700;
    font-size: 90px;
  }
}

@media only screen and(max-width: 768px) {
  .main-copy {
    p {
      font-size: 30px;
    }
    .big-font {
      font-size: 60px;
    }
  }
}
</style>