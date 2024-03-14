<template>
    <div class="meet-the-chefs">
        <h2>Meet The Chefs</h2>
        <div class="meet-the-chefs-cards">
            <div class="card-chef" v-for="item in chefs">
                <img :src="'../../public/img/' + item.image " alt="Daniel Graham">
                <h3>{{ item.name }}</h3>
                <h4>{{ item.role }}</h4>
                <p>
                    {{ item.about }}
                </p>
                <div class="social-media">
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            chefs: {
                0: {
                    image: "chef_1.jpg.webp",
                    name: "Daniel Graham",
                    role: "Master Chef",
                    about: "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.It is a paradisematic country."
                },
                1:{
                    image: "chef_2.jpg.webp",
                    name: "Nick Browning",
                    role: "Master Chef",
                    about: "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.It is a paradisematic country."
                }
            }
        }
    }
}
</script>