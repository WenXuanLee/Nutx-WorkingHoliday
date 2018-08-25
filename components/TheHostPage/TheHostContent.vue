<template>
	<div class="content-wrap">
		<div style="margin-top:0;margin-bottom:0;margin-left:0;margin-right:0">
	    <div class="content-gap"></div>
	    <div class="content-layout-margin">
	    	<div class="host-info-wrap">
	    		<!-- scoll top bar -->

	    		<!-- left host info -->

	    		<!-- 民宿基本介紹 -->
	    		<wt-list-info id="summary"> 
	    		</wt-list-info>

	    		<!-- 換宿工作內容 -->
	    		<wt-list-info>
	    			<h2 slot="list-title" class="list-title-wrap">
	    				<div class="list-title-text"><span>《換宿工作內容》</span></div>
	    			</h2>
						<div slot="list-content" class="content-layout-margin">
							<section class="list-content-text">
								<ul>
                  <div style="margin-top: 8px;">
                     <li>提前入住時間7天取消可獲得50%退款，不含Airbnb服務費。</li>
                  </div>
                  <div style="margin-top: 8px;">
                      <li>若在距離入住時間7天內取消，則整筆預訂費用皆無法退款。</li>
                  </div>
                  <div style="margin-top: 8px;">
                    <li>只有在預訂後的48小時內取消預訂，且房客尚未入住房源時，我們才能退還Airbnb服務費。</li>
                  </div>
                </ul>		
							</section>
						</div>
						<div slot="list-more" class="list-text-notice">
							<button type="button" class="list-read-more-btn" aria-busy="false">
								<span>顯示全部</span>
							</button>
						</div>
	    		</wt-list-info>

	    		<!-- 換宿提供福利 -->
		    	<wt-list-info>
	    			<h2 slot="list-title" class="list-title-wrap">
	    				<div class="list-title-text"><span>換宿福利</span></div>
	    			</h2>
						<div slot="list-content" class="content-layout-margin">
							<section class="list-content-text">
								<ul>
                  <div style="margin-top: 8px;">
                     <li>提前入住時間7天取消可獲得50%退款，不含Airbnb服務費。</li>
                  </div>
                  <div style="margin-top: 8px;">
                      <li>若在距離入住時間7天內取消，則整筆預訂費用皆無法退款。</li>
                  </div>
                  <div style="margin-top: 8px;">
                    <li>只有在預訂後的48小時內取消預訂，且房客尚未入住房源時，我們才能退還Airbnb服務費。</li>
                  </div>
                </ul>		
							</section>
						</div>
						<div slot="list-more" class="list-text-notice">
							<button type="button" class="list-read-more-btn" aria-busy="false">
								<span>顯示全部</span>
							</button>
						</div>
	    		</wt-list-info>

	    		<!-- 換宿幫手需求條件 -->
	    		<wt-list-info>
	    			<h2 slot="list-title" class="list-title-wrap">
	    				<div class="list-title-text"><span>幫手需求</span></div>
	    			</h2>
						<div slot="list-content" class="content-layout-margin">
							<section class="list-content-text">
								<ul>
                  <div style="margin-top: 8px;">
                     <li>提前入住時間7天取消可獲得50%退款，不含Airbnb服務費。</li>
                  </div>
                  <div style="margin-top: 8px;">
                      <li>若在距離入住時間7天內取消，則整筆預訂費用皆無法退款。</li>
                  </div>
                  <div style="margin-top: 8px;">
                    <li>只有在預訂後的48小時內取消預訂，且房客尚未入住房源時，我們才能退還Airbnb服務費。</li>
                  </div>
                </ul>		
							</section>
						</div>
        
						<div slot="list-more" class="list-text-notice">
							<button type="button" class="list-read-more-btn" aria-busy="false">
								<span>顯示全部</span>
							</button>
						</div>
	    		</wt-list-info>
          <!-- 評價區域 -->
          <div class="row-space-4" id="reviews" tabindex="-1">
            <h2 class="list-title-wrap">
              <div class="list-title-text wt-mb"><span>{{ allComments.totalComment}}則評價</span></div>
            </h2>
            <div id="as_host ">
              <div class="reviews wt-mt">
                <the-user-right-intro-comment-item 
                  v-for="comment in allComments.hostComment"
                  :key="comment.commentId"
                  :user-name="comment.userName"
                  :user-link="comment.userLink"
                  :user-img="comment.userImg"
                  :user-location="comment.userLocation"
                  :comment-date="comment.commentDate"
                  :comment-id="comment.commentId"
                  :comment-content="comment.commentContent"></the-user-right-intro-comment-item>    
              </div>
            </div>
          </div>
	    		
	    	</div>
        <!-- right book panel -->
        <div class="host-apply-panel">
          
        </div>
	    </div>
	 	</div>
	</div>
