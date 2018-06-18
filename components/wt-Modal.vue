<template>
	<div aria-modal="true" class="modal-wrap">
		<section>
		  <div class="modal-block">
		  	<!-- X icon part -->
		    <div class="modal-delete-mb">
		      <button @click.prevent="closeModal" type="button" class="modal-delete-button" aria-busy="false">
		        <svg viewBox="0 0 24 24" role="img" aria-label="關閉" focusable="false" style="height: 16px; width: 16px; display: block; fill: rgb(118, 118, 118);">
		        	<path d="m23.25 24c-.19 0-.38-.07-.53-.22l-10.72-10.72-10.72 10.72c-.29.29-.77.29-1.06 0s-.29-.77 0-1.06l10.72-10.72-10.72-10.72c-.29-.29-.29-.77 0-1.06s.77-.29 1.06 0l10.72 10.72 10.72-10.72c.29-.29.77-.29 1.06 0s .29.77 0 1.06l-10.72 10.72 10.72 10.72c.29.29.29.77 0 1.06-.15.15-.34.22-.53.22" fill-rule="evenodd"></path>
		        </svg>
		      </button>
		    </div>

		    <!-- modal header -->
		    <header>
					<slot name="title"></slot> 
		    </header>

		    <!-- modal content -->
		    <section>
					<slot name="content"></slot>
				</section>
			</div>
	</section>
	</div>	
</template>

<script>
	export default {
		props:{
			maxWidth: {
				type: Number,
				default: 0
			},
			isOpenModal: {
				type: Boolean,
				default: false,
			}
		},
		methods: {
			closeModal() {
				this.isOpenModal = false
			}
		}
	}
</script>

<style lang="less" scoped="">
	.modal-wrap {
	  background-color: rgb(255, 255, 255) !important;
	  width: 100% !important;
	  position: relative !important;
	  max-width: 376px !important; // 會隨props變動，待補
	  margin: auto !important;
	}
	
	.modal-block {
    background-color: rgb(255, 255, 255) !important;
    box-sizing: border-box !important;
    padding: 24px !important; // 會隨內容變動，待補
	}

	.modal-delete-mb {
		margin-bottom: 24px !important;
	}

	.modal-delete-button {
		cursor: pointer !important;
    background-color: transparent !important;
    color: buttontext !important;
    border: 0px !important;
    display: block !important;
    padding: 0px;
    margin: 0px;
	}
</style>