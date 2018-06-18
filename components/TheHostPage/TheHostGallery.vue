<template>
	<div class="host-gallery-wrap">
		<wt-modal></wt-modal>
	  <meta itemprop="image" content="imgUrl">
		<span>
			<div class="host-gallery-block" style="background-image:url('https://img.freepik.com/free-photo/blue-mountains-famous-tourism-scenery-lijiang_1417-1143.jpg?size=338&amp;ext=jpg')" aria-hidden="true"></div>
	    <div class="host-gallery-check-button">
	      <button type="button" class="host-gallery-button-style" aria-busy="false">
	      	<span class="button-text">
	      		<span>查看相片</span>
	      	</span>
	      </button>
	    </div>
	  </span>
	  <div>
	    <div class="host-gallery-button-list">
	    	<div class="wt-no-break-line">
	        <div class="wt-inline-block">
	        	<span>
	        		<div class="host-gallery-button-border">
	        			<button type="button" class="host-gallery-button-style" aria-busy="false">
	        				<span class="button-text">
		        				<div class="wt-table-nowidth" style="margin:0 auto">
		        					<div class="wt-vertical-nowidth">
		        						<div style="margin-right:12px">
		        							<svg viewBox="0 0 24 24" role="presentation" aria-hidden="true" focusable="false" style="height:15px;width:15px;display:block;fill:currentColor">
		        								<path d="m22.19 8.5h-3.14a.81.81 0 0 0 -.81.8c0 .44.36.8.81.8h2.33v12.31h-18.76v-12.31h3.11c.45 0 .81-.36.81-.8a.81.81 0 0 0 -.81-.8h-3.92a.81.81 0 0 0 -.81.8v13.91c0 .44.36.8.81.8h20.38c.45 0 .81-.36.81-.8v-13.91a.81.81 0 0 0 -.81-.8zm-14.11-3.82c.19 0 .36-.06.51-.18l2.01-1.58.6-.47v13.79c0 .44.36.8.81.8s.81-.36.81-.8v-13.79l.59.47 2.01 1.58a.8.8 0 0 0 .5.18.81.81 0 0 0 .63-.3.79.79 0 0 0 -.13-1.12l-3.92-3.09a.42.42 0 0 0 -.07-.04l-.07-.03-.01-.01-.05-.03a.76.76 0 0 0 -.3-.06.81.81 0 0 0 -.3.06l-.01.01-.06.04-.07.03a.42.42 0 0 0 -.07.04l-3.92 3.09a.79.79 0 0 0 -.13 1.12c.16.19.39.3.63.3z" fill-rule="evenodd"></path>
		        							</svg>
		        						</div>
		        					</div>
		        					<div class="wt-vertical-nowidth mobile-hide">分享</div>
		        				</div>
	        				</span>
	        			</button>
	            </div>
	          </span>
	        </div>
	        <div class="wt-inline-block" style="margin-left:18px">
	         	<span>
	         		<div class="host-gallery-button-border">
	         			<button type="button" class="host-gallery-button-style" aria-busy="false">
	         				<span class="button-text">
	         					<div class="wt-table-nowidth" style="margin:0 auto">
	         						<div class="wt-vertical-nowidth">
	         							<div style="margin-right:12px">
		         							<svg style="height:15px;width:15px;display:block" viewBox="0 0 32 32" fill="#484848" fill-opacity="0" stroke="#484848" stroke-width="1.5" aria-hidden="true" role="presentation" stroke-linecap="round" stroke-linejoin="round">
		         								<path d="m23.99 2.75c-.3 0-.6.02-.9.05-1.14.13-2.29.51-3.41 1.14-1.23.68-2.41 1.62-3.69 2.94-1.28-1.32-2.46-2.25-3.69-2.94-1.12-.62-2.27-1-3.41-1.14a7.96 7.96 0 0 0 -.9-.05c-1.88 0-7.26 1.54-7.26 8.38 0 7.86 12.24 16.33 14.69 17.95a1 1 0 0 0 1.11 0c2.45-1.62 14.69-10.09 14.69-17.95 0-6.84-5.37-8.38-7.26-8.38">
		         								</path>
		         							</svg>
	         							</div>
	         						</div>
	         					<div class="wt-vertical-nowidth mobile-hide">儲存</div>
	         					</div>
	         				</span>
	         			</button>
	          	</div>
	        	</span>
	      	</div>
	      </div>
			</div>
		</div>
	</div>
</template>
<script>
	import wtModal from '@/components/wt-Modal.vue'

	export default {	
		props: {
			imgs: {
				type: Array,
				default: () => { return []}
			}
		},
		data() {
			return {
				isGalleryOpen: false,
				isShareOpen: false,
				isFavoriteHost: false
			}
		},	

	  methods: {
	  	galleryTrigger() {

	  	},
	  	shareTrigger() {

	  	},
	  	saveToListTrigger() {

	  	}
	  },

	  components: {
	  	wtModal
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

		@media only screen and (min-width : 1128px) and (min-height : 700px) {
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

