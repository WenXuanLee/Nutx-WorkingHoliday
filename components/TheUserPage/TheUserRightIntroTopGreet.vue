<template>
	<div class="col-sm-8 col-md-12 col-lg-12">
	  <h1 class="h1">您好, 我是{{ userName }}！</h1>
	  <div class="h5 space-top-2">
			<a href="/s/台灣" class="link-reset">{{ userLocation }}</a> ·
			<span class="text-normal">加入時間： {{ userJoinTime }}</span>
	  </div>
	  <div class="text-muted space-top-2">
	    <div class="flag-widget text-small">
	      <wt-button title="test1" type="button" custom-class="btn-link btn-link--reset btn-link--icon">
	      	<i class="far fa-flag"></i>
	    		<span class="link-icon__text">
	    			<span>檢舉此用戶</span>
	    		</span>
	      </wt-button>
	    </div>
	  </div>
	  <div v-if="isEqualBroswer" class="edit_profile_container space-3">
	    <a href="/users/edit">編輯個人資料</a>
	  </div>
	</div>
</template>

<script>
	import wtButton from '@/components/wt-Button.vue' 
	export default {
		props: {
			userName: {
				type: String,
				required: true
			},
			userLocation: {
				type: String,
				required: true
			},
			userJoinTime: {
				type: String,
				required: true
			},
			isEqualBroswer: {
				type: Boolean,
				default: false,
				required: true,
			}
		},
		components: {
			wtButton,
		}
	}
</script>