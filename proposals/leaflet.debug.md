Title
=====

Leaflet.Debug - An unobtrusive debug shim for Leaflet based maps

Abstract
========

Leaflet is the bomb... it is the go-to front-end library for web mapping.  Complex at the core for new developers and hard to debug, Leaflet is also an elegantly crafted piece of software, employing an inheritance model that creates compact and easily extended code.  

Leaflet.Debug has three objectives in supporting the development of web maps based on Leaflet.  First, it tries to not get in the way.  The core concept of the debug library is to be able to add a one-line JavaScript include in your app for instant benefit.  If you remove the one include, the library goes away with minimal impact to the Leaflet name-space and data structures.  Second, the debug library dynamically catalogs all classes and instances of Leaflet classes.  This dynamic tracking of the inheritance chains and instances of classes makes debugging and tracking down issues in your map easy and fast.  Finally, the debug library tries to provide helper functions at multiple complexity levels.  In its most basic use scenario, the debug library will warn you if you do not have a simple map object in your map (which is the most common issue for people on #leaflet IRC channel).  In more complex scenarios, there are helper functions related to searching for layer instances etc.  Using Leaflet.Debug, the hope is that you can stop sprinkling debug code throughout your app and rely on the dynamic capability of a common debug library to help you develop your mapping apps.  In the future we are working toward also providing a small pop-up GUI based interface to the debug library to allow even easier exploration of events, objects, and debug capabilities.  

In this talk and live demo of Leaflet.Debug we will go over the basics of how the library integrates with the Leaflet architecture, demonstrate the basic capabilities that come standard with the debug library, and demonstrate how to extend the debug library with your application-specific debug needs.  
