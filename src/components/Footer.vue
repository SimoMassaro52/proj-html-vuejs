<template>
    <footer class="d-flex flex-column">
        <div id="sub-footer" class="d-flex flex-row justify-content-around py-5">
            <div id="address" class="d-flex flex-column py-5">
                <span class="title">Address</span>
                <span>382 NE 191st St # 87394 Miami, FL 33179-3899</span>
                <span>+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)</span>
                <a href="#">support@maxcoach.com</a>
                <div  id="social" class="d-flex flex-row">
                    <a class="d-flex align-items-center px-3 py-2" href="#" v-for="(social, indexS) in socials" :key="indexS">
                        <i :class="`fa-brands ${social.icon}`"></i>
                    </a>
                </div>
            </div>
 
            <div id="explore" class="d-flex flex-column py-5">
                <span class="title">Explore</span>
                <a href="#" v-for="(linkL, indexL) in exploreLinks" :key="indexL" class="py-2">
                    {{linkL.text}}
                </a>
            </div>

            <div id="info" class="d-flex flex-column py-5">
                <span class="title">Information</span>
                <a href="#" v-for="(linkI, indexI) in infoLinks" :key="indexI" class="py-2">
                    {{linkI.text}}
                </a>
            </div>

            <div id="insta" class="py-5">
                <div class="d-flex flex-row">
                    <span class="title">Instagram</span> <a href="#" class="d-flex align-items-center px-1">@maxcoach</a>
                </div>
                <div id="pics" class="d-flex flex-row justify-content-around py-3">
                    <img v-for="(pic, indexP) in instaArr" :key="indexP" :src="require(`@/assets/img/${pic.img}.jpg`)" alt="">
                </div>
            </div>
        </div>
        <div id="copyright" class="text-center py-5">
            <span><i class="far fa-copyright"></i> 2020 Maxcoach. All Rights Reserved</span>
        </div>
    </footer>
</template>

<script>
export default {
    name:'Footer',
    data(){
        return{
            socials:[
                {
                    icon: 'fa-twitter'
                },
                {
                    icon: 'fa-facebook-f'
                },
                {
                    icon: 'fa-instagram'
                },
                {
                    icon: 'fa-linkedin'
                }
            ],
            exploreLinks:[
                {
                    text:'Start here'
                },
                {
                    text:'Succes story'
                },
                {
                    text:'Blog'
                },
                {
                    text:'Courses'
                },
                {
                    text:'Contact us'
                }
            ],

            infoLinks:[
                {
                    text:'Membership'
                },
                {
                    text:'Purchase guide'
                },
                {
                    text:'Privacy policy'
                },
                {
                    text:'Terms of service'
                }
            ],
            instaArr:[
                {
                    img:'120084500_197897808368764_8114555493043279565_n'
                },
                {
                    img:'120012142_177596140500760_8623485824101406058_n'
                },
                {
                    img:'120099363_364334431619755_7198812647386067017_n'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

    .title{
        color: black;
        font-weight: bold;
        font-size: 16px;
        padding: 5px 0;
    } 

    #address{
        .title{
            color: black;
            font-weight: bold;
            font-size: 16px;
        } 

        span, a{
            padding: 5px 0;
            font-size: 14px;
            color: $boulder;
        }
        #social{
            svg{
                color: $silver;
                font-size: 25px;
            }
        }
    } 

    #explore{
        a{
            color: $boulder; 
            font-size: 14px; 
        }
    }

    #info{

        a{
            color: $boulder; 
            font-size: 14px; 
        }
    }

    #insta{
        width: 380px;
        a{
            color: $button-orange;
            font-weight: bold;
            font-size: 14px;
        }

        #pics{
            img{
                widows: 120px;
                height: 115px;
            }
        }
    }

    #copyright{
        color: $silver;
        font-size: 14px;
        svg{
            font-size: 12px;
        }   
    }
</style>