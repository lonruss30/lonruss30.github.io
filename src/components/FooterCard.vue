<template>
    <div class="footer-main-wrapper">
        <div class="footer-main-container">
            <div class="container-group">
                <div v-for="items in informationData.InfoArray" v-bind:key="items" class="contact-info">
                    <p>Contact me</p>
                    <p>{{ items.ContactNumber }}</p>
                    <p>{{ items.Email }}</p>
                </div>
                <div v-for="items in informationData.InfoArray" v-bind:key="items" class="social-info">
                    <p>Connect with me through these socials</p>
                </div>
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
    }
}
</script>
<style scoped>
    .footer-main-wrapper{
        height: 200px;
        background-color: #395144;
        color: #F0EBCE;
    }

    .footer-main-container{
        height: 100%;
    }

    .container-group{
        display: flex;
        justify-content: center;
    }
</style>