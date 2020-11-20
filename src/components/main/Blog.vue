<template>
    <div class="blog">
        <h2>BLOG</h2>
        <div class="divider"></div>
        <v-row class="wrapper" no-gutters justify="center">
            <v-col cols="12" md="4" v-for="(blog, i) in blogs" :key="i" :img="blog.img" :title="blog.title" :text="blog.text">
                <blog-item
                :b_img="blog.img"
                :b_title="blog.title"
                :b_text="blog.text"
                >
                </blog-item>
            </v-col>
        </v-row>
    </div>
</template>

<script>
    export default {
        name:'Blog',
        components: { BlogItem:() => import("@/components/main/BlogItem.vue")
        },
        data(){
            return{
                blogs: [
            {
            img: "https://img.ridicdn.net/cover/509000269/xxlarge",
            title: "잃어버린 세계를 찾아서",
            text:
                "현대 문학사에서 빼놓을 수 없는 위대한 작품으로 평가받는 이 소설은 기억과 추억, 잃어버린 시간을 찾아 떠나는 여행을 그리고 있다. ‘나’라는 화자의 성장과 시선을 통해 인간 의식의 흐름 자체를 따라가며 한 인간이 품을 수 있는 다양한 사유를 펼쳐 보인다."
            },
            {
            img: "https://image.yes24.com/Goods/7039855/L",
            title: "불온한 산책자",
            text:
                "나는 사상가들이 비범한 지성과 집중력, 카리스마를 지녔으며 때로는 엉뚱하기도 하다는 사실을 금방 알게 됐다. 또한 사상가들은 자기 사상을 더 넓은 세상에 전하는 일에 전념하고 있으며 종종 우리 문화에 만연한 반지성주의에 맞서 싸우기도 한다. (…) 이들은 학문과 지식의 민주성을 지키는 투사인 셈이다."
            },
            {
            img: "https://image.yes24.com/Goods/3358759/L",
            title: "first as tragedy, then as farce",
            text:
                "Billions of dollars have been hastily poured into the global banking system in a frantic attempt at financial stabilization. So why has it not been possible to bring the same forces to bear in addressing world poverty and environmental crisis?"
            }
        ]
            };
        }
    }
</script>

<style lang="scss" scoped>
.blog{
    h2{
        text-align: center; 
    }
    text-align: start;
    padding: 30px;
}
</style>