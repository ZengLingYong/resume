<template>
  <div class="box-wrap information" id="information">
    <section class="section section-header">
      <div class="section-bg section-header-bg"></div>
      <div class="section-bg section-content-bg"></div>
      <div class="container">
        <header class="header">
          <div class="header-box">
            <div class="avatar wow inShow no-print">
              <img :src="avatar" alt="avatar" class="img-responsive">
            </div>
            <h1 class="name text-center wow inShow no-print">{{userInfo.nickname}}</h1>
            <h1 class="name text-center hide show-print">{{userInfo.name}}</h1>
          </div>
        </header>
        <div class="section-content">
          <div class="content-box">
            <div class="name-slogan">
              <h2 class="name-in wow inShow no-print" data-wow-delay="0.1s">
                <span class="text-light">{{userInfo.lastName}}</span>&nbsp;{{userInfo.firstName}}
              </h2> 
              <div class="description wow inShow" data-wow-delay="0.15s">{{userInfo.slogan}}</div>
            </div>
            <div class="contact-info">
              <div class="row">
                <div class="col-md-6 col-lg-3">
                  <div class="item wow inShow" data-wow-delay="0.3s">
                    <h4>性别</h4>
                    <div class="info">{{userInfo.sex}}</div>
                  </div>
                </div>
                <div class="col-md-6 col-lg-3">
                  <div class="item wow inShow" data-wow-delay="0.45s">
                    <h4>年龄</h4>
                    <div class="info">{{userInfo.age}}</div>
                  </div>
                </div>
                <div class="col-md-6 col-lg-3">
                  <a class="item wow inShow" data-wow-delay="0.5s" :href="userInfo.website" target="_blank">
                    <h4>经验</h4>
                    <div class="info">{{userInfo.exp}}</div>
                  </a>
                </div>
                <div class="col-md-6 col-lg-3">
                  <a class="item wow inShow" data-wow-delay="0.55s" :href="'mailto:' + userInfo.email" target="_blank">
                    <h4>Email</h4>
                    <div class="info">{{userInfo.email}}</div>
                  </a>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6 col-lg-3">
                  <div class="item wow inShow" data-wow-delay="0.6s">
                    <h4>Location</h4>
                    <div class="info">{{userInfo.location}}</div>
                  </div>
                </div>
                <div class="col-md-6 col-lg-3">
                  <div class="item wow inShow" data-wow-delay="0.65s">
                    <h4>QQ</h4>
                    <div class="info">{{userInfo.qq.number}}</div>
                  </div>
                </div>
                <div class="col-md-6 col-lg-3">
                  <a class="item wow inShow" data-wow-delay="0.7s" :href="userInfo.website" target="_blank">
                    <h4>Website</h4>
                    <div class="info">{{userInfo.website}}</div>
                  </a>
                </div>
                <div class="col-md-6 col-lg-3">
                  <a class="item wow inShow" data-wow-delay="0.75s" :href="'mailto:' + userInfo.github" target="_blank">
                    <h4>Github</h4>
                    <div class="info">{{userInfo.github}}</div>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
  import avatar from '@/assets/images/avatar.png'

  export default {
    name: 'Information',
    props: {
      userInfo: {
        type: Object,
        default: null
      }
    },
    data () {
      return {
        avatar
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import '../styles/variable.scss';

  .avatar {
    border-radius: 20rem;
    max-width: 200px;
    margin: 0 auto;
    overflow: hidden;
  }
  .name {
    height: 40px;
    line-height: 40px;
    font-size: 2rem;
    font-weight: 200;
    margin-top: 1rem;
    margin-bottom: 4rem;
  }
  .name-slogan {
    position: relative;
    top: -2rem;
    .name-in {
      height: 68px;
      line-height: 68px;
    }
  }
  .description {
    font-size: 1.2rem;
    margin-bottom: 2rem;
  }
  .text-light {
    color: $light;
  }
  .header-box {
    position: relative;
    height: 100%;
    display: flex;
    justify-content: center;
    flex-direction: column;
  }
  .content-box {
    position: relative;
    height: 100%;
    display: flex;
    justify-content: center;
    flex-direction: column;
  }
  .contact-info {
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    h4 {
      font-size: 1rem;
      margin: 1.5rem 0;
    }
    .info {
      line-height: 1rem;
    }
    & > div:first-child {
      border-bottom: 2px dashed #404242;
      padding-bottom: 1rem;
    }
  }

  @media (max-width: 1120px) {
    .contact-info{
      position: relative;
    }
  }
</style>
