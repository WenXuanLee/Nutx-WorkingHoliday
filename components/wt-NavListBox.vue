<template>
<div class="dropdown-position">
	<div class="dropdown-wrap">
		<div class="dropdown-block">
			<div>
				<ul role="menu" id="headerNavUserMenu" aria-labelledby="headerNavUserButton" class="dropdown-ul">
					 <li role="none presentation">
				    <nuxt-link to="/editPage" role="menuitem" class="dropdown-item-wrap" >
				      <div class="dropdown-item-cotent">
				        <div class="_2930ex">
				          <div class="wt-vertical-center">
				            <div class="dropdown-item-text">
				              <span>編輯個人資料</span>
				            </div>
				          </div>
				        </div>
				      </div>
				    </nuxt-link>
				  </li>
				</ul>
			</div>
		</div>
	</div>
</div>	
</template>

<script>
	import wtNavListBoxItem from '@/components/wt-NavListBoxItem.vue'
	export default {
		props: {
			listBoxItem: {
				type: Array,
				default: () => { return [] }
			}
		},
		components: {
			wtNavListBoxItem
		}
	}
</script>

<style lang="less" scoped>
	.dropdown-position {
	  position: absolute !important;
	  top: 100% !important;
	  right: 0px !important;
	  padding-top: 24px !important;
	  margin-top: -24px !important;
	  width: 950px !important;
	  z-index: -1 !important;
	}

	.dropdown-wrap {
	  position: absolute !important;
	  width: 100% !important;
	  right: 0px !important;
	}

	.dropdown-block {
	  background-color: rgb(255, 255, 255) !important;
	  box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px !important;
	  min-width: 282px !important;
	  max-width: 950px !important;
	  min-height: 60px !important;
	  position: absolute !important;
	  right: 0px !important;
	  top: 0px !important;
	  border-width: 1px 1px 1px !important;
	  border-style: none solid solid !important;
	  border-color: rgb(219, 219, 219) rgb(219, 219, 219) rgb(219, 219, 219) !important;
	  border-image: initial !important;
	  border-top: none !important;
	}

	.dropdown-ul {
	  list-style-type: none !important;
	  padding: 0px !important;
	  margin: 0px !important;
	}	
	.dropdown-item-wrap {
  display: block !important;
  text-decoration: none !important;
  padding: 0px 16px;
}

.dropdown-item-cotent {
  display: table !important;
  color: rgb(72, 72, 72) !important;
  width: 100% !important;
  padding: 16px 0px !important;
  border-bottom: 1px solid rgb(242, 242, 242) !important;
  border-color: rgb(242, 242, 242) !important;

  &:hover {
    border-bottom: 1px solid rgb(118, 118, 118);
    border-color: rgb(118, 118, 118);
  }
}

.dropdown-item-text {
  font-weight: 600 !important;
  word-wrap: break-word !important;
  font-size: 14px !important;
  line-height: 18px !important;
  letter-spacing: normal !important;
  font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, "Helvetica Neue", sans-serif !important;
  color: rgb(118, 118, 118) !important;
  margin: 0px !important;
}

.dropdown-item-button {
  padding: 0px 16px;
  display: block !important;
  width: 100% !important;
  -webkit-appearance: none !important;
  cursor: pointer !important;
  text-align: left !important;
  user-select: auto !important;
  text-decoration: none !important;
  background: transparent !important;
  border-width: 0px !important;
  border-style: initial !important;
  border-color: initial !important;
  border-image: initial !important;
  margin: 0px !important;
}
</style>