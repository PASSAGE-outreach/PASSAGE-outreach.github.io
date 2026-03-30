#---
#layout: page
#title: Photo Gallery
#subtitle: Get to know us!
#---

#Enjoy some photo gallieries from our various events!

---
layout: gallery
title: A Very Basic Example
no_menu_item: true # required only for this example website because of menu construction
support: [jquery, gallery]
---

Enjoy some photo gallieries from our various events!

{% include gallery-layout.html gallery=site.data.galleries.san-francisco %}

[license]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[repo]: https://github.com/opieters/jekyll-gallery-example
