<script>
  export default {
    name: 'AppFeatures'
  }

</script>


<template>
    <section id="features">
        <div class="container">
            <div class="row justify-content-center text-light">
                <div class="feature d-flex _flex-center gap-3">
                    <a href="#" class="d-flex align-items-center gap-3">
                        <img class="img-fluid" src="../assets/img/buy-comics-digital-comics.png" alt="digital comics">
                        <span>DIGITAL COMICS</span>
                    </a>
                </div>
                <div class="feature d-flex _flex-center gap-3">
                    <a href="#" class="d-flex align-items-center gap-3">
                        <img class="img-fluid" src="../assets/img/buy-comics-merchandise.png" alt="merchandise">
                        <span>DC MERCHANDISE</span>
                    </a>
                </div>
                <div class="feature d-flex _flex-center gap-3">
                    <a href="#" class="d-flex align-items-center gap-3">
                        <img class="img-fluid" src="../assets/img/buy-comics-subscriptions.png" alt="subscriptions">
                        <span>SUBSCRIPTION</span>
                    </a>
                </div>
                <div class="feature d-flex align-items-center">
                    <a href="#" class="d-flex align-items-center gap-3">
                        <img src="../assets/img/buy-comics-shop-locator.png" alt="shop-locator">
                        <span>COMIC SHOP LOCATOR</span> 
                    </a>
                </div>
                <div class="feature d-flex _flex-center gap-3">
                    <a href="#" class="d-flex align-items-center gap-3">
                        <img class="img-fluid" src="../assets/img/buy-dc-power-visa.svg" alt="dc-power-visa">
                        <span>DC POWER VISA</span>
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
