<template>
    <div class="maintenance-main-wrapper">
        <div class="maintenance-main-container">
            <i class="fa-solid fa-person-digging"></i>
            
            <h2>Website is under maintenance</h2>

            <p>This website is currently undergoing scheduled maintenance. We should be back shortly.</p>
        </div>
        <div class="maintenance-contact-container">
            <p>While we're away, connect with us</p>
            <a href="https://github.com/lonruss30" target="_blank"><i class="fa-brands fa-github"></i></a>
            <a href="https://www.linkedin.com/in/lonrusselquinto/" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
            <p>Or submit an email</p>
            <button @click="callModal"><i class="fa-solid fa-envelope"></i></button>
        </div>
        <PopupModal
            v-if="isShowModal" 
            @close="close"
        />  
    </div>
</template>
<script>

import PopupModal from './PopupModal.vue';
export default {
        data(){
            return{
                isShowModal: false
            }
            
        },
        components:{
            PopupModal
        },
        methods: {
            close(){
                this.isShowModal = false;
            },
            callModal(){
                this.isShowModal = true;
            }
        },
        beforeMount(){
            setTimeout(()=> this.isShowModal = true, 4000);
        }
}
</script>
<style scoped>
    *{
        margin: 0;
        padding: 0;
    }

    .maintenance-main-wrapper{
        min-height: 100vh;
    }
    .maintenance-main-container{
        padding-top: 15%;
    }
    .fa-person-digging{
        height: 100px;
    }
    .maintenance-contact-container{
        margin: 50px;
    }
    .maintenance-contact-container a, button{
        color: inherit;
        border: none;
        background: none;
        cursor: pointer;
    }
    .maintenance-contact-container .fa-github,.fa-linkedin,.fa-envelope{
        height: 25px;
        margin: 5px;
    }
    
</style>