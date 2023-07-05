<template>
    <h2 class="footerSectionTitle">{{ title }}</h2>
    <div class="flexRow">
        <fa v-for="media in socialMedia" :icon="['fab',media]" />
    </div>
</template>
<script >
    export default {
    name: 'TheHomePropertyList',
    props: ['title'],
        data () {
            return {
               socialMedia : ['facebook','youtube','twitter','linkedin','instagram']
            }
        }
    }
</script>
<style>
    .svg-inline--fa{
        font-size:2rem;
        margin:5px 5px 0px 0px;
        color: rgb(94 94 94);
        cursor: pointer;
        padding: 3px;
    }
    .footerSectionTitle{
        color: var(--color-banner-heading);
        border-bottom:2px solid var(--color-banner-heading);
        font-size: 1rem;
    }
</style>