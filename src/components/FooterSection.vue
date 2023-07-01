<template>
        <h2 class="footerSectionTitle">{{ title }}</h2>
        <ul>
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/about">About</RouterLink>
            <RouterLink to="/publish-property">Post Property</RouterLink>
        </ul>
</template>
<script>
export default {
    name: 'TheFooterSection',
    props: ['details','title'], 
}
</script>
<style scoped>
    .footerSectionTitle{
        color: var(--color-banner-heading);
        border-bottom:2px solid var(--color-banner-heading);
    }
</style>