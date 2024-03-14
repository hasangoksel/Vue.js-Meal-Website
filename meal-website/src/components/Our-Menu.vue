<template>
    <div ref="ourMenu" id="our-menu" class="menu">
        <div class="menu-title">
            <h2>Menu</h2>
            <p>Free Website Template For Restaurants Made by Goksel</p>
        </div>
        <div class="menu-nav">
            <div class="menu-nav-item">
                <span @click="openBreakfast">Breakfast</span>
                <div id="line-breakfast" class="line" :class="{'menu-nav-item-active': isBreakfast}"></div>
            </div>
            <div class="menu-nav-item">
                <span @click="openBrunch">Brunch</span>
                <div id="line-brunch" class="line" :class="{'menu-nav-item-active': isBrunch}"></div>
            </div>
            <div class="menu-nav-item">
                <span @click="openDinner">Dinner</span>
                <div id="line-dinner" class="line" :class="{'menu-nav-item-active': isDinner}"></div>
            </div>
        </div>
        <div v-if="isBreakfast" class="breakfast">
            <div v-for="item in breakfast">
                <div class="menu-card">
                    <img :src="item.image">
                    <div class="menu-card-content">
                        <h3>{{ item.title }}</h3>
                        <p>{{ item.about }}</p>
                    </div>
                    <span class="price">${{ item.price }}</span>
                </div>
                <div class="menu-card-line"></div>
            </div>
        </div>
        <div v-if="isBrunch" class="brunch">
            <div v-for="item in brunch">
                <div class="menu-card">
                    <img :src="item.image">
                    <div class="menu-card-content">
                        <h3>{{ item.title }}</h3>
                        <p>{{ item.about }}</p>
                    </div>
                    <span class="price">${{ item.price }}</span>
                </div>
                <div class="menu-card-line"></div>
            </div>
        </div>
        <div v-if="isDinner" class="dinner">
            <div v-for="item in dinner">
                <div class="menu-card">
                    <img :src="item.image">
                    <div class="menu-card-content">
                        <h3>{{ item.title }}</h3>
                        <p>{{ item.about }}</p>
                    </div>
                    <span class="price">${{ item.price }}</span>
                </div>
                <div class="menu-card-line"></div>
            </div>
        </div>
    </div>
</template>
<script>
export default{
    mounted() {
        const options = {
            root: null, // viewport'u gözlemle
            rootMargin: '0px', // viewport kenarlarından ne kadar uzakta başlatılacağı
            threshold: 0.0001 // ne kadar oranında görünürse gözleme başlayacak
        };
        const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    // Element görünür hale geldiğinde animasyon sınıfını ekleyin
                    this.$refs.ourMenu.classList.add('fadeInAnimation');
                    observer.unobserve(entry.target); // Gözlemi durdur
                }
            });
        }, options);

        // Gözlemleyiciyi ilgili bölüm üzerinde başlat
        observer.observe(this.$refs.ourMenu);
    },
    data(){
        return{
            isBreakfast: true,
            isBrunch: false,
            isDinner: false,
            breakfast:{
                0:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_1.jpg',
                    title: 'Warm Spinach Deep § Chips',
                    about: 'Spinach and artichokes in a creamy cheese dip with warm tortilla chips & salsa.',
                    price: 10.49
                },
                1:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_2.jpg',
                    title: 'Key Wast Machos',
                    about: 'Crisp tortilla and plantain chips covered with lightly spiced ground beef, melted cheese, pickled jalapeños, guacamole, sour cream and salsa.',
                    price: 11.99
                },
                2:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_3.jpg',
                    title: 'Crispy Onions Rings',
                    about: 'A heaping mountain of rings, handmade with Panko breading and shredded coconut flakes.',
                    price: 15.49
                },
                3:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_1.jpg',
                    title: 'Lobster & Shrimp Quesadilla',
                    about: 'Lobster and tender shrimp, with onions, sweet peppers, spinach and our three cheese blend. Griddled and served with tomato salsa and sour cream.',
                    price: 19.49
                },
            },
            brunch:{
                0:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_3.jpg',
                    title: 'Warm Spinach Deep § Chips',
                    about: 'Spinach and artichokes in a creamy cheese dip with warm tortilla chips & salsa.',
                    price: 10.49
                },
                1:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_2.jpg',
                    title: 'Key Wast Machos',
                    about: 'Crisp tortilla and plantain chips covered with lightly spiced ground beef, melted cheese, pickled jalapeños, guacamole, sour cream and salsa.',
                    price: 11.99
                },
                2:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_1.jpg',
                    title: 'Crispy Onions Rings',
                    about: 'A heaping mountain of rings, handmade with Panko breading and shredded coconut flakes.',
                    price: 15.49
                },
                3:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_3.jpg',
                    title: 'Lobster & Shrimp Quesadilla',
                    about: 'Lobster and tender shrimp, with onions, sweet peppers, spinach and our three cheese blend. Griddled and served with tomato salsa and sour cream.',
                    price: 19.49
                },
            },
            dinner:{
                0:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_2.jpg',
                    title: 'Warm Spinach Deep § Chips',
                    about: 'Spinach and artichokes in a creamy cheese dip with warm tortilla chips & salsa.',
                    price: 10.49
                },
                1:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_3.jpg',
                    title: 'Key Wast Machos',
                    about: 'Crisp tortilla and plantain chips covered with lightly spiced ground beef, melted cheese, pickled jalapeños, guacamole, sour cream and salsa.',
                    price: 11.99
                },
                2:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_1.jpg',
                    title: 'Crispy Onions Rings',
                    about: 'A heaping mountain of rings, handmade with Panko breading and shredded coconut flakes.',
                    price: 15.49
                },
                3:{
                    image: 'https://preview.colorlib.com/theme/meal/images/img_2.jpg',
                    title: 'Lobster & Shrimp Quesadilla',
                    about: 'Lobster and tender shrimp, with onions, sweet peppers, spinach and our three cheese blend. Griddled and served with tomato salsa and sour cream.',
                    price: 19.49
                },
            },
            
        }
    },
    methods:{
        openBreakfast() {
            this.isBreakfast = true;
            this.isBrunch = false;
            this.isDinner = false;
        },
        openBrunch() {
            this.isBreakfast = false;
            this.isBrunch = true;
            this.isDinner = false;
        }, 
        openDinner() {
            this.isBreakfast = false;
            this.isBrunch = false;
            this.isDinner = true;
        },
    }
}
</script>

<style scoped>
.fadeInAnimation {
  animation: fadeInRight 2.3s ease-in-out 1;
}
</style>