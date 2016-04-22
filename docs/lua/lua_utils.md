# Lua Utils

LuaUtils is a component that extends the Lua environment with some commonly used functionality. It can be accessed from Lua scripts via the 'luautils' global variable. This component mostly does a lot of setup work in the background, but it also exposes some handy functions for managing gameobjects in the scene.

# Example

Here's an example of the kind of thing you can do:
```python
local go = luautils.Find("MyObject") -- Find a game object by name
luautils.Destroy(go) -- Destroy it
```

# GameObject Functions

This is the list of GameObject functions provided in luautils.

```python
-- Find a game object by name and returns it.
GameObject Find(string name)

-- Returns one active GameObject tagged tag. Returns null if no GameObject was found.
GameObject FindWithTag(string tag)

-- Returns a list of active GameObjects tagged tag. Returns empty array if no GameObject was found.
GameObject[] FindGameObjectsWithTag(string tag)
			
-- Create a copy of a GameObject.
-- Can be used to instantiate prefabs.
GameObject Instantiate(GameObject go)

-- Destroys an instance of a GameObject.
Destroy(GameObject go)

-- Spawns an instance of a named prefab resource.
-- The prefab must exist in a Resources folder in the project.
GameObject Spawn(string resourceName)
```

# Registering C# Types

The most important function of the LuaUtils component is registering C# types so that instances of those types can be accessed from Lua scripts. 

In order to access the members of a C# type from Lua, the type first has to be registered with MoonSharp. Note that for objects added using the LuaBindings component, the relevant types are registered automatically.

In some cases however, you will need to register a type explicitly. The easiest way to do this is by adding the type's name to the FungusTypes.txt or UnityTypes.txt JSON files referenced by the LuaUtils component. You can also create your own JSON files to register additional types. Note that types that are not contained in the main application DLL will need to use the namespace qualified type name in the JSON file.

# Example JSON Type File

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

# Registering Types Directly

If you need to register types directly from C#, or do a more complex type of registration, you can use the MoonSharp UserData class to do this. See the MoonSharp documentation for a list of supported registration methods. A good place to register C# types is in the Awake method of a custom component.

# Other Utilities

LuaUtils also binds several useful C# classes and components so that you can access them easily from Lua script.

```python
time 			-- The Unity Time class. e.g. 'time.deltaTime' returns the delta time for this frame.
prefs 			-- The FungusPrefs class (documented elsewhere)
factory 		-- The PODTypeFactor class (documented elsewhere)
luaenvironment 	-- The LuaEnvironment component used to execute Lua scripts
luautils 		-- A reference to the LuaUtils component itself
test 			-- Unity Test Tools (if installed)
stringtable 	-- The localisation string table (documented elsewhere)
```

