<template>
    <main>
        <section id="jumbo" class="d-flex justify-content-center align-items-center"> 
            <div id="p-box" class="text-center">
                <h3>Hello, Im Matin</h3>
                <h2>Artist Coaching And Mentoring Might Be for You.</h2>
                <div class="d-flex justify-content-center py-4">
                    <div class="custom_btn">
                        <span>Get started today</span>
                    </div>
                </div>    
            </div>
            <!--BIG BLUE TEXTURE-->  
            <img id="big-blue" src="@/assets/img/artist-shape-03.png" alt="">
            <!--HEAD-->
            <img id="head" src="@/assets/img/artist-hero-image-03.png" alt="">
            <!--ABSTRACT-->
            <img id="abstract" src="@/assets/img/artist-hero-image-02.jpg" alt="">
            <!--MONKEY-->
            <img id="monkey" src="@/assets/img/artist-hero-image-01.jpg" alt="">
            <!--FEATHER-->
            <img id="feather" src="@/assets/img/artist-shape-04.png" alt="">
            <!--BRUSHSTROKE-->
            <img id="brush" src="@/assets/img/artist-shape-05.png" alt="">
            <!--SMALL BLUE TEXTURE-->
            <img id="small-blue" src="@/assets/img/maxcoach-shape-12.png" alt="">
            <!-- B&W PORTRAIT-->
            <img id="portrait" src="@/assets/img/artist-hero-image-04.jpg" alt="">

        </section>
    </main>
</template>

<script>
export default {
    name: 'Main'
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';
@import url('https://fonts.googleapis.com/css2?family=Caveat&display=swap');
    
    #jumbo{
        position: relative;
        background-color: #FBF9F6;
        height: 120vh;
        width: 100%;
        background-image:
            url('~@/assets/img/artist-shape-02-600x324.png'), 
            url('~@/assets/img/artist-shape-01.png');
        background-position:
            left 10px top 0px,
            right 100px top 0px;
        background-repeat: no-repeat;
    }

    #p-box{
        z-index: 3;
        width: 650px;
        h3{
            font-family: 'Caveat', cursive;
            color: $ice-cold;
            font-size: 50px;
        }
        h2{
            font-weight: bold;
            font-size: 40px;
        }
        .custom_btn{
            background-color: $button-orange;
            color: white;
            padding: 14px 30px;
        }
        .custom_btn:hover{
            background-color: $ice-cold;
        }
    }
    /*HERO IMGS*/
    img{
        position: absolute;
    }

    #big-blue{
        bottom: 10px;
        left: 10px;
    }

    #head{
        bottom: 5px;
        left: 350px;
    }

    #abstract{
        top: 100px;
        left: 200px;
        box-shadow: 4px 4px 15px 0px rgba(0,0,0,0.22);
    }

    #monkey{
        bottom: 10px;
        left: 210px;
        box-shadow: 4px 4px 15px 0px rgba(0,0,0,0.22);
    }

    #feather{
        right: 100px;
        top: 70px;
    }

    #brush{
        right: 40px;
        bottom: 0px;
    }

    #small-blue{
        right: 200px;
        bottom: 40px;
    }

    #portrait{
        right: 100px;
        top: 200px;
        box-shadow: 4px 4px 15px 0px rgba(0,0,0,0.22);
    }
</style>