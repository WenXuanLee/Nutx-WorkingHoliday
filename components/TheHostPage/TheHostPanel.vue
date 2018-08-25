<template>
	<div class="panel-wrap">
	  <div style="margin-top:16px;margin-bottom:24px">
	    <div>
	      <div>
					<div class="panel-title-line-height">
						<div class="wt-inline-block">
							<span class="panel-bold-text">
								<span class="text-large">$1,995</span>
							</span> 
							<span class="panel-hint-text">
								<span>一晚</span>
							</span>
    				</div>
					</div>
					<div>
	    			<button type="button" class="botton-wrap" aria-label="查看所有評價。在477則評價中平均獲得5星（滿分5星）。" aria-busy="false">
	    				<span>
	    					<span role="img" aria-label="評分是5（滿分為5）">
	    						<span class="icon-setting">
	    							<svg viewBox="0 0 1000 1000" role="presentation" aria-hidden="true" focusable="false" style="height:1em;width:1em;display:block;fill:currentColor">
	    								<path d="M971.5 379.5c9 28 2 50-20 67L725.4 618.6l87 280.1c11 39-18 75-54 75-12 0-23-4-33-12l-226.1-172-226.1 172.1c-25 17-59 12-78-12-12-16-15-33-8-51l86-278.1L46.1 446.5c-21-17-28-39-19-67 8-24 29-40 52-40h280.1l87-278.1c7-23 28-39 52-39 25 0 47 17 54 41l87 276.1h280.1c23.2 0 44.2 16 52.2 40z">
	    								</path>
	    							</svg>
	    						</span>
								</span> 
								<span class="panel-hint-text"><span>477</span></span>
	        		</span>
	    			</button>
					</div>
			    <div class="line-separation"></div>
				</div>
				<form action="/payments/book?hosting_id=12351" id="book_it_form" method="post">
			    <div class="book-it__fields standard">
			      <div style="margin-top:16px;margin-bottom:8px">
		          <label for="dates_12351" class="text-label">
		          	<small class="text-label-small">
		          		<span>日期</span>
		          	</small>
		          </label>
		          <div class="text-bold-6">
		            <div class="wt-relative wt-inline-block">
		              <div>
		                <div class="panel-datepicker-wrap">
											<!-- datepicker -->
		                </div>
		              </div>
		            </div>
		          </div>
			      </div>
			    </div>
			    <div style="margin-top:24px">
			      <button type="submit" class="panel-button-submit" aria-busy="false" data-veloute="book-it-button">
		      		<div class="submit-text">
		      			<span>申請預訂</span>
		      		</div>
			    	</button>
			    </div>
				</form>
			</div>
		</div>
	</div>	
</template>

<script>
	export default {

	}
</script>

<style lang="less" scoped>
.panel-wrap {
  padding-left: 24px !important;
  padding-right: 24px !important;
  margin: 0px !important;
  border: 1px solid #e4e4e4 !important;
  background-color: #ffffff !important;
}
.panel-title-line-height {
	line-height: 10px !important;
}
.panel-bold-text {
  word-wrap: break-word !important;
  font-size: 18px !important;
  line-height: 26px !important;
  letter-spacing: normal !important;
  font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, "Helvetica Neue", sans-serif !important;
  color: rgb(72, 72, 72) !important;
  font-weight: 800 !important;
  display: inline !important;
  margin: 0px !important;
}
.panel-hint-text {
  font-weight: 600 !important;
  margin: 0px !important;
  word-wrap: break-word !important;
  font-size: 12px !important;
  line-height: 16px !important;
  letter-spacing: normal !important;
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  text-transform: undefined !important;
  color: #484848 !important;
  padding-top: undefined !important;
  padding-bottom: undefined !important;
  display: inline !important;
}

.panel-datepicker-wrap {
  background-color: #fff !important; 
  display: block !important; 
  border: 1px solid #EBEBEB !important;
  border-radius: 2px !important;
  width: 100% !important;
}
.line-separation {
	margin: 24px 0px;
	border-bottom: 1px solid #DBDBDB !important;
}
.botton-wrap {
  -webkit-appearance: none !important;
  -moz-appearance: none !important;
  appearance: none !important;
  background: transparent !important;
  border: 0px !important;
  cursor: pointer !important;
  margin: 0px !important;
  padding: 0px !important;
  text-align: left !important;
  -webkit-user-select: auto !important;
  -moz-user-select: auto !important;
  -ms-user-select: auto !important;
  user-select: auto !important;
  vertical-align: bottom !important;
}
.panel-button-submit {
    cursor: pointer !important;
    display: inline-block !important;
    margin: 0px !important;
    position: relative !important;
    text-align: center !important;
    text-decoration: none !important;
    transition-property: background, border-color, color !important;
    transition-duration: 0.2s !important;
    transition-timing-function: ease-out !important;
    border-radius: 4px !important;
    width: 100% !important;
    font-size: 16px !important;
    line-height: 22px !important;
    letter-spacing: normal !important;
    font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
    text-transform: undefined !important;
    padding-top: 12px !important;
    padding-bottom: 12px !important;
    font-weight: 800 !important;
    border-width: 2px !important;
    border-style: solid !important;
    padding-left: 24px !important;
    padding-right: 24px !important;
    min-width: 77.66563145999496px !important;
    box-shadow: none !important;
    background: #FF5A5F !important;
    border-color: transparent !important;
    color: #ffffff !important;

    .submit-text {
	    margin: 0px !important;
	    word-wrap: break-word !important;
	    font-size: 16px !important;
	    line-height: 22px !important;
	    letter-spacing: normal !important;
	    font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
	    text-transform: undefined !important;
	    padding-top: undefined !important;
	    padding-bottom: undefined !important;
	    font-weight: 800 !important;
	    color: #ffffff !important;
		}
}
.text-label-small {
  font-weight: 600 !important;
  margin: 0px !important;
  word-wrap: break-word !important;
  font-size: 12px !important;
  line-height: 16px !important;
  letter-spacing: normal !important;
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  color: #484848 !important;
}
.icon-setting {
  display: inline-block !important;
  color: #008489 !important;
  font-size: 9px !important;
  height: 10px !important;
  margin-right: 1px !important;
  width: 9px !important;
}
</style>