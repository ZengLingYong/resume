<template>
  <div class="loading" v-show="loading">
    <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      width="24px" height="30px" viewBox="0 0 24 30" style="enable-background:new 0 0 50 50" xml:space="preserve">
      <rect x="0" y="8.02667" width="4" height="14.9467" fill="#e0a80d">
        <animate attributeName="height" attributeType="XML" values="5;21;5" begin="0s" dur="0.6s" repeatCount="indefinite"></animate>
        <animate attributeName="y" attributeType="XML" values="13; 5; 13" begin="0s" dur="0.6s" repeatCount="indefinite"></animate>
      </rect>
      <rect x="10" y="5.97333" width="4" height="19.0533" fill="#e0a80d">
        <animate attributeName="height" attributeType="XML" values="5;21;5" begin="0.15s" dur="0.6s" repeatCount="indefinite"></animate>
        <animate attributeName="y" attributeType="XML" values="13; 5; 13" begin="0.15s" dur="0.6s" repeatCount="indefinite"></animate>
      </rect>
      <rect x="20" y="9.97333" width="4" height="11.0533" fill="#e0a80d">
        <animate attributeName="height" attributeType="XML" values="5;21;5" begin="0.3s" dur="0.6s" repeatCount="indefinite"></animate>
        <animate attributeName="y" attributeType="XML" values="13; 5; 13" begin="0.3s" dur="0.6s" repeatCount="indefinite"></animate>
      </rect>
    </svg>
  </div>
</template>

<script>
  export default {
    name: 'Loading',
    props: {
      loading: {
        type: Boolean,
        default: true
      }
    }
  }
</script>

<style lang="scss">
  .loading {
    position: fixed;
    top: 45%;
    left: 50%;
  }
</style>
