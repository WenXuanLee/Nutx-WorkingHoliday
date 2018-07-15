<template>
	<div style="margin-top:18px;margin-bottom:0">
		<div v-if="isAwesomeHost" class="wt-inline-block mechanism-wrap">
			<div tabindex="0">
				<a class="mechanism-link" rel="noopener noreferrer nofollow">
					<div class="wt-text-break-word" id="superhost-badge-profile">
						<img id="superhost-badge-profile_image" alt="" src="https://a0.muscache.com/airbnb/static/badges/super_host_50_new-e5e09829e1fc5ffefdb2d7387590c462.png" width="28" height="50" class="mechanism-img">
						<div class="mechanism-text">
							<span class="mechanism-text-style">
								<span class="mechanism-text-margin">超讚房東</span>
							</span>
						</div>
					</div>
				</a>
			</div>
		</div>
		<div v-if="isAwesomeHelper" class="wt-inline-block mechanism-wrap">
			<div tabindex="0">
				<a class="mechanism-link" rel="noopener noreferrer nofollow">
					<div class="wt-text-break-word" id="superhost-badge-profile">
						<img id="superhost-badge-profile_image" alt="" src="https://a0.muscache.com/airbnb/static/badges/super_host_50_new-e5e09829e1fc5ffefdb2d7387590c462.png" width="28" height="50" class="mechanism-img">
						<div class="mechanism-text">
							<span class="mechanism-text-style">
								<span class="mechanism-text-margin">超讚小幫手</span>
							</span>
						</div>
					</div>
				</a>
			</div>
		</div>
		<div v-if="userComments" class="wt-inline-block mechanism-wrap">
			<a class="mechanism-link" rel="noopener noreferrer nofollow" href="/users/show/1474347#reviews">
				<div class="wt-text-break-word">
					<div id="undefined_count" class="mechanism-comment-style">
						<span class="wt-relative">{{ userComments }}</span>
					</div>
					<div class="mechanism-text">
						<span class="mechanism-text-style">
							<span class="mechanism-text-margin">則評價</span>
						</span>
					</div>
				</div>
			</a>
		</div>
		<div v-if="isValidated" class="wt-inline-block mechanism-wrap">
			<div tabindex="0">
				<a class="mechanism-link" rel="noopener noreferrer nofollow">
					<div class="wt-text-break-word" id="verified-id-icon">
						<img id="verified-id-icon_image" alt="" src="https://a0.muscache.com/airbnb/static/badges/verified_badge-6ee370f5ca86a52ed6198fac858ac1f4.png" width="32" height="32" class="mechanism-img">
						<div class="mechanism-text">
							<span class="mechanism-text-style">
								<span class="mechanism-text-margin">已驗證</span>
							</span>
						</div>
					</div>
				</a>
			</div>
		</div>
	</div>
</template>

<script> 
export default {
	props: {
		isAwesomeHost: {
			type: Boolean,
			default: false
		},
		isAwesomeHelper: {
			type: Boolean,
			default: false
		},
		userComments: {
			type: Number,
			default: 0,
			required: true,
		},
		isValidated: {
			type: Boolean,
			default: false,
		}
	}
}
</script>
<style lang="less" scoped>
.mechanism-wrap {
	margin-top: 0;
	margin-bottom: 24px;
	margin-right: 25px;
}
.mechanism-link {
  display: block !important; 
  color: inherit !important;
}
.mechanism-img {
  display: inline-block !important;
  width: auto !important;
}
.mechanism-text {
  display: inline-block !important;
  vertical-align: middle !important;
}
.mechanism-text-style {
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
  display: inline !important;

  .mechanism-text-margin {
    display: inline-block !important;
    margin-left: 12px !important;
	}
}

.mechanism-comment-style {
  border-radius: 6px !important;
  color: #ffffff !important;
  font-weight: bold !important;
  font-size: 18px !important;
  display: inline-block !important;
  padding: 6px 9px !important;
  min-width: 28px !important;
  position: relative !important;
  overflow: hidden !important;
  vertical-align: middle !important;
  background: -webkit-linear-gradient(140deg, #ffc333 55%, #FFB400 55%, #FFB400 100%) !important;
  background: -moz-linear-gradient(140deg, #ffc333 55%, #FFB400 55%, #FFB400 100%) !important;
  background: linear-gradient(140deg, #ffc333 55%, #FFB400 55%, #FFB400 100%) !important;
  line-height: 1.1 !important;
  text-rendering: optimizelegibility !important;
  text-align: center !important;
}
</style>