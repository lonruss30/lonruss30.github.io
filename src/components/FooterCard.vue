<template>
    <div class="footer-main-wrapper">
        <div class="footer-main-container">
            <div class="container-group">
                <div class="logo">
                    <h2 @click="scrollTo()">lonrussel</h2>
                </div>
                <div class="middle-group">
                    <div v-for="items in informationData.InfoArray" v-bind:key="items" class="contact-info">
                        <p class="title">Contact me</p>
                        <div class="content">
                            <p class="content-p"><i class="fa-solid fa-phone-volume icon-class"></i>{{
                                items.ContactNumber
                            }}</p>
                            <p class="content-p"><i class="fa-solid fa-inbox icon-class"></i>{{ items.Email }}</p>
                        </div>
                        <div class="resume-div">
                            <p class="title">Resume</p>
                            <div class="content-a">
                                <a href="./LonRusselQuintoResume2023.pdf" download target="_blank"><i
                                        class="fa-solid fa-paperclip icon-class"></i>My CV</a>
                            </div>

                        </div>
                    </div>
                    <div v-for="(items, index) in informationData.InfoArray" v-bind:key="items" class="social-info">
                        <p class="title">Socials</p>
                        <div class="link-main-group">
                            <div class="link-group-1">
                                <a :href="[informationData.InfoArray[index].GithubLink]" target="_blank"
                                    rel="noopener noreferrer"><i class="fa-brands fa-github icon-class"></i></a>
                                <a :href="[informationData.InfoArray[index].LinkedInLink]" target="_blank"
                                    rel="noopener noreferrer"><i class="fa-brands fa-linkedin icon-class"></i></a>
                            </div>
                            <div class="link-group-2">
                                <a :href="[informationData.InfoArray[index].TwitterLink]" target="_blank"
                                    rel="noopener noreferrer"><i class="fa-brands fa-twitter icon-class"></i></a>
                                <a :href="[informationData.InfoArray[index].FacebookLink]" target="_blank"
                                    rel="noopener noreferrer"><i class="fa-brands fa-facebook icon-class"></i></a>
                            </div>
                        </div>

                    </div>
                </div>
            </div>
            <div class="copyright-div">
                <p>Developed by <strong>Lon Russel</strong> <i class="fa-regular fa-copyright"></i> 2023</p>
            </div>

        </div>
    </div>
</template>
<script>
import infoData from "../data/info.json"
export default {
    data() {
        return {
            informationData: infoData
        }
    },
    methods: {
        scrollTo() {
            window.scrollTo(0, 0);
        }
    }
}
</script>
<style scoped>
.footer-main-wrapper {
    background-color: #395144;
    color: #F0EBCE;
}

.footer-main-container {
    height: 100%;
}

.logo h2{
    cursor: pointer;
}

.middle-group {
    margin: 0 5%;
}

.contact-info {
    margin: 0 5%;
}

.social-info {
    margin: 0 5%;
}

.social-info a:hover .icon-class{
    color: #AA8B56;
    transition: all 0.3s ease-in-out;
    transform: scale(1.2);
}

.contact-info,
.social-info,
a {
    color: inherit;
}


@media (min-width: 334px) {
    .footer-main-wrapper {
        height: 300px;
    }

    .container-group {
        height: 80%;
    }

    .logo {
        padding-top: 10px;
    }

    .middle-group {
        display: flex;
    }

    .contact-info {
        width: 60%;
    }

    .social-info {
        width: 40%;
    }

    .contact-info .title,
    .social-info .title {
        font-size: small;
        font-weight: 600;
        padding-top: 30px;
        padding-bottom: 5px;
    }

    .contact-info,
    .social-info,
    a {
        font-size: 12px;
    }

    .contact-info .content-p {
        text-align: left;
        font-size: 12px;
        margin-left: 10%;
    }

    .contact-info .icon-class {
        padding-right: 10px;
    }

    .contact-info .resume-div .content-a {
        text-align: left;
        margin-left: 10%;
    }

    .social-info .icon-class {
        font-size: 28px;
        padding: 5px;
    }

    .copyright-div {
        height: 20%;
        padding-top: 20px;
    }

    .copyright-div p {
        font-size: small;
    }

}

@media (min-width: 558px) {
    .footer-main-wrapper {
        height: 400px;
    }

    .logo {
        padding-top: 20px;
    }

    .logo h2 {
        font-size: 28px;
    }

    .contact-info .title,
    .social-info .title {
        font-size: medium;
        font-weight: 600;
        padding-top: 40px;
        padding-bottom: 10px;
    }

    .contact-info,
    .social-info,
    a {
        font-size: 14px;
    }

    .contact-info .content-p {
        text-align: left;
        font-size: 14px;
        margin-left: 20%;
    }

    .contact-info .icon-class {
        padding-right: 10px;
    }

    .contact-info .resume-div .content-a {
        text-align: left;
        margin-left: 20%;
    }

    .social-info .icon-class {
        font-size: 28px;
        padding: 5px;
    }

    .copyright-div {
        height: 20%;
        padding-top: 25px;
    }

    .copyright-div p {
        font-size: small;
    }
}

@media screen and (min-width: 1104px) {

    .footer-main-wrapper {
        height: 350px;
    }

    .container-group {
        display: flex;
        align-content: center;
        justify-content: center;
        padding: 30px 30px 0 30px;
    }

    .logo {
        padding-top: 0;
        padding-left: 120px;
        width: 30%;
    }

    .logo h2 {
        font-size: 32px;
        text-align: left;
        margin-top: -12px;
    }

    .middle-group {
        width: 60%;
        flex-direction: row;
        text-align: left;
        margin: 0%;
    }

    .contact-info {
        margin: 0%;
        padding-left: 90px;
        width: 50%;
    }

    .social-info {
        margin: 0%;
        width: 50%;
    }

    .contact-info .title,
    .social-info .title {
        font-size: 19.2px;
        font-weight: 500;
        padding-top: 0;
        padding-bottom: 0;
    }

    .contact-info,
    .social-info,
    a {
        font-size: 16px;
    }

    .contact-info .content {
        padding: 15px 0;
        font-size: 16px;
    }

    .contact-info .content-p {
        text-align: left;
        font-size: 16px;
        margin-left: 0;
    }

    .contact-info .icon-class {
        padding-right: 10px;
    }

    .contact-info .resume-div .icon-class {

        padding-top: 15px;
    }

    .contact-info .resume-div .content-a {
        text-align: left;
        margin-left: 0;
    }
    .link-main-group{
        display: flex;
    }

    .social-info .icon-class {
        font-size: 28px;
        padding: 5px;
    }

    .copyright-div {
        height: 20%;
        padding-top: 25px;
    }

    .copyright-div p {
        font-size: small;
    }
}
</style>