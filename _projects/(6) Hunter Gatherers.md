---
name: Hunter Gatherers
tools: [C#, Unity, Multiplayer, Photon]
image: ../assets/img/projects/hunter_gatherers.png
description: A real-time multiplayer battle royal game, created during my GameDevelopment study, in which you try to survive on a island that is flooding. Your goal is to be the last tribe standing.
---

# Hunter Gatherers

Hunter Gatherers is a multiplayer real-time strategy game in which you try to survive on a island that is flooding. Your goal is to be the last tribe standing. You gather resources, place down your camp to rest and craft, and then pack it back up to outrun the flood.

<iframe width="560" height="315" src="https://www.youtube.com/embed/T92sDwTVitk"
		frameborder="0"
		allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
		allowfullscreen>
</iframe>

---

During the project my main job was to provide the multiplayer functionalities to the game. This included:
1. Connecting and joining rooms
2. Separated player properties
3. Raising multiplayer events
4. Synchonization of game objects
5. Pooling and raising of networking request

I wrapped all these functionalities into one big wrapper class to make switching multiplayer libraries a lot easier aswell.