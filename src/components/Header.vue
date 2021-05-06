<template>
    <header>
        <div class="container flex">
            <img src="@/assets/img/dc-logo.png" alt="logo">

             <!-- Links  -->
            <nav class="flex">
                <ul class="flex" >
                    <li v-for= "(link,index) in links" :key= "index"> 
                    <a :class= "{ active: link.current }" :href="link.url">{{ link.text }}</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
import headLinks from "@/data/headLinks.js";

export default {
    name: 'Header',
    data() {
        return {
            links: headLinks
        }
    },
}
</script>

<style scoped lang="scss">
   @import "@/style/vars.scss";
/* Logo */
img{
    align-self: center;
    max-height: 70px;
    max-width: 70px;
}
/* Nav */
nav {
    flex-grow: 1;
    justify-content: flex-end;
}

li { 
    padding: 45px 15px;
    list-style: none;
    a{
        text-decoration: none;
        text-transform: $upperCase;
        font-size: $font;
        font-weight: bold;
        color: rgb(58, 57, 57);  
        transition: color .3s; 
        &.active,
        &:hover{
            color: $azure;
        }
    }
}
</style>