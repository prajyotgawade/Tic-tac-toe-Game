# 🎮 Tic Tac Toe — Android Game

<div align="center">

**A clean, interactive two-player Tic Tac Toe game built natively for Android using Kotlin & Android Studio.**

[![GitHub](https://img.shields.io/badge/GitHub-Tic--tac--toe--Game-181717?style=for-the-badge&logo=github)](https://github.com/prajyotgawade/Tic-tac-toe-Game)
[![Kotlin](https://img.shields.io/badge/Kotlin-Android-7F52FF?style=for-the-badge&logo=kotlin)](https://kotlinlang.org)
[![Android](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android)](https://developer.android.com)
[![Android Studio](https://img.shields.io/badge/IDE-Android_Studio-3DDC84?style=for-the-badge&logo=androidstudio)](https://developer.android.com/studio)

</div>

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Game Rules](#-game-rules)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [How It Works](#-how-it-works)
- [Roadmap](#-roadmap)
- [Contact](#-contact)

---

## 🚀 About the Project

**Tic Tac Toe** is a classic two-player strategy game built as a native Android application using **Kotlin** in Android Studio. This project demonstrates core Android development skills including UI design with XML layouts, game logic implementation, state management, and event handling.

Two players take turns marking spaces on a **3×3 grid**. The player who places three of their marks in a horizontal, vertical, or diagonal row wins the game.

> Built entirely in **Kotlin** — showcasing Android native development, UI/UX design, and clean game logic implementation from scratch.

---

## ✨ Features

### 🎮 Gameplay
- ✅ Two-player local multiplayer on a single device
- ✅ Interactive 3×3 grid with tap-to-play controls
- ✅ Win detection — horizontal, vertical & diagonal
- ✅ Draw detection — when all cells are filled with no winner
- ✅ Turn indicator — shows whose turn it is (Player X / Player O)
- ✅ Win highlight — highlights the winning combination
- ✅ Instant game reset — play again without restarting the app

### 📱 Android UI
- ✅ Clean, minimal Material Design UI
- ✅ Responsive layout that works across screen sizes
- ✅ Smooth tap interactions with visual feedback
- ✅ Score tracking across multiple rounds

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| **Language** | Kotlin |
| **Platform** | Android (Native) |
| **IDE** | Android Studio |
| **UI** | XML Layouts + Material Design |
| **Min SDK** | Android 5.0 (API 21) |
| **Architecture** | MVC (Model-View-Controller) |

---

## 🎯 Game Rules

```
1. The game is played on a 3×3 grid
2. Player X always goes first
3. Players take turns placing their mark (X or O)
4. The first player to get 3 marks in a row WINS:
   → Horizontally   (— — —)
   → Vertically     (| | |)
   → Diagonally     (\ or /)
5. If all 9 squares are filled with no winner → DRAW
6. Tap "Play Again" to restart the game
```

---

## ⚙️ Getting Started

### Prerequisites

- [Android Studio](https://developer.android.com/studio) (Latest stable version)
- Android SDK (API 21 or above)
- Kotlin plugin (comes pre-installed with Android Studio)
- An Android device or emulator

### Installation

**1. Clone the repository**
```bash
git clone https://github.com/prajyotgawade/Tic-tac-toe-Game.git
cd Tic-tac-toe-Game
```

**2. Open in Android Studio**
- Launch Android Studio
- Click **File → Open**
- Select the cloned project folder
- Wait for Gradle sync to complete

**3. Run the app**

**On a physical device:**
- Enable Developer Options & USB Debugging on your Android phone
- Connect via USB
- Click the ▶️ Run button in Android Studio

**On an emulator:**
- Open AVD Manager in Android Studio
- Create a virtual device (e.g. Pixel 6, API 33)
- Click ▶️ Run

---

## 📁 Project Structure

```
Tic-tac-toe-Game/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/prajyot/tictactoe/
│   │   │   │       ├── MainActivity.kt      # Main game logic & UI controller
│   │   │   │       └── GameLogic.kt         # Win/draw detection logic
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   │   └── activity_main.xml    # Game board UI layout
│   │   │   │   ├── drawable/                # Icons & button assets
│   │   │   │   ├── values/
│   │   │   │   │   ├── colors.xml           # App color palette
│   │   │   │   │   ├── strings.xml          # String resources
│   │   │   │   │   └── themes.xml           # App theme
│   │   │   └── AndroidManifest.xml          # App configuration
│   └── build.gradle                         # App-level dependencies
├── build.gradle                             # Project-level build config
├── gradle.properties                        # Gradle settings
└── settings.gradle                          # Module settings
```

---

## 🔄 How It Works

```
App Launch → Game Board Displayed → Player X Turn
     ↓
Player taps a cell → Mark placed (X or O)
     ↓
Win Check → 3 in a row? → 🎉 Show Winner + Highlight
     ↓
No winner? → All cells filled? → 🤝 Draw
     ↓
Cells remaining? → Switch turn → Next player
     ↓
"Play Again" tapped → Reset board → Player X goes first
```

### Win Detection Logic

```kotlin
// Checks all 8 possible winning combinations
val winCombinations = arrayOf(
    // Horizontal
    intArrayOf(0, 1, 2),
    intArrayOf(3, 4, 5),
    intArrayOf(6, 7, 8),
    // Vertical
    intArrayOf(0, 3, 6),
    intArrayOf(1, 4, 7),
    intArrayOf(2, 5, 8),
    // Diagonal
    intArrayOf(0, 4, 8),
    intArrayOf(2, 4, 6)
)
```

---

## 🗺 Roadmap

- [x] Two-player local multiplayer
- [x] Win & draw detection
- [x] Turn indicator
- [x] Game reset functionality
- [x] Clean Android UI with XML layouts
- [ ] Single player mode vs AI (Minimax algorithm)
- [ ] Score tracking across sessions
- [ ] Sound effects & animations
- [ ] Dark mode support
- [ ] Online multiplayer via Firebase

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create your branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 📬 Contact

**Prajyot Gawade**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-prajyotgawade-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/prajyotgawade)
[![GitHub](https://img.shields.io/badge/GitHub-prajyotgawade-181717?style=flat&logo=github)](https://github.com/prajyotgawade)

---

<div align="center">

⭐ **If you liked this project, please give it a star!** ⭐

Built with ❤️ by Prajyot Gawade — Mumbai, India

</div>
