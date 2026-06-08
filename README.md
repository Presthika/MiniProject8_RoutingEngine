# MiniProject8_RoutingEngine

# 🌐 Network Routing Engine

A C++ graph-based routing engine that finds paths through a network while respecting minimum bandwidth constraints.

Built for EECE 2140: Computing Fundamentals for Engineers at Northeastern University.

---

## How it works

- Loads a network topology from a text file (nodes + edges + bandwidth)
- Uses **DFS (Depth-First Search)** to find a valid path between two nodes
- Filters paths by minimum bandwidth requirement
- Built with **smart pointers** (`unique_ptr`) for safe memory management

---

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

---

## Files

| File | Description |
|---|---|
| `RoutingEngine.cpp` | Main source code |
| `network.txt` | Sample network topology |

---

## Tech Stack

- C++
- Smart pointers (`unique_ptr`)
- DFS algorithm
- File I/O

---

## Course

Northeastern University · EECE 2140 · Spring 2026
