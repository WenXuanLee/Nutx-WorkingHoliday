<template>
	<main id="site-content" role="main" tabindex="-1">
	        
		<div class="page-container page-container-responsive space-top-4 space-8">
		  <div class="row">	

		  	<!-- side profile info -->
		  	<div class="col-lg-3 col-md-4 hide-sm">

	        <!-- left propfile photo -->
	        <div id="user" class="space-4 ">
	          <div>
	            <div class="space-2" id="user-media-container">
	              <div id="slideshow" class="slideshow">
	                <div class="slideshow-preload"></div>
	                <ul class="slideshow-images">
	                  <li class="active media-photo media-photo-block">
	                    <img alt="Katie And Peter" class="img-responsive" height="225" src="https://a0.muscache.com/im/users/7629389/profile_pic/1374443098/original.jpg?aki_policy=profile_x_medium" title="Katie And Peter" width="225">
	                  </li>
	                  <li class="media-photo media-photo-block"></li>
	                </ul>
	              </div>
	            </div>
	          </div>
	        </div>

	        <!-- left info panel -->
	        <wt-panel panelTitle="已驗證資訊">
	        	<div slot="panel-content" >
		        	<ul class="list-unstyled space-3" title="已驗證資訊">
				        <li v-for="(verify, index) in verifies" :key="index" class="row row-table space-2">
				          <div class="col-lg-12 col-middle wt-no-float">
				            {{ verify }}
				          </div>
				          <div class="col-lg-3 col-middle">
				            <i class="far fa-check-circle checked-icon" aria-hidden="true"></i>
				          </div>
				        </li>
			      	</ul>
			      	<a class="text-link" href="/help/article/1237">
		            了解詳情 »
		          </a> 
	        	</div>
	        </wt-panel>

	        <wt-panel panelTitle="關於我">
	          <dl slot="panel-content">
	          	<!-- 交叉如何使用v-for -->
	            <dt>語言</dt>
	            <dd>English</dd>
	            <dt>工作</dt>
	            <dd>前端工程師</dd>
	          </dl>
	        </wt-panel>

		  	</div>

		  	<!-- main profile intro -->
		    <div class="col-lg-9 col-md-8 col-sm-12">
		      <div class="row space-4">
		      	<!-- for mobile profile photo -->
		        <div class="col-sm-4 show-sm">
		        </div>
					</div>
				</div>
			</div>
		</div>
	</main> 
</template>

<script>
	import wtPanel from '@/components/wt-Panel.vue'
	export default {
		components: {
			wtPanel
		},
		data() {
			return {
				verifies: ['個人資訊', '電郵地址', '電話號碼']
			}
		}
	}
</script>

<style lang="less" scoped>

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
dt {
	font-weight: bold;
}
dd {
  display: block;
  -webkit-margin-start: 40px;
  margin-left: 0;
  margin-bottom: 10px;
}
.text-link {
  color: #008489;
  text-decoration: none;

  &:hover {
		color: #008489;
    text-decoration: underline  	
  }	
}
.checked-icon {
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  font-size: 24px;
}

.space-1 {
	margin-bottom: 6px;
}
.space-2 {
	margin-bottom: 12px;
}	
.space-3 {
	margin-bottom: 18px;
}	
.space-4 {
	margin-bottom: 24px;
}	
.space-5 {
	margin-bottom: 30px;
}	
.space-6 {
	margin-bottom: 36px;
}	
.space-7 {
	margin-bottom: 42px;
}	
.space-8 {
	margin-bottom: 48px;
}
.space-top-1 {
	margin-top: 6px;
}
.space-top-2 {
	margin-top: 12px;
}	
.space-top-3 {
	margin-top: 18px;
}	
.space-top-4 {
	margin-top: 24px;
}	
.space-top-5 {
	margin-top: 30px;
}	
.space-top-6 {
	margin-top: 36px;
}	
.space-top-7 {
	margin-top: 42px;
}	
.space-top-8 {
	margin-top: 48px;
}	
</style>