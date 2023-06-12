<template>
  <section id="price" class="our-price">
    <div class="container">
    <h2>Запись</h2>
    <form @submit.prevent="submitForm">
      <label for="name">Ваше имя:</label>
      <input id="name" v-model="formData.name" type="text" required>
      
      <label for="email">Ваш email:</label>
      <input id="email" v-model="formData.email" type="email" required>
      
      <label for="date">Дата:</label>
      <input id="date" v-model="formData.date" type="date" :min="minDate" :max="maxDate" required>
      
      <label for="time">Время:</label>
      <select id="time" v-model="formData.time" required>
        <option value="" disabled selected>Выберите время</option>
        <option v-for="timeSlot in availableTimeSlots" :key=timeSlot.id>{{ timeSlot }}</option>
      </select>
      
      <label for="procedure">Процедура:</label>
      <select id="procedure" v-model="formData.procedure" required>
        <option value="" disabled selected>Выберите процедуру</option>
        <option v-for="procedure in availableProcedures" :key=procedure.id>{{ procedure }}</option>
      </select>
      
      <label for="master">Мастер:</label>
      <select id="master" v-model="formData.master" required>
        <option value="" disabled selected>Выберите мастера</option>
        <option v-for="master in availableMasters" :key=master.id :value="master.name">{{ master.name }}</option>
      </select>
      
      <button type="submit">Записаться</button>
    </form>
  </div>
	</section>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: '',
        email: '',
        date: '',
        time: '',
        procedure: '',
        master: ''
      },
      availableTimeSlots: [
        '09:00',
        '10:00',
        '11:00',
        '12:00',
        '13:00',
        '14:00',
        '15:00',
        '16:00',
        '17:00'
      ],
      availableProcedures: [
        'Маникюр',
        'Педикюр',
        'Наращивание ногтей'
      ],
      availableMasters: [
        { name: 'Мастер 1', unavailableDates: ['2023-06-15', '2023-06-20'] },
        { name: 'Мастер 2', unavailableDates: ['2023-06-16', '2023-06-21'] },
        { name: 'Мастер 3', unavailableDates: ['2023-06-17', '2023-06-22'] }
      ]
    };
  },
  computed: {
    minDate() {
      const today = new Date();
      return today.toISOString().split('T')[0];
    },
    maxDate() {
      const tomorrow = new Date();
      tomorrow.setDate(tomorrow.getDate() + 7);
      return tomorrow.toISOString().split('T')[0];
    }
  },
  methods: {
    submitForm() {
      // Проверка занятости времени для выбранного мастера
      const selectedMaster = this.availableMasters.find(master => master.name === this.formData.master);
      if (selectedMaster) {
        const unavailableDates = selectedMaster.unavailableDates;
        if (unavailableDates.includes(this.formData.date)) {
          alert('Выбранное время недоступно для выбранного мастера. Пожалуйста, выберите другую дату или время.');
          return;
        }
      }
      
      // Ваш код обработки отправки формы
      // Можно использовать axios или другую библиотеку для отправки запроса на сервер
      // eslint-disable-next-line no-console
      console.log(this.formData);
    }
  }
};
</script>



<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';

.our-price {
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

 /* Стили для полей ввода текста */
  input[type=text],
  input[type=email],
  select {
    border: none;
    border-bottom: 2px solid #59CCAF;
    outline: none;
    padding: 5px;
    font-size: 16px;
    margin-bottom: 10px;
  }

  /* Стили для кнопки */
  button {
    background-color: #59CCAF;
    color: #fff;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
  }

  /* Стили для заголовка */
  h2 {
    color: #59CCAF;
    margin-bottom: 20px;
  }

	form {
		display: flex;
    flex-direction: column;
	}
}
</style>
