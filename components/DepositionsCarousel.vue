<template>
  <section id="depoimentos" class="depositions">
    <div class="container">
      <h2 class="depositions__title">Отзывы тех, кто был здесь</h2>

      <client-only>
        <carousel
          :per-page="1"
          :per-page-custom="[[768, 2]]"
          pagination-active-color="#69B99D"
          pagination-color="#E4E4E4"
        >
          <slide v-for="author in authors" :key=author.id>
            <figure class="testimony">
              <blockquote class="testimony__quote">
                <p>
                  <span>&ldquo;</span>
                  {{ author.text }}
                </p>
              </blockquote>

              <figcaption class="testimony__author">
                <img v-if="author.name == 'Вероника'" src="@/assets/images/avatarveronika.png" :alt="author.name" />
                <img v-if="author.name == 'Мария'" src="@/assets/images/avatarmasha.png" :alt="author.name" />
                <img v-if="author.name == 'Оксана'" src="@/assets/images/avataroksana.png" :alt="author.name" />
                <img v-if="author.name == 'Елена'" src="@/assets/images/avatar.png" :alt="author.name" />
                <img v-if="author.name == 'Елизавета'" src="@/assets/images/avatarliza.png" :alt="author.name" />
                <cite>{{ author.name }}</cite>
              </figcaption>
            </figure>
          </slide>
        </carousel>
      </client-only>
    </div>
  </section>
</template>

<script>
export default {
  name: 'DepositionsCarousel',
  data() {
    return {
      authors:   [
        {id: 1, name: 'Вероника', text: 'Огромная благодарность Анастасии за такой качественный маникюр!  Буду рекомендовать своим))'},
        {id: 2, name: 'Мария', text: 'Всем советую мастера Алину, она моя находка!  Боялась ходить на маникюр из-за страха, что порежут кутикулу, сменила кучу мастеров. Уже даже перестала делать маникюр, и тут мне советуют Алину. Решила попробовать в положений раз, и не зря.  Не мастер, а подарок! Все так аккуратно, не больно  и при этом быстро, я в полном восторге. Теперь свои руки доверяю только ей)'},
        {id: 3, name: 'Оксана', text: 'Очень нравится делать брови у мастера Яны! Все очень аккуратно и быстро! Качество на высшем уровне. В салоне приятная атмосфера и приветливые сотрудники.'},
        {id: 4, name: 'Елена', text: 'Впервые побывала я в этом замечательном салоне по острой необходимости, так сказать, и нисколько не пожалела! Мне пришёлся по душе необычный интерьер, вежливый и отзывчивый персонал, и, конечно же, высококачественный макияж от мастера Яны.'},
        {id: 5, name: 'Елизавета', text: 'Вежливость и участливость девушек невероятно радует. Спасибо Вам за работу. Ещё хочется выразить особую благодарность мастеру маникюра. Заботливые и чуткие руки :) Профессионал, при этом с чутким и ненавязчивым пониманием желаний клиента. Спасибо Вам. Получили массу положительных эмоций от соприкосновения с данным салоном. Спасибо за Вашу работу! Процветания Вам!'},
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';

.depositions {
  padding-top: 5rem;
  background-color: var(--white);

  @include large {
    padding-top: 7.5rem;
  }

  @include x-large {
    padding-top: 10rem;
  }

  &::after {
    @include gradientBorder;
  }

  &__title {
    @include title;
    max-width: 260px;
    margin-bottom: 4rem;

    @include medium {
      max-width: 480px;
      text-align: center;
      margin: 0 auto 4rem;
    }
  }
}

.testimony {
  padding: 2rem;

  &__quote {
    margin-bottom: 1.5rem;

    p {
      font-size: 1rem;
      line-height: 1.625rem;
      color: var(--green-900);
      position: relative;

      span {
        font-family: serif;
        font-size: 2.5rem;
        font-weight: bold;
        position: absolute;
        top: -0.375rem;
        left: -1.875rem;
        color: var(--green-500);
      }
    }
  }

  &__author {
    display: flex;
    align-items: center;
    gap: 0.5rem;

    cite {
      font-size: 1rem;
      line-height: 1.75rem;
      font-style: normal;
      color: var(--gray-500);
    }
  }
}
</style>
