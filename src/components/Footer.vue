<template>
    <section>
        <div class="container flex">

            <!-- dc comics & shop -->
            <div>
                <ul>
                    <h3> dc comics</h3>
                    <li v-for= "(item, index) in dsComics" :key= "index">
                    <a href="#"> {{ item.text }}</a></li>
                </ul>

                <ul>
                    <h3>shop</h3>
                    <li v-for= " (item,index) in shop " :key= "index"><a href="#"> {{item.text }}</a></li>
                </ul>
            </div>   

             <!-- dc -->
            <ul>
                <h3>dc</h3>
                <li v-for= "(item,index) in dc" :key= "index"><a href="#">{{ item.text }}</a></li>
            </ul>
             
             <!-- sites -->
            <ul>
                <h3>sites</h3>
                <li v-for= "(item,index) in sites" :key= "index" ><a href="#">{{ item.text }}</a></li>       
            </ul>
             
        </div>

         <!-- logo bg -->
        <div class="box">
            <img src="../assets/img/dc-logo-bg.png" alt="logo-bg">
        </div>        
    </section>  
</template>

<script>
export default {
    name: "Footer",
    data() {
        return {
            dsComics: [
                {text: "characters"},
                {text: "comics"},
                {text: "movies"},
                {text: "tv"},
                {text: "games"},
                {text: "videos"},
                {text: "news"},
            ],
            shop: [
                {text: "Shop DC"},
                {text: "Shop DC Collectibles"},
            ],
            dc: [
                {text: "terms Of Use"},
                {text: "Privacy policy (New)"},
                {text: "Ad Choise"},
                {text: "Jobs"},
                {text: "subscriptions"},
                {text: "Talent Workshops"},
                {text: "CPSC Certificates"},
                {text: "Ratings"},
                {text: "Shop Help"},
                {text: "Contact Us"},
            ],
            sites: [
                 {text: "DC"},
                 {text: "MAD Magazine"},
                 {text: "DC Kids"},
                 {text: "DC Universe"},
                 {text: "DC Power Visa"},
            ],
        }
    }
}
</script>

<style scoped lang="scss">
@import "@/style/vars.scss";

section{
    position: relative;
    background-image: url(../assets/img/footer-bg.jpg); 
    
}
.container{
    padding: 60px 0;
}
ul{
    list-style: none;
     padding: 20px;   
} 
h3 {
    margin-bottom: 5px;
    text-transform: $upperCase;
    color: $white;
} 
a{
    text-decoration: none;
    text-transform: capitalize;
    font-size: 12px;
    color: $grey;
    transition: .3s;
    &:hover{
        color:$white;
    }
} 
.box {
    width: 550px;
    height: 430px;
    overflow: hidden;
    position: absolute;
    top: 0;
    left: 50%;
  
} img {
      width: 550px; 
}
</style>