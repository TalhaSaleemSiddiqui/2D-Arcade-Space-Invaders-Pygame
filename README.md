# 2D-Arcade-Space-Invaders-Pygame
A 2D space shooter game developed in Python using Pygame. The player controls a spaceship, avoids incoming asteroids, collects coins and power-ups, and uses a weapon to destroy asteroids and increase the score. The project demonstrates object-oriented programming (OOP), collision detection, keyboard controls, random object spawning, sound effects, background music, health management, score tracking, and persistent high-score storage.

---

## 🎮 Features

**🚀 Spaceship Control**
- Control the spaceship using the arrow keys.
- Rotate the spaceship left and right.
- Move forward and backward based on the spaceship's direction.
- The spaceship wraps around the screen when it moves beyond the screen boundaries.

**☄️ Asteroid Enemies**
- Asteroids spawn at random locations.
- Asteroids move in random directions with different speeds.
- Colliding with an asteroid decreases the player's health.
- When health reaches zero, the player loses one life.
- The game ends when all lives are lost.
- Shooting an asteroid destroys it and increases the score.

**🔫 Weapon & Shooting System**
- Weapon power-ups appear randomly during gameplay.
- Collecting a weapon power-up enables shooting.
- Press `SPACE` to fire bullets.
- Bullets travel in the direction the spaceship is facing.
- Destroying an asteroid with a bullet awards 5 points.

**🛡️ Shield Power-Up**
- Shield power-ups appear randomly during gameplay.
- Collecting a shield activates the player's shield.
- A visual circle is displayed around the spaceship while the shield is active.
- The shield changes how asteroid collisions affect the player's health.
- Collecting the shield power-up awards 1 point.

**🪙 Coin Collection**
- Coins spawn at random locations.
- Coins move across the screen.
- Collecting a coin awards 10 points.
- Coins that move outside the screen are removed.

**❤️ Health & Lives**
- The player starts with 3 lives.
- A health bar is displayed at the top of the screen.
- Asteroid collisions decrease health.
- When health reaches zero, one life is lost.
- After losing a life, the health bar is restored.
- The game ends when the player has no lives remaining.

**🏆 Score & High Score**
- Destroying an asteroid: +5 points
- Collecting a coin: +10 points
- Collecting a shield power-up: +1 point
- The current score is displayed during gameplay.
- The highest score is saved in `highscore.txt`.
- A saved high score is loaded when the game starts.
- The high score is updated when the player achieves a new record.

**🔊 Audio**
- Background music plays continuously during the game.
- Shooting has a sound effect.
- Asteroid destruction has a sound effect.
- Power-up collection has a sound effect.

**🔄 Restart System**
- Press `S` to restart the game.
- Restarting resets:
  - Lives
  - Health
  - Score
  - Bullets
  - Asteroids
  - Spawn counter
  - Game-over state

---

## 🕹️ Controls

| Key | Action |
|---|---|
| `↑` | Move forward |
| `↓` | Move backward |
| `←` | Rotate left |
| `→` | Rotate right |
| `SPACE` | Shoot |
| `S` | Restart the game |
| Close Window | Exit the game |

> **Note:** Shooting is available only after collecting the weapon power-up.

---

## 🧩 Game Objects

The game uses an object-oriented structure with a parent `GameObject` class and multiple specialized classes.

### `GameObject`
The base class for the game's objects. Provides:
- Position (`x`, `y`)
- Image
- Width and height
- Drawing functionality

### `Player`
Represents the player's spaceship.
- Movement
- Rotation
- Direction calculation
- Screen wrapping
- Rendering

### `Bullet`
Represents bullets fired by the player.
- Movement
- Direction and speed
- Screen-boundary detection
- Rendering

### `Asteroid`
Represents enemy asteroids.
- Random spawning
- Random movement
- Collision detection with the player
- Collision detection with bullets
- Rendering

### `Powerup`
Represents the shield power-up.
- Random spawning
- Random movement
- Shield activation
- Collision detection

### `Coin`
Represents collectible coins.
- Random spawning
- Random movement
- Collision detection with the player
- Score increase

### `Weapon`
Represents the weapon power-up. Collecting the weapon enables the player to shoot bullets.

### `HealthBar`
Manages the player's health.
- Displaying the health bar
- Increasing health
- Decreasing health
- Detecting when health reaches zero

---

## 📊 Scoring System

| Action | Points |
|---|---|
| Destroy an asteroid | +5 |
| Collect a coin | +10 |
| Collect a shield power-up | +1 |

The game also maintains a persistent high score using `highscore.txt`.

---

## ⏱️ Object Spawn System

Different objects are spawned at different intervals during the game loop.

| Object | Spawn Interval |
|---|---|
| Asteroid | Every 50 frames |
| Coin | Every 100 frames |
| Weapon Power-Up | Every 200 frames |
| Shield Power-Up | Every 500 frames |

The game loop is limited to approximately 60 FPS.

---

## 📁 Project Structure

```
2D-Arcade-Space-Invaders-Pygame/
│
├── space_invaders_game.py
├── highscore.txt
│
├── starbg.jpg
├── ship_3.png
├── shield.png
├── asteroid50.png
├── coin.png
├── weapon.png
│
├── shoot.wav
├── bangSmall.wav
├── bangLarge.wav
├── background.wav
│
└── README.md
```



---

## 🛠️ Technologies Used

- Python
- Pygame
- Object-Oriented Programming (OOP)
- Collision Detection
- Randomized Object Spawning
- Keyboard Event Handling
- File Handling
- 2D Game Development
- Audio Integration
- Real-Time Rendering

---

## ⚙️ Requirements

**1. Install Python**

Make sure Python 3 is installed on your system. Check your version:
```bash
python --version
```
or:
```bash
python3 --version
```

**2. Install Pygame**
```bash
pip install pygame
```
On some systems, you may need:
```bash
pip3 install pygame
```

**3. Run the Game**
```bash
python space_invaders_game.py
```
or:
```bash
python3 space_invaders_game.py
```

Make sure all image files, audio files, and `highscore.txt` are located in the same project directory as the Python file.

---

## 💡 How to Play

1. Launch the game.
2. Use the arrow keys to control the spaceship.
3. Avoid incoming asteroids.
4. Collect the weapon power-up to unlock shooting.
5. Press `SPACE` to fire bullets.
6. Destroy asteroids to earn points.
7. Collect coins for additional points.
8. Collect the shield power-up for protection.
9. Monitor your health and remaining lives.
10. Press `S` to restart the game.
11. Try to achieve a new high score.

---

## 🏗️ Technical Concepts Demonstrated

- Classes and inheritance
- Object-oriented programming
- Game loop implementation
- Keyboard event handling
- Collision detection using bounding boxes
- Vector-based movement
- Sine and cosine calculations for directional movement
- Randomized spawning
- Randomized object movement
- Health and life management
- Persistent file storage
- Score and high-score management
- Audio integration
- Real-time rendering
- Frame-rate control

---

## 📌 Important Notes

The game depends on the image and audio files referenced in the Python source code. Renaming, deleting, or moving these files without updating the code may cause the game to fail when loading the required assets.

The file `highscore.txt` stores the player's highest score. The game reads the saved high score when it starts and writes a new value when the player achieves a higher score.

