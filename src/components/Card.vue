<template>
    <section>
        <div class="card">
            <div class="img-card">
               <img :src="obj.thumb" :alt="obj.series">
            </div> 
            <h4> {{ obj.series }}</h4>
        </div>
    </section>
</template>

<script>
export default {
  name: "Card",
    props: ["obj"],
}
</script>

<style scoped lang="scss">

section {
    width: calc(100% /6);
} 
 
.card {
    margin: 0 auto; 
    width: 300px;   
}
.img-card {
    height: 155px;
    overflow-y: hidden;    
}
img {
        height: 230px;
        width:170px;
}
h4 {
    margin: 20px 0;
    font-size: 1rem;
    text-transform: uppercase;
    font-weight: 400;
    display: inline-block;
    width:60%;
}
</style>