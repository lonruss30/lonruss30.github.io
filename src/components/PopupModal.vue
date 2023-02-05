<template>
    <div class="popup">
        <div class="popup-inner">
            <div class="email-form">
                <form action="https://formsubmit.co/qlonruss30@gmail.com" method="POST">
                    <h3>Send a message</h3>
                    <input type="hidden" name="_captcha" value="false">
                    <input type="hidden" name="_subject" value="New email from your portfolio!">
                    <div class="input-field">
                        <input type="email" name="email" placeholder="Email Address" required>
                    </div>
                    <div class="input-field">
                        <input type="text" name="name" placeholder="What's your name?" required>
                    </div>
                    <div class="input-field">
                        <textarea name="message" placeholder="Write your thoughts here..." rows="5" required></textarea>
                    </div>
                    <button class="btn-submit" type="submit"><span>Submit </span></button>
                </form>
            </div>
            <button @click="close" class="popup-close">
                Close
            </button>
        </div>
    </div>
</template>
<script>
export default {
    methods:{
        close(){
            this.$emit('close')
        }
    }
}
</script>
<style scoped>
    
    .popup{
        position: fixed;
        top:0;
        left: 0;
        right: 0;
        bottom: 0;
        
        background-color: rgba(0, 0, 0, 0.3);
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .popup .popup-inner{
        position: relative;
        height: 425px;
        width: 480px;
        border-radius: 15px;
        background-color: #395144;
        z-index: 99;
        padding: 32px;
    }
    .popup .popup-inner h3{
        text-align: left;
        padding-left: 40px;
        font-size: 1.35rem;
        color: #F0EBCE;
    }

    .input-field{
        padding-bottom: 20px;
    }
    input{
        height: 30px;
        padding: 5px 5px 5px 10px;
    }

    input, textarea{
        width: 80%;
        font-family: 'Poppins', sans-serif;
        border-radius: 10px;
        color: #395144;
        border: none;
        background-color: #F0EBCE;
        text-decoration: none;
    }
    textarea{
        text-align: start;
        resize: vertical;
        min-height: 100px;
        max-height: 160px;
        padding: 15px 5px 0px 10px;
    }

    .btn-submit span::after{
        content: '\00bb';
        position: absolute;
        opacity: 0;
        top: 0;
        right: -20px;
        transition: 0.5s;
    }
    .btn-submit,.popup-close{
        font-family: 'Poppins', sans-serif;
        cursor: pointer;
        font-size: .976rem;
        padding: 5px 10px 10px 10px;
    }

    .btn-submit{
        background-color: rgba(240, 235, 206, 0.92);
        border: 0;
        border-radius: 10px;
        height: 35px;
        width: 83%;
    }

    .btn-submit:hover{
        background-color: rgb(240, 235, 206);
        padding-left: 35px;
    }

    .btn-submit:hover span {
        padding-right: 25px;
    }

    .btn-submit:hover span::after {
        position:relative;
        opacity: 1;
        right: 0;
    }
    .popup-close{
        padding-top: 10px;
        background: transparent;
        border: 0;
        color: #F0EBCE;
    }
    
</style>