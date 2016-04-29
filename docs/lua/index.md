+ Tutorial video for main bits


+ Lua video should answer 'how to' questions first
+ Tracking down syntax errors
+ Using Require and Resource/Lua

+ Add Examples
+ Add screenshots
+ Add links to other resources

# What is FungusLua?

# Using as a standalone package

FungusLua can be used on its own if you don't need the rest of the functionality in Fungus.

1. Move the Fungus/Thirdparty/FungusLua folder up to the root of the project.
2. Delete the Fungus folder.

The Tools > Fungus menu will now only show options for creating FungusLua objects. Obviously you won't be able to use Fungus functions like say, menu, etc. anymore, but you can still use LuaEnvironment, LuaBindings, LuaScript to add Lua scripting to your game.

# About Lua

[Lua](http://www.lua.org/about.html) is a powerful, fast, lightweight, embeddable scripting language. It is a popular language for game development and supporting user modding. The standard resource for learning Lua is [Programming in Lua](http://www.lua.org/pil/1.html).

# About MoonSharp

[MoonSharp](http://www.moonsharp.org) is an open source implementation of the Lua scripting language written entirely in C#. FungusLua is basically a set of wrapper components built on top of MoonSharp which make it a bit easier to use Lua scripting directly in the Unity editor. MoonSharp does all the hard work really and is completely awesome :)

The [MoonSharp tutorials](http://www.moonsharp.org/getting_started.html) and [MoonSharp forum](https://groups.google.com/forum/#!forum/moonsharp) are great resources to learn how MoonSharp works, especially for more advanced usage.