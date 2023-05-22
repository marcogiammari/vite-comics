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
            ],
            footerSocialMedias: [
                {
                    media: 'Facebook',
                    path: 'footer-facebook.png'
                },
                {
                    media: 'Twitter',
                    path: 'footer-twitter.png'
                },
                {
                    media: 'Youtube',
                    path: 'footer-youtube.png'
                },
                {
                    media: 'Pinterest',
                    path: 'footer-pinterest.png'
                },
                {
                    media: 'Periscope',
                    path: 'footer-periscope.png'
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
    <footer>
            <div id="footer-top-section">
                <div class="container">
                    <div class="row justify-content-start">
                        <div class="col-lg-5">
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
                    </div>
                </div>

            </div>
            <div id="footer-bottom-section" class="_flex-center">
                <div class="container">
                    <div class="row d-flex justify-content-between align-items-center">
                        <div id="sign-up" class="col-4 d-flex justify-content-center align-items-center text-white">
                            <a href="#"><h5 class="p-1 text-white m-0">SIGN-UP NOW!</h5></a>
                        </div>
                        <div id="social-media" class="col-4 _flex-center gap-3">
                            <div>
                                <a href="#"><h5 class="p-1 m-0">FOLLOW US</h5></a>
                            </div>
                            <div class="text-secondary d-none d-lg-flex gap-2 fs-5">
                                <a v-for="icon in footerSocialMedias" href="#"><img class="img-fluid" :src="getImagePath(`../assets/img/${icon.path}`)" :alt="icon.name"></a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
    </footer>
</template>


<style lang="scss" scoped>

@use '../styles/partials/variables' as *;


#footer-top-section {
    background: no-repeat url(../assets/img/footer-bg.jpg);
    background-size: cover;

    h5 {
        font-weight: 700 !important;
        font-family: 'Encode Sans Condensed', sans-serif;
    }

    ul {
        list-style: none;
    }

    li {
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        color: rgba(211, 211, 211, 0.733);
    }

    .container > .row {
        background-image: url(../assets/img/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: right;
    }

    a {
        text-decoration: none !important;
        font-size: 14px;

        &:hover {
            text-decoration: underline grey !important;
        }
    }
}

#footer-bottom-section {
    background-color: #303030;
    min-height: 6rem;
    font-family: 'Encode Sans Condensed', sans-serif;

    h5:hover {
        border: 2px solid $primarycolor;
    }

    a {
        text-decoration: none;
    }

    #social-media h5 {
        color: $primarycolor;
    }

}






</style>