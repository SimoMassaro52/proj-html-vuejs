<template>
  <section id="slider" class="d-flex flex-column py-4">
        <div class="text-center">
            <h2>Testimonials</h2>
            <h3>Why do people love me?</h3>
        </div>   
        <!--SLIDER-->
        <div id="s-box" class="d-flex justify-content-center align-items-center py-5">

            <div v-for="(element, index) in slideArr" :key="index" :class="{opacity: element.overlay }" class="custom_card d-flex flex-column justify-content-between mx-4" >
                <div>
                    <span>{{element.res}}</span>
                    <p class="py-1">{{element.obj}}</p>
                </div>    
                <div class="info d-flex flex-row">
                    <img :src="require(`@/assets/img/${element.img}.jpg`)" class="rounded-circle" alt="">
                    <div class="empl px-3">
                        <span>{{element.name}}</span>
                        <p class="mb-1 py-1">/{{element.occupation}}</p>
                    </div>
                </div>
            </div>
        </div>

        <div id="dots" class="d-flex justify-content-center align-items-center py-2">
            <i class="fa-solid fa-circle"></i>
            <i class="fa-solid fa-circle"></i>
            <i class="fa-solid fa-circle"></i>
            <i class="fa-solid fa-circle"></i>
        </div>
  </section>
</template>

<script>
export default {
    name:'Slider',
    data(){
        return{
            slideArr:[
                {
                    res:'It is a choice of quality for people with special needs',
                    obj:'I am a very strict person so I require everything to be organized and neat. Then, I will be able to make things right and shine. MaxCoach guys just got me.',
                    img:'artist-testimonial-avatar-02',
                    name:'Florence Themes',
                    occupation: 'Multimedia Admin',
                    overlay: true
                },
                 {
                    res:'High level of efficiency and scientific teaching methods',
                    obj:'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me',
                    img:'artist-testimonial-avatar-04',
                    name:'Mina Hollace',
                    occupation: 'Freelancer',
                    overlay: false
                },
                 {
                    res:'Professional team of specialists and passionate mentors at reach',
                    obj:'I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.',
                    img: 'artist-testimonial-avatar-01',
                    name:'Madley Pondor',
                    occupation: 'IT Specialist',
                    overlay: true
                },
            ]
        }
    },

    methods:{
        
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

#slider{
    height: 100vh;
    background-color: #FBF9F6;
    h2{
        font-family: 'Arizonia', cursive;
        color: $ice-cold;
        font-size: 40px;
    }
    
    h3{
        font-weight: bold;
    }

    #s-box{

        .custom_card{
            position: relative;
            background-color: white;
            width: 375px;
            height: 300px;
            border-radius: 5px;
            padding: 35px 25px;

            span{
                font-weight: bold;
                font-size: 14px;
            }

            p{
                font-size: 12px;
            }

            img{
                width: 50px;
                height: 50px;
            }
        }
    }

    #dots{
        svg:first-child{
            color: black;
            font-size: 12px;
        } 
        svg{
            margin: 0 5px;
            color: #d8d8d8;
            font-size: 8px;
        }
    }

    .opacity{
        opacity: 0.5;
    }
}
    
</style>