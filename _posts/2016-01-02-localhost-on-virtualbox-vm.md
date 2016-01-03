---
layout: post
title: Accessing localhost on a VirtualBox VM
---
There are a number of great ways to test your web projects against the growing number of browsers and mobile devices. Lately, I have found myself using [BrowserStack](https://www.browserstack.com/). It's reasonably priced, easy to use, and has a large range of browsers and devices available.

However, for Internet Explorer testing, I find myself going back to the virtual machines that are provided by the team at [Modern.ie](https://dev.windows.com/en-us/microsoft-edge/tools/vms/mac/). They take a little bit of time to download and get installed, but the fantastic [ievms](https://github.com/xdissent/ievms) project makes the download and setup super simple if you are handy with the command line.

One thing that trips me up once I get the environment set up, is how to actually look at my local site in the IE browser that I have loaded in the virtual environment. Unfortunately, it isn't as simple as just typing in `http://localhost:3000` or using your local machine's IP address. To view a site running on localhost, you can simply use `http://10.0.2.2:3000` and that will map back to localhost on your local machine.

I am mainly writing this down because it trips me up every time. Hopefully, it saves other people time and frustration as well.
