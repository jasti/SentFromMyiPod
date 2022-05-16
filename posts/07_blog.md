---
title: Build Your Own Blog
description: Build Your Own Blog
date: 2014-05-08
tags: Code
layout: layouts/post.njk
---

Writing here has gotten me thinking more deeply about things I come across everyday. Talking comes naturally to me and I can spend days having conversations with friends with no real agenda, but I am not as good at writing concrete material and I wanted to work towards changing that. Thinking while speaking with someone usually gets me to a level or two, but writing down forces me to solidify my reflection on a thought. 

It's gotten me to re-read what I create multiple number of times, which is a great patience builder. Plus it's always a good feeling to hear back from that one angel of a reader who emails you to tell you how she found your technical article helpful.

Blog sites like Medium and Tumblr have come a long way with <a href ="http://en.wikipedia.org/wiki/WYSIWYG">WYSIWYG</a> but they all claim to do whatever they want with your content, including monetize. Not to say that I won't write for free, I will, but at my terms.

Excerpt from <a href ="https://medium.com/p/9db0094a1e0f">Medium's terms of service</a> 
<blockquote>
By posting or transferring content to Medium, you give us permission to use your content solely to do the things we need to do to provide Medium Services, including, without limitation, storing, displaying, reproducing, and distributing your content. This may include promoting your content with partner companies or services for broader broadcast, distribution, or publication.
</blockquote>
<br>
 
There are some other obvious reasons to avoid blogging sites. If they <a href ="http://en.wikipedia.org/wiki/Posterous#Shutting_down_Posterous_and_building_PostHaven">shut down</a> they take all your permalinks with them. Switching costs of blog sites are quite high because they make it deliberately hard to export content. Most of them need quite a bit of tweaking to display selectable code snippets or things like quotes.

I started using <a href ="http://www.sublimetext.com/">Sublime Text</a> for programming about a year ago and it has been a total game-changer. If you are a programmer, you'll feel right at home, like you are typing on the command line. Especially if you use the <a href = "https://github.com/buymeasoda/soda-theme/">Soda-theme</a>. I like the ability to do most of the things I want to from the command line or Sublime without having to deal with clunky pixelated user interfaces. The ability to write a blog like we build software - iteratively, with source control and experimentation was a huge requirement.

When I decided to write, I started to research and the obvious pick was to use a <a href ="http://staticsitegenerators.net/" >Static Site Generator</a> and since I was building a rails site for a friend's startup, I decided to go with <a href ="http://jekyllrb.com/">Jekyll </a>. After hacking on it for a couple of weekends, I finally have something that I am quite happy with.
Ultimately, the ability to experiment, learn and see your new features come to fruition instantly, feels quite rewarding. 

<img src="/images/blog/sublime.png"/>


<h2>Jekyll</h2>
I started with Zach Holman's <a href ="https://github.com/holman/left">left theme</a> to work off of a seasoned Jekyll theme. There is no point re-inventing the wheel for this. Yoda once said (or did he?) "If you don't know your destination, it's best to walk sideways or backwards than walking forward." I ended tweaking it to my liking and the biggest change you might notice is in the way the site is laid out and how it looks on mobile.
Using Jekyll's lightly document 'watch' commmand, you can make edits in your editor and have jekyll reload:

{% highlight python %}
# '-watch' instead of '-w' woudn't autogenerate files for some reason
jekyll serve -w
{% endhighlight %}


<h2>GitHub Pages</h2>
Hosting a site of your own has never been easier. All you need is a Github account and a <a href ="https://github.com/jasti/jasti.github.io"> repository</a> to publish your static site. It becomes easier if you plan to use Jekyll because Github will do the site generation bit for you directly serve up the generated HTML and JS.
By default, the site is available, in my case, at jasti.github.com which gets forwarded from <a href ="http://vamseejasti.com">vamseejasti.com</a>. To make this happen, it just takes one line in the  <a href ="http://en.wikipedia.org/wiki/CNAME_record">CNAME</a> file that goes with your static site and Github will replace *.github.io with your custom domain name.
If you plan to use a domain manager to buy a site, I recommend <a href ="https://iwantmyname.com/">iwantmyname.com</a> and has a one click DNS forwarding with Github. 

<h2>Design</h2>
Icons are built with <a href ="http://fortawesome.github.io/Font-Awesome/">Font Awesome</a>. The icons are all vector graphics, which look good on any screen resolution and a lot of the compatibility issues are handled for you.
I use the <a href ="https://www.google.com/fonts/specimen/Oxygen">Oxygen</a> font for all the content and <a href ="http://www.google.com/fonts/specimen/Lobster">Lobster</a> for a header from Google fonts.

This is probably just me but I feel anxious when there are a ton of links on a page I want to read. It feels like an unattended to-do list that can be checked off by clicking on the links. Naturally I want to avoid them as much as possible, but I also want the ability to give the user a deeper experience <i>if they choose to</i>. Played around with some CSS and ended up with all links in a bolded format which I think is less distracting instead of the default underlined blue link. 

I use <a href ="http://pygments.org/">Pygments</a> for syntax highlighting. It's simple and does the job. Example below:

{% highlight javascript %}
var http = require('http');
var fs = require('fs');

fs.readFile('index.html', function (err, html) {   // Your html test file


    if (err) {
        throw err;
    }
    http.createServer(function(request, response) {
        response.writeHeader(200, {"Content-Type": "text/html"});  \
        response.write(html); 
        response.end();
    }).listen(8124, '127.0.0.1');
});
{% endhighlight %}

<h2>Responsive</h2>
The site is responsive and renders appropriately for screens of smaller resolutions by just loading the mobile.css instead of base.css from the css folder. No magic there.
<center>
<img src="/images/blog/mobile.png"/>
</center>

<h2>Google Analytics</h2>
I am a junkie to know how often the blog is being visited and by whom. Google Analytics makes this really easy. Just sign up, link your site and insert the snippet of code in the pages you want to track and you are all set. Easy peasy.

<h2>Disqus</h2>
Today was the first time I tried out  <a href ="http://disqus.com/">Disqus</a> and it was a pleasant surprise. Sign up, generate your custom code and paste your custom code in the footer of your site. The neat thing is that you can carry your Disqus comments to another site if you like, with just a couple of line changes. 

<img src="/images/blog/disqus.png"/>

<h2>Open Source</h2>
I have stripped out my site and created an open source template of the site. So fork it, delete what you don't need and tweak it to your liking. 

You'll find the source on Github : <a href ="https://github.com/jasti/stout">Stout</a>

If you plan to use it, I'd be happy if you gave me a shout on <a href="https://twitter.com/vamseejasti" target="_blank"><i class="icon icon-twitter"></i></a>. I'd still be happy if you didn't tell me, but whatever you do, do not forget the second rule of Fight Club.

<blockquote>
I've already got the prize. The prize is the pleasure of finding the thing out, the kick in the discovery, the observation that other people use it. Those are the real things. - <a href ="https://www.youtube.com/watch?v=Bgaw9qe7DEE#t=1466">Richard Feynman</a>
</blockquote>

---
