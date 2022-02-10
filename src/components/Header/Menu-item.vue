<template>
   <!--DROPDOWN ITEMS-->
    <div class="dropdown_item px-4 h-100" @click="linkData.angle = !linkData.angle" @mouseleave="linkData.angle = false">
        <span>{{linkData.text}}</span>
        <i class="fa-solid fa-angle-down px-1"></i>
        <!--DROPDOWN MENU-->
        <div id="dropdown_menu" class="hidden" :class="{visible: linkData.angle}">
            <a href="#">Lorem</a>
        </div>
    </div>   
</template>

<script>
export default {
    name:'Menu-item',
    props:{
        linkData: Object
    }
}
</script>

<style lang="scss" scoped>

.dropdown_item{
    cursor: pointer;
}

.hidden{
    display: none;
}

.visible{
    display: block;
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


</style>