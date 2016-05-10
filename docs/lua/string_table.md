# String Table

LuaUtils provides support for simple text localisation. 

1. Define your language strings in a JSON file
2. Add a LuaEnvironment to your scene via Tools > Fungus > Create > LuaEnvironment 
3. In the LuaUtils component, set the String Table property to reference the JSON file.
4. Use the {$VarName} syntax to subsitute a localised string anywhere that string substitution is supported. e.g. in a Lua script:

```lua
say("{$hello_world}")
```

You can use the {$VarName} syntax anywhere that variable subsitution is supported. This includes the Say and Menu commands in a Flowchart, Fungus Character names, the Debug Log command, etc.

You can also extend the Fungus string substitution system with your own components. Implement the StringSubstituter.ISubstitutionHandler interface in a Monobehavior subclass and then return the modified string from SubstituteStrings().

# JSON Format

This is an example of the JSON format for the string table. To use this localised string, you would use the {$hello_world} tag.

```json
{
	"hello_world" : {
		"en" : "Hello world!",
		"fr" : "Bonjour le monde!",
		"de" : "Hallo Welt!"
	}
}
```

# Lua Functions

These Lua functions are available for working with the string table.

```lua
-- Set active language for string table
setlanguage(languagecode)

-- Get a named string from the string table
getstring(key)

-- Substitutes variables and localisation strings into a piece of text
-- e.g. v = 10, "Subbed value is [$v]" => "Subbed value is 10"
sub(text)
```

