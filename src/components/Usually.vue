<template>
  <div class="box-wrap usually">
    <section class="section">
      <div class="container">
        <div class="section-bg section-header-bg"></div>
        <div class="section-bg section-content-bg"></div>
        <header class="header">
          <div class="content-box">
            <h2 class="title">常逛&nbsp;/&nbsp;
              <small><i>Usually</i></small>
            </h2>
            <div class="description">经常逛的论坛或技术相关网站</div>
          </div>
        </header>
        <div class="section-content">
          <div class="row usually wow fadeIn" data-wow-delay="0.25s">
            <div class="col-lg-4 col-md-6" v-for="u in userInfo.usually">
              <a v-if="u.link" :href="u.link" target="_blank" class="item" :title="u.link">
              <i class="fa fa-github"></i>
              <h3 class="text-light">{{u.name}}</h3>
              <p>{{u.description}}</p>
            </a>
              <div v-if="!u.link" class="item" :title="u.link">
                <i class="fa fa-github"></i>
                <h3 class="text-light">{{u.name}}</h3>
                <p>{{u.description}}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
  export default {
    name: 'Usually',
    props: {
      userInfo: {
        type: Object,
        default: null
      }
    }
  }
</script>

<style lang="scss" scoped>
  .item {
    margin-right: 3rem;
    margin-bottom: 1rem;
    line-height: 2rem;
    display: inline-block;
    h3 {
      margin-top: 0.5rem;
      margin-bottom: 0.8rem;
      line-height: 1rem;
    }
  }
</style>

