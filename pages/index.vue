<template>
  <div class="container">
    <div>
      <DefaultInputForm />
      <CreateInputForm />
      <Btn :button="preview_btn"></Btn>
      <Btn :button="save_btn"></Btn>
      <Btn :button="comfirm_btn"></Btn>
    </div>
  </div>
</template>

<script>
import DefaultInputForm from "~/components/organisms/DefaultInputForm.vue"
import CreateInputForm from "~/components/organisms/CreateInputForm.vue"
import Btn from "~/components/atoms/Btn.vue"

export default {
  components: {
    DefaultInputForm,
    CreateInputForm,
    Btn
  },
  data() {
    return {
      preview_btn: "プレビュー",
      save_btn: "一時保存",
      comfirm_btn: "確認画面へ進む"
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
}
</style>
