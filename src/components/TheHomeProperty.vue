<template>
    <HomePropertyListItem :details = "propDetails" :title="title" /> 
</template>
<script>
import HomePropertyListItem from './HomePropertyListItem.vue'

export default {
    name: 'TheHomeProperty',
    data () {
     return {
        propDetails : [
           {name: 'prop1', type: 'webp', location: 'Jagatpura', price:'80,000/sq feet'},
           {name: 'prop2', type: 'jpeg', location: 'Mansarovar', price:'80,000/sq feet'},
           {name: 'prop4', type: 'jpg' , location: 'Patrakar Colony', price:'80,000/sq feet'},
           {name: 'prop5', type: 'jpg' , location: 'Jhotwara', price:'80,000/sq feet'},
           {name: 'prop3', type: 'jpg' , location: 'C-Scheme', price:'80,000/sq feet'},
           {name: 'prop6', type: 'webp', location: 'Vaishali Nagar', price:'80,000/sq feet'}
        ],
        title: "Featured Property"
    }
    },    
    components: {
        HomePropertyListItem,
    }
}
</script>