<template>
	<div class="item-wrap">
  	<div class="item-block">
    <div id="hostId" class="item-content">
      <div class="item-img-wrap">
        <div aria-hidden="true" class="wt-relative">
          <div class="item-img-round item-img-cover">
            <div class="item-img-display">
              <a href="#hostUrl" target="_self" aria-hidden="true" tabindex="-1">
                <div class="item-img-overflow">
                  <div class="item-img-nowrap">
                    <div class="item-img-center">
                      <figure class="wt-relative" style="width: 100%; height: 100%;">
                        <img class="item-img-show" alt="Leccio Apartment - Cimbolello" :src="imgUrl">
                      </figure>
                    </div>
                  </div>
                </div>
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class="item-intro">
        <div>
          <a :href="hostUrl" target="_self" rel="noopener" class="item-intro-block">
            <div>
              <div class="item-intro-spec" style="color: rgb(52, 30, 19);">
                <div class="item-intro-spec-overflow" style="color: rgb(52, 30, 19);">
                  <small class="wt-text-subtitle">
                    <span style="color: rgb(52, 30, 19);">
                      <span>
                        整套公寓
                        <span>
                          <span aria-hidden="true"> · </span>
                        </span>
                        {{ hostLocation }}
                      </span>
                    </span>
                  </small>
                </div>
              </div>
              <div></div>
            </div>
            <div style="margin-top: 4px;">
              <div class="item-intro-title-block">
                <div class="wt-text-title">{{ hostName }}</div>
              </div>
            </div>
            <div style="margin-top: 2px;">
              <div>
                <div class="wt-float-left">
                  <div class="wt-normal-line-height">
                    <span>
                      <span class="item-intro-supply">
                        <span>$2,519 TWD</span>
                      </span>
                      <span>
                        <span class="item-intro-supply">
                          <div class="wt-inline-block" style="margin-left: 6px;">
                            <span>一晚</span>
                          </div></span>
                        </span>
                      </span>
                    </div>
                  </div>
                  <div class="wt-overflow-hidden">
                    <div class="item-intro-title-basic">
                      <span>
                        <span aria-hidden="true">&nbsp;·&nbsp;</span>
                        <span class="item-intro-supply">
                          <span>免費取消</span>
                        </span>
                      </span>
                    </div>
                  </div>
                </div>
              </div>
              <div style="margin-top: 2px;">
                <div class="item-intro-notice-block">
                  <div class="wt-inline-block">
                    <span class="item-intro-notice-icon-wrap">
                      <span role="img" aria-label="評分是5（滿分為5）">
                        <span class="item-intro-notice-icon">
                          <svg viewBox="0 0 1000 1000" role="presentation" aria-hidden="true" focusable="false" style="height: 1em; width: 1em; display: block; fill: currentcolor;">
                            <path d="M971.5 379.5c9 28 2 50-20 67L725.4 618.6l87 280.1c11 39-18 75-54 75-12 0-23-4-33-12l-226.1-172-226.1 172.1c-25 17-59 12-78-12-12-16-15-33-8-51l86-278.1L46.1 446.5c-21-17-28-39-19-67 8-24 29-40 52-40h280.1l87-278.1c7-23 28-39 52-39 25 0 47 17 54 41l87 276.1h280.1c23.2 0 44.2 16 52.2 40z"></path>
                          </svg>
                        </span>
                        <span class="item-intro-notice-icon">
                          <svg viewBox="0 0 1000 1000" role="presentation" aria-hidden="true" focusable="false" style="height: 1em; width: 1em; display: block; fill: currentcolor;">
                            <path d="M971.5 379.5c9 28 2 50-20 67L725.4 618.6l87 280.1c11 39-18 75-54 75-12 0-23-4-33-12l-226.1-172-226.1 172.1c-25 17-59 12-78-12-12-16-15-33-8-51l86-278.1L46.1 446.5c-21-17-28-39-19-67 8-24 29-40 52-40h280.1l87-278.1c7-23 28-39 52-39 25 0 47 17 54 41l87 276.1h280.1c23.2 0 44.2 16 52.2 40z">
                            </path>
                          </svg>
                        </span>
                      </span>
                    </span>
                    <span class="item-intro-notice-wrap" aria-label="253則評價">
                      <span class="item-intro-notice">253</span>
                    </span>
                  </div>
                  <span class="item-intro-notice">
                    <span aria-hidden="true"> · </span>
                    <span>超讚房東</span>
                  </span>
                </div>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
	props: ['hostUrl', 'hostName', 'hostLocation', 'imgUrl', ]
}	
</script>

<style lang="less" scoped>

@white: #FFFFFF;
@black: #000000;
@dark_gray: lighten(@black, 20%);
@gray: lighten(@black, 40%);
@light_gray: lighten(@black, 60%);
@accent: #e74c3c;
@container_width: 800px;

.box-shadow( @h-shadow: 0px; @v-shadow: 1px; @blur: 2px; @spread: 0px; @color: fade(@black, 15%); ) {
  -webkit-box-shadow: @arguments;
  -moz-box-shadow: @arguments;
  box-shadow: @arguments;
}

.portfolio-link {
	display: block;
	position: relative;
	max-height: 400px;
	margin: 0 auto;

	&:hover {
		.box-shadow(@blur: 35px; @color: fade(@black, 30%););
	}
}
.item-wrap {
  display: inline-block !important;
  vertical-align: top !important;
  white-space: normal !important;

	&:hover {
		.box-shadow(@blur: 35px; @color: fade(@black, 30%););
	}
}

