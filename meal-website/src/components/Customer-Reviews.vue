<template>
    <div class="customer-reviews">
        <div class="customer-reviews-title">
            <h2>Customer Reviews</h2>
        </div>
        <div class="review" v-if="activeReview !== null">
            <p>{{ reviews[activeReview].content }}</p>
            <img :src="reviews[activeReview].image" :alt="reviews[activeReview].name">
            <h3>{{ reviews[activeReview].name }}</h3>
            <h4>{{ reviews[activeReview].role }}</h4>
        </div>
        <div class="customer-reviews-nav">
            <div v-for="(item, index) in reviews" :key="index" @click="changeReview(index)" class="customer-reviews-item" :class="{ 'customer-reviews-item-active': index === activeReview }"></div>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            reviews: [
                {
                    image: 'https://xsgames.co/randomusers/avatar.php?g=male',
                    name: 'Geert Green',
                    role: 'CEO, Founder',
                    content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati nulla sapiente reiciendis hic impedit voluptatibus magnam nihil laboriosam, corrupti, error est voluptatum ducimus!"
                },
                {
                    image: 'https://xsgames.co/randomusers/avatar.php?g=male',
                    name: 'Green',
                    role: 'CEO, Founder',
                    content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati nulla sapiente reiciendis hic impedit voluptatibus magnam nihil laboriosam, corrupti, error est voluptatum ducimus! Fugiat eum quis pariatur soluta similique quisquam a optio vero mollitia minus."
                },
                {
                    image: 'https://xsgames.co/randomusers/avatar.php?g=male',
                    name: 'Geert Green',
                    role: 'Employee',
                    content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati nulla sapiente reiciendis hic impedit voluptatibus magnam nihil laboriosam."
                }
            ],
            activeReview: 0
        }
    },
    methods: {
        changeReview(index) {
            this.activeReview = index;
        }
    }
}
</script>
