<template>
  <div>
    <div class="title">周末去哪玩</div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img class="item-img" :src="item.imgUrl"/>
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
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
        title: '千岛湖',
        desc: '千年迷魂镇，据传是三国孙权的故里'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
        title: '千岛湖',
        desc: '千年迷魂镇，据传是三国孙权的故里'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
        title: '千岛湖',
        desc: '千年迷魂镇，据传是三国孙权的故里'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
        title: '千岛湖',
        desc: '千年迷魂镇，据传是三国孙权的故里'
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
        background:#eee
        text-indent:.2rem
    .item-img-wrapper
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom: 37.09%
        background:red
        .item-img
            width:100%
    .item-info
        padding: .1rem
        .item-title
            line-height:.54rem
            font-size: .32rem
            ellipsis()
        .item-desc
            line-height: .4rem
            color:#ccc
            ellipsis()
</style>
