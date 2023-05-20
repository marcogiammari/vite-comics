<script>
  export default {
    name: 'AppFeatures',
    data() {
        return {
            features: [
                {
                    txt: 'Digital Comics',
                    path: 'buy-comics-digital-comics.png'
                },
                {
                    txt: 'DC Merchandise',
                    path: 'buy-comics-merchandise.png'
                },
                {
                    txt: 'Subscription',
                    path: 'buy-comics-subscriptions.png'
                },
                {
                    txt: 'Comic Shop Locator',
                    path: 'buy-comics-shop-locator.png'
                },
                {
                    txt: 'DC Power Visa',
                    path: 'buy-dc-power-visa.svg'
                }
            ]
        }
    },
    methods: {
        getImagePath(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
  }

</script>


<template>
    <section id="features">
        <div class="container">
            <div class="row justify-content-center text-light">
                <div v-for="feat in features" class="feature d-flex _flex-center gap-3">
                    <a href="#" class="d-flex align-items-center gap-3">
                        <img class="img-fluid" :src="getImagePath(`../assets/img/${feat.path}`)" alt="digital comics">
                        <span>{{feat.txt.toUpperCase()}}</span>
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

$primarycolor: #0C7CEC;

#features {
    background-color: $primarycolor;
    height: 10rem;
}

a {
    color: white;
    text-decoration: none;
    height: 100%;
}

a:hover {
    color: white;
    text-decoration: underline;
}

span {
    font-family: 'Lucida Sans', sans-serif;
    font-size: .875rem
}

#features img {
    height: 35%;
}

div {
    height: 100%;
}

.feature {
    width: calc(100% / 5);
}

</style>
