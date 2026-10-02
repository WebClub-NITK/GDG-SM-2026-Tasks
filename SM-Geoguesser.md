# Silicon Maze: Multiverse Recon

Mentors: [Harshith Vellapha](https://github.com/harshithv25) ([+91 9480090828](https://wa.me/919480090828)), [Mayank](https://github.com/M4yankkkk) ([+91 9915172290](https://wa.me/9915172290))

**The multiverse is collapsing!** Inspired by the reality-bending events of *Avengers: Doomsday*, this task challenges you to build **Multiverse Recon** — a web-based location guessing game. Players are dropped into a randomly selected street-view or image-based location from across the globe (or the multiverse). To stabilize the timeline, they must identify their exact coordinates by placing a marker on an interactive world map.

This task focuses primarily on **front-end development, API integration, geospatial calculations, and interactive UI/UX**, without requiring a complex backend or database.

---

## Task 1: The Observation Deck (UI & Map Setup) (Total: 50 pts)

### Subtask 1.1 – Location Viewer (25 pts)

Create a responsive web interface to display the current anomaly to the user.

* Implement a location viewer that displays a street-view panorama or a high-quality location image.
* Ensure the layout is clean, thematic (multiverse/Avengers theme), and accessible on both desktop and mobile devices.
* Include an optional first-time game tour/walkthrough that introduces the main game interface and can be skipped by the player.



### Subtask 1.2 – Interactive Nexus Map (25 pts)

Integrate an interactive map for players to pinpoint their location.

* Embed a clickable world map (using libraries like Leaflet, Mapbox, or Google Maps).
* Allow the user to place a single, movable marker on the map to represent their guess.

---

## Task 2: Timeline Stabilization (Core Logic) (Total: 60 pts)

### Subtask 2.1 – Anomaly Generation (20 pts)

Build a system to select random locations for each round.

* Randomly select locations from a predefined list of latitude/longitude coordinates or via a third-party mapping API.
* Ensure the selected location seamlessly updates the Location Viewer created in Subtask 1.1.

### Subtask 2.2 – Convergence Calculation (40 pts)

Implement the core geospatial math required to evaluate the player's guess.

* Write a function to calculate the exact distance (in kilometers or miles) between the actual location's coordinates and the player's guessed marker.
* *Hint: Look into the Haversine formula for calculating distances between two points on a sphere.*

---

## Task 3: The TVA Assessment (Scoring & Progression) (Total: 50 pts)

### Subtask 3.1 – Scoring System (25 pts)

Create a fair and rewarding scoring algorithm.

* Award points inversely proportional to the distance of the guess (i.e., closer guesses yield higher points).
* Establish a maximum point threshold per round and a maximum distance threshold where zero points are awarded.

### Subtask 3.2 – Multi-Round Gameplay & Results (25 pts)

Manage the application state across a full game session.

* Implement a standard game loop consisting of 5 distinct rounds.
* Track and display the cumulative score as the player progresses.
* Create a **Final Results Screen** that displays the total score, a visual summary of all guesses versus actual locations, and a "Play Again" button to restart the loop.

---

## Task 4: Multiversal Anomalies (Bonus Features) (Total: 20 pts)

### Subtask 4.1 – Advanced Mechanics (20 pts)

Push the boundaries of the multiverse by adding optional, advanced features to your game. Implementing one or more of these will earn you bonus points:

* **Time Dilation:** Add countdown timers for each round to increase urgency.
* **Nexus Streaks:** Implement a multiplier system that rewards players for consistently accurate guesses.
* **Difficulty Levels:** Create Easy (hints allowed), Medium, and Hard (strict time limits, zoomed-in images) modes.
* **Leaderboards:** Display high scores across different players, with scores stored in shared persistent storage so the leaderboard is not limited to the current user.



---

## Task 5: Deployment & Documentation (Total: 20 pts)

### Subtask 5.1 – Deployment (10 pts)

Deploy your web app to an online platform so that users can access it.

* Use a service like **GitHub Pages**, **Netlify**, or **Vercel** for hosting.
* Provide a public URL where the game can be played.



### Subtask 5.2 – Documentation (10 pts)

Provide a clear, professional **`README.md`** file at the root of the repository that includes:

* A brief description of your solution and the tech stack used.
* Instructions on how to run or test the project locally.

---

## Grading Criteria

| Task | Points |
| --- | --- |
| **Task 1: The Observation Deck** | **50 pts** |
| - Location Viewer | 25 pts |
| - Interactive Nexus Map | 25 pts |
| **Task 2: Timeline Stabilization** | **60 pts** |
| - Anomaly Generation | 20 pts |
| - Convergence Calculation | 40 pts |
| **Task 3: The TVA Assessment** | **50 pts** |
| - Scoring System | 25 pts |
| - Multi-Round Gameplay & Results | 25 pts |
| **Task 4: Multiversal Anomalies (Bonus)** | **20 pts** |
| - Advanced Mechanics | 20 pts |
| **Task 5: Deployment & Docs** | **20 pts** |
| - Deployment | 10 pts |
| - Documentation | 10 pts |
| **Total** | **200 pts** |