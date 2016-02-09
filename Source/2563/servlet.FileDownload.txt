__NOTOC__ __NOEDITSECTION__ __NOTITLE__
[[Category:Mobile]]
'''Navigation:''' [http://developer.force.com Developer Force] | [http://www2.developerforce.com/mobile/ Salesforce Mobile Services] | Native, HTML5 or Hybrid

[[image:banner.png | center]]
Screens are small, apps are big, and life as we know it is on its head again. In a world that's increasingly social and open, mobile apps play a vital role, and have changed the focus from what's on the Web, to the apps on our mobile device. Mobile apps are no longer an option, they're an imperative. You need a mobile app, but where do you start? 
<!-- cta title="[Get Started]" subtitle="Salesforce Mobile Services" linkurl="http://www2.developerforce.com/mobile"/>
<cta title="[Build] Mobile Apps" subtitle="Salesforce Mobile Packs" linkurl="http://www2.developerforce.com/mobile/services/mobile-packs"/ -->
There are many factors that play a part in your mobile strategy, such as your team’s development skills, required device functionality, the importance of security, offline capability, interoperability, etc., that must be taken into account. In the end, it’s not just a question of what your app will do, but how you’ll get it  there. 

Like Goldilocks, you may have to try a couple beds that are too soft or too hard, before you find the one that’s just right. And sometimes there’s just no perfect choice. Each development scenario has its pros and cons, and those might in be inline, or at odds, with your means. Unlike Goldilocks, there are no bears to contend with, and it’s our intent that this article keeps you from burning your lips on hot porridge (well, figuratively).

While this article addresses mobile app development in general, it is specifically targeted at developers looking to create mobile applications that interact with Salesforce.com, Force.com, or Database.com. Currently, the Salesforce Mobile SDK supports building three types of apps:

* '''Native apps''' are specific to a given mobile platform (iOS or Android) using the development tools and language that the respective platform supports (e.g., Xcode and Objective-C with iOS, Eclipse and Java with Android). Native apps look and perform the best.
* '''HTML5 apps''' use standard web technologies—typically HTML5, JavaScript and CSS. This write-once-run-anywhere approach to mobile development creates cross-platform mobile applications that work on multiple devices. While developers can create sophisticated apps with HTML5 and JavaScript alone, some vital limitations remain at the time of this writing, specifically session management, secure offline storage, and access to native device functionality (camera, calendar, geolocation, etc.)
* '''Hybrid apps''' make it possible to embed HTML5 apps inside a thin native container, combining the best (and worst) elements of native and HTML5 apps.

[[File:Native_html5_hybrid.png|center|550px|link=]]

=Native Mobile Applications=
In a nutshell, native apps provide the best usability, the best features, and the best overall mobile experience. There are some things you only get with native apps:

* '''Multi touch''' - double taps, pinch-spread, and other compound UI gestures
* '''Fast graphics API''' - the native platform gives you the fastest graphics, which may not be a big deal if you’re showing a static screen with only a few elements, or a very big deal if you’re using a lot of data and require a fast refresh. 
* '''Fluid animation''' - related to the fast graphics API is the ability to have fluid animation. This is especially important in gaming, highly interactive reporting, or intensely computational algorithms for transforming photos and sounds.
* '''Built-in components''' - The camera, address book, geolocation, and other features native to the device can be seamlessly integrated into mobile apps. Another important built-in components is encrypted storage, but more about that later. 
* '''Ease of use''' -  The native platform is what people are accustomed to, and so when you add that familiarity with all of the native features they expect, you have an app that’s just plain easier to use. 
* '''Documentation'''  -  There are over 2500 books alone for iOS and Android development, with many more articles, blog posts, and detailed technical threads on sites like StackOverflow. 

[[File:Native components.png|300px|right|link=]]

Native apps are usually developed using an integrated development environment (IDE). IDEs provide tools for building debugging, project management, version control, and other tools professional developers need. While iOS and Android apps are developed using different IDEs and languages, there’s a lot of parity in the development environments, and there’s not much reason to delve into the differences. Simply put, you use the tools required by the device.

You need these tools because native apps are more difficult to develop. Likewise, the level of experience required is higher than other development scenarios, you don’t just cut and paste Objective-C  and expect it to work. Indeed, the technological know-how of your development team is an important consideration. If you’re a professional developer, you don’t have to be sold on proven APIs and frameworks, painless special effects through established components, or the benefits of having your code all in one place. Let’s face it, today a skilled native iOS or Android developer is a rock star, and can make rock star demands. 

While we’ve touched on native apps from a development perspective, there’s also the more important perspective: the end user. When you’re looking for an app, you’ll find it in the store. When you start the app, it fires up immediately. When you use the app, you get fast performance, consistent platform look and feel. When your app needs an update, it tells you so. Native apps give you everything you’d expect from the company that built your device, as if it were simply meant to be.

=HTML5 Mobile Applications=
If you’re new to mobile app development, you’re late to the party. However, for mobile Web-based apps, we’re still partying like it’s 1999! Sure, browsers have gotten better in the past umpteen years, but the underlying technology isn’t that much different than when you feared the Y2K bug. 

But that can be a good thing. An HTML5 mobile app is basically a web page, or series of web pages, that are designed to work on a tiny screen. As such, HTML5 apps are device agnostic and can be opened with any modern mobile browser. And because your content is on the web, it's searchable, which can be a huge benefit depending on the app (shopping, for example). 

[[File:Html5_components.png|300px|left|link=]]

If you have experience developing Web apps, you'll take to HTML5 like a duck to water. If you're new to Web development, the technological bar is lower; it's easier to get started here than in native or hybrid development. Unfortunately, every mobile device seems to have their own idea of what constitutes usable screen size and resolution, and so there's an additional burden of testing on different devices. Browser incompatibility is especially rife on Android devices, so browser beware. 

An important part of the "write-once-run-anywhere" HTML5 methodology is that distribution and support is much easier than for native apps. Need to make a bug fix or add features? Done and deployed for all users. For a native app, there are longer development and testing cycles, after which the consumer typically must log into a store and download a new version to get the latest fix. 

In the last year, HTML5 has emerged as a very popular way for building mobile applications. Multiple UI frameworks are available for solving some of the most complex problems that no developer wants to reinvent. iScroll does a phenomenal job of emulating momentum style scrolling. JQuery Mobile and Sencha Touch provide elegant mobile components, with hundreds if not thousands of plugins that offer everything from carousels to super elaborate controls. 

So if HTML5 apps are easier to develop, easier to support, and can reach the widest range of devices, where do these apps lose out? We already reviewed the major benefits of native development, so we'll just reiterate that you can't access native features on the device. Users won’t have the familiarity of the native look and feel, or be able to use compound gestures they are familiar with. But strides are being made on all fronts, and more and more functionality is supported by browsers all the time. 

The latest batch of browsers support hardware accelerated CSS3 animation properties, providing smooth motion for sliding panels as well transitions between screens, but even that can’t match the power and flexibility of native apps. Today, it’s simply not possible to capture multi-touch input events (determining when more than one finger is on the screen) or create path-style elegance with spinout buttons and photos that hover, then drop into the right place.

However, significant limitations, especially for enterprise mobile, are offline storage and security. While you can implement a semblance of offline capability by caching files on the device, it just isn't a very good solution. Although the underlying database might be encrypted, it’s not as well segmented as a native keychain encryption that protects each app with a developer certificate. Also, if a web app with authentication is launched from the desktop, it will  require users to enter their credentials every time the app it is sent to the background. This is a lousy experience for the user. In general, implementing even trivial security measures on a native platform can be complex tasks for a mobile Web developer.  Therefore, if security is of the utmost importance, it can be the deciding factor on which mobile technology you choose.

=Hybrid Mobile Applications=
Hybrid development combines the best (or worst) of both the native and HTML5 worlds. We define hybrid as a web app, primarily built using HTML5 and JavaScript, that is then wrapped inside a thin native container that provides access to native platform features. PhoneGap is an example of the most popular container for creating hybrid mobile apps. 

For the most part, hybrid apps provide the best of both worlds. Existing web developers that have become gurus at optimizing JavaScript, pushing CSS to create beautiful layouts, and writing compliant HTML code that works on any platform can now create sophisticated mobile applications that don’t sacrifice the cool native capabilities. In certain circumstances, native developers can write plugins for tasks like image processing, but in cases like this, the devil is in the details. 

On iOS, the embedded web browser or the UIWebView is not identical to the Safari browser. While the differences are minor, they can cause debugging headaches. That’s why it pays off to invest in popular frameworks that have addressed all of the limitations. 

[[File:Hybrid.png|center|550px|link=]]

You know that native apps are installed on the device, while HTML5 apps reside on a Web server, so you might be wondering if hybrid apps store their files on the device or on a server? Yes. In fact there are two ways to implement a hybrid app. 

* '''Local''' - You can package HTML and JavaScript code inside the mobile application binary, in a manner similar to the structure of a native application. In this scenario  you use REST APIs to move data back and forth between the device and the cloud. 
* '''Server''' - Alternatively you can implement the full web application from the server (with optional caching for better performance), simply using the container as a thin shell over the UIWebview.

Netflix has a really cool app that uses the same code base for running the UI on all devices: tablets, phones, smart TVs, DVD players, refrigerators, and cars. While most people have no idea, nor care, how the app is implemented, you’ll be interested to know they can change the interface on the fly or conduct A/B testing to determine the optimal user interactions. The guts of decoding and streaming videos are delegated to the native layer for best performance, so it’s a fast, seemingly native app,  that really does provide the best of both worlds.

=Conclusion=
Mobile development is a constantly moving target. Every six months, there’s a new mobile operating system, with unique features only accessible with native APIs. The containers bring those to hybrid apps soon thereafter, with the web making tremendous leaps every few years. Based on current technology, one of the scenarios examined in this article is bound to suit your needs. Let's sum those up in the following table:

{|  class="gallery" border="1" 
|- 
| || '''Native''' || '''HTML5''' || '''Hybrid'''
|- 
| '''App Features''' 
|-
| Graphics || Native APIs || HTML, Canvas, SVG || HTML, Canvas, SVG
|-
| Performance || Fast || Slow || Slow
|-
| Native look and feel || Native || Emulated || Emulated
|-
| Distribution || Appstore || Web || Appstore
|-
| '''Device Access'''
|-
| Camera || Yes || No || Yes
|-
| Notifications || Yes || No || Yes
|-
| Contacts, calendar || Yes || No || Yes
|-
| Offline storage || Secure file storage || Shared SQL|| Secure file system, shared SQL
|-
| Geolocation || Yes || Yes || Yes
|-
| '''Gestures''' 
|-
| Swipe || Yes || Yes || Yes 
|-
| Pinch, spread || Yes || No || Yes
|-
| '''Connectivity''' || Online and offline || Mostly online || Online and offline
|-
| '''Development skills''' || ObjectiveC, Java || HTML5, CSS, Javascript || HTML5, CSS, Javascript 
|}


<!--
=Next Steps=
We encourage you to learn from existing applications, focus on the user experience, and experiment along with us. If you haven't already, 
#Get a [http://developer.force.com/join Developer Edition] organization<!-- or Database.com? -->. <!--Does a DB.com edition give them a developerforce membership and allow them to look at the boards, etc? Without Visualforce, DB.com users are pretty much stuck with Native, and so this article has little to do with them. And with only 7 total customers so far, maybe it's time we stop doing gymnastics to include DB.com in places it doesn't belong. Just a thought. -->
#Download the [https://github.com/forcedotcom/SalesforceMobileSDK-Android Android] or [https://github.com/forcedotcom/SalesforceMobileSDK-iOS iOS] Salesforce Mobile SDK from GitHub.
#Download the [https://github.com/forcedotcom/SalesforceMobileSDK-Samples/raw/master/Mobile_SDK_Workbook.pdf Mobile SDK Workbook], build an app, and step through the code with us. 
#Log into the [http://boards.developerforce.com/t5/Mobile/bd-p/mobile Mobile forum] of the Force.com Discussion Boards, ask questions, and contribute back your stories.

==Recommended Mobile SDK Learning Paths==

* [http://wiki.developerforce.com/page/Getting_Started_with_the_Mobile_SDK_for_Android Getting Started with the Mobile SDK for Android]
* [http://wiki.developerforce.com/page/Getting_Started_with_the_Mobile_SDK_for_iOS Getting Started with the Mobile SDK for iOS]
* [[Webinar:_IntroMobileSDK|Webinar: Introduction to the Mobile SDK]]
* [http://media.developerforce.com/workbooks/Mobile_SDK_Workbook_web.pdf]

== Related Mobile SDK Resources ==

* [https://github.com/forcedotcom/SalesforceMobileSDK-Samples Sample Apps on GitHub]
* [http://blogs.developerforce.com/blog/tag/mobile Recent related blog posts]
* [http://forcedotcom.github.com/SalesforceMobileSDK-Android/index.html API Java Docs for Android]
* [http://forcedotcom.github.com/SalesforceMobileSDK-iOS/Documentation/SalesforceSDK/index.html API Docs for iOS]
* Recent conference sessions
** [http://www.youtube.com/watch?v=NV9gmPpNusc&list=PLF026621A1E285E8E&index=12&feature=plpp_video Developing Native iOS Apps with the Force.com Mobile SDK (Cloudstock March 2012)]
** [http://www.youtube.com/watch?v=auMyviKiGH0&list=PLF026621A1E285E8E&index=3&feature=plpp_video Develop Mobile Web and Hybrid Apps (Cloudstock March 2012)]
** [http://developer.force.com/dreamforce/11/session/Developing-Mobile-Apps-for-Force-com-and-Database-com Developing Mobile Apps for Force.com and Database.com (Dreamforce September 2011)]

-->

'''''Authors: Mario Korf and Eugene Oksman'''''