</template>

<script>

  import TheUserRightIntroCommentItem from '@/components/TheUserPage/TheUserRightIntroCommentItem.vue' 
  import TheUserRightIntroComment from '@/components/TheUserPage/TheUserRightIntroComment.vue' 
	import wtListInfo from '@/components/wt-ListInfo.vue'
	export default {
		components: {
			wtListInfo,
      TheUserRightIntroComment,
      TheUserRightIntroCommentItem
		},
    data() {
      return {
        allComments: {
          "hostComment": [
            {
              "userName": "Morgan",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Comptche",
              "commentDate": "2014-06-08",
              "commentId": "5b4afd5dd52c8fe0e85c5308",
              "commentContent": "Nostrud pariatur aliquip cupidatat Lorem nostrud fugiat. Excepteur exercitation eu officia enim et ea officia est nisi exercitation officia aliqua. Voluptate exercitation adipisicing Lorem aliqua esse consequat sunt est qui ad enim. Ea elit pariatur in nostrud tempor. Dolor tempor esse anim officia eiusmod aute. Laborum voluptate ullamco aliqua velit ad quis. Excepteur cillum aliquip laborum veniam do incididunt cupidatat aliquip."
            },
            {
              "userName": "Carol",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Gibsonia",
              "commentDate": "2015-01-11",
              "commentId": "5b4afd5d653f3d3a64c7f973",
              "commentContent": "Incididunt est pariatur nulla est sunt mollit proident do. Reprehenderit exercitation fugiat exercitation anim consectetur dolor duis duis in. Esse ullamco aliqua laborum et."
            },
            {
              "userName": "Lupe",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Dante",
              "commentDate": "2014-01-31",
              "commentId": "5b4afd5d5d9453c897762aaa",
              "commentContent": "Pariatur laborum nisi voluptate tempor sit amet do. Excepteur nostrud quis exercitation ut labore Lorem sit irure consectetur qui adipisicing. Et excepteur deserunt sit consequat occaecat irure veniam deserunt duis reprehenderit ut laborum. Ullamco voluptate tempor sit commodo pariatur quis."
            },
            {
              "userName": "Marcia",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Eden",
              "commentDate": "2016-12-13",
              "commentId": "5b4afd5dea1b0d7ba9d32fcc",
              "commentContent": "Excepteur duis voluptate cillum exercitation nisi nisi ex cillum magna sunt tempor. Laboris et pariatur id duis nostrud cillum. Consequat labore veniam labore enim fugiat dolore enim."
            },
            {
              "userName": "Geraldine",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Hoagland",
              "commentDate": "2018-04-04",
              "commentId": "5b4afd5d05db30e23a81e4b0",
              "commentContent": "Aute fugiat ea ut duis veniam ex aliquip. Labore officia commodo excepteur nostrud veniam ut qui sit exercitation nulla cillum sint. Commodo commodo occaecat culpa commodo esse cillum non consectetur magna ex deserunt consectetur amet consectetur. Aliqua elit esse cillum amet pariatur sint dolor aliqua eu consequat."
            },
            {
              "userName": "Eddie",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Roulette",
              "commentDate": "2015-06-28",
              "commentId": "5b4afd5dc17b9f562e14e1f4",
              "commentContent": "Laboris eiusmod sint ea sint laboris esse cillum laboris cillum non. Laborum aliquip deserunt commodo est nisi nostrud laborum pariatur mollit est irure ullamco. Dolor eiusmod aute sit id nulla ea adipisicing voluptate duis ea mollit."
            },
            {
              "userName": "Fannie",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Caledonia",
              "commentDate": "2017-09-14",
              "commentId": "5b4afd5d2c2aa723eceb6800",
              "commentContent": "Eiusmod do Lorem cupidatat esse laborum tempor cupidatat cupidatat. Consequat proident fugiat occaecat dolor ut nostrud. Dolor pariatur dolor id eiusmod. Cillum consectetur anim exercitation consequat sint dolore minim."
            },
            {
              "userName": "Bridgette",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Takilma",
              "commentDate": "2016-04-05",
              "commentId": "5b4afd5df439b522cca4e520",
              "commentContent": "Exercitation anim id laborum irure in consequat sit. Tempor minim aliquip ut aliquip culpa cupidatat aute ut aliquip dolore reprehenderit ipsum. Dolore anim enim consectetur exercitation labore sunt consectetur amet commodo quis excepteur do mollit."
            },
            {
              "userName": "Allison",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Smock",
              "commentDate": "2015-08-23",
              "commentId": "5b4afd5dffd0edc6204daf89",
              "commentContent": "Cillum irure in culpa pariatur sint eiusmod sint aute amet deserunt excepteur non anim. Ea consectetur proident exercitation officia deserunt proident aliqua est nulla quis esse nostrud nostrud quis. Officia aliqua qui ad laboris dolor est anim quis cillum exercitation. Amet consectetur qui duis est enim nostrud est voluptate minim pariatur. Do occaecat labore consectetur quis sunt deserunt adipisicing non."
            }
          ],
          "userComment": [
            {
              "userName": "Kirkland",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Matheny",
              "commentDate": "2017-11-14",
              "commentId": "5b4afd5daaad9b5dad37e145",
              "commentContent": "Fugiat esse cupidatat anim ullamco magna nulla. Ad veniam nisi velit aute dolor magna laboris aute est. Ullamco anim consectetur ad qui reprehenderit et laborum nostrud aliqua Lorem Lorem cupidatat enim. Aliqua incididunt eiusmod non voluptate ad cupidatat magna nisi consectetur."
            },
            {
              "userName": "Hickman",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Roosevelt",
              "commentDate": "2016-07-01",
              "commentId": "5b4afd5d69d69e417ac25e14",
              "commentContent": "Et ullamco commodo aute est magna nisi duis. Proident duis adipisicing officia Lorem sit laborum tempor do tempor dolore amet exercitation cillum. Elit nostrud et officia ipsum duis ut. Ea fugiat cillum qui ex eiusmod ut occaecat esse excepteur. Eiusmod duis excepteur consectetur eiusmod do ad exercitation deserunt."
            },
            {
              "userName": "Socorro",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Marenisco",
              "commentDate": "2016-06-30",
              "commentId": "5b4afd5d89e44e6d317a24ae",
              "commentContent": "Magna deserunt id deserunt ipsum. Ipsum culpa nisi minim dolor laborum incididunt. Enim quis id dolore excepteur eiusmod nostrud irure."
            },
            {
              "userName": "Garrison",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Abiquiu",
              "commentDate": "2017-06-18",
              "commentId": "5b4afd5d0c1dc4251efce1aa",
              "commentContent": "Nostrud pariatur commodo id et irure cillum duis aliquip id est labore. Consequat occaecat sunt eiusmod ex non. Deserunt culpa aliquip sint ullamco ipsum amet eiusmod labore occaecat Lorem occaecat eiusmod nulla. In id commodo ipsum mollit dolore proident et proident. Exercitation minim adipisicing excepteur magna consectetur aliqua sit. Ipsum nisi fugiat labore velit nulla deserunt in eu mollit laborum dolore."
            },
            {
              "userName": "Brown",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Wakulla",
              "commentDate": "2017-10-26",
              "commentId": "5b4afd5d248f039841bc72f4",
              "commentContent": "Irure sunt consectetur sunt occaecat quis anim reprehenderit quis qui laboris voluptate occaecat officia non. Aliquip tempor nostrud laborum amet in. Quis incididunt in ullamco cillum. Mollit sint ea consequat nostrud tempor labore anim. Anim magna pariatur quis et aliqua sint excepteur labore non nostrud culpa."
            },
            {
              "userName": "Rose",
              "userLink": "http://placehold.it/32x32",
              "userImg": "http://placehold.it/32x32",
              "userLocation": "Gracey",
              "commentDate": "2017-04-20",
              "commentId": "5b4afd5d04b20be8dbbb5af4",
              "commentContent": "Aliquip do velit non commodo duis amet pariatur. Veniam enim veniam duis aliquip mollit elit occaecat nisi velit ipsum elit sint. Sit non elit aliquip cillum cupidatat voluptate eu consectetur occaecat cupidatat cupidatat incididunt. Nisi elit ex exercitation pariatur dolor aliqua quis consequat dolor cupidatat."
            }
          ],
          "totalComment": 31
        }        
      }
    }
	}
