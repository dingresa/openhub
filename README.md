# OpenHub

## Main idea

**OpenHub** is a web platform of classic minigames, created by a developer from Valencia (Spain) as a learning project in web programming.

The idea is to offer a minigame selector that is accessible from any browser and any device, as long as there is an internet connection, with nothing to install. Just open the page, log in and play.

It is a **free and open source** project. All the games are developed by the project's author, and anyone can study them, modify them, improve them, fix bugs or propose changes through *issues* and *pull requests*.

---

## License

- **Code:** [GNU Affero General Public License v3.0 or later](https://www.gnu.org/licenses/agpl-3.0.html) (`AGPL-3.0-or-later`). You can use, study, modify and share the code, but any modified version offered over a network must also publish its source code under the same license.
- **Images and graphic assets:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.en), unless otherwise stated.
- **Name and logo:** the name "OpenHub" and its logo identify the original project. If you make a fork, please use a different name.

The full text of the license is in the [`LICENSE`](LICENSE) file.

---

## Project structure

```
📂 openhub/
├── 📄 index.html
├── 📄 styles.css
├── 📁 images/
│       ├── 📁 logo/
│       ├── 📁 backgrounds/
│       ├── 📁 icons/
│       └── 📁 covers/
├── 📁 menu/
│       └── 📄 menu.html
└── 📁 games/
        ├── 📄 minigames.html
        ├── 📁 snake/
        │       ├── 📄 snake.html
        │       └── 📄 config.js
        ├── 📁 minesweeper/
        │       ├── 📄 minesweeper.html
        │       └── 📄 config.js
        └── 📁 chess/
                ├── 📄 chess.html
                └── 📄 config.js
```

---

## Home page

### Goal

- Present the site to the user with a login screen (test version).
- Apply a look based on gradient colors between purple, blue and black.

### Contents

- **`index.html`:** the main page and the first one the user sees. It contains the login form, where users sign in with a personal account. The account protects the user's data and saves their progress in the games.
- **`styles.css`:** contains the styles of the site, that is, how it looks: colors, gradients, fonts, sizes and layout of the elements. Since it is separate from the content, changing the look of the site does not require touching the other files.

### Structure

```
📂 openhub/
├── 📄 index.html
└── 📄 styles.css
```

---

## Menu page

### Goal

- Let the user select minigames.
- Offer language and profile settings.

### Contents

- **`menu.html`:** the screen shown after logging in. It works as a game catalog in which each game is displayed with:
  - A **cover image**.
  - A **short description** of what the game is about.
  - A **user manual** with the controls and rules.
- From this menu the user can also **change the language** of the site and **edit their profile** (name, account details, etc.).

### Structure

```
📂 openhub/
├── 📄 index.html
├── 📄 styles.css
└── 📁 menu/
        └── 📄 menu.html
```

---

## Images folder

### Goal

- Keep all the graphic resources of the site in a single place, so they stay organized and easy to find.

### Contents

The `images/` folder is divided into four subfolders according to the use of each resource:

- **`logo/`:** the OpenHub logo in different formats and sizes (for example, for the page header or the browser tab).
- **`backgrounds/`:** background images and textures that go with the purple, blue and black gradients.
- **`icons/`:** small interface icons, such as those for language, profile, settings or logout.
- **`covers/`:** a representative image of each minigame (for example, `snake.png`, `minesweeper.png` and `chess.png`), shown in the selection menu.

> **Note for contributors:** images added to the project must be your own or have a license compatible with the repository's license.

### Structure

```
📂 openhub/
├── 📄 index.html
├── 📄 styles.css
├── 📁 menu/
│       └── 📄 menu.html
└── 📁 images/
        ├── 📁 logo/
        ├── 📁 backgrounds/
        ├── 📁 icons/
        └── 📁 covers/
```

---

## Minigames folder

### Goal

- Gather all the project's minigames. Each one has its own folder, with its HTML file and its JS or configuration files.

### Contents

- **`minigames.html`:** a file shared by all the games. It acts as the connection point between the menu and each minigame.
- **Each game's folder** (`snake/`, `minesweeper/`, `chess/`...): contains everything needed for that game to work independently:
  - **HTML file** (`snake.html`, `minesweeper.html`...): the visual structure of the game.
  - **`config.js`:** the programming and settings of the game, such as logic, rules, difficulty and scores. Since everything is in one place, anyone can open a game's folder, understand it and improve it without affecting the rest.
- To **add a new game**, just create a folder with its HTML and JS files, and register it in the menu.

### Structure

```
📂 openhub/
├── 📄 index.html
├── 📄 styles.css
├── 📁 images/
├── 📁 menu/
│       └── 📄 menu.html
└── 📁 games/
        ├── 📄 minigames.html
        ├── 📁 snake/
        │       ├── 📄 snake.html
        │       └── 📄 config.js
        ├── 📁 minesweeper/
        │       ├── 📄 minesweeper.html
        │       └── 📄 config.js
        └── 📁 chess/
                ├── 📄 chess.html
                └── 📄 config.js
```

---

## Contributing

Contributions are welcome: bug fixes, game improvements, new minigames, translations or suggestions.

1. Fork the repository.
2. Create a branch for your change (`git checkout -b my-improvement`).
3. Commit your changes (`git commit -m "Describe your change"`).
4. Push your branch (`git push origin my-improvement`).
5. Open a pull request explaining what you changed and why.

By submitting code, you agree that it will be published under the same license as the project (`AGPL-3.0-or-later`).

To include the license in your files, add this line at the top of every code file:

```
// SPDX-License-Identifier: AGPL-3.0-or-later
```

---

## Privacy and security

- User accounts and save data are **not part of the repository**.
- Never upload passwords, access keys or databases to the repository.
- If you find a security issue, please report it privately to the author before making it public.

---

## Author

Project created by a developer from Valencia, eager to keep learning web programming.