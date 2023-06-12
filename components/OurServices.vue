<template>
  <section class="our-services">
    <div class="container h-mb3">
      <h2 id="akcii" class="our-services__title">Акции</h2>
       <picture>
          <source
            srcset="@/assets/images/sert.png"
            media="(min-width: 1200px)"
          />

          <img
            src="@/assets/images/sert-mobile.png"
            alt="akcii"
          />
        </picture>
    </div>
    <div class="container">
    
      <h2 id="raboty" class="our-services__title">Примеры работ</h2>
      <p class="our-services__text">
       
      </p>

      <ul class="our-services__list">
        <li class="our-services__item">
          <img src="@/assets/images/photo_1.png" max-height="325px" alt="" />
          <h3>Комбинированный маникюр</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_2.png" max-height="325px" alt="" />
          <h3>Наращивание ногтей</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_3.png" max-height="325px" alt="" />
          <h3>Восстановление архитектуры</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_4.png" max-height="325px" alt="" />
          <h3>Коррекция+окрашивание, бровкой+ламинирование</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_5.png" max-height="325px" alt="" />
          <h3>Покрытие гель-лак</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_6.png" max-height="325px" alt="" />
          <h3>Восстановление архитектуры + покрытие</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_7.png" max-height="325px" alt="" />
          <h3>Восстановление архитектуры + покрытие</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_8.png" max-height="325px" alt="" />
          <h3>Гель-лак</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_9.png" max-height="325px" alt="" />
          <h3>Окрашивание + коррекция + ламинирование</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_10.png" max-height="325px" alt="" />
          <h3>Коррекция + ламинирование</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_11.png" max-height="325px" alt="" />
          <h3>Причёска на выпускной</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_12.png" max-height="325px" alt="" />
          <h3>Локоны</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_13.png" max-height="325px" alt="" />
          <h3>Низкий хвост</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_14.png" max-height="325px" alt="" />
          <h3>Макияж “натуральный”</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_15.png" max-height="325px" alt="" />
          <h3>Дневной макияж</h3>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/photo_16.png" max-height="325px" alt="" />
          <h3>Коррекция + окрашивание + долговременная укладка</h3>
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';

.our-services {
  padding-top: 3rem;

  @include large {
    padding-top: 3.5rem;
  }

  @include x-large {
    padding-top: 10rem;
  }

  &::after {
    @include gradientBorder;
  }

  &__title {
    @include title;
    margin-bottom: 1rem;

    @include medium {
      text-align: center;
    }
  }

  &__text {
    font-size: 1rem;
    line-height: 1.625rem;
    color: var(--green-900);
    margin-bottom: 4rem;

    @include medium {
      text-align: center;
      max-width: 520px;
      margin: 0 auto 4rem;
    }

    a {
      color: var(--green-500);
      font-weight: 700;

      &:hover {
        text-decoration: underline;
      }
    }
  }

  &__list {
    display: grid;
    gap: 1.5rem;

    @include medium {
      grid-template-columns: repeat(2, 1fr);
    }

    @include large {
      grid-template-columns: repeat(3, 1fr);
    }
  }
  .h-mb3 {
    margin-bottom: 3rem;
  }

  &__item {
    padding: 3.75rem 2rem;
    background: var(--gray-300);
    box-shadow: 0px 0px 12px rgba(0, 0, 0, 0.08);
    border-bottom: 4px solid var(--green-500);
    text-align: center;

    img {
      margin-bottom: 1.5rem;
    }

    h3 {
      font-size: 1.5rem;
      line-height: 2.25rem;
      margin-bottom: 0.75rem;
    }

    p {
      font-size: 1rem;
      line-height: 1.625rem;
    }
  }
}
</style>
