<template>
  <v-row class="about-me" justify="center" no-gutters>
    <v-col cols="12" sm="8" md="6" class="wrapper">
      <h2>ABOUT ME</h2>
      <div class="divider"></div>
      <p>
        Vuetify is the #1 component library for Vue.js and has been in active
        development since 2016. The goal of the project is to provide users with
        everything that is needed to build rich and engaging web applications
        using the Material Design specification. It accomplishes that with a
        consistent update cycle, Long-term Support (LTS) for previous versions,
        responsive community engagement, a vast ecosystem of resources and a
        dedication to quality components.
      </p>
      <v-card
        elevation="13"
        rounded="circle"
        width="100"
        style="display: inline-block"
      >
        <v-avatar size="100"><v-img :src="myProfile"></v-img></v-avatar>
      </v-card>
      <div>
        <v-btn outlined class="btn-margin">vutify documentation</v-btn>
      </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "AboutMe",
  data() {
    return {
      myProfile:
        "https://6.vikiplatform.com/image/a11230e2d98d4a73825a4c10c8c6feb0.jpg?x=b&a=0x0&s=590x330&q=h&e=t&f=t&cb=1"
    };
  },
  methods: {
    clickBtn() {
      location.href = "https://vuetifyjs.com/en/";
    }
  }
};
</script>

<style lang="scss" scoped>
.about-me {
  padding: 40px;
}
.wrapper {
  text-align: center;
}
.btn-margin {
  margin: 20px 0;
}
</style>