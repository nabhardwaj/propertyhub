<template>
    <HomePropertyListItem :details = "propDetails" title="Featured Property" design="regular" />
    <HomePropertyListItem :details = "propDetails" title="Popular Projects" design="banner" /> 
    <HomePropertyListItem :details = "propDetails" title="Popular Developers" design="regular" /> 
    <HomePropertyListItem :details = "propDetails" title="Coming Soon..." design="banner-circle" /> 
    <HomePropertyListItem :details = "brandDetails" title="Our Partners" design="circle" /> 
</template>
<script>
import HomePropertyListItem from './HomePropertyListItem.vue'
import img1 from '../assets/images/prop1.webp'
    import img2 from '../assets/images/prop2.jpeg'
    import img3 from '../assets/images/prop3.jpg'
    import img4 from '../assets/images/prop4.jpg'
    import img5 from '../assets/images/prop5.jpg'
    import img6 from '../assets/images/prop6.webp'
export default {
    name: 'TheHomeProperty',
    data () {
     return {
        propDetails : [
           {src: img1, name: 'prop1', type: 'webp', brandSrc: "src/assets/images/brands/anukampa.jpeg",location: 'Jagatpura', price:'80,000/sq feet'},
           {src: img2, name: 'prop2', type: 'jpeg', brandSrc: "src/assets/images/brands/dlf.webp", location: 'Mansarovar', price:'80,000/sq feet'},
           {src: img3, name: 'prop4', type: 'jpg' , brandSrc: "src/assets/images/brands/aradhana.jpg",  location: 'Patrakar Colony', price:'80,000/sq feet'},
           {src: img4, name: 'prop5', type: 'jpg' , brandSrc: "src/assets/images/brands/udb.webp", location: 'Jhotwara', price:'80,000/sq feet'},
           {src: img5, name: 'prop3', type: 'jpg' , brandSrc: "src/assets/images/brands/sunindia.jpg",location: 'C-Scheme', price:'80,000/sq feet'},
           {src: img6, name: 'prop6', type: 'webp', brandSrc: "src/assets/images/brands/sng.png",  location: 'Vaishali Nagar', price:'80,000/sq feet'}
        ],
        brandDetails : [
           {src: "src/assets/images/brands/anukampa.jpeg",      name: 'prop1', },
           {src: "src/assets/images/brands/aradhana.jpg",       name: 'prop2', },
           {src: "src/assets/images/brands/dlf.webp",           name: 'prop4', },
           {src: "src/assets/images/brands/okayplus.png",       name: 'prop5',},
           {src: "src/assets/images/brands/sng.png",            name: 'prop3', },       
           {src: "src/assets/images/brands/sunindia.jpg",       name: 'prop6',},
           {src: "src/assets/images/brands/udb.webp",           name: 'prop6',},
           {src: "src/assets/images/brands/vardhman.jpeg",      name: 'prop6',}
        ]
    }
    },    
    components: {
        HomePropertyListItem,
    }
}
</script>