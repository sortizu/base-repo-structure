## Studio Base Project Template
This is the base repository template for our studio's future Godot 4.x projects.

### Architecture
We use a custom Entity-Component-Controller (ECC) architecture. The main idea here is to use the minimum amount of folders possible and keep components highly reusable across different games.

/entities: The main game actors. An entity is basically a blank page, It doesn't have hard logic by itself.

/components: Scripts with a single responsibility. They give attributes and functionalities to the entities.

/controllers: Scripts designed to orchestrate and manage multiple components at the same time.

/scenes: Generic scenes, prefabs, and UI that don't classify as entities.

/levels: The actual maps or rooms for the game.

Note: All assets (sprites, audio) related to a specific entity are saved directly inside that entity's folder (e.g., /entities/player/). They don't have a separate folder globally. This makes it easier to find files based on the entity that owns them and reduces the total amount of folders.

### Setup & Requirements
Important: We use Git LFS to handle heavy binary files like .png sprite sheets and .wav audio loops.
