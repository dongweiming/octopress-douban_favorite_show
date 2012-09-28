octopress-douban_favorite_show
==============================

Display douban favorite on the awesome blog system Octopress show

## Octopress Plugin For DOUBAN

This is a plugin of [Octopress](http://octopress.org/) (the most awesome blog system), which can display your personal douban status at the sidebar.

### Installation

At first
```bash
git clone git://github.com/dongweiming/octopress-douban_favorite_show.git
cd octopress-douban_favorite_show
cp douban.html /your-blog-root-path/source/_includes/custom/asides/
```

Then edit your ```_config.yml```

1. add `custom/asides/douban.html` to your default_asides array. 
like this: 
default_asides: [asides/recent_posts.html,  asides/github.html, asides/delicious.html, asides/pinboard.html, custom/asides/category_cloud.html, custom/asides/douban.html]
2. add the following configurations to the end or where you like.

```yaml
#Douban
douban_user: 62943420 #The Doban Id ,Leave it blank to display this plugin
douban_people: #Your Douban Name 
douban_apikey: 0ec15d10bdd1901a2c4417323974b04e #YOu can leave it blank
douban_show:  #The type of display ,include: dolist(doing),wishlist(want to),collection(seen), Leave it blank to random
douban_display_category: book|music #The type of display ,include:book music blog movie, format: xx|yy|zz (for example movie|book|music), Leave it blank to All
douban_display: random #What for display, Other options: favorite(good),Leave it blank to display last added
douban_total_show: 10 #How many to display
douban_percolumn: 2 #How many per column 
douban_img_style: medium #The size of the content pictures, Leave it blank to small
douban_hidelogo: true #Leave it blank to false
douban_hideself:  true #Leave it blank to false

```

At last
```
rake generate
rake deploy #if you want deploy it 
```  


