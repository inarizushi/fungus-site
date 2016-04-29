# LuaScript

The LuaScript component provides an easy way to run Lua scripts in your scene. You can create a LuaScript object via (Tools > Fungus > Create > LuaScript).

# ExecuteHandler component

Looking at a LuaScript object in the inspector, you see that the first component is called 'ExecuteHandler'. This component allows you to specify options for when the Lua script should execute.

By default it executes the Lua script when the scene starts, but you can change this to execute after a delay, on every update, on trigger events, etc.

If you want to execute a LuaScript from a custom C# script, set the On Event to 'Nothing' and instead call the LuaScript.OnExecute() method directly. You can also call the OnExecute() method from a UI event, e.g. a UI Button 'On Click' event.

#  Lua script and files

You can enter the Lua code you wish to execute directly into the 'Lua Script' text box. You can also place the Lua code into a text file in your project and use the Lua File property to execute it. 

You can also use both options at the same time. The Lua File contents are loaded first and the Lua Script text is appended to that. This is a handy feature for code reuse and configuration, e.g. create a Lua text file with Lua functions to control your game, and then call those functions from the Lua Script text box.

# Lua modules

The Lua module system allows you to create reusable packages of Lua code and easily include these in your Lua scripts. [This tutorial](http://www.tutorialspoint.com/lua/lua_modules.htm) explains how to write Lua modules.

Modules in FungusLua need to be put into a special folder structure so that the require() function is able to locate them.

To use a module in FungusLua:
1. Create a Resources/Lua folder in your project. The case is important, but this can be created inside an existing folder in your project.
2. Create a mymodule.txt file inside the Lua folder and add your Lua script to it. (Obviously rename mymodule to whatever you want).
3. You can now use the Lua require function to load the module for use in any Lua script, for example
```python
local mymodule = require("mymodule")

-- Call a function on the module
mymodule.myfunction()
```

# Error messages

When a script contains errors there are a few techniques you can use to track down the source. 

FungusLua compiles Lua code at scene startup so that it can be quickly executed when needed later on. This means you will likely see Lua error messages in the console either at startup (during compilation) or when the script actually executes later.

All Lua script errors generate an error message in the Unity log (displayed in red).

For example, if you try to run this invalid code in a LuaScript object:
```python
not valid lua
```

It will generate an error message in the log like this
```python
LuaScript.LuaScript:(1,0-3): unexpected symbol near 'not'
1: not valid lua
```

- The first 'LuaScript.LuaScript' part gives you information about where the code is running from.
- The next part in brackets '(1,0-3)' tells you the line number and character range where the error is located.
- The last part gives you a description of the type of error.
- The next line on contains a listing of the Lua source code used. Use the linenumber info above to locate the line causing the problem.

One of the most common errors is attempting to access a variable that doesn't exist. In this example, we've tried to access the field 'name' on a variable v that hasn't been defined yet.

```python
LuaScript.LuaScript:(1,7-9): attempt to index a nil value
1: print(v.name)
```

To resolve this type of error, carefully check that the variable you want to access has been defined, is spelled correctly and is what you think it is. You can use the print() and inspect() functions to display information about the object on the log.

For runtime errors, a useful technique is to add print() calls in your code close to where the error occurs. You can print out information to the console to help track down the cause of the error.

MoonSharp includes a remote debugger tool you can use to step through Lua code and inspect variables. See the [LuaEnvironment documentation](lua_environment.md) for more information.


# Setting the LuaEnvironment

By default the LuaScript component will use the first LuaEnvironment it finds in the scene to execute, or create one if none exists. If you want to use a specific LuaEnvironment, set it in the Lua Environment property. This is a good way to keep unrelated sets of Lua scripts sandboxed from each other.

# RunAsCoroutine option

This option will run the Lua script as a Lua coroutine which is useful for writing asynchronous code (via the coroutine.yield() function in Lua). If you don't need to execute your script asynchronously, deselecting this option will avoid the overhead of running as a coroutine. Recommended for advanced users only!
