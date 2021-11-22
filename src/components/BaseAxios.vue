<template>
  <div style="margin-top: 10px">{{ title }}</div>
  <div style="margin-top: 10px">{{ name }}</div>
</template>
<script setup>
import axios from 'axios'

const props = defineProps({
  name: {
    type: String,
    default: '',
  },
  title: {
    type: String,
    default: '',
  },
  data: {
    type: [String, Number, Array],
    default: '',
  },
  url: {
    type: String,
    default: '',
  },
  methods: {
    type: String,
    default: '',
  },
})

loadAction()

async function loadAction() {
  let res = await axios({
    method: props.methods,
    url: props.url,
    data: props.data,
  })
  console.log('Response =>', res)
}
</script>
