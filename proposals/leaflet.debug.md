Title
=====

Leaflet.Debug - An unobtrusive debug shim for Leaflet based maps

Abstract
========

Leaflet is the bomb... it is the web mapping got-to front end library.  Leaflet is also an elegantly crafted piece of software, employing an inheritance model that creates compact and easily extended code.  It is also extremely complex at the core and hard to debug.

Leaflet.Debug tries to do three main things to help address the development of web maps based on Leaflet.  First, it tries to not get in the way.  The core concept of the debug library is to be able to add a one line JavaScript include in your app and instantly get the benefit.  If you remove the one include, the library goes away with minimal impact to the Leaflet name-space and data structures.  Second, the debug library dynamically catalogs all classes and instances of Leaflet classes.  This dynamic tracking of the inheritance chains of classes as well as instances of these classes makes debugging and tracking down issues in your map much easier.  Finally, the debug library tries to provide helper functions at multiple complexity levels.  At the simple end of the scale the debug library will warn you if you do not have a simple map object in your map (yes, the most common issue for people on #leaflet IRC channel).  On the more complex end of the spectrum there are helper functions related to searching for layer instances etc.  The hope is that you can stop sprinkling debug code throughout your app and rely on the dynamic capability of a common debug library to help you develop your mapping apps.  In the future we are working toward also providing a small pop-up GUI based interface to the debug library to allow even easier exploration of events, objects, and debug capabilities.  

In this talk we will go over the basics of how the library integrates with the Leaflet architecture, what the basic capabilities are that come standard with the debug library, and how to extend the debug library with your application specific debug needs.  A demo will also be provided to drive home the usefulness of the library and show the basic capabilities.
