<template>
    <HomePropertyListItem :details = "propDetails" title="Featured Property" />
    <HomePropertyListItem :details = "propDetails" title="Popular Projects" /> 
    <HomePropertyListItem :details = "propDetails" title="Popular Developers" /> 
    <HomePropertyListItem :details = "propDetails" title="Coming Soon..." /> 
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
           {src: img1, name: 'prop1', type: 'webp', location: 'Jagatpura', price:'80,000/sq feet'},
           {src: img2, name: 'prop2', type: 'jpeg', location: 'Mansarovar', price:'80,000/sq feet'},
           {src: img3, name: 'prop4', type: 'jpg' , location: 'Patrakar Colony', price:'80,000/sq feet'},
           {src: img4, name: 'prop5', type: 'jpg' , location: 'Jhotwara', price:'80,000/sq feet'},
           {src: img5, name: 'prop3', type: 'jpg' , location: 'C-Scheme', price:'80,000/sq feet'},
           {src: img6, name: 'prop6', type: 'webp', location: 'Vaishali Nagar', price:'80,000/sq feet'}
        ]
    }
    },    
    components: {
        HomePropertyListItem,
    }
}
</script>