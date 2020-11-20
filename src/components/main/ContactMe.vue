<template>
    <div class="contact-me">
        <h2>CONTACT ME</h2>
        <div class="divider"></div>
        <v-form class="contact-form">
            <v-text-field solo v-model="name" placeholder="name*"></v-text-field>
            <v-text-field solo v-model="email" placeholder="email*"></v-text-field>
            <v-text-field solo v-model="subject" placeholder="subject*"></v-text-field>
            <v-textarea solo v-model="message" placeholder="message*"></v-textarea>
            <v-btn color="blue" dark @click="requestSendEmail">submit</v-btn>
        </v-form>
    </div>
</template>

<script>
    import axios from "axios";
    import sg from "@/config/sendGrid.json";
    export default {
        name:'ContactMe',
        data(){
            return{
                name:'',
                email:'',
                subject:'',
                message:''
            };
        },
        mounted () {
            axios.get('https://picsum.photos/v2/list?page=2&limit=50')
            .then(function (data) {
                console.log(data);
            });
            // axios.get('https://picsum.photos/v2/list?page=2&limit=50')
            // .then(function (data) {
            //     console.log(data);
            // });
            // let _promise = function() {
            //     return new Promise (function(resolve){
            //         window.setTimeout(function() {
            //             resolve("해결완료");
            //         },3000);
            //     });
            // };
            // console.log('promise 비동기함수 실행 시작')
            // _promise().then(function(data) {
            //     console.log("첫번째 성공",data);
            //     return _promise()
            // }).then(function (data) {
            //     console.log("두번째 성공",data)
            // });
        //     console.log('promise 비동기함수 실행 시작')
        //     let postRequest = function(param) {
        //         return new Promise(function(resolve,reject) {
        //             window.setTimeout(function() {
        //                 if (param) {
        //                     resolve("해결완료");
        //                 } else {
        //                     reject('실패!!')
        //                 }
        //             },3000);
        //         });
        //     };

        //     postRequest(false).then(
        //         function(data) {
        //             console.log("첫번째 요청 성공",data);
        //             return postRequest(false)
        //         },
        //         function(error) {
        //             console.log("첫번째 요청 실패!! error:",error);
        //         }
        //     ).then(function (data) {
        //             console.log("두번째 성공",data);
        //     });
        },
        methods:{
            promiseSample(){

            },
            requestSendEmail(){
                let body = {
                    "personalizations": [
                        {
                            "to": [
                                {
                                    "email": "mucie567@naver.com"
                                }
                            ],
                            "subject": this.subject
                        }
                    ],
                    "from": {
                        "email": this.email
                    },
                    "content": [
                        {
                            "type": "text/plain",
                            "value": this.message
                        }
                    ]
                };
                let config = {
                    headers: {
                        'content-type': 'application/json',
                        'x-rapidapi-key': sg.key,
                        'x-rapidapi-host': 'rapidprod-sendgrid-v1.p.rapidapi.com'
                }
                }; 
                axios.post('https://rapidapi.p.rapidapi.com/mail/send',body, config).then(res => {
                    console.log(res)
                }).catch (err =>{
                    console.log("전송 실패:",err);
                });
            }
        }
    }
</script>

<style lang="scss" scoped>
    .contact-me{
        text-align: center;
        background-color: #333;
        padding: 30px;
        h2{
            color: #fff;
        }
        .contact-form{
            width: 100%;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }
    }
</style>