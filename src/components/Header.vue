<template>
  <header class="py-4">
    <nav class="d-flex justify-content-between px-3">
        <div class="logo-container">
            <img src="../assets/img/logo-img-01.png" alt="logo" class="img-fluid">
        </div>

        <div>
            <ul>
                <li v-for="(headerElement, index) in headerElementsList" :key="index" class="px-1">
                    <i class="fa-solid fa-arrow-right-long me-2"></i>
                    <a href="#" @click.prevent="">{{ headerElement }}</a> 
                </li>

                <li class="px-2 w-auto">
                    <a href="#" @click.prevent="">
                        <i class="fa-solid fa-magnifying-glass"></i>
                    </a>
                </li>

                <li class="px-2 w-auto">
                    <a href="#" @click.prevent="">
                        <i class="fa-solid fa-bars"></i>
                    </a>
                </li>
            </ul>
        </div>
    </nav>
  </header>
</template>

<script>
export default {
    data: function(){
        return{
            headerElementsList: [
                "Homes",
                "Pages",
                "Blog",
                "Shop",
                "Events",
                "Elements"
                ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

header{
    position: fixed;
    top: 0;
    left: 0;
    z-index: 5;
    background-color: rgba(255, 255, 255, 1);
    width: 100%;
}

nav{
    width: $widthElement;
    margin: 0 auto;
}

ul{
    list-style: none;
    margin: 0;
    text-align: end;
    li{
        display: inline-block;
        width: 120px;
        a{
            text-decoration: none;
            text-transform: uppercase;
            color: black;
            font-size: 14px;
            font-weight: 600;
        }
        i.fa-arrow-right-long{
            display: none;
        }
    }
}
li:hover a{
    color: $textColorHover;
}
li:hover i.fa-arrow-right-long{
    color: $textColorHover;
    display: inline-block;
}

.logo-container{
    width: 150px;
}

</style>