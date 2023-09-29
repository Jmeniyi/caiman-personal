<template>
    <div class="thirdComponent">
        <div class="mainContent__infoBar">
            <div class="mainContent__infoBar_nav">
                <div class="mainContent__infoBar_nav-btns">
                    <p>Our<br /> Works</p>
                    <a href="">View all</a>
                </div>
            </div>
            <div class="mainContent__slider">
                <sliderComponent :items="slides" />
            </div>
        </div>
    </div>
</template>

<script>
import image1Slider from '../assets/img/thirdComponent/image1Third.jpg'
import image2Slider from '../assets/img/thirdComponent/image2Third.jpg'
import image3Slider from '../assets/img/thirdComponent/image3Third.png'
import sliderComponent from './sliderComponent'
export default {
    components: {
        sliderComponent
    },
    data() {
        return {
            slides: [
                {
                    slide: image1Slider,
                    title: "Elegant luxury house1"
                },
                {
                    slide: image2Slider,
                    title: "Elegant luxury house2"
                },
                {
                    slide: image3Slider,
                    title: "Elegant luxury house3"
                },
            ],
        };
    },
};
</script>

<style scoped>
.thirdComponent {
    width: 100%;
    height: 100vh;
    display: flex;
    overflow: hidden;
}

.mainContent__infoBar {
    width: 100%;
    height: 100%;
    display: flex;
    padding-top: 15vh;
    padding-bottom: 15vh;
}

.mainContent__infoBar_nav {
    width: 100%;
    height: 100%;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;

}

.mainContent__infoBar_nav-btns {
    position: relative;
    width: auto;
    height: 100%;
}

.mainContent__infoBar_nav p {
    color: #3A3A3A;
    font-family: Work Sans;
    font-size: 60px;
    font-style: normal;
    font-weight: 700;
    line-height: 70px;
    letter-spacing: 2px;
    text-align: start;
    margin-bottom: 5rem;
}

.mainContent__infoBar_nav a {
    color: #2A2A2A;
    text-decoration-color: #0159B1;
    font-family: Roboto;
    font-size: 30px;
    font-style: normal;
    font-weight: 500;
    line-height: 40px;
    letter-spacing: 0.5px;
    text-transform: uppercase;
}

.mainContent__slider {
    align-self: center;
    position: relative;
    width: 70%;
    height: 100%;
    overflow: hidden;
    flex-shrink: 0;

}

.sliderComponent>>>.controls {
    position: absolute;
    top: 0;
}

.sliderComponent>>>.btnSlide {
    background: transparent;
    color: #0159B1;
    font-size: 60px;
    padding: 10px;
    cursor: pointer;
    border: 1px solid #0159B1;
}

.sliderComponent>>>.btnSlide:hover {
    color: rgba(1, 89, 177, 0.5);
}

.sliderComponent>>>.sliderComponent__slideImage {
    display: flex;
    position: absolute;
    height: 100%;
    width: 60%;
    background-repeat: no-repeat;
    background-size: cover;
}

.sliderComponent>>>.sliderComponent__slideImage_title {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 40%;
    margin: 0px 20px 40px 40px;
    background: transparent;
    color: #FFF;
    font-family: Work Sans;
    font-size: 18px;
    font-style: normal;
    font-weight: 600;
    line-height: 32px;
    /* 177.778% */
    letter-spacing: 0.5px;
    text-transform: uppercase;
}

.sliderComponent>>>.slide-enter-active {
    transition: transform 0.8s;
}

.sliderComponent>>>.slide-leave-active {
    opacity: 0.1;
    transition: transform 0.8s;

}

.sliderComponent>>>.slide-enter-from {
    transform: translateX(100%);
    transition: transform 0.8s;
    opacity: 0.5;

}

.sliderComponent>>>.slide-leave-to {
    transform: translateX(170%);
    opacity: 1;

}</style>