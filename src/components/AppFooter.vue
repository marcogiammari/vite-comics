<script>
  export default {
    name: 'AppFooter',
    data() {
        return {
            footerCols: [
                [
                    {
                        heading: 'Dc Comics',
                        links: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                    },
                    {
                        heading: 'Shop',
                        links: ['Shop DC', 'Shop DC Collectibles']
                    }
                ],
                [
                    {
                        heading: 'Dc',
                        links: ['Terms Of Use', 'Privacy Policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', ' CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                    }
                ],
                [
                    {
                        heading: 'Sites',
                        links: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                    }
                ]
            ]
        }
    } 
  }

</script>


<template>
    <footer>
            <div id="footer-top-section">
                <div class="container">
                    <div class="row justify-content-around">
                        <div class="col-5">
                            <div class="row h-100 py-5">
                                <div v-for="col in footerCols" class="col-4 d-flex justify-content-start flex-column">
                                    <div v-for="obj in col" class="links-list text-white">
                                        <h5>{{ obj.heading.toUpperCase() }}</h5>
                                        <ul class="text-white p-0">
                                            <a v-for="link in obj.links" href="#"><li>{{ link }}</li></a>  
                                        </ul>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-5 h-100 d-flex align-items-center">
                            <img id="bg-logo" src="../assets/img/dc-logo-bg.png" alt="dc logo">
                        </div>
                    </div>
                </div>

            </div>
            <div id="footer-bottom-section" class="_flex-center">
                <div class="container">
                    <div class="row d-flex justify-content-between align-items-center">
                        <div id="sign-up" class="col-3 d-flex justify-content-center align-items-center text-white">
                            <a href="#"><h5 class="p-1 text-white m-0">SIGN-UP NOW!</h5></a>
                        </div>
                        <div id="social-media" class="col-4 _flex-center gap-3">
                            <div>
                                <a href="#"><h5 class="p-1 m-0">FOLLOW US</h5></a>
                            </div>
                            <div class="text-secondary d-flex gap-2 fs-5">
                                <a href="#"><img class="img-fluid" src="../assets/img/footer-facebook.png" alt="facebook"></a>
                                <a href="#"><img class="img-fluid" src="../assets/img/footer-twitter.png" alt="twitter"></a>
                                <a href="#"><img class="img-fluid" src="../assets/img/footer-youtube.png" alt="youtube"></a>
                                <a href="#"><img class="img-fluid" src="../assets/img/footer-pinterest.png" alt="pinterest"></a>
                                <a href="#"><img class="img-fluid" src="../assets/img/footer-periscope.png" alt="periscope"></a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
    </footer>
</template>


<style lang="scss" scoped>

$primarycolor: #0C7CEC;

div {
    height: 100%;
}

#footer-top-section {
    height: 22rem;
    overflow: hidden;
    background: no-repeat url(../assets/img/footer-bg.jpg);
    background-size: cover;
}

#footer-bottom-section {
    background-color: #303030;
    min-height: 6rem;
}

#bg-logo {
    max-height: unset;
}

#footer-top-section h5 {
    font-weight: 700 !important;
}


#footer-bottom-section h5:hover {
    border: 2px solid $primarycolor;
}

#footer-top-section a {
    text-decoration: none !important;
    font-size: 14px;

        &:hover {
            text-decoration: underline grey !important;
        }
}

#footer-bottom-section a {
    text-decoration: none !important;
}


ul {
    list-style: none;
}

li {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    color: rgba(211, 211, 211, 0.733);
}

#social-media h5 {
    color: $primarycolor;
}


</style>