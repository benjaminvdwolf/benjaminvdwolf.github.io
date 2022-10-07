---
name: Maze Generation
tools: [C#, Unity, Algorithms]
image: ../assets/img/projects/maze_generation.png
description: A project I started when I was looking for an intership to graduate as a GameDeveloper, receiving an application assignment from a company I was interested in.
---

# Maze Generation

---

A project I started when I was looking for an intership to graduate as a GameDeveloper, receiving an application assignment from a company I was interested in, asking me to create a maze using an algorithm of my choice in a short ammount of time.

<iframe width="560" height="315" src="https://www.youtube.com/embed/WdHMrPvfjlM"
		frameborder="0" allow="accelerometer; autoplay; clipboard-write; encryptedgyroscope; picture-in-picture" 
		allowfullscreen>
</iframe>

After handing in my entry I expanded on what I had originaly build, adding 9 new algorithms to create the maze making it a total of 10 and a user interface to manage options regarding the generation.

---

## Algorithms Used
- Generation
  - [Recursive Backtracking Algorithm](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Generators/RecursiveBacktrackingGenerator.cs)
  - [Aldous Broder Algorithm](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Generators/AldousBroderGenerator.cs)
  - [BinaryTree Algorithm](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Generators/BinaryTreeGenerator.cs)
  - [Kruskal's Algorithm](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Generators/KruskalGenerator.cs)
  - [Prim's Algorithm](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Generators/PrimGenerator.cs)
  - [Eller's Algorithm](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Generators/EllerGenerator.cs)
  - [Wilson's Algorithm](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Generators/WilsonGenerator.cs)
  - [Hunt And Kil Algorithm](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Generators/HuntAndKillGenerator.cs)
  - [Growing Tree Algorithm (prim variant)](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Generators/PrimsGrowingTreeGenerator.cs)
  - [Sidewinder Algorithm](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Generators/SidewinderGenerator.cs)

- Solving
  - [Recursive Backtracking Algorithm](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Solvers/RecursiveBacktrackingSolver.cs)
  - [DeadEndFilling](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Solvers/DeadEndFillingSolver.cs)
  - [WallFollower](https://github.com/Bvanderwolf/MazeGeneration/blob/main/Assets/Scripts/Solvers/WallFollowerSolver.cs)

## References
1. [James-Buck (The Bucklog) - Recursive Backtracking](https://weblog.jamisbuck.org/2010/12/27 maze-generation-recursive-backtracking)  
2. [James-Buck (The Bucklog) - Aldous-Broder](https://weblog.jamisbuck.org/2011/1/17/maze-generation-aldous-broder-algorithm)  
3. [James-Buck (The Bucklog) - BinaryTree](https://weblog.jamisbuck.org/2011/2/1/maze-generation-binary-tree-algorithm)  
4. [James-Buck (The Bucklog) - Kruskal](http://weblog.jamisbuck.org/2011/1/3/maze-generation-kruskal-s-algorithm)  
5. [James-Buck (The Bucklog) - Prim](http://weblog.jamisbuck.org/2011/1/10/maze-generation-prim-s-algorithm)  
6. [James-Buck (The Bucklog) - Eller](http://weblog.jamisbuck.org/2010/12/29/maze-generation-eller-s-algorithm)  
7. [James-Buck (The Bucklog) - Wilson](http://weblog.jamisbuck.org/2011/1/20/maze-generation-wilson-s-algorithm)  
8. [James-Buck (The Bucklog) - Hunt And Kill](http://weblog.jamisbuck.org/2011/1/24/maze-generation-hunt-and-kill-algorithm)  
9. [James-Buck (The Bucklog) - Growing Tree](http://weblog.jamisbuck.org/2011/1/27/maze-generation-growing-tree-algorithm)  
10. [James-Buck (The Bucklog) - Sidewinder](http://weblog.jamisbuck.org/2011/2/3/maze-generation-sidewinder-algorithm) 
11. [Wikipedia - Recursive Backtracking Algorithm](https://en.wikipedia.org/wiki/Maze_solving_algorithm#Recursive%20algorithm)  
12. [Wikipedia - DeadEndFilling](https://en.wikipedia.org/wiki/Maze_solving_algorithm#Dead-end_filling)  
13. [ProfessorRobertSolis - WallFollower](https://www.youtube.com/watch?v=yz0EOsUkwD4&t=0s&ab_channel=professorrobertsolis)