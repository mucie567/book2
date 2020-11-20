<template>
    <div>
        <v-card
      class="d-flex align-content-space-between justify-center flex-wrap"
      color="grey lighten-2"
      flat
      tile
    >
      <v-card
        v-for="n in 20"
        :key="n"
        class="pa-2"
        outlined
        tile
      >
      </v-card>
    </v-card>
    </div>
</template>

<script>
    export default {
        name:'GalleryItem'
    }
</script>

<style lang="scss" scoped>

</style>