


# Cool uses and abuses of web design #
* Ash made [his site](https://ash.ms/) look and behave like windows 95 and in a tiny super fast footprint
* @paul_v_m made [his site](http://paulvm.com/) look like a 90s website with flashing effects and crappy colors and under construction signs dancing pizza animations and all.

# Blog Frameworks #
Apart from wordpress and medium I've been recently intrigued by static site generators that take your markdown files (such as this website) and process them into a full website.  github is doing that for me here (It uses Jeckyll) but here are some other options:


[Headless CMS](https://headlesscms.org) use with [Static Site Generators](https://www.staticgen.com) this is fundamental to the [JamStack](https://jamstack.org) 
"Fast and secure sites and apps delivered by pre-rendering files and serving them directly from a CDN, removing the requirement to manage or run web servers."




## Feel Best for Me and or Cristi:
 
- -----Full CMS---------
1. [Joomla](https://www.joomla.org) Best Free CMS 2019.  Easy to setup and try out for free at launch.joomla.com huge: 9% of business 6% of CMS 3% worldwide.  Content Versioning. Article and Media management.
2. [Drupal](https://www.drupal.org)
3. [Wordpress](http://wordpress.org)
2. [Laravel](https://laravel.com) Open Source.  "The framework for Web Artisans"   Huge discord.  Passionate dev.  1100 training videos
3. [Anchor](https://anchorcms.com) Open Source Free CMS.  Super lightweight.  Is there a wysiwyg editor or is it all markdown? At least in 2015 WYSIWYG was possible with one of several addons.  Could we get a markdown editor for Cristis phone and mac?
5. [Django-CMS](https://www.django-cms.org/en/) Open Source. Lively. A big deal.  Lean.  Use with desktop or mobile. Drag and drop page design. 
6. [Silverstripe](https://www.silverstripe.org/#tabpane-2432-2) Respected Open Source CMS.  

- -----Modern Lighterweight CMS--------- (Frontend that shows the site to the world)
11. [PostLeaf](https://www.postleaf.org/features) wow.  Minimal Admin experience.  True WYSIWYG. Dynamic images optimized and served responsibly. Styles are defined by the theme not the users. Simple Backup generate a zip with everything.  Does not align with other CMS. Automatic Sitemaps.  Fast Search.  Custom Post Templates. Super clean generated markup with look defined by themes.  SEO Friendly.  Integrated file manager.  Organized with tags.  Easily quick post from anywhere.  Spotlight search around the admin panel.   Revision History UPDATE: damnit  Last github update was 2018.   	[Installing PostLeaf On Digital Ocean](https://www.postleaf.org/installing-postleaf-on-digitalocean) $5/mo and quite a process!
1. [Bolt](https://bolt.cm)	 Free Forever	 Summary: "Easy for editors, and a developer's dream CMS. Bolt is an open source Content Management Tool, which strives to be as simple and straightforward as possible. It is quick to set up, easy to configure, uses elegant templates, and above all: It’s a joy to use."  There is a slack. 	Features: extensive tags for taxonomies.  Its just a folder on the server so updates are easy.   Themes. Forms to email or database.  Fast with Low Memory Usage.  Uses a Database (not like Grav which is just files) 
4. [Grav](https://getgrav.org) 	Summary: flatFile Open Source CMS  "Grav will make you look like a hero developer"  Big Discord.  Markdown Only?   Nope a REALLY cool 2019 plugin called [Editable with content tools](https://github.com/bleutzinn/grav-plugin-editable-contenttools) and I much prefer that our files are open and obvious to them being stuck inside a database.  [Bolt vs Grav](https://www.cmswire.com/digital-experience/bolt-vs-grav-the-lightweight-standoff/)

- -----Headless CMS Backend ---------

5. [Netlify CMS](https://www.netlifycms.org)	Free Forever MIT	"Use Netlify CMS with any static site generator for a faster and more flexible web project" 	Tutorial: [Add to your existing Statically Generated site](https://www.netlifycms.org/docs/add-to-your-site/) installing it looks pretty damn tough but I think I could do it. Since JS is universal and its written in react it should work on any site.   or [Test it using Netlify to get a site up and running in seconds](https://www.netlifycms.org/docs/start-with-a-template/)
1. [Decoupled Drupal](https://www.gatsbyjs.com/docs/sourcing-from-drupal/) Use it with Gatsby for a near perfect combination of user friendliness and speed
2. [Wordpress Headless CMS](https://www.gatsbyjs.com/blog/2019-10-15-free-headless-cms/)
3. [Agility](https://agilitycms.com/pricing) 0/47/579 0 has limits on 2500 content items (pages pictures etc.) 10gb bandwidth and only 5 users.  I dont know but that might be enough ... otoh it says its got hard limits so it will just shut you down if you hit those limits.  You know what though ... If we are talking headless CMS that should be ok.  We still have our site and files on our end so that might work just fine.  If we can switch to another CMS anytime then that will be just fine.  
4. [Sanity.io](https://www.sanity.io/pricing) 0/199  Free has 100k-500k API Requests. 5GB Assets and 10k Documents 10GB Bandwidth 100 listeners and 3 users.	Real Time Collaboration. Document Revision History. Paste Formatted from Google Docs.  Works on your phone.  Batch image uploads.
5. 

- -----Static Site Generator Front Ends ---------
1. [Hexo](https://hexo.io/) Super fast site generator.  Hundreds of themes.  OMG I can use Org-Mode to publish my Website!?!
2. [Hugo](https://gohugo.io) "The Worlds Fastest Framework for Building Websites" Static Site Generator
3. [Jeckyll](https://jekyllrb.com) "Get up and running in seconds" "Free hosting with Github Pages"
4. [Nikola](https://getnikola.com) Blogs with comments tags categories archives and feeds and image galleries and code listings
4. [Gatsby](https://www.gatsbyjs.com) React-based open source framework for websites and apps.  "Fast in every way that matters"  "Create a complete website in the time it takes to build a prototype" 2000+ plugins.   Themes! [Gatsby Wysiwyg with Sanity.io](https://www.youtube.com/watch?v=SLGkyodumKI).  [Tina-Starter-Grande](https://github.com/tinacms/tina-starter-grande) is a fresh starter for Gatsby that lets you edit things wysiwyg.  easy theme customization.  Parallax Hero.  Sanity.io is a headless CMS for Gatsby and is free for 3 users.  [4000 member chat](https://spectrum.chat/gatsby-js/general?tab=posts)  [Some Gatsby Sites pay $0 for hosting!](https://www.gatsbyjs.com/blog/100days-free-hosting/)  [Gatsby vs a few others](https://pagepro.co/blog/is-gatsbyjs-the-best-framework-for-building-static-websites-what-are-the-other-alternatives/)
10. [Vitepress](https://github.com/vuejs/vitepress) 	Free Forever	near instant hot reload and publish.   Really want to try this.	#TryThis Docs say its not ready for prime time
 - ----------------------------- 
2. A comparison of [Gatsby vs Jeckyll vs Hugo](https://www.gatsbyjs.org/features/jamstack/gatsby-vs-jekyll-vs-hugo) which is on the gatsby site so it might be biased but still.  
5. [Pelican](https://blog.getpelican.com)
6. [Poet](http://jsantell.github.io/poet/) Looks great for hackers.  A bit over my head but probably super fast to get going. 2019 update


- ------- CDNs -----------------
15. [Netlify](https://www.netlify.com/pricing/) 0/19/99/dev/mo for 19 you can password protect your site and share environment variables with your other sites. High Performance Hosting and Building 	Q: If you give them your cc to start a free site will they charge you if it gets slashdotted?
 - --------------
17. [DigitalOcean](https://www.digitalocean.com/pricing/) Hosting and virtual servers for Ghost and other stuff.
16. [Vercel](https://vercel.com/guides/deploying-sanity-studio-with-vercel) Like netlify
 - --------------


## Feel Good and Worth Experimenting
1. [Listed](https://listed.to) (0/10/50/150) Super Simple Public Journal. Use [Standard Notes](https://standardnotes.org) to make your blog but that costs 10/mo or 50/yr or 150/5yrs. Paywalls and donations builtin.  Listed comes with an editor or you can use markdown.  They even have a Longevity Statement.  Except that we might have to pay more (since I've already got a web server) I really like this option.  #TryThis This is such a cool simple possibility for a blog.
2. [Strikingly](https://www.strikingly.com) (0/8/16/49/mo) "Within an hour we had the best landing page yet and for a fraction of the price." You can sell one product per site, and you can make unlimited free sites.  They are branded with an ad for strikingly but otherwise totally free.   Simplicity and Style.  Signups, forms, live chats, newsletters all built in (so they claim)  use your domain name if you pay.  Full ecommerce functionality.  Analytics built in.  Password protection.  #TryThis #LandingPage #AmazonAffiliate
3. [Site123](https://www.site123.com)  (0/12/mo) "By far the easiest website builder" Free for a subdomain. 
4. [Hubpages](https://hubpages.com) Start blogging instantly.  I think there are ads.  There is no customization at all but maybe thats ok.  "Hubpages majors on its ability to connect its users with a wide audience and earn revenue from ads and affiliates"   #TryThis #LandingPage #AmazonAffiliate
5. [Penzu](https://penzu.com) Free Military Grade Encrypted Private Journal for your own private thoughts online from mobile or PC.  Save to PDF. Share to the world if they have the link ... wonder if they are indexed by google?  Share to individuals with penzu account. 
 


## Dont feel quite right
5. [Ghost](https://ghost.org) 	Open Source Headless CMS "Publish Online and Deliver Newsletters to their audience"	Super easy to install on PC to try it out locally.  Super difficult to install on a picky Ubuntu linux server.  I have no interest in a complicated install but at least its free.  I was wondering if I could use it on my PC or laptop local and use it to publish to a folder that was a local git instance and then push when I'm ready and then go over to the Static Site Generator and do a build (or nightlies or something) 	Update: Node.js require a VPS or dedicated server so thats right out!  Maybe on DigitalOcean though for just $5/mo
3. [Typo3](https://typo3.org) Open Source, People have some bad impressions of this
6. [Ghost Hosting](https://ghost.org) $29/mo with a beautiful powerful editor.  No free plan. Increased performance, SEO is better, fewer problems with the site.
7. [Wix](http://wix.com)
8. [Weebly](https://www.weebly.com)
9. [Contentful](https://www.contentful.com/pricing/) (0/489/mo) Pretty complicated in ways that I dont think it needs to be but awesome because the content is completely separate from the design.  Free plan could be pretty useful though.  
10. [Tumblr](https://www.tumblr.com) 
11. [Medium](https://medium.com) 
12. [Blogger](http://blogger.com) 
 - ----Cool though Expensive Headless CMSs----------
1. [Butter](https://www.g2.com/products/butter-cms/reviews) 49/124/249 30 day free trial.  "Integrate with Butters API in 60s"  great reviews.  
2. [Bold](https://www.g2.com/products/quintype-bold/reviews) 99 Separates content from presentation enabling new opportunities.  
3. [Mura](https://www.g2.com/products/mura/pricing) PRices Not Listed :( "mura was designed to deliver agile and elegant digital experiences—fast. For content authors, marketers, and developers, we put the power in your hands"
 
 
 
Note:
1. Maybe for every article on the blog publish another similar article on Hubpages.  
2. Maybe theres a way to make wordpress lightning fast?
3. What cmss are built in to inmotionhosting
4. Test Netlify vs Inmotionhosting
5. Free CMS to use with JamStack (see definition above for why)


[Grav](https://discord.com/invite/5VhYVkR) 201/2515
[Laravel](https://discord.com/invite/mPZNm7A) 1483/14141
[Gatsby](https://discord.com/invite/br9rbUE) 849/9822


# Themes #
https://www.creativebloq.com/web-design/free-wordpress-themes-712429
Plus I bought one for Cristi and another for me in 2017
