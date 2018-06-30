<template>
<div style="margin-bottom: 0px;">
  <section>
      <div style="margin-bottom: 16px;">
      	<slot name="list-title"></slot> 
      </div>
      <div>
				<slot name="list-content"></slot> 
      </div>
      <div>
      	<slot name="list-more"></slot>
      </div>
      <div class="content-gap-line"></div>
  </section>
</div>
</template>
<script>
  export default {
  	props: {
  		moreContent: {
  			type: Boolean,
  			default: false
  		},
  	}
  }
</script>

<style lang="less" scoped>
	.content-gap-line {
		margin: 24px 0px;
		border-bottom: 1px solid #DBDBDB !important;
	}
</style>