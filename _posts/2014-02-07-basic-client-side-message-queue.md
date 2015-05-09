---
layout:     post
title:      "A Basic Client-Side Message Queue"
subtitle:   "Odd little thingy you might like"
date:       2014-02-07 12:00:00
author:     "John Kleijn"
header-img: "img/post-bg-02.jpg"
---

Recently I had to create a solution where an AngularJS app had to
communicate with another window that displayed a Sigma.js graph,
animating movement through the graph in response to using the UI of the
AngularJS app.

So I implemented a very basic client-side message queue. It’s no AMQP,
but I think it’s still pretty cool, so I though I’d share anyway.

I chose “localStorage” for communication, but to be fair for a basic
message queue you could use cookies as well (unless your messages are
 huge). Which would even have the advantage of working across browser
types (eg a Safari instance talking to a Chrome instance), but of course
is less “shiny ” (oooh) and I didn’t need that advantage anyway. And of
course cookies are not intended for this purpose, being sent to the
server on refresh and whatnot, so long story short: localStorage seemed
more suitable beyond being more shiny.

It is actually pretty basic. LocalStorage doesn’t support complex types
so you have to JSON encode and decode every time you want to send or
check for new messages, but that’s native and not an issue as long as
your poll / consume interval is reasonable. Add some queue semantics,
share the code between windows, use the same namespace, e voilà, a
message queue of sorts.

CoffeeScript service:
<script src="http://gist.github.com/d624096c90c1d3e4b3e9.js">

Thanks for reading.

