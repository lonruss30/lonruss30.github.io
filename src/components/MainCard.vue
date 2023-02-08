<template>
    <div class="about-wrapper">
        <div class="about-main-container">
            <div class="container-one">
                <div class="profile-section">
                    <img src="../assets/profilepic.jpg" alt="">
                </div>
            </div>
            <div class="container-two">
                <div v-for="(items) in informationData.InfoArray" v-bind:key="items" class="about-me">
                    <h4>About Me</h4>
                    <p>{{ items.About }}</p>
                </div>
                <div class="flex-container">
                    <div class="about-buttons">
                        <h5 class="about-links active-link" @click="openTab('skills')">Skills</h5>
                        <h5 class="about-links" @click="openTab('experiences')">Experiences</h5>
                        <h5 class="about-links" @click="openTab('education')">Education</h5>
                    </div>
                    <div v-if="tabName == 'skills'" class="skills-tab">
                        <div v-for="(items, index) in informationData.Technologies" v-bind:key="items"
                            class="skills-content active-tab">
                            <i :class="[informationData.Technologies[index].Icon]"></i>
                            <p>{{ items.Title }}</p>
                        </div>
                    </div>
                    <div v-if="tabName == 'experiences'" class="experiences-tab">
                        <div v-for="(items) in informationData.ExperienceArray" v-bind:key="items"
                            class="experiences-content">
                            <strong>{{ items.Company }}</strong>
                            <p>{{ items.Date }}</p>
                            <p><strong>Role:</strong> {{ items.Role }}</p>
                        </div>
                    </div>
                    <div v-if="tabName == 'education'" class="education-tab">
                        <div v-for="(items) in informationData.EducationArray" v-bind:key="items"
                            class="education-content">
                            <strong>{{ items.School }}</strong>
                            <p>{{ items.EducationalLevel }} {{ items.Date }}</p>
                            <p>{{ items.Course }}</p>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>

</template>

<script>
import infoData from "../data/info.json"
var tabLinks = document.getElementsByClassName("about-links");
export default {
    data() {
        return {
            tabName: 'skills',
            informationData: infoData
        }

    },
    methods: {

        openTab(tabNameAssign) {
            Array.prototype.forEach.call(tabLinks, (tablink) => {
                tablink.classList.remove("active-link");
            });
            event.currentTarget.classList.add("active-link");
            this.tabName = tabNameAssign;
        }
    }
}
</script>

<style scoped>
/* Galaxy Fold */
.about-wrapper {
    width: 100%;
    color: #4E6C50;
    height: 100%;
}

.about-main-container {
    padding-top: 30px;
    width: 100%;
}

.container-one {
    height: 100%;
    width: 100%;
}

.profile-section {
    padding-bottom: 10px;
}

.profile-section img {
    height: 150px;
    width: 150px;
}

@media only screen and (min-width: 280px) {
    .profile-section img {
        border-radius: 5%;
        object-fit: cover;
        object-position: 100% 0;
    }
}

.container-two {
    height: 100%;
}

.container-two h4 {
    margin-top: 10px;
    margin-bottom: 10px;
    color: #395144;
}

.about-me,
.about-buttons {
    text-align: left;
}

.about-me p {
    text-indent: 40px;
    margin-top: 0;
    font-size: 14px;
    font-family: 'Roboto', sans-serif;
    text-align: justify;
}

.about-buttons {
    display: flex;
    padding-top: 20px;
}

.about-links {
    font-family: 'Poppins', sans-serif;
    color: #395144;
    margin-top: 5px;
    margin-right: 20px;
    position: relative;
    cursor: pointer;
}

.about-links::after {
    content: '';
    width: 0;
    height: 3px;
    background: #AA8B56;
    position: absolute;
    left: 0;
    bottom: -8px;
    transition: 0.5s;
}

.about-links.active-link::after {
    width: 60%;
}

.skills-tab {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding-top: 45px;
    gap: 20px;
}

.skills-content {
    /* background-color: rgba(170, 139, 86, 0.34); */
    background-color: rgba(240, 235, 206, 0.74);
    height: 100px;
    width: 100px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.08);
}

.icon-class {
    color: #395144;
    font-size: 36px;
    padding: 20px 0 0 0;
}

.skills-content p {
    margin: 10px 0;
    font-size: 12px;
}

.experiences-tab {
    padding-top: 35px;
}

.experiences-content {
    text-align: left;
    height: 90px;
    font-size: 10px;
    /* background-color: rgba(170, 139, 86, 0.34); */
    background-color: rgba(240, 235, 206, 0.74);
    margin-top: 10px;
    padding: 13px 0 5px 15px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.08);
}

