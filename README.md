<h1 align="center">🎱 Billiard Helper</h1>

<p align="center">
  <b>Android app for billiard players: match tracking, ball detection and statistics</b><br>
  Software Engineering Project · TU Braunschweig · 2026
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin">
  <img src="https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white" alt="Jetpack Compose">
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV">
  <img src="https://img.shields.io/badge/Android%2016-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android 16">
</p>

<p align="center">
  <img src="demo/demo.gif" width="280" alt="App demo">
</p>

> [!NOTE]
> **This is a showcase repository.** Billiard Helper was built by a student team, so the source code lives in a **private repository**.
> Here you can see what the app does, how it was built and what my part was. Access to the code is available on request.

---

## 💡 About the project

Billiard Helper was developed **from scratch for a real client** as part of the Software Engineering Project at TU Braunschweig.
Players can track every shot of a match, let the camera detect the balls on the table, measure their break speed and follow their progress over time.
The app was delivered to the client and presented at the university's software engineering showcase (**TdSE**).

---

## ✨ Features

| | Feature | Description |
|---|---|---|
| 🎯 | **Match tracking** | Pocketed balls, fouls and innings, in single or team mode |
| 📷 | **Ball detection** | The camera recognises the balls on the table using OpenCV |
| ⚡ | **Break speed** | Measures how fast the break shot was |
| 📊 | **Statistics** | Charts of a player's performance over time |
| 👤 | **Player profiles** | Create and manage local player profiles |
| 📖 | **Rule book** | Rules for 8-Ball, 9-Ball, 10-Ball and 14.1 Straight Pool |
| 🏆 | **Leaderboards** | Rank players by wins and other values |
| 📁 | **CSV export** | Export match data for further analysis |

---

## 📱 Screenshots

<p align="center">
  <img src="demo/screenshots/home.png" width="22%" alt="Home screen">&nbsp;
  <img src="demo/screenshots/match.png" width="22%" alt="Match tracking">&nbsp;
  <img src="demo/screenshots/vision.png" width="22%" alt="Ball detection">&nbsp;
  <img src="demo/screenshots/statistics.png" width="22%" alt="Statistics">
</p>
<p align="center"><i>Home · Match tracking · Ball detection · Statistics</i></p>

---

## 🏗️ Architecture

```mermaid
flowchart LR
    UI["🖼️ ui<br/>Jetpack Compose screens"] --> LOGIC["🧠 logic<br/>game rules & scoring"]
    UI --> VISION["📷 vision<br/>ball detection & break speed"]
    LOGIC --> MODEL["📦 model<br/>data structures"]
    VISION --> MODEL
    LOGIC --> DATA["💾 data<br/>persistence & CSV export"]
```

| Area | Technology |
|---|---|
| Language | Kotlin |
| UI | Jetpack Compose |
| Computer vision | OpenCV |
| Build | Gradle (Kotlin DSL) |
| CI | GitLab CI: lint checks and automatic APK builds |
| Version control | Git with feature branches and merge requests (300+ commits) |

---

## 📋 Software engineering process

We followed the **complete software engineering process**, with all the documentation a real client project needs:

```mermaid
flowchart LR
    A["📝 Requirements<br/>specification"] --> B["📐 Functional &<br/>technical design"]
    B --> C["💻 Implementation<br/>documented code"]
    C --> D["✅ Acceptance<br/>testing"]
    D --> E["🚀 Delivery<br/>to the client"]
```

| Phase | What we produced |
|---|---|
| **Requirements** | Requirements specification (*Pflichtenheft*), agreed with the client |
| **Design** | Functional design (*Fachentwurf*) and technical design (*Technischer Entwurf*) |
| **Implementation** | Fully documented source code, code reviews and merge requests |
| **Testing** | Acceptance test specification (*Abnahmetestspezifikation*) |
| **Delivery** | App handed over to the client and presented at the TdSE showcase |

---

## 👩‍💻 My contribution

I worked on both the **game logic** (`logic`) and the **computer vision** (`vision`) packages, and on the project documentation.

**💻 Development**
- 🧠 Worked on the **game logic**: the rule classes for the different billiard variants (e.g. `NineBallRules`, `TenBallRules`) and the match flow, including rack handling
- 📷 Worked on the **vision package**: the `VisionManager` and `VisionViewModel`, which connect the camera and the ball detection to the app
- 🐞 Found and fixed bugs in the **win/loss detection** (`isGameWon` / `isGameLost`) and in the **last-rack handling** (`handleRackWon`)

**🔍 Code quality**
- Did an extensive **code review** of the game-rule classes, the vision classes and the use of **Kotlin coroutines**

**📋 Documentation**
- Co-wrote the **technical design** (*Technischer Entwurf*)
- Worked on the **test specifications** and the **acceptance test specification** (*Abnahmetestspezifikation*)
- Contributed to the **requirements specification** (*Pflichtenheft*) and the **functional design** (*Fachentwurf*)
- Created the **AI usage documentation** for the project, as required by the course

**🎤 Presentation**
- Presented the app with the team at the TU Braunschweig software engineering showcase (**TdSE**)

---

## 👥 Team

Developed by a team of Computer Science students at **TU Braunschweig** as part of the Software Engineering Project 2026.

<p align="center"><sub>Questions about the project? Reach me on <a href="https://www.linkedin.com/in/wihed-sakri/">LinkedIn</a>.</sub></p>
