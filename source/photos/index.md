---
layout: single-column
slug: "photos"
noDate: "true"
comments: "false"
---
<link type="text/css" href="/css/ins.css" rel="stylesheet">
<link type="text/css" href="/css/jquery.fancybox.css" rel="stylesheet">

<!--<div class="instagram">
    <section class="archives album">
	    <ul class="img-box-ul">
	    </ul>
    </section>
</div>-->

<div class="myalbums">
	<div class="albums">
		<figure class="thumb">
			<div class="myalbums-box">
				<a href="./cat/"><img src="https://raw.githubusercontent.com/huixueee/00/master/photo/cat/封面1.jpg" class="nofancybox" width="100%" height="100%"></a>
			</div>
			<figcaption>猫咖</figcaption>
		</figure>
		<figure class="thumb">
			<div class="myalbums-box">
				<a href="./sanxia/"><img src="https://raw.githubusercontent.com/huixueee/00/master/photo/sanxia/QQ图片20181205210005.png" class="nofancybox" width="100%" height="100%"></a>
			</div>
			<figcaption>三峡</figcaption>
		</figure>
        <figure class="thumb">
        	<div class="myalbums-box">
        		<a href="./cat/"><img src="https://raw.githubusercontent.com/huixueee/00/master/photo/cat/封面1.jpg" class="nofancybox" width="100%" height="100%"></a>
        	</div>
        	<figcaption>西安</figcaption>
        </figure>
	</div>
</div>

<script src="https://lib.baomitu.com/jquery/3.3.1/jquery.js"></script>
<script src="/js/jquery.lazyload.js"></script>
<script src="/js/jquery.fancybox.js"></script>
<script src="/js/photos.js"></script>

<script>
	var that = this;
	$.getJSON("tool.json", function(data) {
		that.photo_render(that.page, data);
	});
	window.onload = function() {
		$("img.lazy").lazyload({
			effect: "fadeIn"
		});
	}
</script>
