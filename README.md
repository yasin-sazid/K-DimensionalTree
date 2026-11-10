# K-Dimensional Tree

An interactive Java implementation of a k-d tree for integer coordinate vectors. The project explores multidimensional search by organizing points into a binary tree whose comparison axis changes with depth.

## Capabilities

- Choose the number of dimensions when starting the program.
- Insert coordinate vectors through a console menu.
- Search for an exact point and report its location in the tree.
- Print the tree structure with root, child, and level information.

## How it works

`KDTree` owns the root and implements insertion, search, and printing. `KDTreeNode` stores a point together with its parent, left child, right child, and level. The node's level determines the active coordinate for successive partitions, connecting an ordinary binary-tree structure to multidimensional comparisons.

[Main.java](KDTree/src/mainPackage/Main.java) handles user interaction independently of the tree classes.

## Run

With a JDK installed, run from the repository root:

```bash
javac -d /tmp/kdtree-classes KDTree/src/mainPackage/*.java KDTree/src/otherPackage/*.java
java -cp /tmp/kdtree-classes mainPackage.Main
```

Enter a positive dimension, then select **Insert**, **Search**, **Print**, or **Exit**. Each point should contain the selected number of integer coordinates. For example, in two dimensions, insert `(3, 6)`, `(8, 2)`, and `(5, 4)`, then search for one of those points and inspect the printed hierarchy.

## Technical focus

Dimension-independent point storage, depth-dependent comparisons, explicit parent/child relationships, and a console driver make the central data-structure decisions visible and easy to study.
