<template lang="html">
  <div class="">
    <h2 class="label-wrapper">

        <label for="new-todo-input"
                class="label__lg"
               :class="{is_filtering: filtering}">
            <slot></slot>
        </label>
    </h2>
    <input
      @input="onInput"
      type="text"
      id="search-input"
      name="query"
      autocomplete="off"
      class="input__lg"
    />
    <button @click="onReset" class="btn btn__green btn__lg">Reset</button>
  </div>
</template>

<script>

export default {
  props: {
    filtering: {default: false, type: Boolean}
  },
  methods: {
    onReset() {
      document.getElementById('search-input').value = "";
      this.$emit('on-reset')
    },
    onInput(e) {
      this.$emit('on-input', e.target.value)
    }
  }
}
</script>

<style lang="css" scoped>
.is_filtering {
  color: #3cac8a;
}
</style>
