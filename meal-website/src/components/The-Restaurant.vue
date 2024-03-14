<template>
    <div ref="about" id="about" class="the-restaurant">
        <div class="the-restaurant-content">
            <h2>The Restaurant</h2>
            <p>Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean. <br/> <br/> It is a paradisematic country, in which roasted parts of sentences fly into your mouth.</p>
           
        </div>
        <div class="the-restaurant-image">
            <img src="../../public/img/bg.webp" alt="Background">
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
          this.$refs.about.classList.add('fadeInAnimation');
          observer.unobserve(entry.target); // Gözlemi durdur
        }
      });
    }, options);

    // Gözlemleyiciyi ilgili bölüm üzerinde başlat
    observer.observe(this.$refs.about);
  }
};
</script>
<style scoped>
.fadeInAnimation {
  animation: fadeIn 2.3s ease-in-out 1;
}

</style>