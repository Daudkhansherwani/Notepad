# CS330 – Notepad App (Assignment 3)

**Author:** Daud Khan Sherwani
**Student ID:** 002353155
**Date:** 25 September 2025

A two-screen **Notepad** built with **Kotlin, Jetpack Compose, and Material 3**.
Notes are stored locally using **Room** and exposed through a **Repository + ViewModel** so the UI is fully reactive and survives configuration changes.
Features include search, pin & sort, undo delete, share, relative timestamps, and automatic dark/light theming.

---

##  Features
* **MVVM architecture** – UI is stateless; ViewModel owns all state.
* **Room database** – persistent storage with Flow for reactive updates.
* **Navigation-Compose** – single-activity, multi-screen design.
* **Dark/Light theme** – follows system setting automatically.
* **Extras** – search, pin/favorite, undo delete, share note intent, relative “x minutes ago” timestamps.

---

## 🛠 Build & Run
* **Android Studio**: Ladybug | 2024.2 or newer
* **Gradle Plugin**: 8.x (project default)
* **Kotlin**: 1.9+
* **Min SDK**: 24 **Target/Compile SDK**: 34

HelloCompose/
├─ app/
├─ docs/
│   ├─ app-light-portrait.png
│   ├─ app-dark-portrait.png
│   ├─ app-light-landscape.png
│   ├─ app-dark-landscape.png
│   └─ app-editor.png
    └─ README.md



ca.bishops.cs330.notepad.s002353155
├── data/
│   ├── Note.kt               # Room entity
│   ├── NoteDao.kt            # DAO interface
│   ├── AppDatabase.kt        # Room database singleton
│   └── NoteRepository.kt     # Repository interface & implementation
│
├── vm/
│   └── NotesViewModel.kt     # ViewModel and UI state holder
│
├── UserInterface/
│   ├── NotesListScreen.kt    # Note list + search + pin + undo + share
│   └── NoteEditorScreen.kt   # Editor for creating/updating notes
│
├── MainActivity.kt           # Navigation host, wires ViewModel to UI
└── ui/theme/                 # Material 3 theme (auto dark/light)
