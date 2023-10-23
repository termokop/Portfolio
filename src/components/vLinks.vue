<script setup>

import IconSoloLearn from './icons/IconSoloLearn.vue'
import IconCodeWars from './icons/IconCodeWars.vue'
import IconGitHub from './icons/IconGitHub.vue'
import IconFacebook from './icons/IconFacebook.vue'
import IconTelegram from './icons/IconTelegram.vue'
import IconLinkedIn from './icons/IconLinkedIn.vue'
import IconGMail from './icons/IconGMail.vue'

</script>

<template>

    <div class="links">
        <h3>You can see my code here:</h3>
        <ul>
            <li>
                <a href="https://www.sololearn.com/profile/27120555" target="_blank"><IconSoloLearn></IconSoloLearn> <br> SoloLearn</a>    
            </li>    
            <li>
                <a href="https://www.codewars.com/users/termokop" target="_blank"><IconCodeWars></IconCodeWars> <br> CodeWars</a>    
            </li>
            <li>
                <a href="https://github.com/termokop" target="_blank"><IconGitHub></IconGitHub> <br> GitHub</a>    
            </li>
        </ul>

        <h3>You can contact me here:</h3>
        <ul class="contacts">
            <li>
                <a class="green" href="https://www.facebook.com/termokop" target="_blank"><IconFacebook></IconFacebook></a>    
            </li>    
            <li>
                <a class="green" href="https://t.me/termokop" target="_blank"><IconTelegram></IconTelegram></a>    
            </li>  
            <li>
                <a class="green" href="https://www.linkedin.com/in/yurii-hruba-085b7a22b/" target="_blank"><IconLinkedIn></IconLinkedIn></a>    
            </li> 
            <li>
                <a class="green" href="https://mail.google.com/mail/u/0/?view=cm&fs=1&tf=1&source=mailto&to=termokop564@gmail.com" target="_blank"><IconGMail></IconGMail></a>    
            </li> 
        </ul>
    </div>

</template>

<style scoped>

.links {
    /* margin-top: 20px; */
    box-sizing: content-box;
    padding: 10px;
    height: 180px;
    width: 300px;
    transform: scale(1, 1);
    margin: 0;

}


ul {
    padding: 0;
}

li{
    display: inline;
}
a {
    outline: none;
    text-decoration: none;
    display: inline-block;
    margin-left: 1%;
    text-align: center;
    padding: 5px;
    box-sizing: border-box;
    width: 31%;
}

.contacts li a {
    width: 24%;
}

h3{
    text-align: center;
    font-weight: bold;
    font-size: 1.2em;
}

@media (min-width: 1024px) {
    .links {
    width: 400px;
}
}

</style>