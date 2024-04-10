<template>
  <header class="container p-4 d-flex justify-content-between align-items-center ">
    <img src="/images/dc-logo.png" alt="logo Header">
    <ul>
        <li v-for="(item, index) in menu" :key="index"><a :href="item.url">{{item.name}}</a></li>
    </ul>
    <!-- <ul class="d-flex">
        <a href=""><li>CHARACTER</li></a>
        <a href=""><li>COMICS</li></a>
        <a href=""><li>MOVIE</li></a>
        <a href=""><li>TV</li></a>
        <a href=""><li>GAMES</li></a>
        <a href=""><li>COLLECTIBLES</li></a>
        <a href=""><li>VIDEOS</li></a>
        <a href=""><li>FANS</li></a>
        <a href=""><li>NEWS</li></a>
        <a href=""><li>SHOP</li></a>
    </ul> -->
  </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data() {
            return {
                menu: [
                    {
                        name: 'CHARACTER',
                        url: '#'
                    },
                    {
                        name: 'COMICS',
                        url: '#'
                    },
                    {
                        name: 'MOVIE',
                        url: '#'
                    },
                    {
                        name: 'TV',
                        url: '#'
                    },
                    {
                        name: 'GAMES',
                        url: '#'
                    },
                    {
                        name: 'COLLECTIBLES',
                        url: '#'
                    },
                    {
                        name: 'VIDEOS',
                        url: '#'
                    },
                    {
                        name: 'FANS',
                        url: '#'
                    },
                    {
                        name: 'NEWS',
                        url: '#'
                    },
                    {
                        name: 'SHOP',
                        url: '#'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
.container {
    margin: 0 auto;
}

 img {
     width: 50px;
 }
ul {
     list-style: none;
     display:flex;
     justify-content: center;
     li {
         margin: 0px 4px;
         font-size: 8px;
        }
     a {
         padding: 5px 5px;
         text-decoration: none;
         color: black;
         font-weight: 700;
         &:hover {color: #44A1FA;
        border-bottom: 3px solid #44A1FA;}
     }
 }


</style>