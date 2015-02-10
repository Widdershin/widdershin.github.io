---
layout: post
title: "Controlling Sonic Pi from vim (or anywhere else)"
date: 2015-02-10 23:13:08 +1300
comments: true
categories: programming
---

Last week I discovered Sonic Pi. I watched [Repl Electric](http://vimeo.com/117516352) perform live at RubyConf AU. He gave a brief demo of Sonic Pi, a tool for progamming live music with Ruby. Instantly my eyes lit up. It was the instrument I'd always wanted.

I tried it out the next day. It has a nice interface, but I'm used to vim and living in the terminal. I googled "vim sonic pi", but there was nothing I could see. I hunted round for a bit, but I couldn't find a command line interface either.

It was [Sam Aaron](http://github.com/samaaron)  (the creator of Sonic Pi) who pointed me in the right direction, a blog post entitled [Connecting Erlang to Sonic Pi](https://joearms.github.io/2015/01/05/Connecting-Erlang-to-Sonic-Pi.html). It turned out that there was an undocumented method of controlling Sonic Pi externally.

The secret:
```ruby
require 'osc-ruby'
code = 'play 50' # or whatever you want
OSC::Client.new('localhost', 4557).send('/run-code', code)
```

That code sends an OSC message ([Open Sound Control](http://osw.sourceforge.net/html/osc.htm)) to Sonic Pi, instructing it to run the given code just as if you had typed it in.

So I put together a simple command line interface to use Sonic Pi from the terminal. [sonic-pi-cli](https://github.com/Widdershin/sonic-pi-cli). I packaged it up as a gem, and released it into the wild.

You can install it with `gem install sonic-pi-cli` and then run music with `sonic_pi play 60` or `echo 'sample :loop_amen' | sonic_pi`.

I was really happy to have a working CLI for Sonic Pi. I quickly whipped up some vim binds so I could use Sonic Pi right from my editor.

```vim
noremap <leader>r :silent w !sonic_pi<CR>
noremap <leader>S :call system("sonic_pi stop")<CR>
```

You can add these commands to your `.vimrc`, and voila, Sonic Pi in your vim. I use the spacebar as my leader key, so these shortcuts feel a lot like using Sonic Pi.

Now, the really amazing part comes. Less than a day since I first released [sonic-pi-cli](https://github.com/Widdershin/sonic-pi-cli) on [RubyGems](https://rubygems.org/gems/sonic-pi-cli), a few awesome projects have already put it to use.

[Robin Newman](http://github.com/rbnpi) has used it to control Sonic Pi from his phone with a Raspberry Pi and telegram.

<iframe width="560" height="315" src="https://www.youtube.com/embed/9o-DY8qrm44" frameborder="0" allowfullscreen></iframe>

[dermusikman](https://github.com/dermusikman) immediately started working on a vim plugin to bring as many features of Sonic Pi to vim as he can, [sonicpi.vim](https://github.com/dermusikman/sonicpi.vim).

At the moment, it contains the shortcuts from above, as well as auto completion for samples and the like, and the use of the .pi file format, with Ruby highlighting.

I'm absolutely astounded by the awesome work that has been put out so rapidly by others in the community. I really love this aspect of open source. There's a good sense of collaboration through Github issues and [gitter](https://gitter.im/samaaron/sonic-pi).

I'm looking forward to contributing more to the Sonic Pi community in future.
