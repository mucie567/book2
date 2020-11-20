<template>
  <div class="parallax">
    <v-parallax
      dark
      src="https://i.pinimg.com/originals/71/b8/b2/71b8b2fdf55d19540432f86f53f90e67.png"
      height="300"
    >
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="2" v-for="(spec, i) in specs" :key="i">
          <h1 class="display-1 font-weight-thin mb-4">
            {{ spec.value }}
          </h1>
          <h4 class="subheading">
            {{ spec.key }}
          </h4>
        </v-col>
      </v-row>
    </v-parallax>
  </div>
</template>

<script>
export default {
  name: "Parallax",
  data() {
    return {
      specs: [
        {
          key: "GITHUB STARS",
          value: "24k"
        },
        {
          key: "RELEASES",
          value: "330+"
        },
        {
          key: "DOWNLOADS/MO",
          value: "1m"
        },
        {
          key: "TOTAL DOWNLOADS",
          value: "5m"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
</style>