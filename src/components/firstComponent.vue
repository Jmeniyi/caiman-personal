<template>
    <div class="mainContent">
        <div class="mainContent__infoBar">
            <div class="container">
                <div class="mainContent__infoBar_btns">
                    <ul class="mainContent__infoBar_btns-list" style="list-style-type: none;">
                        <li>

                            <a href="https://www.instagram.com/">
                                <img class="button" src="../assets/img/logo-instagram.svg" alt="Instagram">
                            </a>
                        </li>
                        <li>
                            <a href="https://www.facebook.com/">
                                <img src="../assets/img/logo-fb-simple.svg" alt="Facebook">
                            </a>
                        </li>
                        <li>
                            <a href="https://www.twitter.com/">
                                <img src="../assets/img/logo-twitter.svg" alt="Twitter">
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="mainContent__infoBar_mainText">
                    <p class="mainContent__infoBar_mainText-Luisa">Luisa</p>
                    <p class="mainContent__infoBar_mainText-Alfonsoa">Alfonso</p>
                    <p class="mainContent__infoBar_mainText-Orellana">Orellana</p>
                    <a href="to">GET STARTED</a>
                </div>
            </div>
        </div>
        <div class="mainContent__slider">
            <sliderComponent :items="slides" />
        </div>
    </div>
</template>

<script>
import image1Slider from '../assets/img/firstComponent/image1Slider.png'
import image2Slider from '../assets/img/firstComponent/image2Slider.jpg'
import image3Slider from '../assets/img/firstComponent/image3Slider.jpg'
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
                },
                {
                    slide: image2Slider,
                },
                {
                    slide: image3Slider,
                },
            ],
        };
    },
};
</script>

<style scoped>
.mainContent {
    width: 100%;
    height: 100vh;
    display: flex;
    overflow: hidden;
}

.mainContent__infoBar {
    width: 30%;
    height: 100%;
}
.mainContent__infoBar_btns {
    height: 50%;
    text-align: center;
}

.mainContent__infoBar_btns-list {
    margin-top: 30%;
}

.mainContent__infoBar_btns-list img {
    width: 60px;
    height: 60px;
    flex-shrink: 0;
    filter: drop-shadow(0px 3.7944445610046387px 8.537500381469727px rgba(0, 0, 0, 0.11));
}
.mainContent__infoBar_mainText {
    background: #FFF;
    z-index: 2;
    position: absolute;
    padding: 0px 80px 40px 0px;
    width: 40%;
    margin-left: 10%;
    margin-top: 5%;
    align-items: center;
    justify-items: center;
}

.mainContent__infoBar_mainText p {
    color: #3A3A3A;
    font-family: Work Sans;
    font-style: normal;
    font-weight: 700;
}

.mainContent__infoBar_mainText-Luisa {
    line-height: 65px;
    font-size: 55px;
}

.mainContent__infoBar_mainText-Alfonsoa {
    font-size: 110px;
    line-height: 120px;
}

.mainContent__infoBar_mainText-Orellana {
    font-size: 65px;
    line-height: 55px;
    margin-bottom: 30px;
}

.mainContent__infoBar_mainText a {
    color: #0159B1;
    font-family: Roboto;
    font-size: 25px;
    font-style: normal;
    font-weight: 500;
    line-height: 30px;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    text-decoration: none;
}
.sliderComponent>>>.controls {
    position: absolute;
    bottom: 0;
    left: 35%;
}

.sliderComponent>>>.btnSlide {
    background-color: #3A3A3A;
    color: #fff;
    font-size: 60px;
    padding: 10px;
    cursor: pointer;
    border-width: 0px 0px 0px 1px;
    border-color: #4A4A4A;
}

.sliderComponent>>>.btnSlide:hover {
    color: rgba(210, 202, 202, 0.7);
}

.mainContent__slider {
    position: relative;
    width: 100%;
    height: 100%;
    overflow: hidden;
}

.sliderComponent>>>.sliderComponent__slideImage {
    position: absolute;
    width: 100%;
    height: 100%;
    background-repeat: no-repeat;
    background-size: cover;
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

}

.sliderComponent>>>.slide-leave-to {
    transform: translateX(0%);

}
</style>