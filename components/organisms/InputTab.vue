<template>
  <b-container fluid>
    <b-row class="mt-2">
      <b-col sm="2">
        <label for="title">タイトル</label>
      </b-col>
      <b-col sm="10">
        <b-input id="title" placeholder="キャンペーン応募"></b-input>
      </b-col>
    </b-row>
    <b-row class="mt-2">
      <b-col sm="2">
        <label for="textarea">説明</label>
      </b-col>
      <b-col sm="10">
        <b-form-textarea id="textarea" placeholder="こちらの"></b-form-textarea>
      </b-col>
    </b-row>
    <b-card bg-variant="light">
      <b-row class="my-1">
        <b-col sm="4" offset="1">
          <Textbox />
        </b-col>
        <b-col sm="4">
          <SelectBox />
        </b-col>
        <b-col sm="2">
          <b-button @click="decrement" variant="danger">削除</b-button>
        </b-col>
      </b-row>
    </b-card>
    <b-row sm="2">
      <b-button @click="increment" variant="primary">項目を追加</b-button>
    </b-row>
    <b-row class="my-1">
      <b-col sm="2" offset="2">
        <Label :label="ogpimg_label"></Label>
      </b-col>
      <b-col sm="6">
        <SelectBox />
      </b-col>
    </b-row>
    <b-row class="my-1">
      <b-col sm="2" offset="2">
        <Label :label="ogptag_label"></Label>
      </b-col>
      <b-col sm="6">
        <SelectBox />
      </b-col>
    </b-row>
  </b-container>
</template>
<script>
import SelectBox from "~/components/atoms/SelectBox.vue"
import Textbox from "~/components/atoms/Textbox.vue"
import Label from "~/components/atoms/Label"

export default {
  components: {
    SelectBox,
    Textbox,
    Label
  },
  data() {
    return {
      ogpimg_label: "OGP画像",
      ogptag_label: "OGPタグ"
    }
  }
}
</script>
