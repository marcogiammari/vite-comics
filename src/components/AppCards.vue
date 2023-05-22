<script>

export default {
    name: 'AppCards',
    props: 
        {
            cards: {
                thumb: String,
                series: String,
            }
        }
}

</script>


<template>
    <section class="position-relative">
        <div class="container">
            <h2 id="current-series" class="text-white position-absolute">CURRENT SERIES</h2>
            <div class="row py-5">
                <div class="my_card col-2 text-center d-flex flex-column gap-3" v-for="card in cards">
                    <div class="img-wrapper">
                        <img class="img-fluid" :src="card.thumb" alt="card.series">
                    </div>
                    <div>
                        <p class="text-white">{{ card.series.toUpperCase() }}</p>
                    </div>
                </div>
            </div>
            <div id="load-btn" class="_flex-center">
                <button class="btn text-white px-5 rounded-0">
                    LOAD MORE
                </button> 
            </div>
        </div>
    </section>

</template>


<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.my_card {
    margin: 1.5rem 0;
    .img-wrapper {
        width: 10vw;
        height: 10vw;
        
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }

        p {
            font-family: 'Open Sans', 'Helvetica Neue', sans-serif !important;

        }
    }
}

#load-btn button {
    background-color: $primarycolor;
    font-family: 'Encode Sans Condensed', sans-serif;
    font-weight: 600;
    margin-bottom: 2rem;
}

#current-series {
    // margin-top: -1rem;
    background-color: $primarycolor;
    font-weight: 700;
    padding: .75rem 3rem;
    font-size: 1.5rem;
    width: fit-content;
    font-family: 'Encode Sans Condensed', sans-serif;
    transform: translate(0%, -50%);
}

</style>