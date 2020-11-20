<template>
    <v-row class="information" justify="center" no-gutters>
        <v-col cols="12" sm="8" md="6" lg="4" class="wrapper">
            <h2 class="me">ABOUT ME</h2>
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
            <v-card elevation="24" rounded="circle" width="70" style="display: inline-block">
                <v-avatar size="70">
                    <v-img :src="imgSrc"></v-img>
                </v-avatar>
                <!-- 그림자 기능 cards -->
            </v-card>
            <div>
                <v-btn outlined>vuetify</v-btn>
            </div>
        </v-col>
    </v-row>
</template>

<script>
    export default {
        name:'Information',
        data () {
            return{
                imgSrc:"data:image/jpeg;base64,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"
            };
        }
    }
</script>

<style lang="scss" scoped>
.wrapper{
    text-align: center;
}
</style>