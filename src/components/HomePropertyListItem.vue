<template>
    <div class="listTitle flexRow spaceBetween">
        <h2>{{ title }}</h2>
        <span >View All</span>
    </div>
    <div class="sliderContainer">
    <div class="listView flexRow">
        <div v-for="(d,index) in details" :key="index" class="list mr-r-1">
            <a class="propLink">
            <div class="displayPic">              
                <img :src="imgSrc+d.name+'.'+d.type" :name=d.name :alt=d.name />
            </div>
            <div class="detailBox flexRow space-between bg-white">
                <span >{{ d.location }}</span>
                <span >{{ d.price }}</span>
            </div>
            </a>
        </div>
    </div>
    </div>
</template>
<script >
    export default {
    name: 'TheHomePropertyList',
    props: ['details','title'],
        data () {
            return {
                imgSrc : `src/assets/images/`
            }
        }
    }
</script>
<style scoped>
.listTitle{
    margin-top:2rem;
    margin-bottom:1rem;
    color: var(--color-heading);
}
.sliderContainer{
    display: block;
    position: relative;
    width:100%;
    overflow:hidden;
}
.listView .list:last-child{
    margin-right: 0px;
}
.propLink{
    cursor: pointer;
}
.displayPic{
    display: block;
    position: relative;
    width:200px;
    height:140px;
    overflow: hidden;
}
.displayPic > img{
    width:200px;
    height:140px;
    object-fit:cover;
    filter:brightness(0.5);
}
.propLink:hover > .displayPic > img{
    filter: initial;
    transition: filter 1.2s ease-in;
}
.detailBox{
    display: flex;
    place-items: center;
    justify-content: space-between;
    color: var(--color-heading);
    font-size: .80rem;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 0px 0px 4px 4px;
    padding:10px;
}
</style>