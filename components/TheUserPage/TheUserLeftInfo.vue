<template>
	<div class="col-lg-3 col-md-4 hide-sm">

	<!-- left propfile photo -->
		<div id="user" class="space-4 ">
	    <div class="space-2" id="user-media-container">
	      <div id="slideshow" class="profile-photo-wrap">
	        <img alt="Katie And Peter" class="img-responsive" height="225" src="https://a0.muscache.com/im/users/7629389/profile_pic/1374443098/original.jpg?aki_policy=profile_x_medium" title="Katie And Peter" width="225">
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
		        <div class="col-lg-3 col-middle wt-no-float">
		          <i class="far fa-check-circle checked-icon " aria-hidden="true"></i>
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

.profile-photo-wrap {
  position: relative;
  height: 230px;
  user-select: none;
}

.img-responsive {
	width: 100%;
	height: auto;
}
</style>