<template>
	<div class="content-wrap">
		<div style="margin-top:0;margin-bottom:0;margin-left:0;margin-right:0">
	    <div class="content-gap"></div>
	    <div class="content-layout-margin">
	    	<div class="host-info-wrap">
	    		<!-- scoll top bar -->

	    		<!-- left host info -->

	    		<!-- 民宿基本介紹 -->
	    		<wt-list-info id="summary"> 
	    		</wt-list-info>

	    		<!-- 換宿工作內容 -->
	    		<wt-list-info>
	    			<h2 slot="list-title" class="list-title-wrap">
	    				<div class="list-title-text"><span>《換宿工作內容》</span></div>
	    			</h2>
						<div slot="list-content" class="content-layout-margin">
							<section class="list-content-text">
								<ul>
                  <div style="margin-top: 8px;">
                     <li>提前入住時間7天取消可獲得50%退款，不含Airbnb服務費。</li>
                  </div>
                  <div style="margin-top: 8px;">
                      <li>若在距離入住時間7天內取消，則整筆預訂費用皆無法退款。</li>
                  </div>
                  <div style="margin-top: 8px;">
                    <li>只有在預訂後的48小時內取消預訂，且房客尚未入住房源時，我們才能退還Airbnb服務費。</li>
                  </div>
                </ul>		
							</section>
						</div>
						<div slot="list-more" class="list-text-notice">
							<button type="button" class="list-read-more-btn" aria-busy="false">
								<span>顯示全部</span>
							</button>
						</div>
	    		</wt-list-info>

	    		<!-- 換宿提供福利 -->
		    	<wt-list-info>
	    			<h2 slot="list-title" class="list-title-wrap">
	    				<div class="list-title-text"><span>換宿福利</span></div>
	    			</h2>
						<div slot="list-content" class="content-layout-margin">
							<section class="list-content-text">
								<ul>
                  <div style="margin-top: 8px;">
                     <li>提前入住時間7天取消可獲得50%退款，不含Airbnb服務費。</li>
                  </div>
                  <div style="margin-top: 8px;">
                      <li>若在距離入住時間7天內取消，則整筆預訂費用皆無法退款。</li>
                  </div>
                  <div style="margin-top: 8px;">
                    <li>只有在預訂後的48小時內取消預訂，且房客尚未入住房源時，我們才能退還Airbnb服務費。</li>
                  </div>
                </ul>		
							</section>
						</div>
						<div slot="list-more" class="list-text-notice">
							<button type="button" class="list-read-more-btn" aria-busy="false">
								<span>顯示全部</span>
							</button>
						</div>
	    		</wt-list-info>

	    		<!-- 換宿幫手需求條件 -->
	    		<wt-list-info>
	    			<h2 slot="list-title" class="list-title-wrap">
	    				<div class="list-title-text"><span>幫手需求</span></div>
	    			</h2>
						<div slot="list-content" class="content-layout-margin">
							<section class="list-content-text">
								<ul>
                  <div style="margin-top: 8px;">
                     <li>提前入住時間7天取消可獲得50%退款，不含Airbnb服務費。</li>
                  </div>
                  <div style="margin-top: 8px;">
                      <li>若在距離入住時間7天內取消，則整筆預訂費用皆無法退款。</li>
                  </div>
                  <div style="margin-top: 8px;">
                    <li>只有在預訂後的48小時內取消預訂，且房客尚未入住房源時，我們才能退還Airbnb服務費。</li>
                  </div>
                </ul>		
							</section>
						</div>
        
						<div slot="list-more" class="list-text-notice">
							<button type="button" class="list-read-more-btn" aria-busy="false">
								<span>顯示全部</span>
							</button>
						</div>
	    		</wt-list-info>
	    		<!-- right book panel -->
	    	</div>
	    </div>
	 	</div>
	</div>
</template>

<script>
	import wtListInfo from '@/components/wt-ListInfo.vue'
	export default {
		components: {
			wtListInfo
		}
	}
</script>

<style lang="less" scoped>
.content-wrap {
  margin-left: auto !important;
  margin-right: auto !important;
  width: auto !important;
  padding-left: 12px !important;
  padding-right: 12px !important;

  @media only screen and (min-width: 1128px) {
    max-width: 1080px !important;
  }
  @media only screen and (min-width: 744px) {
    padding-right: 24px !important;
    padding-left: 24px !important;
    max-width: 696px;  	
  }
}

.content-gap {
	margin-top: -51px !important;
	padding-top: 51px !important;
}

.content-layout-margin {
  margin-left: -8px !important;
  margin-right: -8px !important;

  &:before, &:after {
  	content: " " !important;
    display: table !important;
  }

  &:after {
  	clear: both !important;
  }
}

.host-info-wrap {
  padding-left: 8px !important;
  padding-right: 8px !important;
  min-height: 1px !important;
  position: relative !important;

  @media only screen and (min-width: 1128px) {
    width: 58.333333333333336% !important;
    float: left !important; /*for panel display*/
  }
}

.list-text-notice {
	font-weight: 600 !important;
  margin: 0px !important;
  word-wrap: break-word !important;
  font-size: 16px !important;
  line-height: 22px !important;
  letter-spacing: normal !important;
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  text-transform: undefined !important;
  color: #484848 !important;
  padding-top: undefined !important;
  padding-bottom: undefined !important;
}

.list-read-more-btn {
	color: #008489 !important;
  font: inherit !important;
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  text-decoration: none !important;
  -webkit-appearance: none !important;
  -moz-appearance: none !important;
  appearance: none !important;
  background: transparent !important;
  border: 0px !important;
  cursor: pointer !important;
  margin: 0px !important;
  padding: 0px !important;
  -webkit-user-select: auto !important;
  -moz-user-select: auto !important;
  -ms-user-select: auto !important;
  user-select: auto !important;
  text-align: left !important;	
}

.list-title-wrap {
	color: inherit !important;
  font-size: 1em !important;
  font-weight: inherit !important;
  line-height: inherit !important;
  margin: 0px !important;
  padding: 0px !important;
  display: inline !important;
}

.list-title-text {
  margin: 0px !important;
  word-wrap: break-word !important;
  font-size: 16px !important;
  line-height: 22px !important;
  letter-spacing: normal !important;
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  text-transform: undefined !important;
  color: #484848 !important;
  padding-top: undefined !important;
  padding-bottom: undefined !important;
  font-weight: 800 !important;
}

.list-content {
  padding-left: 8px !important;
  padding-right: 8px !important;
  min-height: 1px !important;
  position: relative !important;
  
}

.list-content-text {
	margin: 0px !important;
  word-wrap: break-word !important;
  font-size: 16px !important;
  line-height: 22px !important;
  letter-spacing: normal !important;
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  text-transform: undefined !important;
  color: #484848 !important;
  padding-top: undefined !important;
  padding-bottom: undefined !important;
  font-weight: normal !important;	
}
</style>