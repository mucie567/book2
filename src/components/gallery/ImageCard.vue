<template>
    <div class="image-card" @mouseover="mouseOver" @mouseleave="mouseLeave">
        <transition name="fade">
            <v-row class="cover text-center" v-show="isOver" no-gutters justify="center" align="center">
                <div>
                    <v-btn icon dark>
                        <v-icon>mdi-link</v-icon>
                    </v-btn>
                    <h4>{{image.author}}</h4>
                </div>
            </v-row>
        </transition>
        <v-img :src="image.download_url" :alt="image.author">
        </v-img>
        <!-- <v-hover v-slot:default="{ hover }" open-delay="200">
            <v-card :elevation="hover ? 16 : 2" class="mx-auto" :class="{ 'on-hover': hover }">
                <v-img :src="image.download_url">
                    <v-expand-transition>
            <div
                v-if="hover"
                class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-3 white--text"
                style="height: 100%;"
            >
            </div>
        </v-expand-transition>
                </v-img>
                <v-fade-transition>
          <v-overlay
            v-if="hover"
            absolute
            :opacity=".9"
            :value="overlay"
          >
          </v-overlay>
        </v-fade-transition>
            </v-card>
        </v-hover> -->
    </div>
</template>

<script>
    export default {
        name:'ImageCard',
        props:['image'],
        data(){
            return{
                isOver:false
            };
        },
        methods:{
            mouseOver(){
                console.log("over");
                this.isOver=true

            },
            mouseLeave(){
                console.log("leave");
                this.isOver=false
            }
        }
    }
</script>

<style lang="scss" scoped>
    // .v-card{
    //     .on-hover{
    //         .theme--dark{
    //             background-color: rgba(#FFF, 0.8)
    //         }
    //     }
    // }
    .image-card{
        position: relative;
    }
    .cover{
        position: absolute;
        background-color: #e49750;
        width: 100%;
        height: 100%;
        opacity: 0.5;
        z-index: 1;
        p{
            text-align: center;
            line-height: 200px;
            font-weight: bold;
            z-index: 2;
        }
    }
    .fade-enter-active,.fade-leave-active{
        transition: opacity .5s;
    }
    .fade-enter,.fade-leave-to{
        opacity: 0;
    }
</style>