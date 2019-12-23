<template>
  <button :type="type" class="button--green">{{ button }}</button>
</template>

<script>
export default {
  props: ["button"]
}
</script>
