<template>
  <section class="container">
    <wt-Card 
      v-for="(host, index) in caseList"
      :key="index"
      :hostUrl="host.hostUrl"
      :hostName="host.hostName"
      :hostLocation="host.hostLocation"
      :imgUrl="host.imgUrl"/>
  </section>
</template>

<script>
import wtCard from '@/components/wt-Card.vue'

export default {
  data() {
    return {
      caseList: [
        {
          hostUrl: 'www.google.com',
          imgUrl: 'https://images.pexels.com/photos/490411/pexels-photo-490411.jpeg?auto=compress&cs=tinysrgb&h=350',
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
    wtCard
  }
}
</script>

<style scoped>
.container {
  min-height: 100vh;
  max-width: 900px;
  min-width: 250vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
