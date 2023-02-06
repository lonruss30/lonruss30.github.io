<template>
    <div class="about-wrapper">
        <div class="about-main-container">
            <div class="container-one">
                <div class="profile-section">
                    <img src="../assets/profilepic.jpg" alt="">
                </div>
            </div>
            <div class="container-two">
                <div class="about-me">
                    <h1>About Me</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                        Dolore consectetur unde ipsam veritatis maiores delectus fuga voluptatem. 
                        Magni dignissimos quos tempora repellendus illum in, voluptatum maiores consectetur aut, provident laborum.
                    </p>
                </div>
                <div class="about-buttons">
                    <h5 class="about-links active-link" @click="openTab('skills')">Skills</h5 >
                    <h5 class="about-links" @click="openTab('experience')">Experience</h5>
                    <h5 class="about-links" @click="openTab('education')">Education</h5>
                </div>
                <div v-if="tabName == 'skills'" class="skills-tab">
                    <div v-for="(items, index) in informationData.Technologies" v-bind:key="items" class="skills-content active-tab">
                        <i :class="[informationData.Technologies[index].Icon]">{{items.Icon}}</i>
                        <p>{{items.Title}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
</template>

<script>
import infoData from "../data/info.json"
export default {
    data(){
            return{
                tabName: 'skills',
                informationData: infoData
            }
            
    },
    methods:{
        openTab(tabNameAssign){
            this.tabName = tabNameAssign;
            console.log(this.tabName);
            console.log(this.informationData.Technologies)
        }
    }
}
</script>

<style scoped>
    .about-wrapper{
        padding-top: 100px;
        width: 100%;
        display: flex;
        justify-content: center;
        color: #4E6C50;
        height: 600px;
    }
        .about-main-container{
            padding-top: 50px;
            width: 100%;
            display: flex;
            gap: 1px;
            flex-direction: row;
            align-items: center;
            justify-content: center;
        }
            .container-one{
                width: 30%;
                height: 100%;
                padding: 0;
            }
                .profile-section img{
                    height: 350px;
                    border-radius: 5%;
                }
            .container-two{
                height: 100%;
                width: 70%;
                padding-right: 30px;
            }
                .container-two h1{
                    margin-top: 10px;
                    margin-bottom: 10px;
                    color: #395144;
                }
                .about-me,.about-buttons{
                    text-align: left;
                }
                    .about-me p{
                        margin-top: 0;
                        font-family: 'Roboto', sans-serif;
                    }
                    .about-buttons{
                        display: flex;
                        padding-top: 20px;
                    }

                        .about-links{
                            font-family: 'Poppins', sans-serif;
                            color: #395144;
                            margin-top: 5px;
                            margin-right: 50px;
                            position: relative;
                            cursor: pointer;
                        }
                        .about-links::after{
                            content: '';
                            width: 0;
                            height: 3px;
                            background: #AA8B56;
                            position: absolute;
                            left: 0;
                            bottom: -8px;
                            transition: 0.5s;
                        }
                        .about-links.active-link::after{
                            width: 60%;
                        }
                    .skills-tab{
                        display: flex;
                        justify-content: center;
                        padding-top: 35px;
                        gap: 20px;
                    }
                        .skills-content{
                            background-color: rgba(170, 139, 86, 0.34);
                            height: 80px;
                            width: 80px;
                            border-radius: 10px;
                            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.08);
                        }
                            .skills-content p{
                                margin: 10px 0;
                                font-size: 12px;
                                
                            }
                            .icon-class{
                                font-size: 32px;
                                padding: 10px 0 0 0;
                            }

    /* @media only screen and (max-width: 950px){
        .about-main-container{
            width: 95%;
        }
        
    } */
</style>