.item-block {
  width: 100% !important;
  height: 100% !important;
  padding-top: 8px !important;
  padding-bottom: 12px !important;
  padding-left: 6px !important;
  padding-right: 6px !important;
}

.item-content {
  position: relative !important;
  color: rgb(72, 72, 72) !important;
  height: 100% !important;
  background: rgb(255, 255, 255) !important;
}

.item-img-wrap {
  width: 100% !important;
  position: relative !important;
  z-index: 0 !important;
}

.item-img-cover {
  padding-top: 66.6667%;
  background: rgb(216, 216, 216);
}

.item-img-round {
  position: relative !important;
  width: 100% !important;
  z-index: 0 !important;
  border-bottom-left-radius: 3px !important;
  border-bottom-right-radius: 3px !important;
  border-top-left-radius: 3px !important;
  border-top-right-radius: 3px !important;
  overflow: hidden !important;
}

.item-img-display {
  position: absolute !important;
  top: 0px !important;
  bottom: 0px !important;
  left: 0px !important;
  right: 0px !important;
  height: 100% !important;
  width: 100% !important;
}

.item-img-overflow {
  height: 100% !important;
  width: 100% !important;
  overflow: hidden !important;
}

.item-img-nowrap {
  width: 100% !important;
  height: 100% !important;
  white-space: nowrap !important;
}
.item-img-center {
  display: inline-block !important;
  vertical-align: middle !important;
  height: 100% !important;
  width: 100% !important;
}

.item-img-show {
  max-width: 100%;
  max-height: 100%;
  width: 100%;
  height: 100%;
  position: absolute !important;
  // animation-name: keyframe_18jn58a !important;
  // animation-duration: 300ms !important;
  // animation-timing-function: ease-out !important;
  border-bottom-left-radius: 3px !important;
  border-bottom-right-radius: 3px !important;
  border-top-left-radius: 3px !important;
  border-top-right-radius: 3px !important;
}

.item-intro {
  padding-top: 8px !important;
}

.item-intro-block {
  display: block !important;
  color: rgb(72, 72, 72) !important;
}

.item-intro-spec {
  height: 16px !important;
  max-height: 16px !important;
  margin-bottom: 2px !important;
  text-transform: uppercase !important;
}
.item-intro-spec-overflow {
  text-overflow: ellipsis !important;
  white-space: nowrap !important;
  overflow: hidden !important;
}

.item-intro-title-block {
  line-height: 22px !important;
  max-height: 44px !important;
  text-overflow: ellipsis !important;
  display: -webkit-box !important;
  -webkit-line-clamp: 2 !important;
  -webkit-box-orient: vertical !important;
  font-size: 19px !important;
  overflow: hidden !important;
}

.item-intro-title-basic {
  line-height: normal !important;
  text-overflow: ellipsis !important;
  white-space: nowrap !important;
  overflow: hidden !important;
}

.item-intro-supply {
  word-wrap: break-word !important;
  font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, "Helvetica Neue", sans-serif !important;
  font-size: 14px !important;
  line-height: 18px !important;
  letter-spacing: normal !important;
  padding-top: 0px !important;
  padding-bottom: 0px !important;
  color: rgb(72, 72, 72) !important;
  font-weight: normal !important;
  display: inline !important;
  margin: 0px !important;
}
.item-intro-notice-wrap {
  vertical-align: middle !important;
  line-height: 21px !important;
  margin-right: 2px !important;
}

.item-intro-notice-block {
  line-height: normal !important;
  max-height: 24px !important;
  text-overflow: ellipsis !important;
  display: -webkit-box !important;
  -webkit-line-clamp: 1 !important;
  -webkit-box-orient: vertical !important;
  overflow: hidden !important;
}

.item-intro-notice {
  font-weight: 600 !important;
  word-wrap: break-word !important;
  font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, "Helvetica Neue", sans-serif !important;
  font-size: 12px !important;
  line-height: 16px !important;
  letter-spacing: normal !important;
  padding-top: 0px !important;
  padding-bottom: 0px !important;
  color: rgb(72, 72, 72) !important;
  display: inline !important;
  margin: 0px !important;
}
.item-intro-notice-icon-wrap {
  vertical-align: middle !important;
  line-height: 21px !important;
  margin-right: 2px !important;
}
.item-intro-notice-icon {
  display: inline-block !important;
  color: rgb(0, 132, 137) !important;
  font-size: 9px !important;
  height: 10px !important;
  margin-right: 1px !important;
  width: 9px !important;
}
@media (min-width: 1780px) {
  .item-wrap {
    width: 16.6667% !important;
  }
}

@media (max-width: 1779px) and (min-width: 1510px) {
  .item-wrap {
    width: 20% !important;
  }
}

@media (max-width: 1509px) and (min-width: 1240px) {
  .item-wrap {
    width: 25% !important;
  }
}

@media (min-width: 1780px) {
  .item-wrap {
    width: 16.6667% !important;
  }
}

@media (max-width: 1239px) and (min-width: 970px) {
  .item-wrap {
    width: 33.3333% !important;
  }
}

@media (max-width: 969px) {
  .item-wrap {
    width: 50% !important;
  }
}

@media (min-width: 744px) {
  .item-block {
    padding-right: 8px !important;
    padding-left: 8px !important;
  }
}
</style>