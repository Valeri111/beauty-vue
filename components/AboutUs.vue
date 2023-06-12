<template>
  <section id="sobre" class="about-us">
    <div class="container">
      <div class="about-us__banner">
        <picture>
          <source
            srcset="@/assets/images/about-desktop.png"
            media="(min-width: 1200px)"
          />

          <img
            src="@/assets/images/about-mobile.png"
            alt="Três cabeleireiras segurando escova e tesoura"
          />
        </picture>
      </div>

      <div class="about-us__content">
        <h2>О нас</h2>
        <p>
          Салон красоты "CreateYourself" - это современное и элегантное место, где каждый клиент может создать и раскрыть свою уникальную красоту. Салон предлагает широкий спектр профессиональных услуг, предназначенных для ухода за внешностью и повышения самооценки.
        </p>

        <p>
          По приходу в "CreateYourself" вас встретят приветливые и опытные специалисты, готовые предложить индивидуальный подход к каждому клиенту. Салон обладает современным интерьером, создающим комфортную и расслабляющую атмосферу. Здесь вы сможете отвлечься от повседневных забот и насладиться приятным отдыхом.
        </p>

        <p>
          "CreateYourself" предлагает широкий выбор услуг, включая уход за кожей лица, волосами, маникюр, педикюр, массаж и многое другое. Каждый специалист имеет высокий уровень квалификации и следует последним тенденциям в индустрии красоты, чтобы предложить вам наилучшие результаты.
        </p>
        <p>
          В салоне используются только качественные и проверенные продукты, которые помогут вам достичь желаемого эффекта и сохранить здоровье ваших волос и кожи. Техники и процедуры, применяемые в "CreateYourself", основаны на передовых методах и инновационных подходах, чтобы гарантировать вам безопасность и эффективность.
        </p>
        
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutUs',
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';
.about-us {
  padding-top: 5rem;
  background-color: var(--white);

  @include large {
    padding-top: 7.5rem;
  }

  @include x-large {
    padding-top: 10rem;
  }

  & > .container {
    @include x-large {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 4rem;
    }
  }

  &::after {
    @include gradientBorder;
  }

  &__banner {
    margin-left: -1.5rem;
    margin-right: -1.5rem;
    text-align: center;

    @include x-large {
      margin-left: 0;
      margin-right: 0;
    }
  }

  &__content {
    @include x-large {
      max-width: 600px;
    }

    h2 {
      @include title;
      margin-top: 2rem;
      margin-bottom: 1rem;

      @include x-large {
        margin-top: 0;
      }
    }

    p {
      font-size: 1rem;
      line-height: 1.625rem;
    }

    p + p {
      margin-top: 1.25rem;
    }
  }
}
</style>
