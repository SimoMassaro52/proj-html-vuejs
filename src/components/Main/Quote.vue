<template>
  <section id="quote" class="d-flex flex-row">
    <div class="d-flex flex-column text-center align-items-center justify-content-center mx-4">
        <img src="@/assets/img/artist-quote-icon.png" alt="">
        <h2 class="py-5">I coach and mentor visual artists, like you, to Create Like You Mean It</h2>
        <h3>Martin Garrix</h3>
    </div>
    <div class="d-flex flex-column justify-content-center mx-4">
        <p>As a coach and mentor, my ultimate goal is to motivate visual artists toward inspired action. I help you get you back on track to being the productive, creative, meaningful and authentic artist you truly want to be.I support artists in crafting and living a creative life as well as feeling good about themselves and their art.</p>
        <p>As an artist and an educator for nearly 30 years, I understand what it takes to create.</p>
        <div class="custom_btn text-center">
            <span>Get started today</span>
        </div>    
    </div>
  </section>    
</template>

<script>
export default {
    name:'Quote'
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

    #quote{
        height: 100vh;
        padding: 0 150px;
        div{
            width: calc(100% / 2);
        }
        img{
            max-width: 40px;
        }

        h2{
            font-weight: bold;
            line-height: 1.3em;
            font-size: 40px;
        }

        h3{
            font-family: 'Arizonia', cursive;
            color: $heading-blue;
            font-size: 35px;
        }

        .custom_btn{
            background-color: $hint-of-red;
            color: $button-orange;
            padding: 15px 30px;

        }

        .custom_btn:hover{
            background-color: $button-orange;
            color: white;
        }
    }  
</style>