+++
date = '2024-11-10T20:22:38-05:00'
draft = true
title = 'Back to Hugo'
+++
Some years ago I was bit by the [Rust bug](https://rust-lang.org), and I decided to rebuild my sites using [Zola](https://www.getzola.org/), a Jekyll-like static site generator. The software does all of the essentials, but I ran into some issues deploying sites built with it. While I was often able to work around those issues, I've since grown tired of its idiosyncrasies.

Back then I was also not particularly a fan of [Go](https://go.dev), but that has changed thanks to awesome tools like [ESBuild](https://esbuild.github.io/).

[Hugo](https://gohugo.io/) was the static site generate I used on my original blog [TooNormal](https://toonormal.com). Rather, it was the static site generator I used after a brief stint with Jekyll, and a decade running WordPress.

My time with Zola was not wasted, as it helped me understand how to build complex websites using static site generators, notably the information website [ludumdare.com](https://ludumdare.com). One of the bigger hiccup I ran into was I that I wanted to generate an `.ics` calender from my data, but unfortunately generating `.ics` was not supported (specifically you can't generate arbitrary file formats). That said, it sounds like folks have had luck doing this with Hugo:

<https://discourse.gohugo.io/t/calendar-ics-template/7137>

I could have worked-on Zola patch, but frankly I should just switch to a software with more support. I've legit avoided blogging due to my frustration with Zola! I'm afraid that's not going to cut it, not anymore. 

Soooo we're going back Hugo!

My first task: rebuild my resume using Hugo. I've been annoyed by the ancient LibreOffice document I used to edit. Since I'm looking for work again, this made sense.
