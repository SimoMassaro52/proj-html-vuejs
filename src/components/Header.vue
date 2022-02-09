<template>
  <header>

      <!-- TIMER SUB SECTION -->
    <section id="timer" class="d-flex justify-content-center">
        <div id="clock" class="d-flex align-items-center justify-content-between">
            <span>Starts TOMORROW! Our biggest event of the year...</span>
            <span class="mx-3"><i class="bi bi-clock"></i> 00 : 00 : 00 : 00</span>
        </div>
        <div class="d-flex align-items-center px-5">
            <div class="custom_btn">
                <span>Get ticket</span>
            </div>
        </div>
    </section>

        <!-- NAV -->
    <nav class="navbar navbar-light bg-light">
        <div class="container justify-content-between">
            <!-- NAV LOGO -->
            <a class="navbar-brand" href="#">
                <img src="@/assets/img/dark-logo.png" alt="" width="" height="25">
            </a>     

            <ul class="navbar-nav d-flex flex-row h-100">
                <!--DROPDOWN ITEMS-->
                <div class="dropdown_item px-4 h-100" @click="element.angle = !element.angle" @mouseleave="element.angle = false" v-for="(element, index) in links" :key="index">
                    <span>{{element.text}}</span>
                    <i class="fa-solid fa-angle-down px-1"></i>
                    <!--DROPDOWN MENU-->
                    <div id="dropdown_menu" class="hidden" :class="{visible: element.angle}">
                        <a href="#">Lorem</a>
                    </div>
                </div>   

            </ul>
            
            <div class="nav-item d-flex flex-row" id="socials">
                <a class="nav-link active" v-for="(social, indexS) in socials" :key="indexS" aria-current="page" href="#">
                    <i :class="`fa-brands ${social.icon}`"></i>
                </a>
            </div>
        </div>
    </nav>
  </header>
  
</template>


<script>

export default {
    name: 'Header',
    data(){
        return{
            links:[
                {
                    text:'Home',
                    angle: false
                },
                {
                    text:'Pages',
                    angle: false
                },
                {
                    text:'Features',
                    angle: false
                },
                {
                    text:'Blog',
                    angle: false
                },
                {
                    text:'Shop',
                    angle: false
                }
            ],
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
            ]
        }
    }
}

</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

/*TIMER SUB SECTION*/
#timer{
    background-color: $silver;
    height: 50px;
}

#clock{
    span:first-child{
        color: $boulder;
    }
}

.custom_btn{
    background-color: $button-orange;
    color: white;
    padding: 5px 30px;
    border-radius: 5px;
    font-weight: 700;
    cursor: pointer;
    transition: 0.2s ease-in-out;
}

.custom_btn:hover{
    background-color: $ice-cold;
}

/*NAV*/

nav{
    background-color: white !important;
}

/*DROPDOWN MENU*/

.dropdown_item{
    cursor: pointer;
}

.hidden{
    display: none !important;
}

.visible{
    display: block !important;
}

.fa-angle-down{
    font-size: 10px;
}

#dropdown_menu{
    position: absolute;
    z-index: 2;
    width: max-content;
    background-color: white;
    padding: 10px 0;
    box-shadow: 1px 1px 2px 0px #000000;
    a{
        display: block;
    }
}

/*SOCIALS*/

#socials{
    a{
        color: $boulder;
        padding: 10px 10px;
    }
}
</style>