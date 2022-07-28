<template>
  <section>
    <div>
        <div class="logos-container d-flex">
            <div class="logo" v-for="(logo, index) in sponsorLogos" :key="index" :class="{'text-center': index === 2, 'text-end': index > 2}">
                <img :src="require(`../../../assets/img/${logo.visibleImg}`)" alt="logo" class="logo-in-sight">
                <img :src="require(`../../../assets/img/${logo.hiddenImg}`)" alt="logo" class="hidden-logo">
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    data: function(){
        return{
            sponsorLogos: [
                {
                    visibleImg: "h4-clients-img-01.png",
                    hiddenImg: "h4-clients-img-02.png"
                },
                {
                    visibleImg: "h4-clients-img-03.png",
                    hiddenImg: "h4-clients-img-04-1.png"
                },
                {
                    visibleImg: "h4-clients-img-05.png",
                    hiddenImg: "h4-clients-img-06-1.png"
                },
                {
                    visibleImg: "h4-clients-img-07.png",
                    hiddenImg: "h4-clients-img-08-1.png"
                },
                {
                    visibleImg: "h4-clients-img-09.png",
                    hiddenImg: "h4-clients-img-10-1.png"
                },
            ]
        }
    }
    
}
</script>

<style lang="scss" scoped>
@import "../../../styles/variables.scss";
section{
    padding: 80px 0;
}

section > div{
    width: $widthElement;
    margin: 0 auto;
}
.logos-container{
    width: 70%;
    margin: 0 auto;
    .logo{
        width: 20%;
    }
}

.logo-in-sight{
    display: inline-block;
}
.hidden-logo{
    display: none;
}

.logo:hover .hidden-logo{
    display: inline-block;
}
.logo:hover .logo-in-sight{
    display: none;
}

</style>