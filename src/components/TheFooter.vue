<script>
    import FooterSection from './footer/FooterSection.vue'
    import FooterSocialMedia from './footer/socialMedia.vue'
    export default {
        data(){
            return{
                qLinks : [
                    {name:'Home',path:'/'},
                    {name:'About',path:'about'},
                    {name:'Contact',path:'/'},
                    {name:'Support',path:'/'},
                    {name:'Career',path:'/'},
                    {name:'Post Property',path:'/'},
                    {name:'Advertise',path:'/'},
                ],
                oLinks : [
                    {name:'Terms & Conditions',path:'/'},
                    {name:'Privacy Policy',path:'/'},
                    {name:'FAQ',path:'/'}
                ],
                sLinks : [
                    {name:'Packers & Movers',path:'/'},
                    {name:'Brokers',path:'/'},
                    {name:'Legal',path:'/'}
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
        <div class="footerSec"><FooterSection title="Other Services" :links="sLinks" /></div>
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
    font-size: .80rem;
}
@media (max-width: 480px) {
    /* footer{
        flex-direction: column;
    } */
}
</style>