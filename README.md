# [CKEditor](http://ckeditor.com/) with [oembed](https://github.com/starfishmod/jquery-oembed-all) (media) plugin.

Originally forked from https://github.com/tsechingho/ckeditor-rails
Media (oembed) plugin for CKEditor https://github.com/starfishmod/jquery-oembed-all for embedding videos.

### Currently Supported Sites by oembed plugin:
  
  * Video

    + Youtube - oembed - YQL
    + Blip - oEmbed
    + Hulu - oEmbed
    + Vimeo - oEmbed
    + National film board of Canada - oEmbed
    + Qik - oEmbed
    + Dotsub - oEmbed
    + Clikthrough - oEmbed
    + Kino Map - oEmbed
    + Funny Or Die - Embedded
    + College Humour - Embedded
    + Metacafe - Embedded
    + embedr - Embedded
    + 5min - oEmbed is XML only - using YQL to translate it
    + ustream.tv - oEmbed is not JSONP enabled - using YQL to translate it
    + viddler - OGP
    + twitvid - Embedded
    + bambuser - Embedded
    + xtranormal - Embedded
    + Gametrailers - Embedded
    + Vzarr - Embedded
    + VHX - oembed
    + bambuser - oembed
    + dailymotion.com - oembed
    + animoto - oembed
    + justin.tv - YQL JSON
    + livestream - OGP
    + scivee - embedded
    + veoh - embedded
    + minoto-video - oembed using YQL
    + TrailerAddict - OGP
    + vodpod - oembed YQL - broken as the oembed has absolute positioning which breaks the display
    + fora.tv -OGP YQL
    + TED - OGP YQL
    + Aniboom - embedded
    + Comedy Central - OGP
    + snotr - embedded
    + zapiks - OGP
    + youku - embedded
    + wistia - Oembed


 

  * Audio

    + Soundcloud - oEmbed
    + HuffDuffer - oEmbed
    + BandCamp - YQL and Embedded
    + podomatic - OGP
    + rdio.com - oEmbed
    + hark.com - OGP
    + chirb.it - YQL and oembed
    + official.fm - YQL and oembed
    + mixcloud - YQL and oembed
    + shoudio - oembed
    + audioboo.fm - OGP
    + Spotify - OGP YQL

  * Photo

    + flickr - oEmbed
    + photobucket - oEmbed
    + instagram - oEmbed
    + yfrog - oEmbed
    + 23HQ - oEmbed
    + Smugmug - oEmbed
    + twitpic - OGP YQL
    + 500px.com - OGP
    + visual.ly - YQL Lookup
    + img.ly - Thumbnail view
    + imgur.com - Thumbnail view
    + twitgoo.com - Thumbnail view
    + gravatar - Thumbnail view when using mailto
    + pintrest - YQL - Embedded view of a sort.
    + circuitlab - image view
    + skitch - YQL oembed
    + graphic.ly - OGP
    + dribble - jsonp lookup
    + Lockerz - YQL lookup
    + AsciiArtFarts - YQL Lookup
    + lego cusoo - OGP over YQL
    + plannary - OGP over YQL
    + propic - OGP
    + avairy.com - OGP
    + lomography - ogp
    + weheartit - ogp
    + glogster - ogp
    + chart.ly - embedded
    + twitrpix - OGP
    + chictopia - OGP

  * Rich

    + Meetup - oEmbed
    + gigapans - Embedded
    + Slideshare - oEmbed
    + ebay - Embedded
    + scribd - Embedded
    + screenr - Embedded
    + tumblr- JSONP lookup
    + imdb - JSONP lookup via imdbapi.com
    + wikipedia- JSONP lookup
    + github- JSONP lookup (CSS)
    + eventful - OGP
    + myspace - OGP
    + live Journal - JSONP Lookup (CSS)
    + wordpress - oEmbed (wordpress.com, wp.me, blogs.cnn.com, techcrunch.com). I can add other wordpress sites as well.
    + circuitbee -Embedded
    + stack overflow - JSONP Lookup (CSS)
    + Facebook - JSONP Lookup (CSS)
    + Pastebin - Embedded
    + Pastie - YQL lookup
    + kickstarter - Embedded
    + issuu - OGP
    + reelapp.com - Embedded
    + Etsy - OGP over YQL
    + Amazon - Embedded - Requires Affiliate code
    + linkedin - Embedded IFRAME - found a link that works :)
    + Lanyrd - YQL (CSS)
    + twitter - Oembed - status only - but that is ok I think
    + github gist - oembed
    + speakerdeck - yql oembed
    + dipity - yql oembed
    + dailymile - oembed
    + deviantart - oembed
    + Roomshare Japan - oembed
    + mobypictures - oembed
    + prezi - embedded
    + popplet - embedded
    + authorstream - OGP
    + googlecalendar - Iframe
    + cacoo - oembed
    + pearltrees - embedded
    + urtak - oembed - is broken in iframe return atm -seems to be an embed.ly issue??
    + jotform - embedded
    + Urban Dictionary - YQL lookup
    + Ars Technica - YQL Lookup
    + Eventbrite - OGP YQL
    + last.fm OGP YQL
    + Rotten Tomatoes - OGP YQL
    + iFixit - OGP
    + qwiki - OGP
    + brighttalk - Meta info
    + tinychat - OGP
    + tourwrist - embedded
    + bnter - OGP
    + bigthink - OGP
    + wirewax - OGP
    + whosay - OGP
    + timetoast - embedded
    + tripline - OGP
    + jsfiddle - embedded


