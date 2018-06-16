<template>
  <li class="wt-table-cell">
    <div class="wt-relative">
      <a href="#" class="navbar-style" aria-busy="false">
        <div class="navbar-border" 
          @click="showListBox">
          <div class="navbar-content">
            <span>{{ navContent }}</span>
            <svg v-if="hasNotice" class="navbar-notice" focusable="false">
              <circle cx="3" cy="3" r="3"></circle>
            </svg>
          </div>
        </div>
      </a>
      <!-- 依照render function邏輯設定prop 有dropdown 才Gen此區塊 -->
      <wt-nav-list-box v-if="isShowListBox" :list-box-item="listBoxItem"></wt-nav-list-box>
    </div>
  </li>
</template>
<script>
  import wtNavListBox from '@/components/wt-NavListBox.vue'
  export default {
    props: {
      navContent: {
        type: String,
        required: true,
        default: 'Home'
      },
      hasNotice: {
        type: Boolean,
        default: false
      },
      hasListBox: {
        type: Boolean,
        default: false
      },
      listBoxItem: {
        type: Array,
        required: this.hasListbox
      }
    },
    data() {
      return {
        setShowListBox: false,
      }
    },
    computed: {
      isShowListBox() {
        return this._uid == this.setShowListBox.uid && this.setShowListBox && this.hasListBox
      }
    },
    methods: {
      showListBox(show) {
        this.setShowListBox.uid = this._uid
        this.setShowListBox = !this.setShowListBox
      }
    },
    components: {
      wtNavListBox
    }
  }
</script>
<style lang="less" scoped>
  @media (min-width: 744px) {
    .navbar-style {
      height: 80px !important;
      line-height: 80px !important;
    }
  }

  .navbar-style {
      -webkit-appearance: none !important;
      color: inherit !important;
      display: inline-block !important;
      height: 64px !important;
      line-height: 64px !important;
      position: relative !important;
      white-space: nowrap !important;
      background: transparent !important;
      border-width: initial !important;
      border-style: none !important;
      border-color: initial !important;
      border-image: initial !important;
      text-decoration: none !important;
      margin: 0px !important;
      padding: 0px 8px !important;
  }

  .navbar-border {
    height: 100% !important;
    vertical-align: middle !important;
    box-sizing: border-box !important;
    border-bottom: 2px solid transparent !important;

    &:hover {
      border-bottom: 2px solid rgb(118, 118, 118) !important;
    }
  }

  .navbar-content {
    display: inline-block !important;
    vertical-align: middle !important;
    line-height: 1 !important;
    padding: 8px !important;
    border-bottom: 2px solid transparent !important;
  }

  .navbar-notice {
      fill: rgb(0, 132, 137) !important;
      height: 6px !important;
      opacity: 0 !important;
      position: absolute !important;
      top: 50% !important;
      transform: translate3d(4px, -8px, 0px) !important;
      -webkit-transform-origin-x: 7px !important;
      -webkit-transform-origin-y: -5px !important;
      width: 6px !important;
  }
</style>