<template>
 <div class="other-services">
        <div class="other-services-title">
            <h2>Other Services</h2>
            <p>Free Website Template For Restaurants Made by Goksel</p>
        </div>
        <div class="other-services-card-container">
            <div class="other-services-card" v-for="item in services">
                <img :src="'../../public/img/' + item.image">
                <div class="other-services-card-content">
                    <h3>{{ item.title }}</h3>
                    <p>{{ item.content }}</p>
                </div>
            </div>
            
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            services: {
                0: {
                    image: "soup.png",
                    title: "Quality Cuisine",
                    content: "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts."
                },
                1: {
                    image: "vegetables.png",
                    title: "Fresh Food",
                    content: "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts."
                }, 
                2: {
                    image: "pancake.png",
                    title: "Bread & Pancake",
                    content: "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts."
                },
                3: {
                    image: "reserve.png",
                    title: "Reserve Now",
                    content: "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts."
                },
                4:{
                    image: "salad.png",
                    title: "Fresh Vegies Salad",
                    content: "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts."
                },
                5:{
                    image: "chicken.png",
                    title: "Whole Chicken",
                    content: "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts."
                }
            }
        }
    }
}
</script>