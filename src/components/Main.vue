<template>
    <main>
        <Jumbo />
        <Coaching />
        <Quote />
    </main>
</template>

<script>
import Jumbo from './Jumbo.vue'
import Coaching from './Coaching.vue'
import Quote from './Quote.vue'



export default {
    name: 'Main',
    components:{
        Jumbo,
        Coaching,
        Quote
    }
}
</script>

<style lang="scss" scoped>

</style>