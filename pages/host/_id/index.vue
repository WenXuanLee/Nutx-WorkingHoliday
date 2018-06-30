<template>
	<main tabindex=-1 class="wt-relative">
		<section>
			<!-- itemScope為定義此事務物符合之類型 -->
			<div id="host" itemscope itemtype="https://schema.org/Service">
				<!-- hostPage 上方圖片區 -->
				<the-host-gallery />

				<!-- hostPage下方content -->
				<the-host-content />
			</div>
		</section>
	</main>
</template>
<script>
	import TheHostGallery from '@/components/TheHostPage/TheHostGallery.vue'
	import TheHostContent from '@/components/TheHostPage/TheHostContent.vue'
	export default {	
		// prtend to send API request
	  asyncData() {
	    return new Promise((resolve, reject) => {
	      setTimeout(() => {
	        resolve({
	          host: [
	          ]          
	        }, 15000)
	      })
	    })
	  },
	  components: {
	  	TheHostGallery,
	  	TheHostContent
	  }
	}
</script>
<style lang="less" scoped>
	.host-gallery-wrap {
		position: relative !important;
    width: 100% !important;
    background-color: #ffffff !important;
    cursor: pointer !important;
	}
	.host-gallery-block {
		background-repeat: no-repeat !important;
    background-size: cover !important;
    background-position: 50% 50% !important;
    height: 368px !important;

		@media only screen and (min-width : 1128px) and (min-width : 700px) {
			height: 552px !important;
		}

		@media only screen and (min-width : 744px) and (min-height : 700px) {
			height: 441.6px !important;
		}

		@media only screen and (min-width : 1128px) and (min-height : 700px) {
			height: 368px !important;	
		}
	}
	.host-gallery-button-border {
		display: inline-block !important;
    box-shadow: 0 1px 1px 1px rgba(0, 0, 0, 0.14) !important;
    border-radius: 4px !important;
	}
	.host-gallery-check-button {
		position: absolute !important;
	  left: auto !important;
	  right: 20px !important;
	  bottom: 30px !important;
	  box-shadow: 0 1px 1px 1px rgba(0, 0, 0, 0.14) !important;	

	  @media only screen and (min-width: 744px) {
	    bottom: 20px !important;
	    left: 20px !important;
	    right: auto !important;	  	
	  }	
	}

	.host-gallery-button-style {
    cursor: pointer !important;
    display: inline-block !important;
    margin: 0px !important;
    position: relative !important;
    text-align: center !important;
    text-decoration: none !important;
    transition-property: background, border-color, color !important;
    transition-duration: 0.2s !important;
    transition-timing-function: ease-out !important;
    width: auto !important;
    border-radius: 4px !important;
    font-size: 14px !important;
    line-height: 18px !important;
    letter-spacing: normal !important;
    font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
    text-transform: undefined !important;
    padding-top: 8px !important;
    padding-bottom: 8px !important;
    font-weight: 600 !important;
    border-width: 1px !important;
    border-style: solid !important;
    padding-left: 16px !important;
    padding-right: 16px !important;
    min-width: 51.77708763999664px !important;
    box-shadow: none !important;
    background: #ffffff !important;
    border-color: transparent !important;
    color: #484848 !important;

    .button-text {
			font-size: 14px !important;
	    line-height: 18px !important;
	    letter-spacing: normal !important;
	    font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
	    text-transform: undefined !important;
	    color: inherit !important;
	    padding-top: undefined !important;
	    padding-bottom: undefined !important;
    }
	}

	.host-gallery-button-list {
    position: absolute !important;
    top: 24px !important;
    right: 24px !important;	

    @media screen and (max-width: 768px) {
    	.host-gallery-button-style {
			  cursor: pointer !important;
			  background-color: transparent !important;
			  color: white !important;
			  border: 0px !important;
			  display: inline-block !important;
			  padding: 0;
			  margin: 0;
    	}

    	.mobile-hide {
    		display: none !important;
    	}
    }	
	}
</style>

