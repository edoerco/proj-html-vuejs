<template>
  <main>
    <Excellence />
    <services />
    <Logistical />
    <Results />
    <Feedback />
    <Touch />
  </main>
</template>

<script>
import Excellence from './Excellence.vue'
import Feedback from './Feedback.vue'
import Logistical from './Logistical.vue'
import Results from './Results.vue'
import Services from './Services.vue'
import Touch from './Touch.vue'
export default {
    name: 'Main',
    components: { 
        Excellence,
        Services,
        Logistical,
        Results,
        Feedback,
        Touch,
        },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';


</style>