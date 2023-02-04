<template>
    <div class="about-wrapper">
        <div class="about-main-container">
            <div class="container-one">
                <div class="profile-section">
                    <img src="../assets/profilepic.jpg" alt="">
                </div>
                <div class="social-links">
                        <div class="link">
                            <a href=""><img src="../assets/Github_black.png" alt=""></a>
                        </div>
                        <div class="link">
                            <a href=""><img src="../assets/LinkedIN_black.png" alt=""></a>
                        </div>
                        <div class="link">
                            <a href=""><img src="../assets/Youtube_black.png" alt=""></a>
                        </div>
                </div>
            </div>
            <div class="container-two">
                <div class="about-me">
                    <h1>Hi, I'm Lon Russel</h1>
                    <p>I am a Junior .NET Developer with 6 months of experience, 
                        who recently graduated in August 2022. With a passion for Web Development, 
                        I have been exploring HTML, CSS, and Vue.js, and I am eager to expand my knowledge 
                        by diving into Laravel soon. My ultimate goal is to use my technical skills to create 
                        beautiful, user-friendly websites and web applications that make a positive impact on 
                        businesses and individuals alike. I am excited to continue my professional growth as a 
                        Web Developer and work with a team that shares my passion for innovation and creativity</p>
                </div>
            </div>
        </div>
    </div>
    
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .about-wrapper{
        padding-top: 100px;
        width: auto;
        display: flex;
        justify-content: center;
        color: #4E6C50;
    }
    .about-main-container{
        display: flex;
        flex-direction: row;
        border-radius: 15px;
        width: 80%;
        background-color: rgb(205, 205, 165);
    }
    .container-one{
        padding: 3%;
        width: 30%;
        border-radius: 15px;
    }
    
    .profile-section{
        padding-top: 25px;
        padding-bottom: 25px;
    }
    .profile-section img{
        height: 15em;
        border-radius: 15%;
    }
    
    .social-links{
        display: flex;
        flex-direction: row;
        justify-content: center;
    }
    .link{
        margin-left: 5%;
        margin-right: 5%;
    }
    .link a{
        font-size: .50rem;
        text-decoration: none;
        color: #4E6C50;
        display: flex;  
        flex-direction: row;
    }
    .link a img{
        height: 25px;
        align-self: center;
    }
    .container-two{
        margin: 3.5%;
        width: 70%;
    }
    .about-me{
        text-align: justify;
        
    }

    @media only screen and (max-width: 950px){
        .main-container{
            width: 95%;
        }
        
    }
</style>