<template>
<div>
  <wt-header>
      <a slot="wt-icon" href="/?logo=1" class="wt-table-cell" aria-label="Working Holiday Home Page">
        <div class="wt-icon-wrap">
          <i class="fas fa-camera-retro" style="color: red"></i>
        </div>
      </a>
      <wt-search-bar slot="wt-search"></wt-search-bar>
      <wt-nav slot="wt-navlinks"></wt-nav>
  </wt-header>

  <main id="app" class="main-wrap">
    <div>
      <div class="main-content">
        <div>
          <div>fixed Button</div>
          <div id="section-wrap">
            <div id="section-cate">
              <div>
                <div class="section-block">
                  <div class="section-title-block">
                    <div class="wt-vertical-center">
                      <div class="wt-mb">
                        <h3 class="section-title">推薦的熱門換宿</h3>
                      </div>
                    </div>
                  </div>
                  <span style="font-size: 0px;"></span>
                  <div class="section-item">
                    <wt-card 
                      v-for="(host, index) in caseList"
                      :key="index"
                      :hostUrl="host.hostUrl"
                      :hostName="host.hostName"
                      :hostLocation="host.hostLocation"
                      :imgUrl="host.imgUrl"/>
                  </div>
                  <div class="section-more">
                    <button type="button" class="section-button" aria-busy="false">
                      <span class="section-text">顯示全部 (超過2000個) </span>
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div>can't get what reason</div>
        </div>

      </div>
    </div>
  </main> 
</div>

</template>

<script>
import wtHeader from '@/components/wt-Header.vue'
import wtSearchBar from '@/components/wt-SearchBar.vue'
import wtCard from '@/components/wt-Card.vue'
import wtNav from '@/components/wt-Nav.vue'

export default {
  data() {
    return {
      caseList: [
        {
          hostUrl: 'www.google.com',
          imgUrl: 'https://img.freepik.com/free-photo/blue-mountains-famous-tourism-scenery-lijiang_1417-1143.jpg?size=338&ext=jpg',
          hostName: '旅居',
          hostLocation: '台北'
        },
        {
          hostUrl: 'www.google.com',
          imgUrl: 'https://images.pexels.com/photos/490411/pexels-photo-490411.jpeg?auto=compress&cs=tinysrgb&h=350',
          hostName: '旅人',
          hostLocation: '屏東'
        },
        {
          hostUrl: 'www.google.com',
          imgUrl: 'https://images.pexels.com/photos/490411/pexels-photo-490411.jpeg?auto=compress&cs=tinysrgb&h=350',
          hostName: '旅人',
          hostLocation: '屏東'
        },
        {
          hostUrl: 'www.google.com',
          imgUrl: 'https://images.pexels.com/photos/490411/pexels-photo-490411.jpeg?auto=compress&cs=tinysrgb&h=350',
          hostName: '旅人',
          hostLocation: '屏東'
        },
        {
          hostUrl: 'www.google.com',
          imgUrl: 'https://images.pexels.com/photos/490411/pexels-photo-490411.jpeg?auto=compress&cs=tinysrgb&h=350',
          hostName: '旅人',
          hostLocation: '屏東'
        }
      ]
    }
  },
  components: {
    wtCard,
    wtHeader,
    wtSearchBar,
    wtNav
  }
}
</script>

<style scoped>

</style>
