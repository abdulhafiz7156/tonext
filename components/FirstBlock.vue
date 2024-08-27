<template>
    <div class="first__block">
      <div class="first__block__child relative">
        <div class="container mx-auto">
          <div class="first__block__texts flex-col flex justify-center text-center items-center">
            <p>НАЧНИТЕ ЗАРАБАТЫВАТЬ ДО 4% ЕЖЕДНЕВНО</p>
            <h2>Децентрализированный <br> <span> Liquid Staking TON</span></h2>
            <button class="flex justify-between items-center first__block__button flex justify-center items-center">
              <span class="button-text text-center">Начать сейчас</span>
              <img src="/images/right-arrow.png" alt="Arrow" class="button-icon">
            </button>
          </div>
          <img src="/images/bg.png" alt="">
          <div class="first__block__tons">
            <img src="/images/bg_ton1.png" alt="">
            <img src="/images/bg_ton2.png" alt="">
          </div>
        </div>
      </div>
  </div>
</template>

<script setup>

</script>

<style>


.first__block__child {
  background-image: url("/images/bg_circles.png");
  background-position: center;
  background-size: cover;
  height: 92vh;
}

.first__block__texts {
  padding-top: 135px;
}

.first__block__texts h2 {
  font-size: 75px;
  font-weight: 700;
  line-height: 80px;
}

.first__block__texts h2 span {
  color: var(--button-bg-color);
}

.first__block__texts p {
  font-size: 14px;
  font-weight: 500;
  line-height: 14px;
  letter-spacing: 5px;
}

.first__block__button {
  background: #0098E9;
  border-radius: 999px;
  color: #fff;
  width: 223px;
  height: 60px;
  padding: 0 8px;
  margin-top: 40px;
}

.first__block__button .button-text {
  flex: 1;
  color: #fff;
}

.first__block__button .button-icon {
  background-color: #fff;
  padding: 16px;
  border-radius: 50%;
  margin-left: auto;
}

.first__block__tons img {
  position: absolute;
}

.first__block__tons img:first-child {
  top: 200px;
  width: calc(17% - 100px);
  animation: moveLeftBottom 5s ease-in-out infinite;
}

.first__block__tons img:last-child {
  top: 150px;
  right: 100px;
  width: calc(20% - 100px);
  animation: moveRightTop 5s ease-in-out infinite;
}

@keyframes moveRightTop {
  0%, 100% {
    transform: translateY(0) translateX(0);
  }
  50% {
    transform: translateY(-40px) translateX(40px);
  }
}

@keyframes moveLeftBottom {
  0%, 100% {
    transform: translateY(0) translateX(0);
  }
  50% {
    transform: translateY(40px) translateX(-40px);
  }
}


</style>