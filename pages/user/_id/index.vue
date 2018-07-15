<template>
	<main id="site-content" role="main" tabindex="-1">
	        
		<div class="page-container page-container-responsive space-top-4 space-8">
		  <div class="row">	

		  	<!-- side profile info -->
				<the-user-left-info></the-user-left-info>

		  	<!-- main profile intro -->
				<the-user-right-intro></the-user-right-intro>
			</div>
		</div>
	</main> 
</template>

<script>
	import TheUserLeftInfo from '@/components/TheUserPage/TheUserLeftInfo.vue'
	import TheUserRightIntro from '@/components/TheUserPage/TheUserRightIntro.vue'
	export default {
	  components: {
	  	TheUserLeftInfo,
	  	TheUserRightIntro
	  }
	}
</script>

<style lang="less" scoped>

.page-container {
  width: 1080px;

  @media (min-width: 744px) {
	  padding-left: 24px;
	  padding-right: 24px;  	
  }
}
.page-container, .page-container-responsive {
  margin-left: auto;
  margin-right: auto;
  padding-left: 12px;
  padding-right: 12px;

  &:before {
		content: " ";
    display: table;
  }

  &:after {
		content: " ";
    display: table;
  	clear: both;
  }
}
.page-container-responsive {
  width: auto;

	@media (min-width: 744px) {
	 	width: 696px;
	 	padding-left: 24px;
    padding-right: 24px;
	}
	@media (min-width: 1128px) {
		width: 1080px;
		margin-left: auto;
    margin-right: auto;
    padding-left: 12px;
    padding-right: 12px;
	}
}




</style>