# CKEditor for rails asset pipeline

[CKEditor](http://ckeditor.com/) is a library for WYSIWYG editor to be used inside web pages.

The `ckeditor_rails` gem integrates the `CKEditor` with the Rails asset pipeline.

And it would work with following environments:

* ruby 1.9.3+
* rails 3.0+

## Basic Usage

### Install ckeditor_rails gem

Include `ckeditor_rails` in Gemefile

    gem 'ckeditor_rails'

Then run `bundle install`

### Include CKEditor javascript assets

Add to your `app/assets/javascripts/application.js` after `//= require jquery_ujs` to work with jQuery

    //= require ckeditor-jquery

### Modify form field for CKEditor

Add `ckeditor` class to text area tag

    <%= f.text_area :content, :class => 'ckeditor' %>


### Initialize CKEditor in Javascript file

    $('.ckeditor').ckeditor({
      // optional config
    });

### Deployment

Since version 4.1.3, non-digested assets of `ckeditor-rails` will simply be copied after digested assets were compiled.

Eric Anderson, thanks.

## Advanced Usage

### Include customized configuration javascript for CKEditor

Add your `app/assets/javascripts/ckeditor/config.js.coffee` like

    CKEDITOR.editorConfig = (config) ->
      config.language = "zh"
      config.uiColor = "#AADC6E"
      true

### Include customized CKEDITOR_BASEPATH setting

Add your `app/assets/javascripts/ckeditor/basepath.js.erb` like

    <%
      base_path = ''
      if ENV['PROJECT'] =~ /editor/i
        base_path << "/#{Rails.root.basename.to_s}/"
      end
      base_path << Rails.application.config.assets.prefix
      base_path << '/ckeditor/'
    %>
    var CKEDITOR_BASEPATH = '<%= base_path %>';

### Include customized stylesheet for contents of CKEditor

Add your `app/assets/stylesheets/ckeditor/contents.css.scss` like

    body {
      font-size: 14px;
      color: gray;
      background-color: yellow;
    }
    ol,ul,dl {
      *margin-right:0px;
      padding:4 20px;
    }

## Gem maintenance

Maintain `ckeditor_rails` gem with `Rake` commands.

Update origin CKEditor source files.

    rake update_ckeditor VERSION=4.2

Publish gem.

    rake release

## Troubleshooting

#### CKEditor only loading after page refresh

This is due to interference with Turbolinks -

The problem stems from the link itself so in order to resolve this issue you must disable turbolinks in the div containing the link pointing to where CKEditor is.

You can visit the Rails Turbolinks Repo for detailed documentation
https://github.com/rails/turbolinks/#opting-out-of-turbolinks

**Example**

    <div class="example" data-no-turbolink>
    ...
    </div>

## License

CKEditor use [CKEditor license](http://ckeditor.com/license).

Other parts of gem use MIT license.
