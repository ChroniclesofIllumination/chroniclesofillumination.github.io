---
author: Mythreyi
date: 2018-03-31 15:35:11+00:00
excerpt: A quick summary of how I switched to Jekyll from my WordPress.com site.
layout: post
slug: switching-to-jekyll
title: Switching to Jekyll
tags: tools jekyll update
---

This has been in the back of my mind for a long while now. I've had my fill of [WordPress](https://www.wordpress.com). There's nothing wrong with WP, I would just prefer more control over my blog. I got triggered into getting this done by Andrej Karpathy's post on [Switching to Jekyll](http://karpathy.github.io/2014/07/01/switching-to-jekyll/). Ironically, he has moved to [Medium.com](https://medium.com), but he has his reasons for that. As Tom Preston-Werner, the creater of Jekyll, said in his post [Blogging like a Hacker](http://tom.preston-werner.com/2008/11/17/blogging-like-a-hacker.html) :

> "I feel a lightness now when I’m writing a post. The system is simple enough that I can keep the entire conversion process in my head. The distance from my brain to my blog has shrunk, and, in the end, I think that will make me a better author."

### How to switch?

1. One needs time. Since this is the first time I've actually tried this, it took me a while to get used to it. To put in numbers, I'd say, to an average person (with some prior experience with Web Development), a switch from WordPress to Jekyll would take about **3 hours**. Most of this time will go into figuring things out, if you're fast at this, the time taken should drastically come down.

2. Follow other people's guides. Here are some I particularly found useful

   1.  [Jekyll Official Documentation](https://jekyllrb.com/docs/home/)

   2. Programming Historian's Tutorial on [Building a Statis Website with Jekyll and GitHub Pages](https://programminghistorian.org/lessons/building-static-sites-with-jekyll-github-pages)

   3. WordPress.com to Jekyll migration tips at [Jekyll Migration Docs](https://import.jekyllrb.com/docs/wordpressdotcom/) and the Exitwp tool's [GitHub Repo](https://github.com/thomasf/exitwp). 

      __Note__: You will need to install some **python** dependencies for this step. They are listed clearly in the repo's readme file.

   4. Finally, for implementing "tags" in the website, Long Qian's brilliant blog post called [Jekyll Tags on GitHub Pages](http://longqian.me/2017/02/09/github-jekyll-tag/). 

      **Note**: 

      - There's a mistake in the code to be added to the `_includes/head.html` file. The condition always evaluates to false, modify it to :

        ```ruby        {% raw %}
        {% if site.tags == "" %}
          {% include collecttags.html %}
        {% endif %}        {% endraw %}
        ```

      - The _tag_generator.py_ file needs to be tweaked for it to work properly. The default export using the _Exitwp_ tool is a **.markdown** file not a **.md** file, hence the appropriate change is needed in [this](https://github.com/qian256/qian256.github.io/blob/4c1239bf085d30d81c8df2e1bb41c21f5754192e/tag_generator.py#L19) line.

        Once you generate the different _tag_ pages, they will all get added to the  **header** section of your blog (making it a collossal mess). To avoid this, you can specify the list of pages you want in your header though `header_pages: ` in the `_config.yml` file. For instance, the `_config.yml` of this website reads as:

      ```ruby
      header_pages:
        - about.md
        - undocumented-explorations.md
      ```

      Both these files exist in the root directory of my site at the moment. If this is not the case, the full path must be specified.

So there it is. That's how to switch and have a functional website up and running. There are naturally a lot of things that can be modified, starting with the looks and also additional functionalities. But I plan to take them all up later, one at a time.

This is, in a way, a _recursive_ post. The post is about the post itself.