<template>
    
    <header id="home">
        <div class="header-content">
            <h1>Welcome to Meal</h1>
            <a href="#reserve">Reserve a table</a>
        </div>
    </header>
</template>
<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<style scoped>
.header-content h1{
    animation: welcomeTitle 2s ease-in-out 1;
}
.header-content a{
    animation: fadeInLeft 2s ease-in-out 1;
}
@keyframes welcomeTitle {
    0%{
        transform: translate3d(200px, -200px, 0);
        opacity: 0;
    }
    /* 25%{
        transform: translate3d(-200px, -200px, 0);
        opacity: .7;
    } */
    50%{
        transform: translate3d(-200px, 200px, 0);
        opacity: 0.7;
    }
    /* 75%{
        transform: translate3d(200px, 200px, 0);
        opacity: 0.7;
    } */
    100%{
        transform: translate3d(0, 0, 0);
        opacity: 1;
    }
}
</style>