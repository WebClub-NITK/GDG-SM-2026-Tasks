# Silicon Maze: Echoes of the Web

## The Story

A city-wide energy surge has fractured the **Aether Core**, scattering its fragments across unstable districts. Bridges have collapsed, machines have gone haywire, and ordinary routes are no longer safe.

You are a young web-slinger tasked with restoring the city. Explore the connected world, help its residents, recover the missing fragments, and use momentum, gravity, collisions, and elastic tethers to reach places that cannot be accessed by walking alone.

## Objective

Create a playable browser game with a **compact open world** containing at least three connected zones. The player must be free to explore, discover objectives, interact with physics-based objects, and complete quests in more than one order.

The task is intentionally open-ended. You may choose the art style, story details, world layout, and technology stack. Evaluation will focus on whether physics meaningfully drives the gameplay - not on the size of the map or the number of assets.

## Core Requirements

### Task 1: Build the World and Movement System (25 points)

#### 1.1 - Connected World (9 points)

- Create at least **three distinct, connected zones** within one explorable world.
- Add solid terrain, platforms, walls, and world boundaries with reliable collision handling.
- Implement a camera that follows the player without exposing areas outside the world.
- Place recognizable landmarks so players can navigate without getting lost.

#### 1.2 - Physics-Based Player Movement (8 points)

- Implement responsive movement using velocity, acceleration, gravity, and drag/friction.
- Support jumping and airborne control without allowing unlimited flight or repeated mid-air jumps.
- Keep movement stable across different frame rates.

#### 1.3 - Web Tether and Swinging (8 points)

- Allow the player to attach an elastic tether to valid world anchors.
- Use the tether to swing, build momentum, and reach otherwise inaccessible locations.
- Let the player release and reconnect the tether cleanly.
- Show clear visual feedback for valid anchors, the active tether, and failed attachment attempts.

### Task 2: Exploration, Objects, and Physics Quests (30 points)

#### 2.1 - Discoverable Objects (8 points)

- Hide at least **six collectible objects** across the world.
- Make at least three collectibles require deliberate use of movement or physics to reach.
- Provide clear feedback when an object is discovered and track collection progress.

#### 2.2 - World Interaction (8 points)

- Include movable objects that respond to forces, gravity, and collisions.
- Allow the player to push, pull, carry, or tether selected objects.
- Make object behavior predictable enough for players to solve puzzles intentionally.

#### 2.3 - Physics-Based Quests (14 points)

Implement at least **three completable quests**. Each quest must have a visible objective and a clear success state. Together, the quests must use at least three of the following ideas:

- momentum or impulse;
- pendulum or swinging motion;
- weight, balance, or counterweights;
- projectile motion;
- friction or slippery surfaces;
- springs, elastic forces, or gravity fields.

At least one quest must combine two physics ideas, and at least one quest must allow more than one valid solution.

### Task 3: Story and Progression (20 points)

#### 3.1 - Quest Flow (7 points)

- Introduce the player to the main objective through an opening scene, dialogue, or in-world message.
- Allow the three core quests to be completed in any order.
- Unlock a final objective after the required quests or fragments are complete.

#### 3.2 - World Feedback (6 points)

- Provide an objective tracker or journal showing active and completed quests.
- Use dialogue, signs, environmental changes, or short scenes to show the consequences of progress.
- Ensure prompts and important state changes are readable and do not block gameplay.

#### 3.3 - Save and Resume (7 points)

- Save collected objects, completed quests, unlocked progress, and essential settings locally.
- Restore a valid saved game after a refresh or restart.
- Include a **New Game / Reset Progress** option.
- If saved data is missing or invalid, start safely from the beginning.

### Task 4: Game Feel, Reliability, and Delivery (25 points)

#### 4.1 - Complete Gameplay Loop (9 points)

- Provide a clear start, playable progression, final objective, and ending state.
- Add checkpoints or safe respawn behavior so failure never requires reloading the page.
- Prevent common soft locks such as lost quest objects, unreachable player states, or broken quest order.

#### 4.2 - Presentation and Accessibility (6 points)

- Add readable controls, objective text, and sufficient color contrast.
- Provide audio controls if the game includes sound.
- Include a reduced-motion option or avoid non-essential intense screen motion.
- Support keyboard play. Touch or gamepad support is optional.

#### 4.3 - Documentation and Deployment (10 points)

- Deploy a playable build that opens in a modern desktop browser.
- Include a `README.md` with:
  - the game premise and controls;
  - the chosen technology stack;
  - setup and run instructions;
  - a short explanation of the physics systems;
  - known limitations;
  - the deployed game link.
- Record a short explanation video showing the world, all required quests, save/resume behavior, and the relevant code.

## Minimum Playable Checklist

A submission is complete when a reviewer can:

1. start a new game and understand the objective;
2. explore three connected zones;
3. move and swing using the physics system;
4. find and collect objects;
5. complete three physics-based quests in any order;
6. unlock and finish the final objective;
7. refresh the game and continue from saved progress; and
8. reset progress and begin again without errors.

## Evaluation Summary

| Area | Points |
| --- | ---: |
| World and movement system | 25 |
| Exploration, objects, and physics quests | 30 |
| Story and progression | 20 |
| Game feel, reliability, and delivery | 25 |
| **Total** | **100** |

Partial implementations will receive points for completed subtasks. A smaller, stable world with polished physics will score better than a large, unfinished map.

## Bonus Challenges (up to 10 bonus points)

- **Physics debug view (2.5):** Toggle velocity vectors, collision shapes, tether length, or force direction.
- **Dynamic world event (2.5):** Add a weather or gravity event that temporarily changes traversal.
- **Advanced accessibility (2.5):** Add remappable controls, scalable text, or a high-contrast mode.
- **Original mechanic (2.5):** Add a well-integrated physics mechanic not already required above.

Bonus work is evaluated only after the core game is functional.

## Technical Guidance

- You may use any web technology or physics library. Suitable choices include [Matter.js](https://brm.io/matter-js/), [Phaser](https://phaser.io/), [p5.js](https://p5js.org/), or a custom implementation using the [Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API).
- External libraries and original or properly licensed assets are allowed. Credit assets and libraries in the submission README.
- Do not spend time building a custom physics engine unless it directly supports your game idea.
- Desktop browser support is required; mobile support is optional.

## Submission Instructions

1. Create a repository containing the complete source code.
2. Keep the repository private until the deadline, then make it public as instructed by the organizers.
3. Include the documentation and deployed game link in the repository.
4. Upload the explanation video to a publicly accessible service such as Google Drive, YouTube, or Loom.
5. Submit the repository and video links through the organizer-provided portal.

Good luck - make the city feel fun to move through before making it big.
