<template>
  <div class="second__block__shadow pt-100 mt-100 relative">
    <div class="container mx-auto second__block flex">
      <div class="second__block__text">
        <Badge icon="check-icon" />
        <h2 class="my-4">Начните стейкать, зарабатывайте и наслаждайтесь наградами</h2>
        <p>
          Ощутите рост вашего баланса TON прямо в вашем кошельке. Хотите узнать больше?
          <br> <br>
          Прокрутите страницу вниз, чтобы узнать, как это работает и в чем заключаются его основные преимущества.
        </p>
      </div>
      <div class="second__block__img ml-56">
        <img src="/images/second_block.svg" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
}
</script>

<style>
.second__block__shadow {
  box-shadow: 0 -174px 77px rgb(255 255 255);
  z-index: 999;
}

.second__block__text h2{
  font-size: 40px;
  font-weight: 800;
  line-height: 50px;
  width: 610px;
}

.second__block__text p{
  width: 560px;
}

.second__block {
  z-index: 999;
}
</style>