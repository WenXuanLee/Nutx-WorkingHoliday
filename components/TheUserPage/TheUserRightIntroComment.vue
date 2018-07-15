<template>
<div>
  <!--   
  心願清單區
    <div class="space-6 hide-sm">
    <h2 class="space-3">
    心願單
    <small>(2)</small>
    </h2>
    <div class="row">
      <div class="col-lg-4 col-md-6">
        <div class="panel">
          <a href="/wishlists/1957484" class="panel-image media-photo media-link media-photo-block wishlist-unit">
            <div class="media-cover media-cover-dark wishlist-bg-img" style="background-image:url('https://a0.muscache.com/im/pictures/23724394/47d546aa_original.jpg?aki_policy=medium');">
            </div>

            <div class="row row-table row-full-height">
              <div class="col-12 col-middle text-center text-contrast">
                <div class="panel-body">
                  <div class="h2"><strong>Vacation Places</strong></div>
                </div>
                <div class="btn btn-guest">3個房源</div>
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>
    <div class="space-top-2"></div>
    </div> 
  -->

  <!-- 評價區 -->
  <div class="row-space-4" id="reviews" tabindex="-1">
    <h2>
      評價
      <small>({{ allComments.totalComment}})</small>
    </h2>

    <div id="as_host">
      <h4 class="space-4">
        房客評價
      </h4>
      <div class="reviews">
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
    <div id="as_guest" class="space-top-3">
      <h4 class="space-4">
        房東評價
      </h4>
      <div class="reviews">
        <the-user-right-intro-comment-item 
          v-for="comment in allComments.userComment"
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
</template>

<script>
  import TheUserRightIntroCommentItem from '@/components/TheUserPage/TheUserRightIntroCommentItem.vue' 
  export default {
    props: {
      allComments: {
        type: Object,
      }
    },
    components: {
      TheUserRightIntroCommentItem
    }
  }
</script>