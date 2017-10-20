<template>
  <div class="box-wrap contact">
    <section class="section no-print">
      <div class="container">
        <div class="section-bg section-header-bg"></div>
        <div class="section-bg section-content-bg"></div>
        <header class="header">
          <div class="content-box">
            <h2 class="title">
              联系&nbsp;/&nbsp;
              <small><i>Contact</i></small>
            </h2>
            <div class="description">通过这些信息可以联系到我</div>
          </div>
        </header>
        <div class="section-content">
          <div class="contact-list">
            <div class="row">
              <div class="col-md-6 col-lg-3">
                <div class="item">
                  <h4>Location</h4>
                  <div class="info">{{userInfo.location}}</div>
                </div>
              </div>
              <div class="col-md-6 col-lg-3">
                <div class="item">
                  <h4>QQ</h4>
                  <div class="info">{{userInfo.qq.number}}</div>
                </div>
              </div>
              <div class="col-md-6 col-lg-3">
                <a class="item" :href="userInfo.website" target="_blank">
                  <h4>Website</h4>
                  <div class="info">{{userInfo.website}}</div>
                </a>
              </div>
              <div class="col-md-6 col-lg-3">
                <a class="item" :href="'mailto:' + userInfo.email" target="_blank">
                  <h4>Email</h4>
                  <div class="info">{{userInfo.email}}</div>
                </a>
              </div>
            </div>
          </div>
          <div class="name-slogan">
            <h2 class="wow inShow">
              <span class="text-light">{{userInfo.lastName}}</span>&nbsp;{{userInfo.firstName}}
            </h2>
            <div class="description wow inShow" data-wow-delay="0.05s">{{userInfo.slogan}}</div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
  export default {
    name: 'Contact',
    props: {
      userInfo: {
        type: Object,
        default: null
      }
    }
  }
</script>

<style lang="scss" scoped>
  .contact-list {
    margin-bottom: 2rem;    
    h4 {
      margin-top: 0.3rem;
      margin-bottom: 0.8rem;
    }
  }
</style>