</script>

<style lang="less" scoped>
.content-wrap {
  margin-left: auto !important;
  margin-right: auto !important;
  width: auto !important;
  padding-left: 12px !important;
  padding-right: 12px !important;

  @media only screen and (min-width: 1128px) {
    max-width: 1080px !important;
  }
  @media only screen and (min-width: 744px) {
    padding-right: 24px !important;
    padding-left: 24px !important;
    max-width: 696px;  	
  }
}

.content-gap {
	margin-top: -51px !important;
	padding-top: 51px !important;
}

.content-layout-margin {
  margin-left: -8px !important;
  margin-right: -8px !important;

  &:before, &:after {
  	content: " " !important;
    display: table !important;
  }

  &:after {
  	clear: both !important;
  }
}

.host-info-wrap, .host-panel-wrap {
  padding-left: 8px !important;
  padding-right: 8px !important;
  min-height: 1px !important;
  position: relative !important;

  @media only screen and (min-width: 1128px) {
    width: 58.333333333333336% !important;
    float: left !important; /*for panel display*/
  }
}

.host-panel-wrap {
  @media only screen and (min-width: 1128px) {
    width: 41.6666666666% !important;
    float: left !important; /*for panel display*/
  }
}

.list-text-notice {
	font-weight: 600 !important;
  margin: 0px !important;
  word-wrap: break-word !important;
  font-size: 16px !important;
  line-height: 22px !important;
  letter-spacing: normal !important;
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  text-transform: undefined !important;
  color: #484848 !important;
  padding-top: undefined !important;
  padding-bottom: undefined !important;
}

