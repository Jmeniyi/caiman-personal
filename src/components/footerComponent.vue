<template>
    <div class="footerComponent">
        <div class="footerComponent__CTA">
            <div class="footerComponent__CTA_label">
                <p>Do you have any project for us?</p>
                <h1>Leave your email and we will contact you as soon as possible</h1>
            </div>
            <div class="footerComponent__CTA_input">
                <input placeholder="Your email">
                <button>Send</button>
            </div>
        </div>
        <div class="footerComponent__contacts">
            <div class="footerComponent__contacts_leftSide">
                <div class="footerComponent__contacts_leftSide_nav">
                    <div class="footerComponent__contacts_leftSide_nav_list">
                        <ul class="footerComponent__contacts_leftSide_nav_list_ul">
                            <li><a @click="scrollTo('firstComponent')">Home</a></li>
                            <li><a @click="scrollTo('secondComponent')">About us</a></li>
                            <li><a @click="scrollTo('thirdComponent')">Our works</a></li>
                        </ul>
                    </div>
                </div>
                <div class="footerComponent__contacts_leftSide_logo">
                    <p>An<br />na</p>
                    <h2>©2021 </h2>
                    <h1>ANNA</h1>
                    <h2>. All Rights Reserved</h2>
                </div>
            </div>
            <div class="footerComponent__contacts_rightSide">
                <h1>(303) 555-0105, (303) 785-0105</h1>
                <h2>anna@info.com</h2>
                <h1>2972 Westheimer Rd. Santa Ana,<br/> Illinois 85486</h1>
                <ul class="footerComponent__contacts_rightSide_btnslist" style="list-style-type: none;">
                    <li>

                        <a href="https://www.instagram.com/">
                            <img src="../assets/img/logo-instagram.svg" alt="Instagram">
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
.footerComponent {
    height: 100vh;
    width: 100%;
    padding-inline: 5%;
}

.footerComponent__CTA {
    height: 50%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.footerComponent__CTA_label {
    position: absolute;
    align-self: flex-start;
    width: 40%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.footerComponent__CTA_label p {
    color: #2A2A2A;
    font-family: Work Sans;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: 38px;
    letter-spacing: 0.5px;
    margin-bottom: 20px;
}

.footerComponent__CTA_label h1 {
    opacity: 0.5;
    color: #2A2A2A;
    /* body_text */
    font-family: Roboto;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 29px;
    /* 181.25% */
    letter-spacing: 0.5px;
    margin-bottom: 20px;
}

.footerComponent__CTA_input {
    position: absolute;
    align-self: flex-end;
    width: 40%;
    display: flex;
    align-items: center;
}

.footerComponent__CTA_input input {
    align-self: flex-start;
    width: 60%;
    height: 30px;
    flex-shrink: 0;
    border: none;
    border-bottom: solid 1px;
}

.footerComponent__CTA_input input::placeholder {
    color: #2A2A2A;
    font-family: Roboto;
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 29px;
    letter-spacing: 0.5px;
    padding: 10px;
}

.footerComponent__CTA_input button {
    color: #0159B1;
    font-family: Roboto;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: 29px;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    background-color: inherit;
    border: none;
    border-bottom: solid 1px;
    border-color: #2A2A2A;
}

.footerComponent__contacts {
    height: 50%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-bottom: 20px;
}

.footerComponent__contacts_leftSide {
    position: absolute;
    align-self: flex-start;
    width: 60%;
    height: 50%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.footerComponent__contacts_leftSide_nav {
    height: 50%;
    position: absolute;
    left: 10%;
    display: flex;
    align-items: center;
}


.footerComponent__contacts_leftSide_nav_list_ul li {
    color: #2A2A2A;
    font-family: Roboto;
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 25px;
    letter-spacing: 0.5px;
    list-style-type: none;
    display: inline-block;
    margin-right: 40px;
}

.footerComponent__contacts_leftSide_logo {
    position: absolute;
    bottom: 0px;
    left: 10%;
    padding-bottom: 20px;
}

.footerComponent__contacts_leftSide_logo p {
    color: #0159B1;
    font-family: Abril Fatface;
    font-size: 30px;
    font-style: normal;
    font-weight: 400;
    line-height: 30px;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    margin-bottom: 10px;
}

.footerComponent__contacts_leftSide_logo h1 {
    color: #0159B1;
    font-family: Roboto;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 25px;
    letter-spacing: 0.5px;
    display: inline;
}

.footerComponent__contacts_leftSide_logo h2 {
    color: #A7A7A7;
    font-family: Roboto;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 25px;
    letter-spacing: 0.5px;
    display: inline;
}

.footerComponent__contacts_rightSide {
    width: 20%;
    height: 50%;
    display: flex;
    position: absolute;
    align-self: flex-end;
    align-items: center;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.footerComponent__contacts_rightSide h1 {
    color: #888;
    font-family: Roboto;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 29px;
    letter-spacing: 0.5px;
    padding-bottom: 10px;
}

.footerComponent__contacts_rightSide h2 {
    color: #0159B1;
    font-family: Roboto;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 29px;
    letter-spacing: 0.5px;
    padding-bottom: 10px;
}


.footerComponent__contacts_rightSide_btnslist li {
    display: inline-block;
    padding-bottom: 10px;
    
}
.footerComponent__contacts_rightSide_btnslist img {
    width: 25px;
    height: 25px;
    flex-shrink: 0;
}

</style>А