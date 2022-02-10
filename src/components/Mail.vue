<template>
    <section id="mail" class="d-flex flex-row align-items-center justify-content-around">
        <h3>Newsletter to get in touch</h3>
        <form action="" class="d-flex justify-content-between">
            <input type="email" id="email" name="email" placeholder="Your e-mail">
            <button name="email" value="email"><i class="fas fa-long-arrow-alt-right"></i></button>
        </form> 
        <!--BACKGROUND-->
        <img id="left" src="@/assets/img/artist-shape-color-paint-top-left.png" alt="">   
        <img id="right" src="@/assets/img/artist-shape-color-paint-bottom-right.png" alt="">   
    </section>
</template>

<script>
export default {
    name: 'Mail'
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';


    #mail{
        position: relative;
        background-color: $bay-of-many;
        color: white;
        height: 200px;
        z-index: 3;
        h3{
            width: 250px;
            text-align: right;
            line-height: 46px;
            font-size: 32px;
            font-family:'Playfair Display', serif;
        }

        form{
            border-bottom: 2px solid rgb(154, 152, 152, 0.3);
            width: 640px;
        }

        input[type=email]{
            width: 90%;
            height: 40px;
            border: none;
            color: white;
            font-weight: 100;
            background-color: transparent;
            font-size: 24px;
            
        }
        input[type=email]::placeholder{
            color: white;       
        }

        input[type=email]:focus{
            outline: none;
        }

        button{
            font-size: 26px;
            color: white;
            border: none;
            background-color: transparent;
        }   

        /*BACKGROUND*/
        #left{
            position: absolute;
            left: 0;
            z-index: -1;
        }

        #right{
            position: absolute;
            right: 0;
            bottom: 0;
            z-index: -1;
        }
    }

</style>