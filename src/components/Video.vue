<template>
    <section id="video" class="d-flex justify-content-center align-items-center">
        <div class="d-flex justify-content-center align-items-center">
            <img id="bg" src="@/assets/img/artist-video-poster.jpg" alt="">
            <img id="fg" src="@/assets/img/icon-youtube-play.png" alt="">
        </div>

        <!-- BACKGROUND -->
        <img id="green-dots" src="@/assets/img/maxcoach-shape-05-150x150.png" alt="">
        <img id="blue-dots" src="@/assets/img/maxcoach-shape-12-150x150.png" alt="">

    </section>
</template>

<script>
export default {
    name: 'Video'
}
</script>

<style lang="scss" scoped>

    #video{
        height: 85vh;
        position: relative;
        div{
            #bg{
                width: 600px;
                position: relative;
                z-index: 1;
                border-radius: 5px;
            }

            #fg{
                position: absolute;
                width: 70px;
                z-index: 2;
            }
        }
        /*BACKGROUND*/
        #green-dots{
            position: absolute;
            left: 300px;
            top: 30px;
        }

        #blue-dots{
            position: absolute;
            right: 200px;
            bottom: 30px;
        }
    }

</style>