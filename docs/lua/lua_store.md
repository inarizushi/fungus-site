# LuaStore

A common issue when working with multiple scenes in Unity is how to persist variable values from one scene to the next. 

The Lua Store component provides an easy way to do this when using Lua scripting. A shared global table called ‘store’ is bound in every Lua Environment when the scene starts. This global table persists between scene loads, which means you can set a store variable in one scene, load another scene, then access the store variable and it will still retain the value you set earlier.

# Example

- Add a LuaStore to the first scene in your game (Tools >Fungus > Create > LuaStore). 
- Set variables in the store in Lua, e.g. 

```lua
store.name = "John"
```

- Load another scene, e.g. using the Load Scene command in Fungus
- Get the same variable from the store, e.g.

```lua
print(store.name) -- prints "John"
```