
# What is FungusLua?

FungusLua is an easy way to embed Lua scripting into your Unity project. Lua is an easy to learn scripting language so it's a great way to empower artists, writers and designers to use more of the power of Unity.

FungusLua provides a simple way to control Unity objects from Lua scripts. It has useful utilities for using Fungus flowcharts and dialogs, persisting variables between scene loads, localization, and working with the Unity Test Tools. 

We made FungusLua in response to requests from the Fungus community for a way to script Fungus commands from a text file or spreadsheet. We figured that if people are going to be writing commands in text files, why not go all the way and add a powerful embedded scripting language?

# Using FungusLua Independently

FungusLua can easily be used on its own if you don't need the rest of the functionality in Fungus.

1. In the project window, move the Fungus/Thirdparty/FungusLua folder up to the root of the project.
2. Delete the Fungus and FungusExamples folders.

The Tools > Fungus menu will now only show options for creating FungusLua objects. Obviously you won't be able to use Fungus functions like say(), menu(), etc. anymore, but you can still use LuaEnvironment, LuaBindings, LuaScript to add Lua scripting to your game.

# About Lua

![Lua logo](images/lua.png)

[Lua](http://www.lua.org/about.html) is a powerful, fast, lightweight, embeddable scripting language. It is a popular language for game development and supporting user modding. The standard resource for learning Lua is [Programming in Lua](http://www.lua.org/pil/1.html).

# About MoonSharp

![MoonSharp Logo](images/moonsharp.png)

[MoonSharp](http://www.moonsharp.org) is an open source implementation of the Lua scripting language written entirely in C#. 

FungusLua is essentially a set of wrapper components built on top of MoonSharp which make it easier to use Lua scripting directly in the Unity editor. MoonSharp does all the hard work really and is a completely awesome project :)

The [MoonSharp tutorials](http://www.moonsharp.org/getting_started.html) and [MoonSharp forum](https://groups.google.com/forum/#!forum/moonsharp) are great resources to learn how MoonSharp works, especially for more advanced usage.