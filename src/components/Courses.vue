<template>
  <section id="courses" class="mt-5">
        <div class="text-center py-4">
            <h2>Artist coaching</h2>
            <h3>Latest Online Courses</h3>
        </div>
        <div id="c-box" class="d-flex flex-wrap flex-row">
            <div class="custom_card px-3 mb-5" v-for="(element,index) in courses" :key="index">
                <div id="thumbnail">
                    <img :src="require(`@/assets/img/${element.img}.jpg`)" alt="">
                </div>
                <div id="info" class="d-flex flex-column py-4 px-3">
                    <span id="price" class="py-1">${{element.price}}</span>
                    <span id="title" class="py-1">{{element.title}}</span>
                    <div id="program" class="d-flex flex-row justify-content-between py-2">
                        <span class="d-flex align-items-center"><i class="far fa-file-alt"></i>{{element.lessons}} Lessons</span>
                        <span class="d-flex align-items-center"><i class="far fa-user"></i>{{element.students}} Students</span>
                    </div>
                </div>
            </div>
        </div>
        <div class="d-flex justify-content-center">
            <div class="custom_btn d-flex align-items-center">
                <span>View all courses</span><i class="fas fa-long-arrow-alt-right"></i>
            </div>
        </div>
        <!--BACKGROUND-->
        <img id="bbpp" src="@/assets/img/artist-shape-01.png" alt="">
  </section>
</template>

<script>
export default {
    name:'Courses',
    data(){
        return{
            courses:[
                {
                    img:'artist-course-08-480x480',
                    price:'18.00',
                    title:'The Acrylic Painting Academy',
                    lessons:'4',
                    stundents:'50'
                },
                {
                    img:'artist-course-07-480x480',
                    price:'21.00',
                    title:'Drawing and Shading: Complete Course',
                    lessons:'14',
                    stundents:'50'
                },
                {
                    img:'artist-course-06-480x480',
                    price:'19.00',
                    title:'The Color Theory for Digital Artist',
                    lessons:'7',
                    stundents:'50'
                },
                {
                    img:'artist-course-05-480x480',
                    price:'35.00',
                    title:'Ultimate Guide to Digital Sketching for Beginner',
                    lessons:'14',
                    stundents:'50'
                },
                {
                    img:'artist-course-04-480x480',
                    price:'19.00',
                    title:'Portrait Drawing The Smart Way',
                    lessons:'2',
                    stundents:'50'
                },
                {
                    img:'artist-course-03-480x480',
                    price:'19.00',
                    title:'Mastering Watercolor Painting for Beginner',
                    lessons:'9',
                    stundents:'50'
                },
                {
                    img:'artist-course-02-480x480',
                    price:'25.00',
                    title:'The Art & Science of Drawing',
                    lessons:'4',
                    stundents:'50'
                },
                {
                    img:'artist-course-01-480x480',
                    price:'22.00',
                    title:'The Colored Pencil Drawing Course',
                    lessons:'6',
                    stundents:'50'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

    #courses{
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

        .custom_card{
            z-index: 1;
            width: 313px;
            #thumbnail{
                width: 280px;
                height: 280px;
                img{
                    object-fit: cover;
                    width: 100%;
                    height: 100%;
                    cursor: pointer;
                }
            }

            #info{
                transition: 0.2s ease-in-out;
                width: 90%;
                z-index: 2;
                background-color: white;
                max-width: 250px;

                #price{
                    color: $button-orange;
                    font-weight: bold;
                }

                #title{
                    font-weight: bold;
                    line-height: 30px;
                    font-size: 20px;
                }

                #program{
                    svg{
                        padding: 0 5px;
                    }
                    span, svg{
                        color: $boulder;
                        font-size: 14px;
                    }
                }
            }


        }

        .custom_card:hover > #info{
            box-shadow: 0 0 0 2px $button-orange, 4px 4px 15px 0px rgba(0,0,0,0.22);
            transform: translate(0, -40px);
        }

        .custom_btn{
            background-color: $hint-of-red;
            color: $button-orange;
            padding: 15px 30px;

            svg{
                padding: 0 7px;
            }
        }

        .custom_btn:hover{
            background-color: $button-orange;
            color: white;
        }

        #bbpp{
            position: absolute;
            transform: rotate(270deg);
            top: 150px;
            right: -340px;
        }
    }
</style>