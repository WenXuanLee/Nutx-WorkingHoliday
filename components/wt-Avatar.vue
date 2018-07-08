<template>
	<div class="avatar-wrapper">
	  <a :href="anchorUrl" class="text-muted" rel="nofollow">
	    <div class="media-photo media-round space-1">
	      <img alt="Hanna" :src="imgUrl" :style="{ height: height, width: width }" >
	    </div>
	    <div v-if="avatarName" class="text-center text-wrap">
	      {{ avatarName }}
	    </div>
	  </a>        
	</div>
</template>
<script>
	export default {
		props: {
			anchorUrl: {
				type: String,
				default: '#'
			}
			imgUrl: {
				type: String,
				default: '',
				require: true
			},
			avatarName: {
				type: String,
				default: ''
			},
			width: {
				type: Number,
				default: 68
			},
			height: {
				type: Number,
				default: 68
			}
		}
	}
</script>

<style lang="less" scoped>

.avatar-wrapper {
  @media (min-width: 744px) {
   	float: right;
  }
}
.media-photo {
  -webkit-backface-visibility: hidden;
  -moz-backface-visibility: hidden;
  backface-visibility: hidden;
  position: relative;
  display: inline-block;
  vertical-align: bottom;
  overflow: hidden;
  background-color: #bbb;
}	

.media-round {
  -webkit-border-radius: 50%;
  -moz-border-radius: 49%;
  border-radius: 50%;
  border: 2px solid #fff;
}

</style>