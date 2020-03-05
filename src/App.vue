<template>
  <div id="app">
    <div class="container">
      <div class="main-wrapper">
        <button class="back"><img src="/static/img/arrow_back.svg" alt=""> Back to cart</button>

        <div class="main-content">
          <!-- CONTENT -->
          <div class="content">
            <router-view/>
          </div>

          <!-- CART -->
          <Chart/>
        </div>
      </div>
    </div>
    <!-- <router-view/> -->
  </div>
</template>

<script>
import Chart from './components/Chart'
export default {
  name: 'App',
  components: {
    Chart
  }
}
</script>

<style lang="stylus">
// GENERAL
$primary-color = #FF8A00
$secondary-color = #1BD97B
body
  background: #FFFAE6
  font-family: Helvetica, Arial, sans-serif
  font-size: 14px

// CONTAINER
.container
  max-width: 1100px
  margin: 0 auto

// MAIN WRAPPER
.main-wrapper
  background: #ffffff
  border-radius: 4px
  padding: 30px 40px
  margin-top: 55px
  box-shadow: 2px 10px 20px 0 rgba(255, 138, 0, .1)

// BUTTON
button
  background: transparent
  padding: 10px
  border: 0
  &.back
    color: rgba(0,0,0,.6)
    padding-left: 0
    padding-right: 0
    img
      margin-right:10px
      display: inline-block

// CONTENT
.main-content
  margin-top: 24px
  display: flex
  margin-left: -15px
  margin-right: -15px
  & > div
    padding-left: 15px
    padding-right: 15px
  .content
    width: 70%
  .cart
    width: 30%
    .cart-inner
      border-left: 1px solid rgba($primary-color, .2)
      padding-left: 20px
      height: 100%
      h4
        font-size: 24px
        color: $primary-color
      .purchased
        opacity: .6
// DIVIDER
.divider
  width: 80px
  height: 1px;
  background: #D8D8D8
  margin: 20px 0

// TEXT COLORS and STYLES
.text-green
  color: $secondary-color
.weight-bold
  font-weight: bold
</style>
