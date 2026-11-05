# Jungle Escape 3D - Temple Run-Style Runner

A feature-packed Temple Run–style 3D endless runner game built with **Three.js**.

## 🎮 Features Included
- **3D Moving Forest Environment**: Modular rainforest with ancient stone pillars, cobblestones, moss, ferns, rocks, and giant canopy trees.
- **Gorilla Starting Voice & Chasing AI**:
  - Realistic, powerful gorilla roar audio (`sounds/gorilla-roar.mp3`) plays on Start before the chase begins.
  - Chases for 7s on start, retreats into the woods, and returns for 5s on obstacle collisions.
  - Two-strike eating mechanic if the player hits obstacles more than once.
- **Dual Coin Challenges & 3 Separate Live Counters**:
  - **300 Yellow Coins Challenge (0m – 300m)**:
    - Normal yellow gold medallion coins spawn frequently throughout the first 300 metres.
    - Live HUD counter: `YELLOW COINS: 0 / 300`.
    - Completing all 300 triggers: `"YELLOW COIN CHALLENGE COMPLETED!"`.
  - **100 Coloured Coins Challenge (300m+)**:
    - Generates 100 special coins: **50 Blue Coins** and **50 Red Coins** distributed across left, middle, and right lanes.
    - 3D floating rotation, glowing luminous halos, and dynamic particle bursts on collection.
    - Live HUD counters: `BLUE COINS: 0 / 50` and `RED COINS: 0 / 50`.
    - Collecting all 50 blue and 50 red coins triggers: `"100 COLOURED COINS COMPLETED!"`, victory fanfare, and an **Invincible 10-Second Energy Shield**!
- **90-Degree Left & Right Turns**: Periodic dead-end temple corners requiring sharp turns with cinematic camera banking.
- **Realistic Flowing Water & Waterfall Cascades**:
  - Blue jungle river flowing alongside the running path with continuous animated waves, caustics, and reflections.
  - Procedural scrolling water and waterfall textures with high rushing velocity.
  - Cascading waterfalls falling down cliffs with white foam rings and animated water splash particles.
  - Dynamic splashes when water hits rocks and boulders.
- **3 Types of Bridges**:
  - **A. Ancient Wooden Plank Bridge**: Hand-hewn timber stringers, weathered wooden planks with slight gaps, side ropes, vertical timber posts, and dynamic deck bounce resonance when running over it.
  - **B. Ancient Stone Temple Bridge**: Arched masonry piers spanning deep canyons, cobblestone roadway deck, carved balustrades with balusters, creeping ivy, and 4 corner entrance pillars with animated burning torches.
  - **C. Suspended Hanging Rope Bridge**: Tall A-frame timber towers, drooping parabolic catenary suspension cables, vertical rope suspenders, suspended wooden slats, and dynamic gentle swinging movement.
  - Dynamic deck elevation keeps the hero positioned naturally without falling through; coins and occasional hurdles spawn on bridge decks.
- **Downward Rope Connection Between Two Separate Bridges (450m+)**:
  - **Upper Wooden Bridge**: High elevation ($Y = 6.2$), reached via an incline ramp, with weathered wooden planks, timber stringers, side rope handrails, and rock cliff abutments.
  - **The Large Empty Gap**: 48-meter wide chasm with **zero road, zero floor, zero platform, and zero stairs** inside the gap, dropping down into mist and deep river canyon waters.
  - **Downward Diagonal Rope**: Braided 3D cylinder rope with helical strands connecting the upper bridge anchor ($Y = 8.2$) diagonally down to the lower bridge anchor ($Y = 2.0$).
  - **Hero Zipline Slide**: At the upper bridge edge, hero automatically jumps and grabs the diagonal rope, hangs suspended with hands overhead, tilts along the rope incline, and kicks legs during the thrilling diagonal descent.
  - **Floating Diagonal Coins**: Spaced along the downward rope in mid-air.
  - **Lower Wooden Bridge**: Low elevation ($Y = 0.2$), where the hero safely releases the rope, lands on the wooden deck, and resumes running back onto the jungle path.
  - **Smooth Camera Tracking**: Camera smoothly tracks the vertical descent from $Y = 6.2$ down to $Y = 0.2$.
- **Grand Water Canal Section (720m – 1000m)**:
  - **720m – 780m (Stone Aqueduct Bridge)**: Hero crosses high above rushing canal waters on an ancient stone bridge (`swimming = false`, `onBridge = true`).
  - **780m – 940m (Canal Swimming)**: Hero dives into the canal with water splash particles and swims with breaststroke animation across dynamic rolling waves.
  - **940m – 1000m (Wooden Footbridge Exit)**: Hero emerges from the canal onto a wooden footbridge and steps smoothly back onto the jungle running path.
- **Classic Frontend Start Screen (`temple-menu.jpg`)**:
  - Authentic Temple Run archway poster with glowing idol.
  - Interactive **PLAY!**, **OBJECTIVES**, **STATS**, **STORE**, **OPTIONS**, and **MORE GAMES** buttons.
- **3D Water Canal Swimming (800m – 1000m)**:
  - Transition into a 200m water canal with stone walls, moss, and animated procedural waves.
  - Hero switches seamlessly to floating breaststroke/crawl swimming animations.
- **3D Hanging Rope Traversal (1200m+)**:
  - Two floating temple platforms separated by a 100m deep chasm with low-lying clouds and stone spires.
  - Advance warning at 1100m: `🪢 ⚠️ HANGING ROPE AHEAD! ⚠️ 🪢`.
  - Hero jumps and grabs a thick braided overhead sagging rope with realistic twisted helical strands.
  - Authentic hanging physics: body roll, side-to-side sway, dangling kicking legs, and hand gripping travel rhythm.
  - Collectible floating coins along the rope route with sliding audio whoosh sound effects.
  - Reaching the other side safely lands the hero onto the stone temple platform and resumes running.
- **Audio Synthesizer & Audio Files**: Real sound files with automated Web Audio API procedural synthesis fallbacks and a 🔊 mute/unmute toggle.
- **Keyboard & Mobile Swipe Controls**: Full desktop and mobile touchscreen swipe and on-screen button support.

---

## 🕹️ Controls

| Action | Keyboard | Touch / Mobile |
| :--- | :--- | :--- |
| **Move Left / Right** | `←` / `→` or `A` / `D` | Swipe Left / Right |
| **Jump** | `↑` / `W` / `Space` | Swipe Up |
| **Slide** | `↓` / `S` | Swipe Down |
| **Start / Restart** | Click button, `Space`, or `Enter` | Tap button |
| **Mute / Unmute** | Click the 🔊 button | Tap 🔊 button |

---

## 🚀 How to Run

### Option 1: Built-in Node Server (Recommended)
Run the built-in static server with zero dependencies:
```bash
npm start
```
Then open your browser at **[http://localhost:3000](http://localhost:3000)**.

### Option 2: Live Server or Direct Browser Preview
You can also open `index.html` using the IDE's live preview, VS Code Live Server extension, or any local static server.

*(Note: Internet connection is needed to load Three.js from the CDN).*

