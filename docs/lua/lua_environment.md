# LuaEnvironment

The LuaEnvironment component manages all the variables, functions, executing code, etc. for a single Lua context.

The LuaScript component and Execute Lua command need a LuaEnvironment to be present in the scene in order to be able to execute Lua code. If you don’t add a LuaEnvironment object in your scene then a default one will automatically be created.

You can use multiple LuaEnvironments to ’sandbox’ the variables, functions and executing code of indepenent sets of Lua scripts. If you do this, make sure to reference the appropriate LuaEnvironment when using LuaScript components, ExecuteLua commands, etc.

The 'Remote Debugger' option activates the built-in MoonSharp remote debugger tool. The application will halt execution on the first executed line of Lua code and open a MoonSharp debugger window in your browser. See the MoonSharp documentation for more information on using the debugger.
 
# LuaUtils
 
 The LuaUtils component adds several useful utilities to the basic LuaEnvironment setup. 

## Registering C# Types

The most important function of LuaUtils is registering C# types so that instances of those types can be accessed from Lua scripts. In order to access the members of a C# type from Lua, the type first has to be registered with MoonSharp. For objects added using the LuaBindings component, the relevant types are registered automatically.

In some cases however, you will need to register a type explicitly. The easiest way to do this is by adding the type's name to the FungusTypes.txt or UnityTypes.txt JSON files referenced by the LuaUtils component. You can also create your own JSON files to register additional types. Note that types that are not contained in the main application DLL will need to use the namespace qualified type name in the JSON file.

Example of types JSON file:
```python
{
    "registerTypes" : [
        "Fungus.Block"
    ],
    "extensionTypes" : [
        "Fungus.LuaExtensions"
    ]
}
```

If you need to register types directly from C#, or do a more complex type of registration, you can use the MoonSharp UserData class to do this. See the MoonSharp documentation for a list of supported registration methods. A good place to register C# types is in the Awake method of a custom component.
