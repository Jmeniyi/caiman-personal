<template>
    <div id="secondComponent">
        <div class="secondComponent__slaiderComponent">
            <sliderComponent :items="quvotes" />
            <img src='../assets/img/secondComponent/Vector.svg' alt="img">
            <img src='../assets/img/secondComponent/Vector2.svg' alt="img">
        </div>
        <div class="secondComponent_brands">
            <img src="../assets/img/client1.svg" alt="client1" height="33" width="139">
            <img src="../assets/img/client2.svg" alt="client2" height="97" width="129">
            <img src="../assets/img/client3.png" alt="client3" height="95" width="95">
            <img src="../assets/img/client4.png" alt="client4" height="62" width="130">
            <img src="../assets/img/client5.png" alt="client5" height="25" width="130">
        </div>
    </div>
</template>
  
<script>
import sliderComponent from './sliderComponent'
export default ({
    components: {
        sliderComponent
    },
    data() {
        return {
            quvotes: [
                {
                    id: 1,
                    title: "1Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et labore et dolore magna aliqua.",
                    author: "Khaksarmadani / CEO"
                },
                {
                    id: 2,
                    title: "2Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et labore et dolore magna aliqua. ",
                    author: "Khaksarmadani / CMO"
                },
                {
                    id: 3,
                    title: "3Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et labore et dolore magna aliqua. ",
                    author: "Khaksarmadani / SEO"
                },
            ]
        }
    },
})
</script>
  
<style scoped>
#secondComponent {
    height: 100vh;
    width: 100%;
    overflow: hidden;
    position: relative;
}

.secondComponent__slaiderComponent {
    display: flex;
    position: absolute;
    height: 50%;
    width: 80%;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -50%);
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.secondComponent__slaiderComponent img {
    width: 20px;
    height: 20px;
    flex-shrink: 0;
    margin-bottom: 150px;
    margin-top: 10px;

}

.secondComponent__slaiderComponent>>>.sliderComponent__slideImage {
    width: 60%;
    height: 50%;
    top: 50%;
    left: 50%;
    margin-right: -50%;
    transform: translate(-50%, -50%);
    position: absolute;
}

.sliderComponent>>>.slide-enter-active,
.sliderComponent>>>.slide-leave-active {
    transition: opacity 0.5s;

}

.sliderComponent>>>.slide-enter-from {
    transform: translateX(100%);
    transition: transform 0.8s;

}

.sliderComponent>>>.slide-leave-to {
    opacity: 0;

}

.secondComponent__slaiderComponent>>>.sliderComponent__slideImage_title {
    display: block;
    color: #2A2A2A;
    text-align: center;
    font-family: Work Sans;
    font-size: 20.869px;
    font-style: normal;
    font-weight: 500;
    line-height: 33.201px;
    /* 159.091% */
}

.secondComponent__slaiderComponent>>>.sliderComponent__slideImage_author {
    margin-top: 70px;
    display: block;
    color: #0159B1;
    text-align: center;
    font-family: Roboto;
    font-size: 15.178px;
    font-style: normal;
    font-weight: 400;
    line-height: 27.51px;
    /* 181.25% */
    letter-spacing: 0.474px;
}

.secondComponent__slaiderComponent>>>.sliderComponent__slideImage_circleContainer {
    display: flex;
    width: 60%;
    height: 50%;
    top: 150%;
    left: 50%;
    margin-right: -50%;
    transform: translate(-50%, -50%);
    position: absolute;
    justify-content: center;
}

.secondComponent__slaiderComponent>>>.sliderComponent__slideImage_circle {
    display: block;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background-color: #000000;
    margin: 10px;
}
.secondComponent__slaiderComponent>>>.sliderComponent__slideImage_circle_Outer-circle {
    display: block;
    border: #000000 5px;
    border-radius: 50%;
    margin: 10px;
}

.secondComponent__slaiderComponent>>>.controls {
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: space-between;
    position: absolute;
    left: 0%;
}

.secondComponent__slaiderComponent>>>.btnSlide {
    align-self: center;
    height: 100%;
    background: transparent;
    color: #0159B1;
    font-size: 60px;
    cursor: pointer;
    border: none;
}


.secondComponent_brands {
    display: flex;
    justify-content: center;
    align-items: center;
    height: auto;
    width: 100%;
    position: absolute;
    bottom: 5%;
    left: 50%;
    transform: translateX(-50%);
    padding: 20px;
}

.secondComponent_brands img {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 20px;
    flex-shrink: 0;
}
</style>