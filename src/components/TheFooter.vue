<script setup>
    import FooterSection from './FooterSection.vue'
</script>

<template>
    <footer>
        <FooterSection title="Quick Links"/>
        <FooterSection title="Follow Us"/>
    </footer>
</template>
<style scoped>
footer{
  background:var(--color-primary);
  padding: 1rem;
  display: flex;
    place-items: center;
    line-height: 1.5;
}
</style>