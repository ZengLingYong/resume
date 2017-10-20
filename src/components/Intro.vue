<template>
  <div class="box-wrap intro">
    <section class="section">
      <div class="container">
        <div class="section-bg section-header-bg"></div>
        <div class="section-bg section-content-bg"></div>
        <header class="header">
          <div class="content-box">
            <h2 class="title">介绍&nbsp;/&nbsp;
              <small><i>Intro</i></small>
            </h2>
            <div class="description">介绍一些个人基本情况</div>
          </div>
        </header>
        <div class="section-content">
          <div class="intro">
            <p v-for="intro in userInfo.intro">{{intro}}</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
  export default {
    name: 'Intro',
    props: {
      userInfo: {
        type: Object,
        default: null
      }
    }
  }
</script>

<style lang="scss">
  .intro p {
    margin-bottom: 1rem;
    line-height: 2rem;
  }
</style>
