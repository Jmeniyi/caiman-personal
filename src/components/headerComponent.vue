<template>
    <div class="headerComponent">
        <div class="headerComponent__logoContainer">
            <p class="headerComponent__logoContainer_Logo">Drip</p>
        </div>
        <div class="headerComponent__list">
            <ul class="headerComponent__list_ul">
                <li><a @click="scrollTo('firstComponent')">Home</a></li>
                <li><a @click="scrollTo('secondComponent')">About us</a></li>
                <li><a @click="scrollTo('thirdComponent')">Our works</a></li>
                <li><a @click="scrollTo('footerComponent')">Contacts</a></li>
            </ul>
        </div>
        <div class="headerComponent__rightMenu">
            <p class="headerComponent__rightMenu_singIn"> Sing in </p>
            <img class="headerComponent__rightMenu_navBurger" src="../assets/img/Menu.svg" alt="navBurger">
        </div>
    </div>
</template>

<script>
export default {
  methods: {
    scrollTo(sectionId) {
      const element = document.getElementById(sectionId);
      element.scrollIntoView({ behavior: 'smooth' });
    }
  }
};
</script>

<style scoped>
.headerComponent {
    height: 100px;
    width: 100%;
    flex-shrink: 0;
    border: 1px solid #0159B1;
    background: #FFF;
    display: flex;
    align-items: center;
    white-space: nowrap;
}

.headerComponent__logoContainer {
    width: 120px;
    height: 40px;
    flex-shrink: 0;
    margin: auto 0px auto 60px;
}

.headerComponent__logoContainer_Logo {
    color: #0159B1;
    text-align: center;
    font-family: Abril Fatface;
    font-size: 50.824px;
    font-style: normal;
    font-weight: 400;
    line-height: 42.353px;
    /* 83.333% */
    letter-spacing: 1.059px;
    text-transform: uppercase;

}

.headerComponent__list {
    width: 70px;
    height: 30px;
    white-space: nowrap;
    display: inline-block;
    margin-left: 90px;
}   

.headerComponent__list_ul li {
    color: #0159B1;
    font-family: Roboto;
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: 30px;
    letter-spacing: 0.5px;
    list-style-type: none;
    display: inline-block;
    margin-right: 40px;
}

.headerComponent__rightMenu {
    position: relative;
    left: auto;
    right: 100px;
    margin-left: auto;
    width: 55px;
    height: 30px;
    display: flex;
    align-items: center;
}

.headerComponent__rightMenu_singIn {
    color: #303030;
    font-family: Roboto;
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 30px;
    letter-spacing: 0.5px;
    margin-right: 30px;
}

.headerComponent__rightMenu_navBurger {
    width: 25px;
    height: 10px;
    margin-right: 40px;
}</style>