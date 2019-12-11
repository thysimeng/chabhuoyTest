<template>
<div>
  <h1>hello: {{ message }}</h1>
  <input type="text" v-model="messageUpdate">
  <button @click="updateData">Update data</button>
  <child :message="message" @childData="message = $event"></child>
  <childEitor :message="message"></childEitor>
</div>
</template>

<script>

import child from './child'
import childEitor from './child editor'
export default {
  name: 'parent',
  data (){
    return {
      message: 'parent',
      messageUpdate: 'Test'
    }
  },
  methods: {
    updateData () {
      this.message = this.messageUpdate
    }
  }
  ,
  components: {
    child,
    childEitor
  }
}
</script>
