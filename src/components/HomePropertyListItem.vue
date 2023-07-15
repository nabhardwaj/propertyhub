<template>
    <div class="container">
    <div class="listTitle flexRow spaceBetween">
        <h2>{{ title }} {{ design }}</h2>
        <span >View All</span>
    </div>
    
        <div class="sliderContainer">
            <!-- if design is regular-->
            <div class="listView flexRow" v-if="design=='regular'">
                <div v-for="(d,index) in details" :key="index" class="list mr-r-1">
                    <a class="propLink">
                    <div class="displayPic">              
                        <!-- <img v-bind:src="`src/assets/images/`+d.name+'.'+d.type" :name=d.name :alt=d.name /> -->
                        <img :src=d.src :name=d.name :alt=d.name :title=d.name />
                        
                    </div>
                    <div class="detailBox flexRow space-between bg-white">
                        <span >{{ d.location }}</span>
                        <span >{{ d.price }}</span>
                    </div>
                    </a>
                </div>
            </div>
            
            <!-- if design is banner circle-->
            <div class="listView flexRow" v-if="design=='banner-circle'">
                <div v-for="(d,index) in details" :key="index" class="banner-circle-list mr-r-1">
                    <a class="propLink">
                    <div class="banner-circle">              
                        <img :src=d.src :name=d.name :alt=d.name :title=d.name class="bannerImg" />
                        <img :src=d.brandSrc :name=d.name :alt=d.name :title=d.name class="brandIcon" />
                    </div>           
                    </a>
                </div>
            </div>
            <!-- if design is circle-->
            <div class="listView flexRow" v-if="design=='circle'">
                <div v-for="(d,index) in details" :key="index" class="list mr-r-1">
                    <a class="propLink">
                    <div class="displayPic circle">              
                        <img :src=d.src :name=d.name :alt=d.name :title=d.name />
                    </div>           
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>
<script >
    export default {
    name: 'TheHomePropertyList',
    props: ['details','title','design'],
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
    place-items: baseline;
}
.container{
    padding: 1rem;
}
.sliderContainer{
    display: block;
    position: relative;
    width:100%;
    overflow:hidden;
}
.listView{
    padding-bottom:20px;
    overflow: auto;
}
.listView::-webkit-scrollbar{
    width: 0px;
    height: 0px;
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
.displayPic.circle{
    width: 94px;
    height: 94px;
    border-radius: 50%;
    border: 1px solid var(--color-primary);
    padding: 3px;
}
.displayPic > img{
    width:200px;
    height:140px;
    object-fit:cover;
    filter:brightness(0.5);
}
.displayPic.circle > img{
    width: 100%;
    height: 100%;
    object-fit: contain;
    filter: initial;
    background-blend-mode: color-burn;
}
.propLink:hover > .displayPic > img{
    filter: initial;
    transform: scale(1.2);
    transition: all .5s ease-in;
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
.banner-circle-list{
    position: relative;
    flex: 1 0 50%;
}
.banner-circle{
    position: relative;
    aspect-ratio: 4/3;
}
.banner-circle > img.bannerImg{
   object-fit: cover;
   width: 100%;
   height: 100%;
   filter: brightness(0.5);
}
.banner-circle > img.brandIcon{
    width: 94px;
    height: 94px;
    border-radius: 50%;
    border: 1px solid var(--color-primary);
    padding: 3px;
    position: absolute;
    object-fit: contain;
    background-blend-mode: color-burn;
    bottom: -48px;
    left: calc(50% - 48px);
    background: #FFF;
    z-index: 1;
}
.banner-circle::before{
    content: '';
    position:absolute;
    background:rgba(255,255,255,0.7);
    top:0;
    right:0;
    left:0;
    bottom:0;
    clip-path: polygon(50% 0%, 60% 100%, 40% 100%);
    z-index: 1;
}
</style>
