# Recipes
Follow these steps to get up and started with Fungus quickly. Then learn more about what Fungus can do and how to do it from the other documentation pages and videos.

## Opening and docking the Flowchart window
You'll need the Fungus Flowchart window when working with Fungus. Open and dock this window somewhere handy by following these steps:

1. Choose menu: ``Tools | Fungus | Flowchart Window``
<br>
![Menu open Fungus window](/images/quickstart/002_docking/1_menu.png "Menu open Fungus window")
<br>
<br>

2. Drag-and-drop the Flowchart window to the location you wish to dock it:
<br>
![Drag Fungus window](/images/quickstart/002_docking/2_window.png "Drag Fungus window")
<br>
<br>

3. The Flowchart window is now docked and part of your Unity window layout:
<br>
![Docked Fungus window](/images/quickstart/002_docking/3_docked.png "Docked Fungus window")

## Finding the example folders and scene files
Two folders are created when you install Fungus, the Fungus features themeslves (in folder 'Fungus') and a set of examples (in folder 'FungusExamples').

Examples include Drag and Drop, Sherlock and Fungus Town:
<br>
![Fungus Examples](/images/quickstart/004_examples/1_examples.png "Fungus Examples")
<br>

You can use the left-hand side of the Unity Project window to explore each example folder:
<br>
![Fungus Examples Project window](/images/quickstart/004_examples/3_project_window.png "Fungus Examples Project window")
<br>

Alternatively, you can 'filter' the Project view to show all scenes (and no other files) by clicking the scene filter icon to the right of the search bar:
<br>
![Fungus Examples Project window filter scenes](/images/quickstart/004_examples/2_filter_scenes.png "Fungus Examples Project window filter scenes")
<br>

You can cancel the filter by clicking the 'x' in the search bar:
<br>
![Fungus Examples Project window filter scenes cancel](/images/quickstart/004_examples/4_filter_scenes_cancel.png "Fungus Examples Project window filter scenes cancel")
<br>

## Loading and playing the example scenes
To **load** an example scene, double click the desired example's scene object in the Projet window, and the scene should load. For example, this screenshot shows the scene and Flowchart windows when the DragAndDrop example scene has been loaded:
<br>
![Fungus Examples Drag Drop](/images/quickstart/004_examples/5_drag_drop.png "Fungus Examples Drag Drop")
<br>

To **run** the currently loaded scene (i.e. to entery **Play-mode**), click the Unity 'play' triangle button at the center top of the Unity application window, and then do whatever makese sense in that scene (e..g click/type text/drag-and-drop objects etc.!):
<br>
![Unity play scene](/images/quickstart/004_examples/6_drag_running.png "Unity play scene")
<br>

Note: you click the 'play' button a second time to end **Play-mode**.

## Changes made during playmode don't persist
As with all Unity projects, you can **change** the properties of gameObjects while a scene is running, but these changes are 'ephemeral' - they only last while the scene is running. As soon as you end play mode the properties of all objects in the Hierarchy will revert to those saved in the Scene file.

This makes it easy to 'tweak' values of objects in **Play-mode**, and then when the desired behaviour is achieved, those values can be set for the saved scene properties.

Values set when Unity is in **Edit-mode** will be saved when you saved your scene (``CTRL-S`` / ``Command-S``, or menu: ``File | Save Scene``).

## Change your preferences to highlight Play-mode
Sometimes we can forget we are in Unity **Play-mode**, and then make changes to Hierarchy gameObject values that are then 'fogotton' when we do stop playing the scene. A good way to avoid this problem is to to set a 'tint' to the Unity editor to make it visually very clear to us when we are in **Play-mode**. To add a tint to **Play-mode** do the following:

1. Open the Unity preferences dialog by choosing menu: ```File | Preferences ...```

2. Select the ```Colors``` preferences, and choose a light colored tint (we chose a light green in this case):
<br>
![Unity preferences dialog](/images/quickstart/005_highlight_play_mode/1_prefs_tint.png "Unity preferences dialog")
<br>
<br>

3. Close the dialog (changes are saved automatically).

4. When you next enter **Play-mode** you'll see most of the Unity Editor windows turn green (apart from the Game and Flowchart windows):
<br>
![Unity Play Mode tinted](/images/quickstart/005_highlight_play_mode/2_green_play_mode.png "Unity Play Mode tinted")
<br>

