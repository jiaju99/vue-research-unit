<template>
  <div :style="cssText">
    <a :href="link" target="_blank" class="unit-banner">
      <img :src="src" alt="">
    </a>
  </div>
</template>
<script type="text/ecmascript-6">
  export default {
    label: 'Banner图',
    props: {
      className: {
        type: String,
        default: ''
      },
      cssText: {
        type: String,
        default: function (index) {
          return 'z-index:' + (index === undefined ? 0 : index) + ';width:100%;'
        }
      },
      src: {
        type: String,
        default: 'static/assets/img/1.png'
      },
      link: {
        type: String,
        default: '#'
      }
    }
  }
</script>
<style>
  .unit-banner{
    display: block;
    overflow: hidden;
  }
  .unit-banner img{
    width: 100%;
    height: auto;
  }
</style>
