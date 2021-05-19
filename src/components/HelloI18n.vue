<template>
<div>
  <p>{{ $t('hello') }}</p>
  <p>{{ $t('message') }}</p>
</div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'HelloI18n'
})
</script>

<i18n>
{
  "en": {
    "hello": "Hello i18n in SFC!"
  },
  "es": {
    "hello": "Hola!"
  }
}
</i18n>
