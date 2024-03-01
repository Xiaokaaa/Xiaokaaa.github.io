小咖的个人主页：[https://xiaokaaa.github.io](https://xiaokaaa.github.io)


#### 2024.3.1：建一个旅游博客栏过程
- 在 `_data/navigation.yml` 设置设置一个网站的导航菜单；
- markdown.md文件中修改
```md
## Locations of key files/directories

* Basic config options: _config.yml
* Top navigation bar config: _data/navigation.yml
* Single pages: _pages/
* Collections of pages are .md or .html files in:
  * _publications/
  * _portfolio/
  * _posts/
  * _trips/
  * _teaching/
  * _talks/
* Footer: _includes/footer.html
* Static files (like PDFs): /files/
* Profile image (can set in _config.yml): images/profile.png
```

- 文件位置: 确保文件是放在正确的文件夹中。你提到的_trips文件夹不是Jekyll的默认文件夹。Jekyll默认从_posts文件夹获取帖子。如果你使用自定义的集合比如_trips，你需要在_config.yml文件中配置它。比如：
```yaml
collections:
  trips:
    output: true
    permalink: /:collection/:name/
```