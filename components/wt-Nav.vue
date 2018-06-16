<template>
	<nav>
		<ul class="nav-wrap">
			<wt-nav-item nav-content="心願清單" :has-list-box="true" list-box=" 
			[
          {
            listItem: '編輯個人資料',
            listUrl: 'url1'
          },
          {
            listItem: '查看個人資料',
            listUrl: 'url1'
          },
          {
            listItem: '換宿申請',
            listUrl: 'url1'
          },
          {
            listItem: '登出',
            listUrl: 'url1'
          }
        ]"></wt-nav-item>
			<wt-nav-item nav-content="換宿管理" :has-list-box="true" list-box=" 
			[
          {
            listItem: '編輯個人資料',
            listUrl: 'url1'
          },
          {
            listItem: '查看個人資料',
            listUrl: 'url1'
          },
          {
            listItem: '換宿申請',
            listUrl: 'url1'
          },
          {
            listItem: '登出',
            listUrl: 'url1'
          }
        ]"></wt-nav-item>
		</ul>
	</nav>
</template>
<script>
	import wtNavItem from '@/components/wt-NavItem.vue'
	export default {
		components: {
			wtNavItem
		}
	}
</script>
<style lang="less" scoped>
	.nav-wrap {
		display: table !important;
		height: 64px !important;
		list-style: none !important;
		padding: 0px !important;
		margin: 0px !important;
	}
</style>