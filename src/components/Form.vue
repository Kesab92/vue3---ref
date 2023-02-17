<template>
  <div class="s-Form">
    <p class="s-Message">{{ message }}</p>
    <input
      class="s-Message__holder"
      type="text"
      placeholder="type something..."
      v-model="message"
    />
    <button class="s-Button" @click="onSubmit">submit</button>
  </div>
</template>
<script>
import { ref, reactive } from 'vue';
export default {
  setup() {
    const message = ref('');
    const onSubmit = () => {
      alert(`The typed message is ${message.value}`);
    };
    return {
      message,
      onSubmit,
    };
  },
};
</script>
<style>
.s-Form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.s-Message {
  color: green;
}
.s-Message__holder {
  height: 40px;
}
.s-Button {
  color: white;
  width: 100px;
  background-color: green;
}
</style>
