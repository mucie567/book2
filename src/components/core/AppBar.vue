<template>
  <v-app-bar color="white">
    <v-avatar size="35">
      <v-img :src="require('../../assets/logo.svg')" alt="logo" contain />
    </v-avatar>
    <h1>NIGHT SLEEP</h1>
    <router-link to="/" class="menu">HOME</router-link>
    <router-link to="/gallery" class="menu">GALLERY</router-link>
  </v-app-bar>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
h1 {
  font-size: 1.5rem;
  margin-left: 15px;
}
.menu{
  margin-left: 30px;
  text-decoration: none;
  color: #000;
  font-weight: bold;
  font-size: 20px;
}
</style>