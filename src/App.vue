<template>
  <v-app>
    <router-view></router-view>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    //
  })
};
</script>
<style lang="scss">
h2 {
  font-size: 48px;
  font-weight: 700;
}
p {
  font-size: 20px;
  font-weight: 300;
}
.divider {
  width: 56px;
  margin: 0 auto 32px;
  border-top: 1px solid grey;
  border-bottom: 1px solid grey;
  height: 5px;
  opacity: 0.3;
}
</style>
