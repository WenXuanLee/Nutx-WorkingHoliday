<template>
	<div class="display-item">
	  <a :href="hostUrl" class="portfolio-link">
      <div class="portfolio-hover">
        <div class="portfolio-hover-content">
            <h3 class="section-subheading text-muted">
            {{ hostName }}</h3> 
            <h3 class="section-subheading text-muted">
            {{ hostLocation }}</h3> 
        </div>
      </div>
      <img :src="imgUrl" class="img-responsive" alt="">
	  </a>
	</div>
</template>

<script>

export default {
	props: ['hostUrl', 'hostName', 'hostLocation', 'imgUrl']
}	
</script>

<style lang="less" scoped>

@white: #FFFFFF;
@black: #000000;
@dark_gray: lighten(@black, 20%);
@gray: lighten(@black, 40%);
@light_gray: lighten(@black, 60%);
@accent: #e74c3c;
@container_width: 800px;

.box-shadow( @h-shadow: 0px; @v-shadow: 1px; @blur: 2px; @spread: 0px; @color: fade(@black, 15%); ) {
  -webkit-box-shadow: @arguments;
  -moz-box-shadow: @arguments;
  box-shadow: @arguments;
}

.display-item {
	
}
.portfolio-item {
  margin: 0 0 15px;
  right: 0;
}

.portfolio-link {
	display: block;
	position: relative;
	max-height: 400px;
	margin: 0 auto;

	&:hover {
		.box-shadow(@blur: 35px; @color: fade(@black, 30%););
	}
}

.portfolio-hover {
	background: #7CEECE;
	position: absolute;
	width: 100%;
	height: 100%;
	opacity: 0;
	transition: all ease 0.5s;
	
	&:hover {
		opacity: 0.9;
	}
	.portfolio-hover-content {
		position: absolute;
	  width: 100%;
	  height: 20px;
	  font-size: 20px;
	  text-align: center;
	  top: 50%;
	  margin-top: -12px;
	  color: white;
	}
}

.section-subheading {
  font-size: 20px;
  font-family: "Droid Serif", "Helvetica Neue", Helvetica, Arial, sans-serif;
  text-transform: none;
  font-style: italic;
  font-weight: 400;
  margin-bottom: 75px;	
}
.text-muted {
  color: @white;
}

.img-responsive {
	display:block;
	max-width:100%;
	height:auto
}
</style>