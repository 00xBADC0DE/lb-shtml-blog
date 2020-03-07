# shtml-blog based on lb by Luke Smith | 00xBADC0DE 

Blogs and RSS feeds in less than 100 lines of shell script, actually, right now, less than 80.  `lb` stands for lightweight blog, or "less bloat", doesn't matter that much.

## Now Mobile Friendly

This fork works great on mobile devices. A minified CSS version is also added to improve your score on PageInsights. This blog is extremely fast, even on low-budget hosts. A 100% speed score should be attainable. 

## Some notes:

1. Style.css contains the editable style of the theme and will be used on all pages. If you want to use the minified version, rename style.min.css to style.css or use something like yui-compressor in order to minify your own css. 

2. The theme/style created by Luke Smith is customized. If you want more themes, hit me up!

3. I may create a PHP based version of this blog, e.g. to automatically add all the stuff between the header tags. 

4. Some Bootstrap 4+ css code was used in the css file. All other bloat was removed for further optimization. 

5. Normalize.css was added for consistent rendering across different browsers with some elements removed. 

6. Do not clone the blog folder from github. It will be set up automatically. 

[Video Showcase from Lukes' LB](https://www.youtube.com/watch?v=S1WQlr42xDM)


## Features


`lb` is an extremely small shell script that lets you write blog posts and will format them in all the ways you could ever want. Here's what it will produce:


- A Rolling Blog Page. See [Luke's own Rolling Page](https://lukesmith.xyz/blog.html) as an example.

- A list of all blog entries with dates: [Blog List File](https://lukesmith.xyz/blogindex.html).

- All your blog posts appear as standalone entries/pages, for example [like this one](https://lukesmith.xyz/blog/the-real-bronze-age-mindset.html).

- These standalone files exist in a `blog/` directory, which you can allow to be browsed manually via your Apache web server as I have [here](http://lukesmith.xyz/blog).

- Blog posts are added, in full form, to an RSS feed of your chosing as well, see [my RSS feed](https://lukesmith.xyz/rss.xml).

- Posts in the rolling blog have divs that can easily be modified via a CSS stylesheet, and in general everything is easily editable.

- One command to delete published entries from the RSS feed, rolling blog and standalone entries simultaneously.

- Published blog entries can now be revised, updating the standalone blog pages, the RSS feed and everything else.



## Usage



`lb` commands are all one letter. They all stand for something though.



```sh

./lb n(ew)  # Make a new blog post draft.

./lb e(dit) # Edit a draft of an entry.

./lb t(rash)  # Delete a draft of an entry.

./lb p(ublish)  # Finalize/publish a blog post draft.

./lb d(elete) # Delete a published blog post.

./lb r(evise) # Revise an already published entry (you can republish it with `lb p` when done)

```



## Installation



+ bash and GNU sed is required. >inb4 bloat

+ Be sure that you own or have writing privileges in the given directory, so the script can create the required directory structure.

+ Download the `lb` script and put it in your website's main directory. The expectation is that your rolling blog file and RSS feed will be there as well. The blog folder may not be required. 

