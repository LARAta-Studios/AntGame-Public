# 🐜 Ant-Game 🐜

A 2d Game where we play as a father Ant who needs to take a cookie crumb to his family in order to survive. This would need to be accomplished without him dying or the cookie crumb destroying.

<img width="1916" height="1076" alt="Screenshot 2026-05-15 152700" src="https://github.com/user-attachments/assets/b760a610-2da6-48fb-86e4-4d7e72eb6fe8" />

---

## 🕹️ Play the Game 🕹️

- Web Build: [Play Here](https://laratastudios.com/AntGame-Public/)
- Windows Build: [Download](https://github.com/LARAta-Studios/AntGame-Public/releases/tag/Windows)
- Android Apk: [Download](https://github.com/LARAta-Studios/AntGame-Public/releases/tag/Android)

---

## 💫 Features 💫

- Animated character sprites and visual effects
- Level progress tracker
- Speedrun timer
- Best times speedrun leaderboard
- Background Music and SFX
- Advance motion mechanics like wall-jump
- Responsive UI Scaling
- Level selection
- Optimized keyboard and controller input
- Optimized Mobile controls
- 30 handcrafted levels

<img width="500" height="300" alt="Screenshot 2026-05-28 141841" src="https://github.com/user-attachments/assets/f987d943-99d1-49a0-b017-8a6977b69e3a" />
<img width="500" height="300" alt="Screenshot 2026-05-28 142039" src="https://github.com/user-attachments/assets/a7e134af-5c9c-4852-848c-35c431c0ae1f" />

<img width="500" height="300" alt="Screenshot 2026-05-28 142137" src="https://github.com/user-attachments/assets/7986f254-1c89-4d5f-ae86-3430fe1b4864" />
<img width="500" height="300" alt="Screenshot 2026-05-28 144254" src="https://github.com/user-attachments/assets/32983d3c-b921-48ef-9549-b48cd2ee9190" />





---

## 🛠️ Built With 🛠️

- Unity
- C#
- GitHub Pages
- Adobe Illustrator

---

## 💡 Important Design Decisions 💡

Throught this project I had to take multiple important decisions regarding the projects future. Some of them were:

### 🌱Ground Detection🌱
At the beginning of the project I was going to detect ground using the collision functions and tags, every time the player is gorunded it would be able to jump. This worked for some time until I wanted the player to be able to jump from the top of objects like spikes, or the ball and since having it check for multiple tags would increase the complexity of the code, I decided to detect ground in a complete different way which was having a ground transform object located an the feet of the player and I could check if the user could jump using the OverlapCircle function in Unity, this function essentially checks if 2 tranforms are within a given radius, so if the ground check transform is far from the ground then the player would not be grounded. This ended up improving the game feel in the future because it also solved another issue which was when a ground tagged object was the ceiling or ground... since the ground check is under the player even if the player touches a ceiling it would not detect it as ground because it isnt within the radius.


### 🚀Level Progression🚀
I knew that I wanted to have a level selection system but I had to decide on whether the levels are unlocked from the beginning or they needed to be progressively unlocked. I ended up deciding on make them unlockable as the user reaches each level, this way the levels that intend to teach the user some game mechanics work as intended and users would feel proud as they unlock new levels.


<img width="400" height="200" alt="Screenshot 2026-05-28 141541" src="https://github.com/user-attachments/assets/b8d98b79-23ad-42cb-af89-1e222750d148" />

<img width="400" height="200" alt="Screenshot 2026-05-28 144310" src="https://github.com/user-attachments/assets/7d2c29c9-4b89-44fc-993c-fc5ba2b5c7ea" />


### 🔗Pulling Mechanic🔗
When developing the game I wanted to make a pulling mechanic so that the player could unstuck the ball when it was pinned into a wall and since the ant/ball mass ratio was 1:10 then the was no way that the player could get underneath and free it. After thinking a lot about it, I decided that it would be best if the pulling mechanic is implemented later as a power-up rather than a base mechanic because it would make the levels and game progression useless and less fun. To solve the ball pinned issue I made it so that the ball mass would decrease just enough when touching a wall so that the player could lift the ball and set it free.


---

## 🎓 What I learned 🎓

This project taught me:
- Game development fundamentals
- Level progression systems
- Data saving systems
- Gamplay mechanics implementation
- Designing UI and UI scaling
- Scene Management
- Mobile controller adaptation

---

## 🎯 Technical Challenges 🎯

The most difficult challenge of this project was designing forgiving strategies to make the game more enjoyable.
Since this was my first time in game development I was not really aware how the collisions worked, but by working and progressing on the project I have learned how collisions are handled by Unity. They are handled by 3 main functions:
- Collision2DEnter() : Gets called when 2 colliders touch
- Collision2DExit()  : Gets called when 2 colliders stop touching
- Collision2DStay()  : Gets called every frame when 2 colliders remain touching

The thing about these 3 functions is that they dont have any forgiveness to them, what I mean by that is that some things have to be frame-perfect for them to work which is something bad because it makes the game unecessarily difficult. I solved this by creating multiple forgiving areas or grace periods to make mechanics more fun and enjoyable. Some of them were:
- Grace period on spikes so the player has time to move the ball out of the spikes
- Grace area on spikes so that the same spike can only damage the cookie once until it exits the grace area
- Forgiving Area on cookie crumb so that the user has time to jump from the top of the ball while it is in the air

---

## 🔮 Future Improvements 🔮

- Skin cuztomization
- Better animations
- More SFX
- More Levels
- Online Leaderboard


---

## ⚙️ Source Code ⚙️

The full source code is private while the project is in active development.
This repository serves as a showcase of the project, including gameplay footage, technical explanations and playable builds. 
























