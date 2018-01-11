<<template>
  <div id="app">
    <Loading :loading="loading"></Loading>
    <TopLink v-if="userInfo" :userInfo="userInfo"></TopLink>
    <Information v-if="userInfo" :userInfo="userInfo"></Information>
    <Intro v-if="userInfo" :userInfo="userInfo"></Intro>
    <Experience v-if="userInfo" :userInfo="userInfo"></Experience>
    <Skills v-if="userInfo" :userInfo="userInfo"></Skills>
    <ProjectExp v-if="userInfo" :userInfo="userInfo"></ProjectExp>
    <Usually v-if="userInfo" :userInfo="userInfo"></Usually>
    <Contact v-if="userInfo" :userInfo="userInfo"></Contact>
  </div>
</template>


<script>
import Loading from './components/Loading'
import TopLink from './components/TopLink'
import Information from './components/Information'
import Intro from './components/Intro'
import Experience from './components/Experience'
import Skills from './components/Skills'
import ProjectExp from './components/ProjectExp'
import Usually from './components/Usually'
import Contact from './components/Contact'
import WOW from 'wowjs'

export default {
  data () {
    return {
      loading: true,
      userInfo: null,
      msg: 'Welcome to Your Vue.js App'
    }
  },
  created () {
    this.getData()
  },
  methods: {
    getData () {
      this.$http.get('/static/data.json').then(response => {
        const resp = response.data
        this.userInfo = resp
        this.$nextTick(() => {
          new WOW.WOW({
            live: false
          }).init()
        })
      }).catch(err => {
        console.log(err)
      })
    }
  },
  components: {
    Loading,
    TopLink,
    Information,
    Intro,
    Experience,
    Skills,
    ProjectExp,
    Usually,
    Contact
  }
}
</script>

<style lang="scss">
  @import './styles/index.scss'; // 全局自定义的css样式
</style>
