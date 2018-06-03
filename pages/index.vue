<template>
  <section class="container">
    <div class="host-list row">
      <wt-Card 
        class="col-md-4"
        v-for="(host, index) in caseList"
        :key="index"
        :hostUrl="host.hostUrl"
        :hostName="host.hostName"
        :hostLocation="host.hostLocation"
        :imgUrl="host.imgUrl"/>    
    </div>
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
    wtCard
  }
}
</script>

<style scoped>

.host-list {
  display: flex;
  align-items: center;
  justify-content: center;
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
