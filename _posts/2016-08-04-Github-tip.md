---
layout: post
title: "Centered Image on Github with Jekyll"
date: 2016-08-04
---

Probably I am not a great blogger, for sure I am not an expert of website visualization.
To write my first blog I struggled to include images the way I wanted. Markdown language is quite minimal, and sometimes it is difficult to stretch it to have the desired results.


I want to share the little I learned in the previous post.

Markdown language inside Github is often updated, so what I write is valid as I write it (August 2016) for the basic github/jekyll template created by [barryclark](https://github.com/barryclark/jekyll-now) of which this blog is a fork.

If you want to include an image according to Github flavoured MD the code syntax is the following:

```![keyword](url)
```


This includes a un-resized left-aligned image in the text.

If you want a resized centered image, it is more complicated. For what I learned you should consider plug-ins, local Jekyll recompilation, or CSS/HTML codes.

I wanted to find the simpliest possible solution that could be directly used on Github. 

Accordingly to my experience the following codes did **not** work to obtain a centered 250px pic:

*  ```![keyword](url =250x)```
*  ```![keyword](url | height=250)```
*  ```![keyword](url){: .center-image }```
*  ```<img src="url" width="250">```
*  ```<img align="middle" src="url" width="250">```


They might work on the wiki, or they might have worked in past versions of Github, or if used in the proper way by an user more expert than myself. But for my experience they all failed.


I solve the problem with a dirty workaround:

*  ```<center><img src="url" width="250"></center>```




If you have a cleaner, more elegant solution that works on Jekyll on Github without using plugins, or compiling the website locally, please let me know!

Here all the examples with some different parameters.


```
This is spongebob:

![spongebob](https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png =25x)

This was spongebob.
```


This is spongebob:

![spongebob](https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png =25x)

This was spongebob. 

```
This is spongebob:

![spongebob](https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png =25)

This was spongebob.
``` 

This is spongebob:

![spongebob](https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png =25)

This was spongebob.

```
This is spongebob:

![spongebob](https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png | height=25 )

This was spongebob.
```

This is spongebob:

![spongebob](https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png | height=25 )

This was spongebob. 

```
This is spongebob:

![keyword](https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png){: .center-image }

This was spongebob.
```

This is spongebob:

![keyword](https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png){: .center-image }

This was spongebob. 

```
This is spongebob:

<img  align="middle" src="https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png" width="25">

This was spongebob. 
```

This is spongebob:

<img  align="middle" src="https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png" width="25">

This was spongebob. 



```
This is spongebob:

<img  align="middle" src="https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png" width=25>

This was spongebob.
```


This is spongebob:

<img  align="middle" src="https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png" width=25>

This was spongebob.

Finally the working example that resizes and centers the image is:

```
This is spongebob:

<center><img src="https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png" width="25" ></center>

This was spongebob. 
```
This is spongebob:

<center><img src="https://upload.wikimedia.org/wikipedia/en/5/5c/Spongebob-squarepants.png" width="25" ></center>

This was spongebob. 


