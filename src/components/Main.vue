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
        <Mail />
    </main>
</template>

<script>
import Jumbo from './Main/Jumbo.vue'
import Coaching from './Main/Coaching.vue'
import Quote from './Main/Quote.vue'
import Video from './Main/Video.vue'
import Slider from './Main/Slider.vue'
import Courses from './Main/Courses.vue'
import Articles from './Main/Articles.vue'
import Events from './Main/Events.vue'
import Mail from './Main/Mail.vue'


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
        Events, 
        Mail
    }
}
</script>

<style lang="scss" scoped>

</style>