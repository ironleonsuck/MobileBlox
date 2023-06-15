# MobileBlox
Mobile Blox Android 32 bits Executor Roblox Open Source, version 2.555.874

This is supposed to be used for learning how Luau Executors work in an Android device
And their differences compared to PC which aren't much.
Also for beginners on Roblox Modding to have a chance at modding android
Which is a good start before continuing to PC where there are more resources available.

Only has loadstring and uses a simple Lua UI as giving away a whole executor with
Lots of script support wouldn't be good.

Addresses located at globals.hpp
Should be easy to update if you know how.

To inject in Roblox just compile the source, then get the library
`libmobileblox.so`

And put it in Roblox's APK folder `lib/`
Now decompile the Roblox's classes.dex and go to 
`com/roblox/client/ActivityNativeMain`

In there find the `OnCreate` method and just below it Paste this

```
const-string v0, "mobileblox"
invoke-static {v0}, Ljava/lang/System;->loadLibrary(Ljava/lang/String;)V

<a href="https://ibb.co/y8xNsxW"><img src="https://i.ibb.co/y8xNsxW/86-B3-B6-EB-2743-41-B5-BB71-C5108-E82-A715.png" alt="86-B3-B6-EB-2743-41-B5-BB71-C5108-E82-A715" border="0"></a> <a href="https://ibb.co/jW2gQRn"><img src="https://i.ibb.co/jW2gQRn/2-E3193-C4-2-CD7-4-A3-E-9-D5-D-9-FCF37036-F3-A.png" alt="2-E3193-C4-2-CD7-4-A3-E-9-D5-D-9-FCF37036-F3-A" border="0"></a>
```
