<template>
	<div class="avatar-wrapper">
	  <a :href="anchorUrl" class="text-muted" rel="nofollow">
	    <div class="media-photo media-round space-1">
	      <img :alt="avatarName" :title="avatarName" :src="imgUrl" :style="{ height: height, width: width }" >
	    </div>
	    <div v-if="avatarName" class="text-center text-wrap">
	      {{ avatarName }}
	    </div>
	  </a>   
    <span v-if="hasDateId" class="show-sm">
      <span class="text-muted">{{ commentDate }}</span>
      <span class="sm-review-date-divider">·</span>
      <span class="review-flag" :id="commentId">
        <button type="button" class="report-flag" aria-busy="false" style="padding: 0px; margin: 0px;">
          <svg viewBox="0 0 24 24" role="img" aria-label="檢舉此評價" focusable="false" style="height: 1em; width: 1em; display: block; fill: rgb(118, 118, 118);">
            <path d="m22.39 5.8-.27-.64a207.86 207.86 0 0 0 -2.17-4.87.5.5 0 0 0 -.84-.11 7.23 7.23 0 0 1 -.41.44c-.34.34-.72.67-1.13.99-1.17.87-2.38 1.39-3.57 1.39-1.21 0-2-.13-3.31-.48l-.4-.11c-1.1-.29-1.82-.41-2.79-.41a6.35 6.35 0 0 0 -1.19.12c-.87.17-1.79.49-2.72.93-.48.23-.93.47-1.35.71l-.11.07-.17-.49a.5.5 0 1 0 -.94.33l7 20a .5.5 0 0 0 .94-.33l-2.99-8.53a21.75 21.75 0 0 1 1.77-.84c.73-.31 1.44-.56 2.1-.72.61-.16 1.16-.24 1.64-.24.87 0 1.52.11 2.54.38l.4.11c1.39.37 2.26.52 3.57.52 2.85 0 5.29-1.79 5.97-3.84a.5.5 0 0 0 0-.32c-.32-.97-.87-2.36-1.58-4.04zm-4.39 7.2c-1.21 0-2-.13-3.31-.48l-.4-.11c-1.1-.29-1.82-.41-2.79-.41-.57 0-1.2.09-1.89.27a16.01 16.01 0 0 0 -2.24.77c-.53.22-1.04.46-1.51.7l-.21.11-3.17-9.06c.08-.05.17-.1.28-.17.39-.23.82-.46 1.27-.67.86-.4 1.7-.7 2.48-.85.35-.06.68-.1.99-.1.87 0 1.52.11 2.54.38l.4.11c1.38.36 2.25.51 3.56.51 1.44 0 2.85-.6 4.18-1.6.43-.33.83-.67 1.18-1.02a227.9 227.9 0 0 1 1.85 4.18l.27.63c.67 1.57 1.17 2.86 1.49 3.79-.62 1.6-2.62 3.02-4.97 3.02z" fill-rule="evenodd">                      
            </path>
          </svg>
        </button>
      </span>
    </span>     
	</div>
</template>
<script>
	export default {
		props: {
			anchorUrl: {
				type: String,
				default: '#'
			},
			imgUrl: {
				type: String,
				default: '',
				require: true
			},
			avatarName: {
				type: String,
				default: ''
			},
			commentId: {
				type: String,
			},
			commentDate: {
				type: String,
			},
			width: {
				type: [String, Number],
				default: '68px'
			},
			height: {
				type: [String, Number],
				default: '68px'
			}
		},
		computed: {
			hasDateId() {
				return Boolean(this.commentDate && this.commentId)
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

.report-flag {
  cursor: pointer !important;
  background-color: transparent !important;
  color: buttontext !important;
  display: inline-block !important;
  border-width: 0px !important;
  border-style: initial !important;
  border-color: initial !important;
  border-image: initial !important;
}
</style>