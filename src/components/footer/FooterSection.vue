<template>
        <h2 class="footerSectionTitle">{{ title }}</h2>
        <div class="flexColumn">
            <RouterLink v-for="(li,index) in links" :key=index :to="li.path">{{ li.name }}</RouterLink>
        </div>
</template>
<script>
export default {
    name: 'TheFooterSection',
    props: ['links','title'], 
}
</script>
<style scoped>
    .footerSectionTitle{
        font-size: 1rem;
        color: var(--color-banner-heading);
        border-bottom:2px solid var(--color-banner-heading);
    }
</style>