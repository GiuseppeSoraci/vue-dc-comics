<template>
    <section>
        <div class="container">
            <ul>
                <li class="flex">
                    <a href="#"> <img src="../assets/img/buy-comics-digital-comics.png" alt="digital-comics"> </a>
                    <a href="#">digital comics</a>
                    </li> 
                <li class="flex"><a href="#"> <img src="../assets/img/buy-comics-merchandise.png" alt="merchandise">  </a><a href="#">dc merchandise</a></li>
                <li class="flex"><a href="#"> <img src="../assets/img/buy-comics-subscriptions.png" alt="subscriptions"> </a><a href="#">subscription</a></li>
                <li class="flex"><a href="#"> <img src="../assets/img/buy-comics-shop-locator.png" alt="shop">  </a><a href="#">comic shop locator</a></li>
                <li class="flex"><a href="#"> <img class="visa" src="../assets/img/buy-dc-power-visa.svg" alt="visa">  </a><a href="#">dc power visa</a></li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    name:"Services",
}

</script>

<style scoped lang="scss">
@import "@/style/vars.scss";

section{
    background: $azure;
}
ul{
    display: flex;
    justify-content: center;
    list-style: none;
} li {
     padding: 60px 0;
    } a:last-child{
        margin-left: 12px;
        margin-right: 60px;
        text-decoration: none;
        text-transform: $upperCase;
        font-size: 14px;
        color: $white;
        line-height: 50px; 
    }   
img{
    max-width: 45px;
    max-height: 45px;
}
.visa{
  width: 45px;
  position: relative;
  top: 8px; 
}

</style>