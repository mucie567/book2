<template>
  <div class="feature-item">
    <v-avatar color="blue darken-2" size="72">
      <v-icon dark>
        {{ f_icon }}
      </v-icon>
    </v-avatar>
    <h3>{{ f_title }}</h3>
    <p>
      {{ f_text }}
    </p>
  </div>
</template>

<script>
export default {
  name: "FeatureItem",
  props: ["f_icon", "f_title", "f_text"],
  data() {
    return {};
  }
};
</script>

<style lang="scss" scoped>
.feature-item {
  padding: 20px;
  background-color: white;
  margin: 10px;
}
h3 {
  margin: 15px 0;
  font-size: 20px;
}
</style>