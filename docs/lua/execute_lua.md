# Execute Lua Command

This command allows you to embed a Lua script to be executed as part of a command sequence in a Block. You can provide an optional LuaEnvironment to use for the execution, but if none is provided then one will be create automatically. You can also choose to store the return value from the Lua script in a Flowchart variable.

#  Evaluating expressions

The Fungus If command can only compare 2 variables at a time. For more complex expressions, you can use Lua to do the evaluation and store the result in a Flowchart variable.

1. Add a Flowchart object (Tools > Fungus > Create > Flowchart). Add some variables to the Flowchart.
2. Add a LuaBindings object (Tools > Fungus > Create > LuaBindings)
3. Add a binding to the Flowchart gameobject, and select the Flowchart component.
4. In the Flowchart, add an ExecuteLua command in a block to evaluate a complex expression. Store the return value in a Boolean Flowchart variable.
5. Add an If command which checks the value of the Boolean variable.

In the Execute Lua command, you can use the getvar() function to get any Flowchart variables to be used in the expression. 
Note: getvar() returns a reference to the Fungus variable object. To access the value of this variable use the .value property.

# Example

Here's an example of evaluating a complex expression involving 3 variables.

```python
local v1 = getvar(flowchart, "Var1")
local v2 = getvar(flowchart, "Var2")
local v3 = getvar(flowchart, "Var3")

return (v1.value == v2.value or v3.value == 5) 
```
