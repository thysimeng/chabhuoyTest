<template>
<div>
  <h1>Child: {{ message }}</h1>
  <input type="text" v-model="messageProps">
  <button @click="updateChild">Child button</button>
</div>
</template>
<script>
export default {
  name: 'child',
  data() {
    return {
      messageProps: this.message
    }
  },
  props:{
    message: String
  },
  methods:{
    updateChild(){
      this.messageProps = this.messageProps
      this.$emit('childData', this.messageProps)
    }
  }
}
</script>
