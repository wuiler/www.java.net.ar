---
title: Home
media_order: 'Wallpaper-Java-Camino.png,Wallpaper-Java-Duke-01.png'
hide_git_sync_repo_link: true
body_classes: 'header-dark header-transparent'
child_type: item
hero_classes: 'text-light title-h1h2 overlay-dark-gradient hero-large parallax'
hero_image: Wallpaper-Java-Duke-01.png
blog_url: /home
show_sidebar: true
show_breadcrumbs: true
show_pagination: true
content:
    items:
        - '@self.children'
    limit: 6
    order:
        by: date
        dir: desc
    pagination: true
    url_taxonomy_filters: true
bricklayer_layout: true
display_post_summary:
    enabled: false
post_icon: newspaper-o
feed:
    limit: 10
    description: 'Sample Blog Description'
sitemap:
    changefreq: monthly
modular_content:
    items: '@self.modular'
    order:
        by: folder
        dir: dsc
pagination: true
---

# For you **Java** 25 years
## Write once, run anywhere
