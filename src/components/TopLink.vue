<template>
  <div class="top-link no-print">
    <!-- <a class="theme-link" href="javascript:void(0);"></a> -->
    <a class="github-button" :href="userInfo.sourceurl" title="查看源码" target="_blank">
      <img src="../assets/images/star.svg" alt="Github"><span>Star</span>
    </a>
  </div> 
</template>

<script>
  export default {
    name: 'TopLink',
    props: {
      userInfo: {
        type: Object,
        default: {}
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import '../styles/variable.scss';
  
  .top-link {
    position: fixed;
    top:20px;
    right:20px;
    z-index: 5;
    img{
      width: 14px;
      vertical-align: middle;
      margin-right:5px;
    }
    a{
      float: left;
      margin-left: 20px;
    }
    .github-button{
      font-size: 14px;
      border: 1px solid #d5d5d5;
      border-radius: 3px;
      padding: 3px 9px;
      color: #333;
      line-height: 14px;
      text-shadow: 0 1px 0 rgba(255,255,255,.9);
      background-color: #eee;
      background-image: linear-gradient(to bottom,#fcfcfc,#eee);
      -ms-filter: "progid:DXImageTransform.Microsoft.gradient(startColorstr='#fcfcfc', endColorstr='#eeeeee')";
      display: block;
      text-decoration: none;
      &:hover{
        background-color: #ddd;
        background-image: linear-gradient(to bottom,#eee,#ddd);
        border-color: #ccc;
        -ms-filter: "progid:DXImageTransform.Microsoft.gradient(startColorstr='#eeeeee', endColorstr='#dddddd')";
      }
      span{
        vertical-align: middle;
      }
    }
    .theme-link{
      width: 24px;
      height: 24px;
      background: $text-gray;
      border-radius: 3px;
    }
  }
</style>

