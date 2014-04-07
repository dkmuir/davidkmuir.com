---
published: true
layout: post
title: "composer dump-autoload --optimize"
date: 2014-04-07 
categories: composer php autoload
---

Just came across the [composer.json cheatsheet](http://composer.json.jolicode.com/).

One thing that I noticed was the line:
	php composer.phar dump-autoload --optimize

> Use --optimize to convert PSR-0 autoloading to classmap to get a faster autoloader. This is strongly recommended for production (you can get a 20% boost), but can take a bit of time to run so it is currently not done by default.

From my [reading](http://mwop.net/blog/245-Autoloading-Benchmarks.html) the performance improvement is biggest when using an opcode cache like [APC](http://www.php.net/manual/en/book.apc.php) or [OPCache](http://www.php.net/manual/en/book.opcache.php). I'm in the process of setting up a new server that will be using OPCache, so it'll be interesting to see the difference in performance once it is ready to go. One for a follow-up post.
