# Tabs for early Internet Explorer (Pocket PC - Windows Mobile - Windows 10 Desktop)
  
One `.exe` that runs on Windows Mobile 2000 to your Windows 10 desktop?  
  
Yes. Here's how it works.  
  
## Why add tabs to IE?
This app is a cross-architecture binary. It'll run on the ARM processors of Windows Mobile, 
to the latest AMD 64-bit processors. Internet Explorer discovered tabs in IE 7 during 2006. 
Our app brings tabs to nearly 1996.
  
Let's take a look at the constraints, complexities - fun parts too - of 
developing for .NET *Compact* Framework 3.5  
  
## A quick overview.
How does this work? The code is almost too easy. We're using Microsoft's .NET CF (Compact Framework). 
It **has a browser already**, just drag-n-drop it in your app. Next comes the tabs, how do we do 
that? It also, **is already a built-in object**. Double click or drag it on your app. That's how easy 
it should be (but it's not).
  
## The problems this repo solves (real cross-compatability).
1. WebBrowser controls crash when put inside a TabControl.
2. Many, many .NET CF controls will instantly crash if you try to run on desktop Windows.
3. This framework was designed for 320px max screen resolution - apps are incredibly blurry on modern screen sizes.
4. The oldest versions of WebBrowser never added `forward`, `backward`, or `history`.
  
## What we'll cover
1. Adding our own `forward`, `back`, `history` ...
2. Checking for high-DPI support for non-blurry apps
3. Multi-Threaded Apartment vs Single-Threaded (adding desktop Windows support)
  
  
References  
@/Rosesam, @/JohnS, https://www.ppcplanet.org/
