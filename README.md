The New ShowcaseView (v5.0)
====

This library has become more popular than I ever intended - but at the same time more unwieldy.
This branch (which will become the next version) is intended to be more stable,
more friendly and better tested. I *will* remove features relative to the previous versions. It
is hoped than I'll add them back (or of course, you can).

What's missing
---

- ShowcaseViews: the class which queues up ShowcaseViews in a tutorial-type method. I never
really liked this class (generally, you should use SCV sparingly); I'll add it back in based on
the Builder class when I can.
- Ghostly hand: this has gone for now until I can test-drive it back in.
- Scale multiplier: this has gone for simplicity - if people really loved it I'll add in back in

FAQs
---

**Where has X feature gone?**

Look one paragraph up!

**What happened to all the other constructors?**

Gone. You should be using the new Target API.

**What if I want to add feature X?**

At the moment, I'm not taking any feature requests. It's unlikely I'll take many anyway,
unless I feel they are both useful and well tested. If you have some cosmetic tweak then I don't
want that added into the library as *another* option. But, if you need to make a tweak to the
library to add such a tweak to your own, overridden ShowcaseView then that is totally great.

ShowcaseView library
====
  
The ShowcaseView library is designed to highlight and showcase specific parts of apps to the user with a distinctive and attractive overlay. This library is great for pointing out points of interest for users, gestures, or obscure but useful items.

The library is based on the "Cling" view found in the Launcher on Ice-Cream Sandwich and Jelly Bean, but extended to be easier to use.

Please check out [the website](http://espiandev.github.com/ShowcaseView) for more information.

![Example image](./example.png)
![Example image](./example2.png)

Set-up
----

The library is now only compatible with Gradle out of the box. To use this library in your project, either:

* ~~Add the dependency from Maven like so: `compile 'com.github.amlcurran:showcaseview:+'`~~ *the library isn't currently available on Maven, but should be shortly*
* Copy the library project into your Gradle project. In your settings.gradle, add the project (using the `include (':libary')` notation). Sync Gradle and then go ahead! 

Usage
----

To use ShowcaseView, use the Builder pattern.

As an example:

~~~
new ShowcaseView.Builder(this)
    .setTarget(new ActionViewTarget(this, ActionViewTarget.Type.HOME))
    .setContentTitle("ShowcaseView")
    .setContentText("This is highlighting the Home button")
    .hideOnTouchOutside()
    .build();
~~~

Copyright and Licensing
----

Copyright Alex Curran ([+Alex](https://plus.google.com/110510888639261520925/posts)) © 2012. All rights reserved.

This library is distributed under an Apache 2.0 License.
