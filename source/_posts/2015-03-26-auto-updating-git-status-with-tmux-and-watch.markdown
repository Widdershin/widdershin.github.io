---
layout: post
title: "Auto updating git status with tmux and watch"
date: 2015-03-26 22:37:10 +1300
comments: true
categories: programming tmux
---
<iframe class="center" src="http://gfycat.com/ifr/HideousPoliteCivet" frameborder="0" scrolling="no" width="562" height="472" style="-webkit-backface-visibility: hidden;-webkit-transform: scale(1);" ></iframe>

One of the great things about tmux is that you can create flexible development layouts.


You can easily display the output of a command and auto update it using `watch`. It has a similar end user experience as `tail -f`, except for commands instead of files. For example:

`$ watch git status`

`watch` will run `git status` every 2 seconds and display the output.

If you want color in your `git status`, you'll need to configure git to display color when being run by `watch`.

`$ git config --global color.status always`
`$ watch --color git status`
