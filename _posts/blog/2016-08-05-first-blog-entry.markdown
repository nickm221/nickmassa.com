---
layout: post
title:  "Hosting a Website on Github"
date:   2016-08-05 12:05:11 am
categories: blog
---

It is incredibly easy to setup and host a static website using GitHub.  In order to setup a basic web page, create a new repository, and create a branch within that repository called "gh-pages".  Add the website’s HTML and CSS files to this repository.  Once you have created some basic content for your website and have stored the files under the gh-pages branch, navigate to “http://www.github.com/username/repository name” and switch to the Settings tab.  Scroll down until you see the GitHub Pages section.  Within this section, ensure that the source is set to the gh-pages branch, and enter your chosen domain name.  Once the settings are complete on the GitHub side, you will need to make some slight adjustments to your DNS settings.  

Follow your DNS provider's instructions to create a CNAME record that points from your default GitHub Pages domain (<your GitHub username>.github.io) to your subdomain.  Be sure to not use a wildcard DNS record, such as *.example.com, because this will allow anyone to host a GitHub pages site on one of your subdomains.  In order to serve the page, your DNS records must point to GitHub’s server.  To point your DNS records to GitHub’s server, follow your DNS provider's directions to create an A record that points to 192.30.252.153 and 192.30.252.154.  
