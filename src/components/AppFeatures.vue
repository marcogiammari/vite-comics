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
        <div class="container py-5">
            <div class="row _flex-center text-light">
                <div v-for="feat in features" class="feature _flex-center col-12 col-md-6 col-lg-3 col-xl-2 my-3">
                    <a href="#" class="d-flex align-items-center gap-3">
                        <img class="img-fluid" :src="getImagePath(`../assets/img/${feat.path}`)" :alt="feat.txt">
                        <span>{{feat.txt.toUpperCase()}}</span>
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

#features {
    background-color: $primarycolor;
    
    a {
        color: white;
        text-decoration: none;
        height: 100%;
        
        &:hover {
            color: white;
            text-decoration: underline;
        }
    }
    
    
    span {
        font-family: 'Lucida Sans', sans-serif;
        font-size: .875rem
    }
    
    img {
        height: 4rem;
    }
}

</style>
