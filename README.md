# FR_OS — Fattesing Rane's Portfolio

> A portfolio that boots like an OS, runs like a terminal, and plays like a game.

---

## What is this?

FR_OS is a single-file interactive portfolio built as a fake desktop operating system. Instead of a traditional scrolling page, visitors land on a Linux-inspired desktop complete with a boot sequence, draggable windows, a working terminal with a command palette, a matrix rain wallpaper, and a playable Snake game.

Built entirely with vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies, no build step.

---

## Features

### 🖥️ Desktop OS Experience
- Fake Linux boot sequence with animated progress bar on load
- Full-screen matrix rain wallpaper (katakana + hex characters) covering the entire desktop
- Draggable, minimizable, and maximizable windows
- Taskbar with live clock
- Desktop icons (double-click to open windows)

### ⌨️ Interactive Terminal
- Fully working bash-style terminal with command execution
- Split layout — output pane on the left, command palette sidebar on the right
- Clickable command chips grouped by category (Navigate / Read / Fun)
- Typing autocomplete hint and Tab key completion
- Arrow key command history (↑↓)
- Chip highlight animation when a command runs
- Subtle scanline shimmer effect on the output pane

### 📂 Portfolio Windows
Each section of the portfolio opens as its own draggable window:

| Window | Content |
|---|---|
| `about.me` | Bio, location, goals, languages |
| `skills.json` | Tech skills with animated progress bars + locked cybersecurity panel |
| `experience.log` | Timeline of roles at Prudencia & Somaiya Debating Society |
| `mun.log` | Full MUN conference history with award badges |
| `contact` | Email, LinkedIn, location |

### 🐍 Snake Game
- Playable Snake game in its own window (`snake.exe`)
- 20×20 grid with subtle dot pattern
- Gradient snake body with directional eyes
- Levels up every 5 apples — speed increases each level
- Score / Best / Level HUD
- On-screen directional buttons + keyboard arrow keys
- Space bar to pause
- Game over screen with score and replay button

### 📱 Mobile Responsive
- All windows go fullscreen on screens ≤640px
- Terminal sidebar collapses into a horizontal scrollable chip bar at the bottom
- Prompt shortens to save space
- Skills and MUN grids collapse to single column
- Terminal auto-maximises on boot for mobile users

---

## Terminal Commands

| Command | Description |
|---|---|
| `whoami` | Identity snapshot |
| `about` | Open About window |
| `skills` | Open Skills window |
| `experience` | Open Experience window |
| `mun` | Open Diplomatic Record window |
| `contact` | Open Contact window |
| `projects` | Print project highlights |
| `education` | Print academic background |
| `ls` | List all sections |
| `banner` | Show ASCII art header |
| `sudo hire` | 👀 Easter egg |
| `clear` | Clear the terminal |
| `help` | List all commands |

---

## Tech Stack

This entire portfolio is a **single HTML file** with no external dependencies except Google Fonts.

```
fattesing_portfolio.html
├── HTML        — structure & all window markup
├── CSS         — OS-style theming, animations, responsive layout
└── JavaScript  — terminal engine, window manager, matrix rain, snake game
```

**Fonts used:** JetBrains Mono (terminal), Space Grotesk (UI)

---

## Project Structure (Conceptual)

```
FR_OS v1.0
├── Boot Sequence
├── Desktop
│   ├── Matrix Rain Canvas
│   ├── Taskbar (logo + clock)
│   ├── Desktop Icons
│   └── Windows
│       ├── Terminal (with command palette sidebar)
│       ├── About
│       ├── Skills
│       ├── Experience
│       ├── MUN Record
│       ├── Contact
│       └── Snake Game
└── Mobile Layout (≤640px)
```

---

## About the Developer

**Fattesing Rane** — Second year B.Tech Computer Engineering student at K.J. Somaiya College of Engineering, Mumbai. Fullstack web developer, Co-Head of Technology at Prudencia 2026, and active MUN delegate with awards across multiple conferences. Aspiring cybersecurity specialist.

- 📧 cypher1906@gmail.com
- 💼 [linkedin.com/in/fattesingrane](https://www.linkedin.com/in/fattesingrane)
- 📍 Mumbai, Maharashtra, India

---

## License

This project is personal and not licensed for reuse or redistribution. Feel free to draw inspiration, but please build your own.

---

*Built with 💚 and way too much terminal nostalgia.*