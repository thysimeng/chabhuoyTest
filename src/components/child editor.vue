<template>
  <h1>child editor: {{ message }}</h1>
</template>
<script>
export default {
  name: 'childEditor',
  props: {
    message: String
  }
}
</script>
