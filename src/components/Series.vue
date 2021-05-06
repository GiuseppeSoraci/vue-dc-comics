<template>
    <section>
       <!-- Title -->
       <div class="container"> 
           <h2>current series</h2>
       </div>

       <!-- Cards -->
       <div class="container flex img">
            <Card v-for= "(serie,index) in cards" :key= "index" :obj= "serie" /> 
       </div>

       <!-- Button --> 
       <div class="container flex">
            <button>load more</button>
       </div>
    </section>
</template>

<script>
import Card from "@/components/Card.vue"
import cards from "@/data/cards.js"
export default {
     name: "Series",
     components: {
         Card,
    },
     data(){
         return {
             cards: cards,                     
        }
    }
}

</script>

<style scoped lang="scss">
@import "@/style/vars.scss";

section{
    background: $black;
    color: $white;
}
.container{
    justify-content: center;
}
h2{
    display: inline-block;
    padding: 10px 30px;
    position: relative;
    bottom: 15px;
    text-transform: $upperCase;
    font-size: 1.2rem;
    background: $azure;    
}
.img{
    flex-wrap: wrap;
    padding: 0 10px;
    padding-bottom: 40px; 
} 
button{
    padding: 10px 60px;
    text-transform: $upperCase;
    font-weight: bold;
    border: none;  
    margin-bottom: 30px; 
    cursor: pointer;
    color: $white;  
    background: $azure;
    transition: .3s;
    &:hover{
        color: $azure;
        background: $white;
    }
}
</style>