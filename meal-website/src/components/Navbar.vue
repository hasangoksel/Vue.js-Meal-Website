<template>
    <div>
        <div v-if="isOpen" class="open-menu" :class="{ 'fadeOutRight': fadeOut }" @animationend="handleAnimationEnd">
            <span @click="closeMenu"><i class="fa-solid fa-xmark"></i></span>
            <ul>
                <li><a href="#home" @click="closeMenu">Home</a></li>
                <li><a href="#about" @click="closeMenu">About Us</a></li>
                <li><a href="#our-menu" @click="closeMenu">Our Menu</a></li>
                <li><a href="#reserve" @click="closeMenu">Reserve A Table</a></li>
                <li><a href="#contact" @click="closeMenu">Contact</a></li>
            </ul>
        </div>
        <nav>
            <div class="container">
                <div class="nav-logo">
                    <a href="#" class="logo">M</a>
                </div>
                <div @click="openMenu" class="hamburger">
                    <div class="hamburger-item"></div>
                    <div class="hamburger-item"></div>
                    <div class="hamburger-item"></div>
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isOpen: false,
            fadeOut: false
        };
    },
    mounted() {
        window.addEventListener("scroll", this.handleScroll);
    },
    methods: {
        openMenu() {
            this.isOpen = true;
            this.fadeOut = false;
        },
        closeMenu() {
            this.fadeOut = true;
        },
        handleAnimationEnd() {
            if (this.fadeOut) {
                this.isOpen = false;
            }
        },
        handleScroll() {
            let scrollValue = window.scrollY;
            let content = document.querySelector("nav");
            let logo = document.querySelector(".logo");

            if (scrollValue > 200) {
                logo.classList.add("scroll");
                content.classList.add("scrolled");
            } else {
                logo.classList.remove("scroll");
                content.classList.remove("scrolled");
            }
        }
    },

    beforeDestroy() {
        window.removeEventListener("scroll", this.handleScroll);
    }
};
</script>

<style scoped>
@keyframes fadeInRight {
    0% {
        opacity: 0;
        right: -300px;
    }

    100% {
        opacity: 1;
        right: 0;
    }
}

@keyframes fadeOutRight {
    0% {
        opacity: 1;
        right: 0;
    }

    100% {
        opacity: 0;
        right: -300px;
    }
}

.open-menu {
    width: 20%;
    height: 100vh;
    background-color: #f8f9fa;
    position: fixed;
    top: 0;
    right: -300px;
    z-index: 99;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    animation: fadeInRight .6s ease 1;
    right: 0;
}

.fadeOutRight {
    animation: fadeOutRight 1s ease 1;
    right: -300px;
}

.open-menu span {
    width: 100%;
    text-align: right;
    padding: 7%;
    margin-top: 7%;
    cursor: pointer;
}

.open-menu span i {
    font-size: 2rem;
}

.open-menu ul {
    margin-top: 50%;
    list-style: none;
}

.open-menu ul li {
    margin-bottom: 14%;
}

.open-menu ul li a {
    text-decoration: none;
    font-size: 1.2rem;
    color: #000;
}
</style>