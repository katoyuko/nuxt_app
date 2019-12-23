<template>
  <b-form-select v-model="selected" :options="options"></b-form-select>
</template>

<script>
export default {
  data() {
    return {
      selected: null,
      options: [
        { value: null, text: "選択してください" },
        { value: "template", text: "test1" },
        { value: "template", text: "test2" },
        { value: "template", text: "test3" }
      ]
    }
  }
}
</script>
