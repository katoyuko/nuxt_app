<template>
  <b-container fluid>
    <b-row class="my-1">
      <b-col sm="2" offset="2">
        <Label :label="template_label"></Label>
      </b-col>
      <b-col sm="6">
        <SelectBox />
      </b-col>
    </b-row>
    <div>
      <b-tabs content-class="mt-3">
        <b-tab title="入力">
          <p>
            <InputTab />
          </p>
        </b-tab>
        <b-tab title="確認">
          <p>確認画面</p>
        </b-tab>
        <b-tab title="完了">
          <DoneTab />
        </b-tab>
      </b-tabs>
    </div>
  </b-container>
</template>

<script>
import Label from "~/components/atoms/Label.vue"
import SelectBox from "~/components/atoms/SelectBox.vue"
import InputTab from "~/components/organisms/InputTab.vue"
import DoneTab from "~/components/organisms/DoneTab.vue"

export default {
  components: {
    Label,
    SelectBox,
    InputTab,
    DoneTab
  },
  data() {
    return {
      template_label: "テンプレート"
    }
  }
}
</script>
