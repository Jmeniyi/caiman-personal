<template>
  <div id="app">
   <headerComponent/>
   <mainWithSliderComponent/>
   <quvotesComponent/>
   <thirdComponent/>
  </div>
  <router-view></router-view>
</template>

<script>
import headerComponent from './components/headerComponent.vue'
import mainWithSliderComponent from './components/firstComponent.vue'
import quvotesComponent from './components/secondComponent.vue'
import thirdComponent from './components/thirdComponent.vue'
export default ({
  data() {
    return{

    }
  },
  components: {
    headerComponent,
    mainWithSliderComponent,
    quvotesComponent,
    thirdComponent
  },
})
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
