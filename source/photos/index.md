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
				<a href="./cat/"><img src="http://pnxkcdttf.bkt.clouddn.com/123.png" class="nofancybox" width="100%" height="95%"></a>
			</div>
			<figcaption>猫咖</figcaption>
		</figure>
		<figure class="thumb">
			<div class="myalbums-box">
				<a hrefs="./sanxia/"><img src="http://pnxkcdttf.bkt.clouddn.com/123.png" class="nofancybox" width="100%" height="95%"></a>
			</div>
			<figcaption>三峡</figcaption>
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