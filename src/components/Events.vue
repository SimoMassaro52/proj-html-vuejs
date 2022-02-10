<template>
    <section id="events" class="d-flex flex-column">
        <div class="text-center py-5">
            <h2>Upcoming Events</h2>
            <h3>Let's Work Together</h3>
        </div>

        <div id="c-box" class="d-flex justify-content-around ">
            <div v-for="(element, indexU) in upperEvents" :key="indexU" class="custom_card d-flex flex-row">
                <img :src="require(`@/assets/img/${element.img}.jpg`)" alt="">
                <div id="text" class="d-flex align-items-center justify-content-center">
                    <div class="d-flex flex-column">
                        <span class="date">{{element.date}}</span>
                        <span class="event py-2">{{element.event}}</span>
                        <span class="location"><i class="fas fa-map-marker-alt"></i>{{element.location}}</span>
                    </div>
                </div>
            </div>
        </div>

        <div id="c-box" class="d-flex justify-content-around py-5">
            <div v-for="(element, indexL) in lowerEvents" :key="indexL" class="custom_card custom_lower d-flex flex-row">
                <div id="text" class="d-flex align-items-center justify-content-center">
                    <div class="d-flex flex-column">
                        <span class="date">{{element.date}}</span>
                        <span class="event py-2">{{element.event}}</span>
                        <span class="location"><i class="fas fa-map-marker-alt"></i>{{element.location}}</span>
                    </div>   
                </div>
                <img :src="require(`@/assets/img/${element.img}.jpg`)" alt="">
            </div>
        </div>

        <!--BACKGROUND-->
        <img id="shape" src="@/assets/img/artist-shape-02-600x324.png" alt="">
        <img id="circle" src="@/assets/img/maxcoach-shape-13.png" alt="">

    </section>
</template>

<script>
export default {
    name:'Events',
    data(){
        return{
            upperEvents:[
                {
                    img:'artist-event-04-250x300',
                    date: 'APR 22, 2021',
                    event:'Storytelling Workshop',
                    location:'Texas, US'
                },
                {
                    img:'artist-event-03-250x300',
                    date: 'OCT 10, 2020',
                    event:'Painting Art Contest 2020',
                    location:'New York, US'
                }
            ],
            lowerEvents:[
                {
                    img:'artist-event-02-250x300',
                    date: 'NOV 23, 2020',
                    event:'International Art Fair 2020',
                    location:'Hamburg, Germany'
                },
                {
                    img:'artist-event-01-250x300',
                    date: 'DEC 15, 2020',
                    event: 'Street Performance: Call for Artist',
                    location:'Illinois, US'
                }
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';


    #events{
        position: relative;
        h2{
            font-family: 'Arizonia', cursive;
            color: $ice-cold;
            font-size: 50px;
        }

        h3{
            font-weight: bold;
            font-size: 35px;
        }

        #c-box{
            .custom_card{

                #text{

                    width: 320px;

                    div{
                        .date{
                            letter-spacing: 2px;
                            color: $boulder;
                        }

                        .event{
                            font-weight: bold;
                            font-size: 18px;
                        }

                        .location{
                            color: $dusty-gray;
                            font-size: 14px;
                            svg{
                                padding: 0 5px;
                            }
                        }
                    }    
                }
            }

            .custom_lower{
                #text{
                    text-align: right;
                }
            }
        }

        /*BACKGROUND*/
        #shape{
            position: absolute;
            transform: rotate(270deg);
            left: -150px;
            bottom: -50px;
        }

        #circle{
            position: absolute;
            right: 50px;
            top: 160px;
        }
    }

</style>