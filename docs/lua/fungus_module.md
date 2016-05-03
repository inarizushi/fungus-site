# Fungus Module

This Lua module provides handy functions for working with Lua, Unity and Fungus. 

In this page we cover some of the more generic functionality in the module, other major features are described elsewhere in the documentation.

# Inspecting Lua objects

You can use Lua's built in print() function to get a basic description of any object printed to the console. When you want to get a more detailed description of an object, use inspect().

```python
-- Prints a short description of object v
print(v)

-- Prints a summary of object v in a human readable format.
inspect(v)
```

## Running Unity coroutines

When you bind to a C# component using Lua Bindings, you can access any public method in the class. If a method returns IEnumerator then that method can be executed [as a coroutine](http://docs.unity3d.com/Manual/Coroutines.html), which is a powerful way to run asynchronous code. 

The runwait() function allows you to call a C# coroutine method from Lua which may take multiple frames to finish its work, and then carry on with the rest of the Lua code once that C# method has finished executing. This is how the say() function works for example.

This is the list of available functions for waiting and working with coroutines.


```python
-- Waits for a number of seconds
wait(duration)

-- Waits until the Lua function provided returns true, or the timeout expires.
-- Returns true if the function succeeded, or false if the timeout expired
waitfor(fn, timeoutduration)

-- Run a C# coroutine and continue execution of Lua script
run(<C# coroutine IEnumerator object>)

-- Run a C# coroutine, wait until it completes, then continue execution of Lua script
runwait(<C# coroutine method IEnumerator object>)
```

## Globals vs Table mode

The Fungus module can be used in two modes.  In globals mode (the default), all the module functions are mapped to global functions. This allows for convenient access to the module methods, but it runs the risk that you might accidentally declare a variable with the same name.

```python
-- sub is a function in the Fungus module, mapped to a global variable
sub("a string")
```

In table mode, all the Lua module functions are accessed through a global table name, which gives a degree of namespace safety at the cost of more typing. Both ways are equivalent, so it's just a matter of personal preference which you want to use.

```python
fungus.sub(“a string")
```