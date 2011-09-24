## Nicer Chrome Experience
by Nelson Minar <nelson@monkey.org>

A bit of Applescript to make Chrome integrate nicely on the Mac.

### OpenURLInNewChromeWindow.app

A replacement browser program that launches URLs in new Chrome windows. Chrome by default opens in tabs which is broken with spaces. This program is [originally by Mike Hardy](http://smoove-operator.blogspot.com/2011/06/open-links-from-external-applications.html); I modified it to always open the browser window at a specific size. More info [on my blog](http://www.somebits.com/weblog/tech/mac/chrome-new-window-spaces.html).

### surl.scpt

Opens the current contents of the clipboard in your browser. If the clipboard looks like a URL it'll open directly, otherwise it will make a Google search query. Handy as a hotkey: I use Alfred to bind this to caps lock. More info [on my blog](http://www.somebits.com/weblog/tech/good/capslock-to-search-google-on-macos.html).

AppleScript is in a binary format. Here's a text copy of the code for your inspection (may be out of date)

    set u to the clipboard
    if not (u starts with "http://" or u starts with "https://") then set u to "http://www.google.com/search?q=" & u
    open location u