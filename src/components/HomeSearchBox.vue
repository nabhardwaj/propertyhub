<template>
    <div class="homeSrchBoxContainer">
        <div class="srchBoxHeading">
            <slot name="heading" class="heading"></slot>
            <input type="radio" value="rent" v-model="pFor" id="rentBtn"/>
            <label for="rentBtn">Rent</label>
            <input type="radio" value="buy" v-model="pFor" id="buyBtn"/>
            <label for="buyBtn">Buy</label>
        </div>
        <div class="homeSrchBox flexRow">
            <input type="text" v-model="city" class="srchBox" placeholder="Enter locality, city, pincode, projects, builders" />
            <span class="srchBtn">
                <fa :icon="['fas','search']" />
            </span>
        </div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                pFor:''
            }
        }
    }
</script>
<style scoped>
     .homeSrchBoxContainer{
            width: 90vw;
            left: 5vw;
            position: relative;
            top: -56px;
        }
    .srchBoxHeading{
        padding: calc(1rem - 12px) 1rem;
        border-radius: 10px 10px 0px 0px;
        background: rgba(255,255,255,0.8);
        color: var(--color-banner-heading);
    }
    .homeSrchBox{
        padding: 1rem;
        border-radius:0px 0px 10px 10px;
        background: rgba(255,255,255,1);
        box-shadow: 0px 5px 10px 1px rgb(84 84 84 / 50%);
        position:relative;
    }
    .srchBox{
        flex: 1 1 auto;
        outline: none;
        border: 1px solid #666;
        border-radius: 8px;
        font-family: inherit;
        font-size: .8rem;
        padding: 10px 12px;
    }
    .srchBtn{
        position: absolute;
        top: 17px;
        right: 18px;
        padding:0px 0px 0px 10px;
        border-radius:0px 8px 8px 0px;
        background:var(--color-primary);
        font-size: 1rem;
    line-height: 1.5rem;
    }
    [type="radio"]{
        display:none
    }
    [type="radio"]+label{
        display:inline-block;
        margin: 5px;
        padding: 5px;
        border-radius:20px;
        width:70px;
        border: 2px solid;
        text-align: right;
        cursor: pointer;
        position: relative;
    }
    [type="radio"]+label:before {
        content: '';
        position: absolute;
        width: 20px;
        height: 20px;
        border-radius: 50%;
        
        left: 7px;
        top: 7px;
        background: #86d335;
        box-shadow: 1px 1px 2px;
    }
    [type="radio"]:not(:checked)+label{

    }
    [type="radio"]:checked+label{
        background: rgb(221 240 201);
        box-shadow: inset 5px 5px 10px #000;
        text-align: left;
        background-image: linear-gradient(to right, #ddf0c9 , #83c73b);
        text-indent: 5px;
    }
     [type="radio"]:checked+label:before{
        left: 40px;
        transition: all 0.5s ease-in-out;
    }
    @media (min-width:780px) {
        .homeSrchBoxContainer{
            width: 50vw;
            position: relative;
            top: -56px;
            left: calc(50% - 25vw);
        }
    }
</style>