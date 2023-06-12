<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__content">
        <img src="@/assets/images/logo-white.svg" alt="Beauty Salon" />

        <p>©2023 CreateYourself.</p>
        <p>Все права защищены.</p>
      </div>

      <div class="footer__social">
        <a href="#">
          <img src="@/assets/images/instagram.svg" alt="Instagram" />
        </a>

        <a href="#">
          <img src="@/assets/images/facebook.svg" alt="Facebook" />
        </a>

        <a href="#">
          <img src="@/assets/images/youtube.svg" alt="Youtube" />
        </a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'TheFooter',
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';

.footer {
  padding: 4rem 0;
  background-color: var(--green-500);

  & > .container {
    @include medium {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
  }

  &__content {
    img {
      margin-bottom: 1.5rem;

      @include large {
        width: 200px;
      }
    }

    p {
      color: var(--gray-300);

      & + p {
        margin-top: 0.75rem;
      }
    }
  }

  &__social {
    display: flex;
    align-items: center;
    gap: 2rem;
    margin-top: 2rem;
  }
}
</style>
