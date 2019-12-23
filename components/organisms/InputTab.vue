<template>
  <b-container fluid>
    <b-row class="my-1">
      <b-col sm="3" offset="3">
        <Textbox />
      </b-col>
      <b-col sm="3">
        <SelectBox />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import SelectBox from "~/components/atoms/SelectBox.vue"
import Textbox from "~/components/atoms/Textbox.vue"

export default {
  components: {
    SelectBox,
    Textbox
  }
}
</script>
