<template>
  <div class="box-wrap experience">
    <section class="section">
      <div class="container">
        <div class="section-bg section-header-bg"></div>
        <div class="section-bg section-content-bg"></div>
        <header class="header">
          <div class="content-box">
            <h2 class="title">工作经验&nbsp;/&nbsp;
              <small><i>Experience</i></small>
            </h2>
            <div class="description">不同时期简短的从业经历介绍</div>
          </div>
        </header>
        <div class="section-content">
          <div class="explist">
            <div class="item" v-for="e in userInfo.experience">
              <div class="row">
                <div class="col-md-5">
                  <div class="time">{{e.time}}</div>
                  <div class="title">{{e.title}}</div>
                  <div class="description">{{e.intro}}</div>
                </div>
                <div class="col-md-7" v-html="e.description"></div>
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
    name: 'Experience',
    props: {
      userInfo: {
        type: Object,
        default: null
      }
    }
  }
</script>

<style lang="scss" scoped>
  .explist {
    margin-left: 2px;
    margin-top: 1rem;
    padding-left: 24px;
    border-left: 2px solid #404242;
    .item{
      position: relative;
      line-height: 2rem;
      margin-top: -15px;
      margin-bottom: 3rem;
      &:before{
        content: '';
        position: absolute;
        top: 6px;
        left: -30px;
        background: #e0a80d;
        border-radius: 5px;
        width: 10px;
        height: 10px;
        box-shadow: 0 0 0 6px #404242;
      }
      ul {
        padding-left: 15px;
        margin-top: 0;
      }
      .time {
        font-size: 0.8rem;
        color: #757575;
        line-height: 1.6rem;
      }
      .description {
        color: #757575;        
      }
    }
  }
</style>

