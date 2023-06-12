<template>
  <section id="inicio" class="hero">
    <div class="container">
      <div class="hero__banner">
        <picture>
          <source
            srcset="@/assets/images/hero-desktop.png"
            media="(min-width: 1200px)"
          />

          <img
            src="@/assets/images/hero-mobile.png"
            alt="Cabeleireira utiliando secador de cabelo na cliente"
          />
        </picture>
      </div>

      <div class="hero__content">
        <h1>CreateYourself создавай себя сама</h1>
        <p>
          Салон красоты, который поможет тебе всегда выглядеть на все 100%.
        </p>
        <base-button>Записаться в салон</base-button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TheHero',
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';

.hero {
  padding-top: 7.5rem;

  @include large {
    padding-top: 8.5rem;
  }

  @include x-large {
    padding-top: 9.5rem;
  }

  &::after {
    @include gradientBorder;
  }

  & > .container {
    text-align: center;

    @include large {
      display: flex;
      align-items: center;
      justify-content: space-between;
      text-align: left;
    }
  }

  &__banner {
    margin-left: -1.5rem;
    margin-right: -1.5rem;

    @include large {
      margin-left: 0;
      margin-right: 0;
    }

    @include x-large {
      img {
        max-width: 460px;
      }
    }
  }

  &__content {
    margin-top: 2rem;

    @include large {
      order: -1;
      max-width: 400px;
      margin-top: 0;
    }

    h1 {
      @include title;
      margin-bottom: 1rem;
    }

    p {
      font-size: 1rem;
      line-height: 1.25rem;
      margin-bottom: 2rem;

      @include large {
        font-size: 1.125rem;
        line-height: 1.5rem;
      }
    }

    button {
      margin: auto;

      @include large {
        margin: 0;
      }
    }
  }
}
</style>
