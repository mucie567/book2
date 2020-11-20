<template>
  <div class="feature">
    <h2>VUETIFY FEATURES</h2>
    <div class="divider"></div>
    <v-row class="wrapper" no-gutters justify="center">
      <v-col cols="12" md="3" v-for="(feature, i) in features" :key="i">
        <feature-item
          :f_icon="feature.icon"
          :f_title="feature.title"
          :f_text="feature.text"
        ></feature-item>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Feature",
  components: {
    FeatureItem: () => import("@/components/main/FeatureItem.vue")
  },
  data() {
    return {
      features: [
        {
          icon: "mdi-account-group-outline",
          title: "VIBRANT COMMUNITY",
          text:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto cupiditate sint possimus quidem atque harum excepturi nemo velit tempora! Enim inventore fuga, qui ipsum eveniet facilis obcaecati corrupti asperiores nam"
        },
        {
          icon: "mdi-alarm",
          title: "FREQUENT UPDATES",
          text:
            "Sed ut elementum justo. Suspendisse non justo enim. Vestibulum cursus mauris dui, a luctus ex blandit. Lorem ipsum dolor sit amet consectetur adipisicing elit. qui ipsum eveniet facilis obcaecati corrupti consectetur adipisicing elit."
        },
        {
          icon: "mdi-glass-pint-outline",
          title: "LONG-TERM SUPPORT",
          text:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto cupiditate sint possimus quidem atque harum excepturi nemo velit tempora! Enim inventore fuga, qui ipsum eveniet facilis obcaecati corrupti asperiores nam"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.feature {
  text-align: center;
  background-color: #eee;
  padding: 30px;
}
</style>