<template>
<div>
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
                      :hostId="host.id"
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

import wtCard from '@/components/wt-Card.vue'


export default {
  components: {
    wtCard,
  },
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        // resolve後的data會被nuxt自動merge到data裡面，此應為放入API request
        resolve({
          caseList: [
            {
              id: 1,
              imgUrl: 'https://img.freepik.com/free-photo/blue-mountains-famous-tourism-scenery-lijiang_1417-1143.jpg?size=338&ext=jpg',
              hostName: '旅居',
              hostLocation: '台北'
            },
            {
              id: 2,
              imgUrl: 'https://images.pexels.com/photos/490411/pexels-photo-490411.jpeg?auto=compress&cs=tinysrgb&h=350',
              hostName: '旅人',
              hostLocation: '台中'
            },
            {
              id: 3,
              imgUrl: 'https://images.pexels.com/photos/490411/pexels-photo-490411.jpeg?auto=compress&cs=tinysrgb&h=350',
              hostName: '旅人',
              hostLocation: '高雄'
            },
            {
              id: 4,
              imgUrl: 'https://images.pexels.com/photos/490411/pexels-photo-490411.jpeg?auto=compress&cs=tinysrgb&h=350',
              hostName: '旅人',
              hostLocation: '屏東'
            },
            {
              id: 5,
              imgUrl: 'https://images.pexels.com/photos/490411/pexels-photo-490411.jpeg?auto=compress&cs=tinysrgb&h=350',
              hostName: '旅人',
              hostLocation: '蘭嶼'
            }
          ]          
        }, 15000)
      })
    })
  }
}
</script>

<style scoped>

</style>
