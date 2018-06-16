<template>
  <div :class="['section-header-block', { 'wt-fixed': isFixed}]">
    <header role="banner" class="wt-relative">
      <div :class="['section-header-wrap', { 'wt-fixed': isFixed, 'header-transparent': isTransparent }]">
        <div class="wt-table">
          <div class="wt-vertical-nowidth">
            <slot name="wt-icon"></slot> 
          </div>
          <div class="wt-vertical">
            <div class="header-search-wrap">
              <div class="searchbar-wrap">
                <slot name="wt-search"></slot>
              </div>
            </div>           
          </div>

          <div class="wt-vertical-nowidth">
            <slot name="wt-navlinks"></slot> 
          </div>
        </div>
      </div>
    </header>
  </div>
</template>

<script>

export default {
	props: {
    isTransparent: {
      type: Boolean,
      default: false
    },
    isFixed: {
      type: Boolean,
      default: false
    } 
  }
}	
</script>

<style lang="less" scoped>

.section-header-block {
  height: 64px !important;
  z-index: 10 !important;
}

.section-header-wrap {
  background-color: rgb(255, 255, 255) !important;
  box-shadow: none !important;
  width: 100% !important;
  border-bottom: 1px solid rgb(228, 228, 228) !important;
}

.header-search-wrap {
  display: block !important;
  position: absolute !important;
  left: 90px !important;
  top: 10px !important;
  right: 12px !important;
  z-index: 100 !important;
}

.header-transparent {
  background-color: transparent !important;
}

.searchbar-wrap {

  &:before, &:after {
    content: "" !important;
    display: table !important;
  }

  &:after {
    clear: both !important;
  }
}

@media (min-width: 744px) {
 .section-header-block {
    height: 81px !important;
  } 

  .header-search-wrap {
    top: 16px !important;
    width: 460px !important;
  }

}

@media (min-width: 1128px) {
  .header-search-wrap {
    left: 80px !important; 
  }
}

</style>