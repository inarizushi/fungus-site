# LuaStore

A common issue when working with multiple scenes in Unity is how to persist variable values from one scene to the next. 

The Lua Store component provides an easy way to do this when using Lua Scripting. A shared global table called ‘store’ is bound in every Lua Environment in the scene. This global table persists between scene loads, which  means you can set a variable like ‘store.speed = 2’ in one scene, load another scene, then do ‘print(store.speed)’ and the value will still be 2.

# Example

1. Add a LuaStore to the first scene in your game (Tools >Fungus > Create > LuaStore). 
2. Set a variables in the store in Lua, e.g. store.name = "John"
3. Load another scene, e.g. using the Load Scene command in Fungus
4. Get the same variable from the store, e.g. print(store.name)