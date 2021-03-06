# Unity Test Tools

If you are using the [Unity Test Tools](http://u3d.as/65h), FungusLua is a powerful and fast way to create integration tests using Lua scripting.

# Example

1. Create a new test in the scene.
2. Add a LuaEnvironemnt (Tools > Fungus > Create > LuaEnvironment) and a LuaScript as children of the test object.
3. Set LuaScript to use the LuaEnvironment as its environemnt (this step is important when you have multiple tests in the scene).
4. In the LuaScript, use the check() function to assert whatever conditions you need for the test. At the end, call pass()

If any of the checks fail, then the test fails immediately.

# Lua Functions

```python
-- Checks if a condition is true
-- Lua has a built in assert function, so we called this check to avoid conflicting.
check(c, reason)

-- Pass an integration test
pass()

-- Fail an integration test
-- reason: Optional string explaining why the test failed.
fail(reason)
```
