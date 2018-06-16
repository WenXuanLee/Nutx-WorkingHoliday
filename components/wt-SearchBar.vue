<template>
<div class="searchbar-block">
	<div>
		<form class="wt-table" action="" method>
			<div class="wt-vertical-nowidth">
				<div class="wt-block">
					<div class="wt-relative">
				    <label class="search-label" for="search">地點</label>
				    <div dir="ltr">
							<div class="search-style">
								<div class="search-wrap">
								  <div class="wt-float-left">
								    <div class="search-icon-wrap">
								      <div class="search-icon-padding">
								        <svg viewBox="0 0 24 24" role="presentation" aria-hidden="true" focusable="false" style="height: 24px; width: 24px; display: block; fill: rgb(118, 118, 118);">
								          <path d="m10.4 18.2c-4.2-.6-7.2-4.5-6.6-8.8.6-4.2 4.5-7.2 8.8-6.6 4.2.6 7.2 4.5 6.6 8.8-.6 4.2-4.6 7.2-8.8 6.6m12.6 3.8-5-5c1.4-1.4 2.3-3.1 2.6-5.2.7-5.1-2.8-9.7-7.8-10.5-5-.7-9.7 2.8-10.5 7.9-.7 5.1 2.8 9.7 7.8 10.5 2.5.4 4.9-.3 6.7-1.7v.1l5 5c .3.3.8.3 1.1 0s .4-.8.1-1.1" fill-rule="evenodd"></path>
								        </svg>
								      </div>
								    </div>
								  </div>
			            <div class="wt-relative wt-overflow-hidden">
			              <input 
                      :placeholder="`試試「${ randomRecommand }」`" 
                      v-model="inputValue"
                      @keyup="searchResult"
                      type="text" 
                      autocomplete="off" 
                      class="search-text" 
                      id="search" 
                      name="query">
			            	<div class="search-delete-icon-wrap">
											<div v-if="hasInput" class="search-inline-block">
										    <button class="search-delete-button" type="button" @click.prevent="clearInput">
										      <svg viewBox="0 0 24 24" role="img" aria-label="Clear Input" focusable="false" style="height: 12px; width: 12px; display: block; fill: currentcolor;">
										         <path d="m23.25 24c-.19 0-.38-.07-.53-.22l-10.72-10.72-10.72 10.72c-.29.29-.77.29-1.06 0s-.29-.77 0-1.06l10.72-10.72-10.72-10.72c-.29-.29-.29-.77 0-1.06s.77-.29 1.06 0l10.72 10.72 10.72-10.72c.29-.29.77-.29 1.06 0s .29.77 0 1.06l-10.72 10.72 10.72 10.72c.29.29.29.77 0 1.06-.15.15-.34.22-.53.22" fill-rule="evenodd"></path>
										      </svg>
										    </button>
											</div>
										</div>
			            </div>									
								</div>
				      </div>
				    </div>	
					</div>
					<wt-search-bar-list-box 
            v-if="hasInput" 
            :list-item="fakeData"
            :selected-input="inputValue"></wt-search-bar-list-box>
		    </div>				
			</div>
		</form>
	</div>
</div>
</template>
<script>
  import wtSearchBarListBox from '@/components/wt-SearchBarListBox.vue'
	export default {
		props: {
	    fullWidth: {
	      type: Boolean,
	      default: false
	    } 
	  },
    components: {
      wtSearchBarListBox
    },
	  data() {
	  	return {
	  		inputValue: '',
	  		randomRecommand: 'Yooo' || '',
	  		fakeData: [ "Taipei", "Taipei City", "Taipei sucks" ],
        defaultIndexResult: 0
	  	}
	  },
	  computed: {
	  	hasInput() {
	  		return Boolean(this.inputValue)
	  	}
	  },
	  methods: {
	  	clearInput() {
	  		this.inputValue = ''
	  	},
      searchResult(e) {
        if(this.hasInput) {
          this.arrowSelectResult(e.keyCode)
        }
        console.log('send API request')
      },
      arrowSelectResult(arrowDirection) {
        let self = this
        switch(arrowDirection) {
          case 38:
            self.defaultIndexResult = self.defaultIndexResult - 1
            if(self.defaultIndexResult < 0) {
              self.defaultIndexResult = self.fakeData.length - 1
            }
            self.inputValue = self.fakeData[self.defaultIndexResult]
            break;
          case 40: 
            self.defaultIndexResult = self.defaultIndexResult + 1
            if(self.defaultIndexResult >= self.fakeData.length) {
              self.defaultIndexResult = 0
            }
            this.inputValue = this.fakeData[this.defaultIndexResult]
            break;
        }
      }
	  },

	}
</script>

<style lang="less" scoped>
.searchbar-block {
  font-size: 19px !important;
  line-height: 24px !important;
  background-color: #ffffff !important;
  border-radius: 4px !important;
  border: 1px solid #DBDBDB !important;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1) !important;
  padding: 0px !important;
  display: table !important;
  table-layout: fixed !important;
  height: 42px !important;
  width: 100% !important;
  position: relative !important;	

  &:before, &:after {
    content: " " !important;
    display: table !important; 	
  }

  &:after {
  	clear: both !important;
	} 
}

.search-label {
  position: absolute !important;
  display: block !important;
  border: 0px !important;
  margin: -1px !important;
  padding: 0px !important;
  height: 1px !important;
  width: 1px !important;
  clip: rect(0, 0, 0, 0) !important;
  overflow: hidden !important;
}

.search-style {
	font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  font-size: 16px !important;
  line-height: 22px !important;
  letter-spacing: undefined !important;
  padding-top: undefined !important;
  padding-bottom: undefined !important;
  color: #484848 !important;
  border-width: 1px !important;
  border-style: solid !important;
  border-radius: 2px !important;
  background-color: #ffffff !important;
  position: relative !important;
  z-index: 0 !important;
  margin-bottom: 0px !important;
  margin-top: 0px !important;
  margin-left: 0px !important;
  margin-right: 0px !important;
  border-color: #ffffff !important;
  display: block !important;
  width: 100% !important;	
}

.search-wrap {
	position: relative;
	overflow: hidden;
}
.search-icon-wrap {
	font-weight: 600 !important;
  padding-left: 12px !important;
  padding-top: 11px !important;	
}

.search-icon-padding {
	padding-left: 4px !important;
  padding-right: 5px !important;	
}

.search-text {
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  font-size: 16px !important;
  line-height: 22px !important;
  letter-spacing: undefined !important;
  padding-top: undefined !important;
  padding-bottom: undefined !important;
  color: #484848 !important;
  background-color: transparent !important;
  border: 0px !important;
  padding: 11px !important;
  width: 100% !important;
  font-weight: 600 !important;
  text-overflow: ellipsis !important;
	outline: none !important;
  &:focus{
  	outline: none !important;
  }
}

.search-delete-icon-wrap {
  position: absolute !important;
  right: 0px !important;
  top: 0px !important;
  bottom: 0px !important;
  height: 100% !important;

  &:before{
  	content: "" !important;
    display: inline-block !important;
    vertical-align: middle !important;
    height: 100% !important;
  }
}


.search-inline-block {
  vertical-align: middle !important;
  display: inline-block !important;	
}

.search-delete-button {
  color: rgb(118, 118, 118) !important;
  cursor: pointer !important;
  background: transparent !important;
  border-width: 0px !important;
  border-style: initial !important;
  border-color: initial !important;
  border-image: initial !important;
  padding: 12px !important;
}
</style>