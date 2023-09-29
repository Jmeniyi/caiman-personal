<template>
    <div class="sliderComponent">
        <transition-group name="slide" v-for="(src, index) in items" :key="index">
          <div 
          v-if="index === currentSlide"
          :title="src.title"
          :style="{ backgroundImage: 'url(' + src.slide + ')' }"
          class="sliderComponent__slideImage"
          >
          <span v-if="index === currentSlide" class="sliderComponent__slideImage_title">{{ src.title }}</span>
          <span v-if="index === currentSlide" class="sliderComponent__slideImage_author">{{ src.author}}</span>
          <div class="sliderComponent__slideImage_circleContainer">
          <div v-for="item in items" :key="item.id" class="sliderComponent__slideImage_circle"></div>
          <div class="sliderComponent__slideImage_circle_Outer-circle"></div>
        </div>
          </div>
      </transition-group>
      <div class="controls">
        <button class="btnSlide" @click="prevSlide">&lt;</button>
        <button class="btnSlide" @click="nextSlide">></button>
      </div>
    </div>
  </template>

  <script>
  export default {
    name: "sliderComponent",
    props: {
          items: {
              type: Array,
              required: true,
          },
      },
    data() {
      return {
        currentSlide: 0,
      };
    },
    methods: {
      prevSlide() {
        this.currentSlide -= 1;
        if (this.currentSlide < 0) {
          this.currentSlide = this.items.length - 1;
        }
      },
      nextSlide() {
        this.currentSlide += 1;
        if (this.currentSlide >= this.items.length) {
          this.currentSlide = 0;
        }
      },
    },
  };
  </script>
  <style>
</style>