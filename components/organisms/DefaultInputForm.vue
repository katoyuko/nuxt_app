<template>
  <b-container fluid>
    <b-row v-for="type in types" :key="type" class="my-1">
      <b-col sm="2" offset="2">
        <label :for="`type-${type}`">
          <code>{{ type.value }}</code>
        </label>
      </b-col>
      <b-col sm="6">
        <b-form-input :id="`type-${type.kye}`" :type="type.key"></b-form-input>
      </b-col>
    </b-row>

    <b-row class="my-1">
      <b-col sm="2" offset="2">
        <Label :label="logo_label"></Label>
      </b-col>
      <b-col sm="6">
        <SelectBox />
      </b-col>
    </b-row>

    <b-row class="my-1">
      <b-col sm="2" offset="2">
        <Label :label="favi_label"></Label>
      </b-col>
      <b-col sm="6">
        <SelectBox />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import Label from "~/components/atoms/Label.vue"
import SelectBox from "~/components/atoms/SelectBox.vue"

export default {
  components: {
    Label,
    SelectBox
  },
  data() {
    return {
      types: [
        { key: "text", value: "フォーム名" },
        { key: "email", value: "通知メール設定" },
        { key: "url", value: "URL" },
        { key: "", value: "モード" },
        { key: "date", value: "開始日時" },
        { key: "date", value: "終了日時" }
      ],
      logo_label: "ロゴ",
      favi_label: "ファビコン"
    }
  }
}
</script>
