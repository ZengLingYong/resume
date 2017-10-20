<<template>
  <div id="app">
    <Loading :loading="loading"></Loading>
    <TopLink></TopLink>
    <Information :userInfo="userInfo"></Information>
    <Intro :userInfo="userInfo"></Intro>
    <Experience :userInfo="userInfo"></Experience>
    <Skills :userInfo="userInfo"></Skills>
    <ProjectExp :userInfo="userInfo"></ProjectExp>
    <Usually :userInfo="userInfo"></Usually>
    <Contact :userInfo="userInfo"></Contact>
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
