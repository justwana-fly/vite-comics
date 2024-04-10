<template>
    <footer>


        <div class="bg-section-one">
            <div class="section-one container p-4 ">
                <ul class="d-flex justify-content-between align-items-center">
                    <li v-for="(item, index) in mercato" :key="index">
                        <a :href="item.url">
                            <img :src="item.img" alt="">{{ item.name }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>

        <div class="bg-section-two">
            <div class="section-two container">2</div>
        </div>

        <div class="bg-section-three">
            <div class="section-three container">3</div>
        </div>



    </footer>
</template>

<script>
export default {
    name: "HeaderComponent",
    data() {
        return {
            mercato: [
                {
                    img: '/images/buy-comics-digital-comics.png',
                    name: 'DIGITAL COMICS',
                    url: '#'
                },
                {
                    img: '/images/buy-comics-merchandise.png',
                    name: 'DC MERCHANDISE',
                    url: '#'
                },
                {
                    img: '/images/buy-comics-subscriptions.png',
                    name: 'SUBSCRIPTION',
                    url: '#'
                },
                {
                    img: '/images/buy-comics-shop-locator.png',
                    name: 'COMIC SHOP LOCATOR',
                    url: '#'
                },
                {
                    img: '/images/buy-ds-power-visa.svg',
                    name: 'DC POWER VISA',
                    url: '#'
                },

            ]
        }
    }
};
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
.bg-section-one {
    background-color: #0282F9;

}

.section-one img {
    width: 20px;
   
}

.section-one li {
    list-style: none;
    
    font-size: 10px;
    a {
        text-decoration: none;
        color: white;
        font-weight: 700;

        &:hover {
            text-decoration: underline;
        }

    }

}

.bg-section-two {
    background-image: url(/images/footer-bg.jpg);


}

.bg-section-three {
    background-color: #303030;

}
</style>
