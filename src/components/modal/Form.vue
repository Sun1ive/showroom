<template>
<div :class="{ 'is-active': isActive }" class="modal">
  <div class="modal-background"></div>
  <div class="modal-content">
    <form id="form" @submit.prevent="submitData">
      <div class="close" @click="closeForm"></div>
      <div class="field">
        <label class="label">Ваше имя</label>
        <div class="control">
          <input required class="input is-info" v-model="userData.name" type="text" placeholder="Введите Ваше имя">
        </div>
      </div>
      <div class="field">
        <label class="label">Ваш телефон</label>
        <div class="control">
          <input required class="input is-info" v-model="userData.phone" type="tel" placeholder="Введите Ваш телефон">
        </div>
        <p class="help is-danger" v-if="error">Пожалуйста введите корректный номер</p>
      </div>
      <button type="submit" class="button is-info">Отправить</button>
    </form>
  </div>
</div>
</template>

<script>
import axios from 'axios';

export default {
  props: {
    isActive: {
      type: Boolean,
      required: true,
    },
  },
  data() {
    return {
      error: false,
      userData: {
        name: '',
        phone: null,
      },
    };
  },
  methods: {
    async submitData() {
      try {
        const validate = new RegExp(/^[0-9]+$/);
        if (!validate.test(this.userData.phone)) {
          this.error = true;
          console.log(this.userData.phone);
          this.userData.phone = '';
          return;
        }
        if (this.error === true) {
          this.error = false;
        }
        await axios.post('https://showroom-fc5ff.firebaseio.com/users.json', this.userData);
        Email.send(
          `info@indresser.com`,
          // 'info@indresser.com',
          'sunliveua@gmail.com',
          'Заявка с сайта showroom.indresser.com',
          `Пользователь: ${this.userData.name}   Телефон: ${this.userData.phone}`,
          'mail.adm.tools',
          'info@indresser.com',
          '6oRAaL4x8Ce7',
        );
        this.userData = {
          name: '',
          phone: null,
        };
      } catch (error) {
        console.log(error);
      }
    },
    closeForm() {
      this.$emit('closeForm');
    },
  },
};
</script>

<style scoped>
.modal-content {
  max-width: 550px;
}
#form {
  border-radius: 13px;
  min-height: 100px;
  background-color: #fff;
  padding: 1rem 5rem;
  position: relative;
}
#form .button {
  margin-top: 1.1rem;
}
#form .close {
  position: absolute;
  top: 10px;
  right: 10px;
  background: url('../../assets/close.svg') no-repeat center center;
  width: 25px;
  height: 25px;
  cursor: pointer;
}
</style>