# LuaBindings component

The LuaBindings component allows you easily map gameobjects and components in your scenes to Lua variables which you can then access in your Lua scripts. You can bind to any component, including standard Unity components, components from the asset store and your own custom scripts.

# Adding LuaBindings

To setup LuaBindings in your scene:

1. Create a LuaBindings object (Tools > Fungus > Create > LuaBindings)
2. Drag the Unity object you want to access to the Object field in the Object Bindings list.
3. The binding key field is automatically populated based on the object name. This will be the variable name you use to access the bound object from Lua script. You can change this key to whatever string you prefer.
4. If the bound object is a GameObject, you can optionally select a component within it to bind to.

Note that you can bind to any Unity object, not just scene GameObjects. This includes things like Prefabs, Materials, TextAssets, etc.


# Using a global table

The bindings specified in a LuaBindings component are automatically registered as global variables in all LuaEnvironments in the scene at startup. 

This feature is very convenient when writing simple scripts, but for more complex scripts it can cause problems when you accidentally define another variable with the same name as a binding. If this is a problem for you, you can use the Table Name property to register bindings in a global table to add a degree of namespace safety.

For example, if your binding is called 'camera' and you've set Table Name to "myobjects", you would access the camera object like this:
```python
myobjects.camera
```

# Looking up members

The Member Info dropdown box allows you to quickly lookup properties and methods for any bound object. When you select a member, the Lua script needed to access it is displayed.

# Register Types option

In order to access a C# type from Lua, the type has to be registered with MoonSharp. When the Register Types option is selected, LuaBindings will do automatically register the types of bound objects and all public properties & methods that the type uses.


