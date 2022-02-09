<template>
    <section id="coaching" class="d-flex flex-column align-items-center mt-5">
        <div id="c-box" class="text-center">
            <h3>Artist coaching</h3>
            <h2>I understand what it takes to create. </h2>
            <h2>I can help you with</h2>
        </div>
        <div id="sec-box" class="d-flex flex-row pt-5">
            <div class="c-card d-flex flex-column px-2 mx-1 my-2" v-for="(section, index) in sections" :key="index">
                <img :src="require(`@/assets/img/${section.img}.png`)" alt="">
                <span class="py-2">{{section.title}}</span>
                <p class="py-2">{{section.paragraph}}</p>
            </div>
        </div>

        <!--BACKGROUND-->
        <img id="bbpp" src="@/assets/img/artist-shape-01.png" alt="">
        <img id="string" src="@/assets/img/maxcoach-shape-14-1024x229.png" alt="">
        <img id="w-circle" src="@/assets/img/maxcoach-shape-13.png" alt="">
    </section>
</template>

<script>
export default {
    name:'Coaching',
    data(){
        return{
            sections:[
                {
                    img:'artist-box-image-01',
                    title:'Online Coures',
                    paragraph:'Online art coaching now offers you a very powerful way to redesign your artist mind.'
                },
                {
                    img:'artist-box-image-02',
                    title:'Online Coures',
                    paragraph:'Online art coaching now offers you a very powerful way to redesign your artist mind.'
                },
                {
                    img:'artist-box-image-03',
                    title:'Online Coures',
                    paragraph:'Online art coaching now offers you a very powerful way to redesign your artist mind.'
                },
                {
                    img:'artist-box-image-04',
                    title:'Online Coures',
                    paragraph:'Online art coaching now offers you a very powerful way to redesign your artist mind.'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

#coaching{
    height: 90vh;
    widows: 100%;
    position: relative;

    #c-box{
        h3{
            font-family: 'Arizonia', cursive;
            color: $ice-cold;
            font-size: 45px;
        }
        h2{
            font-weight: bold;
            font-size: 35px;
        }
    }

    #sec-box{
        padding: 0 140px;
        .c-card{
            width: calc(100% / 4);
            z-index: 1;
            span{
                font-weight: bold;
                font-size: 16px;
            }
            p{
                font-size: 14px;
            }
        }
        img{
            max-width: 135px !important;
            max-height: 135px !important;
        }
    }

    /*BACKGROUND*/

    #bbpp{
        position: absolute;
        transform: rotate(240deg);
        width: 450px;
        bottom: 0px;
        left: -100px
    }
    
    #string{
        position: absolute;
        width: 100vw;
        top: 170px
    }

    #w-circle{
        position: absolute;
        top: 200px;
        right: -40px;
    }
}

</style>