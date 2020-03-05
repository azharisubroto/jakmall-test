<template>
  <div class="cart">
    <div class="cart-inner">
      <h4>Summary</h4>

      <!-- TOTAL PURCHASED ITEMS -->
      <div class="purchased">
        {{items_total}} items purchased
      </div>

      <!-- DELIVER ESTIMATION -->
      <template>
        <div class="divider"></div>
        <div class="weight-bold">Delivery estimation</div>
        <div class="detail_val text-green weight-bold">today by GO-SEND</div>
      </template>

      <!-- PAYMENT METHOD -->
      <template>
        <div class="divider"></div>
        <div class="weight-bold">Payment method</div>
        <div class="detail_val text-green weight-bold">Bank Transfer</div>
      </template>

      <!-- COST DETAILS -->
      <div class="cost-details">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Amet possimus commodi placeat harum consequatur officiis tempore veniam neque sapiente, ullam minus reprehenderit, illum totam omnis, facilis vitae fugiat doloremque voluptatem?
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Chart',
  data () {
    return {
      items_total: 13
    }
  }
}
</script>
<style lang="stylus" scoped>
  .detail_val
    font-size: 16px
    margin-top: 5px
    line-height: 1
  .cost-details
    margin-top: 90px
</style>
