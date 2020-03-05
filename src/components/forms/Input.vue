<template>
  <div class="form-field">
    <div class="form-field__control">
      <input @input="$emit('input', $event.target.value)" autocomplete="off" :id="id" type="text" class="form-field__input" value="" placeholder=" " />
      <label :for="id" class="form-field__label">{{ label }}</label>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Input',
  props: {
    id: String,
    label: String
  }
}
</script>

<style lang="stylus" scoped>
$primary-color = #000
$animation-duration = 0.2s
label-inactive()
  font-size: 16px
  transform: translateY(-1px)
label-active()
  font-size: 13px
  transform: translateY(-14px)
.form-field
  display: block
  margin-bottom: 10px
  padding-bottom:10px
.form-field__label
  label-active()
  display: block
  font-weight: normal
  left: 0
  margin: 0
  padding: 18px 12px 0
  position: absolute
  top: 0
  transition: all $animation-duration
  width: 100%
  color: #000000
  opacity: .4
.form-field__control
  overflow: hidden
  position: relative
  width: 100%
  border: 1px solid #ccc
.form-field__bar
  bottom: 0
  content: ""
  display: block
  left: 0
  margin: 0 auto
  position: absolute
  right: 0
  transform: scaleX(0)
  transition: all $animation-duration
  width: 1%
.form-field__input
  appearance: none
  background: transparent
  border: 0
  color: #333
  display: block
  font-size: 16px
  margin-top: 20px
  outline: 0
  padding: 0 12px 10px 12px
  width: 100%
  // IE 10-11
  &:-ms-input-placeholder
    ~ .form-field__label
      label-inactive()
  // All other browsers except Edge
  &:placeholder-shown
    ~ .form-field__label
      label-inactive()
  &:focus
    ~ .form-field__label
      color: #000
      label-active()
    ~ .form-field__bar
      border-bottom: 2px solid $primary-color
      transform: scaleX(150)
.form-field__textarea
  height: 150px
</style>
