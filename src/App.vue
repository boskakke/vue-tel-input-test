<script setup>
import { VueTelInput } from 'vue-tel-input'
import 'vue-tel-input/vue-tel-input.css'
import { ref, reactive } from 'vue'

const phone = ref(null)
const bindProps = reactive({
  mode: 'international',

  name: 'phone',
  maxLen: 25,

  inputOptions: {
    required: true,
    autocomplete: 'off',
    placeholder: 'Enter a phone number',
    showDialCode: true
  }
})
</script>

<template>
  <VueTelInput v-model="phone" v-bind="bindProps"></VueTelInput>
</template>
