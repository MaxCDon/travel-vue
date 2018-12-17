<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom"
          v-for="item of recommendList"
          :key="item.id">
        <div class="item-img-wrapper">
          <img
            :src="item.imgUrl"
            class="item-img">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1509/fb/c45a951a9b4305.jpg_r_640x214_26fcfd26.jpg',
        title: '临安湍口众安氡温泉',
        desc: '冬日网红温泉，你值得拥有'

      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1509/fb/c45a951a9b4305.jpg_r_640x214_26fcfd26.jpg',
        title: '临安湍口众安氡温泉',
        desc: '冬日网红温泉，你值得拥有'

      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1509/fb/c45a951a9b4305.jpg_r_640x214_26fcfd26.jpg',
        title: '临安湍口众安氡温泉',
        desc: '冬日网红温泉，你值得拥有'

      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    over-flow: hidden
    height: 0
    padding-bottom: 38%
    .item-img
      width: 100%
  .item-info
    flex: 1
    padding: .1rem
    min-width: 0
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
