<template>
    <div>
        <h1>gallery</h1>
        <v-row no-gutters>
            <v-col cols="6" sm="4" lg="3"  v-for="(image, i) in images" :key="i">
                <div>
                    <image-card :image="image"></image-card>
                </div>
            </v-col>
        </v-row>
        <gallery-item></gallery-item>
    </div>
</template>

<script>
import axios from 'axios'
    export default {
        name:'Gallery',
        components: {
        GalleryItem: () => import("@/components/main/GalleryItem.vue"),
        ImageCard:() => import("@/components/gallery/ImageCard.vue")
        },
        data(){
            return{
                images:[]
            }
        },
        mounted(){
            axios.get('https://picsum.photos/v2/list')
            .then((res) => {
                console.log(res.data);
                this.images = res.data.map(el=>{
                    let tmUrl = el.download_url.split('/');
                    tmUrl.splice(-2,2,'300/200.webp');
                    el.download_url = tmUrl.join("/");
                    return el;
                });
                console.log(this.images);
            });
        }
    }
</script>

<style lang="scss" scoped>

</style>