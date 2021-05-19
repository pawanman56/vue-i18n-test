<template>
<div>
  <p>{{ $t('hello') }}</p>
  <p>{{ $t('goodbye') }}</p>

  <button @click="setLocale('es')" class="btn">spanish</button>
  <button @click="setLocale('en')" class="btn">English</button>
  <button @click="setLocale('np')" class="btn">Nepali</button>
</div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'HelloI18n',

  methods: {
    setLocale (locale) {
      this.$i18n.locale = locale;
    }
  }
})
</script>
