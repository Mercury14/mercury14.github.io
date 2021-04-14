---
layout: default
title: Books I am reading
description: Review of books.
featured_image: '/images/home/books.jpg'
---
<section class="hero">

	<div class="hero__image" style="background-image: url({{ page.featured_image | relative_url }})">
		<div class="hero__overlay"></div>
	</div>

	<div class="wrap">

		<h1>My books</h1>
		<p>What I am reading.</p>
	</div>

</section>
<section class="listing">



  <div class="wrap">

		{% for books in site.books reversed %}

		<article class="post">

			<div class="post__image-wrap">
				<div class="post__image" style="background-image: url({{ books.featured_image | relative_url }})"></div>
			</div>

			<div class="post__content-wrap">
				<div class="post__content">
					<h2 class="post__title"><a href="{{ books.url | relative_url }}">{{ books.title }}</a></h2>
					<p class="post__subtitle">{{ books.subtitle }}</p>
					<p class="post__description">{{ books.description }}</p>
				</div>
			</div>

		</article>

		{% endfor %}

	</div>

</section>