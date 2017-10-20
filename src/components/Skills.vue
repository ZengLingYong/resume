<template>
  <div class="box-wrap skills">
    <section class="section">
      <div class="container">
        <div class="section-bg section-header-bg"></div>
        <div class="section-bg section-content-bg"></div>
        <header class="header">
          <div class="content-box">
            <h2 class="title">技能&nbsp;/&nbsp;
              <small><i>Skills</i></small>
            </h2>
            <div class="description">我所掌握的工具和技术栈</div>
          </div>
        </header>
        <div class="section-content">
          <div class="row skill">
            <div class="col-md-6" v-for="s in userInfo.skill">
              <div class="item">
                <div class="text-info">
                  <span class="num text-light">{{s.percent}}</span>{{s.name}}
                </div>
                <div class="progress">
                  <div class="progress-bar wow progressShow" :style="{width: s.percent}"></div>
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
  export default {
    name: 'Skills',
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
    margin-bottom: 2rem;
    padding-right: 2rem;
    .text-info {
      margin-bottom: 1rem;
      font-size: 1.2rem;
    }
    .num {
      display: inline-block;
      margin-right: 1rem;
    }
    .progress {
      position: relative;
      height: 5px;      
      background: #404242;
      .progress-bar {
        height: 100%;
        background: #e0a80d;
      }
    }
  }
</style>

