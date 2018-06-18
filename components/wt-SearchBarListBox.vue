<template>
<ul class="searchbar-listbox-wrap" role="listbox" style="width: 100%; left: 0px; top: 49px;">
  <li class="wt-list-display-none">
  <ul class="listbox-block" v-if="listItem.length">
    <li v-for="(item, index) in listItem" 
      :key="index"
      aria-selected="true" 
      :class="['item-block', {'item-block-focus': index == selectedFocus}]" 
      @click.prevent="sendQuery(item)"
      role="option" 
      tabindex="-1">
      <div class="item-content">
        <div class="item-content-icon-wrap">
          <div class="item-content-icon-block">
            <i class="fas fa-map-marker-alt" style="color: red"></i>
          </div>
        </div>
        <div class="wt-vertical-center">
          <div>
            <div class="item-content-text">{{ item }}</div>
          </div>
        </div>
      </div>
    </li>
  </ul>
  </li>
</ul>
</template>
<script>
  
  export default {
    props: {
      listItem: {
        type: Array,
        default: () => { return [] }
      },
      selectedInput: {
        type: String,
        default: ''
      },
      selectedFocus: {
        type: Number,
        default: 0
      }
    },
    methods: {
      sendQuery(result) {
        /* 注意空白編碼問題 待問Eddie*/ 
        let url = `http://localhost:3000/?query=${ result }`
        console.log(url)
      }
    }
}
</script>
<style lang="less" scoped>
.searchbar-listbox-wrap {
  background-color: rgb(255, 255, 255) !important;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 2px 4px !important;
  padding-top: 16px !important;
  padding-left: 12px !important;
  padding-right: 12px !important;
  padding-bottom: 0px !important;
  position: absolute !important;
  margin-top: 0px !important;
  border-color: rgb(219, 219, 219) !important;
  border-radius: 0px 0px 4px 4px !important;
  border-style: solid !important;
  border-width: 0px 1px 1px !important;
  overflow: hidden !important;
}

.listbox-block {
  margin-bottom: 24px !important;
  padding: 0px !important;
}

.item-block-focus {
  cursor: pointer !important;
  list-style-type: none !important;
  display: table !important;
  width: 100% !important;
  background-color: rgb(204, 238, 235) !important;
  padding: 12px !important;
  border-color: rgb(204, 238, 235) !important;
}

.item-block {
  cursor: pointer !important;
  list-style-type: none !important;
  display: table !important;
  width: 100% !important;
  padding: 8px 12px !important;

  &:hover {
    background-color: rgb(204, 238, 235) !important;
    border-color: rgb(204, 238, 210) !important;    
  }
}

.item-content {
  margin-left: 0px;
}

.item-content-icon-wrap {
  color: rgb(118, 118, 118) !important;
  display: table-cell !important;
  padding-right: 12px !important;
  vertical-align: middle !important;

  .item-content-icon-block {
    font-weight: 600 !important;
    word-wrap: break-word !important;
    font-size: 16px !important;
    line-height: 22px !important;
    letter-spacing: normal !important;
    font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, "Helvetica Neue", sans-serif !important;
    color: rgb(72, 72, 72) !important;
    margin: 0px !important;
  }
}

.item-content-text {
  font-weight: 600 !important;
  word-wrap: break-word !important;
  font-size: 14px !important;
  line-height: 18px !important;
  letter-spacing: normal !important;
  font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, "Helvetica Neue", sans-serif !important;
  color: rgb(72, 72, 72) !important;
  margin: 0px !important;
}

@media (min-width: 744px) {
  .searchbar-listbox-wrap {
    padding: 32px 32px 8px !important;
  }
}

</style>