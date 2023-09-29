<template>
  <div id="app">
   <headerComponent/>
   <section id="firstComponent">
    <firstComponent/>
  </section>
  <section id="secondComponent">
    <secondComponent/>
  </section>
  <section id="thirdComponent">
    <thirdComponent/>
  </section>
  <section id="footerComponent">
    <footerComponent/>
  </section>
  </div>
  <router-view></router-view>
</template>

<script>
import headerComponent from './components/headerComponent.vue'
import firstComponent from './components/firstComponent.vue'
import secondComponent from './components/secondComponent.vue'
import thirdComponent from './components/thirdComponent.vue'
import footerComponent from './components/footerComponent.vue'

export default ({
  data() {
    return{

    }
  },
  components: {
    headerComponent,
    firstComponent,
    secondComponent,
    thirdComponent,
    footerComponent
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
