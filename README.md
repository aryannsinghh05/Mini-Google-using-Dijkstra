# 🚀 MINI GOOGLE MAPS

## 📌 Project Overview

This project is a **Smart Route Finder** that simulates a **mini Google Maps system**. It calculates the **shortest path between locations** like House, Mall, Park, Hospital, and College.

It not only finds the optimal route but also:

* Shows **step-by-step traversal**
* Compares **explored paths vs final chosen path**

---

## 🎯 Features

* 📍 Finds shortest distance between locations
* 🗺️ Navigation-like behavior
* 🔄 Shows explored vs optimal path
* ⚡ Fast backend computation

---

## 🛠️ Tech Stack

* Node.js
* Express.js
* Graph-based logic
* Dijkstra Algorithm

---

## 🧠 Algorithm Used: Dijkstra’s Algorithm

Dijkstra’s Algorithm is used to find the **shortest path from a source node to a destination node** in a weighted graph.

### 🔹 Why this algorithm?

* Ensures **optimal path**
* Works efficiently for **real-world routing**
* Used in **navigation systems**

---

## ⚙️ Backend Logic (Dijkstra Function)

A custom function is implemented in the backend that:

### 🔹 Takes:

* Source node
* Destination node
* Graph (locations + distances)

### 🔹 Performs:

* Tracks **minimum distances**
* Maintains **visited nodes**
* Stores **path traversal**
* Continuously updates shortest path

### 🔹 Key Idea:

At every step, choose the **node with minimum distance** and update its neighbors.

---

## 📊 Step-by-Step Example (Real Case)

### 🎯 Problem:

Find shortest path from **House → Hospital**

---

### 🔹 Given Connections (Weights)

* House → Mall = 3
* House → Park = 5
* House → College = 2
* Mall → Hospital = 4
* Mall → Park = 2
* Park → Hospital = 3
* Park → College = 3

---

### 🔹 Step 1: Initialize

```
House = 0  
Mall = ∞  
Park = ∞  
College = ∞  
Hospital = ∞  
```

---

### 🔹 Step 2: From House

```
Mall = 3  
Park = 5  
College = 2  
```

---

### 🔹 Step 3: Choose smallest → College (2)

Update neighbors:

```
Park = min(5, 2+3=5) → 5  
```

---

### 🔹 Step 4: Choose next → Mall (3)

Update:

```
Hospital = 3+4 = 7  
Park = min(5, 3+2=5) → 5  
```

---

### 🔹 Step 5: Choose next → Park (5)

Update:

```
Hospital = min(7, 5+3=8) → 7  
```

---

### 🔹 Step 6: Reach Hospital (7) ✅

---

## ✅ Final Output

* **Shortest Distance = 7**
* **Path = House → Mall → Hospital**

---

## 🔍 Traversal vs Final Path

### 🟡 Explored Paths

* House → College
* House → Park
* House → Mall

### 🟢 Final Chosen Path

* House → Mall → Hospital

---

## 🔄 Complete Project Flow

1. User selects source & destination
2. Request sent to backend (Express API)
3. Backend runs Dijkstra function
4. Calculates:

   * Shortest path
   * Traversed nodes
5. Sends response
6. Frontend displays:

   * Explored paths
   * Final shortest path

---

## 📡 API Example

```
POST /shortest-path
```

```json
{
  "source": "House",
  "destination": "Hospital"
}
```

---

## 📦 Future Improvements

* Real-time map visualization
* Traffic-based weights
* Priority queue optimization

---

## 👩‍💻 Contributors

* Aryan Singh 
* Contributor - Akshita Singh (created readme file)

---

## 💡 Conclusion

This project demonstrates how **Dijkstra’s Algorithm powers route-finding systems**, making navigation efficient and reliable.

---
