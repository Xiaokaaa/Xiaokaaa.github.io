小咖的个人主页：[https://xiaokaaa.github.io](https://xiaokaaa.github.io)


#### 2024.3.1：建一个旅游博客栏过程
- 在 `_data/navigation.yml` 设置设置一个网站的导航菜单；

- 建一个`trips.html`文件设置 归档及格式

```html
---
layout: archive
permalink: /trips/
title: "旅行"
author_profile: true
redirect_from:
  - /wordpress/blog-posts/
---

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.posts %}
  {% if post.title contains 'trip' or post.url contains 'trip' %}
    {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
    {% if year != written_year %}
      <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
      {% capture written_year %}{{ year }}{% endcapture %}
    {% endif %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
```

- 文件位置: 确保文件是放在正确的文件夹中。你提到的_trips文件夹不是Jekyll的默认文件夹。Jekyll默认从_posts文件夹获取帖子。如果你使用自定义的集合比如_trips，你需要在_config.yml文件中配置它。比如：
```yaml
collections:
  trips:
    output: true
    permalink: /trips/:path/
```