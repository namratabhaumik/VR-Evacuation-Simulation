VR Evacuation Simulation
========================

Overview
--------

The **VR Evacuation Simulation** is a multi-disciplinary research-driven project developed using Unity3D. It aims to analyze pedestrian behavior and player decisions during emergency evacuation scenarios, such as fire evacuations, within a virtual cityscape of Halifax, NS, Canada. The simulation leverages VR technology to create immersive evacuation scenarios that help understand crowd dynamics and enhance safety protocols.

Game Flow
---------

The game begins with the player facing a burning building directly across the road. As the player starts, pedestrians begin evacuating from the nearby building. These pedestrians walk in various directions at different speeds, simulating the chaos of a fire evacuation. The player's task is to follow a group of pedestrians to evacuate the area safely.

- The player can move by following pedestrians, who will guide them towards safety.

- The player can be guided by either **evacuation signs** or **pedestrian voices** that are audible through the VR headset, depending on the scenario.

- The player is considered safe once they reach a **bus stop**, either with or without a bus present. This marks the safe evacuation destination.

The game will stop once the player reaches the marshal point (the exit point, marked by the bus stop). In some cases, the player may not immediately notice the signs and must actively search for them.

There are **12 different scenarios** in the game, each designed with unique conditions. These scenarios are detailed in the attached Excel sheet named **SP_VR_evacuation_updated** in the Sheet 2 of it. Each scenario presents different challenges for the player to navigate, from finding evacuation routes to avoiding other pedestrians.

Features
--------

-   **Realistic Pedestrian Behavior:**

    -   Pedestrians navigate predefined waypoints.
    -   Collision avoidance with other pedestrians and the player using Unity's **CharacterController**, **Rigidbody**, and **Colliders**.
    -   Dynamic group-based pedestrian logic with varying speeds and destinations.
-   **Player Dynamics:**

    -   Player movement integrates VR controllers and head bobbing for realism.
    -   Two player types: Disable the one not using while playing.
        1.  **Normal Player**: Named as XR Origin (XR Rig). Uses thumbsticks or buttons for movement.
        2.  **Wheelchaired Player**: Named as Wheelchaired Player. Moves only forward or backward using buttons and must not use thumbsticks for lateral movement.
    -   Choice-based evacuation paths tracked and analyzed.
-   **Data Collection:**

    -   Tracks and logs:
        -   Game duration.
        -   Total distance traveled.
        -   Chosen evacuation point.
        -   Distance from destinations upon completion.
    -   Saves data in **CSV format** in the file named **NormalPlayerGameData.csv** for normal player and **WheelchairPlayerGameData.csv** for the wheelchaired player for further analysis.
-   **Fire and Emergency Simulation:**

    -   Simulates fire scenarios with visual and auditory cues.
    -   Includes speaking pedestrians and evacuation signs (in specific scenarios).
-   **Dynamic VR Environment:**

    -   A detailed cityscape modeled in SketchUp and imported into Unity.
    -   Includes static assets like trees, buses, and fire with audio effects.

Technologies Used
-----------------

-   **Unity3D (2022.3.46f1):** Game engine for 3D simulations and VR development.
-   **Oculus Quest 3:** VR headset for immersive interaction.
-   **SketchUp:** For creating and importing cityscape models.
-   **C#:** Scripting language for game logic.
-   **Audio Tools:** For fire and voice effects in the simulation.
-   **Git:** Version control.

Research Goals
--------------

1.  **Behavioral Analysis:** Understand how pedestrians react during evacuations.
2.  **Evacuation Efficiency:** Identify bottlenecks and optimize evacuation strategies.
3.  **Safety Enhancements:** Design safer environments and emergency protocols.
4.  **Training Applications:** Provide VR-based training for emergency responders and planners.

Pre-requisites
--------------

Before starting the project, ensure the following are prepared:

1\. **Meta Quest 2 Setup**  

   - Install the Meta Quest app on your PC.  

   - Connect and set up the Meta Quest 2 following the official [Meta Quest Setup Guide](https://www.meta.com/help/quest/). Details are given on their documentation of how to set up the VR headset, right and left sensors and the hand controllers (right and left).

   - Try to play any VR game from the Meta Quest Link app to check if the controllers and headset are working fine.

2\. **SketchUp Model Preparation**  

   - The city model used in this project was built in SketchUp, requiring collaboration with a student from Urban Design field for over a month.   

   - The model includes streets, buildings, sidewalks, trees, buses and designated evacuation points (denoted by bus stops).  

   - The model was exported to a Unity-compatible format such as `.fbx`.

   - The model can be found under the **Sketchup** folder within the **Assets** folder.

   - One model has evacuation signs on the pavements that the pedestrian game objects and the player himself will follow to evacuate and the other one doesn't.

3\. **Unity 3D Project Setup**  

   - Install Unity 2022.3.46f1 or a compatible version.  

   - Create a new Unity 3D project.  

   - Install the required VR packages via Unity Package Manager:  

     - XR Interaction Toolkit  

     - Oculus Integration  

     - OpenXR Plugin  

   - Import the SketchUp model into the project.  

   - Set up an XR Origin (XR Rig) for VR movement and interaction.  

   - Test the VR environment to ensure compatibility with Meta Quest 2.

How to Run
----------

1.  Clone the repository:

    ```
    git clone https://github.com/your-username/vr-evacuation-simulation.git

    ```

2.  Open the project in **Unity (2022.3.46f1)**.
3.  There are 12 different scenarios in the **Scenarios** folder under **Assets**. Double click on any scene to load it.
4.  Connect your **Oculus Quest 3** headset.
5.  Play the simulation using the Oculus platform.

**Screenshots**
----------

![image](https://github.com/user-attachments/assets/93171a14-f6cf-4b4c-8270-f290e0c544e7)
![image](https://github.com/user-attachments/assets/f1360a5d-0c64-404f-bacf-b94e1018b029)
![image](https://github.com/user-attachments/assets/651d5951-df81-40fa-9868-73c70bffa0da)
![image](https://github.com/user-attachments/assets/fd8141fa-f74c-45c9-af02-b26db747869e)
![image](https://github.com/user-attachments/assets/abbc3990-11a8-473d-a865-1e4dc7561009)
![image](https://github.com/user-attachments/assets/44125ddd-6d33-492d-97ef-5d7bcfe2ea91)
![image](https://github.com/user-attachments/assets/198c17fe-713d-485c-ae4b-415775209bbc)
![image](https://github.com/user-attachments/assets/08335909-46b5-4877-b513-d9692663c0ea)



Future Steps
------------

-   Expand scenarios to include more complex evacuation routes and obstacles.
-   Optimize performance for larger pedestrian groups.
-   Implement multiplayer functionality for simultaneous user interaction.

License
-------

This project is licensed under the [MIT License](https://chatgpt.com/c/LICENSE).

Acknowledgments
---------------

-   Research mentors and collaborators.
-   Open-source tools and Unity Asset Store contributors.
