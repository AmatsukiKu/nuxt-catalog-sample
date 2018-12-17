<template>
  <nuxt-link class="button" :to="to" :class="`button--${this.buttonTheme}`">
    <slot />
  </nuxt-link>
</template>
<script>
export default {
  props: {
    to: {
      required: true,
      validator(value) {
        return typeof value === 'string' || typeof value === 'object'
      }
    },
    theme: {
      type: String,
      default: 'default'
    },
    disabled: {
      type: Boolean,
      default: false
    },
  },
  computed: {
    buttonTheme: function () {
      return this.disabled ? 'disabled' : this.theme
    },
    buttonClasses: function () {
      return [
        ,
      ]
    }
  }
}
</script>
<style scoped>
.button {
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: auto;
  min-height: 48px;
  font-size: 1.6rem;
  text-align: center;
  border: 2px solid transparent;
  border-radius: 24px;
  padding-left: 36px;
  padding-right: 36px;
  font-weight: 400;
  cursor: pointer;
  line-height: 1;
}
.button--default {
  color: #000;
  background-color: transparent;
  border-color: #000;
}
.button--black {
  color: #fff;
  background-color: #000;
  border-color: #000;
}
.button--blue {
  color: #fff;
  background-color: #243d87;
  border-color: #243d87;
}
.button--red {
  color: #fff;
  background-color: #D42127;
  border-color: #D42127;
}
.button--disabled {
  color: #fff;
  background-color: #dfe0e2;
  border-color: #dfe0e2;
  pointer-events: none;
  cursor: default;
}
.button--hoverable {
  transition-property: opacity;
  transition-duration: .2s;
  transition-timing-function: ease-in-out;
}
.button--hoverable:hover {
  opacity: 0.8;
}
</style>