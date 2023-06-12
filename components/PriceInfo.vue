<template>
  <section id="price" class="our-services">
    <div class="container">
      <h2 class="our-services__title">Услуги</h2>
      <p class="our-services__text">
        Салон красоты "CreateYourself" - это место, где вы можете расслабиться, отдохнуть и позволить себе быть настоящими. Здесь вы найдете все необходимое для создания своего неповторимого образа и подчеркивания своей естественной красоты.
      </p>

      <ul class="our-services__list">
        <li class="our-services__item">
          <img src="@/assets/images/nails.svg" alt="" />
          <h3>Маникюр</h3>
          <p>
            Мы любим аккуратные и ухоженные ногти. Любим их накрашенными и естественными. Любим, когда они крепкие и здоровые. Поэтому используем лаки и средства ухода марки : Grape, OneNail, KIEMI.  Это динамичный и светский бренд, который появился недавно, но уже покорил ключевые глянцевые издания - VOGUE, ELLE, VANITY FAIR, GIOIA. В составе продукции этой марки нет толуола и других вредных веществ
          </p>
          <table class="table">
            <thead>
              <tr>
                <th>Услуга</th>
                <th width="150px">Цена</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Классический маникюр (+ снятие)</td>
                <td>30 рублей </td>
              </tr>
              <tr>
                <td>Комбинированный маникюр</td>
                <td>30 рублей</td>
              </tr>
              <tr>
                <td>Мужской маникюр</td>
                <td>45 рублей </td>
              </tr>
              <tr>
                <td>Покрытие ель-лак</td>
                <td>50 рублей</td>
              </tr>
              <tr>
                <td>Покрытие с восстановлением архитектуры</td>
                <td>60 рублей </td>
              </tr>
              <tr>
                <td>Наращивание ногтей</td>
                <td>75 рублей </td>
              </tr>
              <tr>
                <td>Френч / стемпинг</td>
                <td>5 рублей </td>
              </tr>
              <tr>
                <td>Снятие без покрытия последующего</td>
                <td>10 рублей</td>
              </tr>
            </tbody>
          </table>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/woman-brow.svg" alt="" />
          <h3>Брови</h3>
          <p>
            Можно долго по утрам рисовать идеальные брови, а можно прийти к нам. Мы подберем вам форму и оттенок подходящие именно вашему лицу. То же самое можем сказать. Избавьте себя от этой рутины в начале дня, пусть брови накрасит вам кто-то другой. Мы работаем с красителем Bronsun, который держится 3-4 недели.
          </p>
          <table class="table">
            <thead>
              <tr>
                <th>Услуга</th>
                <th width="150px">Цена</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Комплекс брови [форма | цвет | долговременная укладка]</td>
                <td>50 рублей </td>
              </tr>
              <tr>
                <td>Архитектура бровей</td>
                <td>35 рублей </td>
              </tr>
              <tr>
                <td>Окрашивание бровей</td>
                <td> 40 рублей</td>
              </tr>
              <tr>
                <td>Окрашивание ресниц</td>
                <td>40 рублей </td>
              </tr>
              <tr>
                <td>Ламинирование ресниц</td>
                <td>50 рублей </td>
              </tr>
              <tr>
                <td>Долговременная укладка бровей</td>
                <td>40 рублей</td>
              </tr>
            </tbody>
          </table>
        </li>
        <li class="our-services__item">
          <img src="@/assets/images/makeup.svg" alt="" />
          <h3>Макияж</h3>
          <p>
           Высокостойкая и безопасная декоративная косметика, используемая в работе, позволит свести беспокойства на «нет». Будьте уверены макияж будет держаться на протяжении всего вечера. Вы же будете на празднике самой главной героиней. 
          </p>
          <table class="table">
            <thead>
              <tr>
                <th>Услуга</th>
                <th width="150px">Цена</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Макияж дневной-лайт</td>
                <td>45 рублей</td>
              </tr>
              <tr>
                <td>Макияж дневной/деловой</td>
                <td>50 рублей</td>
              </tr>
              <tr>
                <td>Макияж вечерний</td>
                <td>70 рублей</td>
              </tr>
              <tr>
                <td>Макияж вечерний сложный/свадебный</td>
                <td>90 рублей</td>
              </tr>
              <tr>
                <td>Пучковое наращивание ресниц</td>
                <td>15 рублей</td>
              </tr>
              <tr>
                <td>Подготовка кожи к макияжу (демакияж, скраб, маска, крем)</td>
                <td>20 рублей</td>
              </tr>
            </tbody>
          </table>
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';

.our-services {
  padding-top: 5rem;

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
      grid-template-columns: repeat(1, 1fr);
    }

    @include large {
      grid-template-columns: repeat(1, 1fr);
    }
  }

  &__item {
    padding: 3.75rem 2rem;
    background: var(--gray-300);
    box-shadow: 0px 0px 12px rgba(0, 0, 0, 0.08);
    border-bottom: 4px solid var(--green-500);
    text-align: center;

    img {
      width: 150px;
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
  .table {
	width: 100%;
	border: none;
	margin-bottom: 20px;
  }
  .table thead th {
    padding: 10px;
    font-weight: 500;
    font-size: 16px;
    line-height: 20px;
    text-align: left;
    color: var(--green-500);
    border-top: 2px solid var(--green-900);
    border-bottom: 2px solid var(--green-900);
  }
  .table tbody td {
    padding: 10px;
    font-size: 14px;
    line-height: 20px;
    color: var(--green-500);
    border-top: 1px solid var(--green-900);
  }
  .table tbody tr:nth-child(1) td{
    border-top: none;
  }
}
</style>