.experiences-content strong {
    color: #395144;
}

.experiences-content p {
    margin: 5px 0;
    font-size: 10px;
}

.education-tab {
    padding-top: 35px;
}

.education-content {
    text-align: left;
    height: 90px;
    font-size: 10px;
    /* background-color: rgba(170, 139, 86, 0.34); */
    background-color: rgba(240, 235, 206, 0.74);
    margin-top: 10px;
    padding: 13px 5px 5px 15px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.08);
}

.education-content strong {
    color: #395144;
}

.education-content p {
    font-size: 10px;
}

/* Iphone XR */
@media only screen and (min-width: 410px) {

    .container-two h4 {
        font-size: large;
    }

    .about-me p {
        font-size: 16px;
    }

    .about-links {
        font-size: medium;
    }

    /* Skills Tab */
    .skills-content {
        height: 150px;
        width: 150px;
    }

    .icon-class {
        color: #395144;
        font-size: 48px;
        padding: 30px 0 0 0;
    }

    .skills-content p {
        margin: 15px 0;
        font-size: 16px;
    }

    /* Experiences Tab */
    .experiences-content {
        height: 110px;
        font-size: 14px;
        padding: 13px 0 5px 15px;
    }

    .experiences-content p {
        margin: 5px 0;
        font-size: 14px;
    }

    .education-content {
        height: 110px;
        font-size: 14px;
        padding: 13px 10px 10px 15px;
    }

    .education-content p {
        font-size: 14px;
    }

}

/* Ipad Mini */
@media only screen and (min-width: 760px) {
    .profile-section img {
        height: 350px;
        width: 350px;

    }

    .container-two h4 {
        font-size: larger;
    }

    .about-me p {
        font-size: 18px;
    }

    .about-links {
        font-size: large;
    }

    /* Skills Tab */
    .skills-content {
        height: 150px;
        width: 150px;
    }

    .icon-class {
        color: #395144;
        font-size: 48px;
        padding: 30px 0 0 0;
    }

    .skills-content p {
        margin: 15px 0;
        font-size: 16px;
    }

    /* Experiences Tab */
    .experiences-content {
        height: 110px;
        font-size: 14px;
        padding: 13px 0 5px 15px;
    }

    .experiences-content p {
        margin: 5px 0;
        font-size: 14px;
    }

    .education-content {
        height: 110px;
        font-size: 14px;
        padding: 13px 10px 10px 15px;
    }

    .education-content p {
        font-size: 14px;
    }

}

/* Nest Hub */
@media only screen and (min-width: 1000px) {
    .about-main-container {
        padding-top: 60px;
        width: 100%;
    }

    .profile-section img {
        object-position: 0 9%;
        border-radius: 5%;
    }

    .container-one {
        height: initial;
    }

    .container-two {
        padding-top: 20px;
        height: initial;
    }

    .container-two h4 {
        font-size: x-large;
    }

    .about-me {
        width: 100%;
        height: initial;
        padding-bottom: 40px;
    }

    .about-me p {
        font-size: 20px;
    }

    .about-links {
        font-size: larger;
    }

    .about-main-container {
        height: 100%;
    }

    .flex-container {
        width: 100%;
    }

    .about-buttons {
        padding: 0;
        align-content: left;
        justify-content: left;
    }

    .about-links {
        text-align: center;
        margin-left: 0;
    }

    /* Skills Tab */

    .skills-tab {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        padding: 45px 20px 0 20px;
        gap: 20px;
    }

    .skills-content {
        /* background-color: rgba(170, 139, 86, 0.34); */
        background-color: rgba(240, 235, 206, 0.74);
        height: 120px;
        width: 120px;
        border-radius: 10px;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.08);
    }

    .icon-class {
        color: #395144;
        font-size: 40px;
        padding: 20px 0 0 0;
    }

    .skills-content p {
        margin: 15px 0;
        font-size: 16px;
    }

    /* Experiences Tab */
    .experiences-content {
        height: 120px;
        font-size: 16px;
        padding: 20px 0 5px 15px;
    }

    .experiences-content p {
        font-size: 16px;
    }

    /* Education Tab */
    .education-content {
        height: 120px;
        font-size: 16px;
        padding: 20px 10px 10px 15px;
    }

    .education-content p {
        font-size: 16px;
    }

}

@media only screen and (min-width: 1150px) {
    .profile-section img {
        object-fit: cover;
        object-position: 0 9%;
        border-radius: 5%;
    }
}
</style>