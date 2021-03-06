
New Cookie Technologies: Harder to See and Remove, Widely Used to Track You
===========================================================================

DEEPLINKS BLOG

Technical Analysis by [Seth Schoen](/about/staff/seth-schoen)

September 14, 2009




*This is part 1 of a three-part series on user tracking on the web today. You can read Part 2 [here](https://www.eff.org/deeplinks/2009/09/online-trackers-and-social-networks).*

Cookies are still a privacy problem for web users, many years after privacy advocates first raised concerns about their use to track web browsing. Today, cookies are one of the main mechanisms that advertising companies like Google use to track and profile users across sites and over time -- often building up a single gigantic profile for years and years. Many EFF members respond to this threat by using their browsers' cookie management features to limit which cookies they'll accept or how long they'll be retained.

But it turns out that the cookie situation is quite a bit trickier today, and sites that want to track users have new technical options that are hard for users to respond to. The traditional "cookie" is an [HTTP cookie](http://en.wikipedia.org/wiki/HTTP_cookie), invented by Lou Montulli and John Giannandrea at Netscape in 1994. But today many browsers implement a range of things with the same kind of cookie-like tracking behavior -- mechanisms that are far less familiar, harder to notice, and often harder to control.

A great overview of the wide range of cookie technologies confronting us today is [Cleaning Up After Cookies](https://www.isecpartners.com/files/iSEC_Cleaning_Up_After_Cookies.pdf), an article published last year by Katherine McKinley at [iSEC Partners](https://www.isecpartners.com/). McKinley describes *five* cookie-like tracking methods that go beyond traditional HTTP cookies, and explains how browsers often fail to let users exercise meaningful control over these varieties of tracking.

The most prominent of these tracking methods is the so-called "Flash cookie", a kind of cookie maintained by the Adobe Flash plug-in on behalf of Flash applications embedded in web pages.<a href="#footnote1_ipafzgs" id="footnoteref1_ipafzgs" class="see-footnote" title="Adobe refers to Flash cookies as Local Shared Objects.  Aside from Flash cookies, the other kinds of cookie-like objects McKinley identifies are HTML 5 DOM storage, Microsoft Silverlight cookies, Microsoft Internet Explorer User Data Persistence, and Google Gears data.">1</a> These cookie files are stored outside of the browser's control. Web browsers do not directly allow users to view or delete the cookies stored by a Flash application, users are not notified when such cookies are set, and these cookies never expire. Flash cookies can track users in all the ways traditionally HTTP cookies do, and they can be stored or retrieved whenever a user accesses a page containing a Flash application. Some of the problems are [highlighted](http://www.gnashdev.org/?q=node/62) by Rob Savoye, the developer of [Gnash](http://www.gnashdev.org/), an open source Flash implementation.

Last month, a group of researchers at UC Berkeley led by Ashkan Soltani released a study, [Flash Cookies and Privacy](http://papers.ssrn.com/sol3/papers.cfm?abstract_id=1446862), about this technology and the ways it's being used to track Internet users today. The study found that Flash cookies are extensively used by popular sites, and that most users probably don't know about them or how to delete them. They also found that at least one major site uses them in a way that violates the advertising industry's own rules on tracking.

What's more, the Berkeley researchers found that Flash cookies are often used to deliberately circumvent users' HTTP cookie policies. That is, a site may intentionally store the *same information* redundantly in both HTTP cookie and Flash cookie forms. When a user deletes the HTTP cookie, the site may "respawn" it from the copy that was stored as a Flash cookie! It seems clear that site operators know many users don't want to be tracked with cookies, but have found a way of circumventing those users' privacy preferences.

These privacy-invasive marketing practices need [greater scrutiny](http://www.eff.org/deeplinks/2009/08/behavioral-tracking). We need more research to reveal whether the other kinds of cookies McKinley described are also being used to track users, as Soltani and his collaborators showed that Flash cookies are. It's entirely possible that Flash cookies will turn out to be just the tip of the next-generation user tracking iceberg.

Meanwhile, browser developers should do more to let users understand and control how they're being tracked -- using any of these techniques. Unfortunately, Adobe has made that extremely difficult with regard to Flash cookies, since they're stored outside of the browser's control, and since the official Flash plug-in isn't open source, users can't easily fix this for themselves. The [BetterPrivacy](https://addons.mozilla.org/en-US/firefox/addon/6623) Firefox plugin tries to address this by finding Flash cookies on the hard drive and regularly deleting them, but Adobe could help by ensuring their cookie system follows the browser's privacy settings.<a href="#footnote2_olcyc17" id="footnoteref2_olcyc17" class="see-footnote" title="Adobe currently provides an interface to manage Flash cookies, but most users are unaware of it, it&#39;s not integrated with browser cookie policies at all, and it seems to focus as much on the disk space Flash cookies can take up as on their privacy implications.  It also doesn&#39;t provide some of the kinds of control over cookies that regular browsers and browser plugins can.">2</a>

Clearly, there's a lot of work to be done to bring these next-generation cookies even to the same level of visibility and control that users experience with regular HTTP cookies.

-   

    <a href="#footnoteref1_ipafzgs" class="footnote-label">1.</a> Adobe refers to Flash cookies as [Local Shared Objects](http://en.wikipedia.org/wiki/Local_Shared_Object). Aside from Flash cookies, the other kinds of cookie-like objects McKinley identifies are HTML 5 [DOM storage](http://en.wikipedia.org/wiki/DOM_storage), [Microsoft Silverlight](http://en.wikipedia.org/wiki/Microsoft_Silverlight) cookies, Microsoft Internet Explorer [User Data Persistence](http://msdn.microsoft.com/en-us/library/ms531424(VS.85).aspx), and [Google Gears](http://en.wikipedia.org/wiki/Gears_(software)) data.
-   

    <a href="#footnoteref2_olcyc17" class="footnote-label">2.</a> Adobe currently provides an [interface to manage Flash cookies](http://www.macromedia.com/support/documentation/en/flashplayer/help/settings_manager07.html), but most users are unaware of it, it's not integrated with browser cookie policies at all, and it seems to focus as much on the disk space Flash cookies can take up as on their privacy implications. It also doesn't provide some of the kinds of control over cookies that regular browsers and browser plugins can.



