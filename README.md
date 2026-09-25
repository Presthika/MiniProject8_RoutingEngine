# Network Routing Engine

A C++ graph-based routing engine that finds a path between two nodes while meeting a minimum bandwidth requirement, built for EECE 2140: Computing Fundamentals for Engineers at Northeastern University (Spring 2026).

## How it works

- Loads a network from a text file where each line is an edge: `from to bandwidth`
- Uses depth-first search (DFS) to find a path to the destination
- Skips any link with less bandwidth than the minimum requested
- Stores nodes with smart pointers (`unique_ptr`) for automatic memory management

## Example output

```
Network Topology:
Node 0: (to: 1, bw: 100) (to: 2, bw: 50)
Node 1: (to: 2, bw: 30) (to: 3, bw: 100)

Finding paths:
Path Found (min BW >= 50): 0 -> 1 -> 3 -> 5
Path Found (min BW >= 100): 0 -> 1 -> 3 -> 5
No path found from 0 to 5 with min BW >= 200
```

## How to run

Run from the repo folder so the program can find `network.txt`:

```bash
clang++ -std=c++17 RoutingEngine.cpp -o routing
./routing
```

## Files

| File | Description |
|---|---|
| `RoutingEngine.cpp` | Source code |
| `network.txt` | Sample network topology |

## Author

Presthika Vijaykumar
