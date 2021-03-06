---
layout: post
---

I want to share a little tip I picked up this weekend (courtesy of [Mr. Ryan Bates](http://railscasts.com/episodes/264-guard)). It's a little gem + browser plugin pair called guard-livereload and livereload. Those two little nuggets paired together allow your browser to automatically refresh the page when you save changes to a file. 

Setup:

The first step is to go download the browser extension from here (don't buy anything, the bit we want is free):

[Live reload browswer extensions](http://help.livereload.com/kb/general-use/browser-extensions)

Install that piece, and please read and follow the additional instructions if you use Chrome.

The next phase is to get livereload working with your rails app.

You will want edit your Gemfile to have this line:

{% highlight ruby %}
gem 'guard-livereload'
{% endhighlight %}

then in the terminal:

    bundle install
    guard init livereload

This will create a Guardfile in your rails dir if you don't already have one, or edit it if you do.

Then, to run guard with your new settings, in the terminal:

    guard

Note: you may have to type in

    bundle exec guard

That's it. Try it out! Not having to remember to hit refresh is not game-changing, but it makes the loop between what I code and what I see just that tiny bit smaller. So I can hold out until [this stuff is deployed](http://vimeo.com/36579366).