# Web

A new, simple browser automation API and library that automatically builds page objects and site structures.

## The API



### USE
Specify which browser to use.  

Accepts a yet to be determined configuration object that is almost, but not entirely unlike Webdriver's "desiredCapabilites" (TODO: LINK)



### LOAD

Load a URL in the browser.

Accepts either a string (URL) or a page object or a site object containing either a URL or BASEURL attribute.

Configuration parameters will determine whether it clears the cache, deletes cookies, loads a browser's user profile, or whatever.  
You probably don't want to dink around with them anyway.



### FIND

Find an element (or area) on the page.  

Accepts either a string or a locator object.  Returns an Element that is alomst (yada yada) a "WebElement".

Gives focus to the element as needed.  Points the mouse over it (if desired).  All sorts of weird configurable and unspecified behaviors.

And by "returns" mentioned above, I mean sets current scope.  Setting the scope is a a big part of what makes **Web** cool and easy to use.  It keeps commands clean and makes it obvious what you're working with.  Scope will undoubtably (undoubtedly?) be the source of many bugs -- not just in your code, but in the framework as well.  

It searches for the element based on the current scope, which by default is the whole page.  It gets tricky after that, but you can also find an element within the scope of another element you find.



### TYPE

Undocumented.



### CLICK

Since there is a whole can of worms around "clicking", suffice it to say that every mouse action and multi-touch action is supported.  It's just hidden from the user.

Secretly, there are "mouse" and "keyboard" (and "screen" for multitouch) that you can press, left, swipe, pinch, spread, pick, flick, wipe, eat, etc.  

You can even combine mouse and keyboard commands like this:

`{ keyboard.press(ctrl, alt, delete), mouse.righti[NotContext]PressAndHold() }`

to create rude guestures and other disgusting behaviours.

**Web** also supports non-traditional inputs from joysticks and XBOX Kinekt (sp?) sensors as well as accessibility related tools like speak-n-spell or artificial limbs.

They're just not implemented yet.



### GET

Get the text (by default) or the HTML (if you're weird) or take a picture (if you're into that).i

I'm not sure how we'll tell it to do that because I don't want you to have to mess with the configuration, but in the interest of keeping the API simple, and after that peek into the complexity of mouse/keyboard/bionic interaction, I'm going to wave my hand and say it just works.

What it gets the whatever from is determined by the aforementioned scope, just like click and type.



## More

You can name pages and locators and elements to make your code more readable.  

You can also build complex actions and name them so that you can call them directly.


* also note how I spelled "behaviours" in the British style once.  That shows that we have support for Internationalities and L18N.



### @TDRL:

LOAD, FIND, CLICK, TYPE, GET



## FAQ

###A. Is this a joke?

No, this isn't a joke. It's just really (kinda?) funny.  And coming soon.

###B. How can I help?

Your assistance is required.  Your cooperation is not expected.

###C. When can I use it?

Read the LICENSE.

###D. What is the license?

Fine, don't read the LICENSE.

###E. How can I use **Web** for testing?

Naturally, being a startup, we're working on a subscription model.  Something Sassy.  I'm pretty sure it will be a mobile app that contains a URL to donate to my paypal account.  And there will be a cool Web 2.0 interface that allows you drag and drop commands and run them in the cloudtubes(TM) and will generate charts guaranteeed to get you a raise when your manager see them.  But of course, that won't be available until we release **Web 2.0**

###F. I meant how can I write tests with Hart?

Check out our sister project [ **Check**  https://github.com/fijiaaron/check ]. It's like a test framework with assertions, but a bit more passive agressive.  And it doesn't mix your tests with your automation.  And it allows you to mix your tests with your automation.  Without mixing them up.

#G. I want to give you money right now.

Give it to OSSO instead http://orphanagesupport.org.  They help orphans.
