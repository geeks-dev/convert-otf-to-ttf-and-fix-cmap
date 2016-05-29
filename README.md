# Convert OTF to TTF and fix cmap

## What is this?

If you convert OTF font like SourceHanSans to TTF using [fontforge](https://fontforge.github.io) or [Glyphs](http://glyphsapp.com), the cmap table in the converted ttf font is incorrect. The cmap table in these fonts maps some glyphs to multiple code, but the cmap in the converted ttf maps one glyph to one code.

`process-cmap.rb` fixes this.


## Prerequisites

* Ruby 1.9 or above
* ruby bundler
 * `gem install bundler`
* ttx : 
 * from [AFDKO](http://www.adobe.com/jp/devnet/opentype/afdko.html)
 * from [fonttools](https://github.com/behdad/fonttools/)
* fontforge


## How to use

```
bundle install
bundle exec ruby process-cmap.rb [original otf font]
```

Fixed font will be generated in the `cmap_modified` directory.

## Related article 

http://qiita.com/skoji/items/5683caa17eaa46b2a78d (in Japanese)
