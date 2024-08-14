<template>
    <div class="first__block">
      <div class="first__block__child">
        <div class="container mx-auto">
          <div class="first__block__texts">
            <p>НАЧНИТЕ ЗАРАБАТЫВАТЬ ДО 4% ЕЖЕДНЕВНО</p>
            <h2>Децентрализированный <br> <span> Liquid Staking TON</span></h2>
            <button class="flex justify-between items-center first__block__button">
              <span class="button-text">Начать сейчас</span>
              <img src="/images/right-arrow.png" alt="Arrow" class="button-icon">
            </button>
          </div>
          <img src="/images/bg.png" alt="">
        </div>
      </div>
  </div>
</template>

<script setup>

</script>

<style>
.first__block {
  background-image: url("/images/bg_blue-shadow.png");
  background-position: center;
  background-size: cover;
  height: 92vh;
}

.first__block__child {
  background-image: url("/images/bg_circles.png");
  background-position: center;
  background-size: cover;
  height: 92vh;
}

.first__block__texts {
  display: flex;
  justify-content: center;
  flex-direction: column;
  text-align: center;
  align-items: center;
}

.first__block__texts h2 {
  font-size: 75px;
  font-weight: 700;
  line-height: 80px;
}

.first__block__texts h2 span {
  color: var(--button-bg-color);
}

.first__block__button {
  background: #0098E9;
  border-radius: 999px;
  color: #fff;
  width: 223px;
  height: 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 8px;
}

.first__block__button .button-text {
  flex: 1;
  text-align: center;
  color: #fff;
}

.first__block__button .button-icon {
  background-color: #fff;
  padding: 16px;
  border-radius: 50%;
  margin-left: auto;
}


</style>