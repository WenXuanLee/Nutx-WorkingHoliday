<template>
  <div>
    <wt-header>
        <nuxt-link to="/" slot="wt-icon" class="wt-table-cell" aria-label="Working Holiday Home Page">
          <div class="wt-icon-wrap">
            <i class="fas fa-camera-retro" style="color: red"></i>
          </div>
        </nuxt-link>
        <wt-search-bar slot="wt-search"></wt-search-bar>
        <wt-nav slot="wt-navlinks"></wt-nav>
    </wt-header>
    <nuxt/>
  </div>
</template>
<script>
  import wtHeader from '@/components/wt-Header.vue'
  import wtSearchBar from '@/components/wt-SearchBar.vue'
  import wtNav from '@/components/wt-Nav.vue'
  export default {
    components: {
      wtHeader,
      wtSearchBar,
      wtNav
    }   
  }
</script>
<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}
header {
  font-weight: 600;
}

div {
  display: block;
}

.main-wrap {
  position: relative !important;
  padding-top: 64px !important;
}
.main-content {
  padding-left: 24px !important;
  padding-right: 24px !important;
  max-width: none !important;
  background-color: transparent;
  min-height: 400px; /* loading時起碼有上方height*/
}

.section-block {
  margin-top: 32px !important;
  margin-bottom: 32px !important;
}

.section-title-block {
  display: table !important;
  table-layout: fixed !important;
  width: 100% !important;
}

.section-item {
  margin-left: -24px !important;
  margin-right: -24px !important;
  padding: 0px 18px !important;
}

.section-more {
  display: inline-block !important;
  text-align: left !important;
  width: 100% !important;
  margin-top: 8px !important;
}

.section-button {
  cursor: pointer !important;
  display: inline-block !important;
  text-align: center !important;
  white-space: nowrap !important;
  width: 100% !important;
  background: transparent !important;
  border-width: 1px !important;
  border-style: solid !important;
  border-color: rgb(0, 132, 137) !important;
  border-image: initial !important;
  border-radius: 4px !important;
  padding: 14px !important;
  text-decoration: none !important;
}
.section-text {
  font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, "Helvetica Neue", sans-serif !important;
  font-size: 14px !important;
  line-height: 18px !important;
  letter-spacing: normal !important;
  padding-top: 0px !important;
  padding-bottom: 0px !important;
  color: rgb(0, 132, 137) !important;
  font-weight: 800 !important;
  display: block !important;
  margin-right: 0px !important;
  text-overflow: ellipsis !important;
  white-space: nowrap !important;
  overflow: hidden !important;
}

.wt-icon-wrap {
  display: table-cell !important;
  height: 64px !important;
  position: relative !important;
  text-align: center !important;
  text-decoration: none !important;
  -webkit-transition: 0.25s color !important;
  -moz-transition: 0.25s color !important;
  transition: 0.25s color !important;
  padding-left: 24px !important;
  padding-right: 24px !important;
  vertical-align: middle !important;
  white-space: nowrap !important;
}
.wt-vertical-nowidth {
  display: table-cell !important;
  vertical-align: middle !important;
}

.wt-vertical {
  display: table-cell !important;
  width: 100%;
  vertical-align: middle !important;
}

.wt-table-cell {
  display: table-cell !important;
}

.wt-table {
  display: table !important;
  width: 100% !important;
}
.wt-table-nowidth {
  display: table !important;
}

.wt-no-break-line {
  white-space: nowrap !important;
  line-height: 0 !important;    
}
.wt-block {
  display: block !important;
  width: 100% !important;
}

.wt-vertical-center {
  display: table-cell !important;
  width: 100% !important;
  vertical-align: baseline !important;
}
.wt-mb {
  margin-bottom: 8px !important;
}
.wt-relative {
  position: relative !important
}
.wt-inline-block {
  display: inline-block !important;
}

.wt-fixed {
  position: fixed;
}

.wt-list-display-none {
  list-style-type: none !important;
}

.wt-text-subtitle {
  word-wrap: break-word !important;
  font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, "Helvetica Neue", sans-serif !important;
  font-size: 12px !important;
  line-height: 16px !important;
  letter-spacing: normal !important;
  padding-top: 0px !important;
  padding-bottom: 0px !important;
  color: rgb(72, 72, 72) !important;
  font-weight: 800 !important;
  margin: 0px !important;
}
.wt-text-title {
  word-wrap: break-word !important;
  font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, "Helvetica Neue", sans-serif !important;
  font-size: 16px !important;
  line-height: 22px !important;
  padding-top: 0px !important;
  padding-bottom: 0px !important;
  color: rgb(72, 72, 72) !important;
  font-weight: 800 !important;
  margin: 0px !important;
}

.wt-float-left {
  float: left !important;
}

.wt-normal-line-height {
  line-height: normal !important;
}

.wt-overflow-hidden {
  overflow: hidden !important;
}
.section-title {
  font-weight: 800 !important;
  margin-bottom: 0px !important;
  font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, "Helvetica Neue", sans-serif !important;
  font-size: 25px !important;
  line-height: 30px !important;
  letter-spacing: normal !important;
  padding-top: 2px !important;
  padding-bottom: 2px !important;
  color: rgb(72, 72, 72) !important;
}

@media (min-width: 744px) {
  .main-wrap {
    padding-top: 80px !important;
  }
  .section-block {
    margin-top: 40px !important;
    margin-bottom: 40px !important;
  }
  .section-item {
    padding: 0px 16px !important;
  }
  .section-button {
    box-shadow: none !important;
    text-align: left !important;
    width: auto !important;
    border-width: initial !important;
    border-style: none !important;
    border-color: initial !important;
    border-image: initial !important;
    padding: 4px 0px !important;
  }
  .section-text {
    font-weight: 600 !important;
    font-size: 17px !important;
    line-height: 22px !important;
    color: rgb(0, 132, 137) !important;
    display: inline !important;
    margin-right: 6px !important;
  }
  .wt-mb {
    margin-bottom: 8px !important;
  }

}

@media (min-width: 1128px) {
  .main-content {
    margin: 0 auto !important;
    position: relative !important;
    padding-left: 80px !important;
    padding-right: 81px !important;
  }
  .section-title-block {
    width: 50% !important;
  }
  .section-item {
    margin-left: -8px !important;
    margin-right: -8px !important;
    padding: 0px !important;
  }
}
</style>
