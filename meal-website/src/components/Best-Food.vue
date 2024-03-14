<template>
     <div ref="bestFood" class="best-food">
        <div class="best-food-title">
            <h2>Find your best food</h2>
            <p>Free Website Template For Restaurants Made by Goksel</p>
        </div>
        <div class="best-food-content">
            <div class="two-card">
                <div class="card-type-h">
                    <div class="card-img-1">
                        <div class="tri-left"></div>
                    </div>
                    <div class="card-content">
                        <h4>VEGIES</h4>
                        <h3>BEEF EMPANADAS</h3>
                        <p>Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.</p>
                        <a href="#" class="card-button">Learn More
                            <i class="fa-solid fa-arrow-right-long"></i>
                        </a>
                    </div>
                </div>
                <div class="card-type-h">
                    <div class="card-content">
                        <h4>FOOD</h4>
                        <h3>BUTTERMILK CHICKEN JIBARITOS</h3>
                        <p>A small river named Duden flows by their place and supplies it with the necessary regelialia.</p>
                        <a href="#" class="card-button">Learn More
                            <i class="fa-solid fa-arrow-right-long"></i>
                        </a>
                    </div>
                    <div class="card-img-2">
                        <div class="tri-right"></div>
                    </div>
                </div>
            </div>
            <div class="one-card">
                <div class="card-type-v">
                    <div class="card-img-3">
                        <div class="tri-top"></div>
                    </div>
                    <div class="card-content">
                        <h4>FOOD</h4>
                        <h3>CHICKEN CHIMICHURRI CROQUETTES</h3>
                        <p>Even the all-powerful Pointing has no control about the blind texts it is an almost unorthographic life.</p>
                        <a href="#" class="card-button" style="margin-top: 12%;">Learn More
                            <i class="fa-solid fa-arrow-right-long"></i>
                        </a>
                    </div>
                </div>
            </div>
          
        </div>
    </div>
</template>
<script>
export default {
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
          this.$refs.bestFood.classList.add('fadeInAnimation');
          observer.unobserve(entry.target); // Gözlemi durdur
        }
      });
    }, options);

    // Gözlemleyiciyi ilgili bölüm üzerinde başlat
    observer.observe(this.$refs.bestFood);
  }
};
</script>

<style scoped>
.fadeInAnimation {
  animation: fadeInBottom 2.3s ease-in-out 1;
}


</style>