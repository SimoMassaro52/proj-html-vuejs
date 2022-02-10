<template>
    <main>
        <Jumbo />
        <Coaching />
        <Quote />
        <Video />
        <Slider />
        <Courses />
        <Articles />
        <Events />
    </main>
</template>

<script>
import Jumbo from './Jumbo.vue'
import Coaching from './Coaching.vue'
import Quote from './Quote.vue'
import Video from './Video.vue'
import Slider from './Slider.vue'
import Courses from './Courses.vue'
import Articles from './Articles.vue'
import Events from './Events.vue'


export default {
    name: 'Main',
    components:{
        Jumbo,
        Coaching,
        Quote,
        Video,
        Slider,
        Courses,
        Articles,
        Events
    }
}
</script>

<style lang="scss" scoped>

</style>