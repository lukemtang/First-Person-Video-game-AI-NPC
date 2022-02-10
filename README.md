
<h1><b>First-Person Shooter Video Game with Reinforcement-Learning Trained Game AI</b></h1>
<body>
  <h2> What is this project?</h2>
  <p>
    This repo containes the source files and runnable builds of my MSc Computer Science project, produced during August and September 2021. The primary goal of the project is to build an AI NPC, with behaviour trained purely through reinforcement learning.
  </p>
    <h2> What files are there?</h2>
   <p>
     Within 'CS_Project_4.26' you will find the entire source project files for the build. In order to open the Unreal Project files, you will need to download and install the Unreal engine, version 4.26 from Epic Games. You can then move the project folder to your local Unreal Projects folder. Open the project by double clicking on 'CS_Project_426/CS_Project_426.uproject'.
   </p>
   <h2> How to access trained models</h2>
   <p>
      Unfortunately, I was not able to export the project to a runnable file. However, it is forunately still possible to access and run the trained models to validate my work.
    <br><br> 1. Install Unreal Engine
     <br> 2. Move 'CS_Project_4.26' to documents/Unreal Projects
     <br> 3. Download any of the trained models you would like to run.
     <br> 4. Move these folders (still zipped!) to: C:\Users\<i>username</i>\AppData\Roaming
     <br> 5. Open the project in Unreal engine and open the 'Enemy1_AI_Controler' blueprint in the content browser: Content/MindMaker/MindmakerStarterDRLContent/Assets/MindmakerDRLStarterContent/Enemy1_AI_Controler
     <br> This is the blue print for the AI controller that controls the agent.
     <br> 6. Go to the Event Graph tab in the middle of the screen. In the right-middle of the blueprint there is an end node called 'Launch Mind Maker')
     <br> 7. On this node, check 'Load Pre Trained Model', and uncheck 'Save Model after Training'. Ensure the variable 'Num Training Episodes' is set to 0. 'Num Eval Episodes' can be set to a value of your choosing. This value determines how long the agent acts for. I reccomend a value of 1000 to 5000 for a few minutes of action. These values can be changed by clicking on the teal coloured box with their names on and then editing the value on the right-hand 'details' column
     <br>This loads a pre-trained model and does not train it.
     <br> 8. In the 'Save/ Load Model Name' enter the names of one of the models listed below. this tells the programme which model to retrieve from the roaming folder they were placed in earlier.
     <br> 9. Click compile in the top left of the blueprint. Press Play along the top ribbon.
     <br> 10. The agent should now begin to act according to its model.     
     <br> The following screenshot illustrates the instructions above, showing the mentioned buttons and text field https://user-images.githubusercontent.com/71343952/135500342-60a32bf0-1925-4125-95fe-756c2c705931.png

   </p>
  <h2> Description of models</h2>
  <p>
    StationaryDQN - Agent moves to the players location if the player does not move from the starting spot. Trained with DQN for 3000 iterations
    <br> Stationary_PPo2 - Agent moves to the players location if the pplayer does not move from the starting sport. Trained with PPO2 for 3000 iterations
    <br> MovingPPO2 - Agent should move towards the player, even if the player moves about. Trained with PPO2 for 5000 iterations.
  </p>
    <h2> Planned future additions</h2>
  <p>
    - Gameplay features beyond just training the agent; linetrace damage system from the player's weapon, NPC respawns, score and rounds, etc.
    <br>-  Cosmetic additions; textures and animations.
  </p>

</body>
