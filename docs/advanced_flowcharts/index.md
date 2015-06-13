# Fungus Advanced - Flowcharts
A Unity scene can contain multiple Flowcharts, and commands can be executing simultaneously in different Flowcharts. In this section of the Fungus docs learn about multiple flowcharts, commands calling other blocks in the same or even another flowchart.

<!-- **************************************************** -->
## Executing Commands in another Block - in the current Flowchart
The Call Command tells Fungus to go and start executing the Commands in named Block. There are several ways to do this, we can tell Fungus to Stop execution completely in the current Block, and just pass control to named Block. We can also tell Fungus to go and completed all Commands in the named Block, and when they are finished, to then continue executing any remaining commands in the current Block. Finally, and perhaps the most complicated/sophisticated technique, we can tell Fungus to both started executing Commands in a named Block WHILE simultaneously continuing to execute remaining Commands in the current Block.

To pass control to another Block, and stop excuting Commands in the current Block, do the following:

1. (setup) If you have not already done so: Create a new scene, add a Fungus Flowchart to the scene, and select the Block in the Flowchart.

1. Rename this Block "Start".

1. Add to Block "Start" a Say Command with the Story Text "I am in Start".
<br>
![block start](./images/002_call_other_blocks/1_start.png "block start")
<br>
<br>

1. Add a new Block to your Flowchart named "Block2".

1. Add to Block "Block2" a Say Command with the Story Text "I am in Block2".
<br>
![block 2](./images/002_call_other_blocks/2_block2.png "block 2")
<br>
<br>

1. Add to Block "Block2" a Call Command, by choosing menu: ```Flow | Call```:
<br>
![flow call](./images/002_call_other_blocks/3_menu_call.png "flow call")
<br>
<br>

1. With this Call Command Selected, in the Inspector choose Block2 from the list of Blocks for property **Target Block**:
<br>
![call block menu](./images/002_call_other_blocks/4_call_block.png "call block menu")
<br>
<br>

1. Note: We will keep the default of **Target Flowchart** (None), which means the current Flowchart.

1. Note: We will keep the default of **Call Mode** Stop, which means that execution in the current Block (Start) will stop once execution of the called Block has begun.

1. You should now see an arrow in the Flowchart window, connecting Block "Start" with Block "Block2". This visually tells us (the game developer) that a Call or Menu Command is present inside Block "Start" that tells Fungus to execute commands in Block "Block2":
<br>
![arrow between blocks](./images/002_call_other_blocks/5_arrow.png "arrow between blocks")
<br>
<br>

<!-- **************************************************** -->
## Using multiple Flowcharts in a scene

For sophisticated and complex games you may wish to diving the logic for a scene into 2 different Fungus Flowcharts.

For example, you might have on Flowchart for maintaining the visuals for the users score and inventory, and a second Flowchart for the game narrative and action.

To use mutliple Flowcharts to a scene do the following:

1. (setup) If you have not already done so: Create a new scene, add a Fungus Flowchart to the scene, and select the Block in the Flowchart.

1. Rename this Block "Start Narrative".

1.

<!-- **************************************************** -->
## Calling a block in another Flowchart

