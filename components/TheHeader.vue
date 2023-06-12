<template>
  <header class="header">
    <div class="container">
      <img class="logo" src="@/assets/images/logo.svg" alt="CreateYourself" />

      <button type="button" class="header__toggle" @click="openMenu()">
        <img src="@/assets/images/menu.svg" alt="" />
      </button>

      <nav class="navigation" :class="{ active: activeMenu }">
        <button type="button" class="navigation__close" @click="closeMenu()">
          <img src="@/assets/images/close.svg" alt="" />
        </button>

        <ul class="navigation__menu">
          <li v-for="link in links" :key="link.id" class="navigation__item">
            <a
              class="navigation__link"
              :href="`${link.id}`"
              :class="{ active: link.id === activeLink }"
             
            >
              {{ link.label }}
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'TheHeader',
  data() {
    return {
      activeMenu: false,
      activeLink: 'inicio',
      links: [
        { label: 'Главная', id: '/' },
        { label: 'О нас', id: '/#sobre' },
        { label: 'Акции', id: '/#akcii' },
        { label: 'Примеры работ', id: '/#raboty' },
        { label: 'Услуги', id: '/price' },
        { label: 'Отзывы', id: '/#depoimentos' },
        { label: 'Запись', id: '/zapici' },
        { label: 'Контакты', id: '/#contato' },
      ],
    }
  },
  methods: {
    openMenu() {
      this.activeMenu = true
    },
    closeMenu() {
      this.activeMenu = false
    },
    handleActiveLink(id) {
      if (!window.matchMedia('(min-width: 768px)').matches) {
        this.closeMenu()
      }

      this.activeLink = id
      const section = document.getElementById(id)
      section.scrollIntoView({ behavior: 'smooth' })
    },
  },
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';
.header {
  position: fixed;
  z-index: 10;
  width: 100%;
  height: 4.5rem;
  border-bottom: 1px solid var(--gray-400);
  background-color: #01251B;

  & > .container {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__toggle {
    background-color: transparent;
    border: 0;
    font-size: 0;
    width: 2.25rem;
    height: 2.25rem;

    @include medium {
      display: none;
    }
  }
}

.logo {
  width: 9rem;

  @include large {
    width: 10rem;
  }
}

.navigation {
  position: fixed;
  inset: 0;
  height: 100%;
  width: 100%;
  background-color: var(--white);

  display: none;
  align-items: center;
  justify-content: center;

  &.active {
    display: flex;
  }

  @include medium {
    display: block;
    position: static;
    background-color: transparent;
    height: auto;
    width: auto;
  }

  &__close {
    position: absolute;
    top: 24px;
    right: 24px;

    font-size: 0;
    border: 0;
    background-color: transparent;

    @include medium {
      display: none;
    }
  }

  &__menu {
    display: flex;
    flex-direction: column;
    text-align: center;
    gap: 4rem;

    @include medium {
      flex-direction: row;
      gap: 2rem;
    }
  }

  &__link {
    font-family: 'Poppins', sans-serif;
    font-weight: 700;
    font-size: 1.875rem;
    color: var(--green-900);

    &.active,
    &:hover {
      color: var(--green-500);
    }

    @include medium {
      font-family: 'DM Sans', sans-serif;
      font-size: 1rem;
      font-weight: 400;
      height: 4.5rem;

      display: flex;
      align-items: center;
      border-bottom: 2px solid transparent;
      transition: 200ms;

      &.active,
      &:hover {
        border-color: var(--green-500);
      }
    }
  }
}
</style>
