<template>
    <main>
        <Jumbo />
        <Coaching />
        <Quote />
        <Video />
        <Slider />
        <Courses />
    </main>
</template>

<script>
import Jumbo from './Jumbo.vue'
import Coaching from './Coaching.vue'
import Quote from './Quote.vue'
import Video from './Video.vue'
import Slider from './Slider.vue'
import Courses from './Courses.vue'


export default {
    name: 'Main',
    components:{
        Jumbo,
        Coaching,
        Quote,
        Video,
        Slider,
        Courses
    }
}
</script>

<style lang="scss" scoped>

</style>