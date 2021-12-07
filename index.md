---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: home
title: Portfolio
---

<div class="gallery-container">
	{% for project in site.projects %}
	<div class="article-container">
		<article class="portfolio-single post entry">
			<a class="entry-image-link" href="{{ project.url }}" aria-hidden="true">
				<img width="220" height="160" src="assets/img/{{ project.thumbnail }}" class="attachment-portfolio-thumb size-portfolio-thumb wp-post-image" alt="" loading="lazy">
			</a>
			<div class="mask">
			  <div class="entry-title desc">
			  	<a href="{{ project.url }}" class="entry-title-link" rel="bookmark" title="US Corr">{{ project.title }}</a>
			  </div>
			  <span class="project-category">
			  	<a rel="category-tag"></a></span>
			  	<span class="center-text">
			  		<a href="{{ project.url }}" class="view-project">{{ project.tag }}</a>
		  	</span>
			</div>
		</article>
	</div>
	{% endfor %}
</div>
