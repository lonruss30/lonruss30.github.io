<template>
    <div class="footer-main-wrapper">
        <div class="footer-main-container">
            <div class="container-group">
                <div class="logo">
                    <h2 @click="scrollTo()">lonrussel</h2>
                </div>
                <div v-for="items in informationData.InfoArray" v-bind:key="items" class="contact-info">
                    <p class="title">Contact me</p>
                    <div class="content">
                        <p><i class="fa-solid fa-phone-volume icon-class"></i>{{ items.ContactNumber }}</p>
                        <p><i class="fa-solid fa-inbox icon-class"></i>{{ items.Email }}</p>
                    </div>
                    <div class="resume-div">
                        <p class="title">Resume</p>
                        <a href="./LonRusselQuintoResume2023.pdf" download target="_blank"><i class="fa-solid fa-paperclip icon-class"></i>My Resume</a>
                    </div>
                    
                    
                    
                </div>
                <div v-for="(items, index) in informationData.InfoArray" v-bind:key="items" class="social-info">
                    <p class="title">Socials</p>
                    <a :href="[informationData.InfoArray[index].GithubLink]" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-github icon-class"></i></a>
                    <a :href="[informationData.InfoArray[index].LinkedInLink]" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-linkedin icon-class"></i></a>
                    <a :href="[informationData.InfoArray[index].TwitterLink]" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-twitter icon-class"></i></a>
                    <a :href="[informationData.InfoArray[index].FacebookLink]" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-facebook icon-class"></i></a>     
                </div>
            </div>
            <div class="copyright-shit">
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
    methods:{
        scrollTo(){
            window.scrollTo(0, 0);
        }
    }
}
</script>
<style scoped>
    .footer-main-wrapper{
        height: 350px;
        background-color: #395144;
        color: #F0EBCE;
    }

    .footer-main-container{
        height: 100%;
    }

    .container-group{
        height: 70%;
        display: flex;
        justify-content: center;
        padding: 30px 30px 0 30px;
        text-align: left;
    }
    .container-group .title{
        font-size: larger;
        font-weight: 500;
    }

    .logo{
        padding-left: 120px;
    }
    .contact-info{
        padding-left: 90px;
    }
    .logo,.contact-info,.social-info{
        width: 30%;
    }

    .logo h2{
        font-size: 32px;
        margin-top: -12px;
        cursor: pointer;
        transition: all 0.5s ease-in-out;
        transform: scale(1);
    }

    .logo h2:hover{
        transform: scale(1.1);
    }
    .contact-info .content{
        padding-top: 15px;
        padding-bottom: 15px;
        font-size: 16px;
    }

    .contact-info .content .icon-class {
        padding-right: 10px;
    }

    .contact-info .resume-div .icon-class{
        padding-right: 10px;
    }

    .resume-div a{
        color: inherit;
        text-decoration: underline;
    }
    .social-info a{
        text-decoration: none;
        color: inherit;
    }
    .social-info .icon-class{
        transition: all 0.5s ease-in-out;
        transform: scale(1);
    }

    .social-info .icon-class:hover{
        color: #AA8B56;
        transform: scale(1.2);
    }
    .social-info .icon-class{
        font-size: 28px;
        padding: 15px 15px 0 0;
        cursor: pointer;
    }

    .copyright-shit{
        height: 30%;
        padding-top: 50px;
    }
</style>