---
layout: post
date: '2020-09-24'
author: Jon Brown
permalink: /blog/whats-the-deal-with-all-the-privacy-requests-in-catalina/
published: true
title: What's the Deal with All the Privacy Requests in Catalina?
description: What's the Deal with All the Privacy Requests in Catalina?
blogimgpath: 20200901Wh
tags:
  - MacOS
  - iOS
categories:
  - articles
fpimage: /assets/images/covers/2020/Header-Catalina-Privacy-fp.jpg
image: /assets/images/covers/2020/Header-Catalina-Privacy.jpg
thumbnail: /assets/images/covers/2020/Header-Catalina-Privacy.jpg
link: /assets/img/app-images/2020/Header-Catalina-Privacy.jpg
cta: 1
comments: true
---
Over the last few releases of macOS, Apple has been beefing up the Mac's
privacy controls so they more closely resemble what the company has done
in iOS. You've undoubtedly noticed that when you first launch a new app
on your iPhone or iPad, it often prompts for access to your contacts or
your photos, the camera or microphone, and so on. The idea behind those
prompts is that you should always be aware of how a particular app can
access your personal data or features of your device. You might not want
to let some new game thumb through your photos or record your voice.

macOS has been heading in this direction too, with macOS 10.15 Mojave
upping the stakes and 10.16 Catalina forcing apps to play this "Mother,
May I?" game in even more ways. As a result, particularly after you
first upgrade and whenever you install a new app, you may be bombarded
with dialogs asking for various permissions. For instance, the
[Loom](https://www.loom.com/) app that helps you make quick video
recordings of your screen requires lots of permissions. Grant them and
Loom won't have to ask again.

<img alt="Blog Photo" src="{{ site.site_cdn }}/assets/images/blog/2020/20200901Wh/Loom-privacy-requests.png" class="img-fluid rounded m-2" width="700" />


Loom's requests are entirely reasonable---it wouldn't be able to do its
job without such access. That applies more generally, too. In most
cases, apps will ask for access for a good reason, and if you want the
app to function properly, you should give it access.

However, be wary if a permission dialog appears and you don't recognize
the name of the app making the request or if you aren't doing anything
related to the request. Apple's hope is that you'll deny access to
requests from malicious apps.

The problem in Catalina is that apps have to ask for permission for so
many basic capabilities that users become overwhelmed by all the
dialogs. A good app, like Loom, will walk the user through accepting
them on its first launch, but even still, answering four or more
requests can be confusing.

You might be tempted to deny access categorically. That's fine from a
privacy standpoint, but not when it comes to functionality---when you
deny a permission request, you prevent that app from working as you
anticipate. Fortunately, you can always grant (or revoke) permission
later. And remember, once you've granted permission, you won't have to
do it again for that app---it's a per-app request, not a per-session
request.

To see which permissions you've granted or denied, open System
Preferences > Security & Privacy > Privacy. A list of categories
appears on the left; click one to see which apps have requested access.
If you've granted access, the checkbox next to the app will be selected;
otherwise it will be empty.

<img alt="Blog Photo" src="{{ site.site_cdn }}/assets/images/blog/2020/20200901Wh/Privacy-request-Camera.png" class="img-fluid rounded m-2" width="400" />


You'll notice that the lock in the lower-left corner of the System
Preferences window is closed. To make changes, click it and sign in as
an administrator when prompted.

Most of these categories are self-explanatory, but it might not always
be obvious why an app wants permission. In the screenshot above, for
instance, Slack has been granted access to the Mac's camera. Why? So its
video call feature can work.

Annoyingly, giving access often requires that you quit the app in
question before the permission takes effect. That's awkward on the first
launch of a new app, since you launch it, respond to a bunch of dialogs,
and then have to quit and relaunch before you can use it.

There are some categories (including some not showing above) that could
use additional explanation:

-   **Accessibility:** Apps that request
    accessibility access want to control your Mac. In essence, they want
    to be able to pretend to click the mouse, type on the keyboard, and
    generally act like a user. Utility and automation software often
    needs such access.
    <img alt="Blog Photo" src="{{ site.site_cdn }}/assets/images/blog/2020/20200901Wh/Privacy-request-KM-Accessibility.png" class="img-fluid rounded m-2" width="700" />

-   **Full Disk Access:** This category is a
    catch-all for access to areas on your drive that aren't normally
    available to apps, such as data in Mail, Messages, Safari, Home, and
    more, including Time Machine backups and some admin settings. Backup
    and synchronization utilities need full disk access, in particular.
    An app can't request full disk access in the normal way; you must
    add it manually by dragging its icon into the list or clicking the +
    button under the list and selecting the app in the Applications
    folder.
    <img alt="Blog Photo" src="{{ site.site_cdn }}/assets/images/blog/2020/20200901Wh/Privacy-request-FullDiskAccess-SD.png" class="img-fluid rounded m-2" width="700" />

-   **Automation:** The Mac has long had a way for
    apps to communicate with and control one another: Apple events. An
    app could theoretically steal information from another via Apple
    events, so the Automation category lets you specify which apps can
    control which other apps. You'll see normal permission requests, but
    they'll explain both sides of the communication. (System Events is a
    behind-the-scenes macOS utility that helps with scripting and
    automation.)
    <img alt="Blog Photo" src="{{ site.site_cdn }}/assets/images/blog/2020/20200901Wh/Privacy-request-Loom-Automation.png" class="img-fluid rounded m-2" width="700" />


So if you've been seeing repeated requests for permission in Mojave and
especially in Catalina, now you know why these dialogs keep popping up.
They're a bit irritating at first, but the added privacy is worthwhile,
and once you've granted permission to an app, you shouldn't hear from it
again.