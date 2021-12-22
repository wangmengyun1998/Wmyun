---
layout: defaults/page
permalink: index.html
narrow: true
<!-- title: <font color=BlueViolet face="华文行楷" size=7>解忧★ㄣ客栈</font> -->
title: chi Ki Chi Ki Chi 
---
<!-- <meta name="referrer" content="no-referrer" />
![][img6]
![][img5]
![][img4]

![][img3]
![][img2]
![][img1]

![][img9]
![][img8]
![][img7]

[img1]: https://c-ssl.duitang.com/uploads/item/202004/10/20200410101433_eTTNZ.thumb.300_300_c.jpeg
[img2]: https://c-ssl.duitang.com/uploads/item/202004/10/20200410101434_iWadw.thumb.300_300_c.jpeg
[img3]: https://c-ssl.duitang.com/uploads/item/202004/10/20200410101434_Z3JVy.thumb.300_300_c.jpeg
[img4]: https://c-ssl.duitang.com/uploads/item/202004/10/20200410101435_NiLkv.thumb.300_300_c.jpeg
[img5]: https://c-ssl.duitang.com/uploads/item/202004/10/20200410101437_CxzYm.thumb.300_300_c.jpeg
[img6]: https://c-ssl.duitang.com/uploads/item/202004/10/20200410101437_wdizF.thumb.300_300_c.jpeg
[img7]: https://c-ssl.duitang.com/uploads/item/202004/10/20200410101438_J8vff.thumb.300_300_c.jpeg
[img8]: https://c-ssl.duitang.com/uploads/item/202004/10/20200410101439_cVcLx.thumb.300_300_c.jpeg
[img9]: https://c-ssl.duitang.com/uploads/item/202004/10/20200410101439_yhUv3.thumb.300_300_c.jpeg -->

<style>
img {
	width: 150px !important;
	height: 150px !important;
	border: 1px solid #EEE;
}
</style>



### Recent Posts

{% for post in site.posts limit:3 %}
{% include components/post-card.html %}
{% endfor %}


