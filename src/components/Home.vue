<template>
  <main class="home">
    <section>
      <!-- HEADLINE -->
      <div class="heading d-flex justify-content-between align-items-center">
        <h2>Delivery Details</h2>

        <div>Send as dropshipper</div>
      </div>

      <form>
        <div class="row">
          <div class="col">
            <jm-input label="Name" id="name" v-model="payload.name"/>
            <jm-input label="Phone number" id="phone" v-model="payload.phone"/>
            <jm-textarea label="Delivery Address" id="address" v-model="payload.phone"/>
          </div>
          <div class="col">
            <jm-input label="Dropshipper name" id="dropshipper_name" v-model="dropshipper.name"/>
            <jm-input label="Dropshipper phone" id="dropshipper_phone" v-model="dropshipper.name"/>
          </div>
        </div>
      </form>
    </section>
  </main>
</template>

<script>
import Input from './forms/Input'
import TextArea from './forms/TextArea'
export default {
  name: 'Home',
  components: {
    'jm-input': Input,
    'jm-textarea': TextArea
  },
  data () {
    return {
      payload: {
        name: '',
        phone: '',
        address: ''
      },
      dropshipper: {
        name: '',
        phone: ''
      }
    }
  }
}
</script>
<style lang="stylus" scoped>
  .heading
    line-height:1
    margin-bottom: 36px
    h2
      font-size: 36px
      color: #FF8A00
      margin: 0
      line-height: 1
    div
      color:#2D2A40
  .row
    margin-left: -15px
    margin-right: -15px
    display: flex
    .col
      width: 50%
      padding-left: 15px
      padding-right: 15px
</style>
