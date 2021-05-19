<template>
<div>
  <!-- <p>{{ $t('hello', { name }) }}</p>
  <p>{{ $t('goodbye') }}</p>
  <p>{{ $t('email', { email }) }}</p>

  <p>{{ $tc('car', 2) }}</p>
  <p>{{ $tc('person', 0) }}</p>
  <p>{{ $tc('person', 1) }}</p>
  <p>{{ $tc('person', 5) }}</p> -->

  <p>{{ $d(new Date(), 'short') }}</p>
  <p>{{ $d(new Date(), 'short', 'en-GB') }}</p>

  <p>{{ $d(new Date(), 'long') }}</p>
  <p>{{ $d(new Date(), 'long', 'en-GB') }}</p>

  <button @click="setLocale('en')" class="btn">English</button>
  <button @click="setLocale('es')" class="btn">Spanish</button>
  <button @click="setLocale('np')" class="btn">Nepali</button>
</div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'HelloI18n',

  data () {
    return {
      name: 'Hari',
      email: 'pawan@mail.com'
    };
  },

  methods: {
    setLocale (locale) {
      this.$i18n.locale = locale;
      localStorage.setItem('locale', locale);
    }
  }
})
</script>
