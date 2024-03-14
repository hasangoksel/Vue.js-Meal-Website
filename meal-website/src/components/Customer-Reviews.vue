<template>
    <div ref="review" class="customer-reviews">
        <div class="customer-reviews-title">
            <h2>Customer Reviews</h2>
        </div>
        <div class="review" v-if="activeReview !== null" :class="{ 'fadeInAnimation': fadeInAnimation }">
            <p>{{ reviews[activeReview].content }}</p>
            <img :src="reviews[activeReview].image" :alt="reviews[activeReview].name">
            <h3>{{ reviews[activeReview].name }}</h3>
            <h4>{{ reviews[activeReview].role }}</h4>
        </div>
        <div class="customer-reviews-nav">
            <div v-for="(item, index) in reviews" :key="index" @click="changeReview(index)"
                class="customer-reviews-item" :class="{ 'customer-reviews-item-active': index === activeReview }"></div>
        </div>
    </div>
</template>

<script>
export default {
    mounted() {
        const options = {
            root: null,
            rootMargin: '0px', 
            threshold: 0.0001 
        };
        const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    this.$refs.review.classList.add('fadeInAnimationStart');
                    observer.unobserve(entry.target); 
                }
            });
        }, options);

        observer.observe(this.$refs.review);
    },
    data() {
        return {
            reviews: [
                {
                    image: 'https://xsgames.co/randomusers/avatar.php?g=male',
                    name: 'Geert Green',
                    role: 'CEO, Founder',
                    content:
                        'Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati nulla sapiente reiciendis hic impedit voluptatibus magnam nihil laboriosam, corrupti, error est voluptatum ducimus!'
                },
                {
                    image: 'https://xsgames.co/randomusers/avatar.php?g=male',
                    name: 'Green',
                    role: 'CEO, Founder',
                    content:
                        'Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati nulla sapiente reiciendis hic impedit voluptatibus magnam nihil laboriosam, corrupti, error est voluptatum ducimus! Fugiat eum quis pariatur soluta similique quisquam a optio vero mollitia minus.'
                },
                {
                    image: 'https://xsgames.co/randomusers/avatar.php?g=male',
                    name: 'Geert Green',
                    role: 'Employee',
                    content:
                        'Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati nulla sapiente reiciendis hic impedit voluptatibus magnam nihil laboriosam.'
                }
            ],
            activeReview: 0,
            fadeInAnimation: false
        };
    },
    methods: {
        changeReview(index) {
            this.fadeInAnimation = false;
            setTimeout(() => {
                this.activeReview = index;
                this.fadeInAnimation = true;
            }, 300);
        }
    }
};
</script>

<style scoped>
.fadeInAnimationStart {
    animation: fadeInBottom 2s ease-in-out 1;
}.fadeInAnimation {
    animation: fadeIn .8s ease-in-out 1;
}
</style>