<template>
  <div>
    <Label :label="label"></Label>
    <Textbox />
  </div>
</template>

<script>
import Label from "~/components/atoms/Label.vue"
import Textbox from "~/components/atoms/Textbox.vue"

export default {
  components: {
    Label,
    Textbox
  },
  data() {
    return {
      label: "フォーム名"
    }
  }
}
</script>
