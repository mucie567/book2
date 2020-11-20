<template>
    <div class="blog-item">
        <v-img :src="b_img" max-height="350" cover max-width="250" class="item-margin bmg">
        </v-img>
        <h3 class="item-margin">{{ b_title }}</h3>
        <p class="item-margin">
        {{ b_text }}
        </p>
        <v-btn class="item-margin">CONTINUE READING</v-btn>
    </div>
</template>

<script>
    export default {
        name:'BlogItem',
        props: ["b_img", "b_title", "b_text"],
        data() {
            return{};
        }
    }
</script>

<style lang="scss" scoped>
.blog-item {
    padding: 20px;
    background-color: white;
    margin: 10px;
}
h3 {
    margin: 15px 0;
    font-size: 20px;
}
.item-margin{
    margin-bottom: 20px;
}
.bmg{
    margin: 0 auto;
}
</style>