.list-read-more-btn {
	color: #008489 !important;
  font: inherit !important;
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  text-decoration: none !important;
  -webkit-appearance: none !important;
  -moz-appearance: none !important;
  appearance: none !important;
  background: transparent !important;
  border: 0px !important;
  cursor: pointer !important;
  margin: 0px !important;
  padding: 0px !important;
  -webkit-user-select: auto !important;
  -moz-user-select: auto !important;
  -ms-user-select: auto !important;
  user-select: auto !important;
  text-align: left !important;	
}

.list-title-wrap {
	color: inherit !important;
  font-size: 1em !important;
  font-weight: inherit !important;
  line-height: inherit !important;
  margin: 0px !important;
  padding: 0px !important;
  display: inline !important;
}

.list-title-text {
  margin: 0px !important;
  word-wrap: break-word !important;
  font-size: 16px !important;
  line-height: 22px !important;
  letter-spacing: normal !important;
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  text-transform: undefined !important;
  color: #484848 !important;
  padding-top: undefined !important;
  padding-bottom: undefined !important;
  font-weight: 800 !important;
}

.list-content {
  padding-left: 8px !important;
  padding-right: 8px !important;
  min-height: 1px !important;
  position: relative !important;
  
}

.list-content-text {
	margin: 0px !important;
  word-wrap: break-word !important;
  font-size: 16px !important;
  line-height: 22px !important;
  letter-spacing: normal !important;
  font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
  text-transform: undefined !important;
  color: #484848 !important;
  padding-top: undefined !important;
  padding-bottom: undefined !important;
  font-weight: normal !important;	
}
</style>