---
title: Webservers That Serve You
description: Webservers That Serve You
date: 2014-04-23
tags: Code
layout: layouts/post.njk
---

I feel like I had been living under a rock for all my web development years. Did you know that the default Python installation comes built in with a Http server?!

Before I get hit by a bus, I want to share this with you :
{% highlight python %}
python -m SimpleHTTPServer
{% endhighlight %}

Run this anywhere on the command line( ofcourse, make sure Python is installed and is part of the PATH variable)
And that's it, you are good to go my friend. Launch a browser window and navigate to localhost:8000/

Cheers to being able to quickly test dynamic HTML/JavaScript changes in the browser without the need for setting up 
Tomcat, which by the way is a giant pain in the rear to maintain, when compared to this gem.

You can accomplish something similar with node, if you are looking for a really simple webserver.

Assuming you have node installed, start by creating a file called nodeserver.js and copy the contents below into it.

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

Save the file and run 

{% highlight javascript %}
node nodeserver.js
{% endhighlight %}

And just like that, you have your own little test webserver by navigating to localhost:8124/ . Create a file called index.html in the same folder and go nuts with linking other HTML/JavaScript files in 	there.
I love the simplicity of node in creating this webserver because almost everything you would usually configure in a webserver is right here in front of your eyes. Having said that, this is obviously an abstraction and there is a ton of other things going on in the 'createServer' statement which I don't get, but that is a topic for another day.

Also, if node has piqued your interest, I highly recommend checking out <a href ="https://github.com/remy/nodemon">nodemon</a> , which basically looks at all your files under the directory and restarts the server on file changes automatically, so you don't have to go back to the browser and press ALT+R like you are having a seizure.

Let me know if you have any questions and I will respond as quickly as I can because you are probably my only reader for this blog and I would hate to keep you waiting!

---

