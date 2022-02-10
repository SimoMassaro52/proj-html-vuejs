<template>
    <section id="articles" class="d-flex flex-column mt-5">
        <div class="text-center py-5">
            <h2>Articles and Tips</h2>
            <h3>Latest From The Blog</h3>
        </div>

  
        <div id="row-container" class="d-flex flex-row justify-content-around">
            <!--LEFT-->
            <div class="custom_card">
                <img src="@/assets/img/artist-blog-03-480x356.jpeg" alt="">
                <div id="text" class="d-flex flex-column p-3">
                    <span class="type py-1">ARTIST</span>
                    <span class="title py-1">Brush Strokes Energize Trees in Paintings</span>
                    <div id="data" class="d-flex flex-row justify-content-between py-3">
                        <span class="d-flex align-items-center"><i class="far fa-calendar"></i>May 15, 2020</span>
                        <span class="d-flex align-items-center"><i class="far fa-eye"></i>1,271 views</span>
                    </div>
                </div>
            </div>

             <!--MID-->
            <div id="mid" class="d-flex flex-column justify-content-end">
                <div id="text" class="d-flex flex-column p-4">
                    <span class="type py-1">ARTIST</span>
                    <span class="title py-1">Connection Between Self-Portraits and Identity</span>
                    <div id="data" class="d-flex flex-row py-3">
                        <span class="d-flex align-items-center"><i class="far fa-calendar"></i>May 15, 2020</span>
                        <span class="d-flex align-items-center"><i class="far fa-eye"></i>1,271 views</span>
                    </div>
                </div>
            </div>

            <!--RIGHT-->
            <div class="custom_card">
                <img src="@/assets/img/artist-blog-01-480x356.jpg" alt="">
                <div id="text" class="d-flex flex-column p-3">
                    <span class="type py-1">ARTIST</span>
                    <span class="title py-1">Pocket-Sized Notebooks Hold Miniature Paintings</span>
                    <div id="data" class="d-flex flex-row justify-content-between py-3">
                        <span class="d-flex align-items-center"><i class="far fa-calendar"></i>May 15, 2020</span>
                        <span class="d-flex align-items-center"><i class="far fa-eye"></i>1,141 views</span>
                    </div>
                </div>
            </div>
        </div>

        <div id="details" class="d-flex justify-content-center py-5">
            <span class="py-5">Get into details now? <a href="#">View all posts <i class="fas fa-long-arrow-alt-right"></i></a></span>
        </div>

        <!--BACKGROUND-->
        <img id="string" src="@/assets/img/maxcoach-shape-03.png" alt="">
        <img id="green-dots" src="@/assets/img/maxcoach-shape-05-150x150.png" alt="">
    </section>
</template>

<script>
export default {
    name:''
}   
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

    #articles{
        background-color: #F5F7FA;

        h2{
            font-family: 'Arizonia', cursive;
            color: $ice-cold;
            font-size: 50px;
        }

        h3{
            font-weight: bold;
            font-size: 35px;
        }

        #row-container{
            position: relative;

            .custom_card:first-child{
                position: absolute;
                left:40px;
                bottom: 110px;
            }

            .custom_card:last-child{
                position: absolute;
                right: 40px;
                top: 50px;
            }

            #mid{
                background-image: url('~@/assets/img/artist-blog-02-500x680.jpg');
                width: 500px;
                height: 650px;
                color: white;
                box-shadow: inset 0px 0px 50px 50px rgba(0,0,0,0.10);
                z-index: 1;

                .type{
                    letter-spacing: 1px;
                }

                .title{
                    font-size: 30px;
                    font-weight: bold;
                }

                #data{
                    span:nth-child(2){
                        padding: 0 35px; 
                    }

                    svg, span{
                        font-size: 14px;
                        padding: 0 3px;
                    }
                }
            }

            .custom_card{
                width: 270px;
                max-height: 385px;
                box-shadow: 4px 4px 15px 0px rgba(0,0,0,0.22);
                z-index: 1;

                img{
                    object-fit: cover;
                    width: 100%;
                }

                #text{
                    background-color: white;
                    .type{
                        letter-spacing: 1px;
                        color: $dusty-gray;
                    }
                    
                    .title{
                        font-weight: bold;
                        font-size: 18px;
                    }

                    #data{
                        svg, span{
                            color: $boulder;
                            font-size: 14px;
                            padding: 0 3px;
                        }

                    }
                }
            }
        } 
        
        #details{
            span{
                color: $boulder;
                a{
                    color: $button-orange;
                    border-bottom: 1px solid $dusty-gray;
                }
            }
        }

        /*BACKGROUND*/
        #string{
            position: absolute;
            width: 100%;
            top: 4850px;
        }
        #green-dots{
            position: absolute;
            top: 4750px;
            left: 310px;
        }

    }

</style>