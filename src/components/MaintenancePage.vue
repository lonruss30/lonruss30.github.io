<template>
    <div class="maintenance-main-wrapper">
        <div class="maintenance-main-container">
            <i class="fa-solid fa-person-digging"></i>
            
            <h2>Website is under maintenance</h2>

            <p>This website is currently undergoing scheduled maintenance. We should be back shortly.</p>
        </div>
        <div class="maintenance-contact-container">
            <p>Connect with me</p>
            <a href="https://github.com/lonruss30" target="_blank"><i class="fa-brands fa-github"></i></a>
            <a href="https://www.linkedin.com/in/lonrusselquinto/" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
            <p>Or submit an email</p>
            <a href="" target="_blank"><i class="fa-solid fa-envelope"></i></a>
        </div>
        <div class="maintenance-email-modal">
            <div class="email-form">
                <form action="https://formsubmit.co/qlonruss30@gmail.com" method="POST">
                    <h3>Send a message</h3>
                    <input type="hidden" name="_captcha" value="false">
                    <input type="hidden" name="_subject" value="New email from your portfolio!">
                    <input type="email" name="email" placeholder="Email Address" required>
                    <input type="text" name="name" placeholder="What's your name?" required>
                    <textarea name="message" placeholder="Write your thoughts here" required></textarea>
                    <button type="submit">Send</button>
                </form>
            </div>
        </div>
        
    </div>
</template>
<script>
export default {
    
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
        padding-top: 17%;
    }
    .fa-person-digging{
        height: 100px;
    }
    .maintenance-contact-container{
        margin: 50px;
    }
    .maintenance-contact-container a{
        color: inherit;
    }
    .maintenance-contact-container .fa-github,.fa-linkedin,.fa-envelope{
        height: 25px;
        margin: 5px;
    }
    .maintenance-email-modal{
        height: 600px;
        width: 500px;
        border-radius: 15px;
        background-color: #395144;
    }
    .maintenance-email-modal h3{
        color: #F0EBCE;
    }
</style>