## Creating, naming and saving a new scene from scratch
To create a new scene in Unity do the following:

1. Choose menu: ```File | New Scene```

2. Note: if you have any unsaved changes for the current scene you need to either save or abandon them before a new scene can be created.

3. You should now have a shiny new scene, with a Hiearchy containing just one gameObject, a Main Camera. The new scene will have been give the default name "Untitled", which you can see in the title of the Application window:
<br>
![New Scene](/images/quickstart/006_new_scene/1_default.png "New Scene")
<br>
<br>

4. Good practice is to save your scene (in the right place, with the right name), before creating your work in the scene. Let's save this scene in the root of our project "Assets" folder, naming it "demo1". First choose menu: ```File | Save Scene As...```

5. Choose the location and name (we'll choose folders "Assets" and scene name "demo1"):
<br>
![Save Scene As dialog](/images/quickstart/006_new_scene/2_save_as.png "Save Scene As dialog")
<br>
<br>

6. Once you have successfully saved the scene you should now see the new scene file "demo1" in your Assets folder in the Project window, and you should also see in the Application window title that you are currently editing the scene named "demo1":
<br>
![Editing newly saved scene](/images/quickstart/006_new_scene/3_saved_scene.png "Editing newly saved scene")
<br>

## Menu: Tools | Fungus
The core Fungus operations are available from the Unith ```Tools``` menu.

Choose menu: ```Tools | Fungs``` to see the options availble:
<br>
![Fungus Tools menu](/images/quickstart/007_tools_menu/3_fungus_tools.png "Fungus Tools menu")
<br>

As can be seen, there are 2 submenus, ```Create``` and ```Utilities```, plus the ```Flowchart Window``` action (which reveals the window if already open, or opens a new window if the Flowchart window was not previously opened).

### Menu: Tools | Fungus | Create
The Fungus Tools ```Create``` submenu offers the following actions:
<br>
![Fungus Tools Create menu](/images/quickstart/007_tools_menu/1_tools_create.png "Fungus Tools Create menu")
<br>


### Menu: Tools |  Fungus | Utilities
The Fungus Tools ```Utilties``` submenu offers the following actions:
<br>
![Fungus Tools Utilties menu](/images/quickstart/007_tools_menu/2_tools_utilities.png "Fungus Tools Utilities menu")
<br>

## Create a Flowchart
To create a Fungus Flowchart do the following:

1. Choose menu: ```Tools | Fungus | Create Flowchart```
<br>
![menu create Flowchart](/images/quickstart/008_create_flowchart/1_tools_create.png "menu create Flowchart")
<br>
<br>

2. A new **Flowchart** gameObject should appear in the Hierarchy window.
<br>
![new Flowchart gameobject](/images/quickstart/008_create_flowchart/2_flowchart_gameobject.png "new Flowchart gameobject")
<br>
<br>

3. Select the **Flowchart** gameObject in the Hierarchy window, and you'll see the **Flowchart's** properties in the Inspector Window:
<br>
![Flowchart properties](/images/quickstart/008_create_flowchart/3_flowchart_properties.png "Flowchart properties")
<br>
<br>

4. If you have not already displayed the Flowchart Window, you can do so by clicking the Flowchart Window button in the Inspector.

5. As you can see, when a new Flowchat is created a single command Block named "New Block" is automatically created, with the Event handler "Game Started" (so it will start executing Fungus commands as soon as the scene goes into **Play Mode**).

## Flowchart Block property viewing and editing
Let's change the name of the default command Block of a new Flowchart in the Flowchart window to "hello". Do the following:

1. Create a new Fungus Flowchart (if you haven't already done so).

2. Click to select the Block in the Flowchart window (when multiple blocks are present, the selected one gets a green highlight border).

3. In the Inspector change the text for the Block Name property to "hello". You should see the Block name change in the Flowchart window:
<br>
![rename Block](/images/quickstart/009_rename_block/1_rename.png "rename Block")
<br>

## Add a Say command
To add a "Say" command to a block do the following:

1. Ensure the block is selected, and you can see its properties in the Inspector.

2. Click the Plus button in the bottom half of the Inspector window, to add a new Command to the Block's properties:
<br>
![new command button](/images/quickstart/010_say_command/1_plus.png "new command button")
<br>
<br>

3. Choose menu: ```Narrative | Say```:
<br>
![add Say command](/images/quickstart/010_say_command/2_narrative_say.png "add Say command")
<br>
<br>

4. Since this Block only has one Command, that command is automatically selected (shown with a green highlght).

5. In the "Story Text" textbox in the bottom half of the Inspector window type in "hello Fugus world":
<br>
![story text](/images/quickstart/010_say_command/3_hello_fungus_world.png "story text")
<br>
<br>

6. Run the scene, and see Fungus create a dialog window, and output the text contents of your Say command:
<br>
![story text output](/images/quickstart/010_say_command/4_scene_running.png "story text output")
<br>
<br>

## Add 2 menu commands
Let's modify our "hello" Say command above to ask a tricky mathematical quesiton, and demonsrate the Menu command by offering the user a choce been "correct' and "incorrect" answers.  Menu commands transfer control to another block - so we'll need to add 2 new blocks to correspond to the 2 answers.
Do the following:

1. Edit your Say command, change the **Story Text** to ask the question: "Is 2 + 2?".

2. Uncheck the "Wait For Click" checkbox (this is so we see the menu options immediately after the Say command has displayed the question):
<br>
![maths say command](/images/quickstart/011_menu_maths/2_edited_say.png "maths say command")
<br>
<br>

3. Create a new Block, named "Correct" which contains a **Say** command with the text "Well done, you are very mathematical!". Click the plus-sign button in the Flowchart window to add a new Block to the Flowchart, rename it "Correct" and then add that Say command:
<br>
![correct block](/images/quickstart/011_menu_maths/1_correct_block.png "correct block")
<br>
<br>

4. Select the "hello" block, and add a Menu command by clicking the plus-sign add Command button in the Inspector and then choosing menu: ```Narrative | Menu```.
<br>
![add menu command](/images/quickstart/011_menu_maths/6_add_menu.png "add menu command")
<br>
<br>

5. With this new Menu command selected (green) in the top half of the Inspector window, set the **Text** to "Yes" and the **Target Block** to your new "Correct" block:
<br>
![menu command](/images/quickstart/011_menu_maths/4_menu_correct.png "menu command")
<br>
<br>

6. You should now see how the 'flow' of commands can change from Block "hello" to Block "correct" in the Flowchart window:
<br>
![flow between blocks in Flowchart](/images/quickstart/011_menu_maths/5_connected_blocks.png "flow between blocks in Flowchart")
<br>
<br>

7. Add a second new Block named "Wrong", containing a Say command with text "Bad luck, perhaps consider a non-mathematical career path..."
<br>
![block for wrong answer](/images/quickstart/011_menu_maths/7_wrong_block.png "block for wrong answer")
<br>
<br>

8. Now we need to add another Menu command to our "hello" block, offering the user the "No" answer to our maths question, and passing control to Block "Wrong" if they disagree that 2 + 2 = 4. Select the "hello" block, and add a Menu command. With this new Menu command selected (green) in the top half of the Inspector window, set the **Text** to "No" and the **Target Block** to your new "Wrong" block.

9. You should now see in the Flowchart window how block "hello" can pass control to either block "Correct" or Block "Wrong" - depending on which menu answer the user selects.
<br>
![block connected to 2 others](/images/quickstart/011_menu_maths/8_three_block_menu.png "block connected to 2 others")
<br>
<br>

10. Run the scene, and you should see the Say question appear at the bottom of the screen, and also the two Menu buttons "Yes" and "No" in the middle of the screen. Clicking "Yes" then runs the "Correct" Block's commands, and clicking "No" runs the "Wrong" block's commands:
<br>
![menu running](/images/quickstart/011_menu_maths/9_menu_running.png "menu running")
<br>
<br>

<br>
![correct screen](/images/quickstart/011_menu_maths/10_correct.png "correct screen")
<br>
<br>


<br>
![wrong screen](/images/quickstart/011_menu_maths/11_wrong.png "wrong screen")
<br>
<br>

[Unity3D.com]: http://www.unity3d.com
[Unity3D.com/get-unity]: http://unity3d.com/get-unity
[FungusGames.com]: http://www.fungusgames.com
