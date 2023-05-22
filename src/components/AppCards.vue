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
    <section>
        <div class="container py-5">
            <div class="row py-5">
                <div class="my_card col-2 _flex-center flex-column gap-4" v-for="card in cards">
                    <div class="img-wrapper">
                        <img class="img-fluid" :src="card.thumb" alt="card.series">
                    </div>
                    <div>
                        <p class="text-white">{{ card.series.toUpperCase() }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>


<style lang="scss" scoped>



.my_card {
    
    .img-wrapper {
        width: 10vw;
        height: 10vw;
        object-fit: cover;
        
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }
    }
}

</style>