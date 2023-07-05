<script>
    import FooterSection from './footer/FooterSection.vue'
    import FooterSocialMedia from './footer/SocialMedia.vue'
    export default {
        data(){
            return{
                qLinks : [
                    {name:'Home',path:'/'},
                    {name:'About',path:'about'},
                    {name:'Contact',path:'/'},
                    {name:'Post Property',path:'/'},
                ],
                oLinks : [
                    {name:'Terms & Conditions',path:'/'},
                    {name:'Privacy Policy',path:'/'}
                ]
            }
        },
        components: {
            FooterSection,
            FooterSocialMedia
        }
    }
</script>

<template>
    <footer>
        <div class="footerSec"><FooterSection title="Quick Links" :links="qLinks" /></div>
        <div class="footerSec"><FooterSection title="Other Links" :links="oLinks" /></div>
        <div class="footerSec"><FooterSocialMedia title="Follow Us"/></div>
    </footer>
</template>
<style scoped>
footer{
  background:var(--color-primary);
  padding: 1rem;
  display: flex;
    place-items: start;
    line-height: 1.5;
    flex-wrap: wrap;
}
.footerSec{
    flex: 1 1 auto;
    padding: 1rem;
}
@media (max-width: 480px) {
    /* footer{
        flex-direction: column;
    } */
}
</style>