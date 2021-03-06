### Install

Gemfile
```
gem 'dxf_tiip_view', :git => 'https://github.com/shinobushiva/dxf-tiip-view-rails'
```

```
$ bundle install
```

routes.rb

```
#DXF Tiip View
mount DxfTiipView::Engine, at: '/dxf_tiip_view'
```

### Font file
You need typeface.js style font file.

You can use the font file as a sample
fonts/honoka_antique_kaku_regular.json

To generate font file, this website will help
***typeface.js generator***
https://gero3.github.io/facetype.js/

To use Japanese font, see here
https://qiita.com/calmbooks/items/4fe8b891950f5a227290

Place font file in your publicly accessible path.
ex) /public/font

### Usage

View (in erb)
```
<%= dxf_tiip('a[href*=".dxf"]', '/font/honoka_antique_kaku_regular.json')  %>
```

View (in haml style)
```
= dxf_tiip 'a[href*=".dxf"]', '/font/honoka_antique_kaku_regular.json'
```
