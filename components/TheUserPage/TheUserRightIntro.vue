<template>
	<div class="col-lg-9 col-md-8 col-sm-12">
	  <div class="row space-4">
	  	<!-- for mobile profile photo -->
	    <div class="col-sm-4 show-sm">
	    </div>
	    <!-- basic Intro -->
			<the-user-right-intro-top-greet
				user-name="Ben"
				user-location="Taiwan"
				user-join-time="2018年7月"
				is-equal-broswer="true"></the-user-right-intro-top-greet>
		</div>

    <!-- brief deescription -->
		<div class="space-top-2">
		  <p>My husband and I have lived  in Hawaii for 16 years. We moved here from another island - Whidbey Island in Washington.  Love to bicycle, hike, swim, stand up board, meet new people, travel.
				<br>We have lived in California, New York,  Washington, Germany, and Switzerland.  
				<br>Ron's retired Boeing, I am an AutoCAD drafter.
				<br>I am the Finish Line Timing Coordinator for the Ironman in Kona.  
				<br>Have much Aloha!  Love living on the Big Island!  So many adventures to be had.  
			</p>
    </div>

    <!-- 機制獎勵顯示 -->
		<the-user-right-intro-mechanism 
			is-awesome-host="true" 
			is-awesome-helper="false"
			user-comments="10"
			is-validated="true"></the-user-right-intro-mechanism>
		<!-- 顯示推薦評價，評價區分為小幫手以及換宿主人評價，因使用者可能同時有兩種身分 -->
		<the-user-right-intro-host-recommend
			user-name="Ben"
			host-recommend-num="10"
			></the-user-right-intro-host-recommend> 
		<!-- 心願清單，暫時不弄 -->
		<div class="show-sm"></div>
		
		<!-- 評價區域 -->
		<the-user-right-intro-comment :all-comments="allComments"></the-user-right-intro-comment> 
	</div>
</template>

<script>
	import TheUserRightIntroTopGreet from '@/components/TheUserPage/TheUserRightIntroTopGreet.vue'
	import TheUserRightIntroMechanism from '@/components/TheUserPage/TheUserRightIntroMechanism.vue' 
	import TheUserRightIntroHostRecommend from '@/components/TheUserPage/TheUserRightIntroHostRecommend.vue' 
	import TheUserRightIntroComment from '@/components/TheUserPage/TheUserRightIntroComment.vue' 
	export default {
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
		},
		components: {
			TheUserRightIntroTopGreet,
			TheUserRightIntroMechanism,
			TheUserRightIntroHostRecommend,
			TheUserRightIntroComment
		}
	}
</script>
