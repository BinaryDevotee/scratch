---
title: "NBDE (Network-Bound Disk Encryption) on Gentoo"
date: 2024-10-27T13:30:00-04:00
categories:
  - blog
tags:
  - Gentoo
  - network
---

One of the hassles of having full-disk encryption (FDE) is not being able to unlock your encrypted block device without being physically present as you need to type your password during boot. This can be a problem if you are managing your hosts remotely (for example via a VPN connection) where entering your password is just not possible.

Even though there are ways around that, like deploying a lightweight SSH server (such as [Dropbear][dropbear]) in your inital RAM disk so you can login and authenticate to your system on a pre-boot stage and then issuing the commands do unlock your encrypted device, this process is not fully automated and does not leverage 

You'll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.


```bash
ls -l ./my_dir
```
Check out the [Project GURU][project-guru] for more information. Also, Red Hat has an extended article that covers Network-Bound Disk Encryption from all angles and should definitely give you a better overview of what can be achieved with the Clevis+Tang combination.

[project-guru]: https://wiki.gentoo.org/wiki/Project:GURU/Information_for_End_Users
[redhat-nbde]: https://access.redhat.com/articles/6987053
[dropbear]: https://github.com/mkj/dropbear