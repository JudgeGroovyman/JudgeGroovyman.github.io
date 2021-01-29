# Jekyll #

- To debug my githubpages (where this is hosted) I had to follow [these steps](https://docs.github.com/en/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll) to install jekyll (easy per documentation no issues)
- Then when Jekyll was installed I did  ``jekyll new jekylltest --force`` and could have done that in my judgegroovyman.github.io folder instead of jekylltest because apparently it only overwrites jekyll files
- I accidentally installed Jeckyll too haha
- then ``bundle exec jekyll serve`` seems to serve a site and then I can go to the .md file but its not interpreted into html :(
- it doesnt show any errors either
- livereload doesnt work ``--livereload`` at the end 
- it seems like it copied all of the .md files over but I dont see any 
- Interesting this claims each of my files might need a yaml front matter section at the top.  They dont for github pages so ...
- Ok on Github it says I might have to [edit a gem file](https://docs.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll)
- in that gemfile it says to run ``bundle update github-pages`` after I've done that but that doesnt work. ``Could not find gem 'github-pages'.``
-  some googling suggests trying ``bundle update jekyll`` and then ``bundle install`` and yeah!  that seemed to work 
- AND it has an error which will let me figure out what to do about my site!! bingo!
- well kind of bingo.  it says games.md is the problem and it says its because there are some invalid non-utf-8 characters, but it doesnt say what they are or what line or anything
- after 3 failed experiments I ended up in notepad++ Encoding menu -> Convert to ANSI and then Convert to UTF-8.  


# Cool uses and abuses of web design #
* Ash made [his site](https://ash.ms/) look and behave like windows 95 and in a tiny super fast footprint
* @paul_v_m made [his site](http://paulvm.com/) look like a 90s website with flashing effects and crappy colors and under construction signs dancing pizza animations and all.

# Blog Frameworks #
Apart from wordpress and medium I've been recently intrigued by static site generators that take your markdown files (such as this website) and process them into a full website.  github is doing that for me here (It uses Jeckyll) but here are some other options:

* [A cool discussion of hosting for JAMStack ](https://news.ycombinator.com/item?id=19982918)
* [Jamstack Virtual Conference Oct 2020](https://www.youtube.com/playlist?list=PL58Wk5g77lF94tg-F3y5zRyDeLVhTDnTg)
* [Headless CMS](https://headlesscms.org) use with [Static Site Generators](https://www.staticgen.com) this is fundamental to the [JamStack](https://jamstack.org) 
* "Fast and secure sites and apps delivered by pre-rendering files and serving them directly from a CDN, removing the requirement to manage or run web servers."

best name that cristi invented Optimule.com (available)

"this time around I've added the requirement that this new stack MUST remove as many barriers to writing and publishing as possible and make it as pain free (maybe even fun) as possible." [josebrowne](https://josebrowne.com/tutorial-static-blog-using-headless-ghost-2-0-gatsby-netlify/) 

## Feel Best for Me and or Cristi:
 
 
- -----Options ---------
1. [Local Ghost + Gatsby + Netlify + Cloudinary](https://josebrowne.com/tutorial-static-blog-using-headless-ghost-2-0-gatsby-netlify/) this is a great and safe and secure and super fast and free option.  Theres no way to know how much it would stress the netlify or cloudinary limits except to try it out.
2. Obviously: Any of the Full or lighterweight CMS options hosted on our site
3. 


 
- ----- Full CMS---------
1. [Joomla](https://www.joomla.org) Best Free CMS 2019.  Easy to setup and try out for free at launch.joomla.com huge: 9% of business 6% of CMS 3% worldwide.  Content Versioning. Article and Media management. Harder to setup than wordpress #inmotion
2. [Drupal](https://www.drupal.org) Harder to setup than Joomla or Wordpress #inmotion
3. [Wordpress](http://wordpress.org) 	Easiest to setup #inmotion
14. [BoldGrid](https://www.boldgrid.com)	"works to make WordPress more intuitive. Tedious tasks are now automated"  	install on Wordpress #inmotion
- ----- Full modern CMS---------
2. [Laravel](https://laravel.com) Open Source.  "The framework for Web Artisans"   Huge discord.  Passionate dev.  1100 training videos
3. [Anchor](https://anchorcms.com) Open Source Free CMS.  Super lightweight.  2minute mostly file based install. There is a graphical editor super simple and lightweight. 3MB #inmotion
5. [Django-CMS](https://www.django-cms.org/en/) Open Source. Lively. A big deal.  Lean.  Use with desktop or mobile. Drag and drop page design. 
7. [PageKit](https://pagekit.com)	Beautiful Editing Features.  Totally Pro.  Built in marketplace with extensions.  Comment System.  Live Markdown preview.  Built sites easily. Stats in one place. 	 #inmotion auto install
20. [Microweber](https://www.phpwcms.org) 	The simplest way to build a great website for free.  Mobile friendly high performance and security. Stores 	300MB #inmotion
21. [Pimcore](https://pimcore.com/en)  	Pro CMS with extensive slick successful commercial side to maintain it which I think is good.  	326MB #inmotion
22. [Atlantis-cms](https://www.atlantis-cms.com)	Built on Laravel. Snappy Real Time On Page Editing. Rapid codeless page creation. 
23. [Zenario](https://zenar.io/about)	WYSIWYG. Forms.  Google Analytics. Dropbox. This seems well organized.  62MB #inmotion
24. [Publii](https://getpublii.com) 	Static Site CMS with GUI. Its a desktop app.  You edit it locally and can share it via dropbox. No security updates.  No databases to manage. WYSIWYG. Block Editor. Markdown. 9hr github. advanced SEO Features "Its so intuitive that something must be wrong" 	#favorite
- ----- Lightweight CMS--------- (Frontend that shows the site to the world)
11. [PostLeaf](https://www.postleaf.org/features) wow.  Minimal Admin experience.  True WYSIWYG. Dynamic images optimized and served responsibly. Styles are defined by the theme not the users. Simple Backup generate a zip with everything.  Does not align with other CMS. Automatic Sitemaps.  Fast Search.  Custom Post Templates. Super clean generated markup with look defined by themes.  SEO Friendly.  Integrated file manager.  Organized with tags.  Easily quick post from anywhere.  Spotlight search around the admin panel.   Revision History UPDATE: damnit  Last github update was 2018.   	[Installing PostLeaf On Digital Ocean](https://www.postleaf.org/installing-postleaf-on-digitalocean) $5/mo and quite a process!
1. [Bolt](https://bolt.cm)	 Free Forever	 Summary: "Easy for editors, and a developer's dream CMS. Bolt is an open source Content Management Tool, which strives to be as simple and straightforward as possible. It is quick to set up, easy to configure, uses elegant templates, and above all: It’s a joy to use."  There is a slack. 	Features: extensive tags for taxonomies.  Its just a folder on the server so updates are easy.   Themes. Forms to email or database.  Fast with Low Memory Usage.  Uses a Database (not like Grav which is just files)  58MB #inmotion  
4. [Grav](https://getgrav.org) 	Summary: flatFile Open Source CMS  "Grav will make you look like a hero developer"  Big Discord.  Markdown Only?   Nope theres an editor built into the admin screen.  and I much prefer that our files are open and obvious to them being stuck inside a database.  [Bolt vs Grav](https://www.cmswire.com/digital-experience/bolt-vs-grav-the-lightweight-standoff/) 30MB #inmotion #flat #Favorite
5. [Redax](https://redaxscript.com/features)	Summary: Ultralightweight and rocketfast.  Responsive with Modern CSS.  WYSIWYG  1.51MB #Inmotion #Favorite


- ----- Simple Website or Blog or CMS -------------
1. [Listed](https://listed.to) (0/10/50/150) Super Simple Public Journal. Use [Standard Notes](https://standardnotes.org) to make your blog but that costs 10/mo or 50/yr or 150/5yrs. Paywalls and donations builtin.  Listed comes with an editor or you can use markdown.  They even have a Longevity Statement.  Except that we might have to pay more (since I've already got a web server) I really like this option.  #TryThis This is such a cool simple possibility for a blog.
5. [Penzu](https://penzu.com) Free Military Grade Encrypted Private Journal for your own private thoughts online from mobile or PC.  Save to PDF. Share to the world if they have the link ... wonder if they are indexed by google?  Share to individuals with penzu account. 
16. [e107](https://e107.org) 	No code website. simple management. Website up in just 5 min. Batch changes. Media Manager. Image Resizing. 	33MB #inmotion
11. [TextPattern](https://textpattern.com)	Mature Classy! "simplify the production of well-structured, standards-compliant web pages. flexible, elegant" 	7MB #inmotion 
44. [Known](https://withknown.com) 	Lets you and the community that you attract create and share stories notes photos songs and more and links and respond to comments from any page on the web.  hashtags to categorize everything.  Responsive for mobile.  Theres a sub-web of other known sites that can interact somewhat. 	2MB Updated 2h ago  #Favorite
- -------- Portals ------------------------------------------
18. [Composr](https://compo.sr/features.htm) 	Community!  Lots of membership options here. Users personal photo galleries.  wiki. Quizzes Surveys tests cheat prevention. Downloads and documents library with ratings and leech protection.   Members can have their own blogs. Unlimited pages. WYSIWYG. Possible to run your own scripts.  Ecommerce.  Subscriptions.  Shopping Cart. Support Tickets. Newsletters (with double opt in).  WElcome email chain.  Bounce cleanup.  Flexible mailings.  (Deliverability?) Great forums and membership.  Content submission. Public awards of best content. Chatrooms. MOderation. Instant Messaging. Points system for members!  A virtual currency for members!  Polls (multiple polls) Spam Protection capcha 	50MB #inmotion
42. [LiveSite](https://livesite.com/features) 	A Whole portal of professional features.  Looks really pro. Live WYSIWYG Editing	42MB #inmotion
- ---------- Flat Files ----------------------------------------
12. [HTMLy](https://www.htmly.com/blog) 	Secure Flat File Blog! 	 3MB #inmotion #Flat
7. [Flatpress](https://www.flatpress.org)	Summary: Mini blog which stores your data as flat text.  Updated last year. totally mature and stable.  #inmotion #flat
39. [SiteMagic](https://sitemagic.org)	"The worlds most beautiful content management system" Pro beautiful designs.  No Database - XML by default (it says secure does that mean encrypted? Human readable?) Automatic mobile and SEO Features.  Extensible. Super fast even on slow sites.  Best web page design software in teh world - like photoshop for websites. TinyMCE.  Easily create sub sites which are isolated sites running on the same instance. 	24MB #inmotion #flat #Favorite 
41. [WonderCMS](https://www.wondercms.com)	WOW 1 step install. Put 5 files on the server.  Responsive.  Themes. Responsive. SEO. Live WYSIWYG. Security.	0.13MB #inmotion #Flat #Favorite
43. [Bludit](https://www.bludit.com)	Simple Fast Secure Flat File CMS. SEO Friendly. Looks slick and super pro.  Updated 33min ago.   	6MB #Flat #inmotion
45. [Kirby](https://getkirby.com/)	 Wow this looks so damn sexy.  Flat file CMS with loads of sexy modern style in the admin at least.  Updated 6min ago. 	12MB #flat #inmotion #Favorite
46. [Sofawiki](https://www.sofawiki.com/en/sofawiki) 	Wiki Flat CMS supports 90k pages or more.  Skins. CSS. Semantic fields for collecting data. This looks really really cool.  I can totally relate to this one.   	0.97MB  #Flat #inmotion 
- ---------- Pro ----------------------------------------
38. [Contao](https://contao.org/en/) 	Professional Websites Scalable Applications accessible for handicapped.  this loosk SUPER professional blogging.  38MB #inmotion
40. [OctoberCMS](https://www.wondercms.com/features) 	Based on Laravel. simplicity, flexibility and modern design.  700 THemes.  Twig. WYSIWYG. CDN Support "After using the system for several minutes, you will know enough to use it forever!"  	53MB #inmotion 
44. [Fork](http://www.fork-cms.com/features)	So slick and polished.  Killer themes. powerful apps. SEO and marketing. 	270MB #inmotion


- -----Headless CMS Back Ends ---------
1. [Netlify CMS](https://www.netlifycms.org)	Free Forever MIT	"Use Netlify CMS with any static site generator for a faster and more flexible web project" 	Tutorial: [Add to your existing Statically Generated site](https://www.netlifycms.org/docs/add-to-your-site/) installing it looks pretty damn tough but I think I could do it. Since JS is universal and its written in react it should work on any site.   or [Test it using Netlify to get a site up and running in seconds](https://www.netlifycms.org/docs/start-with-a-template/) Free custom domains
2. [prismic.io](https://prismic.io/pricing) 0/9/20/100/500 increases number of users and bandwidth. Free is compelling with 100GB and built in CDN!  	Wow built in CDN! 100GB/month 0.10/GB overage.  Q: Can you stick a limit on that and just let people suffer without?  Free plan will limit access to editing unless you pay to upgrade.  Other plans will charge you per GB.
- ------------ --------------------------
1. [Decoupled Drupal](https://www.gatsbyjs.com/docs/sourcing-from-drupal/) Use it with Gatsby for a near perfect combination of user friendliness and speed.  Theres kind of a lot of tutorial there.
3. [Wordpress Headless CMS](https://www.gatsbyjs.com/blog/2019-10-15-free-headless-cms/)
4. [Agility](https://agilitycms.com/pricing) 0/47/579 0 has limits on 2500 content items (pages pictures etc.) 10gb bandwidth and only 5 users.  I dont know but that might be enough ... otoh it says its got hard limits so it will just shut you down if you hit those limits.  You know what though ... If we are talking headless CMS that should be ok.  We still have our site and files on our end so that might work just fine.  If we can switch to another CMS anytime then that will be just fine.   Looks like free custom domains.
5. [Sanity.io](https://www.sanity.io/pricing) 0/199  Free has 100k-500k API Requests. 5GB Assets and 10k Documents 10GB Bandwidth 100 listeners and 3 users.	Real Time Collaboration. Document Revision History. Paste Formatted from Google Docs.  Works on your phone.  Batch image uploads.
6. Also [Genetics Mesh](https://getmesh.io/docs/administration-guide/) Requires Java to be installed on your server
7. [SuluCMS](https://symfony-cms.net/sulu) or 
8. [GraphCMS](https://graphcms.com/pricing) 0/29/129/699 which is free for lt2500 content items 
26. [Directus](https://directus.io) 	API based and database undefined for maximum developer flexibility.  Headless CMS.  This looks too complicated imho, otoh its a headless CMS built in.  This one is a big deal because theres so much flexibility it can legit be a high performance web app since its api based it can handle your game data or VR or wearables or just your raw data.  I have a feeling for an advanced user this could be one of teh most powerful tools in the list. 44MB #inmotion 
- -----Headless CMS Node Required ---------
9. [Strapi](https://strapi.io/documentation/v3.x/getting-started/quick-start.html) 0/how to install Strapi on a computer with node and npm
11. [Apostrophe](https://apostrophecms.com/features) 0 for node.js install



- ------Themes --------------------------
1. [Gantry](http://gantry.org) Themes for Wordpress or Grav or Joomla

- -----Static Site Generator Front Ends ---------
14. [Eleventy](https://www.11ty.dev) "Just the kind of simple / common sense tool I love. The data/folder hierarchy mechanism is super obvious and elegant." "Eleventy is absolutely wonderful. It’s by far the nicest static site generator I’ve used"    "Eleventy was the only one I could find that gave me the fine-grained control I needed at blazingly fast build times."  "“Seriously can't remember enjoying using a Static Site Generator this much. Yes Hugo is rapid, but this is all so logical. It feels like it was designed by someone who has been through lots of pain and success using other SSGs." #Favorite decent sized discord
1. [Hexo](https://hexo.io/) Super fast site generator.  Hundreds of themes.  OMG I can use Org-Mode to publish my Website!?!
2. [Hugo](https://gohugo.io) "The Worlds Fastest Framework for Building Websites" Static Site Generator
3. [Jeckyll](https://jekyllrb.com) "Get up and running in seconds" "Free hosting with Github Pages"
4. [Nikola](https://getnikola.com) Blogs with comments tags categories archives and feeds and image galleries and code listings
4. [Gatsby](https://www.gatsbyjs.com) React-based open source framework for websites and apps.  "Fast in every way that matters"  "Create a complete website in the time it takes to build a prototype" 2000+ plugins.   Themes! [Gatsby Wysiwyg with Sanity.io](https://www.youtube.com/watch?v=SLGkyodumKI).  [Tina-Starter-Grande](https://github.com/tinacms/tina-starter-grande) is a fresh starter for Gatsby that lets you edit things wysiwyg.  easy theme customization.  Parallax Hero.  Sanity.io is a headless CMS for Gatsby and is free for 3 users.  [4000 member chat](https://spectrum.chat/gatsby-js/general?tab=posts)  [Some Gatsby Sites pay $0 for hosting!](https://www.gatsbyjs.com/blog/100days-free-hosting/)  [Gatsby vs a few others](https://pagepro.co/blog/is-gatsbyjs-the-best-framework-for-building-static-websites-what-are-the-other-alternatives/)
10. [Vitepress](https://github.com/vuejs/vitepress) 	Free Forever	near instant hot reload and publish.   Really want to try this.	#TryThis Docs say its not ready for prime time
 - ----------------------------- 
1. [Nift](https://nift.dev) Fastest of all pretty much.  
2. A comparison of [Gatsby vs Jeckyll vs Hugo](https://www.gatsbyjs.org/features/jamstack/gatsby-vs-jekyll-vs-hugo) which is on the gatsby site so it might be biased but still.  
5. [Pelican](https://blog.getpelican.com)
6. [Poet](http://jsantell.github.io/poet/) Looks great for hackers.  A bit over my head but probably super fast to get going. 2019 update
7. [Metalsmith](https://metalsmith.io)
8. [spress](http://spress.yosymfony.com)
9. [Next.js](https://jamstack.org/generators/) For react apps.  Main competitor is Gatsby.  The most popular ssg
11. [Nuxt](https://jamstack.org/generators/) for statically generating Vue.js applications main competitor VuePress
12. [VuePress](https://jamstack.org/generators/) for statically generating Vue.js applications main competitor Nuxt


- ------- CDNs -----------------
1. [Cloudinary](https://cloudinary.com/pricing) 0/99/249/mo Free forever for all small-reasonable sized files
15. [Netlify](https://www.netlify.com/pricing/) 0/19/99/dev/mo for 19 you can password protect your site and share environment variables with your other sites. High Performance Hosting and Building 	Q: If you give them your cc to start a free site will they charge you if it gets slashdotted?
16. [Optimole](https://optimole.com)	 0/23/47/83/179/289 for visits 5k/25k/100k/250k/750k/1.5M	Wordpress plugin to speed up	Super optimizes images and speeds up loading of your wordpress dramatically 
17. [BelugaCDN](https://www.belugacdn.com)	1/20/150/mo and you pay by the gigabyte for overages 
17. [Beluga Hosting](https://hosting.belugacdn.com/cart.php?gid=7)	3/4/8/mo 3 only gives 3 websites 
 - --------------
17. [DigitalOcean](https://www.digitalocean.com/pricing/) Cheap Hosting and virtual servers for Ghost and all other stuff where you have to login like node or maybe even react.
16. [Vercel](https://vercel.com/guides/deploying-sanity-studio-with-vercel) Like netlify
 - -------------- FREE This is feeling somehow wrong but I think its totally right!?!
18. [AeonFree Hosting](https://aeonfree.com)	Seems too good to be true.  Free cpanel wordpress and lots of other software. no bandwidth limits or really any limits.  so weird but hey awesome!  [Bad Reviews here](https://www.saashub.com/compare-profreehost-vs-aeonfree) No forced ads though.
19. [ProFreeHost](https://profreehost.com) Better reviews than AeonFree
20. [Many More Free Hosts](https://www.saashub.com/compare-profreehost-vs-aeonfree) 0/348/3588 at the bottom of the page
21. [Other Free CDNs](https://geekflare.com/free-cdn-list/) and [Other Free CDNs](https://geekflare.com/free-cdn-list/)




## Feel Good and Worth Experimenting
2. [Strikingly](https://www.strikingly.com) (0/8/16/49/mo) "Within an hour we had the best landing page yet and for a fraction of the price." You can sell one product per site, and you can make unlimited free sites.  They are branded with an ad for strikingly but otherwise totally free.   Simplicity and Style.  Signups, forms, live chats, newsletters all built in (so they claim)  use your domain name if you pay.  Full ecommerce functionality.  Analytics built in.  Password protection.  #TryThis #LandingPage #AmazonAffiliate
3. [Site123](https://www.site123.com)  (0/12/mo) "By far the easiest website builder" Free for a subdomain. 
4. [Hubpages](https://hubpages.com) Start blogging instantly.  I think there are ads.  There is no customization at all but maybe thats ok.  "Hubpages majors on its ability to connect its users with a wide audience and earn revenue from ads and affiliates"   #TryThis #LandingPage #AmazonAffiliate
6. [Statamic](https://statamic.com/pricing) Wow this is a really cool Website Designer software.  Free for hobbies.  Pro for $259/yr. 
 - -------------- Blogs and CMS (many from Inmotion)
15. [Concrete](http://www.concrete5.org) 	"a delightful and efficient user experience. Go to any page , and editing toolbar gives you all the controls you need" 	156MB #inmotion
8. [Serendipity](https://docs.s9y.org)	A reliable, secure & extensible PHP blog 	27MB #inmotion 
9. [Dotclear](https://dotclear.org) 	This looks mature	 11MB #inmotion 
17. [Geeklog](https://www.geeklog.net) 	"The Secure CMS" Database Backend.   Blog with comments.  Plugins for forums and image galleries.	70MB #inmotion
18. [QuickCDN](https://opensolution.org/why-quick-cms-is-better.html)	10-20x faster than wordpress or joomla or drupal.  Id like to see that.  "There isn't any other CMS in the world, which would provide the same capabilities at speed this high" 32k websites using it.  Secure like an impregnable fortress.  they sell an upgrade for $150 with better SEO and 70 plugins which promises better SEO and features: .  The whole website and free product is focused on selling the upgrade.  I like that for a simple page its free and super fast and secure with SEO even if the upgrade has much of that better.  Is the free one responsive and mobile friendly?  Looks lik ethe free one doesnt have WYSIWYG  2MB #Inmotion
20. [Mahara](https://mahara.org/view/view.php?id=2) 	This one is really cool its an eportfolio with Collaboration learning and profiling your learning.  like a resume portfolio work samples projects theyve done. "Track your learning progress and achievements" "Give feedback on portfolios and support your students"  "Align your portfolio to a competency framework and visualise, which competencies you have already achieved."  "Create project portfolios together with others and use the discussion forums to talk about your work." Mobile Responsive design 	132MB #inmotion 
21. [CSZ CMS](https://www.cszcms.com)	Responsive " basis of Codeigniter3 and design the structure of Bootstrap3" Slick site. Updates super easy. 
31. [CMSimple](https://www.cmsimple.org)	German. Its so small I'm curious how it works.	4MB #inmotion 	
32. [Expression Engine](https://expressionengine.com/features)	Publish from phone. full featured forum. Multisite. Channels for simple creation of forms to store data for each different area of your site.  Parallax.	23MB #Inmotion
20. [ProcessWire](https://processwire.com)	"A joy to use at any scale"  Really advanced simple ways of collecting the content from your blog.  So reliable it requires no maintenance.   WYSIWYG.  Also it saves time with its ease. "Compared to Grav, Processwire has a much more intuitive UI and features while still very easy to develop for." 	29MB #inmotion
 - -------- Portals ------------------------------------------
10. [b2Evolution](https://b2evolution.net) 	Mature "The most integrated CMS ever.  homepage to a blog, a photo gallery or a newsletter... forums, members directory and private messaging" 	72MB #inmotion 
19. [Tiki](https://info.tiki.org/)  "Web Application Platform with the most built-in features"  Wiki Blog Forum WYSIWYG Galleries User Logins surveys quizzes polls.  Easy Forms for users to fill out.  Bug Tracker for example. Payments. 	164MB #inmotion
12. [Kopage](https://kopage.com/features)	 "With Kopage you can build simple websites, landing pages and blogs, but also professional, advanced websites" Bootstrap.  Themes. Secretly implies that its a flat file database!	20MB #flat #inmotion 
22. [ZSite](https://www.zsite.net/index.html) 	Marketing Portal.	35MB #inmotion
 - -------- Wiki ------------------------------------------
33. [PmWiki](https://pmwiki.org)	Custom skins.  Great access control.  Hundreds of plugins available.  Not WYSIWYG (simple markup used)	8MB #Inmotion
34. [MediaWiki](https://www.mediawiki.org/wiki/MediaWiki)	Obviously the most mature wiki.  Apparently some WYSIWYG Extensions  	200MB #Inmotion
35. [FosWiki](http://foswiki.org/About/WebHome)	Wow this looks so sophisticated and mature and slick.  WYSIWYG Built in	Looks like install wouldnt be too hard on #inmotion but not already supported
36. [Twiki](http://twiki.org) 	This is in PERL so could probably be installed on #Inmotion.  It looks pro and slick and I really like the look.  It loosk liek a pro blog. 
37. [DokuWiki](https://www.dokuwiki.org/dokuwiki) 	Wow this is what we used at work for a while and I really like this one.  Apparently install is super simple.  #Flat #Inmotion
 - -------- Forum ------------------------------------------
38. [PhpBB](https://www.phpbb.com)	Most Widely Used FOSS Bulletin Board in the world.  Loads of styles and extensions.  I like this one	27MB #Inmotion
39. [Simple Machines Forum](https://simplemachines.org)	Really nice and popular I like this one too	8MB #inmotion
40. [MyBB](https://mybb.com)	Great large community about making your own community. Ilike this one too  	8MB #inmotion
41. [Vanilla](https://vanillaforums.com/en/software/)	Easy to install and manage and very popular.
42. [PunBB](https://punbb.informer.com)	 Because Less Is More. This one looks great and I like how tight and lightweight it is.  I wonder if its easy to backup and restore to another server?	2MB #inmotion
43. [FluxBB](https://fluxbb.org) 	Super Lightweight 	1.41MB #inmotion
	
## Dont feel quite right
33. [Postachio](https://postach.io) 	$5/mo Really great idea to make any evernote into a blog!  so smart!  	
32. [WikkaWiki](http://wikkawiki.org/HomePage) 	Dead now unfortunately.  Author shut the doors. 
31. [Genix.me](https://genix.me)	This has almost no website explanation of what this is.  It doesnt sell it at all.
30. [Schlix](https://www.schlix.com) 	Multisite CMS. Handles high traffic load. SEO. Security. Support. Content versioning to go back in time.  	30MB #inmotion
29. [Lepton](https://lepton-cms.org/english/home.php) 	German.  Great Server precheck feature (which all of these should have 100%).  Great two factor authentication feature.  Not enough other clear features to make it appealing. 	21MB #inmotion	
28. [Plikki](https://plikli.com)	This one is sad it was made by one expert guy who literally yesterday wrote a sad letter saying he wasnt going to be able to release his new version of his software because of the 138 installs of his old software (where everyone agreed to leave the ads.txt installed so he would make tiny amounts of money) only 7 people left that in place.   #inmotion
27. [Pluck](https://github.com/pluck-cms/pluck) 	Theres no website for this website software haha.  It might be great but theres no way to know.  	5MB #inmotion
26. [Croogo](https://docs.croogo.org/2.0/en/getting-started/features.html) 	The website doesnt sell this at all.  I dont see anything interesting about it.  	50MB #inmotion
25. [WBCE CMS](https://wbce-cms.org/)	Primarily German forum and most users are German and it doesnt offer anything super unique 24MB 	#Inmotion
24. [Typesetter](https://www.typesettercms.com) 	I really want to like this but its dead :( 	#inmotion
23. [Pluxml](https://www.pluxml.org)	XML Flat File but its all in French so its not really reliably usable for english speakers.  No resentment here though every language deserves a great flat file blog!	3.17MB #Flat #Inmotion
22. [Jamroom](https://www.jamroom.net) 	"Site Builder. Form Designer. Developer Tools Responsive and fast" "Build a place for users to gather around a social topic. Connect with others who share your passion."	75MB #inmotion	
20. [PHPWCMS](https://www.phpwcms.org) 	Fast, flexible, robust, perfect 	20MB #inmotion
19. [ImpressCMS](https://www.impresscms.org/modules/content/content.php?content_id=5&page=showcase) 	small Promotion site to big 20k company website.  Forum. 	54MB #inmotion
18. [WebsiteBaker](https://websitebaker.org/pages/en/home.php) 	Uses PHP Droplets and jQuery.  Easy to use.  User registrations. SEO.  Upload files as a zip and this will unpack them 	22MB #inmotion
6. [Silverstripe](https://www.silverstripe.org/#tabpane-2432-2) Respected Open Source CMS.  (found this before I was in InMotion)  	53MB #inmotion 
20. [Zikula](https://ziku.la/en/downloads) 	"Simple websites and Complex Applications"  212MB #inmotion
19. [Php-Fusion](https://www.php-fusion.co.uk/about/about.php) 	something doesnt feel right about this, otoh their features page is amazing with tons of security and powerful conveniences  20MB #inmotion
18. [CMS Made Simple](http://www.cmsmadesimple.org) 	Too much configuration apparently required 	23MB #inmotion
17. [Xoops](https://xoops.org) 	"the ideal tool for developing small to large dynamic community websites, intra company portals, corporate portals, weblogs and much more" 26MB #Inmotion
16. [Modx](https://modx.com/content-management-framework)  "Create any type of content: blogs, landing pages, catalogs, forms, PDFs, dynamically generated CSV downloads" This is for developers who want to make something large and dynamic and looks really good.  	32MB #inmotion
5. [Ghost](https://ghost.org) 	Open Source Headless CMS "Publish Online and Deliver Newsletters to their audience"	Super easy to install on PC to try it out locally.  Super difficult to install on a picky Ubuntu linux server.  I have no interest in a complicated install but at least its free.  I was wondering if I could use it on my PC or laptop local and use it to publish to a folder that was a local git instance and then push when I'm ready and then go over to the Static Site Generator and do a build (or nightlies or something) 	Update: Node.js require a VPS or dedicated server so thats right out!  Maybe on DigitalOcean though for just $5/mo
3. [Typo3](https://typo3.org) Open Source, People have some bad impressions of this kind of shitty.	92MB #inmotionhosting 
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
6. 84 Portals or CMSs or Blogs on InMotion Alone
7. Tesy should all have a [server precheck](https://lepton-cms.org/english/about.php?lang=EN)
8. What about something like Reddit? Something with voting


[Grav](https://discord.com/invite/5VhYVkR) 201/2515
[Laravel](https://discord.com/invite/mPZNm7A) 1483/14141
[Gatsby](https://discord.com/invite/br9rbUE) 849/9822


Features:
Cool to be able to paywall things with a social tweet.  I'm pretty sure wordpress has this.  
Cool to have some reddit features like upvoting and downvoting
[More Features I might want like SEO](https://opensolution.org/comparison-of-the-quick.cms-and-quick.cms.ext-systems.html)

# Themes #
https://www.creativebloq.com/web-design/free-wordpress-themes-712429
Plus I bought one for Cristi and another for me in 2017

# Hosting #
Using Inmotion
1. I figured out how to transfer a domain over to inmotion  It was a process and you have to own the email that the domain is registered with or I dont think you can even do it.  It takes many steps
2.


# Image Optimization #
https://pngmini.com

[IMG Optim CLI for Batching](https://github.com/JamieMason/ImageOptim-CLI#installation)


`sips --resampleWidth 800 Test2.png`

